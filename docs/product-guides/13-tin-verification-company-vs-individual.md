# TIN verification: company vs individual

*4 min read · All users · Priority*

TIN errors are the single most common cause of rejected invoices. The root cause is almost always the same: the TIN format doesn't match the entity type. This article gives you the reference table you need and the fix steps when it goes wrong.

## What a TIN is

A Tax Identification Number (TIN) is LHDN's unique identifier for a taxpayer — your company, a sole proprietor, an individual, a government body, or a foreign party. Every e-invoice submitted to MyInvois must reference both the issuer's TIN and the recipient's TIN.

JomeInvoice validates TINs against LHDN's database in real time. If LHDN doesn't recognize the TIN, the invoice will be rejected at submission.

## TIN format by entity type

| Entity | TIN format | Example |
| --- | --- | --- |
| Company (Sdn Bhd / Bhd) | C + 11 digits | C12345678901 |
| Sole Proprietor | EI + 11 digits | EI12345678901 |
| Individual (employee, freelancer) | IG + 11 digits | IG12345678901 |
| Government / statutory body | G + 11 digits | G12345678901 |
| Foreign party (no Malaysian TIN) | EI00000000010 (placeholder) | EI00000000010 |

The prefix is the most important part. A real C number (company) entered with the wrong prefix won't be found in LHDN's records.

## What to do on a TIN mismatch

1. **Check the entity type**

   Does the entity type in the Customer record match the TIN prefix?

   - If the customer is a Sdn Bhd, entity type must be **Company**; TIN must start with **C**
   - If the customer is a sole proprietorship, entity type is **Sole Proprietor**; TIN starts with **EI**
   - For foreign companies, entity type must be **Foreign Company** — not Malaysian Individual (a known V1-era misclassification)
2. **Use Search TIN by BRN**

   If you know the customer's BRN but not the TIN — or you suspect the TIN you have is wrong — open the Customer record and click **Search TIN**. JomeInvoice queries LHDN by BRN and returns the matching TIN.

   This is the fastest fix for older customer records where someone typed the wrong TIN years ago.
3. **Confirm with the customer**

   If neither check works, ask the customer to verify their TIN directly. They can find it on their LHDN tax documents or by logging into MyTax.

   The fastest way to get accurate TINs is to invite the customer to self-onboard — they fill in their TIN themselves and it's validated against LHDN before reaching your queue. See article 9.

## Foreign parties

Foreign companies and individuals don't have Malaysian TINs. JomeInvoice handles them with a placeholder TIN (`EI00000000010`) and relaxed validation rules:

- The TIN doesn't need to validate against LHDN's database
- The BRN format restriction is also relaxed (V2 removed the 12-digit requirement for foreign parties specifically)
- The country field must not be Malaysia

For self-billed invoices to foreign suppliers, this is the standard flow — see the Self-billed module.

## Sole Proprietor edge case

Sole Proprietor entities have a special handling: their `onbehalfof` field is stored as `TIN:BRN` rather than just TIN. This is automatic in V2 — you don't need to format it yourself — but it explains why Sole Proprietor invoices look slightly different in the LHDN submission payload.

### Related articles

- [→ Why your invoice was rejected](11-why-your-invoice-was-rejected-error-codes.md)
- [→ Invite customers / suppliers](04-invite-customers-suppliers-to-self-onboard.md)
- [→ Create a sales invoice](05-create-an-invoice.md)
