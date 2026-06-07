# Bulk upload invoices

*7 min read · Accountants, ops, IT · Priority*

JomeInvoice supports two invoice modules and four ways to bring invoices in. Here's how it all fits together:

How invoices flow into JomeInvoice

Inbound methods

Create

Direct Upload

SFTP

API

Invoice modules

Sales — invoices you issue to customers

Self-Billed — on behalf of suppliers

After entry

Approve & Submit → straight to LHDN

Save as Inbound Draft → submit later

Both Sales and Self-Billed invoices can be included in the same CSV upload.
[How to submit to LHDN →](07-how-to-submit-invoices-to-lhdn.md)

> ℹ️ **Note:** Direct Upload accepts **CSV format only**. You can configure field mapping so your existing CSV headers work even if they differ from JomeInvoice's standard template.

## Step-by-step

1. **Go to the invoice module**

   Open **Sales** or **Self-Billed** from the left navigation — whichever matches your invoice type. You can upload both Sales and Self-Billed invoices in the same CSV file.
2. **Select Direct Upload — Inbound**

   In the module header, select **Direct Upload** and choose **Inbound** as the direction.
3. **Click the Upload button**

   Click the **Upload** icon. A popup appears with three options:

   - **Set default field mapping** in Settings (for first-time setup)
   - **Download CSV template** — JomeInvoice's standard template with all required LHDN fields
   - **Upload your CSV file**

   *[Screenshot: Upload popup showing the three options]*
4. **Prepare and upload your CSV**

   Fill in all invoice information in the CSV — one row per line item. All fields required by LHDN must be present. If you're using your own CSV format, the field mapping step (next) handles the translation.

   Once ready, drag and drop or browse to upload the file.
5. **Review page — Section 1: Field mapping check**

   After upload, JomeInvoice opens a **Review page** with three sections. The first checks that all required LHDN field mappings are in place.

   If your CSV headers differ from JomeInvoice's standard template, or if you want to change the mapping, click **Set Field Mapping**. In the mapping panel you can:

   - Search for specific fields using the search box
   - Click **Set as New Default** — a warning dialog will appear confirming this overwrites your current default mapping in Settings. Useful if you always upload from the same source system.
   - Click **Apply for This Upload** — applies the mapping to this batch only, without changing your default. Use this for one-off or different-format uploads.

   *[Screenshot: Review page Section 1 — Field Mapping Check with Set Field Mapping panel open]*
6. **Review page — Section 2: Smart field check**

   JomeInvoice runs a smart check across all row data, validating **55 fields** for compliance with LHDN standards and rules — covering things like valid TIN formats, allowed classification codes, matching tax rates, correct UOM values, and more.

   Any field-level issue is flagged here before submission, so you can fix problems in your source CSV and re-upload rather than discovering rejections after the fact.
7. **Review page — Section 3: Validation result**

   This section shows the full picture of your upload:

   - **Pass rate** — shown as e.g. **4/5 Passed** at the top
   - **Summary by module** — separate totals for Sales and Self-Billed, each broken down by invoice type: Invoice, Credit, Debit, Refund
   - **Row-level list** — paginated at 5 invoices per page. Each row shows invoice number, amount, module, type, status, and error reason for failed rows.
   - **Select / deselect rows** — you can choose which valid rows to include in this submission and exclude others to handle separately
   - **Download errors** — download a CSV of only the failed invoices so you can fix and re-upload them

   *[Screenshot: Validation result section — pass rate, summary counts, row list with error reasons]*
8. **Submit — choose upload type**

   When you click **Submit**, choose how to upload the valid invoices:

   - **Inbound Draft** — uploads as consolidated (draft). Use this for B2C monthly consolidation batches.
   - **Approve and Submit** — submits directly to LHDN as non-consolidated invoices. Use this for standard B2B invoice submissions.

   > ⚠️ **Warning:** Choose the right upload type — Inbound Draft and Approve and Submit follow different submission flows and cannot be easily undone once submitted.
9. **Track in Import Log**

   After submitting, JomeInvoice redirects you to the **Import Log**. Each upload appears as a batch-level row. Click **View** to open the invoice-level details for that batch:

   - Search by invoice number within the batch
   - Total invoice count for the batch
   - Columns: Invoice number, Amount, Module (Sales/Self-Billed), Invoice type, Status, Error reason
   - Error reason column for failed invoices — shows exactly what went wrong per invoice
   - Export button to download the batch log as CSV

   *[Screenshot: Import Log — batch row with View modal showing invoice-level details]*

### Related articles

- [→ Create a single invoice](05-create-an-invoice.md)
- [→ Why your invoice was rejected](11-why-your-invoice-was-rejected-error-codes.md)
