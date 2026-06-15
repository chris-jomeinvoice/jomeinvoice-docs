# Activity Trail

## Overview

The **Activity Trail** page provides a chronological log of key actions and system events in JomeInvoice V2.

Use this page to review what happened in the system, when it happened, who performed the action, and which document or record was affected. It is especially useful for audit checks, troubleshooting, user activity review, and tracking the lifecycle of e-Invoices.

The Activity Trail records both user actions and system-generated events, such as invoice updates, buyer invitations, e-Invoice validation, LHDN processing, cancellation requests, and document conversion.

---

## Who Should Use This Page

This page is useful for:

| User                     | Purpose                                                     |
| ------------------------ | ----------------------------------------------------------- |
| Admin users              | Monitor user and system activity across the workspace       |
| Finance teams            | Track invoice status changes and e-Invoice lifecycle events |
| Support teams            | Investigate user issues or document processing problems     |
| Compliance / audit teams | Review historical actions and system records                |
| Managers                 | Understand who made changes and when they were made         |

---

## Accessing the Activity Trail

To open the Activity Trail:

1. Log in to JomeInvoice V2.
2. Open the left navigation menu.
3. Select **Activity Trail**.

The Activity Trail page will display the latest activity records for the current workspace.

---

## Page Layout

The Activity Trail page contains four main areas:

1. **Page title**
2. **Filter and search controls**
3. **Activity list**
4. **Pagination controls**

---

## Filter and Search Controls

At the top of the page, users can narrow down the activity records using several controls.

### All Actions

Use **All Actions** to filter the activity list by activity type.

This helps users quickly find a specific category of event, such as invoice updates, buyer invitations, validation events, cancellation events, or conversion events.

### All Users

Use **All Users** to filter the activity list by the user who performed the action.

This is useful when investigating actions taken by a specific team member.

### Search

Use the search field to look for a specific keyword, document number, invoice name, buyer name, or other activity detail.

Examples of useful search terms:

```text
Invoice Numbers
Names of users
Error status
```

### Pick a Date Range

Use **Pick a date range** to filter activity records by date.

This is useful when reviewing activity for a specific day, week, month, or audit period.

### Export Trails

Use **Export Trails** to export the filtered activity records.

Before exporting, apply the relevant filters first so the exported file contains only the activity records you need.

---

## Reading an Activity Record

Each activity record shows the event details in a timeline-style format.

A typical activity record may include:

| Field            | Description                                                |
| ---------------- | ---------------------------------------------------------- |
| Activity title   | A short summary of what happened                           |
| Date and time    | When the activity occurred                                 |
| Activity details | More information about the action or affected record       |
| User name        | The user who performed the action, where available         |
| Changed fields   | A list of field-level changes, where applicable            |
| IP address       | The IP address associated with the action, where available |

---

## Example Activity Records

### e-Invoice validated through the MyInvois Portal

This means the e-Invoice has been successfully validated through MyInvois.

Example:

```text
Invoice TestIssue23 status changed to Valid
```

Use this to confirm that an invoice has reached a valid status.

---

### e-Invoice is being processed by LHDN

This means the e-Invoice has entered LHDN submission processing.

Example:

```text
Invoice TestIssue23 status changed to Processing LHDN Submission
```

Use this to check whether the invoice is still being processed before it becomes valid or fails.

---

### e-Invoice Resubmission Requested

This means a user requested to resubmit an e-Invoice.

Example:

```text
Thony: Requested to resubmit non-consolidated e-Invoice (Invoice) for Invoice TestIssue23
```

This activity may also display the IP address associated with the request.

---

### Invoice has been updated

This means a user edited an invoice.

The activity may show both the general update and the exact field-level changes.

Example:

```text
Thony: updated invoice TestIssue23

'Issue Date' changed from '2026-03-01' to '2026-06-10'
Line item 'TEST' - 'Item Code' changed from 'INV-1R710V' to 'TEST'
Line item 'TEST' - 'Discount Type' changed from 'None' to 'Percentage'
```

Use this when investigating what changed in an invoice and who made the change.

---

### Buyer Invited

This means a buyer was invited from the system.

Example:

```text
Invited buyer Pentest
```

Use this to confirm whether a buyer invitation was sent.

---

### Cancellation request processed

This means an invoice cancellation request was successfully processed.

Example:

```text
Invoice INV20260609DR0O cancelled via MyInvois. With reason: Wrong supplier details
```

Use this to confirm the cancellation status and review the cancellation reason.

---

### Invoice has been converted

This means a receipt or source document was converted into an e-Invoice.

Example:

```text
Thony: Converted receipt TestIssue24 into non-consolidated e-Invoice
```

Use this to trace how a document became an e-Invoice.

---

### e-Invoice has been created

This means an e-Invoice record was created in the system.

Example:

```text
Thony: Invoice TestIssue24 converted into non-consolidated e-Invoice (Invoice)
```

Use this to confirm when the e-Invoice record was first created.

---

## IP Address Badges

Some activity records display an IP address below the activity details.

The IP address shows where the action was performed from, based on the available system record.

This is useful for:

- audit review
- suspicious activity investigation
- confirming whether an action came from an expected network or location
- support troubleshooting

Not every activity record will show an IP address.

---

## Pagination

The bottom of the page shows the current page number and total number of pages.

Example:

```text
Page 1 of 3905
```

Use the pagination controls to move between pages:

| Button   | Description                                 |
| -------- | ------------------------------------------- |
| Previous | Go to the previous page of activity records |
| Next     | Go to the next page of activity records     |

If you are on the first page, **Previous** may be disabled.

---

## Recommended Workflows

### Investigate an invoice status change

1. Open **Activity Trail**.
2. Search for the invoice number or document reference.
3. Review the status-related activity records.
4. Check the timestamps to understand the sequence of events.
5. Look for related events such as validation, LHDN processing, resubmission, cancellation, or updates.

---

### Check who edited an invoice

1. Open **Activity Trail**.
2. Search for the invoice number.
3. Look for an **Invoice has been updated** activity.
4. Review the user name shown in the activity details.
5. Review the field-level changes to understand what was edited.
6. Check the IP address if available.

---

### Review actions by a specific user

1. Open **Activity Trail**.
2. Select the user from **All Users**.
3. Apply a date range if needed.
4. Review the filtered activity records.
5. Export the trails if a record is needed for reporting or audit.

---

### Export audit records

1. Open **Activity Trail**.
2. Apply the required filters:
  - Action type
  - User
  - Date range
  - Search keyword, if needed
3. Click **Export Trails**.
4. Use the exported file for audit, reporting, or internal review.

---

## Best Practices

- Use filters before exporting to avoid exporting unnecessary records.
- Search by invoice number or document reference when investigating a specific document.
- Use the date range filter for audit periods or month-end reviews.
- Review the activity sequence from oldest to newest when reconstructing what happened.
- Check field-level changes when reviewing invoice edits.
- Use IP address information as supporting audit context, not as the only proof of user identity.
- Avoid sharing exported activity logs externally unless required, as they may contain user, document, and system activity details.

---

## Troubleshooting

### I cannot find a specific activity

Try the following:

1. Clear all filters.
2. Search using a shorter keyword.
3. Search using the invoice number instead of the customer or buyer name.
4. Expand the date range.
5. Check the next pages using pagination.

---

### The export does not contain the records I expected

Check whether filters were applied before exporting.

The export should reflect the currently selected filters, so confirm the action type, user, search keyword, and date range before clicking **Export Trails**.

---

### The activity record does not show an IP address

This is expected for some activity types.

IP addresses may only appear when the system has captured the relevant information for that action.

---

## Summary

The Activity Trail is the audit and investigation page for JomeInvoice V2. It gives users a clear record of system and user actions, including invoice updates, e-Invoice validation, LHDN processing, buyer invitations, cancellations, conversions, timestamps, users, field-level changes, and IP addresses.

Use this page whenever you need to understand what happened to a document, who performed an action, and when the action took place.
