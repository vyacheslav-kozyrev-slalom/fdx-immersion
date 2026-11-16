---
name: specify
description: 'Create or refine business requirements and user stories from a feature request. Use /specify before UX design or implementation; ask focused questions when scope, users, or acceptance criteria are unclear.'
argument-hint: 'Feature request, existing requirement, or backlog item'
user-invocable: true
---

# Specify a Feature

Turn a feature request into a human-reviewable requirement and story breakdown. This command is the start of the product workflow.

## Procedure

1. Read the relevant business context, existing requirements, and project instructions before drafting.
2. Identify users, problem, desired outcomes, scope boundaries, dependencies, and assumptions.
3. Ask the user focused clarifying questions when answers could materially change scope, user experience, or acceptance criteria. Do not invent client commitments.
4. Create or update a requirement in `specs/requirements/` using the local template. Break scope into independently valuable stories with unique requirement/story IDs and testable acceptance criteria.
5. Link decisions to source documents and label assumptions and unresolved questions.
6. Summarize the stories and open questions, then stop for human review and approval.

## Gate

Do not invoke `/ux`, create screens, or begin planning automatically. Continue only when the user explicitly approves the generated stories and starts the next command.

## Quality bar

- Write business-facing outcomes, not implementation instructions.
- Keep each story small enough to design and verify.
- State exclusions and dependencies; avoid expanding adjacent discovery candidates into committed scope.
- Preserve existing user-authored work and requirement identifiers.

## Output

Report the requirement path, story list, assumptions, and decisions still needing user input. Do not claim approval on the user's behalf.
