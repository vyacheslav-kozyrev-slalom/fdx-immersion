# Evergreen Senior Living Intelligence Hub

This repository is the source of truth for requirements, design, implementation, and validation of a senior living care and operations intelligence hub. The immediate goal is a clickable prototype; a secure production product is a later phase and remains subject to discovery.

## Product direction

The prototype demonstrates the five-screen journey **Identify → Understand → Act → Hand off** for Executive Directors, Directors of Nursing, and related staff:

1. Community command center
2. Resident/family concern detail
3. Resident detail and follow-up
4. Workforce risk detail
5. Shift handoff summary

The prototype uses **React + TypeScript**, a typed HTTP API client, and **Mock Service Worker (MSW)** to return synthetic API responses. The longer-term technology direction is Microsoft-focused: .NET, React/TypeScript, Azure, and optionally Azure AI Foundry. Production integrations, persistence, security, and AI use are not yet approved design commitments.

Use synthetic data only in the prototype. Do not present mock actions as saved or sent, use unsupported predictive scores, or treat the prototype role selector as a security control.

## Start here

- [Business feature inventory](specs/requirements/REQ-001-senior-living-intelligence-hub.md) — prototype features, acceptance criteria, discovery candidates, and open business questions.
- [Architecture overview](docs/architecture/overview.md) — proposed prototype and production architecture, boundaries, risks, and open decisions.
- [Client description](docs/client-description.md) — background and session findings; distinguishes client-stated facts from assumptions and items to confirm.
- [Use case and prototype direction](docs/use-case.md) — user roles, product concept, screens, and prototype success criteria.
- [Roadmap](docs/roadmap.md) — project phases and priorities.
- [Feature development workflow](docs/development-workflow.md) — workspace slash commands, specialist agents, commit/review behavior, and human approval gates.
- [Copilot repository guidance](.github/copilot-instructions.md) — spec-driven development expectations.

## Repository map

| Path | Purpose |
|---|---|
| `.github/` | Repository-specific contributor and Copilot instructions |
| `docs/` | Client context, roadmap, architecture, and architecture decision records |
| `specs/requirements/` | Business and product requirements |
| `specs/design/` | Technical design documents |
| `specs/tasks/` | Implementation task breakdowns |
| `src/` | Application implementation |
| `tests/` | Automated and manual verification |

Each folder has a README with its local conventions.

## Development workflow

1. Confirm the business outcome and scope in a requirement; record assumptions and unresolved questions.
2. Design the solution and document material architecture decisions.
3. Break the approved design into traceable, testable tasks.
4. Implement the smallest complete change in `src/`.
5. Validate acceptance criteria in `tests/` and update related documentation.

Requirements are the source of product intent. Architecture documents and code should link back to them. Do not infer client commitments from illustrative values or placeholders in the discovery notes.

## Build and run status

The repository currently contains specifications and documentation but does not yet define an application package, dependency installation, or run command. Add the appropriate quick-start instructions here when the prototype's project scaffolding is established.
