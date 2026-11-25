# CraftLayer portfolio strategy

**Goal:** reach Rs 10 lakh MRR (about $11.5k) as fast as possible with one shared platform sold into many offline business verticals in India.

## 1. The thesis

Offline small businesses in India already pay for software (Petpooja, Vyapar and Classplus each have large paying bases). What they still lack is a cheap, simple way to **turn walk-in customers into repeat customers**. A QR code in the shop, phone capture with consent, and WhatsApp follow-up do exactly that. The same loop works in a restaurant, gym, salon, garage or PG, so one platform ([core](https://github.com/craftLayer-studio/craftlayer-core/blob/main/README.md)) can serve 11 verticals.

## 2. Portfolio at a glance

Prices are per outlet per month, excluding GST, from each product's `docs/05-pricing-and-revenue.md`.

| Product | Vertical | Tagline | Main plan | Price range | Top competitors |
|---|---|---|---|---|---|
| [DineLoop](https://github.com/craftLayer-studio/dineloop/blob/main/README.md) | Restaurants, cafes, bars, cloud kitchens | Every table becomes a till, a waiter and a marketing channel. | Growth Rs 2,499 | Rs 999 to 4,999 + Rs 4,999 setup | Petpooja, DotPe, Thrive |
| [RepVault](https://github.com/craftLayer-studio/repvault/blob/main/README.md) | Gyms, yoga and fitness studios | Scan in, show up, renew on time. | Growth Rs 1,999 | Rs 999 to 3,499 | FitnessForce, Wellyx, Gymdesk |
| [TurfTime](https://github.com/craftLayer-studio/turftime/blob/main/README.md) | Turfs, box cricket, courts, gaming cafes | Your own booking app, zero commission. | Growth Rs 2,999 | Rs 0 + Rs 19/booking to Rs 5,499 | Playo, Hudle, KheloMore |
| [GlowDesk](https://github.com/craftLayer-studio/glowdesk/blob/main/README.md) | Salons, spas, barbershops | Fill every chair, bring every client back. | Growth Rs 1,499 | Free to Rs 2,999 | DINGG, Invoay, Fresha |
| [CareQueue](https://github.com/craftLayer-studio/carequeue/blob/main/README.md) | Clinics, dental, physio, labs, vets | Wait from anywhere. Your token comes to your phone. | Clinic Rs 1,499 | Rs 699 to 2,999 | Practo Ray, Healthray, eSushrut@Clinic |
| [StayBell](https://github.com/craftLayer-studio/staybell/blob/main/README.md) | Small hotels, homestays, guest houses | Every room rings you directly. | Direct Rs 2,499 | Rs 999 to 4,999 | eZee Absolute, Djubo, Desktell |
| [NestKeep](https://github.com/craftLayer-studio/nestkeep/blob/main/README.md) | PGs, hostels, co-living | Full beds, rent on time, zero chasing. | Rs 20 to 35 per bed | min Rs 499 | RentOk, Stayqa, Room Rover |
| [ShelfMate](https://github.com/craftLayer-studio/shelfmate/blob/main/README.md) | Kirana, general stores, pharmacies | Your shop on every customer's WhatsApp. | Dukaan Pro Rs 699 | Free to Rs 999 | Khatabook/OkCredit, Vyapar, myBillBook |
| [WashTrack](https://github.com/craftLayer-studio/washtrack/blob/main/README.md) | Laundry, dry cleaners | Every garment tagged, every customer updated. | Growth Rs 1,299 | Rs 599 to 2,999 | QDC, Fabklean, Laundry Grow |
| [ClassNest](https://github.com/craftLayer-studio/classnest/blob/main/README.md) | Coaching, tuition, academies | Every student marked, every parent informed, every fee collected. | Growth Rs 1,799 | Rs 999 to 3,499 | Classplus, Teachmint, Edmingle |
| [GaragePilot](https://github.com/craftLayer-studio/garagepilot/blob/main/README.md) | Car/bike garages, car wash, detailing | Digital job cards, WhatsApp approvals, service reminders. | Workshop Rs 2,399 | Rs 1,199 to 4,499 | GaragePlug, Autorox, Tekmetric |

## 3. Which to build first

Scores are 1 (worst) to 5 (best) and are **estimates** from the research in each product folder, to be replaced with pilot data.

| Product | Pain intensity | Willingness to pay | Reuse of core | Competition (5 = weak) | Sales cycle (5 = fast) | Total |
|---|---|---|---|---|---|---|
| DineLoop | 5 | 4 | 5 | 2 | 4 | **20** |
| GlowDesk | 4 | 3 | 5 | 3 | 5 | **20** |
| RepVault | 5 | 4 | 4 | 3 | 4 | **20** |
| ClassNest | 5 | 4 | 3 | 2 | 3 | 17 |
| TurfTime | 4 | 4 | 4 | 2 | 4 | 18 |
| GaragePilot | 4 | 4 | 3 | 4 | 3 | 18 |
| NestKeep | 5 | 3 | 3 | 3 | 4 | 18 |
| WashTrack | 4 | 3 | 4 | 4 | 4 | 19 |
| StayBell | 4 | 4 | 3 | 2 | 3 | 16 |
| ShelfMate | 4 | 2 | 4 | 1 | 4 | 15 |
| CareQueue | 4 | 3 | 3 | 2 | 3 | 15 |

**Recommended sequence**

1. **DineLoop first (weeks 1 to 8).** It is the founder's original idea, a working ordering prototype already exists ([craftLayer-studio/tabletap](https://github.com/craftLayer-studio/tabletap), about 60% of the ordering scope per the DineLoop docs), and it forces us to build the most reusable Core modules (QR, storefront, orders, payments, CRM, WhatsApp, games).
2. **GlowDesk and RepVault next (weeks 9 to 16).** Both add the bookings engine and recurring billing to Core. Salons are the fastest sale (single decision-maker, low price). Gyms have the clearest ROI story: 45% of new members quit within 90 days, and renewals pay for the product.
3. **WashTrack, TurfTime, GaragePilot (months 5 to 7).** Weaker or fragmented competition; each is mostly configuration on top of Core.
4. **ClassNest, NestKeep (months 7 to 9).** Strong pain (fee and rent collection) but extra compliance (children's data, KYC).
5. **StayBell, ShelfMate, CareQueue (later, or only on demand).** Crowded or price-floored markets: free khata apps for kiranas, a Rs 299 government clinic product, entrenched hotel PMSs.

## 4. Path to Rs 10 lakh MRR (estimate)

| Milestone | Paying outlets | Blended ARPU | MRR |
|---|---|---|---|
| Month 3 | 30 (DineLoop) | Rs 2,000 | Rs 60k |
| Month 6 | 150 (3 verticals) | Rs 1,900 | Rs 2.9 lakh |
| Month 12 | 550 (6 verticals) | Rs 1,850 | Rs 10.2 lakh |

Plus one-time setup fees, QR kit and hardware margins, and WhatsApp credit margins.

## 5. Revenue streams shared by every product

1. Monthly or annual subscription (push annual: 2 months free, cash upfront).
2. One-time setup and onboarding fee (menu/catalog import, QR kit, staff training).
3. WhatsApp marketing credits resold at a margin over Meta's rate (about Rs 0.86 marketing, Rs 0.115 utility).
4. Hardware resale: QR stands, thermal printers, tablets for KDS/reception.
5. Payment processing partnership revenue (gateway referral programmes).
6. Later: multi-outlet chain plans, white-label for franchise brands, local ads/marketplace.

## 6. Go-to-market playbook (shared)

1. **Pick one city cluster.** Sell door to door in one neighbourhood until 10 paying outlets per vertical. Physical proximity produces referrals.
2. **Free 14-day pilot with setup done for them.** We import the menu or catalog, print QR codes and train staff in one visit.
3. **Prove ROI in rupees.** Day-30 report on WhatsApp: customers captured, repeat visits, campaign revenue, commission saved.
4. **Referral reward.** One month free for each referred paying outlet.
5. **Local field partners.** Commission-only resellers (printer and POS vendors, CA firms, gym-equipment dealers) at 20% recurring for 12 months.
6. **Content.** Short videos of real outlets ("this cafe got 400 repeat customers in 60 days") on Instagram and YouTube Shorts.

## 7. Portfolio-level risks

| Risk | Mitigation |
|---|---|
| Spreading too thin across 11 verticals | Strict sequence above; a vertical launches only when the previous one has 20+ paying outlets |
| WhatsApp cost increases (Meta raised India marketing rates in 2026 and started charging some service messages) | Message allowances in plans, credits beyond that, SMS/RCS fallback |
| DPDP compliance (main obligations around May 2027) | Consent built into Core from day one ([core/docs/compliance.md](https://github.com/craftLayer-studio/craftlayer-core/blob/main/docs/compliance.md)) |
| Large incumbents add QR + CRM features | Speed, price, done-for-you onboarding, vernacular support, multi-vertical cross-sell |
| Name conflicts | Each product's AGENTS.md lists conflicts found and backup names; run an IP India trademark search before spending on branding |
