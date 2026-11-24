# CraftLayer Core: architecture

## Principles

1. **One platform, many verticals.** Vertical products are feature flags, vocabulary packs and a small amount of vertical code on top of Core.
2. **Mobile web first.** End customers never install an app. They scan a QR and get a fast page (target < 1.5 s on 4G, < 200 KB first load).
3. **Owner on WhatsApp.** Owners live on WhatsApp, so daily summaries, alerts and approvals go there. The dashboard is secondary.
4. **Works on bad internet.** Staff app and kitchen/queue displays queue writes offline and sync when the connection returns.
5. **Tenant isolation by default.** Every row carries `org_id`; Postgres row-level security enforces it.

## Vertical layer pattern

```
core/                      shared modules (accounts, QR, storefront, orders, payments, CRM, messaging, loyalty, games, reviews, analytics)
verticals/<slug>/
    vocabulary.json        "table" / "room" / "bay" / "chair"; "order" / "booking" / "job card"
    features.json          which core modules are enabled, default settings
    templates/             WhatsApp message templates, receipts, print layouts
    modules/               vertical-only code (e.g. KDS for DineLoop, job cards for GaragePilot, rent ledger for NestKeep)
    onboarding.json        wizard steps and sample data
```

## Core data model (simplified)

| Entity | Key fields | Notes |
|---|---|---|
| `org` | id, name, vertical, plan, gstin | The paying business |
| `location` | id, org_id, name, address, timezone | Outlet / branch |
| `spot` | id, location_id, type, label, qr_code | Table, room, bay, chair, court, entrance |
| `catalog_item` | id, org_id, name, price, tax_rate, category, variants, availability | Dish, service, product, plan |
| `customer` | id, org_id, phone (E.164), name, birthday, tags, consent_status | One per business; never shared across tenants |
| `consent_record` | customer_id, purpose, notice_version, granted_at, withdrawn_at, channel | DPDP audit trail |
| `order` | id, location_id, spot_id, customer_id, status, total, source | Generic: order, booking, job, token |
| `order_line` | order_id, item_id, qty, price, notes, status | Kitchen/bay status per line |
| `booking` | id, resource_id, starts_at, ends_at, status | Slots for courts, chairs, rooms, doctors |
| `payment` | id, order_id, method, amount, gateway_ref, status | UPI / card / cash / credit (khata) |
| `loyalty_ledger` | customer_id, delta, reason, expires_at | Points, stamps, cashback |
| `campaign` | id, org_id, segment, template_id, scheduled_at, stats | WhatsApp marketing |
| `game_play` | id, customer_id, game, reward_id, played_at | Rate limited per phone/device |
| `feedback` | id, order_id, rating, text, routed_to | Review funnel |
| `staff` | id, org_id, role, phone, commission_rule | Staff app users |

## Realtime flows

- **Order to station:** customer submits order -> `order.created` event -> KDS/staff app subscribes per location -> line status updates stream back to the customer page.
- **Queue/token:** token issued -> live position pushed to the customer's page and optional WhatsApp "you're next" utility message.

## Security baseline

- OTP login for owners and staff; no customer login needed (phone captured at order/booking with consent).
- Rate limit QR endpoints and game plays per phone and device fingerprint.
- Payment webhooks verified by signature; never trust client-side totals.
- PII encrypted at rest; exports logged; role-based access to customer phone numbers (staff see masked numbers).
