# Backstage (backstage)
Backstage is an open-source developer portal platform created by Spotify. It provides a centralized software catalog, software templates (scaffolder), TechDocs, and a plugin ecosystem for building customizable developer portals. Backstage helps organizations manage their software ecosystem by cataloging services, APIs, resources, and infrastructure, and provides tooling for creating new projects from templates.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/backstage/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags:

 - Developer Portal, Internal Developer Platform, Software Catalog, Open Source

## Timestamps

- **Created:** 2024-12-01
- **Modified:** 2026-04-19

## APIs

### Backstage Catalog API
The Backstage Software Catalog REST API provides JSON-based endpoints for managing and querying catalog entities, locations, and related metadata.

**Human URL:** [https://backstage.io/docs/features/software-catalog/software-catalog-api/](https://backstage.io/docs/features/software-catalog/software-catalog-api/)

#### Tags:

 - Developer Portal, Entities, Software Catalog

#### Properties

- [Documentation](https://backstage.io/docs/features/software-catalog/software-catalog-api/)
- [OpenAPI](openapi/backstage-catalog-openapi.yml)

### Backstage Scaffolder API
The Backstage Scaffolder (Software Templates) REST API provides endpoints for creating, managing, and monitoring scaffolder tasks.

**Human URL:** [https://backstage.io/docs/features/software-templates/](https://backstage.io/docs/features/software-templates/)

#### Tags:

 - Developer Portal, Scaffolding, Software Templates

#### Properties

- [Documentation](https://backstage.io/docs/features/software-templates/)
- [OpenAPI](openapi/backstage-scaffolder-openapi.yml)

### Backstage Auth API
The Backstage Auth API provides endpoints for authenticating users and services with the Backstage backend.

**Human URL:** [https://backstage.io/docs/auth/](https://backstage.io/docs/auth/)

#### Tags:

 - Authentication, Developer Portal, OAuth

#### Properties

- [Documentation](https://backstage.io/docs/auth/)
- [OpenAPI](openapi/backstage-auth-openapi.yml)

### Backstage TechDocs API
The Backstage TechDocs API provides endpoints for generating, publishing, and serving technical documentation for catalog entities.

**Human URL:** [https://backstage.io/docs/features/techdocs/](https://backstage.io/docs/features/techdocs/)

#### Tags:

 - Developer Portal, Documentation, TechDocs

#### Properties

- [Documentation](https://backstage.io/docs/features/techdocs/)
- [OpenAPI](openapi/backstage-techdocs-openapi.yml)

### Backstage Search API
The Backstage Search API provides endpoints for querying the Backstage search index.

**Human URL:** [https://backstage.io/docs/features/search/](https://backstage.io/docs/features/search/)

#### Tags:

 - Developer Portal, Discovery, Search

#### Properties

- [Documentation](https://backstage.io/docs/features/search/)
- [OpenAPI](openapi/backstage-search-openapi.yml)

### Backstage Permissions API
The Backstage Permissions API provides endpoints for evaluating and managing authorization decisions within Backstage.

**Human URL:** [https://backstage.io/docs/permissions/overview](https://backstage.io/docs/permissions/overview)

#### Tags:

 - Authorization, Developer Portal, Permissions

#### Properties

- [Documentation](https://backstage.io/docs/permissions/overview)
- [OpenAPI](openapi/backstage-permissions-openapi.yml)

### Backstage Events System
The Backstage Events system provides a publish-subscribe mechanism for broadcasting and consuming events within a Backstage instance.

**Human URL:** [https://backstage.io/docs/plugins/backends-and-plugins/](https://backstage.io/docs/plugins/backends-and-plugins/)

#### Tags:

 - Developer Portal, Events, Webhooks

#### Properties

- [Documentation](https://backstage.io/docs/plugins/backends-and-plugins/)
- [AsyncAPI](asyncapi/backstage-events-asyncapi.yml)

## Common Properties

- [Backstage Website](https://backstage.io/)
- [Documentation](https://backstage.io/docs/)
- [GettingStarted](https://backstage.io/docs/getting-started/)
- [Blog](https://backstage.io/blog/)
- [GitHubOrganization](https://github.com/backstage)
- [GitHubRepository](https://github.com/backstage/backstage)
- [ChangeLog](https://github.com/backstage/backstage/releases)
- [Community](https://discord.gg/backstage-687207715902193673)
- [Plugin Directory](https://backstage.io/plugins/)

## Features

| Name | Description |
|------|-------------|
| Software Catalog | Central inventory of all software components, APIs, resources, systems, domains, groups, and users. |
| Software Templates (Scaffolder) | Bootstrap new projects, services, and components from customizable templates. |
| TechDocs | Render and serve MkDocs-based technical documentation alongside catalog entities. |
| Plugin Ecosystem | Extensible plugin architecture with 100+ open-source plugins for CI/CD, monitoring, cloud, and more. |
| Search | Full-text search across catalog entities, TechDocs, and any other indexed content. |
| Permissions Framework | Policy-based authorization with conditional rules for resource-level access control. |
| Entity Relations | Model ownership, dependencies, and API consumption relationships between services. |

## Use Cases

| Name | Description |
|------|-------------|
| Internal Developer Portal | Build a unified portal for developers to discover services, read docs, and scaffold projects. |
| Service Catalog | Maintain a complete, up-to-date inventory of all microservices, APIs, and infrastructure. |
| Developer Onboarding | Accelerate new developer onboarding with self-service project scaffolding and documentation. |
| API Governance | Track all internal and external APIs, their owners, and documentation in one place. |

## Integrations

| Name | Description |
|------|-------------|
| GitHub | Catalog ingestion from GitHub repos, GitHub Actions integration for CI/CD visibility. |
| PagerDuty | Show on-call information and incident status on catalog entity pages. |
| Kubernetes | Display Kubernetes workload status for catalog entities. |
| Prometheus | Show metrics and alerts for services directly in the catalog. |
| Snyk | Display security vulnerability information for catalog entities. |
| Datadog | Surface monitoring dashboards within Backstage. |

## Artifacts

Machine-readable API specifications organized by format.

### OpenAPI

- [Backstage Catalog API](openapi/backstage-catalog-openapi.yml)
- [Backstage Scaffolder API](openapi/backstage-scaffolder-openapi.yml)
- [Backstage Auth API](openapi/backstage-auth-openapi.yml)
- [Backstage TechDocs API](openapi/backstage-techdocs-openapi.yml)
- [Backstage Search API](openapi/backstage-search-openapi.yml)
- [Backstage Permissions API](openapi/backstage-permissions-openapi.yml)

### AsyncAPI

- [Backstage Events System](asyncapi/backstage-events-asyncapi.yml)

### JSON Schema

- [Entity](json-schema/catalog-entity-schema.json)
- [EntityMeta](json-schema/catalog-entity-meta-schema.json)
- [ScaffolderTask](json-schema/scaffolder-scaffolder-task-schema.json)
- [SearchResult](json-schema/search-search-result-schema.json)
- [backstage-entity-schema.json](json-schema/backstage-entity-schema.json)
- [+ 11 more schemas](json-schema/)

### JSON-LD

- [Backstage JSON-LD Context](json-ld/backstage-context.jsonld)

## Capabilities

Naftiko capabilities organized as shared per-API definitions composed into customer-facing workflows.

### Shared Per-API Definitions

- [Backstage Catalog API](capabilities/shared/catalog-api.yaml) — 5 operations for catalog entity and location management

### Workflow Capabilities

| Workflow | APIs Combined | Tools | Persona |
|----------|--------------|-------|---------|
| [Developer Portal](capabilities/developer-portal.yaml) | Catalog API | 5 | Platform Engineer, Developer |

## Vocabulary

- [Backstage Vocabulary](vocabulary/backstage-vocabulary.yaml) — Unified taxonomy mapping 7 resources, 9 actions, 1 workflow, and 2 personas across operational (OpenAPI) and capability (Naftiko) dimensions

## Rules

- [Backstage Spectral Rules](rules/backstage-spectral-rules.yml) — 22 rules across 7 categories enforcing Backstage API conventions

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
