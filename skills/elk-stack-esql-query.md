---
name: elk-stack-esql-query
description: Run an ES|QL query against Elasticsearch, synchronously for fast queries and asynchronously with polling and cancellation for long ones — the query path an agent should prefer over hand-built Query DSL.
api: elk-stack:elasticsearch-api
operations:
  - esql-query
  - esql-async-query
  - esql-async-query-get
  - esql-async-query-stop
  - esql-async-query-delete
  - indices-get-mapping
generated: '2026-08-27'
method: generated
source: openapi/elk-stack-elasticsearch-openapi.json
---

# Run an ES|QL query

ES|QL is a piped query language. For an agent it is usually a better target than Query DSL: the query
is one string rather than a nested JSON tree, and the response is columnar, so the shape is
predictable without knowing the mapping in advance.

## 1. Learn the fields first

`indices-get-mapping` — `GET /{index}/_mapping`. ES|QL will fail on a field that does not exist rather
than silently returning nothing, so read the mapping before composing the query. Do not guess field
names.

## 2. Short queries: run them synchronously

`esql-query` — `POST /_query`.

```
{ "query": "FROM logs-* | WHERE @timestamp > NOW() - 1 hour | STATS count = COUNT(*) BY host.name | SORT count DESC | LIMIT 20" }
```

The response is `{ "columns": [{name, type}], "values": [[...]] }` — column metadata and rows, not
nested `_source` documents.

Use the `format` parameter (`json`, `csv`, `tsv`, `txt`, `arrow`) when a non-JSON shape is cheaper to
consume.

**Always end with an explicit `LIMIT`.** ES|QL applies a default limit, but an unbounded query over a
wide time range is the fastest way to exhaust both the cluster's memory and your own context window.

## 3. Long queries: go asynchronous

`esql-async-query` — `POST /_query/async`, with `wait_for_completion_timeout` (for example `10s`).

- If it finishes inside the timeout you get results directly and `is_running: false`.
- If not you get an `id` and `is_running: true`.

Then poll `esql-async-query-get` — `GET /_query/async/{id}` — until `is_running` is `false`.

Back off between polls. There is no rate-limit header telling you how often you may ask.

## 4. Stop or discard

- `esql-async-query-stop` — `POST /_query/async/{id}/stop` returns the results computed **so far** and
  stops the query. Prefer this to abandoning a query: it frees cluster resources and still gives you
  partial data.
- `esql-async-query-delete` — `DELETE /_query/async/{id}` discards a finished query's stored results.

## Reversibility

Read-only. Nothing in this flow writes, so there is nothing to reverse. This is the safest surface on
the whole API to give an agent, and where an unattended agent should be confined by default.

## Errors

- `400` with a parse error — the ES|QL text is wrong. Fix the query; never retry it unchanged.
- `400` `verification_exception` — an unknown field or column. Go back to step 1.
- `429` — cluster under load. Back off; consider the async path instead.
