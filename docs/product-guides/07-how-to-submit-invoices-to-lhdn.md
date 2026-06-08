# How to submit invoices to LHDN

*6 min read · All users · Priority*

Once invoices are inside JomeInvoice — whether created manually, uploaded via CSV, sent through SFTP, or pushed via API — you need to submit them to LHDN. There are two paths depending on whether you are submitting individual B2B invoices or consolidating B2C receipts.

| Path | Use when | Flow |
| --- | --- | --- |
| **Approve and Submit** | B2B invoices — submit each invoice to LHDN immediately | Inbound → Outbound Queue → LHDN |
| **Consolidate** | B2C receipts — batch and submit monthly as one consolidated invoice | Inbound Draft → Tag → Convert → Submit → Outbound Queue → LHDN |

## Path 1 — Approve and Submit (non-consolidated)

Use this for standard B2B invoices. The invoice goes straight from JomeInvoice to LHDN without any consolidation step.

1. **Bring invoices into JomeInvoice**

   Via any inbound method — Create (+button), Direct Upload, SFTP, or API. At the point of entry you have two options:

   - **Approve and Submit** — submits directly to LHDN immediately
   - **Save as Inbound Draft** — holds the invoice in JomeInvoice for you to review and submit later
2. **Submit Inbound Draft invoices (if saved as draft)**

   If you saved invoices as Inbound Draft and want to submit them as non-consolidated, go to the invoice module and click **Bulk Actions → Submit to Non-Consolidated**. JomeInvoice will submit the selected invoices to LHDN.

   *[Screenshot: Bulk Actions menu — Submit to Non-Consolidated option]*
3. **Invoice moves to Outbound Queue**

   JomeInvoice places the invoice in the **Outbound Queue** and submits it to LHDN. Status transitions from Pending → Valid (accepted) or Invalid (rejected with error).

## Path 2 — Consolidate (B2C monthly submission)

Use this for B2C receipts where customers did not individually request an e-invoice. You batch all receipts for the month and submit one consolidated invoice to LHDN. The flow has three stages: **Tag → Convert → Submit**.

To start: go to your invoice module, click **Bulk Actions → Consolidate Invoice**. This tags all eligible Inbound Draft invoices and opens the review flow.

*[Screenshot: Invoice module — Bulk Actions dropdown with Consolidate Invoice option]*

1. **Stage 1 — Tag invoices**

   After clicking Consolidate Invoice, JomeInvoice tags all Inbound Draft invoices and presents them for review. On this screen:

   - **Total selected** — invoices included in this consolidation
   - **Total excluded** — invoices automatically excluded because their amount exceeds **RM10,000**. LHDN requires individual e-invoices for transactions above this threshold, so they cannot be consolidated.
   - You can **cancel the tagging** of individual invoices if you want to remove specific ones from this batch before proceeding.

   *[Screenshot: Tag stage — showing selected count, excluded count, and individual invoice rows]*
2. **Stage 2 — Convert invoices**

   Before converting, set the **consolidated format** — how your receipts will be structured in the consolidated invoice:

   ### Option A: Range of receipts per line item

   Set a **consolidated range limit** — the maximum number of invoices per sub-consolidated invoice. The maximum is **300 invoices per sub-consolidated invoice**.

   For example, if you have 3,000 invoices and set the limit to 300, JomeInvoice creates **10 sub-consolidated invoices**, all grouped under one parent consolidated invoice.

   You can delete individual sub-consolidated invoices from this view — deleted sub-invoices flow back to Inbound Draft so you can handle them separately.

   ### Option B: Single receipt per line item

   Each receipt becomes its own line item in the consolidated invoice. Use this when you need a more granular breakdown in the submission.

   *[Screenshot: Convert stage — consolidated format options and sub-consolidated invoice list]*
3. **Stage 3 — Submit to LHDN**

   At the submit stage, you have three options:

   - **Submit** — sends the consolidated invoice to LHDN. It moves to the Outbound Queue and is submitted to MyInvois.
   - **Export CSV** — download the consolidated invoice data as a CSV before submitting, for internal records or review.
   - **Revert** — undo this consolidation and send all invoices back to Inbound Draft. Use this if you need to make changes before submitting.

   > [!WARNING] 
   > Once you click Submit and the consolidated invoice reaches LHDN, it cannot be reverted. Use the Revert option before submitting if you need to make any changes.

   *[Screenshot: Submit stage — Submit, Export CSV, and Revert options]*

## After submission — Outbound

Whether submitted via Approve and Submit or Consolidate, all invoices flow through the **Outbound** section of the module after submission. Here you can track the submission status, see LHDN validation results, and identify any invoices that were rejected.

### Related articles

- [→ Create an invoice](05-create-an-invoice.md)
- [→ Bulk upload invoices](06-bulk-upload-invoices.md)
- [→ Cancel an invoice (72-hour rule)](10-cancel-an-invoice-within-72-hours.md)
- [→ Why your invoice was rejected](11-why-your-invoice-was-rejected-error-codes.md)
