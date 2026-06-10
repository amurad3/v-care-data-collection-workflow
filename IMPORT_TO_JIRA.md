# Importing this project into JIRA

The [`jira-import.csv`](jira-import.csv) file creates all 10 tickets in a real
JIRA board in a couple of minutes.

## Steps

1. **Create the project**
   - In JIRA, create a new project named **V-CARE Data Collection Workflow Practice**.
   - Choose the **Kanban** template (Team-managed is simplest for practice).

2. **Set up the columns / statuses**
   Rename the board columns (Board → ··· → Configure / Manage columns) to:
   `Backlog`, `Ready for Session`, `In Progress`, `Blocked / Issue Found`,
   `QA Review`, `Done`. Each column maps to a status of the same name.

3. **Import the CSV**
   - Cloud: **Filters → View all filters → Import issues from CSV**, or
     **Project settings → Import**.
   - Upload `jira-import.csv`.

4. **Map the fields** when prompted:

   | CSV column | JIRA field |
   | --- | --- |
   | Issue Key | Issue Key (optional — lets you keep VCDC-# IDs) |
   | Summary | Summary |
   | Issue Type | Issue Type |
   | Priority | Priority |
   | Status | Status |
   | Labels | Labels (space-separated values become separate labels) |
   | Description | Description |
   | Acceptance Criteria | Description (append) or a custom field |

5. **Confirm the import.** Tickets land in the correct column because the **Status**
   value matches each board column.

## Notes
- If your JIRA instance doesn't have the statuses `Ready for Session`,
  `Blocked / Issue Found`, or `QA Review`, create them first (or map them to the
  nearest existing status during import).
- `Improvement` issue type may need to be enabled in your project's issue type
  scheme; otherwise map VCDC-7 to `Task` or `Story`.
