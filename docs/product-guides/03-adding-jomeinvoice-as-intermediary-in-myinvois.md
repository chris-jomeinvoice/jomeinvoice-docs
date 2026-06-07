# Adding JomeInvoice as Intermediary in MyInvois

*5 min read · Director or Company Representative · Priority*

Before JomeInvoice can submit e-invoices on your behalf, you must authorize it as your Intermediary inside the MyInvois portal. This is a one-time setup step — once done, JomeInvoice can submit, cancel, and manage invoices under your company's TIN.

> ⚠️ **Warning:** This step is done inside **MyInvois**, not JomeInvoice. Make sure you are logged in as the **Director or Business Owner** — or as the appointed Company Representative if you completed the delegation step earlier.

## JomeInvoice's credentials (copy these)

When MyInvois asks you to identify the Intermediary, use these values:

| Environment | Company Name | TIN | BRN |
| --- | --- | --- | --- |
| **Pre-prod / Testing** | JXXX\_XXXXD. | `C58501058070` | `202401003248` |
| **Production / Live** | JOM EINVOICE SDN. BHD. | `C58501058070` | `202401003248` |

## Step-by-step

1. **Log in to MyInvois and switch to your company role**

   Go to `mytax.hasil.gov.my` and log in. Under **Role Selection**, click your company name to switch from your individual role to your **Director or Business Owner** role.

   *[Screenshot: MyTax Role Selection — clicking company name to switch role]*
2. **Open MyInvois and go to Profile**

   From the MyTax dashboard, click **MyInvois** to enter the portal. Once inside, navigate to **Profile** in the top navigation.

   *[Screenshot: MyInvois portal — Profile menu]*
3. **Click "Intermediary" and add new**

   Under Profile, click **Intermediary**. This shows your list of currently authorized Intermediaries. For a first-time setup, the list is empty. Click **Add Intermediary**.

   *[Screenshot: MyInvois Intermediary list — Add Intermediary button]*
4. **Enter JomeInvoice's TIN and BRN**

   In the search form, enter:

   - **TIN:** `C58501058070`
   - **BRN:** `202401003248`

   Use the **Production/Live** values unless you are specifically testing on the preprod environment. MyInvois will validate the details and display **JOM EINVOICE SDN. BHD.** as the matched company — confirm this is correct before proceeding.

   *[Screenshot: MyInvois Add Intermediary form with JomeInvoice TIN and BRN entered]*
5. **Grant all three permission scopes**

   MyInvois will ask which actions you authorize JomeInvoice to perform on your behalf. Enable all three:

   - **Submit Documents** — required for creating and submitting invoices
   - **Cancel Documents** — required for the 72-hour cancel feature
   - **Reject Documents** — required for handling buyer rejection workflows

   > ⚠️ **Warning:** If you leave out any scope, the corresponding action in JomeInvoice will fail with a permission error. Enable all three now — you can revoke individual scopes later if needed.
6. **Confirm and save**

   Click **Submit**. JomeInvoice (JOM EINVOICE SDN. BHD.) now appears in your Intermediary list with status **Active**.

   > ℹ️ **Note:** You're done with MyTax and MyInvois setup. From here, all your e-invoicing work happens inside JomeInvoice.

## Troubleshooting

### "Intermediary not found"

The TIN or BRN you entered doesn't match. Double-check against the table above — TIN `C58501058070`, BRN `202401003248`. Make sure you're using the correct environment row.

### "You don't have permission to add an Intermediary"

You're logged in as an individual, not as the company Director/Representative. Go back to MyTax, open **Role Selection**, and click your company name to switch roles.

### "Intermediary not authorized" when submitting later

This means one of the three permission scopes is missing, or your workspace TIN was changed after authorization (making the records out of sync). Remove and re-add JomeInvoice as Intermediary in MyInvois with all three scopes checked.

### Related articles

- [→ Set up MyTax & MyInvois](01-set-up-mytax-myinvois-before-connecting-jomeinvoice.md)
- [→ Create your JomeInvoice account](02-create-your-jomeinvoice-account.md)
- [→ Why your invoice was rejected](11-why-your-invoice-was-rejected-error-codes.md)
