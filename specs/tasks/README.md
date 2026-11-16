# Implementation Tasks

Tasks break an approved requirement and design into small, executable, independently verifiable pieces of work. They are the work plan—not a replacement for the requirement or technical design.

## What belongs here

Create task documents named `TASK-###-short-name.md` using [TASK-template.md](./TASK-template.md). Each task should state:

- Objective and linked requirement/design IDs
- Scope and implementation steps
- Dependencies and sequencing constraints
- Acceptance checks and validation method
- Definition of done, including documentation updates when needed

## Task quality

- Keep each task bounded and outcome-oriented; split work when it cannot be reviewed or validated as a coherent unit.
- Record only real prerequisites in dependency lists.
- Include test work for applicable behavior and data/error states.
- Identify assumptions and blockers instead of encoding guesses as implementation requirements.
- Keep tasks consistent with the approved design and preserve the prototype/production boundary.

For the clickable prototype, likely work may include React screens, typed API contracts/client, MSW handlers and synthetic fixtures, navigation, and browser validation. Create these tasks only after scope and design are agreed.

## Workflow

1. Confirm the parent requirement and design are reviewed.
2. Break the design into sequenced tasks with clear ownership boundaries where useful.
3. Implement and validate tasks against their linked acceptance criteria.
4. Update task status and record test evidence in the project's chosen workflow.

See the [specs workflow](../README.md) for naming and end-to-end traceability.
