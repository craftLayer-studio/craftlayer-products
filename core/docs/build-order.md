# CraftLayer Core: build order

Build Core **through the flagship (DineLoop)**, not in the abstract. Every module ships first inside a real restaurant, then gets generalised for the second vertical.

## Phase 0: weeks 1–2 (foundation)

- Tenant/accounts, OTP auth, roles
- QR engine and printable QR kit (PDF)
- Storefront (menu/catalog page) with AI import from a photo/PDF of the menu
- Consent screen and `consent_record`

## Phase 1: weeks 3–6 (sellable DineLoop MVP)

- Orders engine + kitchen display (KDS) + staff app (PWA)
- Payments: UPI intent + Razorpay; "pay at counter" option
- Customer CRM (auto-built from orders)
- WhatsApp utility messages (order confirmed / ready) through a BSP
- Review funnel (private feedback, then Google review link)
- Owner daily summary on WhatsApp

**Exit criterion:** 3 restaurants live and paying.

## Phase 2: weeks 7–10 (retention engine)

- Loyalty (stamps/points), coupons, birthday offers
- WhatsApp marketing campaigns with segments (lapsed 30 days, VIP, birthday this week)
- Games (spin wheel, scratch card) with reward rules and rate limits
- Analytics: repeat rate, campaign ROI

**Exit criterion:** at least 1 campaign that shows measurable repeat revenue, used as a case study.

## Phase 3: weeks 11–14 (second vertical)

- Bookings/slots engine and token queue (needed by TurfTime, GlowDesk, CareQueue, RepVault)
- Recurring billing with UPI Autopay (RepVault, NestKeep, ClassNest)
- Launch the second vertical chosen in [portfolio/STRATEGY.md](../../portfolio/STRATEGY.md)

## Phase 4: continuous

- Vertical layers, one every 3–4 weeks
- Integrations: aggregators, Google Business Profile, Tally, ONDC
- Move from BSP to direct WhatsApp Cloud API once volume justifies it
