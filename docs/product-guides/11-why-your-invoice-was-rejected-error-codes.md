# Why your invoice was rejected (error codes)

*8 min read · Anyone hitting validation errors · Priority*

This article is a quick-reference. Scan for the error you're seeing and jump to the fix. If your error isn't listed, see the bottom for escalation steps.

## Where to find error details

When an invoice is rejected, open the specific invoice and scroll to the bottom. The **Activity Trail** logs every status change and includes the full error reason for each rejection — this is the most reliable place to read exactly what LHDN returned.

*[Screenshot: Invoice page — Activity Trail at the bottom showing rejection error reason]*

## The most common errors

### TIN mismatch / TIN not found

**What it means:** The TIN you entered doesn't match what LHDN has on file. Most common cause: wrong entity prefix (using C when it should be IG, etc.).

**How to fix:** Open the Customer record, click **Verify TIN**. If that fails, click **Search TIN by BRN** — JomeInvoice will look up the correct TIN using the customer's Business Registration Number. Confirm with the customer if both fail.

### Invalid classification code

**What it means:** The classification code on your line item isn't in LHDN's current list. LHDN occasionally updates codes; pasted values may be outdated.

**How to fix:** Open the line item, clear the classification code, then pick a fresh value from the typeahead dropdown. Never paste classification codes manually.

### Country mismatch (customer)

**What it means:** The customer's registered country doesn't match the billing country, or the entity type doesn't match the country (e.g., a foreign company saved as Malaysian Individual).

**How to fix:** Open the Customer record. For non-Malaysian parties, set Entity Type to **Foreign Company** or **Foreign Individual**. Note that V2 also relaxes TIN validation and BRN format restrictions for foreign customers — they aren't required to provide Malaysian-style identifiers.

### State mapping invalid (Malaysian address)

**What it means:** The state field in your workspace or customer address doesn't map cleanly to an LHDN state code.

**How to fix:** Re-enter the state by selecting from the dropdown rather than typing. JomeInvoice will auto-convert state names to LHDN state codes. The May 2026 V2 release also added auto-conversion logic that retroactively fixes existing data using country + postcode.

### BRN/SSM format issue

**What it means:** The Business Registration Number doesn't match the expected format. V2 removed the strict 12-digit restriction, so both old and new SSM formats are now accepted — but obviously malformed values (letters in wrong places, too short) still fail.

**How to fix:** Confirm the BRN with the customer. Multiple customer codes can now share the same BRN — V2 explicitly supports this case.

### UOM (Unit of Measurement) not allowed

**What it means:** The unit of measurement isn't in LHDN's allowed list.

**How to fix:** Pick from the JomeInvoice dropdown — these are pre-mapped to LHDN values. If you have custom UOMs from V1 data, they should have been migrated automatically.

### Currency without exchange rate

**What it means:** Non-MYR currency was selected, but no exchange rate to MYR was provided.

**How to fix:** Enter the exchange rate. JomeInvoice will not auto-round — use the exact rate from your source.

### Duplicate invoice number

**What it means:** An invoice with this number already exists in your workspace. LHDN doesn't allow duplicate references within the same TIN.

**How to fix:** Change the invoice number. If you're sure this should be a separate invoice, append a suffix (INV-001-A).

### Intermediary not authorized

**What it means:** JomeInvoice doesn't have permission to submit (or cancel) on your behalf in MyInvois.

**How to fix:** See article 3 — Adding JomeInvoice as Intermediary.

### Validation 401 during upload

**What it means:** Intermittent authentication failure during SFTP/API upload — usually transient.

**How to fix:** JomeInvoice's retry mechanism now handles this automatically for queued submissions. If you see this persisting after a minute, contact support.

### Receipt validation but returned to Error folder (SFTP)

**What it means:** The receipt is technically valid but ended up in the wrong folder.

**How to fix:** This was a known bug now fixed — re-process the receipt or wait for the auto-reprocess.

## If your error isn't listed

Some errors return field-level details — read the full message in the red banner before assuming it's a generic problem. If the error is truly unfamiliar:

1. Note the exact error text
2. Open the Import Log entry for additional context
3. Contact JomeInvoice support with the invoice number and error text

### Related articles

- [→ Adding JomeInvoice as Intermediary](03-adding-jomeinvoice-as-intermediary-in-myinvois.md)
- [→ TIN verification](13-tin-verification-company-vs-individual.md)
- [→ Create a sales invoice](05-create-an-invoice.md)
