# Feature Development Workflow

This repository uses a human-gated workflow from business requirements through UX, implementation, and verification. Workspace commands are defined under `.github/skills/`; focused agents are defined under `.github/agents/`.

## End-to-end sequence

```text
/specify
  -> human approves stories
/ux
  -> UX Review agent
  -> Visual Design Review agent
  -> human approves revised screens
/plan
  -> human approves implementation tasks
/implement
  -> Task Implementer agent commits each task separately
  -> Code Reviewer agent reviews the implementation diff
  -> fixes are committed and re-reviewed when needed
/test
  -> Unit Test Author agent
  -> E2E Test Author agent
  -> User Verification Guide agent
  -> automated tests run where feasible
  -> workflow ends
```

Each phase is started explicitly by the user. Commands and agents must stop at the relevant approval gate; no phase may assume approval or automatically start the next command.

## Commands

| Command | Purpose | Human gate |
|---|---|---|
| `/specify` | Ask focused questions as needed and create or refine requirements and independently testable stories. | Review and approve stories before `/ux`. |
| `/ux` | Create SVG feature screens and design notes under `specs/design/screens/` from approved stories. | Run both review agents, then approve revised screens before `/plan`. |
| `/plan` | Create traceable, dependency-aware implementation tasks from approved requirements and screens. | Review and approve tasks before `/implement`. |
| `/implement` | Implement each approved task through a dedicated agent and commit it separately; request a read-only code review and fix actionable findings. | User starts implementation only after approving tasks. `/test` is still separately invoked afterward. |
| `/test` | Generate unit tests, E2E tests, and a user verification checklist; run automated tests where feasible. | Review results and complete any listed manual verification. This is the final workflow phase. |

## Review and implementation agents

| Agent | Invocation | Responsibility |
|---|---|---|
| **UX Review** | User invokes from the agent picker after `/ux`. | Improve usability and requirement coverage in the SVG screens and design notes. |
| **Visual Design Review** | User invokes after UX Review. | Refine visual hierarchy, consistency, readability, and contrast without changing approved behavior. |
| **Task Implementer** | Invoked by `/implement`, once per task. | Implement, validate, and commit only one approved task at a time. |
| **Code Reviewer** | Invoked by `/implement` after task commits and after each fix round. | Review the diff read-only and report actionable findings. |
| **Unit Test Author** | Invoked by `/test`. | Add unit/component coverage for behavior and acceptance criteria. |
| **E2E Test Author** | Invoked by `/test`. | Add browser-level tests for the approved user journey using synthetic data. |
| **User Verification Guide** | Invoked by `/test`. | Create manual, user-observable verification steps under `tests/manual/`. |

## Commit and review policy

- The implementation agent commits one task at a time with a task ID in the commit message.
- Stage only files belonging to that task; leave unrelated user changes untouched.
- Include the repository-required Copilot co-author trailer in agent-created commits.
- Review the implementation diff against the pre-implementation baseline. Code review is read-only.
- If review finds actionable issues, make narrow follow-up fixes in separate commits and re-review. Stop after two fix/review rounds and report unresolved issues.
- Never amend or rewrite existing commits in this workflow.

## Technology and data boundaries

- Prototype: React + TypeScript, typed HTTP API contracts/client, MSW browser handlers, and synthetic fixtures.
- Production direction: ASP.NET Core/.NET and Azure; AI Foundry is optional and requires separate approval.
- MSW is not a production API, security boundary, persistence layer, or silent fallback.
- Do not use real resident, family, health, or employee data in screens, fixtures, logs, or tests.
- Keep health and employee-sensitive data out of AI calls until the data flow and all required approvals are confirmed.
- See the [architecture overview](./architecture/overview.md) and [repository Copilot instructions](../.github/copilot-instructions.md).

## Current validation limitation

The application scaffold and test tooling are not yet established. `/test` must use commands from actual project manifests and configuration; it must report when tests cannot run rather than inventing a runner or claiming success.
