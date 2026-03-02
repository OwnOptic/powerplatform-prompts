# Document Approval with Escalation

## Description

This Power Automate prompt generates a document approval workflow with automatic timeout escalation. The flow monitors a SharePoint library for new uploads, routes each document to the correct reviewer based on a lookup list, waits 48 hours, and escalates to the department manager if no response is received. The final approval status is written back to SharePoint and posted to a Teams channel.

The **timeout-and-escalate** pattern is one of the most commonly needed approval designs but is missing from the repository. This prompt demonstrates how to describe multi-stage conditional approval logic in a single natural-language instruction.

## Prompt

> Build a workflow that monitors a [Start of Text]SharePoint[End of Text] document library for newly uploaded files. When a file is added, look up the designated reviewer for that document from a [Start of Text]SharePoint[End of Text] list that maps document types to reviewers. Send the reviewer an approval request with a link to the file. If the reviewer does not respond within 48 hours, automatically escalate by sending a new approval request to the department manager. Once a final decision is made, update the document's approval status column in [Start of Text]SharePoint[End of Text] and post a message to a [Start of Text]Microsoft Teams[End of Text] channel with the document name, decision, and reviewer name.

### Supported Language(s)

- [English - US](./en-us/prompt.md)

## Authors

Solution|Author(s)
--------|---------
Document Approval with Escalation | [OwnOptic](https://github.com/OwnOptic) ([@OwnOptic](https://twitter.com/OwnOptic))

## Minimal Path to Awesome

1. Navigate to [Power Automate](https://make.powerautomate.com/) and click **Create** > **Describe it to design it**
2. Copy the content from [prompt.md](./en-us/prompt.md) and paste it into the description field
3. Review the generated flow and verify the following steps are present:
   - SharePoint trigger: **When a file is created**
   - SharePoint action: **Get items** (reviewer lookup list)
   - Approval action: **Start and wait for an approval**
   - Delay action: **48-hour wait**
   - Condition: Check approval response
   - Parallel branch for escalation approval
   - SharePoint action: **Update file properties** (status column)
   - Teams action: **Post a message in a channel**
4. Configure your SharePoint site URL, document library name, and reviewer lookup list name
5. Configure your Teams team and channel for approval notifications
6. Test with a sample document upload

## Disclaimer

**THIS CODE IS PROVIDED *AS IS* WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.**

<img src="https://m365-visitor-stats.azurewebsites.net/powerplatform-prompts/samples/power-automate/document-approval-with-escalation" aria-hidden="true" />
