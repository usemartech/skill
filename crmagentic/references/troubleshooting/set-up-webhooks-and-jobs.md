# If something goes wrong: Set up webhooks and background jobs

What a refusal means, and what to do next. Tell the person what happened in plain words.

- **Your AI client says that the webhook or the schedule is on.** Turn it off in **Settings → Webhooks** (/settings/webhooks) or **Settings → Background jobs** (/settings/jobs), and ask again.
- **The address is refused.** The address must be a public web address, with no user name or password in it. Give another address.
- **Your AI client says that the key is already used.** Each schedule has a key of its own, also a schedule in the trash. Choose another key, or ask your AI client to bring the old schedule back.
- **Your AI client says that it may not do this.** Webhooks and background jobs need an admin's **read + write** key. Ask an admin for one.
- **The workflow says Choose the incoming webhook this trigger listens to.** The trigger has no webhook yet. Name the webhook to your AI client, or choose it in the builder.
- **Your AI client says to turn the webhook off first.** It is on. Turn it off in **Settings → Webhooks → Incoming** (/settings/webhooks), and ask again.
