# Brief the other system's developer

From the user guide: Brief the other system's developer with your AI client.

Someone else builds or changes the system that sends events to your incoming webhook, such as the developer of your billing system. You ask your AI client for the brief that tells them what to send. The CRM makes the brief from the webhook's own settings and rules, so it is the same brief as **Copy for your developer** in **Settings** → **Webhooks** → **Incoming**. Connect another system shows what every brief holds.

## Before you start

- You need the admin role, and your AI client needs a key that can read.
- The incoming webhook exists.

## Steps, in this order

Do the steps in this order, each one once. A step with no tool is yours, or it hands back to the person: then wait until they say it is done.

1. Ask for the brief. `crm_inbound_webhook_brief` takes the webhook's id and gives the brief as Markdown, for a webhook that is on or off. Give the person the Markdown to pass on, or the file name in fileName to save it as.
2. Explain the brief to the person in plain words: where the other system sends its events, the one header it adds, what goes in the body, and that the answer to a good event is 202.
3. Remind the person that the brief never holds the secret. They give the secret to the developer separately, by a safe channel such as a password manager, never in the same message or ticket.
4. If the other system has no format for its events yet, first set where the webhook reads the event type, id and time to the shape the brief suggests, with `crm_inbound_webhook_update` while the webhook is off: body:type, body:id and body:occurred_at. Then ask for the brief again.
5. For a system that someone is building, recommend the secret header: one header, Authorization: Bearer and the secret, and no signing. A signing scheme is only for a system that signs its own way and can't add a header.

Example request: *Make the brief for the developer of our billing system for the Billing incoming webhook, and tell me what to send them.*

If a tool refuses, read references/troubleshooting/brief-the-other-systems-developer.md.
