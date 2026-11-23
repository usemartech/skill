# Concepts

## The workspace

You can work in crmagentic from your own AI client as well as in the app. Your AI client connects to the CRM over MCP, the Model Context Protocol, and uses the same tools as the AI in the app. It signs in with a key that acts as you: it can do only what you may do in the app, and only as much as the access you chose for the key.

## Objects

The tools read and write these objects: blog_post, calendar_entry, chatbot, company, contact, dashboard, deal, design_revision, design_work, email_campaign, email_template, email_template_folder, field, field_group, form, funnel, inbound_webhook, inbound_webhook_rule, job_schedule, list, media, media_folder, note, page, persona, pipeline, pipeline_stage, product, report, score_rule, source, task, tracked_content, tracking_site, user, view, webhook, workflow, workflow_snippet. Names are not ids: search first, then pass the id a result gave you.

## Keys and roles

- Only an admin can issue a key. If you do not have the **Admin** role, ask your admin to issue a key for you and to send it to you safely.
- Choose how much the key may do: **read only** to look things up, or **read + write** to change records too.
- The key from **Settings → MCP server** (/settings/mcp) connects an AI client, and it is not an API key: a key from **Settings → API keys** (/settings/api) lets another system use the REST API. You make either key in the app, and an AI client never makes one.
- To give another system an API key, follow Connect another system.
