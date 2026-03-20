# Monte Carlo Simulation — Worked Example

## Scenario

Your team is building a new checkout feature. The backlog has **40 stories** remaining. You want to know: *when will we be done?*

## Step 1 — Gather Historical Throughput

Collect completed items per sprint (last 10 sprints):

| Sprint | Items Completed |
|--------|----------------|
| S-1 | 7 |
| S-2 | 5 |
| S-3 | 9 |
| S-4 | 6 |
| S-5 | 8 |
| S-6 | 4 |
| S-7 | 7 |
| S-8 | 10 |
| S-9 | 6 |
| S-10 | 8 |

**Range:** 4–10 items/sprint  
**Average:** 7 items/sprint  

## Step 2 — Run Simulations

For each simulation:
1. Pick a random throughput value from the historical set
2. Subtract from remaining work
3. Repeat until work reaches 0
4. Record number of sprints needed

Run this **10,000 times**.

## Step 3 — Read the Results

| Confidence | Sprints Needed | Approx Date (2-week sprints) |
|---|---|---|
| 50% | 6 sprints | ~12 weeks |
| 75% | 7 sprints | ~14 weeks |
| 85% | 8 sprints | ~16 weeks |
| 95% | 9 sprints | ~18 weeks |

## Step 4 — Communicate

> "Based on our historical pace, we have an **85% confidence** the feature will be complete within **16 weeks**. There's a 50/50 chance we finish by week 12."

This is far more honest than "we'll be done in 12 weeks" with no uncertainty communicated.

## Spreadsheet Template

A ready-to-use Google Sheets Monte Carlo template is available in this repo: `docs/templates/monte-carlo.xlsx`

## Further Reading

- [Probabilistic Forecasting by Troy Magennis](https://www.focusedobjective.com)
- [Actionable Agile Metrics for Predictability — Daniel Vacanti](https://actionableagile.com)
- Little's Law: https://en.wikipedia.org/wiki/Little%27s_law
