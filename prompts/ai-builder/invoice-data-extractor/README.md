# Invoice Data Extractor

## Description

This prompt uses AI Builder's **image input** capability to extract structured data from invoice images or scanned PDFs. It returns a complete JSON object with all billing fields — vendor, line items, totals, tax, currency, and payment terms — ready for direct consumption by Power Automate without manual data entry.

This is the first prompt in the repository to use an **image-type input** (`invoice_image`) rather than text. It demonstrates how AI Builder's multimodal capabilities can replace dedicated OCR or document processing pipelines for common finance automation scenarios.

A null value is returned for any field not found on the invoice, making the output safe to use in downstream flow conditions without causing parse errors.

## Prompt

> You are an invoice processing assistant. Analyze the [invoice_image] provided and extract all relevant billing information. Return the result strictly as valid JSON with fields: invoice_number, invoice_date, due_date, vendor_name, vendor_address, bill_to, line_items (array), subtotal, tax_amount, tax_rate, total_due, currency, payment_terms. Set missing fields to null.

### Supported Language(s)

- [English - US](./en-us/prompt.md)

## Authors

Solution|Author(s)
--------|---------
Invoice Data Extractor | [OwnOptic](https://github.com/OwnOptic) ([@OwnOptic](https://twitter.com/OwnOptic))

## Minimal Path to Awesome

1. Navigate to [AI Builder](https://make.powerapps.com/) and select **AI Builder** > **Explore**
2. Choose **Prompt** and click **Build your own prompt**
3. Copy the content from [prompt.md](./en-us/prompt.md) and paste it into the prompt editor
4. Add an input named `invoice_image` of type **Image**
5. Test by uploading a sample invoice image (PNG or JPEG)
6. Save and publish the prompt
7. Use it in a Power Automate flow:
   - Trigger: **When an email with attachment arrives** (Outlook) or **When a file is created** (SharePoint)
   - Action: Call this AI Builder prompt, passing the attachment as the image input
   - Action: **Parse JSON** with the schema above
   - Action: Create a record in Dataverse or post to an AP system

## Disclaimer

**THIS CODE IS PROVIDED *AS IS* WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.**

<img src="https://m365-visitor-stats.azurewebsites.net/powerplatform-prompts/samples/ai-builder/invoice-data-extractor" aria-hidden="true" />
