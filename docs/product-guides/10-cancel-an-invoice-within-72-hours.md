# Cancel an invoice (within 72 hours)

*3 min read · All users · Priority*

If you issue an invoice and realize it's wrong — incorrect amount, wrong customer, duplicate, anything — LHDN gives you a 72-hour window to cancel it cleanly. After that window closes, you must issue a Credit Note (CN) or Debit Note (DN) instead.

> 🚨 **Important:** The 72-hour countdown starts from the moment your invoice transitions to *Valid* — not from when you created it. If you submitted at 10am Monday and LHDN validated at 10:01am, your deadline is 10:01am Thursday.

## When you can cancel

- Status is **Valid** (cancellation has no meaning for Pending or Invalid)
- You're within 72 hours of the Valid timestamp
- The invoice has no Credit Note, Debit Note, or Refund Note already issued against it

## When you can't (and what to do instead)

- **72 hours has passed** → issue a Credit Note to negate the invoice, then issue a new correct invoice. Or issue a Debit Note if the original amount needs adjustment upward.
- **Buyer already requested an e-invoice tied to this** → e-invoice requests are blocked when the underlying invoice has any CN/DN/RN, so this scenario should be rare

## Step-by-step

1. **Find the invoice**

   Go to **Sales → Valid** tab. The "Valid hours" column shows how much time you have left to cancel — for example, "12 hours" means 12 of the 72 have already elapsed. Click the invoice to open it.

   > ℹ️ **Note:** If "Valid hours" shows an incorrect number after resubmission, the V2 May 2026 release fixed this calculation. Refresh to see the corrected value.
2. **Click "Cancel invoice"**

   The button appears in the top-right action menu of the invoice page. It's only present if the 72-hour window is still open — if it's missing, the window has closed.
3. **Enter cancellation reason**

   LHDN requires a reason for every cancellation. Be specific — "wrong amount" is fine, but "test" or "mistake" may invite audit questions later. The reason is stored permanently against the invoice.

   *[Screenshot: Cancellation reason modal with example reason]*
4. **Confirm**

   JomeInvoice sends the cancel request to LHDN. Within seconds, the status moves to *Cancelled*.

   The cancelled invoice remains visible in your records (you can't delete it — LHDN requires the audit trail) but is no longer valid for tax purposes. You can reissue a corrected invoice immediately under a new invoice number.

## What if 72 hours has passed?

Issue a Credit Note. From the original invoice page, click **Issue Credit Note**. This creates a new e-invoice that negates the original — for accounting and LHDN purposes, the two cancel out. You then issue a fresh sales invoice with the correct figures under a new invoice number.

The CN/DN/RN module covers this in detail.

### Related articles

- [→ Create a sales invoice](05-create-an-invoice.md)
- [→ Why your invoice was rejected](11-why-your-invoice-was-rejected-error-codes.md)
