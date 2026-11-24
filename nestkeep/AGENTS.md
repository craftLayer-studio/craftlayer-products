# NestKeep — agent brief

Read this before editing any NestKeep doc or building any NestKeep feature.

## Context in five lines

1. NestKeep is a CraftLayer vertical product for PGs, hostels and co-living operators in India (20–500 beds).
2. Wedge: rent collection that runs itself (UPI Autopay, reminders, late fees) plus a QR in every room and common area for complaints, maintenance, meal opt-out and visitor log.
3. Money story: owner gets rent on time, saves food cost, recovers electricity cost, and fills vacant beds faster.
4. Priced per bed per month, anchored to Indian PG software at ₹26–₹35 per bed.
5. India-first, built on the shared [`core/`](../core/README.md) platform.

## Reading order

1. [README.md](README.md)
2. [docs/01-product-plan.md](docs/01-product-plan.md)
3. [docs/05-pricing-and-revenue.md](docs/05-pricing-and-revenue.md)
4. [docs/06-go-to-market-and-onboarding.md](docs/06-go-to-market-and-onboarding.md)
5. [docs/04-market-research.md](docs/04-market-research.md)
6. [docs/02-problems-and-benefits.md](docs/02-problems-and-benefits.md) and [docs/03-pros-cons-risks.md](docs/03-pros-cons-risks.md)

## Glossary

| Term | Meaning |
|---|---|
| PG | Paying guest accommodation: shared or single rooms rented per bed, often with meals |
| Co-living | Professionally managed shared housing, usually branded (Zolo, Stanza Living and smaller operators) |
| Bed | The unit of sale and of pricing; a room has 1–6 beds |
| Resident / tenant | Person occupying a bed; used interchangeably |
| Sharing | Occupancy type: single, double, triple sharing |
| Bed board | Grid of all beds with status: occupied, vacant, on notice, reserved, blocked |
| Notice period | Days a resident must inform before leaving (often 30) |
| Deposit settlement | Refund of security deposit minus dues and damages at exit |
| Meal opt-out | Resident marks a meal they will skip before a cut-off time |
| Sub-meter | Meter per room or floor used to split electricity cost |
| UPI Autopay | NPCI recurring mandate; debits up to ₹15,000 per transaction do not need extra authentication per RBI framework |
| Police verification | Tenant details submitted to local police per city or state directive |
| KYC | Identity document collection and checks (Aadhaar masked, PAN, college/employee ID) |

## Decisions already made

| Decision | Reason |
|---|---|
| Per-bed pricing with a monthly minimum | Matches how owners think (revenue per bed) and how competitors charge (₹26–₹35 per bed) |
| Rent collection is the P0 anchor, not food or QR | Rent is the owner's biggest daily pain and the strongest retention hook |
| Money goes to the owner's account directly (Razorpay route or owner's own UPI); NestKeep does not hold funds | Avoids payment-aggregator licensing |
| Police verification: prepare and track the packet; owner submits on the state portal | Portals differ by state and need the owner's login |
| Store masked Aadhaar only; full documents encrypted; delete after exit plus retention period | DPDP purpose and storage limitation |
| Electricity billed at actual per-unit cost by default | Reselling power above tariff can breach state electricity rules (to be verified per state) |
| No brokerage or listing marketplace in year 1 | Focus on operations; lead page drives owner's own leads |

## Open questions

1. Name conflict check: searches on 2026-11-24 found no PG, hostel or property-software brand called NestKeep. Nearby marks: "NestKeeeper" (poultry app, iOS), Google Nest (smart home). Run an IPO trademark search in Class 9, 36 and 42 before launch. Alternatives if blocked: **BedBook**, **PGPilot**.
2. Late-fee legality: is a fixed daily late fee enforceable without a written agreement clause? Ship templated rent agreement clause; get legal review.
3. Which states to support first for police-verification packet formats (Karnataka, Telangana, Maharashtra, Delhi)?
4. Can UPI Autopay mandates above ₹15,000 work smoothly with the additional-authentication step each month? Test with Razorpay and Cashfree.
5. Should NestKeep charge residents a convenience fee on card payments (common practice) or absorb it?
6. Is there demand for deposit-free move-in via a partner (deposit insurance)? Explore in P2.
7. GST on PG rent: exemption applies only up to ₹20,000 per person per month for stays of 90+ days; rate on non-exempt stays needs confirmation after the September 2025 changes.

## Rules for agents editing these docs

- Follow [CONVENTIONS.md](../CONVENTIONS.md): sources with access date, unsourced numbers labelled **(estimate)**.
- Reference core modules instead of re-specifying them.
- Tie every new feature to one metric: acquisition, activation, retention, revenue or referral.
