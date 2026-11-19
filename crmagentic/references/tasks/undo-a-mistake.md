# Undo a mistake

From the user guide: Restore from the trash.

Every change made through MCP has a way back. Find the job below, and use the tool it names; a restore is a new version on top, so a restore is undone the same way.

## AI does through MCP

- Build a form with your AI client: Ask your AI client to put the form live. Tools: `crm_form_unpublish`.
- Build a form with your AI client: Ask your AI client to remove a draft that you do not need, such as a test form. Tools: `crm_form_restore`, `crm_form_unpublish`.
- Build a form with your AI client: Ask your AI client to undo a change to the questions or the texts. Tools: `crm_form_list_revisions`, `crm_form_restore_revision`.
- Build a landing page with your AI client: To use your own images, upload them to the Media library first. Tools: `crm_media_restore`.
- Build a landing page with your AI client: Ask your AI client to publish. Tools: `crm_page_unpublish`.
- Build a landing page with your AI client: To go back to an earlier version, ask your AI client. Tools: `crm_design_revision_restore`.
- Build a workflow with your AI client: Undo a change. Tools: `crm_workflow_list_revisions`, `crm_workflow_restore_revision`.
- Build a workflow with your AI client: Ask your AI client to remove a draft that you do not need. Tools: `crm_workflow_restore`.
- Find and update records: Ask for a task. Tools: `crm_task_restore`.
- Find and update records: Ask for other changes in the same way: Tools: `crm_note_restore`, `crm_contact_restore`, `crm_company_restore`, `crm_deal_restore`, `crm_task_restore`, `crm_contact_restore_values`, `crm_company_restore_values`, `crm_deal_restore_values`, `crm_task_restore_values`, `crm_note_restore_values`.
- Write an email with your AI client: Ask your AI client to tidy up. Tools: `crm_email_template_restore`.
- Write an email with your AI client: Ask your AI client to undo a change. Tools: `crm_email_template_list_revisions`, `crm_email_template_restore_revision`.

## The person does in the app

### Restore from the trash — **Settings → Trash** (/settings/trash)
1. To delete a contact, open their record and select **Archive**.
2. To see what is in the trash, go to **Settings** and, select **Data model → Trash** (/settings/trash).
3. To put a record back, select **Restore** in its row.
4. An admin can remove a contact, a company or a deal for ever.

If a tool refuses, read references/troubleshooting.md.
