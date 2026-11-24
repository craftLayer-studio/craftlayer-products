# NestKeep — product plan

## Vision

Every PG and hostel in India runs like a well-managed co-living brand: every bed full, every rupee of rent on time, every complaint closed, every resident verified, without the owner spending evenings on WhatsApp.

## Ideal customer profile (ICP)

| Attribute | Primary ICP | Secondary ICP |
|---|---|---|
| Type | Owner-run PG (with or without food) | Student hostel, small co-living operator |
| Beds | 30–150 | 150–500 across properties |
| Rent per bed | ₹5,000–₹15,000 per month | ₹12,000–₹25,000 |
| Location | Bengaluru, Hyderabad, Pune, NCR, Chennai; coaching hubs (Kota, Indore, Delhi North Campus) | Tier 2 education towns |
| Current tools | WhatsApp, notebook, Excel, GPay screenshots | A basic PG app or Excel plus accountant |
| Decision maker | Owner or owner's family member; sometimes a resident manager | Operations head |

Disqualify: under 15 beds (low ARPU), single-family rentals, hotels (route to StayBell).

## Personas

| Persona | Goal | Pain today | What NestKeep gives |
|---|---|---|---|
| Suresh, owner of 3 PGs (110 beds) in Bengaluru | Rent on time, full occupancy | Spends 5–7 days a month chasing rent; does not know true vacancy across buildings | Autopay, reminders, bed board |
| Meena, girls' PG owner near a college in Pune | Safety and parent trust | Paper visitor book; parents call about safety | Visitor log by QR, verified resident records |
| Resident manager / warden | Fewer complaints, clear tasks | Residents message at all hours; no record of what was fixed | Ticket queue with SLA |
| Cook / kitchen manager | Cook the right quantity | Cooks for 80, 55 eat | Daily meal count after opt-out cut-off |
| Resident (student or young professional) | Fair billing, quick fixes, easy payment | Unclear electricity charges; deposit disputes at exit | Clear ledger, sub-meter readings, settlement statement |
| Parent of a student resident | Safety, transparency | No visibility | Optional parent contact for payment receipts (with resident consent) |

## User journeys

### Resident journey

1. Finds PG via owner's NestKeep lead page (shared on WhatsApp, Google Business Profile, NoBroker or Housing listings) and books a visit.
2. On move-in: fills digital form, uploads ID, photo, college/employer ID, emergency contact; reads privacy notice and rules; signs rent terms digitally.
3. Sets UPI Autopay mandate for monthly rent (or pays by link each month).
4. Scans room QR to raise a complaint (water, Wi-Fi, cleaning), see today's menu, opt out of dinner, log a visitor.
5. Sees monthly bill: rent, electricity share from sub-meter, extras, late fee if any.
6. Gives notice in the app; gets exit checklist and deposit settlement statement.

### Owner journey

1. Onboarding wizard (core): properties, floors, rooms, beds, rent per sharing type, deposit rule, due date, late fee rule.
2. Imports residents from Excel or adds them; sends invite links.
3. Daily: bed board, rent due/overdue, open tickets, meal count for next meal, visitors today.
4. Monthly: rent collection report, electricity billing run, vacancy forecast (notices), deposit liabilities.

## Features by phase

### P0 — MVP sellable in 6–8 weeks

| # | Feature | Detail | Metric | Core module |
|---|---|---|---|---|
| 1 | Property, room, bed setup | Sharing types, rent per bed, deposit, bulk import from Excel | Activation: beds loaded in 24 hours | Onboarding wizard |
| 2 | Bed board | Status per bed; vacancy count; notice-ending dates | Revenue: occupancy | Analytics |
| 3 | Rent ledger and invoices | Monthly auto-invoice, partial payments, receipts on WhatsApp | Revenue: % rent collected by due date + 5 | Payments |
| 4 | UPI payment links and Autopay | Razorpay/Cashfree mandates; money to owner account | Revenue: days sales outstanding | Payments |
| 5 | Auto reminders and late fees | Reminders at −3, 0, +3, +7 days; late fee per owner rule; owner can waive | Revenue | Messaging |
| 6 | Room QR: complaints and maintenance | Category, photo, assignee, SLA, resident rating on close | Retention: tickets closed < 24 hours | QR engine, staff app |
| 7 | Tenant onboarding and KYC vault | Form, ID upload, masked Aadhaar, consent record, rules acceptance | Activation, compliance | CRM |
| 8 | Police-verification packet | Pre-filled PDF and field list per city; status (pending/submitted/verified) | Compliance: % residents verified | NestKeep-specific |
| 9 | Owner dashboard and WhatsApp daily digest | Rent due, overdue, tickets, vacancies | Retention: weekly active owners | Analytics, messaging |

### P1 — months 3–5

| # | Feature | Detail | Metric |
|---|---|---|---|
| 10 | Food menu and meal opt-out | Weekly menu; resident opts out before cut-off (for example 4 pm for dinner); kitchen gets headcount | Revenue: food cost per resident |
| 11 | Electricity sub-meter billing | Monthly reading entry (photo), per-unit rate, split among room's residents, added to invoice | Revenue: electricity cost recovered |
| 12 | Notice period and deposit settlement | Notice date, expected exit, checklist, deductions, refund via UPI | Retention, trust (reviews) |
| 13 | Visitor log by QR | Visitor name, phone, purpose, resident host approval, in/out time | Compliance, parent trust |
| 14 | Vacancy lead page | Public page with photos, sharing types, rent, "book a visit" form; lead inbox | Acquisition of residents: lead-to-move-in |
| 15 | Rent agreement template and e-sign | State-aware template with late fee and notice clauses | Activation |
| 16 | Resident referral reward | Rent discount for a referred resident who moves in | Referral |

### P2 — months 6–12

| # | Feature | Detail | Metric |
|---|---|---|---|
| 17 | Multi-property roles | Managers per property; owner sees all | Expansion |
| 18 | Accounting export | Tally / Zoho Books export, GST summaries | Retention |
| 19 | Expense tracking | Groceries, salaries, repairs per property; profit per bed | Retention |
| 20 | Smart meter integration | IoT prepaid meters per room | Revenue |
| 21 | Digital KYC verification | DigiLocker / Aadhaar offline XML | Compliance |
| 22 | Deposit-free move-in partner | Insurance-backed deposit alternative | Acquisition (residents), new revenue |
| 23 | Laundry and add-on services | Paid extras billed to ledger | ARPU |

## MVP scope and plan (6–8 weeks)

| Week | Output |
|---|---|
| 1 | Configure core: tenant, property/room/bed model, bulk import |
| 2 | Rent ledger, monthly invoice job, payment links, receipts |
| 3 | UPI Autopay mandates; reminders and late-fee rules |
| 4 | Room QR complaints and maintenance on staff app |
| 5 | Tenant onboarding form, KYC vault, police-verification packet (Karnataka, Telangana first) |
| 6 | Bed board, owner dashboard, WhatsApp daily digest; pilot at 3 PGs |
| 7–8 | Fix pilot issues; billing; convert pilots to paid |

Out of MVP: food opt-out, electricity billing, visitor log, lead page (all P1, but food opt-out can be pulled into week 6 if pilots demand it).

## Data model (NestKeep-specific entities)

| Entity | Key fields | Notes |
|---|---|---|
| Property | id, tenant_id, name, address, gender policy, licence no., food included (yes/no) | Licence field for city audits |
| Room | id, property_id, number, floor, sharing type, meter_id, qr_code_id | QR bound to room; common-area QRs have room_id null |
| Bed | id, room_id, label, rent, status, current_tenancy_id | Unit of pricing |
| Resident | id, tenant_id, name, phone, email, gender, occupation, emergency contact, consent_service, consent_marketing, consent_at | CRM record (core) |
| ResidentDocument | id, resident_id, type, masked_number, file_ref (encrypted), retention_until | Auto-delete job |
| Tenancy | id, bed_id, resident_id, start_date, rent, deposit, due_day, late_fee_rule, notice_days, notice_given_on, exit_date, status | Core of the ledger |
| Invoice | id, tenancy_id, month, lines (rent, electricity, food, extras, late fee), total, status | Core payments |
| Payment | id, invoice_id, mode (Autopay, link, cash), amount, reference, paid_at | Cash recorded by owner |
| Mandate | id, tenancy_id, provider, max_amount, status | UPI Autopay |
| VerificationRecord | id, resident_id, city, status, submitted_at, reference | Police verification |
| Ticket | id, room_id, resident_id, category, photo, assignee, created_at, resolved_at, rating | SLA metric |
| MealPlan / MealOptOut | property_id, date, meal, menu; resident_id, date, meal | Headcount = residents − opt-outs |
| MeterReading | id, meter_id, month, reading, photo, units, rate | Split per occupied bed-days |
| Visitor | id, property_id, host_resident_id, name, phone, purpose, in_at, out_at | Consent notice shown to visitor |
| Lead | id, property_id, name, phone, sharing wanted, budget, source, status | Lead inbox |
| DepositSettlement | id, tenancy_id, deductions, refund_amount, refunded_at | Exit flow |

## Integrations

| Integration | Phase | Purpose |
|---|---|---|
| Razorpay / Cashfree UPI Autopay and links (core) | P0 | Rent collection to owner account |
| WhatsApp Business Platform via BSP (core) | P0 | Reminders, receipts, digests |
| State police tenant-verification portals | P0 (packet + deep link) | Verification |
| DigiLocker | P2 | Verified ID |
| e-stamping / e-sign provider | P1 | Rent agreements |
| Tally / Zoho Books | P2 | Accounting |
| Smart meter vendors | P2 | Automated readings |
| NoBroker / Housing / Google Business Profile | P1 (links, UTM) | Lead sources for vacancy page |

## Success metrics

| Stage | Metric | Target (estimate) |
|---|---|---|
| Activation | Beds loaded and residents invited within 72 hours | ≥ 90% |
| Activation | Residents on Autopay after 60 days | ≥ 40% |
| Revenue (owner) | Rent collected by due date + 5 days | From about 70% to ≥ 90% |
| Revenue (owner) | Food cost per resident per month | −8% after opt-out live |
| Retention | Owner weekly active | ≥ 85% |
| Retention | Logo churn per month | ≤ 3.5% |
| Acquisition | Vacancy-page leads per vacant bed per month | ≥ 3 |
| Referral | New logos from owner referrals | ≥ 25% by month 9 |
