# Application Source

This folder is for implementation code. The immediate delivery target is a React + TypeScript clickable prototype whose UI calls a typed HTTP API client; Mock Service Worker (MSW) returns synthetic responses during the prototype.

## Prototype implementation guidance

- Organize code around the product experience and clear responsibilities rather than introducing unnecessary service layers.
- Keep screen components independent of mock-specific behavior. Screens should call application-level client functions and render the typed results.
- Keep API contracts, client requests, MSW handlers, and synthetic fixtures distinct and easy to replace or validate.
- Enable MSW only in the prototype/development environment. Do not silently use synthetic data in a production build or after a real API error.
- Keep the role selector demonstrational; it is not authentication or authorization.
- Use synthetic resident, family, and workforce examples only. Never copy client or production personal/health data into fixtures.
- Make mock interactions visibly non-persistent; do not tell users a follow-up was sent, assigned, or saved when it was not.

## Production direction

The candidate later architecture is a React/TypeScript client and an ASP.NET Core API hosted in Azure. The API would own authentication/authorization, approved data access, integration orchestration, and any persisted workflow actions. Source-system adapters and optional Azure AI Foundry capabilities require further design and approval.

Keep the frontend API contract stable enough to replace MSW with the real API without coupling UI components to individual upstream systems. The .NET service should implement and validate the same contract; it does not need to consume TypeScript source directly.

## Suggested organization

Choose the actual layout when project scaffolding is added. A possible prototype layout is:

```text
src/
  web/
    features/
    api/
    mocks/
    app/
```

Add a separate API project only when production or a separately executable backend is in scope. Avoid creating empty folders or layers before a requirement needs them.

## Traceability

Every significant behavior should trace to an approved requirement and, where needed, a design and task in `specs/`. The current business scope is in [REQ-001](../specs/requirements/REQ-001-senior-living-intelligence-hub.md); architecture boundaries are described in [docs/architecture](../docs/architecture/README.md).
