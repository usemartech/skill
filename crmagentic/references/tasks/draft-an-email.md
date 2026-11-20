# Draft an email

From the user guide: Write an email with your AI client; Draft a campaign with your AI client; Sources and the content calendar with your AI client; Email templates; Send a campaign.

You ask your AI client to draft or change an email template, see it the way a recipient gets it, and send yourself a test. Your AI client works on the same template you open in the email designer. You send the campaign from the app. You ask your AI client to make a draft email campaign from a template and a list of contacts, change it, undo a change, set up an A/B test of the subject, and put a draft in the trash. Your AI client works on the same campaign you open in **Email campaigns**. You schedule or send the campaign from the app. You ask your AI client to keep your sources and to plan your content calendar. A source is a UTM campaign that a visit, a contact or a deal comes from, the same one you open in **Sources & traffic**. A calendar entry is a planned email, blog post or social post on the **Content calendar**.

## Before you start

- Connect your AI client with a **read + write** key.
- Your AI client needs a **read + write** key.
- Have the email template ready.
- Have the list of contacts ready.
- Your AI client needs a **read + write** key.

## AI does through MCP

1. Ask to see a template as a recipient gets it. Tools: `crm_email_template_list`, `crm_email_template_render`.
2. Ask for a new template. Tools: `crm_email_template_create`, `crm_email_template_block_catalog`.
3. Ask for changes. Tools: `crm_email_template_patch`, `crm_email_template_get`, `crm_email_template_get_design`, `crm_email_template_set_design`, `crm_email_template_update`.
4. Ask for a test. Tools: `crm_email_template_send_test`.
5. Ask your AI client to tidy up. Tools: `crm_email_template_move`, `crm_email_template_archive`, `crm_email_template_restore`.
6. Ask your AI client to keep the folders of the template library. Tools: `crm_email_template_folder_list`, `crm_email_template_folder_create`, `crm_email_template_folder_rename`, `crm_email_template_folder_move`, `crm_email_template_folder_remove`.
   - `crm_email_template_folder_remove` removes a folder only when it is empty, and your AI client can make it again with the same name.
7. Ask your AI client to undo a change. Tools: `crm_email_template_list_revisions`, `crm_email_template_restore_revision`.
8. Ask what campaigns you have. Tools: `crm_email_campaign_list`, `crm_email_campaign_get`.
9. Ask for a new draft. Tools: `crm_email_campaign_create`.
   - The list must be a list of contacts that is yours or shared with your team.
10. Ask for a change. Tools: `crm_email_campaign_update`.
11. Undo a change. Tools: `crm_email_campaign_restore_values`.
12. Set up an A/B test of the subject. Tools: `crm_email_campaign_create_ab_test`.
   - Variant A has the subject of the template, so the subject of variant B must be different.
   - You cannot remove a test from a draft, so to undo it, your AI client puts the draft in the trash.
13. Ask your AI client to remove a draft that you do not need. Tools: `crm_email_campaign_archive`, `crm_email_campaign_restore`.
14. Ask for a source. Tools: `crm_source_create`, `crm_source_list`, `crm_source_get`.
15. Ask for a change. Tools: `crm_source_update`, `crm_source_restore_values`.
16. Ask for a calendar entry. Tools: `crm_calendar_entry_create`.
17. Move or change an entry. Tools: `crm_calendar_entry_update`, `crm_calendar_entry_restore_values`.
18. Ask your AI client to remove what you do not need. Tools: `crm_source_archive`, `crm_calendar_entry_archive`, `crm_source_restore`, `crm_calendar_entry_restore`.

Worked example (render-a-template): `crm_email_template_list` → `crm_email_template_render`.

Example request: *Show me the welcome email the way a new contact gets it.*
Example request: *Make a draft campaign called Spring sale from the Spring template, for the Webinar guests list.*
Example request: *Make a source Spring webinar for utm_campaign spring-webinar from the newsletter, from 1 to 31 March.*

## The person does in the app

### Email templates — **Marketing & automation → Email templates** (/marketing/templates)
1. In the sidebar, select **Marketing & automation → Email templates** (/marketing/templates).
2. Select **New template**.
3. When you leave the designer, you are on the template's page.
4. Check the **Ready to send** card.
5. Check the preview on the right.
6. Under **Send a test**, enter an address in **Send to** and select **Send test** to get one copy of the email.

### Send a campaign — **Marketing & automation → Email campaigns** (/marketing/campaigns)
1. In the sidebar, select **Marketing & automation → Email campaigns** (/marketing/campaigns).
2. Select **New campaign**.
3. Select **Create campaign**.
4. Check **Set up the campaign**.
5. Select **Send campaign**.

If a tool refuses, read references/troubleshooting.md.
