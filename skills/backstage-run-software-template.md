---
name: backstage-run-software-template
description: Execute a Backstage software template (scaffolder) safely — inspect its parameter schema, rehearse with a dry run, launch the task, follow its logs, and cancel it if it goes wrong. Use when scaffolding a new service, repository or component through Backstage.
api: Backstage Scaffolder API
generated: '2026-09-04'
method: generated
source: openapi/backstage-scaffolder-backend-openapi.yaml, mcp/backstage-mcp-tools-list.json
operations:
  - GetTemplateParameterSchema
  - ListActions
  - DryRun
  - Scaffold
  - GetTask
  - StreamLogsPolling
  - CancelTask
  - Retry
mcp_tools:
  - scaffolder.list-scaffolder-actions
  - scaffolder.dry-run-template
  - scaffolder.execute-template
  - scaffolder.list-scaffolder-tasks
  - scaffolder.get-scaffolder-task-logs
---

# Run a Backstage software template

Base: `https://{backstage-host}/api/scaffolder`, paths under `/v2`. Bearer token required.
Executing a template creates real things in real systems — repositories, pull requests, cloud
resources. Treat it as the highest-consequence operation Backstage exposes.

## Steps

1. **Read the parameter contract.**
   `GET /v2/templates/{namespace}/{kind}/{name}/parameter-schema` (`GetTemplateParameterSchema`)
   returns the JSON Schema for this template's inputs. Never guess parameter names.

2. **Rehearse.** `POST /v2/dry-run` (`DryRun`) with the template YAML, the values and any input
   files. It runs the steps and returns the log plus the resulting file tree WITHOUT creating
   anything. MCP equivalent: `scaffolder.dry-run-template` (readOnly, idempotent). Do this before
   any first execution and any time the values changed.

3. **Execute.** `POST /v2/tasks` (`Scaffold`) with `{ templateRef, values, secrets? }`. Returns a
   task id. MCP equivalent: `scaffolder.execute-template`, annotated `destructiveHint: true` and
   `idempotentHint: false` — a retried call starts a SECOND task. There is no idempotency key on
   this API, so on a network timeout list tasks (`GET /v2/tasks`) and look for yours rather than
   re-posting.

4. **Follow it.** `GET /v2/tasks/{taskId}` (`GetTask`) for status, `GET /v2/tasks/{taskId}/events`
   (`StreamLogsPolling`) with an `after` cursor for the log. MCP equivalent:
   `scaffolder.get-scaffolder-task-logs`.

5. **Reversal, and its limit.** `POST /v2/tasks/{taskId}/cancel` (`CancelTask`) stops a task that
   has not reached a terminal state — that is the whole window: once the task completes, cancel no
   longer applies. Cancelling stops Backstage's execution; it does NOT undo side effects an
   already-completed step created in GitHub, GitLab or a cloud provider. Clean those up in the
   system that owns them. `POST /v2/tasks/{taskId}/retry` (`Retry`) re-runs a failed task rather
   than reversing it.
   **Neither cancel nor retry is exposed as an MCP tool.** An agent that fires
   `scaffolder.execute-template` has no MCP path to stop it — plan for that before calling it.

## Rules

- Never pass a value into `secrets` that the caller did not explicitly supply for this run.
- A 409 `ConflictError` on cancel or retry means the task is not in a compatible state — re-read
  `GetTask` and act on the current status.
- A 403 `NotAllowedError` is the Permissions framework, not a bad token.
