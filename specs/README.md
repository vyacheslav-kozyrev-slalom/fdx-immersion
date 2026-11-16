# Product and Engineering Specifications

This folder is the source of truth for what the product must do, how a feature is designed, and how the work is divided and verified. Keep requirements business-readable and keep technical decisions traceable to them.

## Contents

- [Requirements](./requirements/README.md) — user needs, business value, acceptance criteria, edge cases, and dependencies.
- [Design](./design/README.md) — feature-level solution design and component interactions.
- [Tasks](./tasks/README.md) — sequenced implementation work and validation.
- `*-template.md` files — starting structures for new requirement, design, and task documents.

## Workflow

1. **Requirement:** Establish the need, users, scope, success criteria, and unresolved questions.
2. **Design:** Describe the solution boundaries, data flow, integrations, risks, and decisions.
3. **Tasks:** Break the approved design into small, traceable implementation and validation steps.
4. **Implementation:** Change application code only within the agreed requirement/design scope.
5. **Verification:** Validate acceptance criteria and record results.

Update the earlier artifacts when scope changes; do not allow code or task lists to silently redefine the requirement.

## Naming and traceability

- Requirements use `REQ-###-short-name.md`.
- Feature designs use `DES-###-short-name.md`.
- Tasks use `TASK-###-short-name.md`.
- Link related artifacts and cite requirement IDs in designs, tasks, and tests.
- Keep identifiers unique within their document type and use stable references rather than duplicating full requirements.

## Current product scope

The current business draft is [REQ-001: Senior Living Care and Operations Intelligence Hub](./requirements/REQ-001-senior-living-intelligence-hub.md). It defines the five-screen clickable prototype and separates broader, unconfirmed business opportunities as discovery candidates.

Technical architecture and phase boundaries are documented in [docs/architecture](../docs/architecture/README.md).
