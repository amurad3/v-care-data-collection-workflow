# V-CARE Data Collection Workflow Practice

A lightweight JIRA Kanban project that tracks **data collection sessions** from
preparation to completion: device readiness, participant/session setup, scenario
execution, data validation, issue logging, and final QA review.

> **Live JIRA board:** this project is also built as a real Kanban board on JIRA
> Cloud — project **V-CARE Data Collection Workflow Practice** (key `VCDCWP`) on
> `athirmurad2.atlassian.net`, with all 10 tickets placed across the six columns.

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

## How this maps to the Amazon Data Collection Specialist role

This board is built to demonstrate the exact responsibilities and qualifications in
the job description. Each JD requirement maps to a ticket or workflow stage:

| Job description language | Where it shows up in this board |
| --- | --- |
| *Execute the collection procedure accurately, record data* | **VCDC-3** Run scenario-driven data collection — scripted steps, timestamps, observations |
| *Document any needed information associated to data* | **VCDC-6** Audit session notes; checkbox acceptance criteria on every ticket |
| *Scenario-driven data collection* (preferred qual) | **VCDC-3**, modeled as a scripted scenario with per-step tracking |
| *Experience working with prototype assets* / *device flashing and readiness* | **VCDC-1** Prepare prototype device; **VCDC-9** Stage backup device (build install, login, device ID) |
| *Data auditing / data markup* | **VCDC-5** Validate collected data file; **VCDC-6** Audit completed session notes |
| *Hardware and software testing* | **VCDC-4** Log device issue (Bug) — repro steps, impact, data usability |
| *Proactive behavior in addressing issues and problems* | **Blocked / Issue Found** column + Bug workflow so problems are surfaced, not buried |
| *Contribute to improvements... identifying issues in tools and suggesting enhancements* | **VCDC-7** Update collection protocol suggestion (Improvement type) |
| *Understand changes to collection protocol in response to data needs and workflows* | Acceptance criteria reference the collection protocol; VCDC-7 proposes a protocol change |
| *Providing peer-to-peer feedback* | VCDC-7 written as a constructive, reasoned improvement suggestion |
| *Accuracy, efficiency, passion for data* | **QA Review** gate + **VCDC-8** Final QA review — nothing closes without validation |
| *MS Office / Excel proficiency* | Tickets and statuses exported as a structured CSV (`jira-import.csv`) |
| *Experience with JIRA / agile collaborative workflow* | The whole project: a JIRA Kanban board moving work through defined stages |

The core competency on display: **track tasks, document issues, move work through
stages, and support quality control** — accurately, proactively, and with a paper trail.

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
