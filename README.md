# Dashboard Builder Skill for Claude

A structured framework for designing **100/100 dashboards before you build them** — packaged
as a Claude skill and a free web app.

The proactive companion to the
[Dashboard Review Skill](https://github.com/David-Abu/dashboard-review-skill) by David Abu.
Where that skill tells you what went wrong, this one ensures you never make those mistakes
in the first place.

**Live web app →** [https://ibukunegwu.github.io/dashboard-builder-skill/](https://ibukun-egwuogu.github.io/dashboard-builder-skill/)

---

## What This Skill Does

When you describe a dashboard you want to build, this skill produces a complete blueprint:

- **Audience & question definition** — locks in the design standard before any metric is chosen
- **Domain-specific KPI plan** — the right metrics for your industry, each with a comparison value
- **Layout specification** — reading path, visual hierarchy, page count
- **Chart specifications** — right chart type for every insight, with anti-patterns explicitly excluded
- **Colour system** — colour mapped to meaning, not decoration
- **Data requirements** — source, grain, and refresh frequency per metric
- **Live data API recommendation** — real, connectable data source for your domain
- **Pre-build checklist** — 12+ quality gates spanning all 6 review dimensions

---

## The 6 Dimensions (Built In from the Start)

Every blueprint is designed to score well on all six review dimensions:

| # | Dimension | What the builder addresses |
|---|---|---|
| 1 | Business Question & Purpose | Core question defined; every chart must serve it |
| 2 | Domain Knowledge | Industry-specific KPIs from 16 domain reference library |
| 3 | Audience Fit & Interactivity | Detail level and interactivity matched to audience |
| 4 | Data Accuracy, Story & Definitions | Every KPI has a comparison; units and timestamps planned |
| 5 | Visual Design, Chart Choice & Consistency | Chart selection guide; anti-patterns blocked |
| 6 | Actionability & The So What | Viewer leaves with one clear action |

---

## Quick Start

### Option 1 — Use the Web App (no install needed)

Go to **https://ibukunegwu.github.io/dashboard-builder-skill/**
You will need a free Anthropic API key to use the builder. Get one at [platform.anthropic.com](https://platform.anthropic.com) — it takes 2 minutes and comes with free credits.

Answer five questions, get a full blueprint — ready to take into Power BI, Tableau, or any tool.

### Option 2 — Install as a Claude Skill

1. Download `dashboard-builder.skill` from the [Releases](../../releases) page
2. In Claude.ai, go to **Settings → Connectors → Customize → Skills → (+) → Upload Skill**
3. Upload the `.skill` file
4. Ask Claude: "Help me build a dashboard for [your domain]"

### Option 3 — Use the SKILL.md directly

Copy the contents of `SKILL.md` into any Claude conversation or LLM pipeline.

---

## Triggering the Skill

Any of these will trigger the builder:

```
Help me build a sales dashboard
I want to design a Power BI report for HR
What should my logistics dashboard include?
I'm starting a new analytics portfolio project
What KPIs should I track for e-commerce?
Help me plan a dashboard for [industry]
```

---

## Industry Coverage (16 Domains)

Detailed KPI lists in `references/industry-kpis.md`:

Healthcare · Sales & Retail · Finance & Banking · Telecommunications ·
Logistics & Supply Chain · E-commerce · Education · Energy & Utilities ·
Transportation & Mobility · Marketing & Advertising · Agriculture & Agribusiness ·
Real Estate · HR & People Analytics · Sports Analytics ·
Social Impact / NGO · Government & Public Policy

---

## Live Data Sources Included

The skill recommends and demonstrates real, free public APIs:

| Source | Domain | URL |
|---|---|---|
| WHO Global Health Observatory | Health, disease, interventions | https://ghoapi.azureedge.net/api/ |
| World Bank Open Data | Economics, development | https://api.worldbank.org/v2/ |
| Frankfurter | Exchange rates (NGN, GBP, USD...) | https://api.frankfurter.app/ |
| Open-Meteo | Weather, climate | https://api.open-meteo.com/ |
| Alpha Vantage | Stocks, forex, crypto | https://www.alphavantage.co/ |
| Our World in Data | Multi-domain clean CSVs | https://github.com/owid/owid-datasets |

Full list with sample API calls in `references/live-data-sources.md`.

---

## Repo Structure

```
dashboard-builder-skill/
├── README.md
├── SKILL.md                              ← The Claude skill
├── dashboard-builder.skill               ← Packaged skill file for one-click install
├── docs/
│   └── index.html                        ← GitHub Pages web app
└── references/
    ├── industry-kpis.md                  ← KPI lists for 16 industries
    ├── live-data-sources.md              ← Free API reference with sample calls
    └── portfolio-projects.md             ← 100+ project ideas (Joy Ibe)
```

---

## Companion Tool

This skill pairs with the
[Dashboard Review Skill](https://github.com/David-Abu/dashboard-review-skill) by David Abu:

| Tool | When to use |
|---|---|
| **Dashboard Builder** (this) | Before you build — design decisions, blueprint, checklist |
| **Dashboard Review** (David Abu) | After you build — scoring, critique, improvement priorities |

---

## Built By

**Ibukun Egwu** · Data Analytics & Business Intelligence

Industry KPI reference sourced from Joy Ibe's *100+ Data Analytics Portfolio Projects* guide.
Review framework from David Abu's Dashboard Review Skill (MIT License).

---

## License

MIT — use freely, adapt as needed, attribution appreciated.
