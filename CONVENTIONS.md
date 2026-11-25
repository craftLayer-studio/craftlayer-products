# CraftLayer Products — Documentation Conventions

Every product folder follows the same structure so any human or AI agent can navigate any product the same way.

## Folder layout

```
<product-slug>/
├── README.md                              # One-page summary: name, tagline, ICP, top features, pricing, links
├── AGENTS.md                              # Brief for AI agents: context, glossary, reading order, decisions, open questions
└── docs/
    ├── 01-product-plan.md                 # Vision, ICP, personas, user journeys, features by phase, data model, integrations, metrics
    ├── 02-problems-and-benefits.md        # Problem -> solution -> benefit, per stakeholder (owner, staff, end customer)
    ├── 03-pros-cons-risks.md              # Pros, cons, risks + mitigations, kill criteria
    ├── 04-market-research.md              # Market size, competitors, pricing benchmarks, trends, regulation, sources
    ├── 05-pricing-and-revenue.md          # Tiers (INR + USD), add-ons, revenue streams, unit economics, 12-month scenarios
    └── 06-go-to-market-and-onboarding.md  # Channels, sales script, objection handling, onboarding checklist, retention
```

## Writing rules

1. **Market focus:** India-first (Tier 1–3 cities), global-ready later. Prices in INR with USD equivalents.
2. **No invented facts.** Every statistic, market size or competitor price carries a source link and access date. Anything unsourced is labelled **(estimate)** with its reasoning.
3. **Build on the shared core.** Features that several products need (QR menus/catalogs, CRM, WhatsApp messaging, loyalty, payments, games, reviews, analytics) live in [`core/`](https://github.com/craftLayer-studio/craftlayer-core/blob/main/README.md). Product docs reference core modules instead of re-specifying them.
4. **Compliance:** Any product collecting customer phone numbers must follow India's Digital Personal Data Protection Act 2023 and DPDP Rules 2025: clear notice, explicit opt-in, purpose limitation, easy opt-out, and WhatsApp template/opt-in policy.
5. **Money first.** Every feature states which metric it moves: acquisition, activation, retention, revenue (ARPU) or referral.
6. **Format:** GitHub-flavoured Markdown, tables for comparisons, headings in sentence case, no emoji.
