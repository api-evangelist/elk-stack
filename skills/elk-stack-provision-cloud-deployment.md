---
name: elk-stack-provision-cloud-deployment
description: Create, inspect, resize and safely tear down an Elastic Cloud deployment through the control-plane API, including the shutdown/restore path and what it does not bring back.
api: elk-stack:elastic-cloud-api
operations:
  - get-deployment-templates-v2
  - create-deployment
  - get-deployment
  - get-deployment-es-resource-info
  - update-deployment
  - cancel-deployment-resource-pending-plan
  - shutdown-deployment
  - restore-deployment
  - get-costs-overview
generated: '2026-08-27'
method: generated
source: openapi/elk-stack-elastic-cloud-swagger.json
---

# Provision and manage an Elastic Cloud deployment

Base URL `https://api.elastic-cloud.com/api/v1`, authenticated with
`Authorization: ApiKey <cloud-api-key>`.

**These are different credentials from a cluster API key.** A Cloud key manages deployments and
cannot read a document; an Elasticsearch key reads documents and cannot resize a deployment. Holding
one does not imply the other.

## 1. Pick a deployment template

`get-deployment-templates-v2` — `GET /deployments/templates`. The template id plus the region determines
the topology; you cannot compose one freely.

## 2. Create the deployment

`create-deployment` — `POST /deployments`.

The response carries the generated `deployment_id`, each resource's `ref_id`, the endpoints, and
**the only copy of the generated `elastic` user credentials you will ever be shown**. Capture them on
this response. Recovering them later means a password reset, which invalidates the old one.

There is **no `Idempotency-Key` header on this API.** A timed-out `create-deployment` may well have
succeeded. Do not blind-retry: call `search-deployments` (`POST /deployments/_search`) filtered on
your deployment name first, or you will end up paying for two clusters.

## 3. Read state and wait for readiness

`get-deployment` — `GET /deployments/{deployment_id}`. Changes are applied as *plans*, asynchronously.
The deployment is not usable when the call returns; poll until the resource's plan shows healthy.

`get-deployment-es-resource-info` — `GET /deployments/{deployment_id}/elasticsearch/{ref_id}` gives the
cluster endpoint you then use as `{elasticsearch_endpoint}` for every operation in the other skills.

## 4. Resize or upgrade

`update-deployment` — `PUT /deployments/{deployment_id}` submits a new plan.

If you got the plan wrong, `cancel-deployment-resource-pending-plan` — `DELETE
/deployments/{deployment_id}/{resource_kind}/{ref_id}/plan/pending` — cancels it **only while it is
still pending**. Once applied it can be reversed only by submitting another plan.

## 5. Tear down — and understand what restore does not restore

`shutdown-deployment` — `POST /deployments/{deployment_id}/_shutdown`.

`restore-deployment` — `POST /deployments/{deployment_id}/_restore` — brings back the deployment's
**configuration**. It does **not** bring back the data. Elastic's own words: "the data that was in the
deployment is not restored, since it is deleted as part of the termination process", and on snapshots,
"Snapshots are retained for very a limited amount of time post deletion and we cannot guarantee that
deleted deployments can be restored from snapshots for this reason".

**Elastic states no restore window.** Treat shutdown as irreversible for data. Snapshot to a
customer-owned repository first — see `elk-stack-snapshot-before-destructive-change`.

## 6. Watch the cost

`get-costs-overview` — `GET /billing/costs/{organization_id}`. A deployment bills for as long as it
runs; an agent that creates deployments should read this back.

## Errors

This surface has the best error contract of the three: 186 structured codes in
`errors/elk-stack-problem-types.yml`. Branch on `errors[].code`, not on the message string.

- `deployments.deployment_not_found` (404) — wrong id.
- `security_realm.version_conflict` / `roles.version_conflict` (409) — re-read and retry.
- `billing_service.rate_limited` (429) — back off; no `Retry-After` header is sent.
- `deployments.metadata_internal_error` (449) — Elastic is explicitly asking you to retry the same request.
