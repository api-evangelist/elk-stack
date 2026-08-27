---
name: elk-stack-snapshot-before-destructive-change
description: Take and verify a snapshot before any destructive Elasticsearch operation, then restore from it if the change goes wrong — the only reversal path Elastic offers for a deleted index.
api: elk-stack:elasticsearch-api
operations:
  - snapshot-get-repository
  - snapshot-create
  - snapshot-get
  - snapshot-status
  - indices-close
  - indices-delete
  - snapshot-restore
  - indices-open
  - cat-indices
generated: '2026-08-27'
method: generated
source: openapi/elk-stack-elasticsearch-openapi.json
---

# Snapshot before a destructive change

**Read this before running any of `indices-delete`, `delete-by-query`, or a mapping-breaking
reindex.** Per `conventions/elk-stack-conventions.yml`, `delete-by-query` has **no reversal at all**,
and `indices-delete` is reversible only from a snapshot that already existed *before* the delete.
Elastic publishes no undo window because it does not control one — retention is set by the
customer's own SLM policy.

## 1. Confirm a repository exists

`snapshot-get-repository` — `GET /_snapshot`. With no registered repository you cannot snapshot, and
therefore have no reversal path. **Stop here if this returns empty.** Do not proceed to the
destructive step; report the absence instead.

## 2. Take the snapshot

`snapshot-create` — `PUT /_snapshot/{repository}/{snapshot}` with `?wait_for_completion=true` for a
small index, or without it and then poll.

Restrict `indices` in the body to what you are about to change. Name the snapshot for the change you
are about to make, not the date alone — you may be reading this list under pressure later.

## 3. Verify it before you rely on it

`snapshot-get` — `GET /_snapshot/{repository}/{snapshot}`. Require `state: "SUCCESS"` and
`shards.failed: 0`.

A `PARTIAL` snapshot is not a backup. If it is not `SUCCESS`, do not proceed with the destructive
step.

## 4. Prefer closing to deleting

`indices-close` — `POST /{index}/_close` takes an index offline without destroying it, and
`indices-open` — `POST /{index}/_open` — brings it straight back. This is the one **fully symmetric**
reversal in the whole Elasticsearch surface, with no window and no snapshot dependency.

If closing achieves the goal, close. Only delete when you actually need the storage back.

## 5. The destructive step

`indices-delete` — `DELETE /{index}`. Immediate and unrecoverable except from step 2.

Never send a wildcard here. `DELETE /logs-*` will delete every matching index in one call.

## 6. Restore if it went wrong

`snapshot-restore` — `POST /_snapshot/{repository}/{snapshot}/_restore`.

The target index must not currently exist and must not be open. Use `rename_pattern` and
`rename_replacement` to restore alongside the live data rather than over it — restoring to a new name
first, verifying with `cat-indices`, and only then swapping an alias is far safer than restoring in
place.

## Errors

- `400 snapshot_restore_exception` — the index exists and is open. Close or rename it.
- `404` — wrong repository or snapshot name.
- `409` — a snapshot is already running in this repository. Wait; do not force.
