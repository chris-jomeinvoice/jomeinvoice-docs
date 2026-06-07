# Invite customers / suppliers to self-onboard

*3 min read · Ops, accountants · Priority*

The fastest, most accurate way to add a customer or supplier to your JomeInvoice CRM is not to type their details yourself — it's to send them a link and let them fill it in. This article explains why and how.

## Why self-onboarding beats manual entry

When you type a customer's TIN, BRN, address, and contact info yourself, you're guessing. Even if you have an old invoice from them, the details might be outdated. Wrong TIN means rejected invoices later — which costs you time, not them.

When the customer fills in their own details, they're working from their actual SSM and LHDN records. Errors drop dramatically. JomeInvoice then validates the TIN against LHDN automatically — so by the time the record appears in your CRM, it's already verified.

## Step-by-step

1. **Open the Customer or Supplier list**

   Go to **Customer** (for buyers) or **Supplier** (for vendors). Click **+ Invite** at the top.
2. **Enter their email and customer code**

   Two fields:

   - **Email** — where the onboarding link gets sent
   - **Customer code** (optional) — your internal reference; useful if you want to match their record to an existing accounting system entry

   You can also include a short personal message. JomeInvoice sends a branded email with the JomeInvoice logo (the May 2026 release fixed an earlier bug where the logo failed to render).
3. **The customer fills in their details**

   They click the link, land on a JomeInvoice self-onboarding page (no login required), and fill in:

   - Legal name (matching SSM)
   - TIN — validated against LHDN in real time
   - BRN/SSM
   - Entity type
   - Address
   - Contact email and phone

   If their TIN validation fails, they see an error immediately — meaning they fix it on their side before it ever reaches your queue.

   > ℹ️ **Note:** If your customer's onboarding link returns an error when they click it, this was a known bug in early V2 builds — now fixed in the May 2026 release.
4. **Approve in the Pending Approval queue**

   Once they submit, the record appears in your **Pending Approval** queue. You review and approve. The customer is now active and selectable in invoice creation.

   If you reject (because something looks off), the customer is notified and can resubmit. See "Re-invite after rejection" for that flow.

## Re-inviting existing customers

If you re-invite a customer who's already approved, JomeInvoice no longer overwrites their existing data. The original record is preserved — re-invitation is now safe, even by accident.

## Bulk invites

For inviting many customers at once, use the Bulk Import feature instead: upload a CSV of emails, and JomeInvoice sends invites to all of them in one operation.

### Related articles

- [→ TIN verification](13-tin-verification-company-vs-individual.md)
- [→ Create a sales invoice](05-create-an-invoice.md)
