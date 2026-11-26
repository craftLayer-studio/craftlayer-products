# CraftLayer Products

Vertical SaaS for India's offline small businesses. Each product puts a **QR code inside the business** so walk-in customers can order, book, check in or pay from their own phone, while the owner builds a **consented customer database** and brings customers back with **WhatsApp offers, loyalty and games**.

Website: **[craftlayer.store](https://craftlayer.store)** · Contact: hello@craftlayer.store · Licensing: licensing@craftlayer.store

One shared platform ([CraftLayer Core](https://github.com/craftLayer-studio/craftlayer-core/blob/main/README.md)) powers 11 vertical products.

Each product and the core platform live in their own repository, included here as git submodules. To get everything in one folder:

```bash
git clone --recurse-submodules https://github.com/craftLayer-studio/craftlayer-products.git
```

| Product | For | Repository | App |
|---|---|---|---|
| **DineLoop** | Restaurants, cafes, bars, cloud kitchens | [dineloop/](https://github.com/craftLayer-studio/dineloop/blob/main/README.md) | [dineloop.craftlayer.store](https://dineloop.craftlayer.store) |
| **RepVault** | Gyms, yoga and fitness studios | [repvault/](https://github.com/craftLayer-studio/repvault/blob/main/README.md) | [repvault.craftlayer.store](https://repvault.craftlayer.store) |
| **TurfTime** | Sports turfs, box cricket, courts, gaming cafes | [turftime/](https://github.com/craftLayer-studio/turftime/blob/main/README.md) | [turftime.craftlayer.store](https://turftime.craftlayer.store) |
| **GlowDesk** | Salons, spas, barbershops | [glowdesk/](https://github.com/craftLayer-studio/glowdesk/blob/main/README.md) | [glowdesk.craftlayer.store](https://glowdesk.craftlayer.store) |
| **CareQueue** | Clinics, dental, physio, labs, vets | [carequeue/](https://github.com/craftLayer-studio/carequeue/blob/main/README.md) | [carequeue.craftlayer.store](https://carequeue.craftlayer.store) |
| **StayBell** | Small hotels, homestays, guest houses | [staybell/](https://github.com/craftLayer-studio/staybell/blob/main/README.md) | [staybell.craftlayer.store](https://staybell.craftlayer.store) |
| **NestKeep** | PGs, hostels, co-living | [nestkeep/](https://github.com/craftLayer-studio/nestkeep/blob/main/README.md) | [nestkeep.craftlayer.store](https://nestkeep.craftlayer.store) |
| **ShelfMate** | Kirana, general stores, pharmacies | [shelfmate/](https://github.com/craftLayer-studio/shelfmate/blob/main/README.md) | [shelfmate.craftlayer.store](https://shelfmate.craftlayer.store) |
| **WashTrack** | Laundry and dry cleaners | [washtrack/](https://github.com/craftLayer-studio/washtrack/blob/main/README.md) | [washtrack.craftlayer.store](https://washtrack.craftlayer.store) |
| **ClassNest** | Coaching, tuition, skill academies | [classnest/](https://github.com/craftLayer-studio/classnest/blob/main/README.md) | [classnest.craftlayer.store](https://classnest.craftlayer.store) |
| **GaragePilot** | Car/bike garages, car wash, detailing | [garagepilot/](https://github.com/craftLayer-studio/garagepilot/blob/main/README.md) | [garagepilot.craftlayer.store](https://garagepilot.craftlayer.store) |

## Start here

- [portfolio/STRATEGY.md](portfolio/STRATEGY.md): which products to build first, pricing overview, path to Rs 10 lakh MRR
- [core/README.md](https://github.com/craftLayer-studio/craftlayer-core/blob/main/README.md): shared modules, stack, WhatsApp cost model
- [core/docs/compliance.md](https://github.com/craftLayer-studio/craftlayer-core/blob/main/docs/compliance.md): DPDP Act 2023 / Rules 2025, WhatsApp policy, GST
- [CONVENTIONS.md](CONVENTIONS.md): how every product folder is organised
- [AGENTS.md](AGENTS.md): instructions for AI agents working in this repo

## What is in each product folder

| File | Contents |
|---|---|
| `README.md` | One-page summary |
| `AGENTS.md` | Brief for AI agents: context, glossary, decisions, open questions |
| `docs/01-product-plan.md` | Vision, personas, journeys, prioritised features (P0/P1/P2), data model, metrics |
| `docs/02-problems-and-benefits.md` | Problems solved and benefits for owner, staff and customers |
| `docs/03-pros-cons-risks.md` | Pros, cons, risks, mitigations, kill criteria |
| `docs/04-market-research.md` | Market size, competitors and pricing, trends, regulation, sources |
| `docs/05-pricing-and-revenue.md` | Plans, add-ons, unit economics, revenue scenarios |
| `docs/06-go-to-market-and-onboarding.md` | Sales channels, scripts, onboarding checklist, retention |

## Related repositories

- [craftLayer-studio/tabletap](https://github.com/craftLayer-studio/tabletap): DineLoop's application code: QR ordering, kitchen display, CRM, loyalty, games and campaigns.

## Status

November 2026: every product has a working MVP in its repository (Next.js 16, Postgres via Drizzle, Astryx design system; DineLoop runs on the TableTap codebase). Each app runs with fictional demo data; WhatsApp, email and payments are simulated, and CI passes on all of them. Apps are not deployed yet; they will be served at `https://<product>.craftlayer.store`. Market figures are sourced with access dates; anything unsourced is marked *(estimate)*. No customers or revenue yet.

## Licence

All CraftLayer product repositories are source-available under the [PolyForm Noncommercial License 1.0.0](LICENSE.md). Personal, educational, research and non-profit use is free. **Any commercial use requires a paid licence or written permission from CraftLayer Studio.** See [COMMERCIAL-LICENSE.md](COMMERCIAL-LICENSE.md).
