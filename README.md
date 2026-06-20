# Rowy (rowy)

Rowy is an open-source low-code backend platform that puts an Airtable-like spreadsheet UI on top of Google Cloud Firestore, with JavaScript/TypeScript Cloud Functions, column automations, and webhooks. It is primarily a UI plus a Firebase/GCP framework deployed into the user's own project; its main inbound API surface is per-table webhooks running on Cloud Run, alongside Rowy Run backend services and the underlying Firestore data store accessed via the Firebase SDK.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/rowy/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/rowy/refs/heads/main/apis.yml)

## Tags

- Low-Code
- Backend
- Firestore
- Firebase
- Webhooks
- Cloud Functions

## Timestamps

- **Created:** 2026-06-20
- **Modified:** 2026-06-20

## APIs

### Rowy Webhooks

Rowy's primary inbound API surface. Each table can generate an HTTPS webhook endpoint running on Google Cloud Run (the rowy-hooks service) that receives POST requests from external systems. Built-in types include Basic, Typeform, Sendgrid, and Github; a low-code parser function maps the incoming request into a new row, with optional condition and verification functions.

- **Human URL:** [https://docs.rowy.io/webhooks](https://docs.rowy.io/webhooks)

#### Tags

- Webhooks
- Inbound
- HTTP

#### Properties

- [Documentation](https://docs.rowy.io/webhooks)
- [API Reference](https://docs.rowy.io/webhooks/basic)
- [OpenAPI](openapi/rowy-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [GitHub](https://github.com/rowyio/rowy)
- [Postman Collection](collections/rowy.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/rowy.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Rowy Run / Cloud Functions

Rowy Run is a group of Google Cloud Run services (rowy-backend and rowy-hooks) deployed into the user's own GCP project that powers derivatives, action scripts, webhooks, user management, and one-click Cloud Function deployment. Service URLs are generated at deploy time and stored in Firestore (_rowy_/settings); there is no fixed public REST base URL or documented endpoint catalog.

- **Human URL:** [https://docs.rowy.io/rowy-run](https://docs.rowy.io/rowy-run)

#### Tags

- Cloud Functions
- Cloud Run
- Automation

#### Properties

- [Documentation](https://docs.rowy.io/rowy-run)
- [OpenAPI](openapi/rowy-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [GitHub](https://github.com/rowyio/rowy)
- [Postman Collection](collections/rowy.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/rowy.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Rowy Firestore Data

Rowy tables map directly onto Google Cloud Firestore collections. Programmatic data access is not a Rowy-specific REST API; it is the underlying Firestore data store reached via the Firebase/Google Cloud SDKs and the Firestore REST/RPC API. Rowy provides the spreadsheet UI and low-code layer on top of this data.

- **Human URL:** [https://docs.rowy.io/](https://docs.rowy.io/)

#### Tags

- Firestore
- Database
- SDK

#### Properties

- [Documentation](https://docs.rowy.io/)
- [OpenAPI](openapi/rowy-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [GitHub](https://github.com/rowyio/rowy)
- [Postman Collection](collections/rowy.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/rowy.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/rowyio)
- [LinkedIn](https://www.linkedin.com/company/rowyio)
- [Website](https://www.rowy.io)
- [Documentation](https://docs.rowy.io)
- [Plans](plans/rowy-plans-pricing.yml)
- [Rate Limits](rate-limits/rowy-rate-limits.yml)
- [Fin Ops](finops/rowy-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
