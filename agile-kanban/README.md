# 🔲 agile / agile-kanban

> Part of the [`agile`](../) reference library. A complete practitioner's guide to Kanban — WIP limits, flow, classes of service, cadences, and metrics.

**Live site:** `sathishkumaralagiri.github.io/agile/agile-kanban/`

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightblue.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Stars](https://img.shields.io/github/stars/sathishkumaralagiri/agile?style=social)](.)

---

## Table of Contents

- [Overview](#overview)
- [Core Principles](#core-principles)
- [Kanban Practices](#kanban-practices)
  - [Visualise the Workflow](#visualise-the-workflow)
  - [Limit WIP](#limit-wip)
  - [Manage Flow](#manage-flow)
  - [Make Policies Explicit](#make-policies-explicit)
  - [Implement Feedback Loops](#implement-feedback-loops)
  - [Improve Collaboratively](#improve-collaboratively)
- [The Kanban Board](#the-kanban-board)
- [WIP Limits](#wip-limits)
- [Classes of Service](#classes-of-service)
- [Cadences](#cadences)
- [Flow Metrics](#flow-metrics)
- [Kanban vs Scrum](#kanban-vs-scrum)
- [Anti-Patterns](#anti-patterns)
- [Kanban Cheat Sheet](#kanban-cheat-sheet)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

Kanban is a method for managing knowledge work with an emphasis on just-in-time delivery without overloading team members. It is not a software development framework — it is a **change management method** designed to be overlaid on existing processes.

**Three core properties:**
- Start with what you do now
- Agree to pursue incremental, evolutionary change
- Respect the current process, roles, responsibilities, and job titles

---

## Core Principles

### Change Management Principles
1. **Start with what you do now** — Kanban does not require a specific starting setup
2. **Agree to pursue incremental, evolutionary change** — small, continuous improvements over big transformations
3. **Encourage acts of leadership at all levels** — improvement is everyone's responsibility

### Service Delivery Principles
1. **Understand and focus on customer needs and expectations**
2. **Manage the work; let people self-organise around it**
3. **Regularly review the network of services and policies**

---

## Kanban Practices

### Visualise the Workflow

Map every step from commitment to delivery on a board. Make work visible — including work that is stuck, blocked, or waiting.

**A good workflow visualisation includes:**
- All workflow states (columns)
- Work item types (cards, often colour-coded)
- WIP limits per column
- Explicit policies (e.g. "Definition of Done per stage")
- Blockers and dependencies

---

### Limit WIP

**This is the single most important Kanban practice.**

WIP (Work in Progress) limits constrain how many items can be in a workflow state at any one time. Limiting WIP:
- Reduces context switching
- Surfaces bottlenecks immediately
- Creates pull (new work starts only when capacity exists)
- Improves cycle time

**Setting WIP limits:**
```
Start with: WIP limit = number of team members × 1.5
Observe bottlenecks and adjust over time
Lower limits = faster flow, but more discipline required
```

**⚠️ Anti-pattern:** Treating WIP limits as suggestions. If the limit is 3 and there are 4 items in a column, the team must stop and swarm on the blocked work — not just add a fourth card.

---

### Manage Flow

Monitor how work moves through the system. The goal is smooth, predictable flow — not maximum utilisation.

**Key flow concepts:**
- **Pull system:** work is pulled when downstream capacity exists; never pushed
- **Little's Law:** `WIP = Throughput × Cycle Time`
- **Bottleneck:** the stage where work accumulates; identify and address it first

---

### Make Policies Explicit

Every decision about how work is handled should be written down and visible. Implicit policies create inconsistency and conflict.

**Examples of explicit policies:**
- Entry criteria for each workflow state
- Definition of Done per stage
- How blockers are escalated
- Classes of service and their rules
- How WIP limit exceptions are handled

---

### Implement Feedback Loops

Regular cadences create opportunities to inspect and adapt. See [Cadences](#cadences) section.

---

### Improve Collaboratively

Use models (like the Theory of Constraints or systems thinking) to understand the system and guide improvements. Changes should be agreed by the team, not imposed top-down.

---

## The Kanban Board

A Kanban board represents the workflow. Each column is a workflow state. Cards move left to right.

**Typical board layout:**
```
┌──────────┬──────────┬──────────┬──────────┬──────────┐
│ Backlog  │  Ready   │    In    │  Review  │   Done   │
│          │  (WIP:3) │Progress  │  (WIP:2) │          │
│          │          │  (WIP:4) │          │          │
├──────────┼──────────┼──────────┼──────────┼──────────┤
│  ██████  │  █████   │  ██████  │  █████   │  █████   │
│  ██████  │  █████   │  ██████  │  █████   │  █████   │
│  ██████  │  █████   │  ██████  │          │  █████   │
│  ██████  │          │  ██████  │          │          │
└──────────┴──────────┴──────────┴──────────┴──────────┘
```

**Buffer columns:** add "Done" sub-columns between active stages to make handoffs explicit and measure queue time separately from active time.

---

## WIP Limits

WIP limits are the engine of Kanban. They enforce pull and expose bottlenecks.

### How to set WIP limits

| Team size | Starting WIP limit per active stage |
|-----------|-------------------------------------|
| 1–3 people | 2–3 items |
| 4–6 people | 3–5 items |
| 7–10 people | 5–8 items |

**Little's Law applied:**
```
Cycle Time = WIP / Throughput

Lower WIP → Lower Cycle Time (assuming same throughput)
```

### WIP limit exceptions

Exceptions should be rare and explicit. When a WIP limit must be exceeded:
- Add a visible "expedite" indicator to the card
- Discuss in the next team meeting
- Adjust the limit if exceptions are frequent

---

## Classes of Service

Classes of Service (CoS) define how different types of work should be treated, prioritised, and scheduled.

| Class | Description | SLA / Priority | Example |
|-------|-------------|----------------|---------|
| **Expedite** | Business-critical, must be done immediately | Bypass WIP limits; do now | Production outage, security breach |
| **Fixed Date** | Must be delivered by a specific date | Schedule by date; risk managed | Regulatory deadline, conference demo |
| **Standard** | Normal business value work | First-in, first-out | Feature development, improvements |
| **Intangible** | Long-term value, no immediate urgency | Fill remaining capacity | Tech debt, refactoring, research |

**⚠️ Rule:** Only one Expedite item should be in flight at a time. If everything is Expedite, nothing is.

---

## Cadences

Kanban recommends seven cadences (regular meetings). Not all are required at every team level.

| Cadence | Frequency | Purpose |
|---------|-----------|---------|
| **Strategy Review** | Quarterly | Is the service still fit for purpose? Adjust policies and goals. |
| **Operations Review** | Monthly | Review flow metrics across services. Address systemic issues. |
| **Risk Review** | Monthly | Identify and manage delivery risks. |
| **Service Delivery Review** | Bi-weekly | Review service performance with stakeholders. |
| **Replenishment Meeting** | Weekly | Pull items from the backlog into "Ready". Prioritise by CoS. |
| **Kanban Meeting** | Daily | Walk the board right-to-left. Identify blockers. 15 minutes. |
| **Delivery Planning** | On demand | Coordinate release or deployment decisions. |

**The Kanban Meeting (daily stand-up equivalent):**
```
Walk the board right-to-left (from Done back to Backlog)
Focus on:
→ What is blocked?
→ What is at risk of breaching its SLA?
→ Are any WIP limits being violated?
```

---

## Flow Metrics

Kanban teams rely on flow metrics rather than velocity or story points.

| Metric | Formula | Use |
|--------|---------|-----|
| **Cycle Time** | Done Date − Start Date | How long individual items take |
| **Lead Time** | Done Date − Request Date | Customer experience of wait |
| **Throughput** | Items completed / time period | Team delivery rate |
| **WIP** | Items in progress at any moment | System load |
| **Flow Efficiency** | Active Time / Lead Time × 100% | % of time item is being worked on |

**Flow Efficiency benchmark:**
```
Flow Efficiency = Active Time / Lead Time × 100%

Most teams: 15–40%
High-performing teams: 40%+
< 15% = significant queue/wait time problem
```

**Cumulative Flow Diagram (CFD):**
The primary visual tool for Kanban health. A widening band = bottleneck forming. Parallel bands = healthy flow.

```
Little's Law: WIP = Throughput × Cycle Time

If WIP is high and throughput is unchanged → Cycle Time rises
Reduce WIP → Cycle Time falls
```

---

## Kanban vs Scrum

| Dimension | Kanban | Scrum |
|-----------|--------|-------|
| Cadence | Continuous flow | Fixed-length Sprints |
| Roles | No prescribed roles | Product Owner, Scrum Master, Developers |
| Change | Anytime | Between Sprints |
| WIP limits | Explicit, per column | Implicit (sprint capacity) |
| Estimation | Optional | Usually required (story points) |
| Board | Persistent, evolving | Reset each Sprint |
| Best for | Operational/support work, continuous delivery | Product development with clear goals |

**Can you use both?** Yes — Scrumban combines Sprint cadences with Kanban WIP limits and flow metrics. Common in teams transitioning from Scrum to flow-based delivery.

---

## Anti-Patterns

| Anti-Pattern | Problem | Fix |
|---|---|---|
| WIP limits as decoration | Team ignores limits when convenient | Limits are rules; violations must be discussed and resolved |
| No explicit policies | Decisions made inconsistently | Write down entry/exit criteria for every column |
| Backlog as a dumping ground | Everything goes in; nothing gets removed | Regularly prune and reprioritise; apply CoS |
| Everything is Expedite | Priorities are meaningless | Only one Expedite item at a time |
| Measuring utilisation over flow | Keeping people busy ≠ delivering value | Optimise for cycle time and throughput, not 100% busyness |
| Skipping the Kanban meeting | Blockers go unnoticed for days | Daily walk-the-board is non-negotiable |
| Too many columns | Board is complex; no one understands it | Start with 4–5 columns; add only when a real need emerges |
| No CFD or flow metrics | Team has no visibility into systemic issues | Track cycle time, throughput, and WIP weekly |

---

## Kanban Cheat Sheet

```
# Core Practices
1. Visualise the workflow
2. Limit WIP
3. Manage flow
4. Make policies explicit
5. Implement feedback loops
6. Improve collaboratively

# Key Metrics
Lead Time       = Done Date − Request Date
Cycle Time      = Done Date − Start Date
Throughput      = Items Done / Time Period
Flow Efficiency = Active Time / Lead Time × 100%
Little's Law    = WIP = Throughput × Cycle Time

# Classes of Service (priority order)
Expedite → Fixed Date → Standard → Intangible

# WIP Limit Starting Point
Team size × 1.5 per active workflow stage

# Kanban Meeting Format
Walk board right-to-left · 15 minutes
Focus: blockers · SLA risks · WIP violations
```

---

## Contributing

Contributions are welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md) before submitting a PR.

Areas where we'd love help:
- 📝 Additional CoS examples by industry
- 📊 CFD and flow metric templates in `/docs/templates/`
- 🌍 Translations
- 🔗 Tool comparisons (Jira, Trello, Linear, Azure DevOps)

---

## License

[Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE) © 2026 sathishkumaralagiri

You are free to share and adapt this material for any purpose, even commercially, as long as you give appropriate credit.
