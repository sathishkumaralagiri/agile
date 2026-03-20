# 📊 agile / agile-metrics

> Part of the [`agile`](../) reference library. A comprehensive guide to Agile metrics, estimation techniques, and team performance indicators.

**Live site:** `sathishkumaralagiri.github.io/agile/agile-metrics/`

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightblue.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Stars](https://img.shields.io/github/stars/sathishkumaralagiri/agile?style=social)](.)

---

## Repo Structure

```
agile/                        ← parent repo (sathishkumaralagiri.github.io/agile/)
├── index.html                ← parent landing page
└── agile-metrics/            ← this module (sathishkumaralagiri.github.io/agile/agile-metrics/)
    ├── index.html            ← docs site
    ├── README.md             ← this file
    ├── CONTRIBUTING.md
    ├── LICENSE
    └── docs/
        ├── monte-carlo-example.md
        └── templates/
```

---

## Table of Contents

- [Overview](#overview)
- [Metrics Reference](#metrics-reference)
  - [Velocity](#velocity)
  - [Cycle Time](#cycle-time)
  - [Lead Time](#lead-time)
  - [Throughput](#throughput)
  - [Cumulative Flow Diagram (CFD)](#cumulative-flow-diagram)
  - [Sprint Burndown](#sprint-burndown)
  - [Release Burnup](#release-burnup)
  - [Escaped Defects](#escaped-defects)
- [Estimation Techniques](#estimation-techniques)
  - [Story Points](#story-points)
  - [Planning Poker](#planning-poker)
  - [T-Shirt Sizing](#t-shirt-sizing)
  - [Three-Point Estimation](#three-point-estimation)
  - [Monte Carlo Simulation](#monte-carlo-simulation)
  - [#NoEstimates](#noestimates)
- [Anti-Patterns](#anti-patterns)
- [Formulas Cheat Sheet](#formulas-cheat-sheet)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

This library is a practitioner's reference for teams using Agile methodologies. Whether you're a Scrum Master, Product Owner, engineering lead, or team member, you'll find:

- **Clear definitions** of every major Agile metric
- **Formulas** with worked examples
- **When to use** (and when NOT to use) each metric
- **Estimation techniques** compared side-by-side
- **Anti-patterns** to avoid common traps

---

## Metrics Reference

### Velocity

**Definition:** The amount of work (in story points or items) a team completes in a single sprint.

**Formula:**
```
Velocity = Sum of story points for all completed user stories in a sprint
```

**Example:**
| Sprint | Completed Points |
|--------|-----------------|
| Sprint 1 | 32 |
| Sprint 2 | 28 |
| Sprint 3 | 35 |
| **Average Velocity** | **31.7** |

**Use it for:**
- Sprint planning (use rolling average of last 3–6 sprints)
- Release forecasting

**⚠️ Warning:** Velocity is team-specific. Never compare velocity across teams — it incentivizes point inflation.

---

### Cycle Time

**Definition:** Time from when work *starts* to when it's *done*.

**Formula:**
```
Cycle Time = Done Date − Start Date
```

**Why it matters:** Shorter cycle times mean faster feedback loops and lower risk.

**Histogram tip:** Plot cycle time as a histogram. Target the 85th percentile for forecasting commitments.

---

### Lead Time

**Definition:** Time from when work is *requested* to when it's *delivered*.

**Formula:**
```
Lead Time = Done Date − Request Date
         = Queue Time + Cycle Time
```

| Metric | Measures |
|--------|----------|
| Lead Time | Customer experience of wait |
| Cycle Time | Team's actual work duration |

---

### Throughput

**Definition:** Number of work items completed per unit time (week, sprint, month).

**Formula:**
```
Throughput = Items Completed / Time Period
```

**Example:** 18 stories completed in 4 weeks = **4.5 items/week**

**Use throughput** (not velocity) when items are roughly similar in size, or when using #NoEstimates approaches.

---

### Cumulative Flow Diagram

**Definition:** A stacked area chart showing the count of items in each workflow state over time.

**Key signals to watch:**
- **Widening bands** → bottleneck forming in that stage
- **Flat top line** → no new work entering (good or bad?)
- **Parallel bands** → healthy flow

**Metrics derivable from a CFD:**
```
Average Cycle Time ≈ WIP / Throughput   (Little's Law)
```

---

### Sprint Burndown

**Definition:** Tracks remaining work (hours or points) against time within a sprint.

**Ideal line formula:**
```
Ideal Remaining = Total Points × (Days Remaining / Total Sprint Days)
```

**Healthy burndown:** Actual line stays close to ideal. Flat lines mid-sprint = blockers.

---

### Release Burnup

**Definition:** Tracks completed work against the total scope over multiple sprints.

**Why burnup > burndown for releases:**
- Scope changes are visible (line moves up)
- Shows progress toward a goal clearly

```
Remaining = Total Scope − Completed Work
Projected Completion Date = Today + (Remaining / Avg Velocity)
```

---

### Escaped Defects

**Definition:** Bugs found by customers *after* release that were not caught during development.

**Formula:**
```
Escaped Defect Rate = Bugs Found Post-Release / Total Bugs Found × 100%
```

**Target:** < 10% for most teams. Track trend over time, not absolute value.

---

## Estimation Techniques

### Story Points

**What they are:** Relative units representing effort, complexity, and uncertainty — not hours.

**Fibonacci-like scale (most common):**
```
1 → 2 → 3 → 5 → 8 → 13 → 21 → ?
```

**Rules of thumb:**
- A "1" should be something trivially small (fix a typo, update config)
- If an item is > 13 points, split it
- Points measure *relative* complexity, not time

---

### Planning Poker

**Process:**
1. Product Owner reads a user story
2. Each team member silently picks a card (Fibonacci value)
3. All reveal simultaneously
4. Highest and lowest estimates discuss reasoning
5. Re-vote until consensus

**Why simultaneous reveal?** Prevents anchoring bias.

**Tools:** [PlanningPoker.com](https://planningpoker.com), [Scrumpoker-online.org](https://scrumpoker-online.org)

---

### T-Shirt Sizing

**Sizes:** XS · S · M · L · XL · XXL

**Best for:** Early-stage roadmap estimation, epics, or portfolio-level planning when story-level detail isn't available yet.

| T-Shirt | Story Points Equivalent |
|---------|------------------------|
| XS | 1–2 |
| S | 3 |
| M | 5–8 |
| L | 13 |
| XL | 21+ |
| XXL | Needs breaking down |

---

### Three-Point Estimation

**Formula (PERT):**
```
E = (O + 4M + P) / 6

Where:
  O = Optimistic estimate
  M = Most likely estimate
  P = Pessimistic estimate
```

**Example:**
```
O = 2 days, M = 5 days, P = 14 days
E = (2 + 4×5 + 14) / 6 = (2 + 20 + 14) / 6 = 36/6 = 6 days
```

**Standard deviation:**
```
σ = (P - O) / 6 = (14 - 2) / 6 = 2 days
```

Use σ to communicate uncertainty ranges.

---

### Monte Carlo Simulation

**Concept:** Run thousands of simulated sprints using historical throughput data to produce a probability distribution of completion dates.

**Steps:**
1. Collect last 10–20 sprints of throughput data
2. For each simulation run: randomly sample throughput per sprint
3. Run 1,000–10,000 simulations
4. Plot the distribution of completion dates

**Output example:**
```
50th percentile: Done by June 14
85th percentile: Done by June 28   ← use this for commitments
95th percentile: Done by July 12
```

**Tools:** [Actionable Agile](https://actionableagile.com), [Nave](https://nave.team), spreadsheet templates in `/docs/templates/`

---

### #NoEstimates

**Philosophy:** Replace point estimation with counting work items and using throughput + Monte Carlo for forecasting.

**When it works well:**
- Items are broken down to a roughly uniform size ("right-sized" stories)
- Team has stable historical data (10+ sprints)
- Stakeholders trust probabilistic forecasting

**When it's harder:**
- Highly variable item sizes
- New teams without history
- Fixed-price contracts requiring upfront estimates

---

## Anti-Patterns

| Anti-Pattern | Why It's Harmful | Better Approach |
|---|---|---|
| Comparing velocity across teams | Different teams, different points = meaningless | Use throughput % improvement within a team |
| Using velocity for individual performance | Creates gaming and point inflation | Measure team outcomes, not individual output |
| 100% sprint commitment | No buffer = no room for bugs, learning, or help | Target 70–80% planned, leave slack |
| Treating estimates as commitments | Estimates are probabilistic; commitments are binary | Communicate ranges and confidence levels |
| Velocity as the only metric | Ignores quality, sustainability, customer value | Balance with defect rates, NPS, cycle time |
| Ignoring cycle time outliers | One 30-day item destroys your average | Use percentiles (85th), not averages |

---

## Formulas Cheat Sheet

```
# Flow Metrics
Lead Time        = Done Date − Request Date
Cycle Time       = Done Date − Start Date
Throughput       = Items Done / Time Period
WIP              = Active items at any point in time
Little's Law     = WIP = Throughput × Cycle Time

# Velocity & Forecasting
Velocity (avg)   = Sum(Points, last N sprints) / N
Forecast Date    = Today + (Remaining Scope / Avg Velocity) × Sprint Length

# Estimation (PERT)
Expected         = (Optimistic + 4×MostLikely + Pessimistic) / 6
Std Deviation    = (Pessimistic − Optimistic) / 6

# Quality
Escaped Defect % = Post-release Bugs / Total Bugs × 100
Defect Density   = Defects Found / Size (KLOC or Story Points)
```

---

## Contributing

Contributions are welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md) before submitting a PR.

Areas where we'd love help:
- 📝 Additional estimation technique write-ups
- 📊 Spreadsheet/template examples in `/docs/templates/`
- 🌍 Translations
- 🔗 Tool integrations and comparisons

---

## License

[Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE) © 2026 sathishkumaralagiri

You are free to share and adapt this material for any purpose, even commercially, as long as you give appropriate credit.
