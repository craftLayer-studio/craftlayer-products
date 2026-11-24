# CareQueue

**Tagline:** Wait from anywhere. Your token comes to your phone.

CareQueue is a QR-first front desk for small clinics, dental practices, physiotherapy centres, diagnostic labs and veterinary clinics in India. A patient scans the QR at reception, registers once, gets a token and watches the live queue on their phone instead of in a crowded waiting room. The clinic gets appointment booking, digital prescriptions written by the doctor, follow-up reminders, lab report delivery on WhatsApp, payments and reviews, with patient consent and data protection built in.

CareQueue does **not** give medical advice, triage, diagnose or suggest treatment. All clinical content comes from the registered practitioner.

## Who it is for (ICP)

- Single-doctor and 2–5 doctor OPD clinics (GP, paediatrics, ENT, dermatology, gynaecology) with 30–120 patients a day.
- Dental clinics and physiotherapy centres with repeat-visit treatment plans.
- Diagnostic labs and sample collection centres delivering reports.
- Veterinary clinics (pet parents, vaccination schedules).
- Tier 1–3 cities, receptionist plus paper token slips or a register today.

Not for: hospitals with IPD (use HMIS), large lab chains with LIMS.

## Top features (MVP)

| Feature | Metric it moves |
|---|---|
| Reception QR token with live queue status and "your turn soon" WhatsApp | Activation |
| Patient self-registration with DPDP consent (and ABHA in P1) | Activation |
| Appointment booking with slot or token-time estimate | Acquisition, revenue |
| Doctor-written digital prescription (template-based, no AI suggestions) sent on WhatsApp | Retention |
| Follow-up reminders set by the doctor | Retention, revenue |
| Lab report delivery via secure WhatsApp link | Activation (labs) |
| UPI payment and Google review request | Revenue, acquisition |

Full list with P0/P1/P2: [docs/01-product-plan.md](docs/01-product-plan.md).

## Pricing (per clinic, INR excluding GST)

| Tier | Monthly | Annual (2 months free) | For |
|---|---|---|---|
| Token | ₹699 (~$8) | ₹6,990 | QR token queue, live wait, WhatsApp turn alerts, 1 counter |
| Clinic | ₹1,499 (~$18) | ₹14,990 | 1–2 doctors: plus booking, registration, e-prescription, follow-ups, payments, reviews |
| Clinic Plus | ₹2,999 (~$35) | ₹29,990 | Up to 5 practitioners or a lab: plus report delivery, ABDM (P1), multi-counter, analytics |

30-day free trial on all tiers. WhatsApp messages billed as prepaid credits. Details: [docs/05-pricing-and-revenue.md](docs/05-pricing-and-revenue.md).

## Why it can win

- Indian clinic software sells the **EMR** first (Practo Ray from ₹999/month, Healthray from ₹499/user/month, Clinicea from $59/practitioner/month). CareQueue sells the **waiting room** first: the problem patients complain about in every review.
- Works alongside any EMR. The clinic does not have to change how the doctor writes notes.
- Government eSushrut@Clinic (₹299 effective per month after subsidy) digitises records but is not a patient-experience or WhatsApp tool; CareQueue can integrate with ABDM instead of competing on records.

## Documents

| Doc | Contents |
|---|---|
| [AGENTS.md](AGENTS.md) | Brief for AI agents, glossary, decisions, open questions |
| [01 Product plan](docs/01-product-plan.md) | Vision, personas, journeys, features by phase, data model, metrics |
| [02 Problems and benefits](docs/02-problems-and-benefits.md) | Problem, solution, benefit per stakeholder |
| [03 Pros, cons, risks](docs/03-pros-cons-risks.md) | Risks, mitigations, kill criteria |
| [04 Market research](docs/04-market-research.md) | Market size, competitors, pricing, trends, regulation, sources |
| [05 Pricing and revenue](docs/05-pricing-and-revenue.md) | Tiers, add-ons, unit economics, 12-month scenarios |
| [06 Go-to-market and onboarding](docs/06-go-to-market-and-onboarding.md) | First 10 customers, sales script, onboarding checklist, retention |

Shared platform modules: [core](../core/README.md).
