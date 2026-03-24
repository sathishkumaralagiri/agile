# 🏃 agile / agile-scrum

> Part of the [`agile`](../) reference library. A complete practitioner's guide to the Scrum framework — roles, events, artifacts, values, and anti-patterns.

**Live site:** `sathishkumaralagiri.github.io/agile/agile-scrum/`

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightblue.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Stars](https://img.shields.io/github/stars/sathishkumaralagiri/agile?style=social)](.)

---

## Table of Contents

- [Overview](#overview)
- [The Scrum Values](#the-scrum-values)
- [Roles](#roles)
  - [Product Owner](#product-owner)
  - [Scrum Master](#scrum-master)
  - [Developers](#developers)
- [Events](#events)
  - [The Sprint](#the-sprint)
  - [Sprint Planning](#sprint-planning)
  - [Daily Scrum](#daily-scrum)
  - [Sprint Review](#sprint-review)
  - [Sprint Retrospective](#sprint-retrospective)
- [Artifacts](#artifacts)
  - [Product Backlog](#product-backlog)
  - [Sprint Backlog](#sprint-backlog)
  - [Increment](#increment)
- [Definition of Done](#definition-of-done)
- [Anti-Patterns](#anti-patterns)
- [Scrum Cheat Sheet](#scrum-cheat-sheet)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

Scrum is a lightweight framework for developing and sustaining complex products. It is intentionally incomplete — it defines only the parts required to implement Scrum theory, leaving the rest for teams to figure out.

**Three pillars of empiricism:**
- **Transparency** — the process and work must be visible to those performing and receiving the work
- **Inspection** — Scrum artifacts and progress must be inspected frequently to detect undesirable variances
- **Adaptation** — if any aspect deviates outside acceptable limits, the process must be adjusted

---

## The Scrum Values

| Value | What it means in practice |
|-------|--------------------------|
| **Commitment** | Team members commit to achieving team goals and supporting each other |
| **Courage** | Do the right thing and work on tough problems |
| **Focus** | Everyone focuses on Sprint work and the goals of the Scrum Team |
| **Openness** | Be open about all work and challenges |
| **Respect** | Respect each other as capable, independent people |

> These values give direction to Scrum Team work, actions, and behaviour. Without them, Scrum is just a set of meetings.

---

## Roles

### Product Owner

**Accountable for:** maximising the value of the product resulting from the work of the Scrum Team.

**Key responsibilities:**
- Developing and explicitly communicating the **Product Goal**
- Creating and clearly expressing **Product Backlog items**
- **Ordering** the Product Backlog items
- Ensuring the Product Backlog is **transparent, visible, and understood**

**One person, not a committee.** The Product Owner may represent the needs of many stakeholders but must be a single individual. Decisions are respected — if someone wants to change priorities, they must convince the Product Owner.

**⚠️ Anti-pattern:** A Product Owner who is not empowered to make backlog decisions creates confusion and delays. If a committee overrides the PO, Scrum breaks down.

---

### Scrum Master

**Accountable for:** establishing Scrum as defined in the Scrum Guide, and the Scrum Team's effectiveness.

**Serves the Scrum Team by:**
- Coaching team members in self-management and cross-functionality
- Helping the team focus on creating high-value Increments that meet the Definition of Done
- Removing impediments to progress
- Ensuring all Scrum events take place and are positive and productive

**Serves the Product Owner by:**
- Helping find techniques for effective Product Goal definition and backlog management
- Helping establish empirical product planning for complex environments
- Facilitating stakeholder collaboration as requested or needed

**Serves the Organisation by:**
- Leading, training, and coaching the organisation in Scrum adoption
- Planning and advising Scrum implementations
- Helping stakeholders understand and enact empirical product development

**⚠️ Anti-pattern:** The Scrum Master as a project manager or taskmaster. The SM is a servant-leader, not a boss. Assigning tasks or tracking individual velocity destroys the role.

---

### Developers

**Accountable for:** creating a usable Increment every Sprint.

**Responsibilities:**
- Creating a plan for the Sprint — the **Sprint Backlog**
- Instilling quality by adhering to the **Definition of Done**
- Adapting the plan daily toward the Sprint Goal
- Holding each other accountable as professionals

The term "Developers" refers to anyone on the Scrum Team who is committed to creating any aspect of a usable Increment each Sprint — testers, designers, and analysts included.

**⚠️ Anti-pattern:** Developers waiting to be told what to do. A self-managing Scrum Team decides internally who does what, when, and how.

---

## Events

All events in Scrum are opportunities to inspect and adapt. They are designed to enable transparency and are formal events — skipping or shortening them without intent undermines the framework.

### The Sprint

**Timebox:** 1–4 weeks (fixed length for the duration of a project)

The Sprint is the heartbeat of Scrum. A new Sprint starts immediately after the conclusion of the previous one.

**During a Sprint:**
- No changes are made that would endanger the Sprint Goal
- Quality does not decrease
- The Product Backlog is refined as needed
- Scope may be clarified and renegotiated with the Product Owner

**Cancelling a Sprint:** Only the Product Owner can cancel a Sprint. This happens when the Sprint Goal becomes obsolete. Sprint cancellation is rare and traumatic to the team — avoid unless genuinely necessary.

---

### Sprint Planning

**Timebox:** max 8 hours for a 4-week Sprint (proportionally shorter for shorter Sprints)

**Three topics addressed:**

1. **Why is this Sprint valuable?** — the Product Owner proposes how the Sprint increases value. The team crafts a Sprint Goal.
2. **What can be Done this Sprint?** — Developers select items from the Product Backlog to include in the Sprint Backlog.
3. **How will the work get done?** — Developers plan the work needed to create an Increment that meets the Definition of Done.

**Output:** Sprint Goal + Sprint Backlog

---

### Daily Scrum

**Timebox:** 15 minutes, same time and place each day

**Purpose:** inspect progress toward the Sprint Goal and adapt the Sprint Backlog as necessary.

The Daily Scrum is for Developers. The Scrum Master ensures it happens but does not run it. The Product Owner and Scrum Master participate as Developers if they are working on Sprint Backlog items.

**Common format (not mandatory):**
```
- What did I do yesterday that helped the team meet the Sprint Goal?
- What will I do today to help the team meet the Sprint Goal?
- Do I see any impediments that prevent me or the team from meeting the Sprint Goal?
```

**⚠️ Anti-pattern:** The Daily Scrum as a status update to management. It is a planning event for Developers. Managers attending and asking questions disrupts the purpose entirely.

---

### Sprint Review

**Timebox:** max 4 hours for a 4-week Sprint

**Purpose:** inspect the outcome of the Sprint and determine future adaptations.

The Scrum Team presents the results of their work to key stakeholders and progress toward the Product Goal is discussed. The Product Backlog may be adjusted in response.

**This is NOT a demo.** It is a working session where the whole Scrum Team and stakeholders collaborate on what was done and what to do next.

**Attendees:** Scrum Team + key stakeholders invited by the Product Owner

---

### Sprint Retrospective

**Timebox:** max 3 hours for a 4-week Sprint

**Purpose:** plan ways to increase quality and effectiveness.

The Scrum Team inspects how the last Sprint went with regard to individuals, interactions, processes, tools, and the Definition of Done.

**Three questions to explore:**
1. What went well?
2. What problems were encountered?
3. How can we improve?

**Output:** actionable improvements to be enacted in the next Sprint.

**⚠️ Anti-pattern:** A retrospective that produces a long list of issues but no committed actions. Every retro should end with 1–3 specific, owned improvement items added to the next Sprint Backlog.

---

## Artifacts

Each artifact contains a **commitment** — a mechanism to reinforce empiricism and the Scrum values.

### Product Backlog

**Commitment: Product Goal**

An ordered list of everything that is known to be needed in the product. It is the single source of work for the Scrum Team. The Product Owner is responsible for it.

**Characteristics of good backlog items (INVEST):**
```
I — Independent   (can be developed without depending on another item)
N — Negotiable    (not a fixed contract; details can change)
V — Valuable      (delivers value to the user or business)
E — Estimable     (team can estimate the effort)
S — Small         (fits within a single Sprint)
T — Testable      (acceptance criteria can be defined)
```

**Backlog Refinement:** an ongoing activity (not an event) where backlog items are broken down and defined. Typically consumes no more than 10% of the Developers' capacity.

---

### Sprint Backlog

**Commitment: Sprint Goal**

Composed of:
1. The **Sprint Goal** (the why)
2. The set of **Product Backlog items** selected for the Sprint (the what)
3. An **actionable plan** for delivering the Increment (the how)

The Sprint Backlog is a plan by and for the Developers. It is updated throughout the Sprint as more is learned.

---

### Increment

**Commitment: Definition of Done**

An Increment is a concrete stepping stone toward the Product Goal. Each Increment is additive to all prior Increments and must be usable.

Multiple Increments may be created within a Sprint. The sum of the Increments is presented at the Sprint Review.

**An Increment must meet the Definition of Done to be presented at the Sprint Review.**

---

## Definition of Done

The Definition of Done (DoD) is a formal description of the state of the Increment when it meets the quality measures required for the product.

**Example DoD:**
- Code reviewed by at least one other Developer
- Unit tests written and passing
- Integration tests passing
- No known critical bugs
- Feature flagged if not ready for release
- Documentation updated
- Deployed to staging environment

**⚠️ Important:** If a Product Backlog item does not meet the DoD, it cannot be released or presented at the Sprint Review. It returns to the Product Backlog.

---

## Anti-Patterns

| Anti-Pattern | Problem | Fix |
|---|---|---|
| Scrum Master as project manager | Assigns tasks, tracks individuals, reports to management | SM is a servant-leader; team self-manages |
| Product Owner by committee | No one can make a decision; priorities conflict | One empowered PO owns the backlog |
| Sprint as a mini-waterfall | Design sprint → dev sprint → test sprint | Each Sprint must produce a potentially shippable Increment |
| No Sprint Goal | Team just works through a list with no unifying objective | Every Sprint must have a clear, meaningful goal |
| Skipping the Retrospective | No opportunity for process improvement | Retro is non-negotiable; improvements go into next Sprint |
| Daily Scrum as status meeting | Developers report to managers instead of coordinating with each other | It's a planning event for Developers only |
| Backlog refinement ignored | Sprint Planning becomes a discovery session and overruns | Refine continuously; items must be ready before Sprint Planning |
| DoD ignored under pressure | Incomplete work declared Done to hit velocity targets | DoD is non-negotiable; undone work creates technical debt |
| Extending Sprints | Sprint extended because work isn't done | Fixed timebox; unfinished items return to backlog |

---

## Scrum Cheat Sheet

```
# Roles
Product Owner   → maximises product value; owns the backlog
Scrum Master    → serves the team; removes impediments; coaches Scrum
Developers      → create the Increment; self-managing

# Events & Timeboxes (4-week Sprint)
Sprint          → 1–4 weeks, fixed length
Sprint Planning → max 8 hours
Daily Scrum     → 15 minutes, every day
Sprint Review   → max 4 hours
Retrospective   → max 3 hours

# Artifacts & Commitments
Product Backlog → commitment: Product Goal
Sprint Backlog  → commitment: Sprint Goal
Increment       → commitment: Definition of Done

# Scrum Values
Commitment · Courage · Focus · Openness · Respect

# Three Pillars
Transparency · Inspection · Adaptation
```

---

## Contributing

Contributions are welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md) before submitting a PR.

Areas where we'd love help:
- 📝 Additional anti-pattern examples
- 📋 Facilitation templates in `/docs/templates/`
- 🌍 Translations
- 🔗 Tool comparisons (Jira, Linear, Azure DevOps)

---

## License

[Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE) © 2026 sathishkumaralagiri

You are free to share and adapt this material for any purpose, even commercially, as long as you give appropriate credit.
