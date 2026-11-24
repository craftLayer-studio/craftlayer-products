# CareQueue pros, cons and risks

## Pros

| Pro | Why it matters |
|---|---|
| Visible, universal pain | Waiting rooms are crowded; studies show waits many times longer than consultations (see 04). The doctor sees the problem every day. |
| Fast demo, fast value | QR token works on day one with no change to how the doctor practices. |
| Large base | About 13.86 lakh registered allopathic doctors plus 7.5 lakh AYUSH practitioners (see 04). |
| Low churn potential | Clinics are stable businesses; once patients expect tokens on phone, switching back is hard. |
| Government tailwind | ABDM has 90+ crore ABHA accounts and pays DHIS incentives for linked records; integration adds value and revenue. |
| Shared core | Queue, booking, CRM, WhatsApp and payments come from CraftLayer core. |
| Multiple sub-verticals | GP, dental, physio, labs, vets share 80% of the product. |

## Cons

| Con | Impact |
|---|---|
| Doctors are busy and hard to meet | Higher CAC than salons; sales happens before or after OPD hours. |
| Crowded EMR market (Practo Ray, Healthray, Eka Care, HealthPlix, DocOn, MocDoc, Clinicea) | Some already offer queues; we must stay "front desk first" and integrate, not fight on EMR. |
| Government low-cost alternative | eSushrut@Clinic at ₹299 effective per month after subsidy (see 04) anchors price expectations low for records software. |
| Health data liability | Higher security, legal and support cost than other CraftLayer verticals. |
| Professional conduct restrictions on advertising | Limits marketing campaigns as an upsell; review requests must be tactful. |
| Older patients less comfortable with QR | Receptionist must still be able to issue tokens manually. |

## Risks and mitigations

| Risk | Likelihood | Impact | Mitigation |
|---|---|---|---|
| Patient data breach | Low–medium | Very high | Encryption at rest/in transit; India region; role-based access; OTP-protected expiring links instead of attachments; access logs kept 1+ year; annual third-party pen test; breach response plan meeting DPDP Rules 2025 notice duties (to Board and affected persons). |
| DPDP non-compliance | Medium | High | Clinic is data fiduciary, CareQueue is processor under a written data processing agreement; consent logged with notice version; deletion/export workflow; core rules apply from about May 2027, build now. |
| Feature drifts into medical advice (e.g. "AI prescription") | Medium | Very high | Binding clinical safety boundaries in [01](01-product-plan.md); product review checklist; no AI clinical features. |
| Receptionist keeps paper tokens in parallel | High | High | Onboarding on site at OPD time; TV display; set "QR only" target by day 7; printable token fallback inside the app for non-smartphone patients. |
| WhatsApp template rejection or quality drop | Medium | Medium | Utility templates only for service messages; no promotional content; monitor quality rating. |
| EMR vendors bundle free queues | Medium | Medium | Integrate with EMRs; win on patient-side experience, WhatsApp alerts and price. |
| eSushrut@Clinic adoption by small clinics | Medium | Medium | Position CareQueue as complementary (queue, WhatsApp, payments, reviews), not a records system; consider integration via ABDM. |
| Telemedicine or e-Rx rule changes | Low | Medium | Keep e-Rx format aligned with Telemedicine Practice Guidelines 2020 annexure; registration number on all e-Rx; track NMC notices. |
| Sensitive specialities (psychiatry, sexual health, IVF) | Medium | High | Per-clinic setting: no review requests, discreet message wording ("Your appointment at [clinic]" only), shorter link validity. |
| CAC too high for ₹1,499 ARPU | Medium | High | Lean on doctor referrals, medical association events, lab partner channels; annual prepaid push. |

## Kill criteria

| Checkpoint | Kill or pivot if |
|---|---|
| Week 8 (pilot, 5 clinics) | Fewer than 3 clinics issue 50%+ of tokens through CareQueue after 2 weeks |
| Week 12 | Fewer than 10 paying clinics after 80+ doctor demos |
| Month 4 | Trial-to-paid below 20% |
| Month 6 | Monthly logo churn above 6% for 2 consecutive months, or CAC payback above 10 months |
| Month 9 | Fewer than 50 paying clinics or MRR below ₹80,000 |
| Any time | A security incident exposing patient data caused by a design flaw: pause sales until fixed and audited |

Pivot options before killing: (a) labs only (report delivery + home collection, clearer ROI), (b) dental and physio only (appointment and session-plan focus, higher ARPU), (c) white-label queue for EMR vendors.
