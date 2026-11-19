# Concepts

## The workspace

You can work in crmagentic from your own AI client as well as in the app. Your AI client connects to the CRM over MCP, the Model Context Protocol, and uses the same tools as the AI in the app. It signs in with a key that acts as you: it can do only what you may do in the app, and only as much as the access you chose for the key.

## Objects

The tools read and write these objects: company, contact, deal, design_revision, design_work, email_template, field, form, media, note, page, pipeline, task, user, workflow. Names are not ids: search first, then pass the id a result gave you.

## Keys and roles

- Only an admin can issue a key. If you do not have the **Admin** role, ask your admin to issue a key for you and to send it to you safely.
- Choose how much the key may do: **read only** to look things up, or **read + write** to change records too.
