# Documentation

This folder contains product context and technical guidance used to make requirements and design decisions. Treat client-session notes as discovery evidence, not as a substitute for confirmed requirements.

## Documents

- [Client description](./client-description.md) — Evergreen's operating context and discovery findings. Items are identified as stated, derived, assumed, or needing review; retain those distinctions when reusing the information.
- [Use case and prototype direction](./use-case.md) — proposed intelligence-hub concept, primary users, five-screen prototype flow, and prototype success criteria.
- [Project roadmap](./roadmap.md) — high-level project phases.
- [Architecture overview](./architecture/overview.md) — prototype boundary, MSW/API contract approach, production direction, risks, and open technical decisions.
- [Architecture README](./architecture/README.md) — architecture documentation principles and change process.
- [Architecture decision records](./adr/README.md) — how to record significant decisions and their rationale.

## Keeping documentation reliable

- Distinguish client-confirmed facts from derived figures, assumptions, placeholders, and external research.
- Link technical decisions to the requirements and business outcomes they support.
- Update the architecture overview when a decision changes component boundaries, data flows, integrations, security, or deployment.
- Use an ADR when a consequential choice needs a durable rationale and alternatives.
- Keep roadmap scope and dates explicit about whether they are confirmed or proposed.

For business needs and acceptance criteria, use [specs/requirements](../specs/requirements/README.md). For feature-level technical designs, use [specs/design](../specs/design/README.md).
