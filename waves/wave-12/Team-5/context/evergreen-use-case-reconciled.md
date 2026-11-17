# Evergreen: Use case handoff (reconciled)

**Date:** 2026-11-17
**Purpose:** One handoff for continuing the intake-funnel use case, the ROI and the deck. It merges the original handoff (`evergreen-use-case-handoff.md`, from a separate session) with the transcript-grounded work in this session.

## How to read this file

**Source priority, highest first.** A lower source complements a higher one and never overrides it.

| Tag | Source | Meaning |
|---|---|---|
| **[T]** | Cora's two sessions (S1 = `Cora's Room.vtt`, S2 = `Cora's Room (1).vtt`) | Stated by the client. Highest priority. |
| **[D]** | Derived | Math from [T] numbers. |
| **[P]** | PRD and prototype brief | Documents about Evergreen, not statements from Cora. |
| **[R]** | Research | Web research and the original handoff. External, unverified for Evergreen. |
| **[A]** | Assumption | Placeholder to confirm. |

`🔎 REVIEW` marks a point to check against the transcript or the client. Timestamps are approximate.

---

## 1. Client context (reconciled)

| Item | Value | Tag |
|---|---|---|
| Client | Evergreen Living Services, a senior living operator with a skilled nursing and healthcare component | [T] |
| Communities | 14, mostly East, West and South; urban, suburban and rural; all facilities owned | [T] S1 ~04:10, ~05:07, ~08:14 |
| Residents | Just shy of 2,500 | [T] S1 ~04:15 |
| Beds | About 3,200 (2,500 ÷ 0.78) | [D] |
| Occupancy | About 78% and falling; maybe worse in suburban than rural (she'd verify) | [T] S1 ~04:26, S2 ~16:24 |
| Target | 88–90%; timeline (1, 2 or 3 years) not decided | [T] / open |
| Staff turnover | 38% | [T] S1 ~04:34 |
| Workforce mix | About 60% skilled nursing, 20% operations, 20% non-medical care (her estimate); **no headcount given** | [T] S1 ~12:05 |
| Decision cycle | Typically 3–6 months; prospects tour other places | [T] S2 ~07:40 |
| Intake | Counselor completes the intake form during the conversation (name, address, nearby family), gives tours, follows up after the first visit | [T] S2 ~07:00–09:12 |
| Referrals | Mostly informal, resident to friend; no medical or partner referrals; no incentive and no special treatment | [T] S1 ~15:35, S2 ~01:00 |
| Decline reasons | Counselors ask, and the form has a line for it, but it is anecdotal and not aggregated, even in a spreadsheet | [T] S2 ~02:00–02:40 |
| Feedback | No standardized resident or family feedback; no official family channel | [T] S1 ~21:48, S2 ~05:07 |
| CRM | "Technically a CRM" but "antiquated and pretty basic," used for intake and follow-up; name unknown; whether one instance or per community is not stated | [T] S2 ~21:01 |
| Medical records | Shared across communities with access limited to those who need it | [T] S2 ~19:12 |
| Resident-facing technology | None | [T] S1 ~19:41 |
| Marketing | Light regional radio and mailers, managed per location, not rolled up; paid advertising is not in the budget and sits with the CMO; she's "not opposed" | [T] S1 ~17:35, S2 ~21:30 |
| Budget | Tight; none shared. **$3M is our assumption.** | [T] / [A] |
| Board | Wants an answer on how AI will shape the future | [T] S2 ~14:36 |
| Compliance | HIPAA and privacy; need-to-know access | [T] S1, S2 |
| Microsoft and Azure | Assumed, not stated | [A] 🔎 |
| Rural connectivity, paper care notes, lean IT, overtime and no-shows | In the PRD only | [P] 🔎 |

## 2. Where the original handoff conflicted, and how it was resolved

| Original handoff | Resolution |
|---|---|
| About 3,600 beds | Replaced by about 3,200 [D]. The 3,600 was a placeholder. |
| 76% occupancy | Replaced by about 78% [T]. |
| "No loss-reason codes" | Reworded: a reason line exists on the form but is anecdotal and uncoded [T]. |
| Funnel stage "application" | Use Cora's stages: inquiry, intake form, tour, follow-up, move-in. Add "application" only if Evergreen has it. 🔎 |
| ChatGPT-style tool, no usage limits, staff untrained | Not in the transcripts. Keep only as an unverified question. 🔎 |
| Microsoft | Keep, labeled assumed [A]. |
| About 600 staff in the training line | No headcount stated; my estimate is about 1,500 [A]. Unreconciled. 🔎 |
| Recording and transcribing tours and calls | Not discussed by Cora, and she stressed privacy. Moved to an **optional later phase**. 🔎 |
| $300–600K differentiation campaign | Advertising is not budgeted (CMO decision). Keep as an open decision, not a committed line. 🔎 |

## 3. Core idea

Use AI to instrument the intake funnel, learn why prospects drop off, and act on it.

- **Standardize the funnel** across all 14 communities using the stages above. [T]-based
- **Coded loss reasons** built on the reason line that already exists on the intake form, with AI suggesting a code for staff to confirm. [T]-based
- **Short lost-prospect and family surveys** (new). Cora has no feedback process, and tour notes alone can't explain why someone never came back. Needs consent.
- **Tracked referral sources and recognition** (fits her openness to recognizing referrers).
- **Optional phase 2:** opt-in recording and transcription of tours, with a no-recording path that is still coded and followed up. Needs legal review of state consent rules.
- **Optional, pending a decision:** a differentiation-based marketing campaign.

## 4. Compliance notes

**Stated by Cora [T]:** HIPAA and resident privacy; health information limited to people who need it; human review before action.

**Kept from the original handoff [R], to validate with counsel (not legal advice):**
- HIPAA may not cover pure sales conversations, but it blurs once tours touch diagnoses, medications or care needs. Treat it all as sensitive.
- Use vendors that sign a business associate agreement and don't train on Evergreen data.
- Recording consent varies by state. Store reason codes, not health details; redact before analysis; control and log access.
- Don't infer conditions from prospects' words. Keep a human reviewing AI-generated marketing claims (fair housing and truthful advertising).

## 5. Market benchmarks [R] (unverified for Evergreen; sources conflict)

- **Monthly rate, assisted living:** working range **$5,200–6,200**; mid **$5,700**. CareScout median $6,200, NIC MAP asking rent about $5,479, and the Genworth-attributed $5,900 used in this session. All sit inside the range. Confirm Evergreen's own rates and care mix. 🔎
- **Occupancy (NIC MAP, 2026):** assisted living about 88%, independent living about 91%, industry near 90%. Industry occupancy is rising while Evergreen's is falling, so the gap looks Evergreen-specific.
- **Funnel:** inquiry to tour about 29%; tour to move-in about 29–34%; inquiry to move-in about 4–12% (about 8.6% in the handoff); cycle about 120–145 days.
- **Length of stay:** medians about 19.6–22 months (averages 2.5–3 years). Modeling range 1.8–2.5 years.
- **Margins:** stabilized assisted living NOI margin about 25–32%; incremental margin on filled beds higher.
- **Wages (BLS, May 2025):** RN median $97,550; LPN about $32.73 an hour; personal care aides about $35,800 a year.
- **Staffing rules:** no federal assisted-living staffing rule; some states set ratios. Evergreen's states are unknown. 🔎

## 6. Revenue math, rebased on the transcript numbers [D]

Base: 2,500 residents at 78% means about 3,205 beds, so **one occupancy point is about 32 beds**.

| Monthly rate | One point, per year | 78% to 88% (+321 residents) | 78% to 90% (+385 residents) | Current revenue (78%) |
|---|---|---|---|---|
| $5,200 | $2.0M | $20.0M | $24.0M | $156M |
| $5,700 (mid) | $2.2M | $21.9M | $26.3M | $171M |
| $6,200 | $2.4M | $23.8M | $28.6M | $186M |

(The original handoff's $27–37M figures used 3,600 beds and 76%, so they overstate the gap. Superseded.)

**Funnel check:** to hold 88% occupancy (about 2,820 residents) at a 1.8–2.5-year stay needs about **1,130–1,570 move-ins a year**. Use **1,200 for both move-ins and move-outs** in the model, which implies about a 2.1-year average stay and holds occupancy flat. Inquiries then follow from the conversion rate (about 12,000 at 10%). 🔎 Cora gave no inquiry, tour or move-in counts.

## 7. Margin and ROI, reconciled

### Margin per added resident (monthly rate $5,700)
| Lens | Margin per resident per year | Share of rent | Value of one occupancy point per year | Point-years to recover $3M |
|---|---|---|---|---|
| Flat 35% (session placeholder) | $23,940 | 35% | $0.77M | 3.9 |
| Original handoff bottom-up, care labor fully variable | $27,960 | 41% | $0.90M | 3.3 |
| Original handoff bottom-up, 70% variable | $38,040 | 56% | $1.22M | 2.5 |
| Original handoff bottom-up, 50% variable | $44,760 | 65% | $1.44M | 2.1 |

The bottom-up inputs are $2,800 care labor per added resident per month and other variable costs of 10% of rent. 🔎 Evergreen's real margin is unknown. The session's 35% is the conservative floor.

### What drives ROI: occupancy points attributable to the project
Illustrative 3-year ROI on **$3M**, assuming the final gain ramps at 15%, 50% and 90% of its size in years one to three (a ramp I assumed):

| Points gained by year 3 | 35% flat | 41% (labor fully variable) | 56% (70% variable) |
|---|---|---|---|
| **2.2** (the three funnel benefits below) | -13% | +2% | +39% |
| **2.7** (plus resident retention) | +7% | +25% | +70% |
| 5 | +98% | +132% | +215% |
| 8 | +217% | +270% | +404% |
| 10 (the full gap to 88%) | +296% | +363% | +530% |

**Reading it.** The original handoff's 380–850% ROI assumes about 8 or more attributable points by year 3 (conversion of 5.5–9.5 points plus retention). The transcript-grounded benefits sized in this session claim about 2–3 points, which is break-even to modestly positive on $3M. The gap between them is the attribution question, and it should be settled with real data in the pilot.

**Attribution caution [R].** The market alone is lifting occupancy, so a skeptical client will ask what share of any gain is the project's. Evergreen's own occupancy is falling while the industry rises, so the project's share could be larger, but it needs a baseline to show it.

**Separate case, not to be mixed in.** The EnhanceIQ Calculate workspace for the integrated workforce and care case shows -31% (revenue basis) and about -72% (margin basis) on $1.635M of cost with two benefits. It has a different scope (predictive models plus LLM drafting) and cost base.

### Benefit formulas and inputs from this session (EnhanceIQ), all placeholders unless noted
| Benefit | Inputs | Annual amount, revenue / margin (35%) |
|---|---|---|
| Improved lead conversion | 12,000 inquiries; 10% current rate; 5% relative lift; $5,900 (or $2,065 margin); 6 months | $2.12M / $743K |
| Shorter time to move-in | 1,200 move-ins; 135 days; 5% reduction; $5,900 ÷ 30 per day | $1.59M / $558K |
| Revenue uplift from surfaced insights (decline recovery) | 2,300 declined prospects; 30% addressable; 5% recovery; $5,900; 6 months | $1.22M / $427K |
| Resident retention (update to 1,200 move-outs) | 1,200 move-outs; 35% avoidable; 8% reduction; $5,900; 6 added months | $1.19M / $416K |

Added occupied beds (steady state): about 30 + 22 + 17 + 17 = **about 86 beds, about 2.7 points, about 27% of the gap**. The benefits overlap (they fill the same empty beds), so total claims should be capped, and confidence kept at 40–60%.

## 8. Plan, reconciled

The original handoff's 12-month plan and this session's plan agree on shape. Merged proposal, all dates assumed:

- **Months 1–3, foundation and first pilot:** map intake at all communities; one funnel and one coded reason list; AI usage guardrails and privacy review; CRM data access (name, export, dates); baseline conversion; pilot go-live in **two** communities by about week 12.
- **Months 4–6, pilot:** widen to three or four communities; lost-prospect surveys; 90-day readout; first real drop-off data.
- **Months 7–9, scale and learn:** all 14 communities; monthly dashboard; ranked drop-off drivers.
- **Months 10–12, act and optimize:** fix the drivers; test the differentiation campaign if approved; measure lift; year-two business case.
- **Timing caveat:** move-ins lag conversion gains because of the 3–6 month decision cycle, so reaching 88% likely lands in year two or three.
- The PRD expects initial findings in **6–8 weeks** [P], which fits the foundation phase.

## 9. Technology and cost lines [R] (3 years; to confirm with quotes)

| Line | Basis | Low | High | Transcript status |
|---|---|---|---|---|
| Senior living CRM | $550–900 per community per month | $277K | $454K | A CRM exists but is basic; replace or add-on undecided |
| HIPAA-capable transcription | About 52 seats | $73K | $127K | Not discussed; optional phase 2 |
| Microsoft Copilot | 150–400 users | $162K | $432K | Depends on the Microsoft assumption |
| Devices | About 4 per community | $17K | $34K | Not discussed |
| Staff training time | 600 staff, 8 hours | $126K | $189K | Headcount unknown |
| Trainers and curriculum | Estimate | $150K | $300K | Estimate |
| Integration and data | Estimate | $150K | $400K | CRM name and export unknown |
| Compliance and security | Estimate | $50K | $150K | Estimate |
| Lost-prospect surveys | Estimate | $40K | $100K | New; consent needed |
| Campaign testing | Estimate | $300K | $600K | Paid advertising not budgeted |
| **All lines** | | **$1.35M** | **$2.79M** | Excludes consulting fees |

**Core intake-funnel scope** (CRM, integration, compliance, surveys, trainers, training time): about **$0.8M–$1.6M** over three years, before consulting fees. Optional lines (transcription, Copilot, devices, campaign) are about $0.55M–$1.2M more. A $1M program breaks even at about 13–18 added residents at placeholder rates.

## 10. Other ideas, and the transcript fit

- **Early-warning retention signals:** supported in concept (move-out reasons are anecdotal); no data yet.
- **Faster AI-assisted lead response with human review:** fits the follow-up gap.
- **Tailor tours and messaging to the adult-child decision-maker:** not discussed; idea only.
- **Referral partnerships with hospital discharge planners:** fits, since Cora has no medical referral partners.
- **Cross-community benchmarking:** fits; nothing rolls up to the central office today.
- **Hiring pipeline to match occupancy growth:** fits her hiring and turnover concerns.

## 11. Risks and open questions for Cora

1. How is occupancy measured, and what is the total bed count and care mix? By community?
2. Average monthly rate per resident and margin; share on Medicare or Medicaid.
3. Annual inquiries, tours and move-ins (and move-outs), in total and by community.
4. Is the CRM's name known? Can it export records with dates for each stage? One instance or per community?
5. Who owns intake and marketing data? Is there a CMO?
6. Total headcount by category; turnover by role; agency and overtime spend.
7. Which states? Recording-consent and staffing-ratio rules.
8. Is there an AI tool in use today, and any usage policy? (The original handoff claimed one; not in the transcripts.)
9. Timeline target (1, 2 or 3 years) and 88% versus 90%.
10. Who is the sponsor, and when does the board expect the AI answer?

## 12. Deliverables

- **Original handoff documents:** the AI-Enabled Occupancy Growth doc (https://claude.ai/artifact/8Wu19GQkq4GkyF1zfwxjYd) and the 13-slide script (https://claude.ai/artifact/FxmiATop9yQTkGGiRUJ1qU). They should be revised to this file's numbers before use.
- **Five-slide deck built in this session:** https://claude.ai/artifact/DqdjfyTD1gZP47RvAZ9iPu (private until shared).
- **Files in this folder:** `evergreen-session-context.md` (full session summary), the two transcripts, the two templates and the screenshots.
- **Spreadsheets in `~/Downloads/`:** roles and task templates (Marketing and Evergreen), `Evergreen_AI_ROI_Model.xlsx`, `Use_Case_Import_Intake_Funnel_Intelligence.xlsx`.

## 13. Next steps

1. Revise the original handoff's doc and 13-slide script to the numbers in section 6 and 7 and the plan in section 8.
2. Ask Cora the questions in section 11, starting with inquiry, tour and move-in counts and the CRM.
3. Replace placeholders (rate, margin, headcount, stay length) with Evergreen data.
4. Get vendor quotes for each line in section 9.
5. Decide whether recording and the differentiation campaign are in the first release.
6. Add an attribution view separating market lift from project lift.
