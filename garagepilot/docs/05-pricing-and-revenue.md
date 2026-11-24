# 05 Pricing and revenue — GaragePilot

Prices exclude 18% GST. USD at about ₹83 = $1, rounded (estimate conversion).

## Pricing logic

- **Floor anchors (India):** RAMP ₹9,870/year; Vyapar Silver ₹3,419/year; BUSY ₹5,000–₹12,000/year ([Codingclave](https://codingclave.com/guides/best-auto-repair-shop-software-india-2026), accessed 2026-11-24).
- **Ceiling anchors:** GaragePlug reported floor about $1,188/year ([CostBench](https://costbench.com/software/automotive-shop-software/garageplug/)); Autorox $899 per user per year ([Software Advice](https://www.softwareadvice.com/accounting/autorox-profile/)); Tekmetric $179–$439 per month ([Tekmetric](https://tekmetric.com/pricing)). All accessed 2026-11-24.
- **Position:** Bay matches RAMP on price but adds WhatsApp approvals, status and reminders. Workshop is about 20% of GaragePlug's reported floor.
- **Value metric:** job cards per month (tracks garage revenue and our message cost). Unlimited users on every plan so mechanics are never locked out.
- **ROI line:** "Two extra cars a month from reminders pays for the year."

## Tiers

| | Bay | Workshop (recommended) | Pro |
|---|---|---|---|
| Monthly billing | ₹1,199/mo ($15) | ₹2,399/mo ($29) | ₹4,499/mo ($55) |
| Annual billing (per month) | ₹999/mo = ₹9,999/yr ($12) | ₹1,999/mo = ₹19,999/yr ($24) | ₹3,999/mo = ₹39,999/yr ($48) |
| Job cards per month | 150 | 500 | Unlimited |
| Locations | 1 | 1 | Up to 3 (then ₹1,499/location/mo) |
| Users | Unlimited | Unlimited | Unlimited |
| Digital job card, photos, video | Yes (12-month media retention) | Yes (36 months) | Yes (unlimited) |
| QR status + WhatsApp estimate approval | Yes | Yes | Yes |
| GST invoices, UPI links, credit ledger | Yes | Yes | Yes |
| Service-due reminders | Yes | Yes + declined-work follow-ups | Yes + custom campaigns |
| Parts inventory | Basic stock | Full (purchases, suppliers, margins) | Full + stock transfer |
| Mechanic tracking and incentives | Assignment only | Yes | Yes |
| Wash subscriptions and passes | No | Yes | Yes |
| Insurance claim tracker | No | Yes | Yes |
| Tally / GSTR-1 export | No | No | Yes |
| WhatsApp utility messages included per month | 600 | 2,000 | 6,000 |
| Reminder (marketing-rate) messages included per month | 100 | 300 | 1,000 |
| Support | Chat | Chat + onboarding visit | Dedicated manager |

Free trial: 14 days. 30-day money-back on annual plans.

## Add-ons

| Add-on | Price | Cost to us | Notes |
|---|---|---|---|
| Extra utility messages | ₹25 per 100 | About ₹13.6 per 100 | Meta utility about ₹0.115 + GST ([MyOperator](https://myoperator.com/blog/whatsapp-business-api-pricing-india-2026)) |
| Extra reminder/marketing messages | ₹125 per 100 | About ₹102 per 100 | Meta marketing ₹0.8631 + GST, same source |
| Wash subscription billing (Bay plan) | ₹499/mo | | Included in Workshop |
| Number plate OCR + registration lookup | ₹299/mo | Lookup provider fee (estimate ₹0.5–1 per lookup) | P1 |
| Extra location | ₹1,499/mo | | Pro only |
| Printed QR job-card stickers and counter standee | ₹699 kit | About ₹250 | Onboarding |
| Data migration from Vyapar/Excel | ₹2,999 one-time | Staff time | Waived on annual |

## Revenue streams

1. Subscriptions (target 80%).
2. Message credits (10–15%).
3. Parts ordering commission via distributor partner (P2; estimate 2–5% of parts GMV; not in base case).
4. Payment gateway revenue share (if negotiated; not in base case).
5. Insurance and extended-warranty lead referrals to insurers/brokers (P2; regulatory review required before launch).

## Message cost per account (estimate, Workshop garage with 250 job cards/month)

| Message | Volume per month | Category | Cost with GST |
|---|---|---|---|
| Check-in + status link | 250 | Utility | ₹34 |
| Estimate approval | 250 | Utility | ₹34 |
| Ready + invoice | 500 | Utility | ₹68 |
| Service-due and declined-work reminders | 300 | Marketing (assumed) | ₹305 |
| Customer replies within 24 hours | Any | Service (free) | ₹0 |
| **Total** | **1,300** | | **About ₹441** |

## Unit economics (estimates)

| Item | Value | Reasoning |
|---|---|---|
| Blended ARPU | ₹1,900/month | Mix 30% Bay, 55% Workshop, 15% Pro at annual prices + ₹200 add-ons |
| Direct costs | ₹700/month | WhatsApp ₹440, media storage and hosting ₹150, support ₹90, payments overhead ₹20 |
| Gross margin | About 63% | |
| CAC, founder-led and partner | ₹4,000–5,000 | Garage-street visits, parts-dealer referrals |
| CAC, paid field sales | ₹7,000–8,000 | Rep at ₹28,000 + ₹10,000 travel closing 5–6 per month + ₹1,000 marketing |
| Payback (gross-margin basis) | 3.5–7 months | CAC / (₹1,900 × 63% = ₹1,200) |
| Cash payback on annual prepay | Immediate | ₹19,999 upfront |
| Monthly logo churn | 2.5% target | Garages switch less once history is inside |
| Lifetime | About 40 months | |
| LTV (gross margin) | About ₹48,000 | |
| LTV/CAC | 6–12× | |

## 12-month scenarios (estimates)

| | Conservative | Base | Aggressive |
|---|---|---|---|
| New garages per month (months 1–3) | 4 | 8 | 15 |
| New garages per month (months 4–12) | 6 | 15 | 30 |
| Paying garages at month 12 (after 2.5% churn) | About 65 | About 150 | About 295 |
| MRR at month 12 (₹1,900 ARPU) | ₹1.2 lakh | ₹2.9 lakh | ₹5.6 lakh |
| ARR run-rate | ₹15 lakh | ₹34 lakh | ₹67 lakh |
| Team | Founder + 1 engineer | Founder + 2 engineers + 1 sales | Founder + 3 engineers + 3 sales |

## Upsell paths

1. Bay to Workshop: when job cards exceed 150 or the owner wants inventory margins, wash subscriptions or insurance tracking.
2. Workshop to Pro: second outlet, Tally export, or more than 500 job cards.
3. Reminder credit packs before festivals and monsoon ("monsoon check-up" campaigns).
4. Wash and detailing add-on for garages that add a washing bay.
5. Cross-sell within CraftLayer: tyre and accessory shops attached to garages can use ShelfMate for retail counter billing.
