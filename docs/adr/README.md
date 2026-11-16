# Architecture Decision Records

Use this folder to record significant technical decisions that affect system structure, technology selection, integrations, data handling, security, or operations. ADRs preserve the decision and its reasoning so later changes can revisit it deliberately.

## When to write an ADR

Create an ADR when a choice:

- Has meaningful consequences for privacy, security, reliability, delivery, or operating cost.
- Affects component boundaries, API contracts, data ownership, or integration strategy.
- Selects or rules out a foundational technology or hosting approach.
- Resolves a recurring or cross-team design question.

Do not use an ADR for routine implementation details or decisions already fully specified by an approved requirement.

## Naming and status

Use sequential names, for example `ADR-001-api-contracts.md`. Suggested statuses:

- **Proposed** — under review; not yet adopted.
- **Accepted** — approved and the current direction.
- **Superseded** — replaced by a later ADR; link to its replacement.
- **Rejected** — considered but not adopted; retain the rationale.

## Required sections

Each ADR should include:

1. **Title and status**
2. **Context** — the problem, constraints, and requirement(s) involved
3. **Decision** — the choice and its scope
4. **Consequences** — benefits, costs, risks, and follow-up work
5. **Alternatives considered** — credible options and why they were not selected

Include date, owners, or links to related design documents when useful. Clearly label assumptions and decisions that still need approval.

## Workflow

1. Capture the question and relevant requirement/design links.
2. Compare viable options, including the cost of deferring a choice.
3. Mark the ADR **Proposed** while review is pending.
4. Update its status when the decision is made and update affected architecture/design documents.
5. When superseding a decision, retain the original ADR and cross-link both records.

See the [architecture overview](../architecture/overview.md) for the current prototype and production direction.
