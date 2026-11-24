# StayBell

**Tagline:** Every room rings you directly. Turn OTA guests into direct guests.

StayBell is a guest-service and direct-booking layer for small hotels, homestays, guest houses and small resorts (5–60 rooms) in India. A QR code in every room lets guests order food, ask for housekeeping, raise complaints, buy late checkout or local experiences, and complete digital check-in with ID upload. Every guest who scans becomes a consented contact in the owner's CRM, so the next stay can be booked directly instead of through an OTA that keeps 15–25%.

## Who it is for

| Segment | Size | Why they buy |
|---|---|---|
| Homestays and guest houses | 3–15 rooms, owner-run | No front desk at night; OTA commission eats margin; paper ID register |
| Independent budget and mid-scale hotels | 10–40 rooms, ADR ₹1,500–₹5,000 | Room-service revenue leaks through phone calls; no repeat-guest marketing |
| Small resorts and boutique stays | 10–60 rooms, leisure markets | Upsell experiences and late checkout; review volume drives OTA ranking |

India-first: hill stations, pilgrimage towns, beach belts and Tier 2–3 business towns. Global-ready later (Southeast Asia, Middle East guest houses).

## Top features

| Priority | Feature | Metric it moves |
|---|---|---|
| P0 | Room QR: in-room dining, housekeeping, complaints, front-desk chat | Revenue (F&B per occupied room), retention |
| P0 | Digital check-in with ID upload, Form C data pack for foreign guests | Activation (time saved at desk), compliance |
| P0 | Guest CRM with DPDP-compliant consent captured at check-in and scan | Retention (repeat direct bookings) |
| P0 | Review funnel: happy guests to Google/TripAdvisor, unhappy to owner | Acquisition (rank), retention |
| P1 | Direct booking site and commission-free booking engine with UPI | Revenue (OTA commission saved) |
| P1 | Upsells: late checkout, early check-in, experiences, packages | ARPU |
| P1 | WhatsApp concierge and pre-arrival / post-stay journeys | Retention, referral |
| P2 | Channel-manager integration, rate parity alerts, multi-property | Expansion revenue |

## Pricing (summary)

| Plan | INR / month | USD / month | For |
|---|---|---|---|
| Room QR | ₹999 (up to 10 rooms) | $12 | Homestays that want room service, requests, reviews, digital check-in |
| Direct | ₹2,499 (up to 25 rooms) | $29 | Adds booking site, CRM campaigns, WhatsApp concierge, upsells |
| Pro | ₹4,999 (up to 60 rooms, 2 properties) | $57 | Adds channel-manager link, multi-property, advanced analytics |

Annual billing: 2 months free. Extra rooms ₹69/room/month. WhatsApp messages billed at Meta cost plus 20%. USD at ₹88 per USD (estimate). Full model: [05-pricing-and-revenue.md](docs/05-pricing-and-revenue.md).

## Why now

- GST on rooms up to ₹7,500 per night dropped from 12% (with ITC) to 5% (without ITC) from 22 September 2025, which pushes budget-hotel demand but squeezes owner margins because input credit is lost ([ClearTax](https://cleartax.in/s/impact-of-gst-hospitality-industry), accessed 2026-11-24). Every rupee of OTA commission saved now matters more.
- Third-party portals held about 58.66% of India's online accommodation market in 2025, with direct channels growing faster ([Mordor Intelligence](https://www.mordorintelligence.com/industry-reports/india-online-accommodation-market), accessed 2026-11-24).
- DPDP Rules 2025 were notified on 14 November 2025 with full obligations by May 2027 ([PIB](https://static.pib.gov.in/WriteReadData/specificdocs/documents/2025/nov/doc20251117695301.pdf), accessed 2026-11-24). Paper guest registers full of ID copies become a liability; a consented digital register becomes a selling point.

## Built on the shared core

QR engine, storefront, ordering and booking engine, payments (Razorpay/UPI), CRM, WhatsApp messaging, reviews funnel, staff app, analytics and onboarding wizard come from [`core/`](../core/README.md). StayBell adds hotel-specific modules: room inventory and rates, guest register and ID vault, Form C data pack, housekeeping board, upsell catalog and direct booking site.

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
