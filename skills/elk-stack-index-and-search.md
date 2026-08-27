---
name: elk-stack-index-and-search
description: Create an Elasticsearch index with an explicit mapping, bulk-load documents into it idempotently, and read them back with a query — the base flow every other Elasticsearch task builds on.
api: elk-stack:elasticsearch-api
operations:
  - indices-exists
  - indices-create
  - indices-get-mapping
  - bulk
  - index
  - indices-refresh
  - search
  - count
generated: '2026-08-27'
method: generated
source: openapi/elk-stack-elasticsearch-openapi.json
---

# Index and search documents in Elasticsearch

Base URL is the customer's own cluster (`https://{elasticsearch_endpoint}`). Authenticate with
`Authorization: ApiKey <base64(id:api_key)>`. There is no Elastic-hosted endpoint for this API.

## 1. Check whether the index already exists

`indices-exists` — `HEAD /{index}`. A `200` means it exists, `404` means it does not.
Do this first: `indices-create` on an existing index returns `400
resource_already_exists_exception`, which is not the same as success.

## 2. Create the index with an explicit mapping

`indices-create` — `PUT /{index}`. Send `mappings.properties` in the body.

Do not skip the mapping and rely on dynamic mapping for anything you intend to keep. Elasticsearch
infers a field's type from the first document it sees, and **a field's type cannot be changed once
set** — correcting it means reindexing into a new index. Getting the mapping right here is the single
highest-leverage decision in this flow.

## 3. Load documents

For more than one document use `bulk` — `POST /_bulk` — with the NDJSON action/source line pairs.

**Idempotency (see `conventions/elk-stack-conventions.yml`).** There is no `Idempotency-Key` header
anywhere on this API. Retry-safety comes from the document id:

- `index` — `PUT /{index}/_doc/{id}` with an id **you** choose is idempotent. Replaying it converges.
- `POST /{index}/_doc` with **no** id is **not** idempotent — Elasticsearch generates a new id each
  call, so a retry after a timeout creates a duplicate.

Always supply your own `_id` (a natural key, or a hash of the source) when a retry is possible.

Inside a bulk body, use `"index"` to upsert and `"create"` to fail on an existing id. A bulk request
can return `200` while individual items failed — **read `items[].error`; do not trust the HTTP status
alone.** This is the most common silent data-loss bug against this API.

## 4. Make the writes visible

`indices-refresh` — `POST /_refresh`. Elasticsearch is near-real-time, not real-time: a document is
searchable after the next refresh (1s by default), not on write acknowledgement. If you search
immediately after writing and get nothing, this is why. Use `?refresh=wait_for` on the write instead
of forcing a refresh in production — a forced refresh on every write will wreck indexing throughput.

## 5. Query

`search` — `GET|POST /{index}/_search`. `count` — `POST /{index}/_count` when you only need the number.

Use `filter_path` to prune the response to the fields you actually need; on a large result set it is
the cheapest lever you have on response size.

## Paging

- `from` + `size` only up to `index.max_result_window` (10,000 by default). Past that it errors.
- Beyond that, `search_after` with a sort, ideally inside a point-in-time (`open-point-in-time` →
  page with `search_after` → `close-point-in-time`) so the view cannot shift under you.
- Do not use `scroll` for new work; Elastic recommends `search_after` + PIT instead.

## Errors

No `application/problem+json`. Elasticsearch returns `{ "error": { "type", "reason", "root_cause" },
"status" }`. See `errors/elk-stack-problem-types.yml`.

- `409 version_conflict_engine_exception` — concurrent write. Re-read and retry; this one is retryable.
- `429` — write queue rejection (`es_rejected_execution_exception`). Back off exponentially. There is
  no `Retry-After` header and no rate-limit header to read a budget from.
- `400` — malformed request or mapping conflict. Retrying unchanged will fail identically.
