# ClassNest

**Tagline:** Every student marked, every parent informed, every fee collected.

ClassNest is the front-desk app for coaching institutes, tuition centres and music, art and skill academies in India. A QR code at the entrance marks attendance and alerts parents on WhatsApp. UPI fee links and automatic reminders shrink the defaulter list. The same QR on posters and flyers books demo classes during admission season.

## Who it is for (ICP)

| Segment | Size | Why they buy |
|---|---|---|
| Neighbourhood tuition and coaching centre (Class 6–12, boards, foundation) | 50–400 students, 2–10 teachers, 1 branch | Fee defaulters, parent trust, admission-season leads |
| Competitive-exam coaching (JEE/NEET/CA/banking/SSC) | 100–1,000 students, 1–3 branches | Attendance proof for parents, test results, batch management |
| Music, dance, art, chess, coding and language academies | 30–200 students, 1–6 instructors | Monthly fee collection, slot/batch scheduling, demo-class bookings |

Tier 2 and Tier 3 cities first (Jaipur, Indore, Lucknow, Patna, Nagpur, Coimbatore), then Tier 1 suburbs.

## Top features (MVP)

1. **QR attendance + parent WhatsApp alerts** — student scans the entrance QR (or teacher marks in one tap); parents of absent students get an alert within 15 minutes. Moves: retention.
2. **Fee collection with UPI and auto-reminders** — instalment plans, UPI payment links, reminders at D-3, D0, D+3, D+7, digital GST receipts, defaulter dashboard. Moves: revenue.
3. **Enquiry CRM + demo-class booking via QR** — QR on posters, flyers and banners opens a booking page; leads land in a pipeline with WhatsApp follow-up. Moves: acquisition.
4. **Batches and timetable** — batches, rooms, teachers, holidays, clash detection. Moves: activation.
5. **Tests, marks and report cards** — marks entry, rank, parent report card on WhatsApp. Moves: retention and referral.
6. **Homework and notes sharing** — PDFs and images per batch. Moves: retention.
7. **Teacher payout tracking** — per-batch or per-hour pay, monthly payout sheet. Moves: activation (owner stickiness).

## Pricing (summary)

| Plan | INR / month (billed yearly) | USD | Students |
|---|---|---|---|
| Starter | ₹799 (₹7,999/yr) | $12 | Up to 100 |
| Growth | ₹1,499 (₹14,999/yr) | $19 | Up to 300 |
| Pro | ₹2,999 (₹29,999/yr) | $39 | Up to 1,000, multi-branch |

WhatsApp messages beyond the plan's bundle are billed as credits. Zero platform fee on UPI fee collection. Details in [docs/05-pricing-and-revenue.md](docs/05-pricing-and-revenue.md).

Anchor: Classplus lists Starter at ₹19,999/year + GST and Grow at ₹22,999/year + GST ([Capterra](https://www.capterra.com/p/208852/Class-Plus/reviews/), accessed 2026-11-24). ClassNest Growth is about 25–35% cheaper and is built for the offline centre, not for selling online courses.

## Documents

| Doc | What it covers |
|---|---|
| [AGENTS.md](AGENTS.md) | Brief for AI agents: context, glossary, decisions, open questions |
| [01 Product plan](docs/01-product-plan.md) | ICP, personas, journeys, features P0/P1/P2, data model, metrics |
| [02 Problems and benefits](docs/02-problems-and-benefits.md) | Problem, solution and benefit per stakeholder |
| [03 Pros, cons, risks](docs/03-pros-cons-risks.md) | Risks, mitigations, kill criteria |
| [04 Market research](docs/04-market-research.md) | Market size, competitors, regulation, sources |
| [05 Pricing and revenue](docs/05-pricing-and-revenue.md) | Tiers, add-ons, unit economics, 12-month scenarios |
| [06 Go-to-market and onboarding](docs/06-go-to-market-and-onboarding.md) | First 10 customers, sales script, onboarding checklist |

Built on the CraftLayer shared core: [core/README.md](../core/README.md).
