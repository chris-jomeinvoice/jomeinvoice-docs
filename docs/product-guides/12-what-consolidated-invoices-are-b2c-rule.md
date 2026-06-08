# What consolidated invoices are (B2C rule)

*4 min read · B2C SMEs (retail, F&B, fuel) · Priority*

If you run a B2C business — retail shop, restaurant, café, fuel station, parking lot — you do not need to issue an e-invoice for every single transaction. LHDN allows you to **consolidate all your B2C receipts for the month into a single e-invoice**, submitted once per month.

This article explains why, who it applies to, the one exception, and how it works in JomeInvoice.

## The rule, in one sentence

For walk-in customers who do not request a proper e-invoice, you may consolidate all sales receipts for the month into a single monthly e-invoice — submitted to LHDN by the 7th of the following month.

## Who this applies to

- Retail stores (clothing, supermarkets, electronics)
- F&B (restaurants, cafés, hawker stalls with POS)
- Fuel stations
- Parking operators
- Any business where most customers don't ask for an invoice

If you primarily sell B2B (other businesses are your customers), this doesn't apply to you — issue regular sales invoices.

## The one exception

If a customer asks for a proper e-invoice within 72 hours of their purchase, you must issue one specifically for that transaction. Their request goes through JomeInvoice's Request module — they scan a QR code or follow a link, fill in their TIN, and you approve.

When you approve a request and convert it to a proper e-invoice, that receipt is automatically *excluded* from the monthly consolidation — preventing double-counting.

## How the consolidation flow works in JomeInvoice

JomeInvoice handles consolidation in three stages: **Tagging → Conversion → Submission**.

1. **Tagging — review receipts**

   Throughout the month, your POS or accounting system sends individual receipts into JomeInvoice (via SFTP, API, or direct upload). They land in **Console → Tagging**.

   Each receipt shows the amount and date. JomeInvoice displays a running total of the receipts in the tagging stage so you can see the consolidation's size before you proceed.

   You can exclude any receipt — for example, if a customer already requested a proper e-invoice through the Request module, that receipt should be excluded here.
2. **Conversion — generate the consolidated draft**

   When you're ready (typically at month-end), click **Convert**. JomeInvoice creates a draft consolidated invoice per branch — so if you operate 5 outlets, you'll get 5 separate consolidations, one for each branch.

   Review the totals on each draft. You can still make edits before submission.
3. **Submission — submit to LHDN**

   Submit each draft. JomeInvoice sends them to LHDN; status moves from Draft → Pending → Valid (or Invalid with reason).

   Once Valid, the consolidated invoices are your tax records for that month's B2C sales.

> [!NOTE] 
> JomeInvoice doesn't lock you into the current month. If you missed a previous month, you can still go back and consolidate it from the Console.

## Common questions

### What if I issued some real e-invoices and some receipts in the same month?

That's normal. The real e-invoices are independent and already submitted. The receipts (the ones where customers didn't request anything) all go into the monthly consolidation. The two never overlap.

### What about returns or refunds during the month?

Returns/refunds on consolidated B2C transactions are netted into the monthly total before submission. For real e-invoices that need adjustment, issue a Refund Note (RN) against the specific invoice.

### Does JomeInvoice remind me to consolidate?

You can configure team notifications under **Settings → Team → Notifications** to alert specific team members at month-end. This is especially useful for chain operators.

### Related articles

- [→ Create a sales invoice (for B2B)](05-create-an-invoice.md)
- [→ Cancel an invoice within 72 hours](10-cancel-an-invoice-within-72-hours.md)
