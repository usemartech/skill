# Do design work handed to you

From the user guide: Hand design work to your AI client.

You give your AI client a piece of work on a landing page or an email template, the way you would give it to a colleague: a work item that says what to change and what done means. Your AI client finds the work, starts it, does it and marks it done.

## Before you start

- Connect your AI client with a **read + write** key.
- Your key signs in as an agent.

## AI does through MCP

1. Add the work item. Tools: `crm_design_work_create`.
2. Ask your AI client for its work. Tools: `crm_design_work_list`.
3. Let it do the work. Tools: `crm_design_work_claim`, `crm_design_work_complete`.
4. To stop a piece of work, ask your AI client to cancel it with `crm_design_work_cancel`. Tools: `crm_design_work_cancel`.
   - Only the person who added the item, the one it is assigned to or an admin can cancel it.

Worked example (list-design-work): `crm_email_template_list` → `crm_design_work_create` → `crm_design_work_list` → `crm_design_work_claim` → `crm_design_work_complete`.

Example request: *Add a work item on the welcome email: shorten the welcome text. Then list your open work, take the item and mark it done.*

## The person does in the app

If a tool refuses, read references/troubleshooting/do-design-work.md.
