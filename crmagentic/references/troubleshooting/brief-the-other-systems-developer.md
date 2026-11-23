# If something goes wrong: Brief the other system's developer

What a refusal means, and what to do next. Tell the person what happened in plain words.

- **Your AI client says the webhook is not found.** Ask it to list your incoming webhooks with `crm_inbound_webhook_list` and use the id from there.
- **The brief has no rule in it.** No rule is on yet. The brief then suggests a payload; map the fields after the first test event.
- **Your AI client says to turn the webhook off first.** Changing where the webhook reads values works only while it is off. Turn it off in **Settings → Webhooks → Incoming** (/settings/webhooks), and ask again.
