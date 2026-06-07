# Understanding invoice statuses

*3 min read · All users*

Every invoice in JomeInvoice has a status that tells you exactly where it is in its lifecycle — from the moment you create it to after LHDN validates it. Knowing what each status means tells you what action to take next.

| Status | What it means | What to do |
| --- | --- | --- |
| **Inbound Draft** | Invoice is inside JomeInvoice, not yet submitted to LHDN | Review and submit — either Approve and Submit or Consolidate |
| **Pending** | Submitted to LHDN, awaiting validation response | Wait — usually resolves within 30 seconds. JomeInvoice retries automatically if stuck. |
| **Valid** | LHDN accepted. UUID and QR code issued. | Send to customer. 72-hour cancel window starts now. |
| **Invalid** | LHDN rejected with a validation error | Check Activity Trail for error reason, fix, and resubmit |
| **Cancelled** | You cancelled within 72 hours of Valid | Reissue a new corrected invoice if needed |
| **Rejected** | Your customer rejected the invoice within 72 hours | Investigate reason and reissue or issue a CN/DN |

## The standard lifecycle

Inbound Draft

Pending

Valid

Sent to customer

## Inbound vs Outbound

In JomeInvoice, invoices also have an **Inbound** or **Outbound** direction:

- **Inbound** — the invoice has entered JomeInvoice but has not yet been submitted to LHDN. This includes Inbound Draft.
- **Outbound** — the invoice has been submitted from JomeInvoice to LHDN. This includes Pending, Valid, Invalid, Cancelled, and Rejected.

### Related articles

- [→ Why your invoice was rejected](11-why-your-invoice-was-rejected-error-codes.md)
- [→ Resubmitting sales invoices](08-resubmitting-sales-invoices.md)
- [→ Cancel an invoice (72-hour rule)](10-cancel-an-invoice-within-72-hours.md)
