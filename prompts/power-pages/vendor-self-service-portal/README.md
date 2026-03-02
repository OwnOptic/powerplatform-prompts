# Vendor Self-Service Portal

## Description

This Power Pages Copilot prompt creates an authenticated vendor portal for procurement teams. Vendors can register, upload compliance documents, track their purchase orders and payment status, and submit invoices. The portal dashboard includes expiry alerts for certifications about to expire.

This prompt introduces two patterns not found in other Power Pages samples: **authenticated access** (vendors must create an account) and **document lifecycle management** (upload, expiry tracking, status monitoring). It represents a realistic B2B procurement scenario suitable for manufacturing, retail, and professional services organizations.

## Prompt

> As a procurement manager, I need a secure vendor self-service portal where suppliers can register their company with contact details and tax ID, upload compliance certifications and insurance documents, view the status of their submitted purchase orders, and submit invoices against approved purchase orders. The portal should include a vendor dashboard showing open purchase orders, payment status (Pending, Processing, Paid), and document expiry alerts for certifications due to expire within 30 days. Use a professional, corporate design with the company's neutral color palette. Require vendors to create an account before accessing the portal.

### Supported Language(s)

- [English - US](./en-us/prompt.md)

## Authors

Solution|Author(s)
--------|---------
Vendor Self-Service Portal | [OwnOptic](https://github.com/OwnOptic) ([@OwnOptic](https://twitter.com/OwnOptic))

## Minimal Path to Awesome

1. Navigate to [Power Pages](https://make.powerpages.microsoft.com/) and click **Create a site**
2. Select **Describe your site with Copilot**
3. Copy the content from [prompt.md](./en-us/prompt.md) and paste it as the site description
4. Review the generated pages and verify:
   - Vendor registration page (company name, contact, tax ID)
   - Document upload page (certifications, insurance)
   - Purchase order status page with payment status badges
   - Invoice submission form
   - Dashboard with expiry alerts (30-day window)
5. Configure **Power Pages authentication**: enable external identity providers (Azure AD B2C or local account)
6. Set page-level permissions so dashboard and submission pages require a signed-in vendor account
7. Connect the invoice submission to a Power Automate flow that notifies the accounts payable team
8. Configure a scheduled Power Automate flow to send email alerts 30 days before document expiry
9. Publish and share the portal URL with your vendor onboarding communication

## Disclaimer

**THIS CODE IS PROVIDED *AS IS* WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.**

<img src="https://m365-visitor-stats.azurewebsites.net/powerplatform-prompts/samples/power-pages/vendor-self-service-portal" aria-hidden="true" />
