# If something goes wrong: Receive events from another system

What a refusal means, and what to do next. Tell the person what happened in plain words.

- **No sample came in.** **Listen** ran out after 15 minutes, nothing was sent, or the test was refused. Ask your AI client to read the last refusal, then use **Listen** again.
- **Listen is refused.** The webhook has no secret yet. Choose **Set secret** first.
- **The refusal is signature_missing.** The signature header has another name, or the prefix is missing. Compare the setting with the header names of the refusal.
- **The refusal is signature_mismatch.** The scheme, the prefix, the encoding or the secret is wrong. Check each one against the other system.
- **The refusal is timestamp_outside_tolerance.** The timestamp header is wrong, or the clock of the other system is off by more than the tolerance (5 minutes by default).
- **The refusal is unsupported_type, too_large or bad_json.** The body is not sent as JSON, is over 256 KB, or is not a JSON object. Change what the other system sends.
- **The refusal is address_not_allowed.** The other system sends from an address that is not on the webhook's allow-list. Add its address to the list, or empty the list.
- **The workflow says Choose the incoming webhook this trigger listens to.** The trigger has no webhook yet. Name the webhook to your AI client, or choose it in the builder.
- **Your AI client says to turn the webhook off first.** It is on. Turn it off in **Settings → Webhooks → Incoming** (/settings/webhooks), and ask again.
