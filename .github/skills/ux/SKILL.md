---
name: ux
description: 'Create SVG feature screens and a user flow from human-approved stories. Use /ux only after the user approves requirements produced by /specify.'
argument-hint: 'Approved requirement ID(s) and any UX constraints'
user-invocable: true
---

# Create UX Screens

Create screen artifacts for stories the user has explicitly approved. The immediate product is a React + TypeScript clickable prototype backed by synthetic MSW responses; design the user experience, not implementation code.

## Procedure

1. Confirm the referenced requirement/story set is approved by the user. If approval is not clear, ask before producing screens.
2. Read the approved requirements, architecture overview, use-case description, and any existing screen artifacts.
3. Map each story's primary flow, key decisions, states, and accessibility needs to a minimal set of screens.
4. Generate editable SVG screen artifacts under `specs/design/screens/`. Give each file a stable, descriptive name and include a concise design note mapping it to story IDs, actions, and states.
5. Use synthetic names and content only. Avoid unsupported predictive probabilities or claims that actions persist.
6. Stop and report the artifacts and review sequence.

## Gate

Do not create implementation tasks or code. The user must run the **UX Review** agent first, then the **Visual Design Review** agent. After reviewing the revised screens, the user explicitly approves them and starts `/plan`.

## Screen quality

- Represent the user's goal and primary action clearly.
- Include loading, empty, missing/stale-data, and error states where relevant to the flow.
- Prefer accessible contrast, legible type, semantic labels, and clear focus/order cues.
- Keep SVGs usable as review artifacts and do not assume production APIs, persistence, or security controls.

## Output

Report the SVG and design-note paths, the stories represented, and any unresolved UX questions. Leave the next action to the user.
