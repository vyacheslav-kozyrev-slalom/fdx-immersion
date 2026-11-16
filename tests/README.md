# Verification and Tests

This folder contains automated and manual evidence that implementation meets its requirements. Tests should verify user-visible behavior and acceptance criteria, not merely mirror internal code structure.

## Prototype validation

The initial product is a React + TypeScript clickable prototype using MSW for synthetic HTTP responses. Validate:

- The five-screen journey: command center, resident/family concern, resident detail/follow-up, workforce risk, and shift handoff.
- The prioritized issue can be identified within the prototype's stated 30-second goal.
- Surfaced concerns include understandable contributing signals and clear next steps.
- Role-based presentation changes the example appropriately without implying actual access control.
- Mock responses cover useful states, including empty, missing, stale, and error responses where applicable.
- Prototype-only actions are not presented as persisted or sent.
- Production builds do not enable MSW or silently fall back to mock data.

Use synthetic test data only. Do not add real resident, family, or employee information to fixtures, test output, screenshots, or logs.

## Test levels

Select tools when implementation scaffolding is established; no test runner is prescribed yet.

- **Unit/component:** Validate presentation and focused behavior for screens and shared UI.
- **API contract/mock:** Check that client request/response types and MSW handlers agree, including error and boundary cases.
- **End-to-end:** Exercise the prototype's primary user journey in a browser.
- **Production integration:** When a real ASP.NET Core API and integrations exist, test authentication, authorization, community scoping, source-system failures, and persistence independently from prototype mocks.

## Traceability and evidence

For each requirement, identify the scenarios that verify its acceptance criteria. Record how to run the test, expected result, and any relevant environment or fixture assumptions. Link test evidence to the applicable requirement and task.

Business acceptance criteria are in [specs/requirements](../specs/requirements/README.md); architecture constraints are in [docs/architecture](../docs/architecture/README.md).
