# CareQueue — brief for AI agents

## Context

CareQueue is the small-clinic product in the CraftLayer portfolio. It runs on the shared CraftLayer core (QR engine, booking engine, CRM, WhatsApp messaging, payments, reviews, staff app, analytics). This folder documents only what is specific to clinics, dental, physio, diagnostic labs and veterinary practices.

Commercial thesis: in Indian outpatient settings, waiting time is many times longer than consultation time (studies report 59–98 minute waits against 6–7 minute consultations; see [04](docs/04-market-research.md)). Small clinics run on paper token slips and a shouting receptionist. A QR token with a live queue on the patient's phone is a visible, cheap fix that a doctor can buy in one conversation. Once the clinic has the patient's number with consent, follow-ups, prescriptions on WhatsApp and report delivery add retention and revenue.

Health data is high-stakes. Product, copy and agents must treat it carefully.

## Reading order

1. [README.md](README.md)
2. [docs/01-product-plan.md](docs/01-product-plan.md) — including the "clinical safety boundaries" section.
3. [docs/04-market-research.md](docs/04-market-research.md) — regulation section before writing any feature.
4. [docs/05-pricing-and-revenue.md](docs/05-pricing-and-revenue.md)
5. [docs/06-go-to-market-and-onboarding.md](docs/06-go-to-market-and-onboarding.md)
6. [docs/02-problems-and-benefits.md](docs/02-problems-and-benefits.md), [docs/03-pros-cons-risks.md](docs/03-pros-cons-risks.md)

## Glossary

| Term | Meaning |
|---|---|
| Clinic | One physical practice location. Pricing is per clinic. |
| Practitioner | Registered doctor, dentist, physiotherapist or veterinarian who consults. |
| Counter | A queue served by one practitioner or one service point (e.g. sample collection). |
| Token | Queue number given at check-in. Can be walk-in or appointment. |
| Live wait | Estimated minutes until a token is called, shown on the patient's phone. Based on rolling average consultation time. |
| e-Rx | Digital prescription authored and approved by the practitioner. |
| Follow-up | Revisit date set by the practitioner; triggers a reminder. |
| Report delivery | Lab or imaging report sent as an OTP-protected link on WhatsApp. |
| ABDM | Ayushman Bharat Digital Mission, India's national digital health network. |
| ABHA | Ayushman Bharat Health Account: the patient's 14-digit health ID / address. |
| HFR / HPR | Health Facility Registry / Healthcare Professionals Registry under ABDM. |
| Scan and Share | ABDM feature where a patient scans a facility QR to share ABHA profile and get a token. |
| M1 / M2 / M3 | ABDM integration milestones: ABHA creation/verification; linking records as health information provider; fetching records as health information user. |
| DHIS | Digital Health Incentive Scheme: ABDM pays facilities per ABHA-linked digital record above a base level; software vendors get a share. |
| Data fiduciary / processor | Under DPDP Act: the clinic decides purpose (fiduciary); CareQueue processes on its behalf (processor). |

## Decisions made

1. **No medical advice features.** No symptom checker, triage, AI diagnosis, drug suggestions or dosage calculators. Prescriptions are typed or picked from the practitioner's own saved templates and must be approved by the practitioner before sending.
2. **Queue first, EMR light.** We do not try to replace full EMRs. MVP has registration, visit record, e-Rx and follow-up date. Clinical notes are free text owned by the practitioner.
3. **Per-clinic flat pricing**, 30-day free trial, no permanent free tier (storage of health data carries cost and liability).
4. **Report and prescription sharing uses OTP-protected links**, not PDF attachments, so data is not left in chat backups without control, and links can expire.
5. **Consent at registration** with separate checkboxes: (a) service messages for this visit (token, report, prescription), (b) follow-up reminders, (c) offers and health camp news. Only (a) is required to use the queue.
6. **India data residency.** Store all patient data in Indian cloud regions; encrypt at rest and in transit; access logs kept at least one year.
7. **Marketing restraint.** Doctors in India are bound by professional conduct rules on advertising. CareQueue sends no promotional campaigns by default; only practitioner-approved reminders and health-camp notices.
8. **Vets** use the same product with pet profiles; ABDM does not apply.

## Open questions

1. **Name check.** No major established brand named "CareQueue" was found; only two 2025 hackathon projects on Devfolio and a similar-sounding cloud queue tool "QueueCare" (see [04](docs/04-market-research.md)). Folder slug and name stay `carequeue`. Run a formal trademark search (Class 9, 42, 44) before launch. Backup names if a conflict appears: **TokenCare**, **ClinicQ**.
2. ABDM integration timing: build M1 (ABHA verify via Scan and Share) in P1 or wait for 50 paying clinics? DHIS incentive and doctor interest argue for P1.
3. Should CareQueue be ABDM-certified as an HMIS/clinic software to earn the 25% DSC share of DHIS incentives, or stay as a front-desk tool that integrates with certified EMRs?
4. Teleconsultation (P2): build to Telemedicine Practice Guidelines 2020, or partner?
5. Does the government eSushrut@Clinic (₹299 effective/month) cap what small clinics will pay? Test price sensitivity in pilot.
6. Children's data: confirm with counsel the scope of DPDP Rules 2025 exemption from verifiable parental consent for clinical establishments and healthcare professionals (paediatric clinics, vet not affected).
7. Medical records retention period for small clinics (commonly cited 3 years under Indian Medical Council professional conduct regulations 2002; verify) versus DPDP erasure on request: define the rule with counsel.
8. Payments for consultation: GST-exempt healthcare services versus our GST-bearing subscription: confirm invoice handling with CA.

## Rules for agents editing this folder

- Follow [CONVENTIONS.md](../CONVENTIONS.md).
- Never add a feature that gives a patient or staff member clinical advice. If unsure, it is out of scope.
- Every new number needs a source link with access date, or **(estimate)** with reasoning.
- Tie every feature to one metric: acquisition, activation, retention, revenue or referral.
- Any new data field about patients needs a stated purpose and retention rule.
