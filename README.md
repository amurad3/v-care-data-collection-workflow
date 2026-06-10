# V-CARE Data Collection Workflow Practice

A lightweight JIRA Kanban project that tracks **data collection sessions** from
preparation to completion: device readiness, participant/session setup, scenario
execution, data validation, issue logging, and final QA review.

This repository is a file-based representation of the JIRA project so it can live
on GitHub. It includes:

- A readable [Kanban board](board.md) showing where each ticket sits.
- One file per ticket under [`tickets/`](tickets/) with description and acceptance criteria.
- A [`jira-import.csv`](jira-import.csv) you can load directly into JIRA to create the real board.

---

## Purpose

Track each data collection session through clear stages so that work is visible,
issues are documented, and nothing reaches "Done" without passing quality control.

## Board columns (simple Kanban)

| Column | Meaning |
| --- | --- |
| **Backlog** | Tasks that need to be done. |
| **Ready for Session** | Tasks prepared and ready to execute. |
| **In Progress** | Active data collection or testing work. |
| **Blocked / Issue Found** | Delayed by a device issue, missing info, unclear instructions, or data problem. |
| **QA Review** | Data has been collected and needs validation. |
| **Done** | Completed and documented. |

See the current snapshot in [board.md](board.md).

## Issue types used

- **Task** — standard work item in the session workflow.
- **Bug** — something broke (e.g., a device issue) during a session.
- **Improvement** — a suggested change to the protocol or process.

---

## How this maps to the Amazon role

This workflow mirrors the day-to-day of a data collection / data technician role:

- **Prototype device readiness** — charge, update, label, verify build and login.
- **Scenario-driven data collection** — run scripted scenarios, record timestamps and observations.
- **Issue logging** — capture device failures with repro steps and data-usability impact.
- **Data validation & QA** — check fields, naming conventions, folder structure before closing.
- **Process feedback** — suggest protocol improvements based on what happened in the session.

The point is to show the core competency: **track tasks, document issues, move work
through stages, and support quality control.**

---

## Create the real JIRA project from this repo

1. In JIRA, create a project named **V-CARE Data Collection Workflow Practice** (Kanban template).
2. Rename the board columns to match the six columns above.
3. Go to **Filters → Import issues from CSV** (or Project settings → Import).
4. Upload [`jira-import.csv`](jira-import.csv) and map the columns
   (Summary, Issue Type, Description, Priority, Status, Labels).
5. Confirm — the 10 tickets land in the correct columns via the **Status** field.

> Note: column names in JIRA are mapped to statuses. If your JIRA uses default
> statuses, map "Ready for Session", "Blocked / Issue Found", and "QA Review" to
> the matching custom statuses (or the nearest default) during import.
