# Suppliers

## Overview

The **Suppliers** page is the main supplier management page in JomeInvoice V2.

A supplier is the person, company, or organisation that has sold goods or services to your company. In the e-Invoice flow, suppliers are used to record the seller information for purchase-side or outbound e-Invoice records where your company is capturing transactions from parties that supplied to the business.

Use this page to view, manage, add, and review supplier records before using them in purchase documents, self-billed e-Invoices, credit notes, debit notes, refund notes, and related supplier-side transaction records.

The Suppliers page helps ensure that supplier details such as supplier name, email, country, entity type, and approval status are properly maintained before documents are issued, imported, converted, or submitted.

---

## Who Should Use This Page

This page is useful for:

| User                           | Purpose                                                                      |
| ------------------------------ | ---------------------------------------------------------------------------- |
| Finance users                  | Manage supplier records used in purchase-side or self-billed e-Invoice flows |
| Admin users                    | Review, approve, and maintain supplier master data                           |
| Procurement / operations teams | Add or check supplier details before recording purchase transactions         |
| Support teams                  | Investigate supplier-related issues in e-Invoices                            |
| Compliance / audit teams       | Review supplier information used for e-Invoice reporting                     |

---

## Accessing the Suppliers Page

To open the Suppliers page:

1. Log in to JomeInvoice V2.
2. Open the left navigation menu.
3. Select **Suppliers**.

The page will display the latest supplier records for the current workspace.

---

## Page Layout

The Suppliers page contains five main areas:

1. **Page title**
2. **Supplier action buttons**
3. **Supplier status tabs**
4. **Search and filter controls**
5. **Supplier records table**
6. **Pagination controls**

---

## Supplier Action Buttons

At the top of the page, users can perform supplier-related actions.

### More Actions

Use **More Actions** to access additional supplier actions.

The available actions may depend on the selected supplier records, user permissions, and system configuration.

If bulk actions are supported, users may need to select one or more supplier records before using this button.

### Add Supplier

Use **Add Supplier** to create a new supplier record.

Create a supplier when the seller does not already exist in the system and needs to be used for purchase-side or self-billed e-Invoice creation.

Before adding a new supplier, users should first search the supplier list to avoid creating duplicate supplier profiles.

---

## Supplier Status Tabs

The Suppliers page groups supplier records by approval status.

These tabs help users quickly understand whether supplier records are ready to use, pending review, or awaiting further action.

| Status           | Description                                                                  |
| ---------------- | ---------------------------------------------------------------------------- |
| Approved         | Supplier records that have been approved and are ready for normal use        |
| Pending Approval | Supplier records waiting for review or approval                              |
| Awaiting         | Supplier records waiting for a required action, response, or completion step |

The page also shows the number of records in each status.

Example:

```text id="i10swz"
Approved: 68
Pending Approval: 5
Awaiting: 14
```

Use the tabs to switch between supplier groups.

---

## Search and Filter Controls

The top section contains controls that help users find specific supplier records.

### Search

Use the search field to look for a specific supplier.

You can search by:

```text id="se7msz"
Supplier name
Email address
Registration number
Supplier reference
Supplier code
```

Examples of useful search terms:

```text id="z7093g"
ISETAN
Safeguards
Sunway
Supplier Sample
finance-ap@safeguards-ss.com.my
```

### Country

Use the **Country** filter to narrow the supplier list by country.

This is useful when reviewing suppliers from a specific jurisdiction or when checking whether Malaysian and non-Malaysian suppliers are recorded correctly.

### Filter

Use **Filter** to apply additional filtering options, where available.

This helps narrow the supplier list when there are many records.

---

## Supplier Records Table

The main table displays the list of supplier records.

Each row represents one supplier.

| Column        | Description                                        |
| ------------- | -------------------------------------------------- |
| Supplier      | Supplier name or identifier                        |
| Status        | Current approval status of the supplier            |
| Email         | Supplier email address                             |
| Country       | Supplier country                                   |
| Entity        | Supplier entity type                               |
| Last Modified | Date and time the supplier record was last updated |
| Action        | Available action, such as **View**                 |

---

## Reading a Supplier Record

Each row should be read from left to right.

Example:

```text id="w8vcr3"
Supplier: ISETAN OF JAPAN SDN BHD
Supplier Code: 1000
Status: Approved
Email: lindplus0303@gmail.com
Country: MALAYSIA
Entity: Individual
Last Modified: Feb 23, 2026, 01:57 PM
Action: View
```

This means the supplier record has been approved, is associated with Malaysia, and can be reviewed by clicking **View**.

Another example:

```text id="px290c"
Supplier: Safeguards Secure Solution Sdn Bhd
Supplier Code: -
Status: Approved
Email: finance-ap@safeguards-ss.com.my
Country: MALAYSIA
Entity: Private Limited
Last Modified: May 29, 2026, 11:57 AM
Action: View
```

This means the supplier is a private limited entity in Malaysia and is currently approved.

---

## Common Supplier Statuses

### Approved

**Approved** means the supplier record has been reviewed and is ready for normal use.

Approved suppliers can generally be selected when creating purchase-side documents, self-billed e-Invoices, or other supplier-related transaction records, depending on the system workflow.

---

### Pending Approval

**Pending Approval** means the supplier record has been created or updated but still requires approval.

Use this status to identify supplier records that need to be reviewed before they are used in production documents.

A supplier may be pending approval because:

* the record was newly created
* important supplier details were changed
* approval is required by internal workflow
* supplier information needs to be checked before use

---

### Awaiting

**Awaiting** means the supplier record is waiting for a required next step.

This may indicate that information, confirmation, verification, or another action is still pending before the record can move forward.

Users should open the supplier record using **View** to understand what is still required.

---

## Entity Types

The **Entity** column shows the supplier’s legal or business type.

Examples shown on the page include:

| Entity Type     | Meaning                                             |
| --------------- | --------------------------------------------------- |
| Individual      | A person supplying goods or services to the company |
| Private Limited | A private company or incorporated business entity   |
| Public Limited  | A public company or listed business entity          |

The entity type is important because it may affect the supplier details required for e-Invoice issuance, such as registration details, identification details, TIN, or other seller information.

---

## Available Actions

### View

Click **View** to open the supplier record.

Use this to review supplier details such as:

* supplier name
* supplier code, where available
* email address
* country
* entity type
* approval status
* registration or identification details, if available
* e-Invoice seller details
* last modified information

Users should use **View** before editing, approving, or investigating a supplier record.

### Open Menu

Each supplier row may also show an additional menu.

Use this menu to access row-specific actions, where available.

The exact options may depend on user permissions, supplier status, and system configuration.

---

## Supplier Country

The **Country** column shows the country associated with the supplier.

Examples shown on the page include:

```text id="1o5sab"
MALAYSIA
ALAND ISLANDS
```

The country value is important for e-Invoice reporting because different supplier types or jurisdictions may require different seller information.

For Malaysian suppliers, users should ensure the supplier’s required local e-Invoice details are accurate.

For foreign suppliers, users should check that the country and entity type are correctly recorded.

---

## Last Modified

The **Last Modified** column shows when the supplier record was last updated.

Use this field to check whether supplier details were recently changed.

This is useful when:

* investigating why a purchase-side document used certain supplier details
* checking whether a supplier profile was updated before issuing or submitting an e-Invoice
* reviewing recent supplier master data changes
* confirming whether an old supplier profile may need updating

---

## Pagination

The bottom of the page shows pagination controls.

Use the pagination controls to move between pages of supplier records.

| Control     | Description             |
| ----------- | ----------------------- |
| Previous    | Go to the previous page |
| Page number | Jump to a specific page |
| Next        | Go to the next page     |

Example page controls shown:

```text id="c6oe4c"
Previous
1
2
3
4
5
...
Next
```

If there are many supplier records, use search, status tabs, or filters before navigating through multiple pages.

---

## Recommended Workflows

### Add a new supplier before recording a purchase-side e-Invoice

1. Open **Suppliers**.
2. Search for the supplier first to check whether the record already exists.
3. If the supplier does not exist, click **Add Supplier**.
4. Enter the required supplier details.
5. Save the supplier record.
6. Check whether the supplier requires approval.
7. Use the supplier when creating the relevant purchase-side, self-billed, or supplier-related e-Invoice document.

---

### Check whether a supplier is ready to use

1. Open **Suppliers**.
2. Search for the supplier name, email, supplier code, or registration number.
3. Check the **Status** column.
4. If the supplier is **Approved**, the record is ready for normal use.
5. If the supplier is **Pending Approval** or **Awaiting**, click **View** to check what action is required.

---

### Review suppliers pending approval

1. Open **Suppliers**.
2. Click the **Pending Approval** tab.
3. Review each supplier record.
4. Click **View** to inspect supplier details.
5. Approve, update, or escalate the record based on internal workflow.

---

### Find suppliers from a specific country

1. Open **Suppliers**.
2. Click the **Country** filter.
3. Select the relevant country.
4. Review the filtered supplier list.
5. Use **View** to inspect any supplier record that needs checking.

---

### Investigate which supplier was used for a purchase-side document

1. Open **Suppliers**.
2. Search using the supplier name, email, supplier code, or registration number from the document.
3. Open the supplier record using **View**.
4. Compare the supplier details against the seller information on the e-Invoice.
5. Check the **Last Modified** date to understand whether the supplier details may have changed recently.

---

## Best Practices

* Search for an existing supplier before creating a new one.
* Avoid duplicate supplier records for the same seller.
* Keep supplier names, emails, countries, and entity types accurate.
* Review **Pending Approval** and **Awaiting** suppliers regularly.
* Confirm supplier details before issuing, importing, converting, or submitting supplier-side e-Invoice records.
* Use the **Country** filter when reviewing local versus foreign suppliers.
* Use **Last Modified** to identify recently changed supplier records.
* Open the supplier record using **View** before taking further action.
* Treat supplier data as master data because it affects e-Invoice accuracy and auditability.

---

## Troubleshooting

### I cannot find a supplier

Try the following:

1. Clear all filters.
2. Search using a shorter keyword.
3. Search by email address instead of supplier name.
4. Search by supplier code, registration number, or identifier, if available.
5. Check all status tabs: **Approved**, **Pending Approval**, and **Awaiting**.
6. Check whether the supplier may have been created under a different spelling or legal entity name.

---

### The supplier is not available when creating an e-Invoice

Possible reasons include:

* the supplier is not approved
* the supplier is still pending approval
* the supplier is awaiting required action
* required supplier details are incomplete
* the supplier was created under a different record
* filters or search terms are hiding the supplier

Open the supplier record using **View** to check the status and details.

---

### There are duplicate supplier records

If duplicate records appear:

1. Compare the supplier name, supplier code, email, country, and entity type.
2. Open each record using **View**.
3. Check which record has the most accurate and complete information.
4. Confirm which record has been used in existing e-Invoices.
5. Follow the company’s internal process to update, merge, deactivate, or avoid using the duplicate record.

---

### The supplier status is Pending Approval

This means the supplier record needs review before it can be fully used.

Open the record using **View** and check whether any required fields, approval steps, or internal review actions are pending.

---

### The supplier country or entity type looks incorrect

Open the supplier record using **View** and confirm the supplier details.

Incorrect country or entity type may affect e-Invoice seller information, so the record should be corrected before issuing or submitting related documents.

---

## Summary

The Suppliers page is the supplier master data page for JomeInvoice V2.

It allows users to add, view, search, filter, and review suppliers who sell goods or services to the company. These supplier records are used as seller information when the company records purchase-side, self-billed, or supplier-related e-Invoice transactions.

Use this page whenever you need to create a supplier, check whether a supplier is approved, review supplier details, or investigate supplier information used in an e-Invoice document.
