# Backstage (backstage)

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

Backstage is an open-source developer portal platform created by Spotify. It provides a centralized software catalog, software templates (scaffolder), TechDocs, and a plugin ecosystem for building customizable developer portals. Backstage helps organizations manage their software ecosystem by cataloging services, APIs, resources, and infrastructure, and provides tooling for creating new projects from templates.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/backstage/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/backstage/refs/heads/main/apis.yml)

## Scope

- **Type:** Index
- **Position:** Consumer
- **Access:** 3rd-Party

## Tags

- Developer Portal
- Internal Developer Platform
- Software Catalog
- Open Source

## Timestamps

- **Created:** 2024-12-01
- **Modified:** 2026-04-21

## APIs

### Backstage Catalog API

The Backstage Software Catalog REST API provides JSON-based endpoints for managing and querying catalog entities, locations, and related metadata. The catalog stores information about all software components, APIs, resources, systems, domains, groups, and users in an organization. Supports entity CRUD, filtering, full-text search, cursor-based pagination, faceted queries, location management, entity validation, and ancestry lookups.

- **Human URL:** [https://backstage.io/docs/features/software-catalog/software-catalog-api/](https://backstage.io/docs/features/software-catalog/software-catalog-api/)

#### Tags

- Developer Portal
- Entities
- Software Catalog

#### Properties

- [Documentation](https://backstage.io/docs/features/software-catalog/software-catalog-api/)
- [OpenAPI](openapi/backstage-catalog-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/backstage-catalog.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/backstage-catalog.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Backstage Scaffolder API

The Backstage Scaffolder (Software Templates) REST API provides endpoints for creating, managing, and monitoring scaffolder tasks. It enables programmatic execution of software templates to bootstrap new projects, components, and other software assets. Supports task creation and cancellation, real-time event streaming, log retrieval, template parameter schema inspection, available action listing, and dry-run execution for template validation.

- **Human URL:** [https://backstage.io/docs/features/software-templates/](https://backstage.io/docs/features/software-templates/)

#### Tags

- Developer Portal
- Scaffolding
- Software Templates

#### Properties

- [Documentation](https://backstage.io/docs/features/software-templates/)
- [OpenAPI](openapi/backstage-scaffolder-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/backstage-scaffolder.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/backstage-scaffolder.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Backstage Auth API

The Backstage Auth API provides endpoints for authenticating users and services with the Backstage backend. It supports multiple authentication providers (GitHub, Google, Okta, SAML, etc.) and handles OAuth flows, token issuance, token refresh, and session management. The Auth API is used by the Backstage frontend to initiate login flows and by backend plugins to verify caller identity via Backstage tokens.

- **Human URL:** [https://backstage.io/docs/auth/](https://backstage.io/docs/auth/)

#### Tags

- Authentication
- Developer Portal
- OAuth

#### Properties

- [Documentation](https://backstage.io/docs/auth/)
- [OpenAPI](openapi/backstage-auth-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/backstage-auth.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/backstage-auth.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Backstage TechDocs API

The Backstage TechDocs API provides endpoints for generating, publishing, and serving technical documentation for catalog entities. TechDocs uses MkDocs under the hood to render Markdown documentation into static HTML pages. The API supports fetching rendered documentation, syncing docs from external storage, retrieving metadata, and managing documentation lifecycle.

- **Human URL:** [https://backstage.io/docs/features/techdocs/](https://backstage.io/docs/features/techdocs/)

#### Tags

- Developer Portal
- Documentation
- TechDocs

#### Properties

- [Documentation](https://backstage.io/docs/features/techdocs/)
- [OpenAPI](openapi/backstage-techdocs-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/backstage-techdocs.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/backstage-techdocs.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Backstage Search API

The Backstage Search API provides endpoints for querying the Backstage search index. It enables full-text search across all indexed content including catalog entities, TechDocs pages, and any other content indexed by search collators. The API supports filtering by document type, pagination via cursors, and term-based queries.

- **Human URL:** [https://backstage.io/docs/features/search/](https://backstage.io/docs/features/search/)

#### Tags

- Developer Portal
- Discovery
- Search

#### Properties

- [Documentation](https://backstage.io/docs/features/search/)
- [OpenAPI](openapi/backstage-search-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/backstage-search.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/backstage-search.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Backstage Permissions API

The Backstage Permissions API provides endpoints for evaluating and managing authorization decisions within Backstage. It enables plugins to check whether a given user or service has permission to perform a specific action. The framework supports policy-based authorization with conditional rules that can be applied to resources.

- **Human URL:** [https://backstage.io/docs/permissions/overview](https://backstage.io/docs/permissions/overview)

#### Tags

- Authorization
- Developer Portal
- Permissions

#### Properties

- [Documentation](https://backstage.io/docs/permissions/overview)
- [OpenAPI](openapi/backstage-permissions-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/backstage-permissions.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/backstage-permissions.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Backstage Events System

The Backstage Events system provides a publish-subscribe mechanism for broadcasting and consuming events within a Backstage instance. It enables plugins to emit events when significant actions occur (such as catalog entity changes, scaffolder task completions, or permission policy updates) and allows other plugins or external systems to subscribe to those events via HTTP webhooks or the internal event bus.

- **Human URL:** [https://backstage.io/docs/plugins/backends-and-plugins/](https://backstage.io/docs/plugins/backends-and-plugins/)

#### Tags

- Developer Portal
- Events
- Webhooks

#### Properties

- [Documentation](https://backstage.io/docs/plugins/backends-and-plugins/)
- [AsyncAPI](asyncapi/backstage-events-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [Postman Collection](collections/backstage-auth.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/backstage-auth.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/backstage-catalog.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/backstage-catalog.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/backstage-permissions.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/backstage-permissions.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/backstage-scaffolder.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/backstage-scaffolder.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/backstage-search.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/backstage-search.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/backstage-techdocs.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/backstage-techdocs.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/showcase/backstage-from-spotify)
- [Website](https://backstage.io/)
- [Documentation](https://backstage.io/docs/)
- [Getting Started](https://backstage.io/docs/getting-started/)
- [Blog](https://backstage.io/blog/)
- [GitHub Organization](https://github.com/backstage)
- [GitHub Repository](https://github.com/backstage/backstage)
- [Changelog](https://github.com/backstage/backstage/releases)
- [Community](https://discord.gg/backstage-687207715902193673)
- [Developer  Tools](https://backstage.io/plugins/)
- [JSON Schema](json-schema/backstage-entity-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/backstage-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Spectral Rules](rules/backstage-spectral-rules.yml)
- [Vocabulary](vocabulary/backstage-vocabulary.yaml)
- [Features](undefined)
- [Use Cases](undefined)
- [Integrations](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
