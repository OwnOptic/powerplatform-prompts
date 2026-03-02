# Email to Planner Task

## Description

This Power Automate prompt creates a flow that converts flagged or starred Outlook emails into Planner tasks automatically. The task gets the email subject as its title, sender and body excerpt as context notes, an auto-calculated due date (2 business days), and the mailbox owner as assignee. A Teams notification confirms creation with a direct task link.

This solves one of the most common productivity pain points: **important emails that require action getting buried in the inbox**. The flag/star trigger respects the user's existing behavior — they already flag emails they need to act on — so no new habit is required.

## Prompt

> Build a workflow that monitors a [Start of Text]Microsoft Outlook[End of Text] mailbox and automatically creates a task in [Start of Text]Microsoft Planner[End of Text] whenever an email is flagged or starred. Task title = email subject, notes = sender + date + first 500 chars of body, due date = 2 business days after receipt, assigned to mailbox owner. Send a [Start of Text]Microsoft Teams[End of Text] notification with a direct link to the task.

### Supported Language(s)

- [English - US](./en-us/prompt.md)

## Authors

Solution|Author(s)
--------|---------
Email to Planner Task | [OwnOptic](https://github.com/OwnOptic) ([@OwnOptic](https://twitter.com/OwnOptic))

## Minimal Path to Awesome

1. Navigate to [Power Automate](https://make.powerautomate.com/) and click **Create** > **Describe it to design it**
2. Copy the content from [prompt.md](./en-us/prompt.md) and paste it into the description field
3. Review the generated flow and verify:
   - Outlook trigger: **When an email is flagged**
   - Planner action: **Create a task** with subject, body excerpt, and due date
   - Expression for due date: `addDays(triggerOutputs()?['body/receivedDateTime'], 2)` (adjust for business days)
   - Teams action: **Send a notification** with the Planner task deep link
4. Select your Planner plan and bucket in the Create Task action
5. Test by flagging an email in your Outlook inbox and confirming the task appears in Planner within seconds

## Disclaimer

**THIS CODE IS PROVIDED *AS IS* WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.**

<img src="https://m365-visitor-stats.azurewebsites.net/powerplatform-prompts/samples/power-automate/email-to-planner-task" aria-hidden="true" />
