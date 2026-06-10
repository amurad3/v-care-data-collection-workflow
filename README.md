# V-CARE Data Collection Workflow Practice

A lightweight JIRA Kanban project that tracks **data collection sessions** from
preparation to completion: device readiness, participant/session setup, scenario
execution, data validation, issue logging, and final QA review.

> **Live JIRA board:** this project is also built as a real Kanban board on JIRA
> Cloud — **[Open the V-CARE Kanban board ↗](https://athirmurad2.atlassian.net/jira/software/projects/VCDCWP/boards/3)**
> (project key `VCDCWP`), with all 10 tickets placed across the six columns.
> *(Sign-in required — the board is on the owner's personal Atlassian site.)*

This repository is a file-based representation of the JIRA project so it can live
on GitHub. It includes:

- A readable [Kanban board](board.md) showing where each ticket sits.
- One file per ticket under [`tickets/`](tickets/) with description and acceptance criteria.
- A [`jira-import.csv`](jira-import.csv) to recreate the same board in any other JIRA instance.

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

## What this project demonstrates

The goal is to model a real, repeatable process as a clean Kanban workflow and use
JIRA the way a team actually does. Concepts shown here:

| JIRA / Kanban concept | How it's used in this board |
| --- | --- |
| **Workflow as columns** | Work flows left → right through clearly defined stages, so anyone can see status at a glance. |
| **Issue types** | The right type for the job — **Task** for standard work, **Bug** for a failure (VCDC-4), **Improvement** for a process suggestion (VCDC-7). |
| **Acceptance criteria** | Every ticket has an explicit, checkable definition of done — no ambiguity about when work is complete. |
| **Surfacing blockers** | A dedicated **Blocked / Issue Found** column makes impediments visible instead of letting them stall silently. |
| **Quality gate** | Nothing reaches **Done** without passing through **QA Review** and a final validation step (VCDC-8). |
| **Prioritization & labels** | Priorities and labels (`device`, `qa`, `data-validation`, …) keep the backlog organized and filterable. |
| **Continuous improvement** | Lessons from a session feed back as Improvement tickets, closing the loop on the process itself. |

The core competency on display: **track work, document issues, move it through
defined stages, and gate quality before anything is called done.**

*Context: the sample tickets follow a hardware/data-collection session (device prep,
scenario-driven collection, validation, QA) to keep the example concrete and realistic.*

---

## Recreate this board elsewhere

The live board already exists (link at the top). To rebuild it in a different JIRA
instance, import [`jira-import.csv`](jira-import.csv) — see
[IMPORT_TO_JIRA.md](IMPORT_TO_JIRA.md) for the step-by-step guide.
