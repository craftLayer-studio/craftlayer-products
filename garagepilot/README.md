# GaragePilot

**Tagline:** Digital job cards, WhatsApp approvals, and service reminders that bring every car back.

GaragePilot runs the service desk of independent car and bike garages, car wash and detailing studios in India. Every vehicle gets a digital job card with photo and video inspection. The customer scans a QR on the job card (or taps a WhatsApp link) to see live repair status and approve estimates. GST invoices, parts stock and mechanic tasks sit in the same app. Service-due reminders based on kilometres and date bring the vehicle back, and repeat visits are where the money is.

## Who it is for (ICP)

| Segment | Size | Why they buy |
|---|---|---|
| Independent multi-brand car garage | 3–15 mechanics, 4–12 bays, 100–400 job cards/month | Estimate disputes, lost repeat customers, messy GST billing |
| Two-wheeler service centre (independent or small dealer sub-centre) | 2–8 mechanics, 300–1,000 jobs/month | Volume, reminders, parts stock |
| Car wash and detailing studio | 3–12 staff, 200–800 washes/month | Subscriptions, ceramic/PPF job tracking, repeat bookings |

Tier 1 suburbs and Tier 2 cities first (Pune, Ahmedabad, Jaipur, Lucknow, Chandigarh, Coimbatore, Kochi).

## Top features (MVP)

1. **Digital job card with photo/video inspection** — capture odometer, fuel, dents and scratches at check-in. Moves: retention (trust) and revenue (fewer disputes).
2. **QR job card + live status** — customer scans or taps the link to see "Inspection, Waiting approval, In repair, Washing, Ready". Moves: retention.
3. **Estimate approval on WhatsApp** — line items with photos; customer approves or rejects each item. Moves: revenue (ARPU per job).
4. **GST invoices with UPI payment link** — parts at 18% GST, labour as a service line. Moves: revenue.
5. **Service-due reminders by km and date** — predicts next due date from average daily km; WhatsApp reminder with booking link. Moves: retention (repeat revenue).
6. **Parts inventory** — stock, reorder level, purchase entries, part-wise margin. Moves: revenue.
7. **Mechanic task tracking** — jobs per mechanic, time on job, incentive sheet. Moves: activation.

P1: car wash subscriptions, insurance claim tracker, online booking, loyalty.

## Pricing (summary)

| Plan | INR / month (billed yearly) | USD | Fit |
|---|---|---|---|
| Bay | ₹999 (₹9,999/yr) | $12 | Single garage, up to 150 job cards/month |
| Workshop | ₹1,999 (₹19,999/yr) | $24 | Up to 500 job cards/month, inventory, subscriptions, insurance tracker |
| Pro | ₹3,999 (₹39,999/yr) | $48 | Multi-location, unlimited job cards, Tally export |

Anchors: RAMP Garage Management lists ₹9,870/year; GaragePlug is quote-based with a reported floor around $1,188/year; Tekmetric Start is $179/month in the US ([Codingclave](https://codingclave.com/guides/best-auto-repair-shop-software-india-2026), [CostBench](https://costbench.com/software/automotive-shop-software/garageplug/), [Tekmetric](https://tekmetric.com/pricing), accessed 2026-11-24). Details in [docs/05-pricing-and-revenue.md](docs/05-pricing-and-revenue.md).

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
