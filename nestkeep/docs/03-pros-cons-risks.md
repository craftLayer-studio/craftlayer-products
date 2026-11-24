# NestKeep — pros, cons, risks and kill criteria

## Pros

| Pro | Why it matters |
|---|---|
| Monthly, recurring pain | Rent is due every month; the product is used every month |
| Dense clusters | Hundreds of PGs within a few km in Bengaluru (Marathahalli, BTM, HSR), Hyderabad (Madhapur, Ameerpet), Kota, Delhi North Campus; one rep covers many |
| High switching cost once live | Resident ledger, Autopay mandates and history live in NestKeep |
| Clear ROI | Food and late-rent savings are visible in 1–2 months |
| Regulation tailwind | City licensing and verification drives (Bengaluru, Delhi draft) push owners to keep records |
| Reuses CraftLayer core | QR, payments, WhatsApp, CRM, staff app already built |

## Cons

| Con | Impact |
|---|---|
| Crowded low-price category | Many PG apps at ₹299–₹999 per month or ₹26–₹35 per bed; price pressure |
| Owners are cash-comfortable | Some residents and owners prefer cash; Autopay adoption slow |
| Low ARPU per small PG | A 30-bed PG on Rent plan pays ₹600 per month |
| Residents churn often | Students leave in May–June; bed counts fluctuate |
| Fragmented state rules | Verification formats, licence rules and electricity rules vary by state |

## Risks and mitigations

| Risk | Likelihood | Impact | Mitigation |
|---|---|---|---|
| RentOk or a funded competitor gives the same features free | High | High | Differentiate on QR food opt-out, verification packet, lead page; field onboarding in 48 hours; per-bed price owners understand |
| Residents refuse Autopay | High | Medium | Payment links plus reminders still work; small rent discount (owner-funded) for Autopay |
| Autopay above ₹15,000 needs extra authentication each debit (RBI e-mandate framework) | Medium | Medium | Fall back to link with one-tap UPI; most PG beds are under ₹15,000 **(estimate)** |
| Payment provider risk flags rent collection | Low | High | Owner is the merchant of record; KYC each owner; no pooled funds |
| Data breach of ID documents | Low | Very high | Encryption, masked Aadhaar, role access, audit log, deletion after exit, DPDP breach process |
| Late fees disputed as unfair | Medium | Medium | Fee only if in signed agreement; caps configurable; owner waiver; log of reminders sent |
| Electricity resale rules | Medium | Medium | Default to actual per-unit cost; show utility bill rate; state-specific review |
| City crackdowns close unlicensed customers | Medium | Medium | Offer licence document storage and checklist; sell to compliant operators first |
| Seasonality in student towns | High | Medium | Annual plans; bill on minimum, not on occupied beds only |
| WhatsApp quality rating drops from reminder volume | Medium | Medium | Utility templates only, frequency caps, opt-out handling |

## Kill criteria

| Checkpoint | Kill or pivot if |
|---|---|
| Week 8 (pilot end) | Fewer than 3 of 5 pilot PGs agree to pay at least ₹20 per bed |
| Week 8 | Rent collected by due date + 5 does not improve by at least 10 percentage points in pilots |
| Month 4 | Fewer than 20 paying properties or fewer than 1,500 paid beds, or CAC above ₹8,000 |
| Month 6 | Monthly logo churn above 6% for two consecutive months |
| Month 6 | Under 20% of residents on Autopay or links (owners still collecting mostly cash) |
| Month 9 | MRR under ₹1,50,000 with no channel producing more than 30% of new logos |

Pivot options: (a) sell to co-living operators only (higher ARPU, fewer logos); (b) narrow to student hostels with a parent-facing safety product; (c) become the white-label resident app for a larger operator.
