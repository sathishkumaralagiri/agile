# 🎭 agile / agile-ceremonies

> Part of the [`agile`](../) reference library. Facilitation guides and templates for every Agile ceremony — sprint planning, daily standups, reviews, retrospectives, backlog refinement, and more.

**Live site:** `sathishkumaralagiri.github.io/agile/agile-ceremonies/`

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightblue.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Stars](https://img.shields.io/github/stars/sathishkumaralagiri/agile?style=social)](.)

---

## Table of Contents

- [Overview](#overview)
- [Ceremonies at a Glance](#ceremonies-at-a-glance)
- [Sprint Planning](#sprint-planning)
- [Daily Standup](#daily-standup)
- [Backlog Refinement](#backlog-refinement)
- [Sprint Review](#sprint-review)
- [Sprint Retrospective](#sprint-retrospective)
- [Facilitation Tips](#facilitation-tips)
- [Templates](#templates)
- [Anti-Patterns](#anti-patterns)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

Agile ceremonies are the structured touchpoints that keep a team aligned, unblocked, and improving. Done well, they are short, purposeful, and energising. Done poorly, they are the meetings people dread.

This guide covers:
- **Purpose** — why each ceremony exists
- **Timebox** — maximum duration
- **Who attends** — and who facilitates
- **Agenda** — a practical run-of-show
- **Facilitation techniques** — tools to make each session effective
- **Templates** — ready-to-use formats in `/docs/templates/`

---

## Ceremonies at a Glance

| Ceremony | Timebox | Cadence | Facilitator | Output |
|----------|---------|---------|-------------|--------|
| Sprint Planning | 2 hrs / week of Sprint | Start of Sprint | Scrum Master | Sprint Goal + Sprint Backlog |
| Daily Standup | 15 min | Daily | Team (rotating) | Updated plan for the day |
| Backlog Refinement | 1 hr | Mid-Sprint (weekly) | Product Owner + SM | Refined, estimated backlog items |
| Sprint Review | 1 hr / week of Sprint | End of Sprint | Product Owner | Updated Product Backlog |
| Sprint Retrospective | 45 min / week of Sprint | End of Sprint | Scrum Master | 1–3 improvement actions |

---

## Sprint Planning

**Purpose:** Set the Sprint Goal and select the work the team will commit to for the Sprint.

**Timebox:** 2 hours per week of Sprint length (e.g. 4-hour cap for a 2-week Sprint, 8-hour cap for a 4-week Sprint)

**Attendees:** Entire Scrum Team

### Agenda

```
Part 1 — Why (30 min)
  Product Owner presents the top priorities
  Team and PO agree on the Sprint Goal

Part 2 — What (45 min)
  Developers select Product Backlog items
  Validate that selected items meet the Definition of Ready
  Confirm capacity (holidays, leave, known interruptions)

Part 3 — How (45 min)
  Developers break selected items into tasks
  Estimate tasks if needed
  Confirm the plan is achievable within the Sprint
```

### Definition of Ready checklist

Before an item can be pulled into Sprint Planning, it should meet:

- [ ] User story is written and understood by the team
- [ ] Acceptance criteria are defined and agreed
- [ ] Dependencies identified and resolved (or plan in place)
- [ ] Sized/estimated by the team
- [ ] UI/UX designs available (if applicable)
- [ ] Test approach agreed

### Facilitation techniques

**Capacity planning:**
```
Available capacity = (team size × sprint days) - (leave days + ceremonies + overhead)
Target commitment  = available capacity × 0.75–0.80
```

**Sprint Goal format:**
```
We will [achieve outcome] by [delivering what] so that [stakeholder benefit].

Example:
"We will reduce checkout abandonment by delivering the saved cart feature
so that returning users can complete purchases without re-entering items."
```

---

## Daily Standup

**Purpose:** Inspect progress toward the Sprint Goal and adapt the day's plan.

**Timebox:** 15 minutes

**Attendees:** Developers (Scrum Master + Product Owner optional unless working on Sprint items)

**Format (three questions):**
```
1. What did I complete yesterday toward the Sprint Goal?
2. What will I work on today toward the Sprint Goal?
3. Is anything blocking me?
```

### Facilitation techniques

**Walk the board:** Instead of going person-by-person, walk the board right-to-left (from Done to In Progress to To Do). Focus on the work, not the people.

**Parking lot:** Keep a visible "parking lot" for topics that need deeper discussion. If something comes up that needs > 2 min, note it and continue — handle it after standup with only the relevant people.

**Timekeeper rotation:** Rotate who facilitates weekly. Shared ownership prevents it from becoming a status update to one person.

**⚠️ Anti-pattern:** Running the standup as a status report to the Scrum Master or manager. The team is coordinating with each other, not reporting upward.

---

## Backlog Refinement

**Purpose:** Ensure the backlog is ready — items are well-understood, sized, and ordered before they reach Sprint Planning.

**Timebox:** No more than 10% of the Sprint capacity (e.g. ~4 hours for a 2-week Sprint, split across 1–2 sessions)

**Attendees:** Product Owner + Developers (Scrum Master facilitates)

### Agenda

```
1. Review newly added items (10 min)
   PO explains new items; team asks clarifying questions

2. Refinement of upcoming items (35 min)
   Walk through top items in priority order
   Discuss, split if needed, estimate

3. Acceptance criteria review (10 min)
   Ensure ACs are testable and complete

4. Prioritisation check (5 min)
   PO confirms order is still correct given any new information
```

### Story splitting patterns

| Pattern | Example |
|---------|---------|
| By workflow step | "User registers" → "User enters details" + "User verifies email" |
| By user role | "Admin exports data" + "User exports data" |
| By data type | "Search by name" + "Search by email" + "Search by date" |
| By happy/unhappy path | "Login succeeds" + "Login fails (wrong password)" |
| By CRUD | "View report" + "Edit report" + "Delete report" |
| By spike | "Research payment providers" + "Implement chosen provider" |

### Estimation techniques reference

See [`agile-metrics`](../agile-metrics/) for full details on:
- Planning Poker
- T-shirt sizing
- Three-point / PERT estimation
- Monte Carlo simulation

---

## Sprint Review

**Purpose:** Inspect the Increment and adapt the Product Backlog based on what was learned.

**Timebox:** 1 hour per week of Sprint length (e.g. 2-hour cap for a 2-week Sprint)

**Attendees:** Scrum Team + key stakeholders (invited by Product Owner)

### Agenda

```
1. Context setting (5 min)
   Scrum Master: Sprint Goal recap, what was planned vs completed

2. Increment showcase (40 min)
   Developers demonstrate completed work against acceptance criteria
   Stakeholders interact with the working software
   Questions and discussion throughout — not at the end

3. Product Backlog update (10 min)
   Product Owner reviews what's next
   Stakeholders suggest adjustments based on what they saw

4. Wrap-up (5 min)
   Key decisions noted
   Next Sprint goal previewed if known
```

### Facilitation techniques

**Working software only:** Only items that meet the Definition of Done are shown. Do not demo incomplete work — it sets false expectations.

**Invite interaction:** Rather than presenting slides, let stakeholders click through the actual product. Real interaction reveals real feedback.

**Capture feedback live:** Have a shared document or digital board visible to everyone. Write feedback as it's given — don't rely on memory.

**⚠️ Anti-pattern:** The Sprint Review as a one-way presentation. It should be a conversation, not a PowerPoint show.

---

## Sprint Retrospective

**Purpose:** Inspect how the last Sprint went and identify one or more improvements to enact next Sprint.

**Timebox:** 45 minutes per week of Sprint length (e.g. 90-minute cap for a 2-week Sprint)

**Attendees:** Scrum Team only (no external stakeholders)

### Retrospective formats

#### Format 1 — Start / Stop / Continue

Simple and effective for most teams.

```
Start   → What should we start doing that we haven't tried?
Stop    → What should we stop doing that isn't helping?
Continue → What's working well that we should keep doing?
```

#### Format 2 — 4Ls

Good for surfacing feelings alongside facts.

```
Liked    → What did you enjoy or appreciate?
Learned  → What did you learn?
Lacked   → What was missing or could have been better?
Longed for → What did you wish had existed?
```

#### Format 3 — Sailboat / Speedboat

Visual metaphor. Draw a boat with wind (helping forces), anchors (things slowing us down), rocks (risks ahead), and the island (the goal).

```
Wind (Propellers)  → What's helping us go faster?
Anchors            → What's slowing us down?
Rocks              → What risks are ahead?
Island             → What's the goal we're sailing toward?
```

#### Format 4 — Mad / Sad / Glad

Good for emotionally honest retrospectives or after difficult Sprints.

```
Mad  → What frustrated you?
Sad  → What disappointed you?
Glad → What made you happy or proud?
```

### Facilitation flow

```
1. Set the stage (5 min)
   Check-in question: "In one word, how was this Sprint?"
   Remind the team: this is a safe space; we improve the system, not blame people.

2. Gather data (15 min)
   Silent sticky note writing (3–5 min)
   Read out and group similar themes

3. Generate insights (15 min)
   Dot voting on top themes (each person gets 3–5 votes)
   Discuss the top 2–3 themes in depth

4. Decide what to do (10 min)
   Pick 1–3 specific, actionable improvements
   Assign an owner and a target date for each

5. Close (5 min)
   Retro feedback: "One word for how this retro felt"
   Confirm improvements will be added to next Sprint Backlog
```

### Improvement action template

```
Improvement: [clear description of what will change]
Owner:       [name of the person responsible]
Success looks like: [how we'll know it worked]
Review at:   [date or next retro]
```

**⚠️ Anti-pattern:** A retro that produces a list of issues but no committed actions. Every retro should end with 1–3 specific, owned improvement items added to the Sprint Backlog.

---

## Facilitation Tips

### General

- **Start on time, end on time.** Respect the timebox — it signals that meetings are efficient and worthwhile.
- **Psychological safety first.** Establish team agreements at the start of any retrospective: what's said in the room stays in the room.
- **Make it visual.** Use a physical or digital board. Sticky notes, dot votes, and visible outputs keep people engaged.
- **Silent writing before discussion.** Give people 3–5 minutes to write ideas silently before opening to discussion. This prevents the loudest voice dominating.
- **Parking lot.** Keep a visible space for off-topic topics — acknowledge them and move on.

### Remote facilitation

| Tool | Best for |
|------|---------|
| Miro / Mural | Visual boards, retrospectives, mapping |
| FigJam | Collaborative whiteboarding |
| EasyRetro | Dedicated retro format with voting |
| PlanningPoker.com | Estimation sessions |
| Zoom / Teams | Video with breakout rooms for group work |

### Energy management

- Short ceremonies (Daily, Retro) → first thing in the morning
- Longer ceremonies (Planning, Review) → after a break, not at end of day
- Rotate facilitation → prevents meeting fatigue and grows facilitation skills across the team

---

## Templates

Ready-to-use templates are in `/docs/templates/`:

| Template | File | Format |
|----------|------|--------|
| Sprint Planning agenda | `sprint-planning-agenda.md` | Markdown |
| Definition of Ready checklist | `definition-of-ready.md` | Markdown |
| Sprint Goal canvas | `sprint-goal-canvas.md` | Markdown |
| Retrospective: Start/Stop/Continue | `retro-start-stop-continue.md` | Markdown |
| Retrospective: 4Ls | `retro-4ls.md` | Markdown |
| Retrospective: Sailboat | `retro-sailboat.md` | Markdown |
| Improvement action tracker | `improvement-tracker.md` | Markdown |

---

## Anti-Patterns

| Ceremony | Anti-Pattern | Fix |
|----------|-------------|-----|
| Sprint Planning | No Sprint Goal defined | Spend the first 30 min agreeing the goal before selecting items |
| Sprint Planning | Over-committing capacity | Target 75–80% of available capacity; leave buffer |
| Daily Standup | Status update to manager | Walk the board; team coordinates with team |
| Daily Standup | Running over 15 min | Park all discussions; use a parking lot |
| Backlog Refinement | Skipped until Sprint Planning | Refine weekly; items must be Ready before Planning |
| Backlog Refinement | Estimating without understanding | Clarify before estimating; use "?" as a valid answer |
| Sprint Review | PowerPoint presentation | Show working software; invite interaction |
| Sprint Review | Only developers attend | Stakeholders must be present to give feedback |
| Retrospective | No actions committed | Every retro ends with 1–3 owned actions in the next Sprint |
| Retrospective | Same format every time | Rotate formats to keep energy and honesty fresh |
| All ceremonies | Run by one person always | Rotate facilitation; it builds team ownership |

---

## Contributing

Contributions are welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md) before submitting a PR.

Areas where we'd love help:
- 📝 New retrospective formats
- 📋 Template additions in `/docs/templates/`
- 🌍 Translations
- 🔗 Remote facilitation tool comparisons

---

## License

[Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE) © 2026 sathishkumaralagiri

You are free to share and adapt this material for any purpose, even commercially, as long as you give appropriate credit.
