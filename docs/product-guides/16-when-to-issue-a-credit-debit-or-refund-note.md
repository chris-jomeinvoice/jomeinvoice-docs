# When to issue a Credit, Debit, or Refund Note

*4 min read · All users*

Once a sales invoice is past the 72-hour cancellation window and becomes locked, you can no longer cancel it. Instead, you issue an adjustment note — a Credit Note (CN), Debit Note (DN), or Refund Note (RN) — against the original invoice. Each serves a different purpose.

| Note type | Use when | Effect on original invoice |
| --- | --- | --- |
| **Credit Note (CN)** | You need to reduce the invoice amount — wrong price, overcharge, returned goods, or full cancellation after 72 hours | Reduces the taxable amount. Effectively negates if issued for the full amount. |
| **Debit Note (DN)** | You need to increase the invoice amount — undercharge, additional charges not in the original | Increases the taxable amount. |
| **Refund Note (RN)** | You are refunding money to the customer — not an invoice correction, but an actual payment reversal | Records the refund for tax purposes. |

> ℹ️ **Note:** CN, DN, and RN are submitted to LHDN just like regular invoices — they go through the same validation flow and receive their own UUID and QR code once valid.

## The 72-hour rule recap

- **Within 72 hours of Valid** — cancel the invoice directly. No CN/DN needed.
- **After 72 hours** — issue a Credit Note to reduce or negate, or a Debit Note to increase.
- **Refunding a payment** — issue a Refund Note regardless of timing.

## How to create CN/DN/RN in JomeInvoice
<div style="position: relative; box-sizing: content-box; max-height: 80vh; max-height: 80svh; width: 100%; aspect-ratio: 1.60; padding: 40px 0 40px 0;">
  <iframe src="https://app.supademo.com/embed/cmq49gohu1s0vqm6u9pkwzroj?embed_v=2&utm_source=embed" loading="lazy" title="Create and Submit Credit Notes on MyInvoice" allow="clipboard-write" frameborder="0" webkitallowfullscreen="true" mozallowfullscreen="true" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
</div>
Open the original invoice, click **Issue Credit / Debit / Refund Note** from the action menu, and select the note type. The note is pre-linked to the original invoice — LHDN records the relationship between the two documents automatically.

### Related articles

- [→ Cancel an invoice (72-hour rule)](10-cancel-an-invoice-within-72-hours.md)
- [→ Understanding invoice statuses](15-understanding-invoice-statuses.md)
