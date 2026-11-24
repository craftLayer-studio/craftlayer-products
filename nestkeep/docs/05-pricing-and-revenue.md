# NestKeep — pricing and revenue

USD figures use ₹88 per USD **(estimate)**. Competitor anchors are in [04-market-research.md](04-market-research.md) (accessed 2026-11-24).

## Pricing logic

| Anchor | Price | Read |
|---|---|---|
| Room Rover | ₹35 per bed (1–50 beds) to ₹26 per bed (200+) | Per-bed pricing is the market norm |
| Kipinn | ₹30 per bed | Same band |
| Stayqa | Free, ₹999, ₹2,499 per month flat | Flat tiers for owners who dislike per-bed math |
| TrackMyPG | ₹299–₹599 per month | Floor for tiny PGs (not our ICP) |
| RentOk | Free essentials, paid premium on quote | Free tier sets expectation that basic rent tracking is cheap |
| Value created for a 50-bed PG | About ₹15,000–₹20,000 per month (food, vacancy, electricity, time) **(estimate, see table below)** | Price should stay under 15% of value |

Rule: the Rent plan undercuts per-bed rivals at ₹20 to win the switch; Pro sits at the top of the market band (₹35) because it adds food opt-out, verification and lead page that rivals charge extra for or lack.

## Plans

| | Rent | Pro (recommended) | Operator |
|---|---|---|---|
| INR per bed per month (monthly billing) | ₹20 | ₹35 | ₹30 (annual only) |
| Monthly minimum | ₹499 | ₹1,199 | ₹9,000 (300 beds) |
| Annual billing | 2 months free | 2 months free | Included in price |
| USD per bed | $0.23 | $0.40 | $0.34 |
| Billable beds | All configured beds (not only occupied) | Same | Same |
| Bed board, rent ledger, invoices, receipts | Yes | Yes | Yes |
| UPI links and Autopay to owner's account | Yes | Yes | Yes |
| Auto reminders and late fees | Yes | Yes | Yes |
| Room QR: complaints and maintenance tickets | Yes | Yes | Yes |
| Tenant onboarding form and KYC vault | Basic (upload only) | Yes, with consent records | Yes |
| Police-verification packet and tracker | — | Yes | Yes |
| Food menu and meal opt-out | — | Yes | Yes |
| Electricity sub-meter billing | — | Yes | Yes |
| Visitor log by QR | — | Yes | Yes |
| Notice and deposit settlement | Notice only | Yes | Yes |
| Vacancy lead page and inbox | — | Yes | Yes, per property |
| Multi-property, manager roles | 1 property | Up to 3 properties | Unlimited |
| Accounting export, expense tracking (P2) | — | — | Yes |
| WhatsApp utility messages included | 5 per bed per month | 8 per bed per month | 10 per bed per month |
| Support | WhatsApp, business hours | WhatsApp, 7 days | Named manager |

## Add-ons

| Add-on | Price | Note |
|---|---|---|
| Onboarding and data import (Excel or notebook to NestKeep) | ₹1,999 one-time; free on annual | Ops time about 2–3 hours **(estimate)** |
| QR kit (room and common-area acrylic standees, visitor-gate QR) | Included up to 20 QRs; ₹79 per extra | Print cost about ₹60 **(estimate)** |
| Digital ID verification (DigiLocker, P2) | ₹15 per resident | Provider cost dependent **(estimate)** |
| Rent agreement with e-sign (P1) | ₹99 per agreement plus state stamp duty pass-through | e-sign provider cost about ₹30–₹50 **(estimate)** |
| Extra WhatsApp messages | Meta rate plus 20% (utility about ₹0.115 before GST, per [MyOperator](https://myoperator.com/blog/whatsapp-business-api-pricing-india-2026)) | |
| Vacancy boost (sponsored listing management on NoBroker / Housing, P2) | ₹999 per month | Service add-on |
| Smart meter hardware (P2, partner) | Partner price; NestKeep earns 10% referral **(estimate)** | |

## Revenue streams

| Stream | Phase | Share of revenue at month 12 **(estimate)** |
|---|---|---|
| Per-bed subscriptions | P0 | 82% |
| Onboarding fees and QR kits | P0 | 6% |
| WhatsApp margin | P0 | 3% |
| Agreements and verification fees | P1 | 5% |
| Vacancy boost and partner referrals (meters, deposit insurance) | P2 | 4% |

Not in plan: a cut of rent collected. Owners see rent as their money; a percentage fee would block adoption. Residents may pay card convenience fees set by the payment gateway.

## Unit economics (estimate)

| Metric | Value | Reasoning |
|---|---|---|
| Average beds per customer | 55 for Rent and Pro; 350 for Operator | ICP 30–150 beds |
| Plan mix | 40% Rent, 55% Pro, 5% Operator | Pro pushed in demo through food and verification |
| Blended subscription ARPU | About ₹2,025 per month | 0.40 × ₹1,100 + 0.55 × ₹1,925 + 0.05 × ₹10,500 |
| ARPU with add-ons | About ₹2,200 per month | Agreements, extra QR, WhatsApp margin |
| COGS per customer | About ₹420 per month | Hosting ₹100, WhatsApp utility about ₹45 (330 messages), support ₹250, storage ₹25 |
| Gross margin | About 81% | |
| CAC (field) | About ₹4,500 | Rep ₹30,000 per month closes 8 PGs per month in a dense cluster, plus ₹750 onboarding labour |
| CAC (owner referral) | About ₹2,700 | One free month of Pro plus onboarding |
| Blended CAC (60% field, 40% referral and inbound) | About ₹3,800 | |
| Contribution per customer per month | About ₹1,780 | |
| Payback | About 2.1 months | ₹3,800 ÷ ₹1,780 |
| Monthly logo churn target | 3.5% | |
| Lifetime | About 29 months | |
| LTV (gross margin) | About ₹51,000 | |
| LTV ÷ CAC | About 13x blended, 11x field-only | |

## Value proof for the owner (sales table)

| PG profile | Plan and monthly price | Food saving | Faster fill of vacancies | Electricity recovered | Total value | ROI |
|---|---|---|---|---|---|---|
| 30 beds, ₹7,000 rent, food included | Pro, ₹1,199 (minimum) | About ₹6,100 | About ₹2,300 (1 bed filled 10 days sooner) | About ₹3,000 | About ₹11,400 | 9.5x |
| 80 beds, ₹9,000 rent, food included | Pro, ₹2,800 | About ₹16,200 | About ₹6,000 (2 beds) | About ₹6,000 | About ₹28,200 | 10x |
| 300 beds across 4 properties, no food, ₹12,000 rent | Operator, ₹9,000 | — | About ₹24,000 (6 beds 10 days sooner at ₹4,000) | About ₹20,000 | About ₹44,000 plus manager time | 4.9x |

**(estimate)**: food saving = beds × 2 meals × 30 days × ₹45 raw cost × 15% waste × 50% reduction. Vacancy and electricity values are illustrative and must be replaced with pilot data. Late-rent benefit (cash flow and owner time) is excluded.

## 12-month scenarios (estimate)

Assumptions: paid plans from month 3 after pilots; 1 field rep in one city from month 3, second city rep from month 6; 3.5% monthly churn.

| Month | Conservative paying properties | Base | Aggressive |
|---|---|---|---|
| 3 | 6 | 10 | 15 |
| 6 | 20 | 45 | 80 |
| 9 | 35 | 85 | 160 |
| 12 | 50 | 120 | 250 |

| Month 12 | Conservative | Base | Aggressive |
|---|---|---|---|
| Paid beds (about 70 average incl. operators) | 3,500 | 8,400 | 17,500 |
| MRR (ARPU ₹2,200) | ₹1,10,000 | ₹2,64,000 | ₹5,50,000 |
| ARR run-rate | ₹13.2 lakh | ₹31.7 lakh | ₹66 lakh |
| One-time onboarding revenue in year 1 | ₹60,000 | ₹1,40,000 | ₹3,00,000 |
| Sales cost in year 1 | ₹3.0 lakh | ₹4.5 lakh | ₹7.5 lakh |

## Upsell paths

| From | To | Trigger | Pitch |
|---|---|---|---|
| Rent | Pro | Food-included PG, or inspection notice, or a vacancy lasting 2+ weeks | "Your kitchen cooks for everyone. Let residents opt out and save about ₹X a month." |
| Pro | Operator | Fourth property or 300+ beds | "One dashboard, managers per building, one invoice." |
| Any | Annual | Month 3 on monthly | "Pay for 10 months, get 12, free onboarding." |
| Any | Agreements add-on | New move-ins | "Signed agreement with late-fee clause before move-in." |
| Any | Vacancy boost | Vacancy above 10% for 30 days | "We manage your listings and leads for ₹999." |
