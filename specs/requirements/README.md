# Requirements

Requirements describe the business problem, intended users, outcomes, and observable behavior the product must support. Write them before designing or implementing a solution.

## What belongs here

Create one Markdown document per feature or cohesive initiative, named `REQ-###-short-name.md`. A requirement should normally include:

- Problem and context
- User story and business value
- Scope and explicit exclusions
- Prioritized user scenarios or acceptance criteria
- Edge cases
- Dependencies, assumptions, and unresolved questions
- Measurable success criteria when appropriate

Start from [REQ-template.md](./REQ-template.md). The [current feature inventory](./REQ-001-senior-living-intelligence-hub.md) is a draft that groups the clickable prototype into backlog-ready business features and records separate discovery candidates.

## Writing and review guidance

- Describe what users need and why; leave implementation choices to design documents.
- Make each acceptance criterion observable and testable.
- Distinguish confirmed facts from assumptions, sample values, and proposals.
- Keep scope, non-goals, and unresolved decisions visible; do not silently assume client approval.
- Prioritize user journeys by value and dependency, not just by screen order.
- Keep a requirement focused enough that it can be designed, implemented, and verified as a coherent increment.

## Traceability

Designs and tasks should reference the relevant `REQ-###` identifiers. Tests should verify the requirement's acceptance criteria. When scope changes, update the requirement first and then review dependent designs and tasks.

See the [specs workflow](../README.md) for the full lifecycle.
