# Senior Living Care and Operations Intelligence Hub — Backlog Feature Inventory

**Status:** Draft for backlog refinement
**Date:** 2026-11-16
**Sources:** [Client description](../../docs/client-description.md), [Use case](../../docs/use-case.md)

## Problem

Care and operations signals are spread across records, schedules, complaints, and handoffs. Community leaders and frontline staff can struggle to see what needs attention, understand why, and pass relevant information to the next shift. Evergreen also has broader business concerns—including low occupancy, staffing turnover, and rising operating costs—but the available documents do not establish that the prototype will address those problems.

## User story

As a senior living care or operations leader, I want one role-aware view of emerging care, family-engagement, and workforce concerns, with understandable evidence and next steps, so that my team can respond earlier and maintain continuity of care.

## Business value

- Focus staff attention on meaningful exceptions instead of requiring them to interpret a wall of metrics.
- Make surfaced concerns understandable and actionable.
- Improve continuity between shifts while limiting information to the people who need it.
- Test the intelligence-hub concept before committing to predictive models or broader operational integrations.

## Scope baseline

- **Discovery method:** Review of the two supplied business documents.
- **Items reviewed:** 2 documents.
- **Prototype scope:** The five-screen flow in the use case: command center, care risk detail, resident detail, workforce risk detail, and shift handoff summary.
- **Recommended backlog breakdown:** 6 prototype-ready business features below.
- **Not treated as committed scope:** Marketing/intake, occupancy growth, referral management, financial optimization, and facilities management. These appear as business context or hypotheses in the client description, but are not part of the five-screen prototype flow.

## Users and priority

- **Primary prototype users:** Executive Directors and Directors of Nursing.
- **Related users:** Clinical managers and care coordinators; HR, staffing and scheduling teams; shift nurses and other care staff.
- **Priority convention:** P1 means required to demonstrate the prototype’s core “Identify → Understand → Act → Hand off” story. This does not establish a production release priority.

## Backlog features

### REQ-001 — Community command center (P1)

**Business outcome:** A leader can quickly identify the most important care, family, workforce, and operational items needing attention.

**User story:** As an Executive Director or Director of Nursing, I want a prioritized community snapshot so that I can see what needs my attention without searching separate reports.

**Acceptance criteria:**

1. Given the user opens the command center, when the view loads, then it presents a prioritized “Needs your attention” area and a concise current-day snapshot.
2. Given the view contains care and workforce concerns, when the user scans it, then the categories are distinguishable and the highest-priority item is identifiable in under 30 seconds.
3. Given a concern is selected, when the user opens it, then the command center takes the user to the relevant detail view.

**Edge cases:** No items need attention; some signal categories have no available data; multiple items have the same priority.

**Dependencies:** Agreed example data and priority language; prototype navigation and content for the detail features below.

### REQ-002 — Explainable resident and family concern detail (P1)

**Business outcome:** Care leaders can understand why a resident or family concern was surfaced and what evidence supports it.

**User story:** As a care leader, I want a plain-language explanation and relevant recent activity for a resident or family concern so that I can decide what follow-up is appropriate.

**Acceptance criteria:**

1. Given a resident or family concern is selected, when the detail view opens, then it explains the concern using observable contributing signals and relevant recent activity.
2. Given the concern is based on multiple signals, when the user reviews it, then the signals are presented in understandable language rather than as an unexplained score.
3. Given the example includes care-related information, when it is displayed, then the view is framed for an authorized care role and does not expose unrelated resident information.

**Edge cases:** There is insufficient evidence to explain a concern; activity sources conflict; recent activity is unavailable.

**Dependencies:** Approved sample signals and activity timeline. The documents do not confirm which systems contain these signals or whether the data can be combined.

### REQ-003 — Resident detail and follow-up (P1)

**Business outcome:** A care team member can move from understanding a concern to a clear follow-up action.

**User story:** As a care team member, I want to review the resident context and record or assign an appropriate follow-up so that a surfaced concern can lead to accountable action.

**Acceptance criteria:**

1. Given the user opens a resident from a concern, when the resident detail is shown, then it provides the context needed to understand the concern without presenting unrelated information.
2. Given the user identifies a needed follow-up, when they choose an available action, then the prototype makes the action and its intended owner or recipient clear.
3. Given no follow-up action is appropriate or available, when the user reviews the detail, then the view does not imply that an action was completed.

**Edge cases:** The resident has no relevant detail available; an action has no assigned owner; the user lacks authorization for some information.

**Dependencies:** Product decision on whether “assign follow-up” and “contact family” are clickable demonstrations or real workflow capabilities. The use case suggests these actions but does not define their operational behavior.

### REQ-004 — Explainable workforce risk detail (P1)

**Business outcome:** Operations and workforce leaders can investigate workforce strain and see its contributing conditions.

**User story:** As an operations or workforce leader, I want to see relevant staffing conditions together so that I can understand where a team may need attention.

**Acceptance criteria:**

1. Given a team or shift has a workforce concern, when the user opens its detail, then the view can show relevant observable signals such as overtime, open shifts, schedule changes, turnover, and coverage.
2. Given several workforce signals contribute to a concern, when the user reviews the detail, then the explanation describes the contributing conditions in plain language.
3. Given no validated predictive model has been established, when the concern is displayed, then it uses explainable status language and does not claim a probability that a named employee will leave.

**Edge cases:** Staffing signals are missing, stale, or contradictory; the team has no open shifts; coverage targets have not been defined.

**Dependencies:** Representative workforce data and agreed definitions for overtime, coverage, schedule changes, and turnover. The figures in the use case are examples, not confirmed Evergreen data.

### REQ-005 — Role-appropriate shift handoff summary (P1)

**Business outcome:** The next shift receives a concise, relevant summary of what changed and what needs monitoring.

**User story:** As a shift nurse or operations staff member, I want a handoff summary tailored to my role so that I can continue relevant care and operational follow-up.

**Acceptance criteria:**

1. Given a shift handoff is available, when the next shift opens it, then it highlights residents needing attention, what changed, and what to monitor.
2. Given community updates are relevant, when the handoff is shown, then it can include operational updates such as maintenance issues, staffing changes, or agency assignments.
3. Given a user views a handoff, when the user needs more context, then they can identify how to view the full handoff.
4. Given the handoff includes resident health information, when it is displayed, then access is limited to the intended, authorized care audience.

**Edge cases:** There are no updates for the shift; an update is incomplete; the summary contains information not relevant or authorized for the receiving role.

**Dependencies:** Agreement on handoff content, recipients, and source information. The client description says nurses use medical-record software; paper-based notes in the use case are not confirmed and must not be assumed.

### REQ-006 — Role-based relevance across the hub (P1)

**Business outcome:** Each user sees information relevant to their responsibilities rather than an identical, undifferentiated dashboard.

**User story:** As a hub user, I want concerns and detail presented in a way that fits my role so that I can focus on the information and actions relevant to me.

**Acceptance criteria:**

1. Given two different roles view the same underlying example, when each opens the hub, then the emphasis or detail can differ to match their responsibilities.
2. Given a user views a care or workforce concern, when the view is tailored, then role relevance does not bypass access restrictions for resident health information.
3. Given a role has not been defined for the prototype, when that user opens the hub, then the prototype does not imply unsupported permissions or responsibilities.

**Edge cases:** A user has multiple responsibilities; no role is available; role-specific views would otherwise omit information needed for a safe handoff.

**Dependencies:** Agreed prototype personas and role-specific examples. The role examples in the use case are illustrative, not a confirmed access-control matrix.

## Cross-cutting constraints

- Every surfaced concern should have understandable evidence or contributing signals.
- Use status language such as “High attention” rather than predictive percentages unless a model has been validated.
- Apply need-to-know handling to resident health information; the client description identifies HIPAA and resident privacy as concerns.
- Do not use electronic health record data for marketing or intake features without the required authorization and privacy review.
- Treat illustrative names, counts, rates, thresholds, and dates in either source as sample values unless confirmed by Evergreen.

## Candidate discovery backlog — not yet committed

These are supported business problem areas or hypotheses in the client description, but are outside the five-screen prototype flow. Refine them into separate requirements only after confirming priorities, data availability, users, and scope.

| Candidate feature | Business need / evidence | Discovery needed |
|---|---|---|
| Occupancy and inquiry-to-move-in visibility | Occupancy is reported at about 78%, against a stated 88–90% target; intake and follow-up rely on an antiquated, basic CRM and anecdotal tracking. | Confirm occupancy by community, funnel stages, data sources, and whether intake/marketing belongs in this product. |
| Referral and local outreach management | Many new residents reportedly come through informal referrals; outreach is managed locally and does not roll up centrally. | Confirm desired referral workflows, owners, measurement, and whether paid marketing or incentives are in scope. |
| Workforce retention and staffing operations | The client reports 38% staff turnover; the prototype covers workforce signals, but not workforce interventions. | Confirm headcount, role/community breakdown, turnover definitions, staffing data, and which actions teams may take. |
| Operating-cost and procurement insights | Rising food, staffing, and energy costs are described; some purchasing is centralized and facilities work is mostly local. | Confirm the target cost categories, baselines, owners, available financial/operations data, and business value. |
| Family feedback and communication | The client reports no official post-move-in family channel and no standardized feedback; the prototype uses family concern signals. | Confirm feedback capture and communication processes, consent/privacy needs, and how this relates to the hub. |

## Explicitly outside this prototype

- Automated clinical decisions, diagnoses, or resident care recommendations.
- Unvalidated predictive risk scores or claims about a specific person's future behavior.
- Production integrations, data migrations, or a full CRM, scheduling, EHR, or facilities-management implementation.
- Marketing campaigns, referral incentives, occupancy optimization, ROI guarantees, or facilities investment decisions.

## Success criteria

1. A representative Executive Director or Director of Nursing can identify the top issue in under 30 seconds.
2. Every concern shown in the prototype includes understandable evidence or contributing signals.
3. Each care and workforce detail view makes a relevant next step clear without implying an uncompleted action.
4. The handoff demonstrates role-appropriate continuity for the next shift.
5. In prototype review, users recognize the concept as an actionable intelligence hub rather than another reporting dashboard.

## Decisions and open questions for backlog refinement

1. Is the first deliverable the five-screen care/workforce prototype, or should the first backlog instead prioritize the client's stated occupancy and intake concerns?
2. Which business problem is the top outcome: occupancy, staffing/retention, operating costs, or care/family experience? The client description says this was not ranked.
3. Are assignment, family contact, and handoff actions prototype-only, or are real workflow capabilities expected?
4. What validated data sources and access rules are available for resident/family signals and workforce signals?
5. Are the example workforce thresholds and signals illustrative only? Confirm actual definitions and targets before implementation.
6. Confirm whether the handoff is based on existing electronic medical-record workflows; do not assume paper notes.
7. Confirm whether the broader candidate areas belong in the same product and release.

## Requirement quality check

- [x] Feature requirements have unique, sequential REQ identifiers.
- [x] Each prototype feature has a user story, business outcome, acceptance criteria, edge cases, and dependencies.
- [x] Prototype scope is separated from unvalidated business candidates.
- [x] Success criteria are user-focused and verifiable.
- [x] Material assumptions and unresolved scope decisions are visible for backlog refinement.
