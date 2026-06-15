# Customers

## Overview

The **Customers** page is the main customer management page in JomeInvoice V2.

A customer is the person, company, or organisation that has bought from your company. In the e-Invoice flow, customers are used as the buyer information for inbound revenue recorded by your company.

Use this page to view, manage, add, and review customer records before using them in sales e-Invoices, credit notes, debit notes, refund notes, and related revenue documents.

The Customers page helps ensure that buyer details such as customer name, email, country, entity type, and approval status are properly maintained before documents are issued or submitted.

---

## Who Should Use This Page

This page is useful for:

| User                     | Purpose                                                  |
| ------------------------ | -------------------------------------------------------- |
| Finance users            | Manage customer records used in sales e-Invoices         |
| Admin users              | Review, approve, and maintain customer master data       |
| Sales / operations teams | Add or check customer details before issuing documents   |
| Support teams            | Investigate customer-related issues in invoices          |
| Compliance / audit teams | Review customer information used for e-Invoice reporting |

---

## Accessing the Customers Page

To open the Customers page:

1. Log in to JomeInvoice V2.
2. Open the left navigation menu.
3. Select **Customers**.

The page will display the latest customer records for the current workspace.

---

## Page Layout

The Customers page contains five main areas:

1. **Page title**
2. **Customer action buttons**
3. **Customer status tabs**
4. **Search and filter controls**
5. **Customer records table**
6. **Pagination controls**

---

## Customer Action Buttons

At the top of the page, users can perform customer-related actions.

### More Actions

Use **More Actions** to access additional customer actions.

The available actions may depend on the selected customer records, user permissions, and system configuration.

If bulk actions are supported, users may need to select one or more customer records before using this button.

### Add Customer

Use **Add Customer** to create a new customer record.

Create a customer when the buyer does not already exist in the system and needs to be used for sales e-Invoice creation.

Before adding a new customer, users should first search the customer list to avoid creating duplicate customer profiles.

---

## Customer Status Tabs

The Customers page groups customer records by approval status.

These tabs help users quickly understand whether customer records are ready to use, pending review, or awaiting further action.

| Status           | Description                                                                  |
| ---------------- | ---------------------------------------------------------------------------- |
| Approved         | Customer records that have been approved and are ready for normal use        |
| Pending Approval | Customer records waiting for review or approval                              |
| Awaiting         | Customer records waiting for a required action, response, or completion step |

The page also shows the number of records in each status.

Example:

```text id="41qztf"
Approved: 214
Pending Approval: 20
Awaiting: 79
```

Use the tabs to switch between customer groups.

---

## Search and Filter Controls

The top section contains controls that help users find specific customer records.

### Search

Use the search field to look for a specific customer.

You can search by:

```text id="h8wy25"
Customer name
Email address
Registration number
Customer reference
```

Examples of useful search terms:

```text id="i2ckaz"
Thony
ISETAN
hello@jomeinvoice.my
198101009265
```

### Country

Use the **Country** filter to narrow the customer list by country.

This is useful when reviewing customers from a specific jurisdiction or when checking whether Malaysian and non-Malaysian customers are recorded correctly.

### Filter

Use **Filter** to apply additional filtering options, where available.

This helps narrow the customer list when there are many records.

---

## Customer Records Table

The main table displays the list of customer records.

Each row represents one customer.

| Column        | Description                                        |
| ------------- | -------------------------------------------------- |
| Customer      | Customer name or identifier                        |
| Status        | Current approval status of the customer            |
| Email         | Customer email address                             |
| Country       | Customer country                                   |
| Entity        | Customer entity type                               |
| Last Modified | Date and time the customer record was last updated |
| Action        | Available action, such as **View**                 |

---

## Reading a Customer Record

Each row should be read from left to right.

Example:

```text id="38ghd4"
Customer: Thony
Status: Approved
Email: hello@jomeinvoice.my
Country: MALAYSIA
Entity: Individual
Last Modified: Jan 20, 2026, 11:08 AM
Action: View
```

This means the customer record belongs to an individual customer in Malaysia, has been approved, and can be reviewed by clicking **View**.

Another example:

```text id="nl0b7v"
Customer: TT
Status: Approved
Email: kwanxer20101@gmail.com
Country: ARUBA
Entity: Private Limited
Last Modified: Apr 13, 2026, 05:33 PM
Action: View
```

This means the customer is a private limited entity from Aruba and is currently approved.

---

## Common Customer Statuses

### Approved

**Approved** means the customer record has been reviewed and is ready for normal use.

Approved customers can generally be selected when creating sales e-Invoices or other revenue documents, depending on the system workflow.

---

### Pending Approval

**Pending Approval** means the customer record has been created or updated but still requires approval.

Use this status to identify customer records that need to be reviewed before they are used in production documents.

A customer may be pending approval because:

* the record was newly created
* important customer details were changed
* approval is required by internal workflow
* customer information needs to be checked before use

---

### Awaiting

**Awaiting** means the customer record is waiting for a required next step.

This may indicate that information, confirmation, verification, or another action is still pending before the record can move forward.

Users should open the customer record using **View** to understand what is still required.

---

## Entity Types

The **Entity** column shows the customer’s legal or business type.

Examples shown on the page include:

| Entity Type     | Meaning                                   |
| --------------- | ----------------------------------------- |
| Individual      | A person buying from the company          |
| Private Limited | A company or incorporated business entity |

The entity type is important because it may affect the customer details required for e-Invoice issuance, such as registration details, identification details, TIN, or other buyer information.

---

## Available Actions

### View

Click **View** to open the customer record.

Use this to review customer details such as:

* customer name
* email address
* country
* entity type
* approval status
* registration or identification details, if available
* e-Invoice buyer details
* last modified information

Users should use **View** before editing, approving, or investigating a customer record.

### Open Menu

Each customer row may also show an additional menu.

Use this menu to access row-specific actions, where available.

The exact options may depend on user permissions, customer status, and system configuration.

---

## Customer Country

The **Country** column shows the country associated with the customer.

Examples shown on the page include:

```text id="4v29ox"
Malaysia
MALAYSIA
ARUBA
AFGHANISTAN
```

The country value is important for e-Invoice reporting because different customer types or jurisdictions may require different buyer information.

For Malaysian customers, users should ensure the customer’s required local e-Invoice details are accurate.

For foreign customers, users should check that the country and entity type are correctly recorded.

---

## Last Modified

The **Last Modified** column shows when the customer record was last updated.

Use this field to check whether customer details were recently changed.

This is useful when:

* investigating why an invoice used certain customer details
* checking whether a customer profile was updated before issuing an e-Invoice
* reviewing recent customer master data changes
* confirming whether an old customer profile may need updating

---

## Pagination

The bottom of the page shows pagination controls.

Use the pagination controls to move between pages of customer records.

| Control     | Description             |
| ----------- | ----------------------- |
| Previous    | Go to the previous page |
| Page number | Jump to a specific page |
| Next        | Go to the next page     |

Example page controls shown:

```text id="893f2d"
Previous
1
2
3
4
5
...
Next
```

If there are many customer records, use search, status tabs, or filters before navigating through multiple pages.

---

## Recommended Workflows

### Add a new customer before issuing a sales e-Invoice

1. Open **Customers**.
2. Search for the customer first to check whether the record already exists.
3. If the customer does not exist, click **Add Customer**.
4. Enter the required customer details.
5. Save the customer record.
6. Check whether the customer requires approval.
7. Use the customer when creating the relevant sales e-Invoice or revenue document.

---

### Check whether a customer is ready to use

1. Open **Customers**.
2. Search for the customer name, email, or registration number.
3. Check the **Status** column.
4. If the customer is **Approved**, the record is ready for normal use.
5. If the customer is **Pending Approval** or **Awaiting**, click **View** to check what action is required.

---

### Review customers pending approval

1. Open **Customers**.
2. Click the **Pending Approval** tab.
3. Review each customer record.
4. Click **View** to inspect customer details.
5. Approve, update, or escalate the record based on internal workflow.

---

### Find customers from a specific country

1. Open **Customers**.
2. Click the **Country** filter.
3. Select the relevant country.
4. Review the filtered customer list.
5. Use **View** to inspect any customer record that needs checking.

---

### Investigate which customer was used for a sales document

1. Open **Customers**.
2. Search using the customer name, email, or registration number from the sales document.
3. Open the customer record using **View**.
4. Compare the customer details against the buyer information on the e-Invoice.
5. Check the **Last Modified** date to understand whether the customer details may have changed recently.

---

## Best Practices

* Search for an existing customer before creating a new one.
* Avoid duplicate customer records for the same buyer.
* Keep customer names, emails, countries, and entity types accurate.
* Review **Pending Approval** and **Awaiting** customers regularly.
* Confirm customer details before issuing sales e-Invoices.
* Use the **Country** filter when reviewing local versus foreign customers.
* Use **Last Modified** to identify recently changed customer records.
* Open the customer record using **View** before taking further action.
* Treat customer data as master data because it affects revenue document accuracy.

---

## Troubleshooting

### I cannot find a customer

Try the following:

1. Clear all filters.
2. Search using a shorter keyword.
3. Search by email address instead of customer name.
4. Search by registration number or identifier, if available.
5. Check all status tabs: **Approved**, **Pending Approval**, and **Awaiting**.
6. Check whether the customer may have been created under a different spelling or entity name.

---

### The customer is not available when creating an e-Invoice

Possible reasons include:

* the customer is not approved
* the customer is still pending approval
* the customer is awaiting required action
* required customer details are incomplete
* the customer was created under a different record
* filters or search terms are hiding the customer

Open the customer record using **View** to check the status and details.

---

### There are duplicate customer records

If duplicate records appear:

1. Compare the customer name, email, country, and entity type.
2. Open each record using **View**.
3. Check which record has the most accurate and complete information.
4. Confirm which record has been used in existing e-Invoices.
5. Follow the company’s internal process to update, merge, deactivate, or avoid using the duplicate record.

---

### The customer status is Pending Approval

This means the customer record needs review before it can be fully used.

Open the record using **View** and check whether any required fields, approval steps, or internal review actions are pending.

---

### The customer country or entity type looks incorrect

Open the customer record using **View** and confirm the customer details.

Incorrect country or entity type may affect e-Invoice buyer information, so the record should be corrected before issuing or submitting related sales documents.

---

## Summary

The Customers page is the customer master data page for JomeInvoice V2.

It allows users to add, view, search, filter, and review customers who buy from the company. These customer records are used as buyer information when the company records inbound revenue through sales e-Invoices and related documents.

Use this page whenever you need to create a customer, check whether a customer is approved, review customer details, or investigate customer information used in a revenue document.
