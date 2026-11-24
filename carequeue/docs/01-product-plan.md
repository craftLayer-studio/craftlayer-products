# CareQueue product plan

## Vision

No patient in a small Indian clinic should sit in a crowded waiting room without knowing when they will be seen. Every clinic runs a calm, digital front desk: token on the phone, prescription and report on WhatsApp, follow-up never forgotten, and patient data protected by default.

## Ideal customer profile

| Attribute | Ideal | Acceptable | Avoid (for now) |
|---|---|---|---|
| Type | GP, paediatric, ENT, skin, gynae OPD clinic; dental; physio | Diagnostic lab / collection centre; vet clinic; AYUSH clinic | Hospitals with IPD; corporate hospital OPDs |
| Volume | 30–120 patients/day, visible waiting crowd | 15–30/day with appointment focus (dental, physio) | Under 10/day |
| Practitioners | 1–5 | Visiting consultants on fixed days | 10+ practitioners |
| Location | Tier 1–2 city residential area | Tier 3 town with strong OPD | Rural with low smartphone use |
| Current tools | Paper tokens, register, receptionist on phone | Basic EMR used only by doctor | Locked into enterprise HMIS |
| Decision maker | Owner doctor present daily | Clinic manager with doctor approval | Committee or corporate procurement |

## Personas

| Persona | Goal | Pain today | What CareQueue gives |
|---|---|---|---|
| Owner doctor (Dr. Mehta, 45, GP, 80 patients/day, Lucknow) | See patients without chaos; keep loyal patients; protect reputation | Crowd, noise, arguments about turn, bad reviews about waiting | Ordered digital queue, calmer room, review funnel |
| Receptionist (Sunita, 30) | Manage tokens, calls, payments | Phone rings constantly "kitna time lagega?", manual register | Patients see wait on their phone; fewer calls |
| Lab manager (Arif, 34, collection centre) | Deliver reports fast | Patients call or come back to collect printouts | Report link on WhatsApp when ready |
| Physio / dentist (Dr. Rao, 36) | Patients finish treatment plans | Patients drop off after 2–3 sessions | Session reminders and follow-ups |
| Patient (Ramesh, 62, diabetic) | Be seen on time, keep prescription | Waits 1–2 hours, loses paper prescription | Live wait, e-Rx on WhatsApp, follow-up reminder |
| Pet parent (Ananya, 28) | Vaccination on time | Forgets booster dates | Vaccination due reminders |

## User journeys

### Walk-in token (P0)

1. Patient arrives, scans QR at reception ("Scan for token — no need to stand at counter").
2. First time: enters name, age, gender, phone; verifies with WhatsApp OTP. Sees privacy notice in Hindi/English/regional language with consent choices. Returning patients just confirm.
3. Picks doctor/counter and visit type (new, follow-up, report review).
4. Gets token number and live wait estimate; can leave and return. WhatsApp alerts at "3 patients ahead" and "your turn next".
5. Receptionist or doctor taps "next" on the staff app; display screen (optional TV) shows current token.
6. After consultation: practitioner-approved e-Rx and follow-up date sent on WhatsApp as secure link; payment link if not paid at counter; review request 2 hours later (only if consented and not for sensitive specialities, configurable).

### Appointment (P0)

1. Patient opens clinic link (Google Business Profile, WhatsApp, website).
2. Picks practitioner, date and either a time slot (dental, physio) or a token window (OPD).
3. Optional advance consultation fee via UPI.
4. Reminder 24 hours and 2 hours before. On arrival, scans QR to check in; joins queue in priority order configured by clinic.

### Lab report delivery (P0 for labs)

1. Sample collected; booking linked to patient phone.
2. Lab uploads PDF or marks "ready" from LIS export.
3. Patient gets WhatsApp "Your report is ready" with OTP-protected link valid for 30 days (configurable). Referring doctor can be sent a copy only if patient consented.

### Follow-up loop (P0)

1. Practitioner sets follow-up date or session plan (e.g. physio 10 sessions).
2. Reminder 2 days before and on the day; one reminder if missed.
3. Booked follow-ups count as retained visits on the dashboard.

## Clinical safety boundaries (binding)

| Allowed | Not allowed |
|---|---|
| Queue, booking, registration, payments, reminders | Symptom checkers, triage scoring, chatbots answering medical questions |
| Practitioner types e-Rx or uses their own saved templates | System-suggested drugs, doses, interactions, diagnoses |
| Showing practitioner's registration number on e-Rx (required) | Sending e-Rx without practitioner approval |
| Follow-up dates set by practitioner | Automated health advice messages |
| Health-camp notices approved by practitioner | Promotional discounts on medical services that breach professional conduct rules |
| Vaccination schedule reminders entered by the vet/doctor | Auto-generated vaccination schedules presented as advice |

Auto-reply on WhatsApp: "We cannot answer medical questions here. Please call the clinic or visit. In an emergency, call 112."

## Features by phase

Priority: P0 = MVP, sellable in 6–8 weeks. P1 = months 3–5. P2 = months 6–12.

| # | Feature | Priority | Core module | Metric |
|---|---|---|---|---|
| 1 | Reception QR token, live queue page, WhatsApp turn alerts | P0 | QR engine, booking engine, messaging | Activation |
| 2 | Staff app: call next, skip, mark no-show, priority (elderly, emergency) | P0 | Staff app | Activation |
| 3 | Patient self-registration with consent capture and family members under one phone | P0 | CRM | Activation |
| 4 | Appointment booking (slots or token windows) with optional advance fee | P0 | Booking engine, payments | Acquisition, revenue |
| 5 | Practitioner-authored e-Rx with registration number, own templates, sent as secure link | P0 | — (product-specific) | Retention |
| 6 | Follow-up date and session-plan reminders | P0 | Messaging | Retention, revenue |
| 7 | Lab report upload and secure WhatsApp delivery | P0 | Messaging, storage | Activation (labs), retention |
| 8 | UPI payment link and daily collection summary | P0 | Payments | Revenue |
| 9 | Google review request (configurable per speciality) | P0 | Reviews | Acquisition |
| 10 | Owner daily summary: patients seen, average wait, collections, follow-ups due | P0 | Analytics | Retention (of the clinic) |
| 11 | TV display mode for current token | P1 | QR engine | Activation |
| 12 | ABDM M1: ABHA verification and Scan and Share-compatible check-in; HFR/HPR linking | P1 | — (integration) | Activation, revenue (DHIS) |
| 13 | ABDM M2: link visit records/e-Rx/reports to ABHA (health information provider) | P1 | — (integration) | Revenue (DHIS share) |
| 14 | Multi-counter and multi-practitioner queues, visiting consultant schedules | P1 | Booking engine | Revenue (Plus tier) |
| 15 | Vet module: pet profiles, vaccination due reminders | P1 | CRM | Retention |
| 16 | Dental/physio treatment plans with session tracking and package payments | P1 | Payments | Revenue |
| 17 | Basic billing with GST-exempt healthcare invoice plus taxable items (e.g. products) | P1 | Payments | Activation |
| 18 | Patient data export and deletion requests workflow (DPDP rights) | P1 | CRM | Compliance |
| 19 | Home sample collection booking for labs | P2 | Booking engine | Revenue |
| 20 | Teleconsultation compliant with Telemedicine Practice Guidelines 2020 | P2 | — | Revenue |
| 21 | ABDM M3: fetch patient records with consent (health information user) | P2 | — | Retention |
| 22 | Integration with popular EMRs (export/import visit) | P2 | — | Activation |
| 23 | Multi-branch dashboard | P2 | Analytics | Revenue |

### MVP scope (6–8 weeks, 2 developers + founder)

Weeks 1–2: clinic setup, practitioners, counters, QR generation, token queue page, staff "call next" app.
Weeks 3–4: registration with consent, WhatsApp templates (token, turn alert, appointment reminder), appointment booking.
Weeks 5–6: e-Rx with templates and secure link, follow-up reminders, lab report upload and delivery, UPI link.
Weeks 7–8: owner summary, audit log, encryption review, pilot with 5 clinics (2 GP, 1 dental, 1 physio, 1 lab).

Out of MVP on purpose: full EMR, billing with insurance, pharmacy stock, ABDM (P1), teleconsultation.

## Data model (product-specific entities)

Core entities (tenant, customer, consent, message, payment, review) live in [core](../../core/README.md). CareQueue adds:

| Entity | Key fields | Retention (draft, confirm with counsel) |
|---|---|---|
| Clinic | tenant_id, name, type (opd, dental, physio, lab, vet), address, hfr_id | Life of account |
| Practitioner | clinic_id, name, qualification, registration_council, registration_number, hpr_id | Life of account |
| Counter | clinic_id, practitioner_id, name, avg_consult_min | Life of account |
| Patient | phone (household key), name, age or dob, gender, abha_address (optional), relation_to_account_holder | As per clinic policy; minimum medical records period |
| Pet | owner_patient_id, name, species, breed, dob | Same |
| Token | counter_id, patient_id, number, type (walkin, appointment), priority, status, joined_at, called_at | 1 year (analytics), then aggregate |
| Appointment | practitioner_id, patient_id, slot, status, fee_paid | Medical records period |
| Visit | token_id, practitioner_id, patient_id, notes (free text, practitioner-only), follow_up_date | Medical records period |
| Prescription | visit_id, items (text), advice (text), approved_by, approved_at, link_token, link_expires_at | Medical records period |
| Report | patient_id, lab_order_id, file_url (encrypted), ready_at, link_token, expires_at, viewed_at | Medical records period |
| SessionPlan | patient_id, practitioner_id, total_sessions, done, next_due | Medical records period |
| AccessLog | user_id, entity, entity_id, action, at, ip | At least 1 year |

All patient-linked fields encrypted at rest; file storage in an Indian region; role-based access (receptionist cannot read clinical notes or prescriptions).

## Integrations

| Integration | Purpose | Phase |
|---|---|---|
| WhatsApp Business Platform via BSP | Token alerts, reminders, report/e-Rx links | P0 |
| Razorpay / UPI | Consultation fees, advance payments | P0 |
| Google Business Profile booking link | Acquisition | P0 (manual link) |
| ABDM sandbox and production (ABHA, HFR, HPR, HIP) | ABHA verify, Scan and Share, record linking, DHIS | P1 |
| LIS export (CSV/PDF drop) for labs | Report delivery | P1 |
| TV/Chromecast display | Token board | P1 |

## Success metrics

| Stage | Metric | Target |
|---|---|---|
| Activation | Clinic issues 70%+ of tokens via CareQueue within 7 days | 70% of new clinics |
| Activation | Patients registering with phone and consent | 80% of tokens |
| Patient experience | Average in-room waiting time reduction (self-reported or measured) | 30% (estimate) |
| Retention (patient) | Follow-ups booked or attended after reminder | 40% (estimate) |
| Retention (clinic) | Monthly logo churn | under 3% |
| Revenue | Trial to paid conversion | 40% |
| Acquisition | New Google reviews per clinic per month | +15 (estimate) |
| Referral | Paying clinics referring another doctor in 6 months | 25% |
