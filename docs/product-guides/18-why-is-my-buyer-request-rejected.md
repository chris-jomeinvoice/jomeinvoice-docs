# Why is my buyer request rejected

*2 min read · B2C businesses*

A buyer's request for an e-invoice can be rejected by you (the merchant) or blocked automatically by JomeInvoice. Here are the reasons and what to do.

## Automatic blocks by JomeInvoice

| Reason | Why it happens | What to do |
| --- | --- | --- |
| 72-hour window expired | The customer requested more than 72 hours after the original purchase | Nothing — LHDN does not allow retroactive individual e-invoices for consolidated B2C transactions after the window closes |
| Invoice already has a CN/DN/RN | The underlying transaction already has an adjustment note issued against it | Advise the customer — the original invoice has already been adjusted |
| Transaction already consolidated | The receipt was already included in a monthly consolidated invoice submission | The customer cannot request after consolidation. Advise them to request within 72 hours next time. |

## When you (the merchant) reject a request

You can manually reject a buyer request from the **Request → Pending** queue. When rejecting, enter a reason — the customer is notified. Common reasons to reject:

- The TIN the customer provided doesn't match their company name
- The transaction amount doesn't match your records
- Duplicate request for the same transaction

### Related articles

- [→ Share your e-invoice request link / QR](17-share-your-e-invoice-request-link-and-qr-code.md)
- [→ Consolidated invoices (B2C rule)](12-what-consolidated-invoices-are-b2c-rule.md)
