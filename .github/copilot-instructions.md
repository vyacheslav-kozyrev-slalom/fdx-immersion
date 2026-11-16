# Copilot Instructions for this repository

## Mission

Use this repository as a spec-driven development (SDD) project. Keep requirements, design, and validation aligned with the implementation.

## Technology direction

- **Current priority:** A clickable web prototype using React, TypeScript, a typed HTTP API client, and Mock Service Worker (MSW).
- **Later production direction:** ASP.NET Core/.NET and Azure; Azure AI Foundry is optional and requires separate approval for use cases and data.
- Treat production architecture choices as proposals until confirmed in [the architecture overview](../docs/architecture/overview.md).
- Do not add a framework, package, cloud resource, or service just because it is available; use the simplest option that satisfies an approved requirement.

## Code rules

### React and TypeScript prototype

- Keep UI components focused on presentation and user interaction. Call typed API-client functions rather than embedding fetch logic or MSW-specific behavior in screens.
- Keep API contracts, client code, MSW handlers, and synthetic fixtures clearly separated. Handlers should implement the same request/response behavior expected from the later ASP.NET Core API.
- Prefer explicit types and narrow unions. Avoid `any`, unsafe type assertions, and non-null assertions; validate data at untrusted boundaries.
- Keep state local to the feature that owns it unless sharing is required by a user flow. Avoid introducing global state libraries without a demonstrated need.
- Handle loading, empty, missing/stale-data, and error states explicitly. Do not silently substitute mock data when a request fails.
- Use semantic HTML and accessible controls; preserve keyboard operation, visible focus, and meaningful labels.
- Keep the MSW worker restricted to prototype/development builds. Do not present mocked actions as persisted, sent, or assigned.
- Use synthetic resident, family, and workforce data only. Never copy real personal, health, or employee data into source, fixtures, logs, screenshots, or tests.

### ASP.NET Core/.NET production code (when approved)

- Keep HTTP/API concerns at the service boundary and business rules in testable application/domain code; do not make controllers responsible for integration orchestration or persistence details.
- Enforce authentication, role authorization, and community-level access on the server for every protected operation. A UI role or client-supplied community identifier is not authorization.
- Use dependency injection and asynchronous I/O for external or database operations. Propagate cancellation tokens through request-bound work.
- Validate request contracts at the boundary and return consistent, documented error responses; do not expose stack traces, secrets, or protected data.
- Isolate upstream systems behind adapters and define timeouts and explicit failure behavior. Do not silently treat unavailable source data as current or complete.
- Store secrets in approved Azure secret-management services or managed identity flows; never commit credentials or environment-specific secrets.
- Add dependencies only when required by an approved design. Follow the repository's configured formatting, analyzers, and target framework once established; do not invent versions or conventions.

### Azure AI Foundry (only when approved)

- Call AI services only from a trusted server-side component, never directly from the browser.
- Do not send PHI or employee-sensitive information until the data flow, service configuration, contractual terms, and security/privacy approvals are confirmed.
- Keep AI optional for core product workflows. Show supporting signals, handle unavailable or invalid model output explicitly, and require human review before generated content is acted on or communicated.
- Do not implement autonomous clinical, staffing, or employment decisions or unsupported individual risk probabilities.

## Working principles

1. Start from a requirement, not from code.
2. Write clear user stories and acceptance criteria before implementation.
3. Prefer small, tested changes.
4. Update docs when behavior or design changes.
5. Keep architectural decisions traceable in ADRs.

## Required workflow

- Requirements live under `specs/requirements/`
- Design decisions live under `specs/design/`
- Execution tasks live under `specs/tasks/`
- Implementation lives under `src/`
- Verification lives under `tests/`
- Follow the human-gated command sequence in [the development workflow](../docs/development-workflow.md): `/specify` → `/ux` → UX Review → Visual Design Review → `/plan` → `/implement` → `/test`.
- Never infer approval or automatically advance to the next phase. Each command must stop at its documented human approval gate.
- `/implement` commits each approved task separately, reviews the resulting diff with the read-only Code Reviewer agent, and fixes/re-reviews actionable findings.
- `/test` is the final phase: generate and run unit/E2E tests where feasible and provide a user verification checklist.

## Expectations for Copilot

- Propose solutions that follow the project’s architecture and design constraints.
- Ask clarifying questions when requirements are ambiguous.
- Add or suggest test coverage for behavior changes; test at the smallest level that proves the acceptance criteria.
- Keep comments and documentation concise and useful.
- Avoid writing code that is not traceable to a requirement or task.
- Do not claim a build, test, or runtime check passed unless it was actually run.

## Default project quality bar

- The code should be readable and idiomatic.
- Business logic should be covered by tests where practical.
- Hidden assumptions should be written down in docs or ADRs.
- Changes should be reversible and easy to reason about.
- Update relevant requirements, design, README, and architecture documents when behavior or technical decisions change.

## Build and test commands

The application scaffold and test tooling have not yet been established. Do not invent install, build, lint, or test commands; once the React/.NET projects are created, document and use the commands defined by their manifests and CI configuration.
