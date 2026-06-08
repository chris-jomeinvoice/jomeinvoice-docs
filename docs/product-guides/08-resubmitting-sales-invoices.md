# Resubmitting sales invoices

*3 min read · All users · Priority*

When an invoice is rejected by LHDN — or fails validation before submission — you can fix the issue and resubmit without creating a new invoice from scratch. This article covers when and how to resubmit.

## When to resubmit

- Invoice status is **Invalid** — LHDN rejected the submission with an error
- Invoice is in **Inbound Draft** and failed smart field validation during upload
- You corrected the data (e.g. fixed a TIN, changed a classification code) and want to try again

> [!NOTE] 
> You cannot resubmit a **Cancelled** invoice. If an invoice was cancelled within the 72-hour window, you must create a new one.

## How to resubmit

1. **Open the rejected invoice**

   Go to the Sales module and filter by **Invalid** status. Click the invoice to open it.
2. **Check the Activity Trail for the error reason**

   Scroll to the bottom of the invoice page and read the **Activity Trail**. The error reason from LHDN is logged here — this tells you exactly what to fix before resubmitting.

   *[Screenshot: Invoice Activity Trail showing LHDN rejection reason]*
3. **Edit and fix the invoice**

   Click **Edit** to open the invoice form. Fix the field that caused the rejection — common fixes include:

   - Correcting the customer TIN or entity type
   - Selecting the correct classification code from the dropdown
   - Updating the UOM to an LHDN-allowed value
   - Adding a missing exchange rate for non-MYR invoices

   Not sure what caused the error? See [Why your invoice was rejected →](11-why-your-invoice-was-rejected-error-codes.md)
4. **Resubmit**

   Click **Submit to LHDN**. The invoice status returns to **Pending** while LHDN revalidates. If the fix was correct, it transitions to **Valid**.

## Resubmitting a bulk upload failure

For invoices that failed during a CSV upload, download the error file from the Import Log (the Export button in the batch View modal). Fix the data in the CSV and re-upload. JomeInvoice deletes the original failed record automatically to prevent duplicates.

### Related articles

- [→ Why your invoice was rejected](11-why-your-invoice-was-rejected-error-codes.md)
- [→ Bulk upload invoices](06-bulk-upload-invoices.md)
- [→ Cancel an invoice (72-hour rule)](10-cancel-an-invoice-within-72-hours.md)
