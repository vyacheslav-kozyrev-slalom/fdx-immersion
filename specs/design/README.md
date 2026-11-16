# Feature Design

Design documents explain how an approved requirement will be realized. They connect business intent to component responsibilities, data movement, contracts, and operational constraints without duplicating the requirement.

## What belongs here

Create a document named `DES-###-short-name.md` for a feature or cohesive set of requirements. Start with [DES-template.md](./DES-template.md) and include, as applicable:

- Summary and linked requirement IDs
- Design goals and constraints
- Components and their responsibilities
- Data flow, ownership, and model changes
- API contracts and external integrations
- Security, privacy, and non-functional considerations
- Risks, mitigations, alternatives, and open decisions
- Validation approach

Use the shared [architecture overview](../../docs/architecture/overview.md) for cross-cutting system boundaries and deployment direction. Put durable cross-feature decisions in [ADRs](../../docs/adr/README.md), then link them from relevant designs.

## Design guidance

- Keep design proportional to the requirement; do not design unapproved candidate features as committed scope.
- Label decisions as confirmed, proposed, or open and identify who or what must resolve open items.
- For the prototype, keep React screens independent of MSW; use typed API contracts so mock responses can later be replaced by an ASP.NET Core API.
- Do not assume production identity, source systems, storage, hosting, or AI use until validated.
- Specify how the design handles errors, missing data, and relevant security/privacy constraints.

## Workflow

Review the design against its linked requirement before creating implementation tasks. If a design changes user-visible behavior or scope, revise the requirement and acceptance criteria as well.

See the [specs workflow](../README.md) for lifecycle and traceability conventions.
