---
name: dashboard-builder
description: >
  Use this skill whenever a user wants to BUILD, DESIGN, or PLAN a dashboard from scratch —
  not just review one. Triggers include: "help me build a dashboard", "I want to create a
  Power BI report", "what should my dashboard include", "I'm starting a new analytics project",
  "how do I structure this dashboard", "what KPIs should I track", "help me plan a data
  visualization", "I want to build a portfolio project", "what metrics matter for X industry",
  or any request to produce a dashboard before it exists. Also triggers when a user mentions
  an industry or domain and asks what analytics to build. This skill produces a complete
  dashboard blueprint: audience definition, KPI selection, chart specifications, layout plan,
  data source recommendations (including live public APIs), and a pre-build checklist that
  maps directly to every dimension a senior analyst would later review. Use proactively —
  if someone shares data and seems to be heading toward a dashboard, offer to run this skill.
---

# Dashboard Builder Skill

A structured framework for designing 100/100 dashboards *before* you build them — so you
never have to fix a fundamental design mistake after the fact.

Built as the proactive companion to the dashboard-review skill. Every step here maps directly
to the 6 dimensions that a reviewer would later score, so a dashboard built with this skill
should score well on review by design.

## Core philosophy

A dashboard is not a collection of charts. It is an answer to a specific question, delivered
to a specific person, in the minimum time possible.

Every decision — what KPIs to include, which chart type, what colour — must be traceable back
to: *does this help [this audience] answer [this question] faster?*

If yes: include it. If no: cut it.

---

## How to use this skill

When a user wants to build a dashboard:

1. Work through Steps 0–5 in order
2. Never skip Step 0 — audience and question definition changes every subsequent decision
3. Reference `references/industry-kpis.md` for domain-specific metric lists
4. Reference `references/live-data-sources.md` for public API recommendations
5. Deliver output in the structured Blueprint format defined in Step 5
6. End with the Pre-Build Checklist — this is the quality gate before any tool is opened

---

## STEP 0 — Define the audience and the question

Before choosing a single metric, lock in two things:

### 0a. Who is this for?

| Audience | Primary need | Max time on dashboard | Detail level |
|---|---|---|---|
| C-Suite / Executive | Go/no-go, situation awareness | 3–5 min | 3–5 headline KPIs only |
| Department Head | Performance management | 5–10 min | Summary + one breakdown |
| Operations Manager | What to act on today | 10–20 min | Task-level status, ownership |
| Analyst / Data Team | Pattern investigation | Unlimited | Full granularity, drill-through |
| Field / Frontline | What do I do next | 30 seconds | One unambiguous action signal |
| External Stakeholder | Confidence, accountability | 2–3 min | Curated highlights, no jargon |

**Rules:**
- One audience per dashboard page. Mixing audiences on one page = design failure
- If the audience is unclear, the dashboard cannot be designed — stop and clarify
- The audience determines every subsequent decision in this skill

### 0b. What is the one question this dashboard answers?

Write it as a complete sentence. Examples:
- "Are our regional sales teams hitting their monthly targets, and where are the gaps?"
- "Which warehouses are creating delivery delays, and what is the root cause?"
- "How has malaria intervention coverage changed across Africa from 2007–2017?"
- "Which customer segments are churning and what triggers the decision?"

If you cannot write this sentence, the dashboard is not ready to design. Work with the user
to define it before proceeding.

---

## STEP 1 — Select the right metrics

### 1a. Metric quality test

For every proposed metric, ask:
- **Diagnostic**: Does it diagnose a problem, or just describe a state?
- **Actionable**: Can this audience do something different because of this number?
- **Leading or lagging**: Leading metrics predict outcomes; lagging confirm them. Balance both.
- **Comparable**: Is there a target, prior period, or benchmark to compare against?
  A number without comparison is a fact, not an insight.

### 1b. The vanity metric trap

Cut any metric that:
- Makes the team look busy without proving business value
- Cannot be influenced by the audience's decisions
- Has no agreed definition or target
- Would not change a decision even if it moved significantly

### 1c. Metric count by audience

| Audience | Primary KPIs | Supporting metrics | Max charts per page |
|---|---|---|---|
| Executive | 3–5 | 2–4 trend lines | 5 |
| Department Head | 5–8 | Breakdowns | 6–8 |
| Operations Manager | 8–12 | Task tables, status flags | 8–10 |
| Analyst | Unlimited | Drill-throughs, slicers | No limit |

For domain-specific metric lists, see `references/industry-kpis.md`.

---

## STEP 2 — Design the layout

### 2a. The top-left priority rule

The most important finding for this audience must occupy the top-left of the dashboard.
This is where every viewer looks first. Wasting it on a logo or navigation = design failure.

### 2b. Reading path design

Structure every page as:
```
[Top-left: Most critical KPI / headline finding]
[Top-right: Key supporting context or trend]
[Middle: Breakdown / distribution]
[Bottom: Detail / drill-down / table]
```

### 2c. Layout grid decisions

- **Executive dashboard**: 2–3 KPI cards top, 1–2 trend charts below, nothing else
- **Operations dashboard**: Status summary top, prioritised action list middle, detail table bottom
- **Analyst dashboard**: Filter panel left, overview top, drill-through panels below

### 2d. Page count

- 1 page for executive dashboards (if they scroll, you've already lost them)
- 2–4 pages for operational and analytical dashboards — one clear theme per tab
- Name tabs as verbs or questions: "Revenue performance" not "Page 2"

---

## STEP 3 — Choose the right charts

### 3a. Chart selection guide

| You want to show | Best chart | Anti-patterns to avoid |
|---|---|---|
| Change over time | Line chart | Bar chart for long time series |
| Comparison across categories | Horizontal bar | Pie/donut with 5+ segments |
| Part of a whole (≤4 categories) | Donut or stacked bar | 3D pie |
| Distribution | Histogram or box plot | — |
| Correlation between two variables | Scatter plot | — |
| Geographic distribution | Choropleth map (if quantity varies) | Dot map for quantitative data |
| Progress toward a target | Bullet chart or progress bar | Gauge / speedometer |
| Ranking | Ranked bar (sorted) | Unsorted table |
| Two metrics over time | Dual-axis line (labelled clearly) | Dual-axis bar |

### 3b. Anti-pattern hard stops

Never include these — flag and remove before building:
- 3D charts of any kind (always distort perception)
- Pie/donut with 5+ categories
- Gauge/speedometer charts (low data-ink, misleading range)
- Maps encoding no quantitative data (decoration, not information)
- Colour as the only differentiator (accessibility failure)
- More than 2 axes on a single chart

### 3c. Chart count

2–3 key visuals per page is the standard. 4–5 is acceptable for operational dashboards.
6+ charts per page dilutes the message — split into multiple pages instead.

---

## STEP 4 — Design the colour and visual system

### 4a. Colour encodes meaning — not decoration

Assign colour to communicate, not to make it look nice:
- **Red** = at risk / behind target / urgent action needed
- **Amber** = caution / approaching threshold / monitor
- **Green** = on track / healthy / no action needed
- **Blue/teal** = neutral information / selected item
- **Grey** = baseline / historical / inactive

### 4b. Consistency rules

- Same colour = same meaning everywhere in the dashboard. No exceptions.
- Use a single primary colour for positive states, a single colour for negative states
- Never use more than 3–4 colours on a single chart
- Test the palette with a free colour blindness simulator before finalising

### 4c. Accessibility minimum

- Minimum 4.5:1 contrast ratio between text and background
- Never rely on colour alone — add icons, labels, or patterns as secondary encodings
- Ensure all text is ≥12px

---

## STEP 5 — Plan the data and interactivity

### 5a. Data requirements per metric

For each KPI in the blueprint, document:
- Source table/API
- Grain (row = one what?)
- Refresh frequency needed (real-time / daily / weekly / monthly)
- Filters it should respond to
- Target / benchmark source

### 5b. Interactivity by audience

| Audience | Slicers/filters | Cross-filtering | Drill-through | Tooltips |
|---|---|---|---|---|
| Executive | Pre-set only | Minimal | No | Yes |
| Operations Manager | Date, region, status | Yes | Yes | Yes |
| Analyst | Full control | Yes | Yes | Yes |

### 5c. What to add that most builders forget

- **"Data as of" timestamp** — mandatory on every page
- **Unit labels** on every axis and KPI card (£, %, thousands, per 1,000, etc.)
- **Definition tooltips** for any non-obvious metric
- **Empty state design** — what does the dashboard show when there's no data?
- **Mobile/tablet layout** if the audience will access on those devices

For live public data sources, see `references/live-data-sources.md`.

---

## STEP 6 — Pre-Build Checklist (quality gate)

Run through every item before opening Power BI, Tableau, or any other tool.
Every NO is a design decision you must resolve first.

### Audience & Question
- [ ] Audience is named and specific (not "everyone" or "the team")
- [ ] One primary question is written in full — not a topic, a question
- [ ] Dashboard serves one audience on each page

### Metrics
- [ ] Every metric has a comparison value (target, prior period, or benchmark)
- [ ] Vanity metrics have been cut
- [ ] Each metric is defined with agreed calculation logic
- [ ] Metric count is calibrated to audience attention span

### Layout
- [ ] Most important finding is top-left
- [ ] Reading path flows: headline → context → breakdown → detail
- [ ] Page count and tab names are defined before building starts
- [ ] Chart count per page is within audience-appropriate limits

### Charts
- [ ] Each chart is selected from the chart selection guide
- [ ] No anti-pattern charts appear in the plan
- [ ] Every chart has a title that answers "what does this show?"

### Colour & Accessibility
- [ ] Colour palette defined with explicit meaning per colour
- [ ] Colour is consistent across all pages
- [ ] Secondary encoding (icon, label, pattern) added for colour-only signals

### Data & Interactivity
- [ ] Data source identified for every metric
- [ ] Refresh frequency is feasible with the data source
- [ ] "Data as of" stamp planned
- [ ] Unit labels planned for every axis and card
- [ ] Interactivity level matches audience needs

---

## Reference files

- `references/industry-kpis.md` — Domain-specific KPI lists for 16 industries
- `references/live-data-sources.md` — Free public APIs with sample use cases
- `references/portfolio-projects.md` — 100+ project ideas by industry and skill level

---

## Output format (Step 5 — The Blueprint)

Return the dashboard blueprint in this format:

---

**DASHBOARD TITLE** — Working title

**AUDIENCE** — Who, and how determined

**CORE QUESTION** — The one question this dashboard answers

**KPI PLAN:**

| Metric | Definition | Comparison | Source | Unit |
|---|---|---|---|---|
| ... | ... | ... | ... | ... |

**LAYOUT PLAN** — Page structure described or sketched in text/ASCII

**CHART SPECIFICATIONS:**
Each chart: type, data, title, and any notes

**COLOUR SYSTEM** — Colour → meaning mapping

**DATA REQUIREMENTS** — Source, grain, refresh frequency per metric

**INTERACTIVITY PLAN** — Filters, slicers, drill-through

**PRE-BUILD CHECKLIST** — All items completed, with notes on any NOs

**LIVE DATA RECOMMENDATION** — If applicable, which public API to use and why
