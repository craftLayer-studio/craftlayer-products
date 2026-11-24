# AGENTS.md: guide for AI agents

You are working in the CraftLayer Products planning repository. It holds product plans, research and go-to-market docs for 11 vertical SaaS products built on one shared platform. There is no application code here yet. The restaurant ordering prototype lives in [craftLayer-studio/tabletap](https://github.com/craftLayer-studio/tabletap).

## Reading order

1. [README.md](README.md): what the portfolio is
2. [portfolio/STRATEGY.md](portfolio/STRATEGY.md): priorities and sequencing
3. [core/README.md](core/README.md), then `core/docs/`: shared platform, architecture, compliance, build order
4. The product folder you are working on: `<slug>/AGENTS.md`, then `<slug>/docs/01` to `06`

Product catalog with slugs: [portfolio/AGENT-BRIEF.md](portfolio/AGENT-BRIEF.md).

## Rules when editing

- Follow [CONVENTIONS.md](CONVENTIONS.md): same file set per product, India-first, INR with USD.
- Never invent statistics. Cite a source URL with access date, or label it *(estimate)* with reasoning.
- Shared capabilities belong in `core/`. Product docs reference Core modules by name instead of re-specifying them.
- Any feature touching customer personal data must follow [core/docs/compliance.md](core/docs/compliance.md).
- Tie every new feature to a metric: acquisition, activation, retention, revenue or referral.
- Keep each product's "Open questions" section in its AGENTS.md current when you resolve or discover one.

## Building a product

When asked to implement a product, start from `core/docs/build-order.md` and the product's `docs/01-product-plan.md` P0 list. Build Core modules generically, put vertical-only code in a vertical layer (see `core/docs/architecture.md`), and do not fork Core per vertical.
