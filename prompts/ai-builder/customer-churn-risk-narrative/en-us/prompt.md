You are a customer success analyst. Based on the following customer signals, generate a clear churn risk narrative that a non-technical account manager can act on immediately.

Customer signals provided:
- Last login date: [last_login_date]
- Support tickets opened in last 90 days: [ticket_count]
- Last support ticket sentiment: [ticket_sentiment]
- Contract renewal date: [renewal_date]
- Product usage trend (last 3 months): [usage_trend]
- NPS score (if available): [nps_score]
- Account tier: [account_tier]

Think step by step:
Step 1 — Assess each signal individually: is it a warning sign, neutral, or positive indicator?
Step 2 — Identify which signals carry the most weight for churn prediction.
Step 3 — Determine the overall churn risk level: Critical / High / Medium / Low.
Step 4 — Write a 2–3 sentence plain-English narrative explaining WHY this customer is at risk (or not).
Step 5 — Recommend exactly 3 concrete actions the account manager should take this week, ordered by urgency.

Format your output exactly as:

## Churn Risk: [Critical | High | Medium | Low]

## Why
[2–3 sentence narrative]

## Recommended Actions This Week
1. [Action — be specific, include a suggested channel: call, email, in-app message]
2. [Action]
3. [Action]

## Signal Summary
| Signal | Status |
|--------|--------|
| Last Login | [Positive / Neutral / Warning] |
| Support Tickets | [Positive / Neutral / Warning] |
| Ticket Sentiment | [Positive / Neutral / Warning] |
| Renewal Proximity | [Positive / Neutral / Warning] |
| Usage Trend | [Positive / Neutral / Warning] |
| NPS | [Positive / Neutral / Warning / N/A] |
