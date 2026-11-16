---
name: test
description: 'Generate unit and end-to-end tests for implemented, approved stories, run automated tests where feasible, and create user-run verification steps. Use /test after implementation and code review.'
argument-hint: 'Requirement/task IDs and implemented feature paths'
user-invocable: true
---

# Generate and Run Tests

After implementation and code review, use focused agents to create unit tests, end-to-end tests, and a manual verification checklist.

## Procedure

1. Confirm implementation and code review are complete. Read the approved requirement, tasks, source changes, repository instructions, package/test configuration, and existing tests.
2. If the test tooling or runnable app is not available, do not invent commands or add arbitrary tooling. Generate appropriate test artifacts only when feasible and clearly report execution blockers.
3. Invoke `unit-test-author` to add tests for the changed logic and acceptance criteria, following existing patterns.
4. Invoke `e2e-test-author` to add end-to-end coverage for the approved user journey, using synthetic data and existing browser tooling.
5. Invoke `verification-guide` to create a concise manual checklist under `tests/manual/` with user-observable steps and expected outcomes.
6. Run the smallest relevant unit and end-to-end test commands available from project manifests/configuration. Report exact commands and pass/fail results. Do not silently rewrite production code to make tests pass.
7. If a failure indicates a likely implementation defect, report it and stop for a fix through the approved implementation workflow; do not mark the feature verified.
8. Present the test artifacts, execution results, and manual verification checklist. This is the end of the defined workflow.

## Boundaries

- Do not add real resident, family, employee, or health data to tests or logs.
- Do not modify product behavior in order to make tests green.
- Test failures and unavailable infrastructure must be surfaced explicitly.
- Do not launch another workflow phase after reporting results.

## Output

Report unit/E2E test files, manual checklist path, commands run, results, and any tests the user still needs to execute.
