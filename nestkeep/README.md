# NestKeep

**Tagline:** Full beds, rent on time, zero chasing.

NestKeep runs the daily business of PGs, hostels and co-living operators in India (20–500 beds). Rent is collected by UPI Autopay and payment links with automatic reminders and late fees. A QR code in every room and common area lets residents raise complaints and maintenance tickets, see the food menu and opt out of meals (so the kitchen cooks less and wastes less), and log visitors. Owners get bed-level vacancy, KYC and police-verification records, electricity sub-meter billing, notice-period and deposit tracking, and a lead page that fills empty beds.

## Who it is for

| Segment | Size | Why they buy |
|---|---|---|
| Owner-run PGs (boys, girls, mixed) | 20–150 beds, 1–3 buildings | Rent chasing on WhatsApp, food waste, verification paperwork |
| Student hostels near colleges and coaching hubs | 50–400 beds | Parents want safety records; seasonal vacancy |
| Small co-living operators | 100–500 beds, 3–15 properties | Need one dashboard across properties; staff accountability |

India-first: Bengaluru, Hyderabad, Pune, NCR, Chennai, Mumbai, Kota, Indore, Jaipur, Chandigarh. Global-ready later for hostels and shared housing in the Gulf and Southeast Asia.

## Top features

| Priority | Feature | Metric it moves |
|---|---|---|
| P0 | Rent collection: UPI Autopay, payment links, auto reminders, late fees, receipts | Revenue (owner cash on time), retention |
| P0 | Bed board: occupied, vacant, notice, reserved, per bed | Revenue (occupancy), activation |
| P0 | Room QR: complaints and maintenance tickets with SLA | Retention (resident satisfaction) |
| P0 | Tenant onboarding: digital form, KYC upload, consent, police-verification packet | Activation, compliance |
| P1 | Food menu and meal opt-out by QR | Revenue (food cost saved) |
| P1 | Electricity sub-meter billing per room | Revenue (recovered cost) |
| P1 | Notice period and deposit settlement tracker | Retention, trust |
| P1 | Visitor log by QR | Compliance, parent trust |
| P1 | Vacancy lead page and lead inbox | Acquisition of residents |
| P2 | Multi-property roles, accounting export, resident referral rewards | Expansion |

## Pricing (summary)

| Plan | INR | USD | For |
|---|---|---|---|
| Rent | ₹20 per bed per month (minimum ₹499) | $0.23 per bed | Rent collection, reminders, bed board, QR complaints |
| Pro (recommended) | ₹35 per bed per month (minimum ₹1,199) | $0.40 per bed | Adds KYC and verification, food opt-out, electricity billing, visitor log, notice and deposits, lead page |
| Operator | ₹30 per bed per month, 300+ beds, annual | $0.34 per bed | Multi-property, roles, exports, priority support |

Annual billing: 2 months free. KYC verification and WhatsApp messages billed per use. USD at ₹88 per USD (estimate). Full model: [05-pricing-and-revenue.md](docs/05-pricing-and-revenue.md).

## Why now

- Organised co-living is about 0.3 million beds against 6.6 million beds of organised demand in 2025 (Colliers, via [Tribune India](https://www.tribuneindia.com/news/business/indias-co-living-market-inventory-set-at-1-million-beds-by-2030-colliers), accessed 2026-11-24). The gap is filled by owner-run PGs that run on WhatsApp and notebooks.
- City crackdowns: a Bengaluru audit found 3,597 of 5,480 PGs operating without licences ([OneIndia](https://www.oneindia.com/bengaluru/bengaluru-pg-audit-finds-3-597-facilities-operating-without-licences-east-tops-list-8243241.html), accessed 2026-11-24), and Delhi has proposed PG licences with police verification ([The Hans India](https://www.thehansindia.com/news/cities/new-delhi/delhi-plans-pg-regulation-bill-with-licences-police-clearance-and-public-registry-1119952), accessed 2026-11-24). Records are becoming mandatory.
- DPDP Rules 2025 (notified 14 November 2025) make a drawer full of Aadhaar photocopies a liability ([PIB](https://static.pib.gov.in/WriteReadData/specificdocs/documents/2025/nov/doc20251117695301.pdf), accessed 2026-11-24).

## Built on the shared core

QR engine, public pages, payments (Razorpay/UPI and Autopay), CRM, WhatsApp messaging, staff app, analytics and onboarding wizard come from [`core/`](../core/README.md). NestKeep adds: property, room and bed inventory; tenancy ledger; KYC vault and verification packet; meal plan and opt-out; meter readings; visitor log; notice and deposit settlement.

## Documents

| Doc | Contents |
|---|---|
| [AGENTS.md](AGENTS.md) | Brief for AI agents: glossary, decisions, open questions |
| [01-product-plan.md](docs/01-product-plan.md) | Vision, ICP, personas, journeys, features P0–P2, data model, MVP scope |
| [02-problems-and-benefits.md](docs/02-problems-and-benefits.md) | Problem, solution, benefit per stakeholder |
| [03-pros-cons-risks.md](docs/03-pros-cons-risks.md) | Pros, cons, risks, mitigations, kill criteria |
| [04-market-research.md](docs/04-market-research.md) | Market size, competitors, pricing benchmarks, regulation, sources |
| [05-pricing-and-revenue.md](docs/05-pricing-and-revenue.md) | Tiers, add-ons, unit economics, 12-month scenarios |
| [06-go-to-market-and-onboarding.md](docs/06-go-to-market-and-onboarding.md) | First 10 customers, sales script, onboarding checklist, retention |
