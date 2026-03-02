# Timesheet App

## Description

This Power Apps Copilot prompt generates a weekly timesheet app for professional services employees. It covers the full lifecycle: time entry per day with project and task type selection, running daily and weekly hour totals, weekly submission with manager approval routing, and a history screen showing past timesheets with approval status.

Timesheet management is a near-universal need in consulting, agencies, legal, IT services, and any project-based organization. The combination of multi-entry-per-day, running totals, lock-on-submit, and approval history covers the real-world requirements that simpler time-tracking apps miss.

## Prompt

> Create a weekly timesheet app for professional services employees. Display Monday–Friday with multiple time entries per day (project from list, task type: Development/Design/Meeting/Admin/Support, hours, optional note). Show running daily and weekly totals. Submit button locks and routes to manager for approval. History screen shows past weeks with Pending/Approved/Rejected status. Store in Dataverse.

### Supported Language(s)

- [English - US](./en-us/prompt.md)

## Authors

Solution|Author(s)
--------|---------
Timesheet App | [OwnOptic](https://github.com/OwnOptic) ([@OwnOptic](https://twitter.com/OwnOptic))

## Minimal Path to Awesome

1. Navigate to [Power Apps](https://make.powerapps.com/) and click **Create** > **Start with Copilot**
2. Copy the content from [prompt.md](./en-us/prompt.md) and paste it into the Copilot description field
3. Review the generated Dataverse tables (Projects, TimesheetEntries, TimesheetWeeks) and adjust column names if needed
4. Add your project list to the Projects table in Dataverse
5. Verify the weekly total calculation formula in the app
6. Connect the Submit button to a Power Automate flow that:
   - Sets the timesheet status to "Pending"
   - Sends an approval request to the employee's manager
   - Updates the status to "Approved" or "Rejected" based on the manager's response
   - Notifies the employee via email or Teams of the decision
7. Test with a sample week including multiple projects per day
8. Share the app with all employees in the organization

## Disclaimer

**THIS CODE IS PROVIDED *AS IS* WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, INCLUDING ANY IMPLIED WARRANTIES OF FITNESS FOR A PARTICULAR PURPOSE, MERCHANTABILITY, OR NON-INFRINGEMENT.**

<img src="https://m365-visitor-stats.azurewebsites.net/powerplatform-prompts/samples/power-apps/timesheet-app" aria-hidden="true" />
