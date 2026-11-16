# Architecture

This folder is the home for the product's high-level architecture: component boundaries, data movement, deployment assumptions, and material technical risks. Keep the architecture aligned with business requirements and clearly distinguish confirmed decisions from proposals.

## Current direction

- **Immediate priority:** Build a browser-based clickable prototype for the five-screen “Identify → Understand → Act → Hand off” journey.
- **Prototype stack:** React + TypeScript, a typed HTTP API client, and Mock Service Worker (MSW) to return synthetic API responses.
- **Reuse goal:** Keep the prototype's product-facing API contracts representative of the later ASP.NET Core API, so the UI can switch from MSW to the real service with minimal changes.
- **Production direction:** .NET, React/TypeScript, Azure, and optionally Azure AI Foundry. Production components and services in the overview are candidates, not approved implementation choices.
- **Business traceability:** The prototype maps to [REQ-001 feature inventory](../../specs/requirements/REQ-001-senior-living-intelligence-hub.md).

## Architecture principles

1. Keep the clickable prototype small; do not build production infrastructure before it is needed.
2. Use synthetic data only in the prototype. MSW is a development mock layer, never a production API, security boundary, persistence layer, or silent fallback.
3. Keep UI components independent of mock implementation. The UI calls typed API contracts; MSW and the future ASP.NET Core API implement the same product-facing behavior.
4. In production, enforce authentication, role/community authorization, and source-data access in the server-side API—not in the UI.
5. Treat resident health and employee information as sensitive. Minimize data movement and require privacy/security approval before integrating sources or using AI.
6. Make concerns explainable through observable signals. Do not imply validated predictions or automate clinical, staffing, or employment decisions.
7. Keep Azure AI Foundry optional; core viewing and navigation must remain available when AI is not used or unavailable.
8. Surface missing, stale, and unavailable data instead of presenting it as current and certain.

## Documents

- [Architecture overview](./overview.md) — proposed prototype architecture, production direction, data flow, deployment assumptions, technical requirements, risks, and open decisions.

## Expected contents

Add or update architecture documentation when a material design decision or system boundary is established:

- Architecture overview and component responsibilities
- Module and service boundaries, dependency flow, and API/service interaction model
- Data movement, source-system integrations, and data ownership
- Deployment and environment assumptions
- Security, privacy, availability, and other non-functional constraints
- Risks, trade-offs, and unresolved decisions

Use focused documents for substantial topics (for example, API contracts or deployment topology) and link them from the overview. Feature-specific technical designs belong in [specs/design/](../../specs/design/); business needs and acceptance criteria belong in [specs/requirements/](../../specs/requirements/).

## Change process

1. Trace architectural changes to an approved requirement or a clearly identified discovery question.
2. Mark each choice as **confirmed**, **proposed**, or **open**; do not turn assumptions from client notes into commitments.
3. Update the overview and any affected focused documents together.
4. For production choices, document the alternatives and trade-offs where they materially affect privacy, operations, cost, or delivery.
5. Keep diagrams and descriptions consistent with the prototype/production boundary and the current code.

## Open production decisions

Before committing to production architecture, confirm the source systems and supported interfaces, identity and role model, community-level access, Azure tenant and landing zone, hosting and networking requirements, data retention and ownership, and whether AI Foundry may process the relevant data. See the [architecture overview](./overview.md#decisions-still-required-before-production-design) for the current decision list.
