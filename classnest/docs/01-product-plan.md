# 01 Product plan — ClassNest

## Vision

Every offline coaching centre in India runs its front desk on ClassNest. Parents always know whether their child reached class, how they scored and what fee is due. Owners collect fees on time and fill batches every admission season without hiring a manager.

## Ideal customer profile

| Attribute | ICP value |
|---|---|
| Business | Offline coaching or tuition centre, or skill academy (music, dance, art, chess, coding, spoken English) |
| Size | 50–400 active students, 2–10 teachers, 1–2 branches |
| Geography | Tier 2 and Tier 3 cities first; Tier 1 suburbs second |
| Current tools | Paper register, Excel, WhatsApp groups, UPI QR sticker, a fee diary |
| Trigger | A bad fee month, an admission season starting (March–June, and October–November for crash courses), a parent complaint about an absent child |
| Budget | ₹500–₹2,500 per month (estimate: 0.3–1% of revenue for a centre with 150 students at ₹1,500/month average fee) |

Not ICP for MVP: large chains with 10+ branches, schools, pure online creators, home tutors with fewer than 20 students.

## Personas

| Persona | Role | Goal | Frustration |
|---|---|---|---|
| Rajesh, 41, owner of a Class 9–12 science coaching centre in Indore | Owner and physics teacher | Collect ₹4–6 lakh fees per month on time; get 80 new admissions in April | Spends Sundays calling defaulters; loses leads written on paper |
| Priya, 29, front-desk coordinator | Staff | Finish attendance, fee entries and parent calls before the evening batch | Parents call to ask "did my son come today?" |
| Mr. Sharma, 45, parent | Pays fees | Know the child attended and is improving | Finds out about bunked classes weeks later |
| Aarav, 16, student | Learner | Get notes and test scores without chasing teachers | Notes lost in a 200-member WhatsApp group |
| Meena, 35, owner of a music academy in Coimbatore | Owner and instructor | Monthly fees and makeup classes tracked | Students skip fees for "missed" classes |
| Arjun, 27, part-time chemistry teacher | Teacher | Correct monthly payout | Disputes over hours taught |

## User journeys

### Daily attendance (core loop)

1. Student scans the entrance QR with their phone, or the teacher taps "present" on the batch list in the staff app.
2. 15 minutes after batch start, ClassNest marks unscanned students absent.
3. Parent of each absent student receives a WhatsApp utility template: "Aarav was marked absent for Physics 5:00 pm batch today. Reply 1 if you know, 2 to call the institute."
4. Owner sees today's attendance by batch and a weekly list of chronic absentees.

### Fee cycle (money loop)

1. Owner assigns a fee plan at admission (one-shot, monthly, or 2–4 instalments).
2. ClassNest sends a UPI payment link 3 days before each due date, on the due date, and at D+3 and D+7.
3. Parent pays by UPI; receipt with GST details arrives on WhatsApp instantly.
4. Cash payments are entered by staff and get the same receipt.
5. Defaulter dashboard shows overdue amount by batch; one tap sends a polite escalation or schedules a call.

### Admission season (growth loop)

1. Owner prints the poster QR on flyers, banners and newspaper inserts.
2. Parent scans, sees courses, fees, faculty and results, and books a free demo class.
3. Lead enters the enquiry pipeline: New, Demo booked, Demo attended, Fee discussed, Admitted, Lost.
4. Auto WhatsApp: demo reminder, post-demo feedback, offer expiry.
5. Admitted lead converts into a student with a fee plan in one tap.

### Results and report card (retention loop)

1. Teacher enters marks per test in the staff app (or uploads a sheet).
2. ClassNest computes rank, percentile and trend.
3. Parent receives a report-card link on WhatsApp; monthly summary with attendance and fee status.

## Features by phase

Priority key: P0 = MVP, sellable in 6–8 weeks; P1 = months 3–6; P2 = months 6–12.

| Feature | Priority | Metric moved | Notes |
|---|---|---|---|
| Institute, branch, batch, course setup with Excel import | P0 | Activation | Onboarding wizard from core; target setup in under 30 minutes |
| Student and guardian records with consent capture | P0 | Activation | Verifiable parental consent for under-18s (see compliance) |
| Entrance QR attendance + one-tap teacher marking | P0 | Retention | Works offline on the staff app; syncs later |
| Absence alerts to parents on WhatsApp | P0 | Retention | Utility template; absence-only by default |
| Fee plans, instalments, discounts, late fee | P0 | Revenue | Pro-rata refund calculator for the 2024 guidelines |
| UPI payment links and auto-reminders | P0 | Revenue | Razorpay via core payments |
| Digital receipts with GST fields | P0 | Revenue | Coaching is taxable at 18% GST (see doc 04) |
| Defaulter dashboard | P0 | Revenue | The demo moment in every sales call |
| Enquiry CRM + poster QR demo booking | P0 | Acquisition | Needed before March admission season |
| Owner dashboard (attendance %, collected vs due, leads) | P0 | Retention | |
| Batches and timetable with clash detection | P1 | Activation | |
| Tests, marks, rank and parent report cards | P1 | Retention, referral | Report cards are shared by parents; add "Powered by ClassNest" |
| Homework and notes per batch | P1 | Retention | PDF and image; storage cap per plan |
| Teacher payouts (per batch, per hour, per student) | P1 | Retention | Owner stickiness; hard to migrate away |
| UPI AutoPay mandates for monthly fees | P1 | Revenue | Within NPCI limits |
| "Arrived safely" alerts add-on | P1 | Revenue (ARPU) | Per-message credits |
| Hindi, Marathi, Tamil, Telugu, Bengali UI and templates | P1 | Acquisition | |
| Compliance pack (registration data, student age check, refund log, fee display page) | P1 | Retention | For states that notify coaching laws |
| Multi-branch and role permissions | P2 | Revenue (ARPU) | Pro plan |
| Student app (notes, tests, schedule) | P2 | Retention | PWA |
| Online test engine (MCQ with auto-grading) | P2 | Revenue (ARPU) | Add-on |
| Fee financing partner (EMI for annual fees) | P2 | Revenue | Referral commission |
| Referral program (parent refers parent, fee discount) | P2 | Referral | Uses core loyalty |
| Music/art academy mode (slots, makeup classes, recitals) | P2 | Acquisition | |

## MVP scope (6–8 weeks, 2 engineers + founder)

| Week | Deliverable |
|---|---|
| 1 | Tenant, branch, course, batch, student, guardian models on core; Excel import |
| 2 | Staff app attendance; entrance QR scan flow; offline sync |
| 3 | WhatsApp utility templates approved (absence, fee due, receipt, demo reminder); absence alert job |
| 4 | Fee plans, instalments, ledger, UPI links, receipts |
| 5 | Reminder scheduler; defaulter dashboard; cash entry |
| 6 | Poster QR, demo booking page, enquiry pipeline |
| 7 | Owner dashboard; consent capture and consent ledger; onboarding wizard polish |
| 8 | Pilot with 5 institutes; fix; pricing page; launch |

Out of MVP: live classes, video hosting, online course store, student app, payroll beyond a payout sheet.

## Data model (key entities)

| Entity | Key fields |
|---|---|
| Institute | id, name, GSTIN, registration number (state), plan, owner_user_id |
| Branch | id, institute_id, address, entrance_qr_id |
| Course | id, name, duration, fee_plan_template_id |
| Batch | id, course_id, branch_id, teacher_ids, schedule (days, start, end), room, capacity |
| Student | id, name, date_of_birth, class/grade, photo (optional), status |
| Guardian | id, name, phone, relation, consent_id |
| Consent | id, guardian_id, student_id, purposes[], method (OTP + DigiLocker/ID check), timestamp, withdrawn_at |
| Enrolment | id, student_id, batch_id, start_date, end_date, fee_plan_id |
| FeePlan | id, total, instalments[{due_date, amount}], discount, late_fee_rule |
| Payment | id, enrolment_id, amount, mode (UPI/cash/card), gateway_ref, receipt_no, gst_amount |
| Refund | id, enrolment_id, pro_rata_amount, requested_at, paid_at |
| AttendanceEvent | id, student_id, batch_id, date, status, source (QR/teacher), alert_sent |
| Test / Mark | test_id, batch_id, max_marks; student_id, score, rank |
| Material | id, batch_id, file_url, type |
| Lead | id, source (poster QR id, walk-in, call), guardian phone, course interest, stage, demo_slot |
| Teacher / Payout | teacher_id, rate_type, rate; month, sessions, amount, paid_at |
| MessageLog | id, template, category, recipient, cost, status |

## Integrations

| Integration | Purpose | Phase |
|---|---|---|
| WhatsApp Business Platform (via core BSP) | Alerts, reminders, receipts, report cards | P0 |
| Razorpay (UPI links, AutoPay, cards) | Fee collection | P0 (links), P1 (AutoPay) |
| SMS fallback | Parents without WhatsApp | P0 |
| DigiLocker or OTP-based ID check | Verifiable parental consent | P0 (OTP), P1 (DigiLocker) |
| Google Sheets / Excel import-export | Migration and accountant handoff | P0 |
| Tally / Zoho Books export | GST accounting | P2 |
| Biometric or RFID devices | Large institutes that already own them | P2 |

## Success metrics

| Metric | Target by month 6 |
|---|---|
| Activation: institute marks attendance on 5 of first 7 days | 70% of new accounts |
| Fee collected through ClassNest / total fee due | 60% |
| Reduction in overdue amount after 60 days (customer-reported) | 30% (estimate) |
| Lead-to-admission conversion for poster-QR leads | 25% (estimate) |
| Logo churn per month | Under 3% |
| Net revenue retention | Over 100% (credits + upgrades) |
| Paying institutes | 150 (base scenario, doc 05) |
