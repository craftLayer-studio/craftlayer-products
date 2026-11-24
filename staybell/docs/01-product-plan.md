# StayBell — product plan

## Vision

Every small stay in India owns its guest relationship. A guest who stays once through an OTA comes back directly, and while they are in the room, every request and every rupee of in-stay spend goes through the owner's own channel.

## Ideal customer profile (ICP)

| Attribute | Primary ICP | Secondary ICP |
|---|---|---|
| Property type | Homestay, guest house, independent budget hotel | Small resort, boutique stay, heritage property |
| Rooms | 6–30 | 30–60, or 2–3 properties |
| ADR | ₹1,500–₹5,000 (inside the 5% GST band) | ₹5,000–₹12,000 |
| OTA dependence | 50%+ of room nights from OTAs (estimate) | Mix of OTA, walk-in, travel agent |
| Location | Hill stations, beaches, pilgrimage towns, Tier 2 business towns | Wildlife and wellness resorts |
| Current tools | Paper register, Excel, WhatsApp, maybe eZee/Djubo | Full PMS plus channel manager |
| Decision maker | Owner or owner's son/daughter running operations | General manager with owner approval |

Disqualify: OYO/Treebo franchise properties (brand controls guest data), properties under 4 rooms, hostels with dorm beds (route to NestKeep or a hostel-specific plan later).

## Personas

| Persona | Goal | Pain today | What StayBell gives |
|---|---|---|---|
| Rakesh, owner of a 14-room hotel in Rishikesh | More profit per room night | Pays MakeMyTrip 18–25%; does not know who his repeat guests are | Guest CRM, direct booking site, WhatsApp campaigns |
| Anjali, homestay host in Coorg | Run the stay without being on call all night | Guests call her mobile for towels, food, Wi-Fi password | Room QR with request routing to caretaker |
| Front-desk / caretaker staff | Fewer calls, clear task list | Requests lost on phone; blamed in reviews | Staff app with request queue and timers |
| Guest (domestic) | Fast check-in, quick food, no app download | Paper forms, wait for ID photocopy, phone the desk repeatedly | Web page from QR, pre-arrival check-in, UPI pay |
| Guest (foreign) | Smooth arrival | Passport and visa details re-entered on paper | Upload passport and visa once; owner gets Form C data pack |

## User journeys

### Guest journey

1. Booking confirmed (OTA or direct). Owner sends WhatsApp utility message with a pre-check-in link (P1) or guest scans the desk QR on arrival (P0).
2. Guest enters name, phone, address, purpose of visit, uploads ID (Aadhaar masked, DL, passport and visa for foreigners), accepts privacy notice. Separate optional opt-in for offers.
3. In the room, guest scans Room QR: Wi-Fi details, menu, housekeeping, "report a problem", local experiences, late checkout.
4. Orders food; pays by UPI or adds to room bill. Kitchen gets the order on the staff app.
5. On checkout, a review prompt: 4–5 stars go to Google review link, 1–3 stars go to a private feedback form and the owner is alerted.
6. 30–90 days later (only if opted in): "Book direct next time, get 10% off and free breakfast" with link to the owner's booking site.

### Owner journey

1. Signs up through onboarding wizard (core): property details, rooms, menu, staff phone numbers.
2. Prints QR standees (we ship them in week 1).
3. Daily: sees requests board, check-ins, foreign guests pending Form C, open complaints.
4. Weekly: sees direct vs OTA bookings, repeat guests, review score, F&B revenue per occupied room.
5. Monthly: runs one WhatsApp campaign to past guests for slow dates.

## Features by phase

### P0 — MVP sellable in 6–8 weeks

| # | Feature | Detail | Metric | Core module |
|---|---|---|---|---|
| 1 | Room QR pages | One QR per room, room-aware URL, no app install, Hindi and English | Activation: % rooms with QR scanned in week 1 | QR engine, storefront |
| 2 | In-room dining | Menu, cart, notes, pay by UPI or add to room bill; kitchen ticket | Revenue: F&B per occupied room | Ordering, payments |
| 3 | Housekeeping and service requests | Towels, cleaning, water, maintenance; assigned staff; SLA timer | Retention: complaints resolved in < 30 minutes | Staff app |
| 4 | Complaints with escalation | Category, photo, escalates to owner WhatsApp after 15 minutes unresolved | Retention: review score | Messaging |
| 5 | Digital check-in and guest register | Guest form, ID upload, consent capture, printable/exportable register (CSV and PDF) | Activation: check-ins done digitally | CRM |
| 6 | Form C data pack | For foreign guests: all Form C fields captured and shown in portal order, reminder at 12 hours and 20 hours after arrival | Compliance: Form C filed < 24 hours | StayBell-specific |
| 7 | Guest CRM | Every check-in and scanner, stay history, tags, opt-in status | Retention: contactable guests per month | CRM |
| 8 | Review funnel | Post-checkout rating, route to Google review link or private feedback | Acquisition: new Google reviews per month | Reviews |
| 9 | Owner dashboard | Today's requests, check-ins, revenue, review score | Retention: weekly active owners | Analytics |

### P1 — months 3–5

| # | Feature | Detail | Metric |
|---|---|---|---|
| 10 | Direct booking site and booking engine | Template site, room types, rates, availability calendar, UPI/card, 0% commission, "best rate direct" badge | Revenue: direct room nights |
| 11 | Upsell catalog | Late checkout, early check-in, room upgrade, packages, local experiences (vendor-supplied) | ARPU, in-stay revenue |
| 12 | WhatsApp concierge | Pre-arrival message, directions, check-in link, checkout bill, post-stay review | Retention |
| 13 | Campaigns to past guests | Segments (stayed in last 12 months, weekend guests, families), slow-date offers | Revenue: repeat bookings |
| 14 | Pre-arrival online check-in | Link before arrival, ID upload in advance | Activation |
| 15 | Referral offer | Guest shares a link; friend gets direct discount; guest gets free breakfast next stay | Referral |

### P2 — months 6–12

| # | Feature | Detail | Metric |
|---|---|---|---|
| 16 | Channel manager integration | Read OTA bookings from STAAH/Djubo/eZee to auto-create guest records | Activation, retention |
| 17 | Rate parity monitor | Show if OTA price is lower than direct price | Revenue |
| 18 | Multi-property | Group dashboard, shared CRM | Expansion |
| 19 | Simple PMS lite | Room status board, folio, GST invoice | ARPU, retention |
| 20 | Experiences marketplace | Local vendors list experiences; StayBell takes 10% from vendor | New revenue stream |
| 21 | Loyalty | Stay count rewards | Retention |

## MVP scope and plan (6–8 weeks)

| Week | Output |
|---|---|
| 1 | Configure core: tenant, rooms, QR generation, room-aware storefront |
| 2 | In-room dining and requests on staff app; WhatsApp alert to owner |
| 3 | Digital check-in form, ID upload to encrypted storage, consent capture, register export |
| 4 | Form C data pack and reminders; complaints with escalation |
| 5 | Review funnel, owner dashboard, Hindi strings |
| 6 | Pilot at 3 properties (free 30 days), fix issues |
| 7–8 | Print kit, onboarding wizard polish, billing; convert pilots to paid |

Out of MVP: booking engine, channel manager, payments split, PMS functions.

## Data model (StayBell-specific entities)

| Entity | Key fields | Notes |
|---|---|---|
| Property | id, tenant_id, name, address, GSTIN, star/category, check-in/out times, Form C portal user id (not password) | One tenant may have several properties |
| Room | id, property_id, number, type, floor, qr_code_id, status | QR is bound to room |
| RoomType | id, property_id, name, base_rate, max_guests, amenities | Used by booking engine (P1) |
| Stay | id, property_id, room_id, guest_id (primary), arrival_at, departure_at, source (OTA name / direct / walk-in), booking_ref, amount | Source drives direct-share metric |
| Guest | id, tenant_id, name, phone, email, city, nationality, consent_service, consent_marketing, consent_at, consent_text_version | CRM record (core) |
| GuestDocument | id, guest_id, stay_id, type (Aadhaar masked / DL / passport / visa), file_ref (encrypted), retention_until | Auto-delete job |
| FormCRecord | id, stay_id, passport_no, visa_no, visa_type, arrival_from, next_destination, status (pending/filed), filed_at, filed_by | Reminder job |
| ServiceRequest | id, stay_id, room_id, category, note, photo, assigned_to, created_at, resolved_at | SLA metric |
| Order | core order with room_id, stay_id, payment_mode (UPI / room bill) | Core ordering |
| Upsell | id, property_id, name, price, type (late checkout / experience / package), vendor_id | P1 |
| Review | core review with stay_id, rating, routed_to | Core reviews |

## Integrations

| Integration | Phase | Purpose |
|---|---|---|
| Razorpay / UPI (core) | P0 | In-room orders, direct bookings |
| WhatsApp Business Platform via BSP (core) | P0 | Alerts, concierge, campaigns |
| Google Business Profile review link | P0 | Review funnel |
| Bureau of Immigration Form C portal | P0 (deep link only) | Foreign guest reporting |
| DigiLocker / Aadhaar offline XML (masked) | P1 | Verified ID without storing full Aadhaar number |
| STAAH, Djubo, eZee APIs | P2 | Import OTA bookings |
| Tally / Zoho Books export | P2 | Accounting |

## Success metrics

| Stage | Metric | Target (estimate) |
|---|---|---|
| Activation | Rooms with QR scanned at least once in first 7 days | ≥ 70% |
| Activation | Check-ins done digitally in month 1 | ≥ 50% |
| Retention | Owners active weekly | ≥ 80% |
| Retention | Logo churn per month | ≤ 3% |
| Revenue | In-room F&B per occupied room night | +15% vs pre-StayBell baseline |
| Revenue | Direct share of room nights after 6 months (Direct plan) | +10 percentage points |
| Acquisition | New Google reviews per property per month | 2x baseline |
| Referral | Customers from owner referrals | ≥ 20% of new logos by month 9 |
