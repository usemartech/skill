# Set up webhooks and background jobs

From the user guide: Webhooks and background jobs with your AI client; Receive events from another system with AI.

You ask your AI client to set up a webhook, which tells another system, such as your website or an automation tool, when a contact, a company or a deal is created, changed or put in the trash. You also ask it to set up a background job schedule, which runs one of the CRM's jobs every so often. Your AI client makes both switched off, and you turn them on yourself in **Settings** → **Webhooks** and **Settings** → **Background jobs**. You ask your AI client to set up an incoming webhook: an address that another system, such as your product or your billing system, sends its events to. You also ask it for the rules that turn those events into contacts, with fields, tags and a timeline entry. Your AI client makes the webhook switched off and with no secret. You set the secret and turn the webhook on yourself in **Settings** → **Webhooks** → **Incoming**.

## Before you start

- You need the admin role, and your AI client needs a **read + write** key.
- For a webhook, have the address of the other system ready: a public web address, with no user name or password in it.
- You need the admin role, and your AI client needs a **read + write** key.
- Find out how the other system signs its events: the header that holds the signature, and whether it signs the body or a time and the body.

## AI does through MCP

1. Ask what you have. Tools: `crm_webhook_list`, `crm_webhook_get`, `crm_job_schedule_list`, `crm_job_schedule_get`.
2. Ask for a webhook. Tools: `crm_webhook_create`.
   - The answer never gives the webhook's signing secret: you get it in **Settings → Webhooks** (/settings/webhooks).
3. Ask for a change. Tools: `crm_webhook_update`, `crm_webhook_restore_values`.
   - A webhook that is on cannot change: turn it off first.
4. Ask for a background job schedule. Tools: `crm_job_schedule_create`, `crm_job_schedule_update`, `crm_job_schedule_restore_values`.
5. Ask your AI client to remove what you do not need. Tools: `crm_webhook_archive`, `crm_job_schedule_archive`, `crm_webhook_restore`, `crm_job_schedule_restore`.
6. Ask for a workflow that starts on another system's events. Tools: `crm_workflow_node_catalog`, `crm_workflow_create`.
   - When an incoming webhook files contacts (**Settings → Webhooks → Incoming** (/settings/webhooks)), the **Webhook received** trigger starts a run for each event that a rule files: from one incoming webhook, and, if you want, only some event types, such as user.signed_up, or subscription.* for every subscription event.
7. Ask what you have. Tools: `crm_inbound_webhook_list`, `crm_inbound_webhook_get`.
   - They never give the secret itself.
8. Ask for an incoming webhook. Tools: `crm_inbound_webhook_create`.
9. Ask your AI client to read a sample. Tools: `crm_inbound_webhook_events`, `crm_inbound_webhook_event_get`.
10. Ask for rules from the sample. Tools: `crm_inbound_webhook_rule_create`, `crm_inbound_webhook_rule_update`, `crm_inbound_webhook_rule_reorder`.
11. Ask for a change. Tools: `crm_inbound_webhook_update`, `crm_inbound_webhook_restore_values`.
12. Ask your AI client to remove what you do not need. Tools: `crm_inbound_webhook_rule_archive`, `crm_inbound_webhook_archive`, `crm_inbound_webhook_rule_restore`, `crm_inbound_webhook_restore`.

Example request: *Make a webhook called Website sync that tells https://hooks.example.com/crm when a contact is created, and leave it off.*
Example request: *Make an incoming webhook called Product sign-ups that reads an HMAC signature from the x-signature header and the event type from body:type, and leave it off.*

## The person does in the app

- Turn it on yourself. Open **Settings → Webhooks** (/settings/webhooks) or **Settings → Background jobs** (/settings/jobs), and switch the webhook or the schedule on. Your AI client cannot turn them on or off, send a test event, or run a job now.
- Set the secret and turn it on yourself. Open **Settings → Webhooks → Incoming** (/settings/webhooks), choose **Set secret**, give the secret to the other system, and switch the webhook on. Your AI client cannot set the secret, turn the webhook on or off, use **Listen**, or process events again.

If a tool refuses, read references/troubleshooting/set-up-webhooks-and-jobs.md.
