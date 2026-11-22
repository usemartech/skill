# Set up webhooks and background jobs

From the user guide: Webhooks and background jobs with your AI client.

You ask your AI client to set up a webhook, which tells another system, such as your website or an automation tool, when a contact, a company or a deal is created, changed or put in the trash. You also ask it to set up a background job schedule, which runs one of the CRM's jobs every so often. Your AI client makes both switched off, and you turn them on yourself in **Settings** → **Webhooks** and **Settings** → **Background jobs**.

## Before you start

- You need the admin role, and your AI client needs a **read + write** key.
- For a webhook, have the address of the other system ready: a public web address, with no user name or password in it.

## AI does through MCP

1. Ask what you have. Tools: `crm_webhook_list`, `crm_webhook_get`, `crm_job_schedule_list`, `crm_job_schedule_get`.
2. Ask for a webhook. Tools: `crm_webhook_create`.
   - The answer never gives the webhook's signing secret: you get it in **Settings → Webhooks** (/settings/webhooks).
3. Ask for a change. Tools: `crm_webhook_update`, `crm_webhook_restore_values`.
   - A webhook that is on cannot change: turn it off first.
4. Ask for a background job schedule. Tools: `crm_job_schedule_create`, `crm_job_schedule_update`, `crm_job_schedule_restore_values`.
5. Ask your AI client to remove what you do not need. Tools: `crm_webhook_archive`, `crm_job_schedule_archive`, `crm_webhook_restore`, `crm_job_schedule_restore`.

Example request: *Make a webhook called Website sync that tells https://hooks.example.com/crm when a contact is created, and leave it off.*

## The person does in the app

- Turn it on yourself. Open **Settings → Webhooks** (/settings/webhooks) or **Settings → Background jobs** (/settings/jobs), and switch the webhook or the schedule on. Your AI client cannot turn them on or off, send a test event, or run a job now.

If a tool refuses, read references/troubleshooting/set-up-webhooks-and-jobs.md.
