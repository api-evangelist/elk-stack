# Retired scaffold specifications

The eight OpenAPI files in this directory were **hand-authored scaffolds**, not
contracts Elastic published. They were written into this repo by an earlier
bulk sweep: one 19-operation `elk-stack-openapi.yml` describing a handful of
Elasticsearch endpoints against `http://localhost:9200`, plus the seven
per-tag files a refine pass split out of it.

They were retired on **2026-08-27**, when the enrichment pipeline located
Elastic's own machine-readable contracts and harvested them verbatim into
`../openapi/`:

| File | Source | Operations |
|---|---|---|
| `elk-stack-elasticsearch-openapi.json` | `elastic/elasticsearch-specification` → `output/openapi/elasticsearch-openapi.json` | 845 |
| `elk-stack-kibana-openapi.yaml` | `elastic/kibana` → `oas_docs/output/kibana.yaml` | 731 |
| `elk-stack-elastic-cloud-swagger.json` | live at `https://api.elastic-cloud.com/api/v1/api-docs/swagger.json` | 297 |

Nothing in `apis.yml` points at this directory any more. These files are kept
only so the record of what was previously published under this provider's name
is not lost. **Do not re-wire them** — every operationId in them is invented,
and Elastic's real specs use a different naming convention entirely
(`cat-indices`, `cluster-health`, `indices-get-mapping`, not `catIndices`,
`getClusterHealth`, `getIndexMapping`).

The Postman and OpenCollection files still in `../collections/` were generated
from these scaffolds and share the same defect. They are not referenced from
`apis.yml`.
