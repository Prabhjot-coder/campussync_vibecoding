# Campus Daybook (prompt-first / vibe-coded)

This app was built from a single prompt, with no proposal or spec, for Step 1 of the spec-driven development exercise (BITS Pilani WILP, STL ZG502, Immersion I):

> Create a web application for college students to manage their daily schedules.

It exists for comparison with the spec-driven version, **CampusSync** ([Prabhjot-coder/campussync](https://github.com/Prabhjot-coder/campussync)), which was built only from an approved `spec.md` (REQ-01 to REQ-09).

## What the AI built
- Day and week timelines from 7 AM to 11 PM, with a "now" line
- Schedule items of seven types (class, lab, study, exam, work, event, personal) that repeat weekly or happen once
- Overlap warnings when two items clash
- A "day at a glance" panel: what's now or next, hours in class, studying and working, free time and the longest free stretch
- An assignment list grouped into overdue, today, the next 7 days and later, with priorities and quick add
- An example week shown on first open

## Assumptions the AI made on its own (worksheet section 1)

| # | Assumption | Would the team have chosen it? | Why |
|---|---|---|---|
| 1.2 | Students sign in and each schedule is saved to their account, synced across devices (browser storage only as a fallback) | No | The agreed scope is no login and no backend |
| 1.3 | Extra planner features: weekly repeating classes, 7 item types, week view, free-time totals, overlap warnings, assignment priorities | Partly | Overlap warnings and due dates fit the problem; the rest is scope nobody asked for |
| 1.4 | Defaults nobody asked for: a made-up example week, a 7 AM to 11 PM day, weeks starting Monday, 12-hour clock | Not now | The Product Owner should set defaults; fake data can confuse real users |

## Storage in this copy
Account sync only works when the page runs as a Claude artifact. Hosted here, it saves to the browser's `localStorage`, so data stays on one device and one browser.

## Run locally
Open `index.html` in any browser. There is no build step.
