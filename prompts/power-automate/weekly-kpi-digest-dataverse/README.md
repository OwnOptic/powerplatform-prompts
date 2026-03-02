# Weekly KPI Digest from Dataverse

## Description

This Power Automate prompt creates a scheduled weekly report that queries Dataverse sales records, computes key KPIs, and distributes an HTML summary email to the sales team every Monday morning. It also handles the empty-data edge case by sending a shorter notification when no activity was recorded.

This is the first prompt in the repository to explicitly target **Dataverse** as a data source for a scheduled report — a very common enterprise automation pattern. It demonstrates how to combine scheduled triggers, Dataverse queries, aggregation logic, and HTML email formatting in a single natural-language instruction.

## Prompt

> Build a scheduled workflow that runs every Monday at 8:00 AM. Query [Start of Text]Dataverse[End of Text] to retrieve all sales opportunity records where the close date falls within the previous 7 days. Calculate the following KPIs: total revenue from won opportunities, total number of opportunities closed, number of won versus lost, and average deal size. Format the results into an HTML email with a summary table and a brief performance comment. Send the email via [Start of Text]Outlook[End of Text] to a distribution list. If no opportunities were closed in the past 7 days, send a shorter email noting that no activity was recorded for the week.

### Supported Language(s)

- [English - US](./en-us/prompt.md)

## Authors

Solution|Author(s)
--------|---------
Weekly KPI Digest from Dataverse | [OwnOptic](https://github.com/OwnOptic) ([@OwnOptic](https://twitter.com/OwnOptic))

## Minimal Path to Awesome

1. Navigate to [Power Automate](https://make.powerautomate.com/) and click **Create** > **Describe it to design it**
2. Copy the content from [prompt.md](./en-us/prompt.md) and paste it into the description field
3. Review the generated flow and verify the following steps:
   - Recurrence trigger: **Every Monday at 8:00 AM**
   - Dataverse action: **List rows** on the Opportunity table with a date filter
   - Variable actions to compute totals, counts, and average deal size
   - Condition: Check if the result set is empty
   - HTML email composition (true branch: full table, false branch: no activity message)
   - Outlook action: **Send an email (V2)**
4. Set the distribution list email address in the Outlook action
5. Adjust the Dataverse table name and column names to match your environment's schema
6. Test by manually running the flow and reviewing the email output

## Disclaimer

**THIS CODE IS PROVIDED *AS IS* WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.**

<img src="https://m365-visitor-stats.azurewebsites.net/powerplatform-prompts/samples/power-automate/weekly-kpi-digest-dataverse" aria-hidden="true" />
