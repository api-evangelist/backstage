# Backstage (backstage)
Backstage is an open-source developer portal platform created by Spotify. It provides a centralized software catalog, software templates (scaffolder), TechDocs, and a plugin ecosystem for building customizable developer portals. Backstage helps organizations manage their software ecosystem by cataloging services, APIs, resources, and infrastructure, and provides tooling for creating new projects from templates.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/backstage/refs/heads/main/apis.yml)

## Scope

- **Type:** Index 
- **Position:** Consuming 
- **Access:** 3rd-Party 

## Tags:

 - Developer Portal, Software Catalog, Internal Developer Platform

## Timestamps

- **Created:** 2024-12-01 
- **Modified:** 2026-03-18 

## APIs

### Backstage Catalog API
The Backstage Software Catalog REST API provides JSON-based endpoints for managing and querying catalog entities, locations, and related metadata. The catalog stores information about all software components, APIs, resources, systems, domains, groups, and users in an organization. Supports entity CRUD, filtering, full-text search, cursor-based pagination, faceted queries, location management, entity validation, and ancestry lookups.

**Human URL:** [https://backstage.io/docs/features/software-catalog/software-catalog-api/](https://backstage.io/docs/features/software-catalog/software-catalog-api/)


#### Tags:

 - Developer Portal, Software Catalog, Entities

#### Properties

- [Documentation](https://backstage.io/docs/features/software-catalog/software-catalog-api/)
- [OpenAPI](openapi/backstage-catalog-openapi.yml)

### Backstage Scaffolder API
The Backstage Scaffolder (Software Templates) REST API provides endpoints for creating, managing, and monitoring scaffolder tasks. It enables programmatic execution of software templates to bootstrap new projects, components, and other software assets. Supports task creation and cancellation, real-time event streaming, log retrieval, template parameter schema inspection, available action listing, and dry-run execution for template validation.

**Human URL:** [https://backstage.io/docs/features/software-templates/](https://backstage.io/docs/features/software-templates/)


#### Tags:

 - Developer Portal, Software Templates, Scaffolding

#### Properties

- [Documentation](https://backstage.io/docs/features/software-templates/)
- [OpenAPI](openapi/backstage-scaffolder-openapi.yml)

### Backstage Auth API
The Backstage Auth API provides endpoints for authenticating users and services with the Backstage backend. It supports multiple authentication providers (GitHub, Google, Okta, SAML, etc.) and handles OAuth flows, token issuance, token refresh, and session management. The Auth API is used by the Backstage frontend to initiate login flows and by backend plugins to verify caller identity via Backstage tokens.

**Human URL:** [https://backstage.io/docs/auth/](https://backstage.io/docs/auth/)


#### Tags:

 - Developer Portal, Authentication, OAuth

#### Properties

- [Documentation](https://backstage.io/docs/auth/)
- [OpenAPI](openapi/backstage-auth-openapi.yml)

### Backstage TechDocs API
The Backstage TechDocs API provides endpoints for generating, publishing, and serving technical documentation for catalog entities. TechDocs uses MkDocs under the hood to render Markdown documentation into static HTML pages. The API supports fetching rendered documentation, syncing docs from external storage, retrieving metadata, and managing documentation lifecycle.

**Human URL:** [https://backstage.io/docs/features/techdocs/](https://backstage.io/docs/features/techdocs/)


#### Tags:

 - Developer Portal, Documentation, TechDocs

#### Properties

- [Documentation](https://backstage.io/docs/features/techdocs/)
- [OpenAPI](openapi/backstage-techdocs-openapi.yml)

### Backstage Search API
The Backstage Search API provides endpoints for querying the Backstage search index. It enables full-text search across all indexed content including catalog entities, TechDocs pages, and any other content indexed by search collators. The API supports filtering by document type, pagination via cursors, and term-based queries.

**Human URL:** [https://backstage.io/docs/features/search/](https://backstage.io/docs/features/search/)


#### Tags:

 - Developer Portal, Search, Discovery

#### Properties

- [Documentation](https://backstage.io/docs/features/search/)
- [OpenAPI](openapi/backstage-search-openapi.yml)

### Backstage Permissions API
The Backstage Permissions API provides endpoints for evaluating and managing authorization decisions within Backstage. It enables plugins to check whether a given user or service has permission to perform a specific action. The framework supports policy-based authorization with conditional rules that can be applied to resources.

**Human URL:** [https://backstage.io/docs/permissions/overview](https://backstage.io/docs/permissions/overview)


#### Tags:

 - Developer Portal, Authorization, Permissions

#### Properties

- [Documentation](https://backstage.io/docs/permissions/overview)
- [OpenAPI](openapi/backstage-permissions-openapi.yml)

### Backstage Events System
The Backstage Events system provides a publish-subscribe mechanism for broadcasting and consuming events within a Backstage instance. It enables plugins to emit events when significant actions occur (such as catalog entity changes, scaffolder task completions, or permission policy updates) and allows other plugins or external systems to subscribe to those events via HTTP webhooks or the internal event bus.

**Human URL:** [https://backstage.io/docs/plugins/backends-and-plugins/](https://backstage.io/docs/plugins/backends-and-plugins/)


#### Tags:

 - Developer Portal, Events, Webhooks

#### Properties

- [Documentation](https://backstage.io/docs/plugins/backends-and-plugins/)
- [AsyncAPI](asyncapi/backstage-events-asyncapi.yml)

## Common Properties

- [Website](https://backstage.io/)
- [Documentation](https://backstage.io/docs/)
- [Getting Started](https://backstage.io/docs/getting-started/)
- [Blog](https://backstage.io/blog/)
- [GitHub Organization](https://github.com/backstage)
- [GitHubRepository](https://github.com/backstage/backstage)
- [Change Log](https://github.com/backstage/backstage/releases)
- [Community](https://discord.gg/backstage-687207715902193673)
- [Developer Tools](https://backstage.io/plugins/)
- [JSONSchema](json-schema/backstage-entity-schema.json)
- [JSON-LD](json-ld/backstage-context.jsonld)

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
