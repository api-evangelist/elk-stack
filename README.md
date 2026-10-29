# Elastic Stack

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

**Areas:** Analytics · Logging · Monitoring · Observability · Search · Security · Vector Search · SIEM · Machine Learning

## Elastic Stack on APIs.io

Everything profiled for Elastic Stack is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/elk-stack/](https://apis.io/providers/elk-stack/)** — or go straight to one of the APIs or properties below.

### APIs (133)

- [Elastic Cloud API](https://apis.io/apis/elk-stack/elastic-cloud-api/) — The Elastic Cloud control-plane API creates, scales, upgrades and deletes Elasticsearch and Kibana deployments, and manages accounts, organizations, IAM,…
- [Elastic Stack (ELK Stack) Accounts API](https://apis.io/apis/elk-stack/elk-stack-accounts-api/) — The Accounts API from Elastic Stack (ELK Stack) — 1 operation(s) for accounts.
- [Elastic Stack (ELK Stack) Actions API](https://apis.io/apis/elk-stack/elk-stack-actions-api/) — The Actions API from Elastic Stack (ELK Stack) — 1 operation(s) for actions.
- [Elastic Stack (ELK Stack) agent builder API](https://apis.io/apis/elk-stack/elk-stack-agent-builder-api/) — Agent Builder is a set of AI-powered capabilities for developing and interacting with agents that work with your Elasticsearch data. Most users will…
- [Elastic Stack (ELK Stack) Alerting API](https://apis.io/apis/elk-stack/elk-stack-alerting-api/) — Alerting enables you to define rules, which detect complex conditions within your data. When a condition is met, the rule tracks it as an alert and runs the…
- [Elastic Stack (ELK Stack) Alerting V2 API](https://apis.io/apis/elk-stack/elk-stack-alerting-v2-api/) — Alerting V2 is an ES|QL-first alerting API for managing rules, alert actions, and action policies. Use these endpoints to create and manage detection rules,…
- [Elastic Stack (ELK Stack) Analytics API](https://apis.io/apis/elk-stack/elk-stack-analytics-api/) — The analytics API from Elastic Stack (ELK Stack) — 3 operation(s) for analytics.
- [Elastic Stack (ELK Stack) APM agent configuration API](https://apis.io/apis/elk-stack/elk-stack-apm-agent-configuration-api/) — Adjust APM agent configuration without need to redeploy your application.
- [Elastic Stack (ELK Stack) APM agent keys API](https://apis.io/apis/elk-stack/elk-stack-apm-agent-keys-api/) — Configure APM agent keys to authorize requests from APM agents to the APM Server.
- [Elastic Stack (ELK Stack) APM annotations API](https://apis.io/apis/elk-stack/elk-stack-apm-annotations-api/) — Annotate visualizations in the APM app with significant events. Annotations enable you to easily see how events are impacting the performance of your…
- [Elastic Stack (ELK Stack) APM server schema API](https://apis.io/apis/elk-stack/elk-stack-apm-server-schema-api/) — Create APM fleet server schema.
- [Elastic Stack (ELK Stack) APM sourcemaps API](https://apis.io/apis/elk-stack/elk-stack-apm-sourcemaps-api/) — Configure APM source maps. A source map allows minified files to be mapped back to original source code--allowing you to maintain the speed advantage of…
- [Elastic Stack (ELK Stack) Authentication API](https://apis.io/apis/elk-stack/elk-stack-authentication-api/) — The Authentication API from Elastic Stack (ELK Stack) — 12 operation(s) for authentication.
- [Elastic Stack (ELK Stack) Billing Costs Analysis API](https://apis.io/apis/elk-stack/elk-stack-billingcostsanalysis-api/) — The BillingCostsAnalysis API from Elastic Stack (ELK Stack) — 6 operation(s) for billingcostsanalysis.
- [Elastic Stack (ELK Stack) Cases API](https://apis.io/apis/elk-stack/elk-stack-cases-api/) — Cases are used to open and track issues. You can add assignees and tags to your cases, set their severity and status, and add alerts, comments, and…
- [Elastic Stack (ELK Stack) Cat API](https://apis.io/apis/elk-stack/elk-stack-cat-api/) — The cat API from Elastic Stack (ELK Stack) — 45 operation(s) for cat.
- [Elastic Stack (ELK Stack) Ccr API](https://apis.io/apis/elk-stack/elk-stack-ccr-api/) — The ccr API from Elastic Stack (ELK Stack) — 12 operation(s) for ccr.
- [Elastic Stack (ELK Stack) Cluster API](https://apis.io/apis/elk-stack/elk-stack-cluster-api/) — The cluster API from Elastic Stack (ELK Stack) — 35 operation(s) for cluster.
- [Elastic Stack (ELK Stack) Comments API](https://apis.io/apis/elk-stack/elk-stack-comments-api/) — The Comments API from Elastic Stack (ELK Stack) — 2 operation(s) for comments.
- [Elastic Stack (ELK Stack) Connector API](https://apis.io/apis/elk-stack/elk-stack-connector-api/) — The connector API from Elastic Stack (ELK Stack) — 24 operation(s) for connector.
- [Elastic Stack (ELK Stack) Connectors API](https://apis.io/apis/elk-stack/elk-stack-connectors-api/) — Connectors provide a central place to store connection information for services and integrations with Elastic or third party systems. Alerting rules can use…
- [Elastic Stack (ELK Stack) Dashboards API](https://apis.io/apis/elk-stack/elk-stack-dashboards-api/) — > This documentation is temporarily hosted at a separate location. > > **[View the full Dashboards API reference…
- [Elastic Stack (ELK Stack) data stream API](https://apis.io/apis/elk-stack/elk-stack-data-stream-api/) — The data stream API from Elastic Stack (ELK Stack) — 14 operation(s) for data stream.
- [Elastic Stack (ELK Stack) Data streams API](https://apis.io/apis/elk-stack/elk-stack-data-streams-api/) — Data stream APIs enable you to manage data streams, which are collections of indices that share the same index template and are managed as a single unit for…
- [Elastic Stack (ELK Stack) data views API](https://apis.io/apis/elk-stack/elk-stack-data-views-api/) — Data view APIs enable you to manage data views, formerly known as Kibana index patterns.
- [Elastic Stack (ELK Stack) Deployments API](https://apis.io/apis/elk-stack/elk-stack-deployments-api/) — The Deployments API from Elastic Stack (ELK Stack) — 58 operation(s) for deployments.
- [Elastic Stack (ELK Stack) Deployments Traffic Filter API](https://apis.io/apis/elk-stack/elk-stack-deploymentstrafficfilter-api/) — The DeploymentsTrafficFilter API from Elastic Stack (ELK Stack) — 8 operation(s) for deploymentstrafficfilter.
- [Elastic Stack (ELK Stack) Deployment Templates API](https://apis.io/apis/elk-stack/elk-stack-deploymenttemplates-api/) — The DeploymentTemplates API from Elastic Stack (ELK Stack) — 2 operation(s) for deploymenttemplates.
- [Elastic Stack (ELK Stack) Document API](https://apis.io/apis/elk-stack/elk-stack-document-api/) — The document API from Elastic Stack (ELK Stack) — 19 operation(s) for document.
- [Elastic Stack (ELK Stack) Elastic Agent actions API](https://apis.io/apis/elk-stack/elk-stack-elastic-agent-actions-api/) — Elastic Agent actions APIs enable you to manage actions performed on Elastic Agents, including agent reassignment, diagnostics collection, enrollment…
- [Elastic Stack (ELK Stack) Elastic Agent binary download sources API](https://apis.io/apis/elk-stack/elk-stack-elastic-agent-binary-download-sources-api/) — Elastic Agent binary download sources APIs enable you to manage download sources for Elastic Agent binaries, including creating, updating, and deleting…
- [Elastic Stack (ELK Stack) Elastic Agent policies API](https://apis.io/apis/elk-stack/elk-stack-elastic-agent-policies-api/) — Elastic Agent policies APIs enable you to manage agent policies, including creating, updating, and deleting policies, as well as to retrieve agent policy…
- [Elastic Stack (ELK Stack) Elastic Agent status API](https://apis.io/apis/elk-stack/elk-stack-elastic-agent-status-api/) — Enables you to retrieve status information about Elastic Agents, including health summaries and operational status.
- [Elastic Stack (ELK Stack) Elastic Agents API](https://apis.io/apis/elk-stack/elk-stack-elastic-agents-api/) — Elastic Agents APIs enable you to manage Elastic Agents, including retrieving agent information, managing agent lifecycle, handling file uploads, and…
- [Elastic Stack (ELK Stack) Elastic Package Manager (EPM) API](https://apis.io/apis/elk-stack/elk-stack-elastic-package-manager-epm-api/) — Elastic Package Manager (EPM) APIs enable you to manage packages and integrations, including installing, updating, and uninstalling packages, managing…
- [Elastic Stack (ELK Stack) Enrich API](https://apis.io/apis/elk-stack/elk-stack-enrich-api/) — The enrich API from Elastic Stack (ELK Stack) — 4 operation(s) for enrich.
- [Elastic Stack (ELK Stack) Eql API](https://apis.io/apis/elk-stack/elk-stack-eql-api/) — The eql API from Elastic Stack (ELK Stack) — 3 operation(s) for eql.
- [Elastic Stack (ELK Stack) Esql API](https://apis.io/apis/elk-stack/elk-stack-esql-api/) — The esql API from Elastic Stack (ELK Stack) — 12 operation(s) for esql.
- [Elastic Stack (ELK Stack) Extensions API](https://apis.io/apis/elk-stack/elk-stack-extensions-api/) — The Extensions API from Elastic Stack (ELK Stack) — 2 operation(s) for extensions.
- [Elastic Stack (ELK Stack) Features API](https://apis.io/apis/elk-stack/elk-stack-features-api/) — The features API from Elastic Stack (ELK Stack) — 2 operation(s) for features.
- [Elastic Stack (ELK Stack) Fleet agentless policies API](https://apis.io/apis/elk-stack/elk-stack-fleet-agentless-policies-api/) — The Fleet agentless policies API from Elastic Stack (ELK Stack) — 4 operation(s) for fleet agentless policies.
- [Elastic Stack (ELK Stack) Fleet API](https://apis.io/apis/elk-stack/elk-stack-fleet-api/) — The fleet API from Elastic Stack (ELK Stack) — 4 operation(s) for fleet.
- [Elastic Stack (ELK Stack) Fleet cloud connectors API](https://apis.io/apis/elk-stack/elk-stack-fleet-cloud-connectors-api/) — Fleet cloud connectors APIs enable you to manage Fleet cloud connectors, including creating, updating, and deleting cloud connector configurations for Fleet…
- [Elastic Stack (ELK Stack) Fleet enrollment API keys API](https://apis.io/apis/elk-stack/elk-stack-fleet-enrollment-api-keys-api/) — Fleet enrollment API keys APIs enable you to manage enrollment API keys for Fleet, including creating, retrieving, and revoking API keys used for agent…
- [Elastic Stack (ELK Stack) Fleet internals API](https://apis.io/apis/elk-stack/elk-stack-fleet-internals-api/) — Fleet internals APIs enable you to manage Fleet internal operations, including checking permissions, monitoring Fleet Server health, managing settings, and…
- [Elastic Stack (ELK Stack) Fleet managed integrations API](https://apis.io/apis/elk-stack/elk-stack-fleet-managed-integrations-api/) — The Fleet managed integrations API from Elastic Stack (ELK Stack) — 4 operation(s) for fleet managed integrations.
- [Elastic Stack (ELK Stack) Fleet outputs API](https://apis.io/apis/elk-stack/elk-stack-fleet-outputs-api/) — Fleet outputs APIs enable you to manage Fleet outputs, including creating, updating, and deleting output configurations, generating Logstash API keys, and…
- [Elastic Stack (ELK Stack) Fleet package policies API](https://apis.io/apis/elk-stack/elk-stack-fleet-package-policies-api/) — Fleet package policies APIs enable you to manage Fleet package policies, including creating, updating, and deleting policies, performing bulk operations,…
- [Elastic Stack (ELK Stack) Fleet proxies API](https://apis.io/apis/elk-stack/elk-stack-fleet-proxies-api/) — Fleet proxies APIs enable you to manage Fleet proxies, including creating, updating, and deleting proxy configurations for Fleet agent communication.
- [Elastic Stack (ELK Stack) Fleet remote synced integrations API](https://apis.io/apis/elk-stack/elk-stack-fleet-remote-synced-integrations-api/) — Use the Fleet remote synced integrations API to check the status of the automatic integrations synchronization on a remote cluster: * Use the…
- [Elastic Stack (ELK Stack) Fleet Server hosts API](https://apis.io/apis/elk-stack/elk-stack-fleet-server-hosts-api/) — Fleet Server hosts APIs enable you to manage Fleet Server hosts, including creating, updating, and deleting Fleet Server host configurations.
- [Elastic Stack (ELK Stack) Fleet service tokens API](https://apis.io/apis/elk-stack/elk-stack-fleet-service-tokens-api/) — Enables you to create tokens for Fleet service authentication and authorization.
- [Elastic Stack (ELK Stack) Fleet uninstall tokens API](https://apis.io/apis/elk-stack/elk-stack-fleet-uninstall-tokens-api/) — Fleet uninstall tokens APIs enable you to manage Fleet uninstall tokens, including retrieving metadata and decrypted tokens for agent uninstallation.
- [Elastic Stack (ELK Stack) Graph API](https://apis.io/apis/elk-stack/elk-stack-graph-api/) — The graph API from Elastic Stack (ELK Stack) — 1 operation(s) for graph.
- [Elastic Stack (ELK Stack) Health Report API](https://apis.io/apis/elk-stack/elk-stack-health-report-api/) — The health_report API from Elastic Stack (ELK Stack) — 2 operation(s) for health_report.
- [Elastic Stack (ELK Stack) Iam Service API](https://apis.io/apis/elk-stack/elk-stack-iamservice-api/) — The IamService API from Elastic Stack (ELK Stack) — 31 operation(s) for iamservice.
- [Elastic Stack (ELK Stack) Ilm API](https://apis.io/apis/elk-stack/elk-stack-ilm-api/) — The ilm API from Elastic Stack (ELK Stack) — 10 operation(s) for ilm.
- [Elastic Stack (ELK Stack) Indices API](https://apis.io/apis/elk-stack/elk-stack-indices-api/) — The indices API from Elastic Stack (ELK Stack) — 63 operation(s) for indices.
- [Elastic Stack (ELK Stack) Inference API](https://apis.io/apis/elk-stack/elk-stack-inference-api/) — The inference API from Elastic Stack (ELK Stack) — 40 operation(s) for inference.
- [Elastic Stack (ELK Stack) Info API](https://apis.io/apis/elk-stack/elk-stack-info-api/) — The info API from Elastic Stack (ELK Stack) — 1 operation(s) for info.
- [Elastic Stack (ELK Stack) Ingest API](https://apis.io/apis/elk-stack/elk-stack-ingest-api/) — The ingest API from Elastic Stack (ELK Stack) — 12 operation(s) for ingest.
- [Elastic Stack (ELK Stack) License API](https://apis.io/apis/elk-stack/elk-stack-license-api/) — The license API from Elastic Stack (ELK Stack) — 5 operation(s) for license.
- [Elastic Stack (ELK Stack) Links API](https://apis.io/apis/elk-stack/elk-stack-links-api/) — The Links API from Elastic Stack (ELK Stack) — 2 operation(s) for links.
- [Elastic Stack (ELK Stack) Logstash API](https://apis.io/apis/elk-stack/elk-stack-logstash-api/) — The logstash API from Elastic Stack (ELK Stack) — 4 operation(s) for logstash.
- [Elastic Stack (ELK Stack) Maintenance Window API](https://apis.io/apis/elk-stack/elk-stack-maintenance-window-api/) — You can schedule single or recurring maintenance windows to temporarily reduce rule notifications. For example, a maintenance window prevents false alarms…
- [Elastic Stack (ELK Stack) Markdowns API](https://apis.io/apis/elk-stack/elk-stack-markdowns-api/) — The Markdowns API from Elastic Stack (ELK Stack) — 2 operation(s) for markdowns.
- [Elastic Stack (ELK Stack) Message Signing Service API](https://apis.io/apis/elk-stack/elk-stack-message-signing-service-api/) — Enables you to rotate message signing key pairs for secure Fleet communication.
- [Elastic Stack (ELK Stack) Migration API](https://apis.io/apis/elk-stack/elk-stack-migration-api/) — The migration API from Elastic Stack (ELK Stack) — 7 operation(s) for migration.
- [Elastic Stack (ELK Stack) ml anomaly API](https://apis.io/apis/elk-stack/elk-stack-ml-anomaly-api/) — The ml anomaly API from Elastic Stack (ELK Stack) — 45 operation(s) for ml anomaly.
- [Elastic Stack (ELK Stack) Ml API](https://apis.io/apis/elk-stack/elk-stack-ml-api/) — The ml API from Elastic Stack (ELK Stack) — 7 operation(s) for ml.
- [Elastic Stack (ELK Stack) ml data frame API](https://apis.io/apis/elk-stack/elk-stack-ml-data-frame-api/) — The ml data frame API from Elastic Stack (ELK Stack) — 12 operation(s) for ml data frame.
- [Elastic Stack (ELK Stack) ml trained model API](https://apis.io/apis/elk-stack/elk-stack-ml-trained-model-api/) — The ml trained model API from Elastic Stack (ELK Stack) — 12 operation(s) for ml trained model.
- [Elastic Stack (ELK Stack) Observability AI Assistant API](https://apis.io/apis/elk-stack/elk-stack-observability-ai-assistant-api/) — Interact with the Observability AI Assistant resources.
- [Elastic Stack (ELK Stack) Organizations API](https://apis.io/apis/elk-stack/elk-stack-organizations-api/) — The Organizations API from Elastic Stack (ELK Stack) — 15 operation(s) for organizations.
- [Elastic Stack (ELK Stack) Platform API](https://apis.io/apis/elk-stack/elk-stack-platform-api/) — The Platform API from Elastic Stack (ELK Stack) — 3 operation(s) for platform.
- [Elastic Stack (ELK Stack) Platform Configuration Instances API](https://apis.io/apis/elk-stack/elk-stack-platformconfigurationinstances-api/) — The PlatformConfigurationInstances API from Elastic Stack (ELK Stack) — 2 operation(s) for platformconfigurationinstances.
- [Elastic Stack (ELK Stack) Platform Configuration Networking API](https://apis.io/apis/elk-stack/elk-stack-platformconfigurationnetworking-api/) — The PlatformConfigurationNetworking API from Elastic Stack (ELK Stack) — 2 operation(s) for platformconfigurationnetworking.
- [Elastic Stack (ELK Stack) Platform Configuration Security API](https://apis.io/apis/elk-stack/elk-stack-platformconfigurationsecurity-api/) — The PlatformConfigurationSecurity API from Elastic Stack (ELK Stack) — 12 operation(s) for platformconfigurationsecurity.
- [Elastic Stack (ELK Stack) Platform Configuration Snapshots API](https://apis.io/apis/elk-stack/elk-stack-platformconfigurationsnapshots-api/) — The PlatformConfigurationSnapshots API from Elastic Stack (ELK Stack) — 2 operation(s) for platformconfigurationsnapshots.
- [Elastic Stack (ELK Stack) Platform Configuration Templates API](https://apis.io/apis/elk-stack/elk-stack-platformconfigurationtemplates-api/) — The PlatformConfigurationTemplates API from Elastic Stack (ELK Stack) — 1 operation(s) for platformconfigurationtemplates.
- [Elastic Stack (ELK Stack) Platform Configuration Trust Relationships API](https://apis.io/apis/elk-stack/elk-stack-platformconfigurationtrustrelationships-api/) — The PlatformConfigurationTrustRelationships API from Elastic Stack (ELK Stack) — 2 operation(s) for platformconfigurationtrustrelationships.
- [Elastic Stack (ELK Stack) Platform Infrastructure API](https://apis.io/apis/elk-stack/elk-stack-platforminfrastructure-api/) — The PlatformInfrastructure API from Elastic Stack (ELK Stack) — 51 operation(s) for platforminfrastructure.
- [Elastic Stack (ELK Stack) Query Rules API](https://apis.io/apis/elk-stack/elk-stack-query-rules-api/) — The query_rules API from Elastic Stack (ELK Stack) — 4 operation(s) for query_rules.
- [Elastic Stack (ELK Stack) Reindex API](https://apis.io/apis/elk-stack/elk-stack-reindex-api/) — The reindex API from Elastic Stack (ELK Stack) — 3 operation(s) for reindex.
- [Elastic Stack (ELK Stack) Roles API](https://apis.io/apis/elk-stack/elk-stack-roles-api/) — Manage the roles that grant Elasticsearch and Kibana privileges.
- [Elastic Stack (ELK Stack) Rollup API](https://apis.io/apis/elk-stack/elk-stack-rollup-api/) — The rollup API from Elastic Stack (ELK Stack) — 8 operation(s) for rollup.
- [Elastic Stack (ELK Stack) saved objects API](https://apis.io/apis/elk-stack/elk-stack-saved-objects-api/) — Export sets of saved objects that you want to import into Kibana, resolve import errors, and rotate an encryption key for encrypted saved objects with the…
- [Elastic Stack (ELK Stack) Script API](https://apis.io/apis/elk-stack/elk-stack-script-api/) — The script API from Elastic Stack (ELK Stack) — 5 operation(s) for script.
- [Elastic Stack (ELK Stack) Search API](https://apis.io/apis/elk-stack/elk-stack-search-api/) — The search API from Elastic Stack (ELK Stack) — 29 operation(s) for search.
- [Elastic Stack (ELK Stack) Search Application API](https://apis.io/apis/elk-stack/elk-stack-search-application-api/) — The search_application API from Elastic Stack (ELK Stack) — 4 operation(s) for search_application.
- [Elastic Stack (ELK Stack) Searchable Snapshots API](https://apis.io/apis/elk-stack/elk-stack-searchable-snapshots-api/) — The searchable_snapshots API from Elastic Stack (ELK Stack) — 7 operation(s) for searchable_snapshots.
- [Elastic Stack (ELK Stack) Security AI Assistant API](https://apis.io/apis/elk-stack/elk-stack-security-ai-assistant-api-api/) — Manage and interact with Security Assistant resources.
- [Elastic Stack (ELK Stack) Security API](https://apis.io/apis/elk-stack/elk-stack-security-api/) — The security API from Elastic Stack (ELK Stack) — 64 operation(s) for security.
- [Elastic Stack (ELK Stack) Security Attack discovery API](https://apis.io/apis/elk-stack/elk-stack-security-attack-discovery-api-api/) — Use the Attack discovery APIs to generate and manage Attack discoveries. Attack Discovery leverages large language models (LLMs) to analyze alerts in your…
- [Elastic Stack (ELK Stack) Security Detections API](https://apis.io/apis/elk-stack/elk-stack-security-detections-api-api/) — Use the detections APIs to create and manage detection rules. Detection rules search events and external alerts sent to Elastic Security and generate…
- [Elastic Stack (ELK Stack) Security Endpoint Exceptions API](https://apis.io/apis/elk-stack/elk-stack-security-endpoint-exceptions-api-api/) — Endpoint Exceptions API allows you to manage detection rule endpoint exceptions to prevent a rule from generating an alert from incoming events even when…
- [Elastic Stack (ELK Stack) Security Endpoint Management API](https://apis.io/apis/elk-stack/elk-stack-security-endpoint-management-api-api/) — Interact with and manage endpoints running the Elastic Defend integration.
- [Elastic Stack (ELK Stack) Security Entity Analytics API](https://apis.io/apis/elk-stack/elk-stack-security-entity-analytics-api-api/) — Use the Security entity analytics APIs to manage entity analytics and risk scoring, including asset criticality, privileged user monitoring, and entity engines.
- [Elastic Stack (ELK Stack) Security entity store API](https://apis.io/apis/elk-stack/elk-stack-security-entity-store-api/) — The Security entity store API from Elastic Stack (ELK Stack) — 16 operation(s) for security entity store.
- [Elastic Stack (ELK Stack) Security Exceptions API](https://apis.io/apis/elk-stack/elk-stack-security-exceptions-api-api/) — Exceptions are associated with detection and endpoint rules, and are used to prevent a rule from generating an alert from incoming events, even when the…
- [Elastic Stack (ELK Stack) Security Lists API](https://apis.io/apis/elk-stack/elk-stack-security-lists-api-api/) — Lists can be used with detection rule exceptions to define values that prevent a rule from generating alerts. Lists are made up of: * **List containers**: A…
- [Elastic Stack (ELK Stack) Security Osquery API](https://apis.io/apis/elk-stack/elk-stack-security-osquery-api-api/) — Run live queries, manage packs and saved queries.
- [Elastic Stack (ELK Stack) Security Solution Initialization API](https://apis.io/apis/elk-stack/elk-stack-security-solution-initialization-api-api/) — Use the initialization API to set up the assets Elastic Security needs to operate in a Kibana space. A single request can run one or more initialization…
- [Elastic Stack (ELK Stack) Security Timeline API](https://apis.io/apis/elk-stack/elk-stack-security-timeline-api-api/) — You can create Timelines and Timeline templates via the API, as well as import new Timelines from an ndjson file.
- [Elastic Stack (ELK Stack) short url API](https://apis.io/apis/elk-stack/elk-stack-short-url-api/) — Manage Kibana short URLs.
- [Elastic Stack (ELK Stack) Significant Events API](https://apis.io/apis/elk-stack/elk-stack-significant-events-api/) — The significant_events API from Elastic Stack (ELK Stack) — 4 operation(s) for significant_events.
- [Elastic Stack (ELK Stack) Slm API](https://apis.io/apis/elk-stack/elk-stack-slm-api/) — The slm API from Elastic Stack (ELK Stack) — 8 operation(s) for slm.
- [Elastic Stack (ELK Stack) Slo API](https://apis.io/apis/elk-stack/elk-stack-slo-api/) — SLO APIs enable you to define, manage and track service-level objectives
- [Elastic Stack (ELK Stack) Snapshot API](https://apis.io/apis/elk-stack/elk-stack-snapshot-api/) — The snapshot API from Elastic Stack (ELK Stack) — 12 operation(s) for snapshot.
- [Elastic Stack (ELK Stack) Spaces API](https://apis.io/apis/elk-stack/elk-stack-spaces-api/) — The Spaces API from Elastic Stack (ELK Stack) — 7 operation(s) for spaces.
- [Elastic Stack (ELK Stack) Sql API](https://apis.io/apis/elk-stack/elk-stack-sql-api/) — The sql API from Elastic Stack (ELK Stack) — 6 operation(s) for sql.
- [Elastic Stack (ELK Stack) Stack API](https://apis.io/apis/elk-stack/elk-stack-stack-api/) — The Stack API from Elastic Stack (ELK Stack) — 3 operation(s) for stack.
- [Elastic Stack (ELK Stack) Streams API](https://apis.io/apis/elk-stack/elk-stack-streams-api/) — The streams API from Elastic Stack (ELK Stack) — 16 operation(s) for streams.
- [Elastic Stack (ELK Stack) Synonyms API](https://apis.io/apis/elk-stack/elk-stack-synonyms-api/) — The synonyms API from Elastic Stack (ELK Stack) — 3 operation(s) for synonyms.
- [Elastic Stack (ELK Stack) Synthetics API](https://apis.io/apis/elk-stack/elk-stack-synthetics-api/) — Synthetics APIs enable you to check the status of your services and applications.
- [Elastic Stack (ELK Stack) System API](https://apis.io/apis/elk-stack/elk-stack-system-api/) — Get information about the system status, resource usage, features, and installed plugins.
- [Elastic Stack (ELK Stack) Tags API](https://apis.io/apis/elk-stack/elk-stack-tags-api/) — The Tags API from Elastic Stack (ELK Stack) — 2 operation(s) for tags.
- [Elastic Stack (ELK Stack) task manager API](https://apis.io/apis/elk-stack/elk-stack-task-manager-api/) — Task manager APIs enable you to check the health of the Kibana task manager, which is used by features such as alerting, actions, and reporting to run…
- [Elastic Stack (ELK Stack) Tasks API](https://apis.io/apis/elk-stack/elk-stack-tasks-api/) — The tasks API from Elastic Stack (ELK Stack) — 4 operation(s) for tasks.
- [Elastic Stack (ELK Stack) Telemetry API](https://apis.io/apis/elk-stack/elk-stack-telemetry-api/) — The Telemetry API from Elastic Stack (ELK Stack) — 1 operation(s) for telemetry.
- [Elastic Stack (ELK Stack) Text Structure API](https://apis.io/apis/elk-stack/elk-stack-text-structure-api/) — The text_structure API from Elastic Stack (ELK Stack) — 4 operation(s) for text_structure.
- [Elastic Stack (ELK Stack) Transform API](https://apis.io/apis/elk-stack/elk-stack-transform-api/) — The transform API from Elastic Stack (ELK Stack) — 13 operation(s) for transform.
- [Elastic Stack (ELK Stack) Trusted Environments API](https://apis.io/apis/elk-stack/elk-stack-trustedenvironments-api/) — The TrustedEnvironments API from Elastic Stack (ELK Stack) — 1 operation(s) for trustedenvironments.
- [Elastic Stack (ELK Stack) Upgrade API](https://apis.io/apis/elk-stack/elk-stack-upgrade-api/) — The Kibana Upgrade Assistant API helps you prepare for the next major Elasticsearch release. > warn > This is a Kibana REST API (not an Elasticsearch API)…
- [Elastic Stack (ELK Stack) Uptime API](https://apis.io/apis/elk-stack/elk-stack-uptime-api/) — Uptime APIs enable you to view and update uptime monitoring settings.
- [Elastic Stack (ELK Stack) user session API](https://apis.io/apis/elk-stack/elk-stack-user-session-api/) — Enables you to invalidate user sessions for security and session management purposes.
- [Elastic Stack (ELK Stack) User Role Assignments API](https://apis.io/apis/elk-stack/elk-stack-userroleassignments-api/) — The UserRoleAssignments API from Elastic Stack (ELK Stack) — 1 operation(s) for userroleassignments.
- [Elastic Stack (ELK Stack) Users API](https://apis.io/apis/elk-stack/elk-stack-users-api/) — The Users API from Elastic Stack (ELK Stack) — 3 operation(s) for users.
- [Elastic Stack (ELK Stack) Visualizations API](https://apis.io/apis/elk-stack/elk-stack-visualizations-api/) — > This documentation is temporarily hosted at a separate location. > > **[View the full Visualizations API reference…
- [Elastic Stack (ELK Stack) Watcher API](https://apis.io/apis/elk-stack/elk-stack-watcher-api/) — The watcher API from Elastic Stack (ELK Stack) — 13 operation(s) for watcher.
- [Elastic Stack (ELK Stack) Workflows API](https://apis.io/apis/elk-stack/elk-stack-workflows-api/) — Workflows enable you to automate multi-step processes directly in Kibana. Define sequences of steps in YAML to transform data insights into automated…
- [Elastic Stack (ELK Stack) Xpack API](https://apis.io/apis/elk-stack/elk-stack-xpack-api/) — The xpack API from Elastic Stack (ELK Stack) — 2 operation(s) for xpack.
- [Elastic Stack Index API](https://apis.io/apis/elk-stack/elk-stack-index-api/) — The Index API from Elastic Stack — 3 operation(s) for index.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Elk Stack Webhooks](https://apis.io/asyncapis/elk-stack/elk-stack-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [elk-stack-mcp.yml](https://apis.io/servers/elk-stack/elk-stack-mcp-yml/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Elk Stack Agentic Access](https://apis.io/agentic-access/elk-stack/elk-stack-agentic-access/)

#### Collections (8)

Postman and Open Collection request collections.

- [Elasticsearch REST API](https://apis.io/collections/elk-stack/open-elk-stack/)
- [Elasticsearch REST Cat API](https://apis.io/collections/elk-stack/open-elk-stack-cat-api/)
- [Elasticsearch REST Cat Cluster API](https://apis.io/collections/elk-stack/open-elk-stack-cluster-api/)
- [Elasticsearch REST Cat Document API](https://apis.io/collections/elk-stack/open-elk-stack-document-api/)
- [Elasticsearch REST Cat Index API](https://apis.io/collections/elk-stack/open-elk-stack-index-api/)
- [Elasticsearch REST Cat Ingest API](https://apis.io/collections/elk-stack/open-elk-stack-ingest-api/)
- [Elasticsearch REST Cat Search API](https://apis.io/collections/elk-stack/open-elk-stack-search-api/)
- [Elasticsearch REST Cat Snapshot API](https://apis.io/collections/elk-stack/open-elk-stack-snapshot-api/)

#### Overlays (135)

OpenAPI overlays, including conversational phrasing for each operation.

- [Elk Stack Accounts Api Phrasing Overlay](https://apis.io/overlays/elk-stack/elk-stack-accounts-api-phrasing-overlay/)
- [Elk Stack Actions Api Phrasing Overlay](https://apis.io/overlays/elk-stack/elk-stack-actions-api-phrasing-overlay/)
- [Elk Stack Agent Builder Api Phrasing Overlay](https://apis.io/overlays/elk-stack/elk-stack-agent-builder-api-phrasing-overlay/)
- [Elk Stack Alerting Api Phrasing Overlay](https://apis.io/overlays/elk-stack/elk-stack-alerting-api-phrasing-overlay/)
- [Elk Stack Alerting V2 Api Phrasing Overlay](https://apis.io/overlays/elk-stack/elk-stack-alerting-v2-api-phrasing-overlay/)
- [Elk Stack Analytics Api Phrasing Overlay](https://apis.io/overlays/elk-stack/elk-stack-analytics-api-phrasing-overlay/)
- [Elk Stack Apm Agent Configuration Api Phrasing Overlay](https://apis.io/overlays/elk-stack/elk-stack-apm-agent-configuration-api-phrasing-overlay/)
- [Elk Stack Apm Agent Keys Api Phrasing Overlay](https://apis.io/overlays/elk-stack/elk-stack-apm-agent-keys-api-phrasing-overlay/)
- [Elk Stack Apm Annotations Api Phrasing Overlay](https://apis.io/overlays/elk-stack/elk-stack-apm-annotations-api-phrasing-overlay/)
- [Elk Stack Apm Server Schema Api Phrasing Overlay](https://apis.io/overlays/elk-stack/elk-stack-apm-server-schema-api-phrasing-overlay/)
- [Elk Stack Apm Sourcemaps Api Phrasing Overlay](https://apis.io/overlays/elk-stack/elk-stack-apm-sourcemaps-api-phrasing-overlay/)
- [Elk Stack Authentication Api Phrasing Overlay](https://apis.io/overlays/elk-stack/elk-stack-authentication-api-phrasing-overlay/)
- [Elk Stack Billingcostsanalysis Api Phrasing Overlay](https://apis.io/overlays/elk-stack/elk-stack-billingcostsanalysis-api-phrasing-overlay/)
- [Elk Stack Cases Api Phrasing Overlay](https://apis.io/overlays/elk-stack/elk-stack-cases-api-phrasing-overlay/)
- [Elk Stack Cat Api Phrasing Overlay](https://apis.io/overlays/elk-stack/elk-stack-cat-api-phrasing-overlay/)
- [Elk Stack Ccr Api Phrasing Overlay](https://apis.io/overlays/elk-stack/elk-stack-ccr-api-phrasing-overlay/)
- [Elk Stack Cluster Api Phrasing Overlay](https://apis.io/overlays/elk-stack/elk-stack-cluster-api-phrasing-overlay/)
- [Elk Stack Comments Api Phrasing Overlay](https://apis.io/overlays/elk-stack/elk-stack-comments-api-phrasing-overlay/)
- [Elk Stack Connector Api Phrasing Overlay](https://apis.io/overlays/elk-stack/elk-stack-connector-api-phrasing-overlay/)
- [Elk Stack Connectors Api Phrasing Overlay](https://apis.io/overlays/elk-stack/elk-stack-connectors-api-phrasing-overlay/)
- [Elk Stack Dashboards Api Phrasing Overlay](https://apis.io/overlays/elk-stack/elk-stack-dashboards-api-phrasing-overlay/)
- [Elk Stack Data Stream Api Phrasing Overlay](https://apis.io/overlays/elk-stack/elk-stack-data-stream-api-phrasing-overlay/)
- [Elk Stack Data Streams Api Phrasing Overlay](https://apis.io/overlays/elk-stack/elk-stack-data-streams-api-phrasing-overlay/)
- [Elk Stack Data Views Api Phrasing Overlay](https://apis.io/overlays/elk-stack/elk-stack-data-views-api-phrasing-overlay/)
- [Elk Stack Deployments Api Phrasing Overlay](https://apis.io/overlays/elk-stack/elk-stack-deployments-api-phrasing-overlay/)
- …and 110 more published on APIs.io

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Elk Stack Authentication](https://apis.io/security/elk-stack/elk-stack-authentication/)
- [Elk Stack Domain Security](https://apis.io/security/elk-stack/elk-stack-domain-security/)
- [Elk Stack Trust Center](https://apis.io/security/elk-stack/elk-stack-trust-center/)
- [Elk Stack Vulnerability Disclosure](https://apis.io/security/elk-stack/elk-stack-vulnerability-disclosure/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Elk Stack Plans Pricing](https://apis.io/plans/elk-stack/elk-stack-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Elk Stack Rate Limits](https://apis.io/rate-limits/elk-stack/elk-stack-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Elk Stack Finops](https://apis.io/finops/elk-stack/elk-stack-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.elastic.co/elastic-stack/)
- [Documentation](https://www.elastic.co/docs)
- [Getting started](https://www.elastic.co/docs/get-started)
- [API reference](https://www.elastic.co/docs/api)
- [Pricing](https://www.elastic.co/pricing/)
- [Sign up](https://www.elastic.co/cloud/elasticsearch-service/signup)
- [Support](https://www.elastic.co/support)
- [Blog](https://www.elastic.co/blog/)
- [Terms of service](https://www.elastic.co/legal/terms-of-use)
- [Privacy policy](https://www.elastic.co/legal/privacy-statement)
- [GitHub](https://github.com/elastic)
- [Status](https://status.elastic.co/)

## API Evangelist rating

**Kin Score 76.9** — exemplar · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 80.0 |
| Contract quality | 56.3 |
| Contract governance | 4.5 |
| Operational transparency | 60.5 |
| Developer ergonomics | 80.4 |
| Access clarity | 92.1 |

**Agent readiness 43.9** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | templated |
| Auth Clarity | bearer (partial credit) |
| Idempotency | derived (partial credit) |
| Error Semantics | verified |
| OpenAPI Examples | verified |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | yes |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | yes |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | — |

**Regulatory alignment 32.7** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/elk-stack/](https://apis.io/providers/elk-stack/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Elastic Stack: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/elk-stack/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
