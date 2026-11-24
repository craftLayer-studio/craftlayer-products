# StayBell — agent brief

Read this before editing any StayBell doc or building any StayBell feature.

## Context in five lines

1. StayBell is a CraftLayer vertical product for small hotels, homestays, guest houses and small resorts in India (5–60 rooms).
2. Wedge: a QR code in every room. Guests self-serve (food, housekeeping, complaints, upsells, digital check-in); the owner captures consented guest contacts.
3. Money story: cut OTA commission (15–25% per booking) by converting past guests into direct, repeat bookings through the owner's own booking site and WhatsApp.
4. StayBell is not a full PMS or channel manager. It sits beside eZee, Djubo, STAAH or a paper register and integrates later (P2).
5. India-first, priced in INR, built on the shared [`core/`](../core/README.md) platform.

## Reading order

1. [README.md](README.md) — one-page summary
2. [docs/01-product-plan.md](docs/01-product-plan.md) — what to build and in what order
3. [docs/05-pricing-and-revenue.md](docs/05-pricing-and-revenue.md) — how it makes money
4. [docs/06-go-to-market-and-onboarding.md](docs/06-go-to-market-and-onboarding.md) — how to sell it
5. [docs/04-market-research.md](docs/04-market-research.md) — evidence and sources
6. [docs/02-problems-and-benefits.md](docs/02-problems-and-benefits.md) and [docs/03-pros-cons-risks.md](docs/03-pros-cons-risks.md)

## Glossary

| Term | Meaning |
|---|---|
| ADR | Average daily rate: room revenue divided by room nights sold |
| OTA | Online travel agency: MakeMyTrip, Goibibo, Booking.com, Agoda, Airbnb |
| PMS | Property management system: reservations, front desk, folio, night audit |
| Channel manager | Syncs rates and inventory to many OTAs (STAAH, Djubo, eZee Centrix) |
| Booking engine | Commission-free booking widget on the hotel's own site |
| Form C | Mandatory report of a foreign guest's stay to the Bureau of Immigration within 24 hours of arrival, filed on the online Form C portal |
| FRRO | Foreigners Regional Registration Office |
| Guest register | Record of guest name, address, ID, arrival/departure, required by local police norms |
| Room QR | The printed QR standee or sticker in each room; resolves to a room-specific page |
| Upsell | Paid add-on sold during the stay: late checkout, experiences, packages |
| Direct share | Share of room nights booked without an OTA |
| DPDP | Digital Personal Data Protection Act 2023 and DPDP Rules 2025 |
| NIDHI+ | Ministry of Tourism's National Integrated Database of Hospitality Industry |

## Decisions already made

| Decision | Reason |
|---|---|
| Do not build a full PMS or channel manager in year 1 | Crowded, sticky market (eZee, Djubo, STAAH, Hotelogix); integration beats replacement |
| Room QR plus digital check-in is the P0 wedge | Visible on day 1, no behaviour change for owner, collects guest contacts with consent |
| 0% commission on direct bookings | Core sales message is "stop paying 15–25%"; a commission would undercut it |
| Flat monthly plans by room band, not per booking | Small owners prefer predictable bills; anchors below ₹2,250/month eZee entry price |
| Form C: prepare data and deep-link, do not file on the guest's behalf in MVP | Portal requires the property's own login; automating it risks credential handling |
| ID images stored encrypted, auto-deleted after the retention period set by the owner (default 1 year, estimate) | DPDP purpose limitation and storage limitation |
| WhatsApp marketing only to guests who opted in | Meta policy and DPDP; utility messages (booking confirmation) do not need marketing opt-in |

## Open questions

1. Name conflict check: web searches on 2026-11-24 found no hotel-software brand called StayBell. Similar marks exist (STAY guest app, IHG's Staybridge Suites). Run an IPO trademark search in Class 9, 35, 42 and 43 before launch. Alternatives if blocked: **RoomRing**, **StayDesk QR**.
2. Which channel manager to integrate first: STAAH (wide India reach) or Djubo / eZee Centrix? Decide after first 20 customers by counting what they use.
3. Can the Form C portal be filled by a browser extension the owner runs under their own login (no credential storage)? Needs legal review.
4. Pricing per property vs per room above 60 rooms: unvalidated.
5. GST 5% without ITC (from 22 September 2025): does it make owners more or less willing to pay for software? Test in sales calls.
6. Should StayBell take a commission on third-party experiences (taxi, trek, scuba) sold through the room QR? Proposed 10% from the vendor, not the hotel.

## Rules for agents editing these docs

- Follow [CONVENTIONS.md](../CONVENTIONS.md): sources with access date, unsourced numbers labelled **(estimate)**.
- Reference core modules instead of re-specifying them.
- Tie every new feature to one metric: acquisition, activation, retention, revenue or referral.
