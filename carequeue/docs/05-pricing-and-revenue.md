# CareQueue pricing and revenue

USD equivalents use ₹85 = $1 (estimate). Prices exclude GST (18%, estimate, confirm with CA). Competitor anchors are sourced in [04 market research](04-market-research.md).

## Pricing logic

- Indian clinic software sits at ₹499–₹1,999 per month per user (Practo Ray, Healthray, Eka Care). The government eSushrut@Clinic sets a ₹299 floor for records software.
- CareQueue does not compete as an EMR. It sells patient flow and follow-up revenue. We price flat per clinic so adding a visiting consultant does not raise the bill until Plus.
- The ₹699 Token tier is an easy "yes" to get the QR on the counter; the upgrade comes once the clinic sees follow-ups and e-Rx on WhatsApp.
- No permanent free tier: health data needs secure storage and support. A 30-day trial replaces it.

## Tiers (per clinic)

| | Token | Clinic (default pitch) | Clinic Plus |
|---|---|---|---|
| Monthly | ₹699 ($8.20) | ₹1,499 ($17.60) | ₹2,999 ($35.30) |
| Annual prepaid | ₹6,990 ($82) | ₹14,990 ($176) | ₹29,990 ($353) |
| Practitioners / counters | 1 counter | 2 practitioners | 5 practitioners or lab counters |
| QR token, live wait, WhatsApp turn alerts | Yes | Yes | Yes |
| Staff app (call next, priority, no-show) | Yes | Yes | Yes |
| Patient registration with consent | Basic (name, phone) | Full, family profiles | Full |
| Appointment booking with advance fee | No | Yes | Yes |
| e-Rx with practitioner templates, secure link | No | Yes | Yes |
| Follow-up and session-plan reminders | No | Yes | Yes |
| UPI payments, daily collection summary | Yes | Yes | Yes |
| Google review request | No | Yes | Yes |
| Lab report delivery | No | 100 reports/month | Unlimited |
| TV token display (P1) | No | Yes | Yes |
| ABDM M1/M2 and DHIS claim support (P1) | No | No | Yes |
| Vet module, dental/physio treatment plans (P1) | No | Yes | Yes |
| Analytics (wait time, no-shows, follow-up rate) | Basic | Standard | Full + monthly review |
| Support | WhatsApp, same day | WhatsApp + call | Priority + onsite onboarding |

30-day free trial on all tiers, no card needed.

## Add-ons

| Add-on | Price | Notes |
|---|---|---|
| WhatsApp credits, utility (tokens, reminders, report links) | ₹0.20 per message | Meta ≈ ₹0.11–₹0.12 + BSP; margin ≈ ₹0.05 (estimate) |
| WhatsApp credits, marketing (health camps, practitioner-approved) | ₹1.15 per message | Meta ≈ ₹0.86 |
| Extra practitioner on Clinic Plus | ₹499/month | |
| Lab report pack on Clinic tier | ₹499/month for unlimited | For clinics with in-house collection |
| QR kit (reception standee, 2 wall posters, token sign) | ₹799 one-time, free on annual | Cost ≈ ₹300 (estimate) |
| TV display stick, preconfigured | ₹2,999 one-time | Pass-through hardware + setup |
| Google Business Profile optimisation | ₹1,999 one-time | Hours, photos, booking link |
| ABDM onboarding (HFR, HPR registration help) | ₹1,499 one-time | Free on annual Plus |

## Revenue streams

1. Subscriptions (target 80%+).
2. WhatsApp credits margin (5–8%; mostly utility so small).
3. One-time setup, QR kits, TV display, GBP and ABDM onboarding (5–10%).
4. DHIS share as a Digital Solution Company: 25% of incentives earned by facilities using CareQueue for ABHA-linked records, if CareQueue qualifies (P1–P2, estimate; depends on certification and current DHIS rules).
5. Not pursued: pharma sponsorships, selling data, patient advertising. These conflict with trust and DPDP purpose limitation.

## Typical clinic WhatsApp usage (estimate)

GP clinic, 70 patients/day, 25 days/month = 1,750 visits:

| Message | Count/month | Rate | Cost to clinic |
|---|---|---|---|
| Token confirmation | 1,750 | ₹0.20 | ₹350 |
| Turn alert ("3 ahead", "your turn") — often inside 24 h service window after patient's OTP reply, free (estimate 50%) | 1,750 | ₹0.10 avg | ₹175 |
| e-Rx link | 1,000 | ₹0.20 | ₹200 |
| Follow-up reminders | 400 | ₹0.20 | ₹80 |
| Total | | | ≈ ₹800/month |

GlowDesk-style marketing volume is not expected here. CareQueue margin on credits ≈ ₹150/month (estimate).

## Unit economics (estimate)

| Metric | Value | Reasoning |
|---|---|---|
| Plan mix | 25% Token, 55% Clinic, 20% Plus | Clinic is default pitch; labs and multi-doctor take Plus |
| Subscription ARPU (list) | ₹1,599 | 0.25×699 + 0.55×1,499 + 0.2×2,999 |
| After annual discount on 50% of base | ≈ ₹1,465 | |
| Credits margin + add-ons (monthly average) | ≈ ₹180 | |
| Blended ARPU | **≈ ₹1,645/month** ($19) | |
| Direct cost per clinic | ≈ ₹350/month | encrypted storage and backups ₹100, hosting ₹80, support ₹150, misc ₹20 |
| Gross margin | ≈ 79% | |
| Compliance overhead (fixed) | ≈ ₹1.5 lakh/year | pen test, legal review, DPA templates (estimate); not in per-clinic COGS |
| CAC, founder-led (first 10) | ≈ ₹1,500 | travel + kits |
| CAC, field rep | ≈ ₹6,000 | rep ₹28,000 salary + ₹5,000 travel / 6 closes a month = ₹5,500 + kit ₹300 + ₹200 misc |
| CAC, doctor referral | ≈ ₹1,600 | 1 month free for referrer |
| Blended CAC (month 6+) | ≈ ₹4,500 | 55% field, 35% referral, 10% events/digital |
| CAC payback | **≈ 3.5 months** blended; 4.6 months field-only | CAC / (ARPU × GM) |
| Monthly logo churn target | 3% | clinics more stable than salons (estimate) |
| Lifetime | 33 months | |
| LTV (gross margin) | ≈ ₹42,900 | 1,645 × 0.79 × 33 |
| LTV:CAC | ≈ 9.5 blended; 7.1 field-only | |

## 12-month scenarios (paying clinics and MRR, estimate)

Assumes MVP ready week 8; founder sells months 3–4; first field rep month 5; second rep month 8. Doctor sales cycles are longer than salons (2–3 visits).

| Month | Conservative | Base | Aggressive |
|---|---|---|---|
| 3 | 4 | 8 | 12 |
| 6 | 20 | 40 | 70 |
| 9 | 45 | 100 | 180 |
| 12 | 70 | 170 | 350 |
| MRR at month 12 (× ₹1,645) | ₹1.15 lakh | ₹2.80 lakh | ₹5.76 lakh |
| ARR run-rate at month 12 | ₹14 lakh | ₹34 lakh | ₹69 lakh |
| One-time revenue in year | ₹0.8 lakh | ₹2 lakh | ₹4 lakh |
| Monthly burn at month 12 | ≈ ₹3.8 lakh | ≈ ₹3.8 lakh | ≈ ₹5.5 lakh |

Base case reaches product-level breakeven around month 13–14. Shared core costs with GlowDesk and other CraftLayer products improve this.

## Upsell paths

| From | To | Trigger | Pitch |
|---|---|---|---|
| Trial | Token or Clinic | Day 21: show tokens issued, average wait, calls saved | "Your patients already expect the WhatsApp token." |
| Token | Clinic | Doctor asks for e-Rx on WhatsApp or follow-ups; lost follow-up patients | "Every follow-up you set gets a reminder. 3 extra visits a day pays for a year." |
| Clinic | Clinic Plus | Second/visiting consultant, in-house lab, ABDM interest | "All consultants in one queue, reports on WhatsApp, ABDM incentives." |
| Monthly | Annual | Month 2, after 1,000+ tokens issued | "2 months free + free QR kit and TV setup." |
| Any | TV display | Crowded room, patients ask "which number?" | "Token board on your existing TV." |
| Labs on Plus | Home collection (P2) | Lab already does home visits by phone | "Patients book home collection on WhatsApp." |
