# Elastic Stack (ELK Stack) (elk-stack)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

The Elastic Stack (formerly known as the ELK Stack) is the collection of open-source products from Elastic — Elasticsearch, Logstash, Kibana, and Beats/Elastic Agent — designed for taking data from any source, in any format, and searching, analyzing, and visualizing it in real time. It is widely used for log management, observability, security analytics (SIEM), and increasingly as a vector database and retrieval layer for RAG and agentic AI applications. Elastic publishes machine-readable OpenAPI descriptions for all three of its programmable surfaces: the Elasticsearch REST API, the Kibana APIs, and the Elastic Cloud control-plane API. The stack is deployment-hosted — self-managed, Elastic Cloud Hosted, or Elastic Cloud Serverless — so the Elasticsearch and Kibana base URLs are always specific to the customer's own cluster or project.

**Website:** [https://www.elastic.co/elastic-stack/](https://www.elastic.co/elastic-stack/)

## Scope

- **Type:** Index
- **Position:** Consumer
- **Access:** 3rd-Party

## Tags

- Analytics
- Logging
- Monitoring
- Observability
- Search
- Security
- Vector Database
- SIEM
- Machine Learning

## Timestamps

- **Created:** 2024-01-01
- **Modified:** 2026-08-27

## APIs

### Elasticsearch REST API

The Elasticsearch REST API is the programmable surface of the distributed search, analytics and vector engine at the heart of the Elastic Stack — 581 paths and 845 operations covering indices, documents, search, ES|QL, inference, machine learning, security, snapshots, ingest pipelines, connectors, transforms, ILM/SLM and cluster administration. Elastic publishes it as OpenAPI 3.0.3 generated from the canonical elasticsearch-specification repository.

- **Human URL:** [https://www.elastic.co/docs/api/doc/elasticsearch/](https://www.elastic.co/docs/api/doc/elasticsearch/)
- **Base URL:** `https://{elasticsearch_endpoint}`

#### Tags

- Search
- Indices
- Documents
- Machine Learning
- Vector Database

#### Properties

- [OpenAPI](openapi/elk-stack-elasticsearch-openapi.json)
- [Overlay](overlays/elk-stack-elasticsearch-overlay.yaml)
- [Documentation](https://www.elastic.co/docs/reference/elasticsearch)
- [API Reference](https://www.elastic.co/docs/api/doc/elasticsearch/)
- [Source Code](https://github.com/elastic/elasticsearch-specification)

### Kibana API

The Kibana APIs expose the visualization, alerting, cases, Fleet, machine learning, Elastic Security and Elastic Observability surfaces that sit on top of Elasticsearch — 531 paths and 731 operations, including the Agent Builder MCP endpoint that turns a Kibana deployment into an MCP server. Elastic publishes it as OpenAPI 3.0.3 from the kibana repository.

- **Human URL:** [https://www.elastic.co/docs/api/doc/kibana/](https://www.elastic.co/docs/api/doc/kibana/)
- **Base URL:** `https://{kibana_url}`

#### Tags

- Analytics
- Dashboard
- Visualization
- Alerting
- Fleet
- Security

#### Properties

- [OpenAPI](openapi/elk-stack-kibana-openapi.yaml)
- [Overlay](overlays/elk-stack-kibana-overlay.yaml)
- [Documentation](https://www.elastic.co/docs/reference/kibana)
- [API Reference](https://www.elastic.co/docs/api/doc/kibana/)
- [Source Code](https://github.com/elastic/kibana)
- [MCP Server](mcp/elk-stack-mcp.yml)
- [Tool Crosswalk](mcp/elk-stack-tool-crosswalk.yml)

### Elastic Cloud API

The Elastic Cloud control-plane API creates, scales, upgrades and deletes Elasticsearch and Kibana deployments, and manages accounts, organizations, IAM, traffic filters, extensions, deployment templates and billing costs — 190 paths and 297 operations, published as Swagger 2.0 straight from the live control plane at api.elastic-cloud.com.

- **Human URL:** [https://www.elastic.co/docs/api/doc/cloud/](https://www.elastic.co/docs/api/doc/cloud/)
- **Base URL:** `https://api.elastic-cloud.com/api/v1`

#### Tags

- Cloud
- Deployments
- Provisioning
- Billing
- IAM

#### Properties

- [Swagger](openapi/elk-stack-elastic-cloud-swagger.json)
- [Overlay](overlays/elk-stack-elastic-cloud-overlay.yaml)
- [Documentation](https://www.elastic.co/docs/deploy-manage/deploy/elastic-cloud)
- [API Reference](https://www.elastic.co/docs/api/doc/cloud/)

## Common Properties

- [Website](https://www.elastic.co/elastic-stack/)
- [Developer Portal](https://www.elastic.co/docs)
- [Documentation](https://www.elastic.co/docs)
- [API Reference](https://www.elastic.co/docs/api)
- [Getting Started](https://www.elastic.co/docs/get-started)
- [Support](https://www.elastic.co/support)
- [Help Center](https://discuss.elastic.co/)
- [Blog](https://www.elastic.co/blog/)
- [GitHub Organization](https://github.com/elastic)
- [Pricing](https://www.elastic.co/pricing/)
- [Sign Up](https://www.elastic.co/cloud/elasticsearch-service/signup)
- [Terms of Service](https://www.elastic.co/legal/terms-of-use)
- [Privacy Policy](https://www.elastic.co/legal/privacy-statement)
- [LinkedIn](https://www.linkedin.com/company/elastic-co)
- [Integrations](https://www.elastic.co/integrations)
- [Status Page](https://status.elastic.co/)
- [llms.txt](llms/elk-stack-llms.txt)
- [Packages](packages/elk-stack-packages.yml)
- [SDKs](packages/elk-stack-packages.yml)
- [CLI](cli/elk-stack-cli.yml)
- [Components](components/elk-stack-components.yml)
- [Well-Known](well-known/elk-stack-well-known.yml)
- [security.txt](well-known/elk-stack-security.txt)
- [MCP Server](mcp/elk-stack-mcp.yml)
- [Tool Crosswalk](mcp/elk-stack-tool-crosswalk.yml)
- [Agent Skills](skills/_index.yml)
- [Webhooks](asyncapi/elk-stack-webhooks.yml)
- [Conformance](conformance/elk-stack-conformance.yml)
- [Compliance](security/elk-stack-trust-center.yml)
- [Error Catalog](errors/elk-stack-problem-types.yml)
- [Lifecycle](lifecycle/elk-stack-lifecycle.yml)
- [Deprecation](lifecycle/elk-stack-lifecycle.yml)
- [Change Log](changelog/elk-stack-changelog.yml)
- [Conventions](conventions/elk-stack-conventions.yml)
- [Idempotency](conventions/elk-stack-conventions.yml)
- [Data Model](data-model/elk-stack-data-model.yml)
- [Sandbox](sandbox/elk-stack-sandbox.yml)
- [Plans](plans/elk-stack-plans-pricing.yml)
- [Rate Limits](rate-limits/elk-stack-rate-limits.yml)
- [Authentication](authentication/elk-stack-authentication.yml)
- [Domain Security](security/elk-stack-domain-security.yml)
- [Trust Center](security/elk-stack-trust-center.yml)
- [Vulnerability Disclosure](security/elk-stack-vulnerability-disclosure.yml)
- [Security](security/elk-stack-vulnerability-disclosure.yml)
- [Agentic Access](agentic-access/elk-stack-agentic-access.yml)
- [FinOps](finops/elk-stack-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
