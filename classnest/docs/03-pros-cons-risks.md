# 03 Pros, cons, risks — ClassNest

## Pros

| Pro | Why it matters |
|---|---|
| Clear money pain (fee defaulters) | Owners understand ROI in one sentence; short sales cycles |
| Large, fragmented market | About 27% of Indian students take private coaching ([CMS:Education 2025 via Careers360](https://news.careers360.com/27-of-students-rely-on-private-coaching-urban-participation-higher-cms-education-survey-2025), accessed 2026-11-24) |
| Daily habit | Attendance happens every day, so the product is opened every day |
| Viral surfaces | Report cards and demo pages are seen by parents, who also know other centre owners |
| Shared core | QR, payments, CRM and WhatsApp are reused from CraftLayer core; MVP is mostly vertical logic |
| Seasonality creates urgency | Admission season (March–June) gives a natural deadline to buy |

## Cons

| Con | Impact |
|---|---|
| Crowded category: Classplus, Teachmint, Edmingle, Fedena and many local vendors | Need a sharp offline-first positioning and lower price |
| Price-sensitive buyers; many already use free tools (Teachmint free tier, Classplus Lite) | Must win on fee recovery ROI, not on feature lists |
| WhatsApp cost scales with students, not with our price | Margin risk if alerts are not controlled (see doc 05) |
| Seasonal churn: some centres pause in May–June or after exams | Annual billing and an off-season plan needed |
| Children's data raises compliance cost | Consent flows, retention rules, audit logs |

## Risks and mitigations

| Risk | Likelihood | Impact | Mitigation |
|---|---|---|---|
| DPDP Rules 2025 children's-data obligations (Rule 10 verifiable parental consent) become fully enforceable around May 2027, 18 months after notification | High | High | Build VPC and consent ledger in MVP; no tracking, profiling or ads to children; data deletion after course end + retention window; legal review before launch |
| Coaching centres turn out not to be covered by the "educational institution" exemption | Medium | Medium | Assume no exemption; collect VPC for every under-18 student |
| State coaching laws based on the 2024 Ministry of Education guidelines restrict under-16 enrolment for covered centres | Medium | Medium | Target Class 11–12, competitive-exam and skill academies first; add age check and compliance pack; tuition centres below the guideline threshold remain addressable (verify threshold per state) |
| WhatsApp price increases (marketing went up about 10% in 2026) | High | Medium | Default to utility templates; bundle credits; pass through excess with markup |
| Free competitors (Teachmint, Classplus Lite) undercut | High | Medium | Sell fee recovery and parent alerts, which free tiers do not do well offline; 30-day money-back guarantee |
| Payment gateway or UPI AutoPay limits block quarterly fee auto-debit | Medium | Low | Use payment links for large instalments; AutoPay only for monthly fees within limits |
| Owner does not get staff to use the app | Medium | High | Teacher app with one-tap attendance; onboarding visit; activation SLA |
| Data breach of minors' data | Low | Very high | Encryption, role-based access, breach playbook with DPB notification, minimal data fields |
| Seasonal churn after exam season | High | Medium | Annual plans at 2 months free; "pause" plan at ₹199/month keeps data |

## Kill criteria

Review at the end of month 6 after launch. Stop or pivot ClassNest if two or more of these are true:

| Criterion | Threshold |
|---|---|
| Paying institutes | Fewer than 40 |
| Trial-to-paid conversion | Below 15% |
| Monthly logo churn (excluding seasonal pauses) | Above 6% |
| Blended CAC payback | Over 9 months |
| Share of fee volume collected via ClassNest in active accounts | Below 30% (signals the core value is not landing) |
| WhatsApp cost as % of subscription revenue | Above 35% after tuning |

Pivot options if killed: sell only the enquiry CRM + demo booking for admission season; or fold attendance and fees into a white-label module for CraftLayer's RepVault (dance/martial-arts studios overlap).
