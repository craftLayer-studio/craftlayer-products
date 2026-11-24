# AGENTS.md — ClassNest

Brief for AI agents and new contributors working on ClassNest. Read this first.

## Context in five lines

- ClassNest is CraftLayer's vertical SaaS for coaching institutes, tuition centres and music/art/skill academies in India.
- Wedge: a QR code at the entrance marks student attendance and triggers parent WhatsApp alerts; UPI fee links with automatic reminders cut fee defaulters.
- Secondary wedge: the same QR engine on admission posters and flyers books demo classes into an enquiry CRM.
- The buyer is the institute owner (often also the lead teacher). Parents are the end customers who pay; students are mostly minors.
- Because most students are under 18, children's-data rules under the DPDP Act 2023 and DPDP Rules 2025 shape the data model. Treat compliance as a feature, not an afterthought.

## Reading order

1. [README.md](README.md) — one-page summary.
2. [docs/01-product-plan.md](docs/01-product-plan.md) — what to build and in which order.
3. [docs/05-pricing-and-revenue.md](docs/05-pricing-and-revenue.md) — what we charge and why.
4. [docs/06-go-to-market-and-onboarding.md](docs/06-go-to-market-and-onboarding.md) — how we sell.
5. [docs/04-market-research.md](docs/04-market-research.md) — evidence and sources.
6. [docs/02-problems-and-benefits.md](docs/02-problems-and-benefits.md) and [docs/03-pros-cons-risks.md](docs/03-pros-cons-risks.md).
7. Shared platform: [../core/README.md](../core/README.md).

## Glossary

| Term | Meaning |
|---|---|
| Institute | A tenant: one coaching business, which may have several branches |
| Branch | A physical location with its own entrance QR |
| Batch | A group of students taking the same course at the same time slot (for example "Class 10 Maths, Mon/Wed/Fri 5 pm") |
| Course | What is taught; has a fee plan and a duration |
| Fee plan | Total fee, instalment schedule, discounts, late-fee rule |
| Defaulter | Student with an instalment overdue by more than the grace period |
| Guardian | Parent or legal guardian; the WhatsApp contact and the consenting party for a minor |
| Enquiry / lead | Prospective student captured from a poster QR, walk-in or call |
| Demo class | Free trial class booked from an enquiry |
| Entrance QR | Static QR at the door; the student scans it with their own phone or a shared kiosk tablet scans the student's ID-card QR |
| Utility message | WhatsApp template category for transactional alerts (attendance, fee due); much cheaper than marketing |
| VPC | Verifiable parental consent, required under DPDP Rules 2025 Rule 10 for data of persons under 18 |

## Core modules used

| Need | Core module |
|---|---|
| Entrance and poster QR codes | QR engine |
| Demo-class booking page | Public storefront + booking engine |
| UPI fee links, AutoPay mandates | Payments (Razorpay/UPI) |
| Parent and student records, leads | Customer CRM |
| Attendance, fee and result alerts | WhatsApp/SMS messaging |
| Teacher app (mark attendance, enter marks) | Staff app |
| Fee collection, attendance, conversion reports | Analytics dashboard |
| Setup in under 30 minutes | Onboarding wizard |

ClassNest-specific modules: batches/timetable, fee plans and instalments, tests and report cards, homework/notes, teacher payouts, consent ledger for minors, coaching-guideline compliance pack.

## Decisions made

| Decision | Reason |
|---|---|
| Absence-only alerts by default; "arrived safely" alerts are an opt-in add-on | One alert per student per day costs more in WhatsApp fees than the Starter plan earns (see doc 05) |
| Parent is the primary contact; student phone optional | Parents pay; students are mostly minors; VPC flows run through the parent |
| No live-class streaming or course marketplace in MVP | Classplus, Teachmint and Edmingle own online delivery; our wedge is the offline centre |
| No ads, no behavioural tracking, no targeted marketing to students | Keeps us within the DPDP children's-data restrictions and their exemptions |
| Zero platform fee on UPI fee collection | Fee collection is the hook; we monetise via subscription and message credits |
| Android-first PWA, Hindi + English at launch | Owners and parents in Tier 2/3 cities |

## Open questions

1. Does a private coaching centre qualify as an "educational institution" for the Fourth Schedule exemptions in the DPDP Rules 2025? Until legal review answers this, build full verifiable parental consent for every student under 18.
2. Which states have notified their own coaching-centre laws based on the Ministry of Education 2024 guidelines, and what reports do they require? Needed for the compliance pack.
3. Can education fees get a higher UPI AutoPay no-AFA limit than ₹15,000? Sources disagree (see doc 04). Affects whether quarterly fees can be auto-debited.
4. Should music/art academies get a separate landing page and plan ("ClassNest Studio")? Their needs (monthly fees, slot booking, recitals) differ from exam coaching.
5. Name check: no established product named "ClassNest" was found (only a hackathon project on FOSS United). Similar names exist (Classplus, ClassInTown, ClassNet). Run an Indian trademark search in Class 9, 41 and 42 before launch. Backup names if a conflict appears: **BatchBell**, **TuitionTrack**.
