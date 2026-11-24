# CraftLayer Core: the shared platform behind every product

CraftLayer Core is the one codebase and one set of modules that every vertical product (DineLoop, RepVault, GlowDesk and the rest) is built on. Each vertical is a **configuration plus a thin vertical layer** on top of Core, not a separate app built from scratch.

**Why this matters for revenue:** we build each module once and sell it 11 times. A new vertical should take 3 to 4 weeks to launch, not 3 to 4 months.

## The shared wedge

Every CraftLayer product starts from the same loop:

```
QR in the physical business  ->  customer self-serves (order / book / check in / pay)
        ->  phone number captured with consent  ->  CRM profile
        ->  WhatsApp follow-up (offers, reminders, loyalty, review request)
        ->  customer returns  ->  owner sees revenue lift in dashboard  ->  owner renews
```

The owner pays for the **repeat-customer revenue** this loop produces. Every feature should strengthen one step of it.

## Modules

| # | Module | What it does | Used by |
|---|---|---|---|
| 1 | Tenant & accounts | Multi-tenant orgs, outlets/branches, roles (owner, manager, staff), subscriptions & billing | All |
| 2 | QR engine | Generate per-location QR codes (table, room, bay, mirror, entrance); printable kits; scan analytics | All |
| 3 | Storefront | Mobile web page per business: menu / service list / catalog / slots, brand theme, multilingual | All |
| 4 | Orders & bookings engine | Cart, orders, appointments, slots, queue tokens, resource calendars, status pipeline | All |
| 5 | Payments | UPI intent, Razorpay/Cashfree, payment links, UPI Autopay mandates, refunds, settlement reports | All |
| 6 | Billing & GST | GST invoices, HSN/SAC codes, credit notes, thermal and A4 print, e-invoice export | Most |
| 7 | Customer CRM | Unified customer profile, visit/order history, tags, segments (new, regular, lapsed, VIP) | All |
| 8 | Messaging | WhatsApp Cloud API (templates, campaigns, two-way inbox), SMS fallback, opt-in/opt-out registry | All |
| 9 | Loyalty & rewards | Points, stamps, cashback, coupons, referral codes, birthday/anniversary offers | All |
| 10 | Engagement games | Spin-the-wheel, scratch card, quiz, mini arcade; reward rules; fraud limits | DineLoop, GlowDesk, ShelfMate, TurfTime, StayBell |
| 11 | Reviews & feedback | Private feedback first; happy customers routed to Google review; unhappy ones to owner alert | All |
| 12 | Staff app | PWA for staff: order/ticket queue, tasks, attendance, commissions | All |
| 13 | Analytics | Owner dashboard: revenue, repeat rate, campaign ROI, staff performance; daily WhatsApp summary to owner | All |
| 14 | Onboarding wizard | Import menu/catalog from photo/PDF/Excel (AI-assisted), QR kit ordering, first campaign setup | All |
| 15 | Consent & privacy | DPDP-compliant notices, consent logs, data-principal requests (access/erase), retention jobs | All |
| 16 | Integrations hub | Aggregators (Zomato/Swiggy via UrbanPiper-type partners), Google Business Profile, Tally export, ONDC | Per vertical |

## Recommended stack

| Layer | Choice | Reason |
|---|---|---|
| Frontend | Next.js (App Router) + TypeScript + Tailwind, PWA | One codebase for storefront, owner dashboard and staff app; installable on cheap Android phones |
| Backend | Next.js route handlers / Node services, tRPC or REST | Small team speed |
| Database | Postgres (Neon or Supabase), row-level tenant isolation | Relational data, cheap branching for dev |
| Realtime | Postgres LISTEN/NOTIFY, Supabase Realtime or Ably | Live kitchen display, queue boards |
| Messaging | WhatsApp Cloud API direct, or a BSP (Gupshup, AiSensy, Interakt) at first | Direct is cheapest at scale; BSP is fastest to launch |
| Payments | Razorpay (UPI, links, Autopay), Cashfree as backup | Indian standard |
| Printing | ESC/POS thermal printers via local bridge app or Bluetooth | Kitchens, counters, job cards |
| AI | Claude (claude-sonnet-5-5 for menu/catalog extraction, campaign copywriting; claude-haiku-5-5 for high-volume classification) | Faster onboarding, owner-facing copy in Hindi/English/regional |
| Hosting | Vercel + managed Postgres, Cloudflare for QR redirects | Low ops |

## Messaging costs to budget for (India)

Meta has charged per delivered template message since July 2025. Reported India rates (verify on Meta's official rate card before pricing):

| Category | Approx. rate per message | Notes |
|---|---|---|
| Marketing | ~Rs 0.86 | Raised ~10% from ~Rs 0.78 on 1 Jan 2026 |
| Utility (order updates, reminders) | ~Rs 0.115 | Some BSPs report Rs 0.145 |
| Authentication (OTP) | ~Rs 0.115 to 0.145 | |
| Service (replies within 24h window) | Free tier, then charged | Check current rules |

Plus BSP platform fee if any, plus 18% GST. **Pricing rule for all products:** include a monthly message allowance in each plan and sell extra marketing messages as credit packs at a margin (e.g. Rs 1.25 to 1.50 per message).

Sources (accessed 2026-11-24): [Meta pricing docs](https://developers.facebook.com/docs/whatsapp/pricing), [MyOperator India 2026](https://myoperator.com/blog/whatsapp-business-api-pricing-india-2026), [AiSensy Jan 2026 update](https://m.aisensy.com/blog/whatsapp-api-new-pricing/), [TeleCRM breakdown](https://telecrm.in/blog/whatsapp-business-api-pricing/).

## Further docs

- [docs/architecture.md](docs/architecture.md): tenancy, data model, vertical layer pattern
- [docs/compliance.md](docs/compliance.md): DPDP Act 2023 / Rules 2025, WhatsApp policy, GST, payments
- [docs/build-order.md](docs/build-order.md): which modules to build first and why
