# Multilingual Support Router

## Description

This prompt processes an incoming customer support ticket and returns a structured JSON object containing the detected language, issue category, urgency level, extracted entities, and a pre-written acknowledgment reply — all in a single AI Builder call.

The key innovation is automatic language detection combined with same-language reply generation. If a ticket arrives in French, Spanish, or German, the acknowledgment reply is automatically written in that language, without requiring separate translation steps.

The strict JSON-only output format makes the result directly consumable by Power Automate flows or Power Apps without additional parsing logic.

## Prompt

> Analyze this [support_ticket] and perform the following tasks:
>
> 1. Detect the language of the ticket (return the ISO 639-1 code, e.g. "en", "fr", "de")
> 2. Classify the issue into exactly one category: Billing / Technical / Account / General
> 3. Assess urgency: Critical / High / Normal / Low
> 4. Extract key entities if present: product name, error code, account ID (return null if not found)
> 5. Generate a brief acknowledgment reply in the SAME language as the ticket.
>
> Return the result strictly as valid JSON. Do not include any text outside the JSON object.

### Supported Language(s)

- [English - US](./en-us/prompt.md)

## Authors

Solution|Author(s)
--------|---------
Multilingual Support Router | [OwnOptic](https://github.com/OwnOptic) ([@OwnOptic](https://twitter.com/OwnOptic))

## Minimal Path to Awesome

1. Navigate to [AI Builder](https://make.powerapps.com/) and select **AI Builder** > **Explore**
2. Choose **Prompt** and click **Build your own prompt**
3. Copy the content from [prompt.md](./en-us/prompt.md) and paste it into the prompt editor
4. Add an input named `support_ticket` of type **Text**
5. Test with a sample ticket in English, then try one in French or Spanish to verify multilingual output
6. Save and publish, then call this prompt from a Power Automate flow triggered by a new email or Teams message
7. Use **Parse JSON** in Power Automate with the schema above to branch logic by `category` and `urgency`

## Disclaimer

**THIS CODE IS PROVIDED *AS IS* WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.**

<img src="https://m365-visitor-stats.azurewebsites.net/powerplatform-prompts/samples/ai-builder/multilingual-support-router" aria-hidden="true" />
