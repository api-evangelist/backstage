---
name: backstage-register-catalog-entity
description: Register a software component in a Backstage Software Catalog from a catalog-info.yaml URL, validating it first and confirming the resulting entity. Use when adding a service, API, resource or system to a Backstage instance over the REST API or the MCP Actions endpoint.
api: Backstage Software Catalog API
generated: '2026-09-04'
method: generated
source: openapi/backstage-catalog-backend-openapi.yaml, mcp/backstage-mcp-tools-list.json
operations:
  - ValidateEntity
  - AnalyzeLocation
  - CreateLocation
  - GetEntityByName
  - RefreshEntity
  - DeleteLocation
mcp_tools:
  - catalog.validate-entity
  - catalog.register-entity
  - catalog.get-catalog-entity
  - catalog.refresh-catalog-entity
  - catalog.unregister-entity
---

# Register a catalog entity in Backstage

Backstage is self-hosted. Every URL below is relative to the operator's own backend:
`https://{backstage-host}/api/catalog`. Send `Authorization: Bearer <backstage-token>`; the
`JWT` bearer scheme is the only securityScheme these operations declare.

## Steps

1. **Validate the descriptor before you register it.**
   `POST /validate-entity` (`ValidateEntity`) with the parsed `catalog-info.yaml` content and its
   `location`. This changes nothing, so it is always safe to run first. A malformed descriptor
   comes back as HTTP 400 with `error.name: InputError` — fix and re-send.
   MCP equivalent: `catalog.validate-entity` (readOnly, idempotent).

2. **Optionally inspect the target first.** `POST /analyze-location` (`AnalyzeLocation`) reports
   what Backstage would discover at a URL, including entities it would generate. Use it when the
   caller gave you a repository rather than a descriptor file.

3. **Register.** `POST /locations` (`CreateLocation`) with `{ type: "url", target: "<https URL of
   catalog-info.yaml>" }`. This creates a Location entity that owns everything ingested from that
   file. MCP equivalent: `catalog.register-entity`, whose only input is `locationUrl`.
   This tool is annotated `idempotentHint: false` — re-sending it is NOT free, so do not retry
   blindly on a timeout; read back with step 4 instead. There is no Idempotency-Key header on this
   API.

4. **Confirm.** `GET /entities/by-name/{kind}/{namespace}/{name}` (`GetEntityByName`) with the ref
   from the descriptor (`namespace` defaults to `default`). Ingestion is asynchronous, so a 404
   immediately after registering means "not processed yet", not "failed". Poll, or force a pass
   with `POST /refresh` (`RefreshEntity`).

5. **Reversal.** `DELETE /locations/{id}` (`DeleteLocation`) unregisters the Location and the
   entities it owns. There is no time window on this — it works whenever. It removes the
   registration, not the `catalog-info.yaml` in the source repository. MCP equivalent:
   `catalog.unregister-entity`, which is annotated `destructiveHint: true`.

## Rules

- Entity identity is the ref `<kind>:<namespace>/<name>` — use it, not the opaque `uid`, in
  anything a human will read.
- Errors are `{ error: { name, message }, request, response }`, not RFC 9457 problem+json.
  Switch on `error.name`: `InputError` (400), `NotAllowedError` (403, the Permissions framework
  denied it), `ConflictError` (409).
- A 403 is not a credential problem. It means the operator's permission policy denied the named
  catalog permission for this identity; escalate to the operator rather than re-authenticating.
- Listing is cursor-paged: prefer `GET /entities/by-query` with `cursor` and read
  `pageInfo.nextCursor` back. `GET /entities` is the older unpaged endpoint the docs steer away from.
