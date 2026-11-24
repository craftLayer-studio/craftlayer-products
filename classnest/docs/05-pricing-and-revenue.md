# 05 Pricing and revenue — ClassNest

Prices exclude 18% GST. USD shown at about ₹83 = $1 and rounded for global listing (estimate conversion).

## Pricing logic

- **Anchor:** Classplus Starter is ₹19,999/year + GST and Grow ₹22,999/year + GST ([Capterra](https://www.capterra.com/p/208852/Class-Plus/reviews/), accessed 2026-11-24). TutorBird is $14.95/month per tutor ([TutorBird](https://www.tutorbird.com/pricing), accessed 2026-11-24).
- **Position:** ClassNest Growth at ₹14,999/year is about 25–35% below Classplus and does more for the offline front desk.
- **Value metric:** active students. It tracks the institute's revenue and our WhatsApp cost.
- **ROI line for sales:** "Recover one ₹1,500 defaulted fee a month and Starter is free."

## Tiers

| | Starter | Growth (recommended) | Pro |
|---|---|---|---|
| Monthly billing | ₹999/mo ($15) | ₹1,799/mo ($24) | ₹3,499/mo ($45) |
| Annual billing (per month) | ₹799/mo = ₹7,999/yr ($12) | ₹1,499/mo = ₹14,999/yr ($19) | ₹2,999/mo = ₹29,999/yr ($39) |
| Active students | Up to 100 | Up to 300 | Up to 1,000 |
| Branches | 1 | 1 | Up to 3 (then ₹999/branch/mo) |
| Staff logins | 3 | 10 | Unlimited |
| QR attendance + absence alerts | Yes | Yes | Yes |
| Fee plans, UPI links, reminders, receipts | Yes | Yes | Yes |
| Enquiry CRM + poster QR demo booking | 1 poster campaign | Unlimited | Unlimited + lead source analytics |
| Tests, marks, report cards | No | Yes | Yes |
| Homework and notes | 2 GB | 10 GB | 50 GB |
| Teacher payouts | No | Yes | Yes |
| UPI AutoPay mandates | No | Yes | Yes |
| Compliance pack | Basic (age check, refund calculator) | Full | Full + state reports |
| WhatsApp utility messages included per month | 1,000 | 2,500 | 8,000 |
| Support | Chat | Chat + onboarding call | Dedicated manager |

Free trial: 14 days, no card. 30-day money-back on annual plans.
Off-season pause plan: ₹199/month keeps data and the enquiry page live (May–June).

## Add-ons

| Add-on | Price | Cost to us | Notes |
|---|---|---|---|
| Extra WhatsApp utility messages | ₹25 per 100 | About ₹13.6 per 100 (₹0.115 + 18% GST) | Meta utility rate from [MyOperator](https://myoperator.com/blog/whatsapp-business-api-pricing-india-2026), accessed 2026-11-24 |
| WhatsApp marketing messages (admission campaigns to opted-in parents) | ₹125 per 100 | About ₹102 per 100 (₹0.8631 + GST) | Same source |
| "Arrived safely" daily alerts | ₹5 per student per month | About ₹3 (22 messages × ₹0.115 + GST) | Opt-in by parent |
| Online MCQ test engine (P2) | ₹499/mo | Hosting only | |
| Extra branch | ₹999/mo | | Pro only |
| Data migration and setup | ₹2,999 one-time | Staff time | Waived on annual plans |
| Printed QR standee + poster kit | ₹499 | About ₹200 | Sold at onboarding |

## Revenue streams

1. Subscriptions (target 80% of revenue).
2. Message credits and alert add-ons (10–15%).
3. Payment partner revenue share on fee volume, if negotiated with the gateway (estimate 0.1–0.3% of GMV; not assumed in base case).
4. Fee financing referrals for annual courses (P2; per-loan commission, not assumed in base case).
5. Setup and print kits (under 5%).

## WhatsApp cost control

A naive design sends one "arrived" message per student per day. For a 300-student centre that is 300 × 22 = 6,600 messages a month, about ₹900 with GST: more than half the Growth price. So:

| Message | Default | Monthly volume, 300 students (estimate) | Cost with GST |
|---|---|---|---|
| Absence alert (assume 10% absent rate) | On | 660 | ₹90 |
| Fee reminders (3 per due) and receipt | On | 1,200 | ₹163 |
| Monthly report card | On | 300 | ₹41 |
| Demo and enquiry follow-ups | On | 300 | ₹41 |
| **Total** | | **2,460** | **₹335** |

This fits the Growth bundle of 2,500 messages. Replies within 24 hours are free service messages under Meta's model ([Meta](https://developers.facebook.com/docs/whatsapp/pricing)).

## Unit economics (estimates)

| Item | Value | Reasoning |
|---|---|---|
| Blended ARPU | ₹1,350/month | Plan mix 35% Starter, 50% Growth, 15% Pro at annual prices, plus ₹150 add-ons |
| Direct costs per account | ₹500/month | WhatsApp ₹300, hosting and storage ₹80, payment and SMS overhead ₹40, support ₹80 |
| Gross margin | About 63% | (1,350 − 500) / 1,350 |
| CAC, founder-led and referral | ₹3,000–4,000 | Walk-in demos in one city, flyers, partner commissions |
| CAC, paid field sales | ₹6,000–7,000 | One rep at ₹25,000 salary + ₹8,000 travel closing 6 per month, plus ₹1,500 marketing per deal |
| Payback (gross-margin basis) | 4–8 months | CAC / (₹1,350 × 63% = ₹850) |
| Cash payback on annual prepay | Immediate | ₹14,999 collected upfront covers CAC |
| Monthly logo churn | 3% | Target; seasonal pauses not counted |
| Lifetime | About 33 months | 1 / 3% |
| LTV (gross margin) | About ₹28,000 | ₹850 × 33 |
| LTV/CAC | 4–9× | |

Targets: keep CAC under ₹5,000 and push annual plans to over 50% of new sales.

## 12-month scenarios (estimates)

New paying institutes per month, starting at launch.

| Month | Conservative | Base | Aggressive |
|---|---|---|---|
| 1–3 | 4/month | 8/month | 15/month |
| 4–6 (admission season Mar–Jun if launched in Jan) | 6/month | 15/month | 30/month |
| 7–12 | 6/month | 15/month | 30/month |
| Paying institutes at month 12 (after 3% churn) | About 65 | About 150 | About 290 |
| MRR at month 12 (₹1,350 ARPU) | ₹0.9 lakh | ₹2.0 lakh | ₹3.9 lakh |
| ARR run-rate | ₹10.5 lakh | ₹24 lakh | ₹47 lakh |
| Team | Founder + 1 engineer | Founder + 2 engineers + 1 sales | Founder + 3 engineers + 3 sales |

## Upsell paths

1. Starter to Growth: triggered at 90 students or when the owner asks for report cards. In-app nudge after the first test season.
2. Growth to Pro: second branch, more than 300 students, or a need for teacher-level permissions.
3. Add-ons: "arrived safely" alerts sold to parents through the institute (parent-funded upsell), admission marketing credits in February–April.
4. Cross-sell within CraftLayer: dance and martial-arts academies to RepVault-style memberships; hostels near coaching hubs to NestKeep.
