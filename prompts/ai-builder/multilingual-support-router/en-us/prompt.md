Analyze this [support_ticket] and perform the following tasks:

1. Detect the language of the ticket (return the ISO 639-1 code, e.g. "en", "fr", "de")
2. Classify the issue into exactly one category: Billing / Technical / Account / General
3. Assess urgency: Critical / High / Normal / Low
4. Extract key entities if present: product name, error code, account ID (return null if not found)
5. Generate a brief acknowledgment reply in the SAME language as the ticket. The reply must thank the customer, confirm the category and urgency, and state that the team will respond within the expected SLA.

Return the result strictly as valid JSON using this schema:
{
  "language": "string",
  "category": "string",
  "urgency": "string",
  "entities": {
    "product": "string or null",
    "error_code": "string or null",
    "account_id": "string or null"
  },
  "reply": "string"
}

Do not include any text outside the JSON object.
