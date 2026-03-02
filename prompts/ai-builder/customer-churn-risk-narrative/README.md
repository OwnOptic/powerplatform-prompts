# Customer Churn Risk Narrative

## Description

This prompt takes six quantitative customer signals (login recency, support ticket volume and sentiment, renewal date, usage trend, NPS) and transforms them into a plain-English churn risk narrative with a risk level, a 2–3 sentence explanation, and three concrete actions ordered by urgency — all formatted for a non-technical account manager.

This combines two patterns: **chain-of-thought reasoning** (five explicit internal steps before output) and **multi-signal synthesis** (converting raw metrics into a human-readable story). It bridges the gap between a predictive model that outputs a score and a person who needs to know *what to do next*.

The direct business ROI is retention: catching a "Critical" or "High" risk account a week earlier can prevent churn that costs many times the cost of an intervention.

## Prompt

> You are a customer success analyst. Based on [last_login_date], [ticket_count], [ticket_sentiment], [renewal_date], [usage_trend], [nps_score], and [account_tier], think step by step to assess each signal, determine overall churn risk (Critical/High/Medium/Low), write a plain-English narrative, and recommend 3 concrete actions ordered by urgency.

### Supported Language(s)

- [English - US](./en-us/prompt.md)

## Authors

Solution|Author(s)
--------|---------
Customer Churn Risk Narrative | [OwnOptic](https://github.com/OwnOptic) ([@OwnOptic](https://twitter.com/OwnOptic))

## Minimal Path to Awesome

1. Navigate to [AI Builder](https://make.powerapps.com/) and select **AI Builder** > **Explore**
2. Choose **Prompt** and click **Build your own prompt**
3. Copy the content from [prompt.md](./en-us/prompt.md) and paste it into the prompt editor
4. Add the following inputs of type **Text**: `last_login_date`, `ticket_count`, `ticket_sentiment`, `renewal_date`, `usage_trend`, `nps_score`, `account_tier`
5. Save and publish the prompt
6. Integrate with Power Automate on a weekly scheduled flow:
   - Query Dataverse (or Dynamics 365) for all active accounts
   - For each account, pass the signals to this AI Builder prompt
   - Parse the output and update a `Churn Risk` column in Dataverse
   - For accounts where risk is "Critical" or "High", send a Teams notification to the responsible account manager with the narrative and recommended actions
7. Optionally surface the output in a Power Apps dashboard for the CS team

## Disclaimer

**THIS CODE IS PROVIDED *AS IS* WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.**

<img src="https://m365-visitor-stats.azurewebsites.net/powerplatform-prompts/samples/ai-builder/customer-churn-risk-narrative" aria-hidden="true" />
