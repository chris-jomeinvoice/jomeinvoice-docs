# Create your JomeInvoice account

*4 min read · Anyone (you'll become Admin) · Priority*

Once you've completed the MyTax and MyInvois setup, creating your JomeInvoice account takes just a few minutes. The flow is: sign up → verify email → create your workspace → verify your workspace with LHDN details. After that, you're ready to issue your first e-invoice.

> [!NOTE]
> Make sure you've completed the MyTax and MyInvois setup first — including adding JomeInvoice as your Intermediary. [Start here →](01-set-up-mytax-myinvois-before-connecting-jomeinvoice.md)

## Part 1 — Sign up

1. **Go to the sign-up page**

   Visit `https://v2.jomeinvoice.my/auth/register`. Enter your work email and choose a password. The email you use here becomes the Admin email for your workspace.
2. **Verify your email**

   JomeInvoice sends a verification email — usually within seconds. Click the link in the email to confirm your account. You'll be redirected back into JomeInvoice, logged in.

## Part 2 — Create your workspace

A **workspace** represents one legal entity — one company with one set of LHDN credentials. If you operate multiple Sdn Bhds, you'll create one workspace per company.

To create a workspace, you only need three things:

1. **Company name**

   Enter your registered legal name exactly as it appears on SSM.
2. **BRN / SSM**

   Your Business Registration Number from SSM. Both old and new SSM formats are accepted.
3. **Country**

   Select your company's country of registration. For most users, this is Malaysia.

Click **Create workspace**. Your workspace is created and you land on the dashboard.

[*[Screenshot: Create workspace form — Company Name, BRN/SSM, Country]*](https://api.scalar.com/cdn/images/fYzj9LUlX1c7mY4tkVrDg/4la8gEcCQsavwivPpXGWk.jpeg)

## Part 3 — Verify your workspace

Creating the workspace gets you in the door, but before JomeInvoice can submit invoices to LHDN on your behalf, you need to verify the workspace with your LHDN details. This is a separate step.

Go to **Settings → Workspace** and complete the four verification fields:

1. **TIN — Tax Identification Number**

   Enter your company TIN including the entity prefix (e.g. `C12345678901` for a company). JomeInvoice validates this against LHDN in real time — a green tick confirms LHDN recognizes it.

   Not sure of your TIN format? See [TIN verification: company vs individual →](13-tin-verification-company-vs-individual.md)
2. **Entity type**

   Select the type that matches your company: Company, Sole Proprietor, Individual, Government, or Foreign. This must match the prefix in your TIN.
3. **MSIC code**

   Your 5-digit Malaysia Standard Industrial Classification code. This describes your business activity (e.g. `47110` for retail stores). You can look yours up from the SSM or LHDN classification list.
4. **Registered address**

   Enter your company's registered address — country, state, city, postcode. JomeInvoice automatically converts your state name to the LHDN-required state code, so you just select from the dropdown.

Click **Save & Verify**. Once verified, your workspace status turns active and you're ready to create invoices.

> [!NOTE] 
> Workspace verified — you can now create invoices, add customers and suppliers, and start submitting to LHDN through JomeInvoice.

## Adding team members

If you want colleagues to access the workspace, go to **Settings → Team** and invite them by email. You can assign branch-level access so each person only sees invoices from their location.

### Related articles

- [→ Add JomeInvoice as Intermediary](03-adding-jomeinvoice-as-intermediary-in-myinvois.md)
- [→ Create your first sales invoice](05-create-an-invoice.md)
- [→ TIN verification: company vs individual](13-tin-verification-company-vs-individual.md)
