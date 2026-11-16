---
name: plan
description: 'Break human-approved requirements and approved UX screens into sequenced, testable implementation tasks. Use /plan only after both screen review agents have run and the user approves the screens.'
argument-hint: 'Approved requirement IDs and screen artifact paths'
user-invocable: true
---

# Plan Implementation Tasks

Create a task breakdown aligned to approved requirements, reviewed screens, and the Microsoft technology direction.

## Procedure

1. Confirm the user explicitly approved the requirements and the revised screens after UX and visual design review. If unclear, stop and ask.
2. Read the linked requirements, approved SVGs/design notes, architecture overview, repository instructions, and any existing tasks.
3. Decompose the work into small, dependency-aware tasks. Cover the React/TypeScript experience, typed API contracts/client, MSW handlers and synthetic fixtures, accessibility, and tests as required by the approved scope.
4. Create task documents under `specs/tasks/` using the local template. Link each task to requirement/story IDs and screen artifacts; state objective, boundaries, dependencies, acceptance checks, and validation.
5. Separate prototype work from production-only work. Do not add production integrations, persistence, Azure services, or AI Foundry tasks unless the user has approved them.
6. Present the ordered task list and dependencies, then stop for human approval.

## Gate

Do not invoke `/implement` or modify application code. The user must approve the task list and explicitly start `/implement`.

## Output

Report task paths, ordering/dependencies, traceability, assumptions, and decisions still open. Do not claim task approval on the user's behalf.
