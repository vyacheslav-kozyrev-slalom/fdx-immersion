# Evergreen Senior Living: Use Case Handoff

Paste this into a new session to continue. Everything here is a working estimate on placeholder inputs, to be validated with client data and vendor quotes. The client is fictional.

## Context

- Client: Evergreen, a senior living operator with 14 communities and about 3,600 beds (placeholder, real count to be updated later)
- Current occupancy: 76%. Goal: 88% to 90%. Timeline (1, 2, or 3 years) is still undecided
- Evergreen has a central office with some data, but no surveys or loss-reason codes explaining why prospects drop off. Staff say the experience is pleasant, but that is anecdotal
- Staff include licensed nurses for assisted living, non-nurse staff, and general staff
- Evergreen uses Microsoft and already has a ChatGPT-style tool with no usage restrictions. Staff lack training, and knowledge sharing with the central office is limited
- Investment budget: $3 million
- The goal for now is to build the use case through discussion, then a deck

## Core idea

Use AI to (1) instrument the intake funnel and capture loss reasons, (2) diagnose why prospects drop off, and (3) act on it with retention work and a differentiation-based marketing campaign.

- Standardize intake and funnel stages (inquiry, tour, application, move-in) across all 14 communities
- Required loss-reason codes in the CRM, with AI transcription of tours and calls that suggests a code for staff to confirm
- Short follow-up surveys with lost prospects and families, because tour transcripts alone cannot explain why someone never came back
- Opt-in or opt-out recording as an experiment: track opt-in rates by community, test wording, compare conversion between recorded and unrecorded paths
- Keep the no-recording path coded and followed up, to avoid bias toward more trusting prospects

## Compliance and reputation notes

- HIPAA may not cover pure sales conversations, but it blurs once tours touch diagnoses, medications, or care needs, especially for communities with licensed nurses or Medicare/Medicaid billing. Treat it all as sensitive
- Use only vendors that sign a business associate agreement and do not train on Evergreen data
- Recording consent rules vary by state
- Store reason codes, not health details. Redact before analysis. Control and log access
- Avoid profiling or inferring conditions from prospects' words
- Keep a human reviewing AI-generated marketing claims (fair housing and truthful advertising rules)
- Compliance counsel should validate before launch. I am not a lawyer
- Research on attitudes: in one health-system survey of AI transcription, comments mostly worried about note accuracy (39%), privacy and security (13%), and being recorded (13%). A 2026 Future of Privacy Forum survey of adults 55+ found privacy a top barrier to AgeTech adoption. Pew finds older adults generally less comfortable with data uses, but views are mixed

## Market benchmarks (researched)

- Assisted living national median cost: $6,200 a month ($74,400 a year), per the 2025 CareScout Cost of Care Survey. NIC MAP average asking rent was about $5,479 a month in Q4 2025
- Working rate range: $5,200 to $6,200 a month. Flagged to validate with Evergreen's central office, along with the mix of assisted living, independent living, and memory care, and how care-level fees are structured
- Occupancy (NIC MAP, 2026): assisted living about 88%, independent living about 91%, industry near 90%
- Funnel benchmarks: inquiry to tour about 29%, tour to move-in about 29% (assisted living benchmarks up to about 46%, top performers 35% to 42%), inquiry to move-in about 8.6%. Volume about 32 to 44 inquiries per 100 units a month
- Length of stay: averages cited at 2.5 to 3 years, but medians are about 19.6 to 22 months. Modeling range 1.8 to 2.5 years
- Margins: typical assisted living NOI margin 25% to 32% at stabilized communities, top quartile above 40%. Labor near 30% of revenue at high performers. Incremental margin on filled beds runs higher than average (one REIT reported 55% incremental flow-through)
- Wages (BLS, May 2025): RN median $97,550 ($46.90 an hour), LPN about $32.73 an hour, personal care aides $35,800 a year ($17.21 an hour)
- Staffing rules: no federal assisted living staffing rule. Twelve states set numeric ratios (for example 1:15 by day in Georgia and Mississippi). Evergreen's state needs to be confirmed
- Care staff hours per resident per day: about 3.5 in an Oregon study

## 12-month plan

- Months 1 to 3, Foundation: map intake at all communities, define one funnel and reason codes, confirm connectivity, set AI usage guardrails, compliance review. Milestone: baseline conversion rate
- Months 4 to 6, Pilot: three or four communities, opt-in transcription, staff training, lost-prospect surveys. Milestone: first real drop-off data and opt-in rates
- Months 7 to 9, Scale and Learn: all 14 communities, staff AI enablement with a shared prompt library, monthly dashboard, ranked drop-off drivers
- Months 10 to 12, Act and Optimize: fix drivers, test the differentiation campaign, measure lift, year-two business case
- Caveat: move-ins lag conversion gains, so 88% likely lands in year two or three

## Revenue math (3,600 beds placeholder)

- Each occupancy point is about 36 beds, worth about $2.2 to $2.8 million a year in revenue depending on rate
- Current revenue at 76%: about $171M ($5,200), $180M ($5,479), $204M ($6,200)
- Going from 76% to 88%: about $27M to $32M a year more. To 90%: about $31M to $37M more
- Funnel check: about 14,000 to 19,000 inquiries a year, 1,200 to 1,600 move-ins at industry averages. Funnel math overstates gains because it ignores move-outs. At 76% occupancy, move-outs run about 1,100 to 1,500 a year, and holding 88% needs about 1,300 to 1,800 move-ins a year

## ROI model (working assumptions)

- Rate $5,700 a month (mid), care labor about $2,800 per added resident per month (3.5 hours at loaded wages, 25% benefits load), other variable costs 10% of rent, 70% of care labor variable with occupancy (sensitivity 50% to 100%)
- Investment $3M, phased about $2.0M, $0.6M, $0.4M
- Conversion plus retention levers: conversion adds about 5.5, 8, or 9.5 points by year 3 (conservative, base, stretch). Retention modeled as a 3%, 5%, or 8% cut in move-outs, ramping slowly (about 5% is only about 70 residents a year)
- Results over 3 years:
  - Conservative: about 84% occupancy, about $26M revenue, about $14M margin, ROI about 380%
  - Base: about 88%, about $38M revenue, about $21M margin, ROI about 610% (about 420% if care labor is fully variable, about 740% if half variable)
  - Stretch: about 92% (upside only), ROI about 850%
  - Worst case (no retention benefit, conservative conversion, fully variable labor, $5,200 rate): about 81.5%, ROI about 110%
- Payback during year two. Each point of occupancy held for a year is worth about $0.86M to $1.35M in margin, so the $3M is recovered with about 2 to 3.5 point-years
- Attribution: if the market alone lifts occupancy about half a point a year, crediting the project with only the excess trims base ROI to roughly 450% (earlier flat-margin version)
- Earlier flat-margin versions used 35%, 45%, and 55% incremental margin; the bottom-up model replaced them

## Technology and training cost estimates (3 years, to confirm with quotes)

| Item | Basis | Low | High |
|---|---|---|---|
| Senior living CRM | $550 to $900 per community per month (WelcomeHome publishes $550 or $700; Aline is quote-based) | $277,000 | $454,000 |
| HIPAA-capable transcription | About $39 to $68 per seat per month, about 52 seats (BAA only on enterprise tiers) | $73,000 | $127,000 |
| Microsoft Copilot | $30 per user per month enterprise ($21 Business tier), 150 to 400 users | $162,000 | $432,000 |
| Devices | About 4 per community at $300 to $600 (my estimate) | $17,000 | $34,000 |
| Staff training time | 600 staff, 8 hours, loaded wage (my estimate) | $126,000 | $189,000 |
| Trainers and curriculum | My estimate | $150,000 | $300,000 |
| Integration and data | My estimate | $150,000 | $400,000 |
| Compliance and security | My estimate | $50,000 | $150,000 |
| Lost-prospect surveys | My estimate | $40,000 | $100,000 |
| Campaign testing | My estimate | $300,000 | $600,000 |
| Total | | about $1.35M | about $2.79M |

Excludes consulting fees for the delivery team. Licenses are the small part; integration, people, and the campaign are the big assumptions.

## Other ideas for the client

- Early-warning retention signals from engagement and family feedback
- Faster, AI-assisted lead response with human review
- Tailor tours and messaging to the adult-child decision-maker
- Referral partnerships with hospital discharge planners
- Cross-community benchmarking
- Hiring pipeline to match occupancy growth

## Risks and open questions

- Real bed count, care mix, and rate structure
- Evergreen's actual inquiry volume and move-out rate
- State staffing and recording-consent rules
- Nursing labor availability and agency premiums
- Vendor quotes for every investment line
- A skeptical client will ask what share of the occupancy gain is due to the market, not the project

## Deliverables created

- Detailed doc: Evergreen Senior Living: AI-Enabled Occupancy Growth (why, how, returns, other ideas, risks, ask): https://claude.ai/artifact/8Wu19GQkq4GkyF1zfwxjYd
- Slide-by-slide script, 13 slides with speaker notes and the itemized investment table: https://claude.ai/artifact/FxmiATop9yQTkGGiRUJ1qU
- No real slide file was built, because no slide tool was available. The script is meant to be pasted into PowerPoint or Google Slides

## Suggested next steps

- Replace placeholders (bed count, rate mix, state) with Evergreen data
- Get real vendor quotes for each investment line
- Decide the timeline target (1, 2, or 3 years) and 88% versus 90%
- Add an attribution view separating market lift from project lift
- Build the loss-reason code list and a sample funnel with illustrative rates
- Turn the slide script into a real deck
