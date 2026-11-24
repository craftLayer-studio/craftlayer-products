# AGENTS.md — GaragePilot

Brief for AI agents and new contributors working on GaragePilot. Read this first.

## Context in five lines

- GaragePilot is CraftLayer's vertical SaaS for independent car and bike garages, car wash and detailing studios in India.
- Wedge: a digital job card with photo/video inspection and a QR (or WhatsApp link) that shows live repair status; estimates are approved on WhatsApp.
- The money engine is service-due reminders by kilometres and date: they turn one-time walk-ins into repeat customers.
- The buyer is the garage owner (often the head mechanic). Staff are service advisors and mechanics. End customers are vehicle owners (and sometimes fleets and insurers).
- Most vehicle owners leave authorised dealers after warranty; independent garages win that business on price but lose it on trust. GaragePilot sells trust (photos, approvals, invoices) and recall (reminders).

## Reading order

1. [README.md](README.md)
2. [docs/01-product-plan.md](docs/01-product-plan.md)
3. [docs/05-pricing-and-revenue.md](docs/05-pricing-and-revenue.md)
4. [docs/06-go-to-market-and-onboarding.md](docs/06-go-to-market-and-onboarding.md)
5. [docs/04-market-research.md](docs/04-market-research.md)
6. [docs/02-problems-and-benefits.md](docs/02-problems-and-benefits.md), [docs/03-pros-cons-risks.md](docs/03-pros-cons-risks.md)
7. Shared platform: [../core/README.md](../core/README.md)

## Glossary

| Term | Meaning |
|---|---|
| Job card / RO | Repair order: one vehicle visit with complaints, inspection, estimate, work done, invoice |
| DVI | Digital vehicle inspection: photos and videos with checklist results |
| Service advisor | Staff who receives vehicles, writes job cards and talks to customers |
| Bay | A workspace for one vehicle |
| Estimate | Proposed parts and labour; each line can be approved or declined |
| Declined work | Lines the customer rejected; a follow-up opportunity |
| Service due | Next service predicted from date and kilometres (for example 10,000 km or 12 months) |
| Avg daily km | Kilometres per day estimated from odometer readings across visits |
| Cashless claim | Insurance repair where the insurer pays the garage directly after surveyor approval; only at the insurer's network garages |
| Surveyor | Insurer's assessor who approves the damage estimate |
| Wash pass / subscription | Prepaid bundle of washes or monthly plan |
| Utility / marketing template | WhatsApp template categories; marketing costs about 7.5× utility in India |

## Core modules used

| Need | Core module |
|---|---|
| Job card QR, counter QR, booking QR | QR engine |
| Status page, booking page, wash-plan page | Public storefront + booking engine |
| UPI invoices, subscription billing | Payments (Razorpay/UPI) |
| Vehicle owners, vehicles, history | Customer CRM |
| Status, approvals, invoices, reminders | WhatsApp/SMS messaging |
| Wash points, referral rewards | Loyalty and rewards |
| Google review request after delivery | Reviews and Google review funnel |
| Mechanic app | Staff app |
| Revenue, ARO, comeback rate | Analytics dashboard |

GaragePilot-specific modules: job card and DVI, estimate approval, parts inventory and purchases, mechanic tasks, service-due engine, insurance claim tracker, wash subscriptions.

## Decisions made

| Decision | Reason |
|---|---|
| Customer never needs an app; everything works via WhatsApp link or QR | Car owners will not install a garage app |
| Mobile-first service-advisor flow (job card in under 2 minutes) | Advisors stand next to the car, not at a desk |
| Line-item approval with photos, not a single "approve all" | Raises approved estimate value and reduces disputes |
| Service-due reminders billed with a bundle, then credits | Reminders may be classed as marketing templates; cost must be visible |
| No marketplace or lead selling to garages in MVP | Avoid the GoMechanic channel-conflict model; we sell software to the garage |
| GST invoice with HSN for parts and SAC for labour | Owners need clean invoices after the September 2025 GST change |

## Open questions

1. Will Meta classify km/date service-due reminders as utility (tied to an existing service relationship) or marketing? Budget assumes marketing until tested.
2. Can we get read access to insurer claim portals, or only track claim status manually? Affects the insurance tracker scope.
3. Parts catalogue: build our own, or partner with a parts distributor (Boodmo, Uno Minda, Bosch) for lookups and ordering commission?
4. OBD dongle integration for automatic odometer readings: worth it in P2, or only for fleet customers?
5. Name check: no established product named "GaragePilot" was found. Similar names exist: GaragePlug (Indian garage software, direct competitor) and WrenchPilot (US garage software). The closeness to GaragePlug may cause confusion in Indian search and sales. Run a trademark search in Class 9 and 42. Backup names if needed: **BayBook**, **JobCardly**.
