# CraftLayer Core: compliance checklist (India)

This is a product checklist, not legal advice. Get a lawyer to review consent notices and terms before launch.

## 1. Digital Personal Data Protection (DPDP) Act 2023 and DPDP Rules 2025

The DPDP Rules were notified on 13–14 November 2025 and take effect in phases. The provision on consent managers (Rule 4) takes effect about one year after notification, around November 2026. Most remaining obligations, including breach reporting and retention, take effect after 18 months, around May 2027. Build for full compliance from day one, because retrofitting consent onto an existing customer database is expensive.

**Roles:** the business owner (our customer) is usually the **Data Fiduciary**. CraftLayer is the **Data Processor**. Our contracts must say this. Our product must make it easy for the owner to comply.

| Requirement | How Core implements it |
|---|---|
| Notice before collection, in clear language (English + 22 scheduled languages on request) | Consent screen on every QR flow: what is collected, why, how to withdraw. Versioned notices. |
| Free, specific, informed, unambiguous consent | Separate, unticked checkboxes: (a) order/booking updates, (b) offers and marketing. Never bundle marketing consent with ordering. |
| Easy withdrawal | "STOP" on WhatsApp, an unsubscribe link and a dashboard toggle; withdrawal syncs across channels within minutes. |
| Purpose limitation and erasure | Retention jobs delete or anonymise inactive customers after a configurable period; erase on request. |
| Children's data (under 18) | Verifiable parental consent; no behavioural tracking or targeted ads. Critical for **ClassNest**, relevant to TurfTime and RepVault. |
| Security safeguards and breach notice | Encryption, access logs, incident runbook; notify the Board and affected people when the rules require it. |
| Consent records | `consent_record` table with notice version, timestamp and channel. Exportable as an audit trail. |

Sources (accessed 2026-11-24): [PIB DPDP Rules 2025 PDF](https://static.pib.gov.in/WriteReadData/specificdocs/documents/2025/nov/doc20251117695301.pdf), [AZB & Partners update](https://www.azbpartners.com/bank/update-indias-digital-personal-data-protection-framework-comes-into-effect/), [SCC Online highlights](https://www.scconline.com/blog/post/2025/12/26/digital-personal-data-protection-rules-2025-key-highlights/), [Bar & Bench](https://www.barandbench.com/news/centre-notifies-digital-personal-data-protection-rules-2025-how-different-are-they-from-the-draft-rules).

## 2. WhatsApp Business Platform policy

- Marketing messages need prior opt-in for WhatsApp specifically. Store proof of that opt-in.
- Use approved templates. Keep marketing frequency low (Meta rate-limits poor-quality senders and blocks some marketing to users who disengage).
- Honour opt-outs immediately.
- Per-message pricing: see [core/README.md](../README.md#messaging-costs-to-budget-for-india).

## 3. Games, contests and rewards

- Games must be free to play and must not require payment to enter. Prizes are discounts or freebies redeemable at the business. This keeps them as promotional schemes rather than gambling or lotteries under state laws.
- Publish simple terms: who can play, prize limits, expiry, and that the business may change offers.
- Rate limit: one play per order/visit per phone.

## 4. GST and invoicing

- GST invoices with GSTIN, HSN/SAC and tax breakup. Restaurant services are mostly 5% without ITC. Other verticals vary: salons, gyms and clinics have their own rates or exemptions, so per-vertical docs specify them.
- E-invoicing (IRN) applies only above the turnover threshold. Most of our customers are below it, but support export for those above.
- CraftLayer's own subscription invoices carry 18% GST.

## 5. Payments

- Use RBI-authorised payment aggregators (Razorpay, Cashfree). Never hold customer funds ourselves.
- UPI Autopay mandates for recurring subscriptions (RepVault, NestKeep, ClassNest, WashTrack plans).

## 6. Vertical-specific regulation

Each product's `docs/04-market-research.md` lists its own rules, for example FSSAI (DineLoop), Form C and guest registers (StayBell), Telemedicine Practice Guidelines and ABDM (CareQueue), the 2024 coaching-centre guidelines (ClassNest), and drug-licence rules (ShelfMate pharmacies).
