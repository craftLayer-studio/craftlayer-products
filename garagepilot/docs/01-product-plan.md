# 01 Product plan — GaragePilot

## Vision

Every independent garage in India looks as trustworthy as a dealer workshop and remembers every customer like a family mechanic. Owners see each job, each part and each rupee; customers see their car's status and approve work from their phone; reminders bring vehicles back on time.

## Ideal customer profile

| Attribute | ICP value |
|---|---|
| Business | Independent multi-brand car garage, two-wheeler service centre, car wash or detailing studio |
| Size | 3–15 staff, 100–1,000 job cards per month |
| Geography | Tier 1 suburbs and Tier 2 cities first |
| Current tools | Paper job card book, Vyapar/Tally/Busy for billing, WhatsApp photos, a diary of phone numbers |
| Trigger | Estimate dispute, a customer who did not come back, GST notice, opening a second outlet, launching wash subscriptions |
| Budget | ₹800–₹4,000 per month (estimate: under 1% of revenue for a garage billing ₹5–15 lakh per month) |

Not ICP for MVP: authorised dealer workshops (use OEM DMS), large chains with 20+ outlets, roadside puncture shops.

## Personas

| Persona | Role | Goal | Frustration |
|---|---|---|---|
| Sandeep, 44, owner of a 6-bay multi-brand garage in Pune | Owner, ex-dealer technician | More repeat customers, higher bill per car | Customers vanish after one visit; disputes over "extra" work |
| Imran, 30, service advisor | Staff | Fast check-in, quick approvals | Calls customers 3–4 times for approvals; customers do not pick up |
| Ravi, 24, mechanic | Staff | Clear task list, fair incentive | Rework because the complaint was written badly |
| Neha, 34, car owner | End customer | Know the status and the cost before paying | "They changed parts I didn't ask for" |
| Vikram, 38, detailing studio owner in Chandigarh | Owner | Sell monthly wash plans and ceramic packages | Tracks plans in a notebook; plans expire unused |
| Fleet manager (cabs, delivery bikes) | Customer | Uptime, invoices per vehicle | Paper bills, no history |

## User journeys

### Check-in to delivery (core loop)

1. Advisor scans the vehicle number plate (OCR) or types it; history loads.
2. Records odometer, fuel level, complaints (voice-to-text in Hindi/English), and 4–8 photos or a 30-second walk-around video.
3. Job card prints or shows a QR; customer gets a WhatsApp link: "Your Swift MH12AB1234 is checked in. Track status here."
4. Mechanic inspects; advisor builds the estimate with parts from stock and labour lines; adds photos of worn parts.
5. Customer approves or declines each line on WhatsApp. Declined lines are saved as follow-up items.
6. Mechanic updates status in the staff app; customer sees progress.
7. Vehicle ready: GST invoice with UPI link; payment; delivery; Google review request 2 hours later.
8. Service-due engine sets the next due date by km and date.

### Repeat visit (money loop)

1. Engine predicts due date from avg daily km (for example, 10,000 km interval at 30 km/day gives about 330 days) or the calendar interval, whichever is first.
2. Reminder at 15 days and 3 days before due, with a booking link and slot picker.
3. Declined items get a separate reminder after 30–60 days ("Front brake pads were at 3 mm in June").
4. Booking lands in the bay calendar.

### Car wash subscription

1. Customer scans the counter QR and picks a plan (for example 4 washes per month).
2. Pays by UPI or AutoPay mandate.
3. Each visit: advisor scans the customer's plan QR; a wash is deducted.
4. Renewal reminder; unused washes shown to push usage.

### Insurance claim (P1)

1. Accident vehicle checked in with photos; claim number, insurer and surveyor entered.
2. Tracker stages: Intimated, Survey scheduled, Estimate submitted, Approved, Repair, Final bill, Payment received, Customer liability (depreciation, excess) collected.
3. Owner sees claims pending by insurer and days outstanding.

## Features by phase

Priority key: P0 = MVP, sellable in 6–8 weeks; P1 = months 3–6; P2 = months 6–12.

| Feature | Priority | Metric moved | Notes |
|---|---|---|---|
| Vehicle and customer records with history | P0 | Activation | Import from Excel/Vyapar |
| Digital job card (complaints, odometer, fuel, photos, video) | P0 | Activation, retention | Under 2 minutes per check-in |
| QR job card and WhatsApp live status link | P0 | Retention | |
| Estimate with line-item WhatsApp approval | P0 | Revenue (ARO) | Photos per line |
| GST invoice, UPI link, cash entry, credit (udhaar) ledger | P0 | Revenue | Parts and labour lines with HSN/SAC |
| Service-due engine (km + date) and reminders with booking link | P0 | Retention | The main reason to buy |
| Basic parts inventory (stock, purchase entry, reorder alert) | P0 | Revenue | |
| Mechanic assignment and status updates in staff app | P0 | Activation | |
| Owner dashboard: jobs, revenue, ARO, parts margin, due list | P0 | Retention | |
| Declined-work follow-ups | P1 | Revenue | |
| Car wash subscriptions and passes | P1 | Revenue, retention | Core payments + loyalty |
| Insurance claim tracker | P1 | Revenue | Days outstanding per insurer |
| Online booking page and Google Business link | P1 | Acquisition | |
| Mechanic time tracking and incentive sheet | P1 | Retention | |
| Google review funnel after delivery | P1 | Acquisition | Core reviews |
| Number plate OCR | P1 | Activation | |
| Hindi, Marathi, Tamil, Kannada, Malayalam UI and templates | P1 | Acquisition | |
| Multi-location, stock transfer, role permissions | P2 | Revenue (ARPU) | Pro plan |
| Tally / Zoho Books export, GSTR-1 export | P2 | Retention | |
| Parts ordering via distributor partner | P2 | Revenue (commission) | |
| Fleet accounts (per-vehicle billing, monthly statement) | P2 | Revenue | |
| OBD odometer sync | P2 | Retention | Fleets first |
| Referral rewards (refer a friend, get free wash) | P2 | Referral | Core loyalty |

## MVP scope (6–8 weeks, 2 engineers + founder)

| Week | Deliverable |
|---|---|
| 1 | Garage, user, customer, vehicle models on core; import |
| 2 | Job card flow with photo/video upload (compressed, offline queue) |
| 3 | Estimate builder; WhatsApp templates (check-in, estimate, ready, invoice, reminder) |
| 4 | Customer status page and line-item approval page |
| 5 | Invoices with GST, UPI links, credit ledger |
| 6 | Parts inventory and purchase entry; mechanic status in staff app |
| 7 | Service-due engine and reminder scheduler; owner dashboard |
| 8 | Pilot with 5 garages; fixes; pricing page; launch |

## Data model (key entities)

| Entity | Key fields |
|---|---|
| Garage | id, name, GSTIN, address, type (car/bike/wash), plan |
| Location / Bay | id, garage_id, name, bay_count |
| Customer | id, name, phone, consent_id, type (retail/fleet/insurer) |
| Vehicle | id, customer_id, reg_no, make, model, variant, fuel, year, avg_daily_km |
| JobCard | id, vehicle_id, location_id, odometer_in, fuel_level, complaints[], status, advisor_id, created_at, delivered_at |
| Inspection | id, jobcard_id, checklist_results[], media[] |
| EstimateLine | id, jobcard_id, type (part/labour), part_id, qty, price, tax_rate, status (proposed/approved/declined), media_id |
| Invoice | id, jobcard_id, number, lines, taxable, cgst, sgst, igst, total, payment_status |
| Payment | id, invoice_id, mode, amount, gateway_ref |
| Part | id, name, brand, hsn, unit_cost, sell_price, stock, reorder_level |
| PurchaseEntry | id, supplier, part lines, invoice no, date |
| MechanicTask | id, jobcard_id, mechanic_id, task, start, end |
| ServiceDue | id, vehicle_id, due_date, due_km, source_jobcard_id, reminder_status |
| InsuranceClaim | id, jobcard_id, insurer, claim_no, surveyor, stage, approved_amount, received_amount |
| WashPlan / Subscription | plan_id, customer_id, washes_left, valid_till, mandate_id |
| MessageLog | id, template, category, recipient, cost, status |

## Integrations

| Integration | Purpose | Phase |
|---|---|---|
| WhatsApp Business Platform (core BSP) | Status, approvals, invoices, reminders | P0 |
| Razorpay UPI links and AutoPay | Payments, wash subscriptions | P0, P1 |
| SMS fallback | Customers without WhatsApp | P0 |
| Google Business Profile link | Reviews and bookings | P1 |
| Vehicle data (registration lookup via licensed provider) | Auto-fill make/model | P1 |
| Tally / Zoho Books | Accounting export | P2 |
| Parts distributor APIs | Price and availability, ordering | P2 |
| OBD dongles | Odometer sync | P2 |

## Success metrics

| Metric | Target by month 6 |
|---|---|
| Activation: 20 job cards in first 7 days | 70% of new garages |
| Share of job cards with photos | 60% |
| Estimate approval via WhatsApp (not phone call) | 50% of estimates |
| Average repair order value change after 90 days | +10% (estimate; from line-item photos and declined-work follow-ups) |
| Reminder-to-booking conversion | 15–20% (estimate) |
| Monthly logo churn | Under 3% |
| Paying garages | 150 (base scenario) |
