# Draft an email

From the user guide: Write an email with your AI client; Email templates.

You ask your AI client to draft or change an email template, see it the way a recipient gets it, and send yourself a test. Your AI client works on the same template you open in the email designer. You send the campaign from the app.

## Before you start

- Connect your AI client with a **read + write** key.

## AI does through MCP

1. Ask to see a template as a recipient gets it. Tools: `crm_email_template_list`, `crm_email_template_render`.
2. Ask for a new template. Tools: `crm_email_template_create`, `crm_email_template_block_catalog`.
3. Ask for changes. Tools: `crm_email_template_patch`, `crm_email_template_get`, `crm_email_template_get_design`, `crm_email_template_set_design`, `crm_email_template_update`.
4. Ask for a test. Tools: `crm_email_template_send_test`.
5. Ask your AI client to tidy up. Tools: `crm_email_template_move`, `crm_email_template_archive`, `crm_email_template_restore`.
6. Ask your AI client to undo a change. Tools: `crm_email_template_list_revisions`, `crm_email_template_restore_revision`.

Worked example (render-a-template): `crm_email_template_list` → `crm_email_template_render`.

Example request: *Show me the welcome email the way a new contact gets it.*

## The person does in the app

### Email templates — **Marketing & automation → Email templates** (/marketing/templates)
1. In the sidebar, select **Marketing & automation → Email templates** (/marketing/templates).
2. Select **New template**.
3. When you leave the designer, you are on the template's page.
4. Check the **Ready to send** card.
5. Check the preview on the right.
6. Under **Send a test**, enter an address in **Send to** and select **Send test** to get one copy of the email.

If a tool refuses, read references/troubleshooting.md.
