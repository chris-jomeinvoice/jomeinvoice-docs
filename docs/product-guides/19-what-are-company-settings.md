# Organisation

You can view your organisation structure here. All organisations will have a Main HQ, and you may add Branches if necessary.

Think of a Branch as a new shop, or a new channel.

## Main HQ - need Supademo

Here you can modify and manage your:

- Business Information
- Users assigned to receive Notifications about HQ invoices
- Secret Keys (used for APIs, applications, etc).

Editable Business Information:

- Business Name
- Business TIN
- Business BRN / SSM
- Entity Type
- Country
- Primary Business Email Contact
- Primary Business Phone Contact
- Business MSIC Code
- Business Registered Address
- (Optional) SST No.
- (Optional) Tourism Tax No.

## Branches - need Supademo

To add a new branch, you will need:

- Name of the Branch
- Address of the Branch
- (Optional) Branch Code - this is specific to your organisation structure.

How Do I Change HQ or Branch Information?

To modify an existing branch, go to Organisation and click on View next to the Branch you wish to edit.

Now, click on the Edit button.

After that, you'll be able to:

- Change the Branch Name
- Change the Branch Code
- Change the Branch Address
- Add / Remove Users from the Branch
- Change the Primary User of a Branch
- Enable / Disable / Edit specific Footers for this Branch

After that, don't forget to hit Save or your changes may be lost.

How do I set or change who will receive email notifications for the HQ or a specific Branch?

1. Go to Organisation
2. Select the HQ or Branch that you wish to change and click View
3. Now click on the Edit button
4. Go to Contact
5. If the User you want to add is not in the list, click on Select Existing Member to add them.
  1. ❗️ The User must have added their Phone Number to their account. If they haven't yet, they can do so by:
    1. Click Settings
    2. Look for Account Settings, then click Edit
    3. Add the contact number in the following format: *60161234123*

# Email Notifications

In this section, you can modify the email notifications that your Users, Customers, and Suppliers receive.

This takes the form of Email Templates for each category of notification. You can make changes to who receives the email, what the email says, how the content of the email looks, and who sent the email.

## Customisation

Header

- This is a universal image that is placed in the head (top) of each and every email notification that will be sent out.
- Most users will want to place their company logo here.

How to add, change, or remove the email logo or email header image?

1. Go to Settings
2. Find Workspace Settings, then click View
3. Click on Email Notifications
4. Find Customisation, then click on Header
5. Click Upload Logo to change to a new image.

---

WORK IN PROGRESS

---

## Invoice Template

### New Invoice

- This is the email template for when New Invoices are generated - it'll inform your customer? supplier?
- You can add CC or BCC addresses here. In-case you want to ensure certain Users receive this notification when sent.
- You can edit the From Address to make it look like your own company email address
- You can edit the Subject of the Email
- You can edit the Body of the email with minimal basic formatting.
- You can add Variables into the Body of the email in order to make the email dynamic and personalised.

#### List of Email Variables:

- invoice_type
- company_name
- customer_name
- recipient_name
- invoice_number
- invoice_date
- amount
- due_date
- currency

### Cancel Invoice

- This is the email template for when Invoices are Cancelled - internal notification? also informs customer / supplier?
- You can add CC or BCC addresses here. In-case you want to ensure certain Users receive this notification when sent.
- You can edit the From Address to make it look like your own company email address
- You can edit the Subject of the Email
- You can edit the Body of the email with minimal basic formatting.
- You can add Variables into the Body of the email in order to make the email dynamic and personalised.

#### List of Email Variables:

- invoice_type
- company_name
- customer_name
- recipient_name
- invoice_number
- invoice_date
- cancelled_date
- amount
- currency
- cancellation_reason

## Customer Template

### Invite Customer

- This is the email notification to your Customer (Buyer), inviting them to fill up their Business Profile information at JomeInvoice, so that they can be part of the e-Invoice process.
- You can add CC addresses here. In-case you want to ensure certain Users receive this notification when sent.
- You can edit the From Address to make it look like your own company email address
- You can edit the Subject of the Email
- You can edit the Body of the email with minimal basic formatting.
- You can add Variables into the Body of the email in order to make the email dynamic and personalised.

#### List of Email Variables:

- company_name
- customer_name
- recipient_name
- registration_link

### Customer Submitted

- Email notification for when your Customers (Buyer) apply to be part of your Customer List, but are pending your approval.
- You can add CC addresses here. In-case you want to ensure certain Users receive this notification when sent.
- You can edit the From Address to make it look like your own company email address
- You can edit the Subject of the Email
- You can edit the Body of the email with minimal basic formatting.
- You can add Variables into the Body of the email in order to make the email dynamic and personalised.

#### List of Email Variables:

- company_name
- customer_name
- recipient_name
- password
- login_link

### Customer Approved

- Email notification for when your Customers (Buyer) are successfully approved to be part of your Customer List.
- You can add CC addresses here. In-case you want to ensure certain Users receive this notification when sent.
- You can edit the From Address to make it look like your own company email address
- You can edit the Subject of the Email
- You can edit the Body of the email with minimal basic formatting.
- You can add Variables into the Body of the email in order to make the email dynamic and personalised.

#### List of Email Variables:

- company_name
- customer_name
- recipient_name
- login_link

## Supplier Template

### Invite Supplier

- This is the email notification to your Supplier (Seller), inviting them to fill up their Business Profile information at JomeInvoice, so that they can be part of the e-Invoice process.
- You can add CC addresses here. In-case you want to ensure certain Users receive this notification when sent.
- You can edit the From Address to make it look like your own company email address
- You can edit the Subject of the Email
- You can edit the Body of the email with minimal basic formatting.
- You can add Variables into the Body of the email in order to make the email dynamic and personalised.

#### List of Email Variables:

- company_name
- supplier_name
- recipient_name
- registration_link

### Supplier Submitted

- Email notification for when your Supplier (Seller) apply to be part of your Customer List, but are pending your approval.
- You can add CC addresses here. In-case you want to ensure certain Users receive this notification when sent.
- You can edit the From Address to make it look like your own company email address
- You can edit the Subject of the Email
- You can edit the Body of the email with minimal basic formatting.
- You can add Variables into the Body of the email in order to make the email dynamic and personalised.

#### List of Email Variables:

- company_name
- supplier_name
- recipient_name
- password
- login_link

### Supplier Approved

- Email notification for when your Supplier (Seller) are successfully approved to be part of your Customer List.
- You can add CC addresses here. In-case you want to ensure certain Users receive this notification when sent.
- You can edit the From Address to make it look like your own company email address
- You can edit the Subject of the Email
- You can edit the Body of the email with minimal basic formatting.
- You can add Variables into the Body of the email in order to make the email dynamic and personalised.

#### List of Email Variables:

- company_name
- supplier_name
- recipient_name
- login_link

## Differences between V1 and V2

- Email Logo is now managed in the Customisation > Header tab.

# User Roles

Here you can add, modify, and delete User Roles. User Roles are a set of permissions and abilities granted to specific users.

Common User Roles are

- Admins - who can do everything including make more admins
- Finance - who will can do everything related to e-Invoices but not make admins, add or remove people
- Purchasing - who will do everything related to the Supplier side.

How do I create a New User Role?

Supa Demo Link:

[https://app.supademo.com/demo/cmq3cmyz916xgqm6uz02f2r5r?utm_source=link](https://app.supademo.com/demo/cmq3cmyz916xgqm6uz02f2r5r?utm_source=link)

1. Go to Settings
2. Find Workspace Settings, then click View
3. Click on User Roles
4. Click on Create User Role
5. Fill in Name, Description, and select the appropriate permissions for this Role.

# Team

Here you can add, modify, and delete Users.

Something about Teams as well and managing them. Finance, Billing, Purchasing.

# General

Here you can manage all the General settings of JomeInvoice for your Company.

# Mappings

Here you can manage all the mappings for your file uploads. We currently have mappings for Customers, Suppliers, and Unit of Measurement.

### Related articles

- [→ Share your e-invoice request link / QR](17-share-your-e-invoice-request-link-and-qr-code.md)
- [→ Consolidated invoices (B2C rule)](12-what-consolidated-invoices-are-b2c-rule.md)
