# Import Log

## Overview

The **Import Log** page provides a record of files imported into JomeInvoice V2.

Use this page to monitor uploaded or synced import files, check whether each import was completed or failed, review how many rows were processed, and open the import result for further investigation.

The Import Log is especially useful for tracking CSV or SFTP-based imports, checking failed imports, and confirming whether imported receipts or invoices were successfully created in the system.

---

## Who Should Use This Page

This page is useful for:

| User                     | Purpose                                                                     |
| ------------------------ | --------------------------------------------------------------------------- |
| Finance users            | Confirm whether imported receipts or invoices were processed successfully   |
| Admin users              | Monitor import activity across the workspace                                |
| Operations teams         | Check whether uploaded files were completed, failed, or partially processed |
| Support teams            | Investigate import errors and failed files                                  |
| Compliance / audit teams | Review import history and supporting records                                |

---

## Accessing the Import Log

To open the Import Log:

1. Log in to JomeInvoice V2.
2. Open the left navigation menu.
3. Select **Import Log**.

The page will display the latest import records for the current workspace.

---

## Page Layout

The Import Log page contains five main areas:

1. **Page title**
2. **Import source selector**
3. **Date controls**
4. **Status summary cards**
5. **Import records table**
6. **Pagination controls**

---

## Import Source Selector

At the top of the page, users can select the import source or import method.

### SFTP

The page currently displays **SFTP** import records.

Use this when reviewing files imported through the SFTP import flow.

---

## Filter and Date Controls

The top section contains controls that help users narrow down the import records.

### Created Date

Use **Created Date** to review import records based on when the import file was created or received by the system.

This helps users investigate imports from a specific period.

### Past 3 Months

Use **Past 3 Months** to filter the import records by time period.

This is useful for month-end checking, recent import review, and narrowing the table to recent import activity.

---

## Status Summary Cards

The status summary cards show a quick count of import records by status.

These cards help users understand the current state of import processing at a glance.

| Status    | Description                                                 |
| --------- | ----------------------------------------------------------- |
| All       | Total number of import records matching the current filters |
| Syncing   | Files currently being synced into the system                |
| Chunking  | Files being split or prepared for processing                |
| Failed    | Files that failed to import successfully                    |
| Partial   | Files where only some rows were successfully imported       |
| Completed | Files that completed processing successfully                |

Clicking or selecting a status card may filter the table to records with that status, depending on system configuration.

---

## Import Records Table

The main table displays the list of imported files.

Each row represents one imported file.

| Column        | Description                                                          |
| ------------- | -------------------------------------------------------------------- |
| File Name     | Name of the imported file                                            |
| Trans.Type    | Transaction type associated with the imported file, where available  |
| Import Status | Current status of the import                                         |
| Created On    | Date and time the import record was created                          |
| Import Result | Number of rows detected or processed in the import file              |
| # Receipt     | Number of receipts created or associated with the import             |
| Result        | Success count for the import, such as `1/1 Success` or `0/1 Success` |
| Action        | Available action, such as **View**                                   |

---

## Reading an Import Record

Each row should be read from left to right.

Example of a completed import:

```text id="2km9yz"
File Name: RedSquare Template2.csv
Trans.Type: -
Import Status: Completed
Created On: 6/9/2026, 2:42:11 PM
Import Result: 1 Rows
# Receipt: 1
Result: 1/1 Success
Action: View
```

This means the file was imported successfully, one row was processed, and one receipt was created or associated with the import.

Example of a failed import:

```text id="osudac"
File Name: TestFailed - TESTNEG - Letest3.csv.csv (1).csv
Trans.Type: -
Import Status: Failed
Created On: 6/9/2026, 10:34:11 AM
Import Result: 1 Rows
# Receipt: 1
Result: 0/1 Success
Action: View
```

This means the file was received and processed, but the row did not import successfully.

---

## Common Import Statuses

### Syncing

**Syncing** means the file is currently being retrieved or synced into JomeInvoice V2.

Users should wait for the sync process to complete before reviewing the final import result.

---

### Chunking

**Chunking** means the file is being prepared for processing.

This may happen when the system breaks the file into smaller parts before importing the rows.

---

### Completed

**Completed** means the import process finished successfully.

A completed import should usually show a successful result count, such as:

```text id="qdvkhd"
1/1 Success
```

Use this status to confirm that the imported file was processed successfully.

---

### Failed

**Failed** means the import did not complete successfully.

A failed import may show a result such as:

```text id="ew3iup"
0/1 Success
```

Use **View** to inspect the failure details and determine what needs to be corrected.

---

### Partial

**Partial** means only some rows in the file were imported successfully.

This may happen when one or more rows contain errors, missing fields, invalid formatting, or unsupported values.

Users should review the failed rows, correct the source file, and re-import if needed.

---

## Available Actions

### View

Click **View** to open the import record.

Use this to review the import details, including:

* file information
* import status
* number of rows processed
* number of successful rows
* failed rows, if available
* error messages, if available
* related receipts or invoices created from the import

---

## Result Column

The **Result** column shows how many rows were successfully imported.

Examples:

| Result         | Meaning                                         |
| -------------- | ----------------------------------------------- |
| `1/1 Success`  | One out of one row was successfully imported    |
| `0/1 Success`  | Zero out of one row was successfully imported   |
| `5/10 Success` | Five out of ten rows were successfully imported |

Use this column to quickly understand whether the import fully succeeded, partially succeeded, or failed.

---

## Import Result Column

The **Import Result** column shows the number of rows detected or processed in the imported file.

Example:

```text id="usx573"
1 Rows
```

This means the system detected one row in the import file.

---

## Pagination

The bottom of the page shows the current result range and total number of records.

Example:

```text id="79kad0"
Results: 1 - 10 of 10
```

Use the pagination controls to move between pages.

| Control       | Description                                 |
| ------------- | ------------------------------------------- |
| Rows per page | Select how many records to display per page |
| Previous      | Go to the previous page                     |
| Page number   | Jump to a specific page                     |
| Next          | Go to the next page                         |

If there are many import records, use the date filter or status filters before navigating through multiple pages.

---

## Recommended Workflows

### Review recent import activity

1. Open **Import Log**.
2. Confirm the import source is set to **SFTP**.
3. Use the date filter, such as **Past 3 Months**.
4. Review the status summary cards.
5. Check the latest import records in the table.
6. Click **View** for any record that needs further review.

---

### Check whether an import was successful

1. Open **Import Log**.
2. Find the imported file in the table.
3. Check the **Import Status** column.
4. Review the **Import Result** column.
5. Review the **Result** column.
6. If the result shows full success, the import was completed successfully.
7. If the result shows zero or partial success, click **View** to inspect the details.

---

### Investigate a failed import

1. Open **Import Log**.
2. Select or filter by **Failed**.
3. Find the failed file.
4. Check the **Created On** timestamp.
5. Review the **Import Result** and **Result** columns.
6. Click **View** to open the import details.
7. Review the error details, if available.
8. Correct the source file and re-import if needed.

---

### Review partially successful imports

1. Open **Import Log**.
2. Select or filter by **Partial**.
3. Open the relevant import record using **View**.
4. Compare the number of successful rows against the total row count.
5. Review the failed rows or error messages.
6. Correct only the failed rows if possible.
7. Re-import the corrected file if needed.

---

### Confirm receipt creation from an import

1. Open **Import Log**.
2. Find the relevant imported file.
3. Check the **# Receipt** column.
4. Compare it against the expected number of receipts.
5. Review the **Result** column to confirm success.
6. Click **View** if the number does not match expectations.

---

## Best Practices

* Check the **Result** column before assuming an import was successful.
* Use **View** for any failed or partially successful import.
* Keep source file names clear and easy to identify.
* Use consistent file naming so imports can be traced later.
* Review failed imports before re-uploading the same file.
* Correct the source CSV before re-importing.
* Use the date filter when reviewing a specific accounting or operational period.
* Treat **Completed** together with the success count as the confirmation of import success.
* Do not rely on file name alone; always check status, row count, and result.

---

## Troubleshooting

### I cannot find an imported file

Try the following:

1. Confirm the import source is correct.
2. Expand the date range.
3. Check whether the file appears under another status.
4. Review the next page using pagination.
5. Confirm that the file was actually uploaded or synced.

---

### The import status is Failed

A failed import means the file did not process successfully.

Possible causes include:

* missing required fields
* invalid field values
* incorrect CSV format
* unsupported transaction type
* duplicate or invalid document references
* buyer or supplier details that cannot be matched
* system validation failure

Click **View** to inspect the specific failure details.

---

### The result shows 0/1 Success

This means the file contained one row, but the row was not successfully imported.

Open the record using **View**, review the error details, correct the source file, and re-import if needed.

---

### The import is stuck in Syncing or Chunking

The file may still be processing.

If the status does not change after a reasonable period, check whether:

* the file is unusually large
* the SFTP sync is delayed
* the file format is invalid
* the system is processing a backlog
* there is a technical issue with the import service

Escalate to the support or technical team if the status remains unchanged.

---

### The receipt count does not match the expected number

Check the following columns:

| Column        | What to verify                                               |
| ------------- | ------------------------------------------------------------ |
| Import Result | Number of rows detected in the file                          |
| # Receipt     | Number of receipts created or associated                     |
| Result        | Number of successful rows                                    |
| Import Status | Whether the import completed, failed, or partially succeeded |

If the numbers still seem incorrect, open the record using **View** and review the import details.

---

## Summary

The Import Log is the main tracking page for imported files in JomeInvoice V2.

It allows users to review SFTP import records, monitor import statuses, check row counts, confirm successful receipt creation, identify failed or partial imports, and open individual import records for investigation.

Use this page whenever you need to confirm whether an imported file was processed successfully or investigate why an import failed.
