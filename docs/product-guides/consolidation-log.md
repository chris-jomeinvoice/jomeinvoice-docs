# Consolidation Log

## Overview

The **Consolidation Log** page provides a record of consolidated e-Invoice batches created in JomeInvoice V2.

Use this page to monitor the consolidation lifecycle, review consolidation status, check how many receipts or invoices were included, and continue actions such as viewing or submitting a consolidated invoice.

The Consolidation Log is especially useful for tracking receipts or invoices that are grouped together before being converted or submitted as consolidated e-Invoices.

---

## Who Should Use This Page

This page is useful for:

| User                     | Purpose                                                                                 |
| ------------------------ | --------------------------------------------------------------------------------------- |
| Finance users            | Track consolidated e-Invoice batches and submission status                              |
| Admin users              | Monitor consolidation activity across branches and users                                |
| Operations teams         | Check whether receipts or invoices have been tagged, converted, submitted, or discarded |
| Compliance / audit teams | Review consolidation history and supporting records                                     |
| Managers                 | Monitor consolidation volume and completion progress                                    |

---

## Accessing the Consolidation Log

To open the Consolidation Log:

1. Log in to JomeInvoice V2.
2. Open the left navigation menu.
3. Select **Consolidation Log**.

The page will display the latest consolidation records for the selected workspace.

---

## Page Layout

The Consolidation Log page contains five main areas:

1. **Page title**
2. **Module selector**
3. **Filter and date controls**
4. **Status summary cards**
5. **Consolidation records table**
6. **Pagination controls**

---

## Module Selector

At the top of the page, users can select the module for the consolidation records.

### Sales

The page currently displays **Sales** consolidation records.

Use this when reviewing consolidated sales receipts or sales invoices that are being prepared for e-Invoice submission.

---

## Filter and Date Controls

The top section contains controls that help users narrow down the consolidation records.

### All Types

Use **All Types** to filter the records by consolidation type.

This is useful when you only want to view a specific category of consolidated documents.

### Date Created

Use **Date Created** to sort or filter records based on when the consolidation record was created.

This helps users review the most recent records or investigate records created during a specific period.

### Past 3 months

Use **Past 3 months** to filter records by time period.

This is useful for month-end review, audit checking, and narrowing the table to recent consolidation activity.

### Search

Use the search field to find a specific consolidation record.

You can search by:

```text
Consolidation invoice number
Created by user
Branch name
Status
Related invoice or receipt reference
```

Examples of useful search terms:

```text
CS/INV2606090003
Converted
Discarded
Tagged
HQ
```

---

## Status Summary Cards

The status summary cards show a quick count of consolidation records by status.

These cards help users understand the current state of consolidation activity at a glance.

| Status    | Description                                                                      |
| --------- | -------------------------------------------------------------------------------- |
| All       | Total number of consolidation records matching the current filters               |
| Tagged    | Records where receipts or invoices have been tagged for consolidation            |
| Converted | Records that have been converted into consolidated e-Invoices                    |
| Queue     | Records waiting to be processed                                                  |
| Completed | Records that have completed the consolidation flow                               |
| Discarded | Records that have been discarded and will not continue in the consolidation flow |

Clicking or selecting a status card may filter the table to records with that status, depending on system configuration.

---

## Consolidation Records Table

The main table displays the list of consolidation records.

Each row represents one consolidation batch.

| Column             | Description                                                                |
| ------------------ | -------------------------------------------------------------------------- |
| Invoice #          | The consolidation invoice or batch reference number                        |
| Status             | The current status of the consolidation record                             |
| Created On         | Date and time the consolidation record was created                         |
| Created By         | User who created or processed the consolidation record                     |
| Branch             | Branch associated with the consolidation record                            |
| # eInvoices        | Number of e-Invoices generated from the consolidation record               |
| # Receipt/Invoices | Number of source receipts or invoices included in the consolidation record |
| Result             | Processing result or output, where available                               |
| Action             | Available actions such as View or Submit                                   |

---

## Reading a Consolidation Record

Each row should be read from left to right.

Example:

```text
Invoice #: CS/INV2606090003
Status: Converted (Processing)
Created On: Jun 9, 2026, 09:57 AM
Created By: User
Branch: HQ
# eInvoices: 1
# Receipt/Invoices: 1
Result: -
Action: View
```

This means a consolidation record was created, has produced one e-Invoice from one source receipt or invoice, and is currently in a converted processing state.

---

## Common Consolidation Statuses

### Tagged

**Tagged** means the receipts or invoices have been selected or grouped for consolidation.

Use this status to identify records that may still need review, conversion, or further processing.

---

### Converted

**Converted** means the tagged receipts or invoices have been converted into a consolidated e-Invoice.

A converted record may be ready for submission, depending on its processing state.

---

### Converted (Processing)

**Converted (Processing)** means the consolidation record has been converted and is still being processed.

Users should wait for processing to complete before assuming the final result is available.

---

### Queue

**Queue** means the consolidation record is waiting for processing.

This may happen when the system is handling multiple consolidation jobs or background tasks.

---

### Completed

**Completed** means the consolidation flow has been completed.

Use this status to confirm that the consolidation process has finished successfully.

---

### Discarded

**Discarded** means the consolidation record was removed from the active flow.

Discarded records should not be submitted or processed further unless a new consolidation record is created.

---

## Available Actions

### View

Click **View** to open the consolidation record.

Use this to review the details of the consolidation batch, including the related receipts, invoices, generated e-Invoices, status, and processing result.

### Submit

Click **Submit** to submit the consolidated e-Invoice, where available.

The **Submit** action may only appear when the record is eligible for submission.

Before submitting, users should confirm that:

* the correct receipts or invoices are included
* the generated e-Invoice count is correct
* the branch is correct
* the record is not discarded
* the consolidation status is ready for submission

---

## Result Column

The **Result** column shows the processing result of the consolidation record, where available.

If the result shows:

```text
-
```

This means there is no result displayed yet, or the result is not applicable for that record.

A result may appear after processing, conversion, submission, or completion, depending on system behaviour.

---

## Pagination

The bottom of the page shows the current result range and total number of records.

Example:

```text
Results: 1 - 10 of 79
```

Use the pagination controls to move between pages.

| Control       | Description                                 |
| ------------- | ------------------------------------------- |
| Rows per page | Select how many records to display per page |
| Previous      | Go to the previous page                     |
| Page number   | Jump to a specific page                     |
| Next          | Go to the next page                         |

If there are many consolidation records, use filters or search before navigating through multiple pages.

---

## Recommended Workflows

### Review recent consolidation activity

1. Open **Consolidation Log**.
2. Confirm the module is set to **Sales**.
3. Use the date filter, such as **Past 3 months**.
4. Review the status summary cards.
5. Check the latest records in the table.
6. Click **View** for any record that needs further review.

---

### Find a specific consolidation record

1. Open **Consolidation Log**.
2. Enter the consolidation invoice number in the search field.
3. Review the matching record in the table.
4. Check the status, created date, created by user, branch, and source document count.
5. Click **View** to inspect the record in detail.

---

### Check whether a consolidation record is ready to submit

1. Open **Consolidation Log**.
2. Search for the consolidation invoice number.
3. Check the **Status** column.
4. Confirm the **# eInvoices** and **# Receipt/Invoices** counts.
5. Review the **Result** column.
6. If the **Submit** button is available, open the record and confirm the details before submitting.

---

### Review discarded consolidation records

1. Open **Consolidation Log**.
2. Select or filter by **Discarded**.
3. Review the discarded records.
4. Click **View** to check why the record was discarded, if details are available.
5. Create a new consolidation record if the receipts or invoices still need to be consolidated.

---

### Monitor processing records

1. Open **Consolidation Log**.
2. Look for records with **Converted (Processing)** or **Queue** status.
3. Check the created date and time.
4. Wait for processing to complete.
5. Refresh or revisit the page later to confirm whether the status has changed to **Completed**, **Converted**, or another final state.

---

## Best Practices

* Search by consolidation invoice number when investigating a specific record.
* Use the date filter before reviewing large volumes of consolidation records.
* Check the status summary cards first to understand the overall consolidation workload.
* Always review the source receipt or invoice count before submitting.
* Do not submit a consolidation record unless the included documents are correct.
* Use **View** to inspect the record before taking further action.
* Treat **Discarded** records as inactive and create a new consolidation record if needed.
* Use pagination only after applying filters, especially when there are many records.

---

## Troubleshooting

### I cannot find a consolidation record

Try the following:

1. Clear all filters.
2. Search using only part of the consolidation invoice number.
3. Expand the date range.
4. Check whether the record belongs to a different status.
5. Move to the next page using pagination.

---

### The Submit button is not available

The record may not be eligible for submission.

Possible reasons include:

* the record is still tagged
* the record is still processing
* the record has been discarded
* the record has already been submitted or completed
* there are no generated e-Invoices
* required consolidation details are incomplete

Open the record using **View** to check the details.

---

### The Result column shows a dash

A dash means no result is currently displayed.

This may happen when:

* processing is still ongoing
* the record has not reached a result stage
* no result is applicable
* the record was discarded before producing a result

---

### The numbers do not look correct

Check the following columns:

| Column             | What to verify                                                   |
| ------------------ | ---------------------------------------------------------------- |
| # eInvoices        | Number of generated e-Invoices                                   |
| # Receipt/Invoices | Number of source documents included                              |
| Status             | Whether the record is tagged, converted, completed, or discarded |
| Branch             | Whether the record belongs to the expected branch                |

If the numbers still seem incorrect, open the record using **View** and compare the included documents.

---

## Summary

The Consolidation Log is the main tracking page for consolidated e-Invoice batches in JomeInvoice V2.

It allows users to review consolidation records, monitor statuses, check source document counts, view generated e-Invoices, identify discarded or processing records, and submit eligible consolidated e-Invoices.

Use this page whenever you need to understand the status of a consolidation batch, confirm what was included, or continue the consolidation process.
