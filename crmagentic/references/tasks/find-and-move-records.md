# Find and move contacts and deals

From the user guide: Find and update records; Find and view contacts; The pipeline.

You ask your AI client to find contacts, companies and deals, read what happened with them, and change them for you: add a contact, move a deal to another stage, add a task or a note, or fill in a custom field.

## Before you start

- Connect your AI client.
- To change records, your key needs **read + write**.

## AI does through MCP

1. Ask for the records you want. Tools: `crm_contact_list`, `crm_company_list`, `crm_deal_list`, `search_crm`.
2. Ask what happened with a record. Tools: `read_contact_history`, `read_company_history`, `read_deal_history`, `crm_contact_get`, `crm_company_get`, `crm_deal_get`.
3. Ask your AI client to move a deal. Tools: `crm_pipeline_list`, `crm_deal_set_stage`.
4. Ask for a task. Tools: `crm_task_create`, `crm_user_list`, `crm_task_complete`, `crm_task_reopen`, `crm_task_update`, `crm_task_archive`, `crm_task_restore`.
5. Ask for other changes in the same way: Tools: `crm_contact_create`, `crm_company_create`, `crm_contact_update`, `crm_company_update`, `crm_deal_create`, `crm_deal_update`, `crm_note_create`, `crm_note_list`, `crm_note_get`, `crm_note_update`, `crm_note_archive`, `crm_note_restore`, `crm_field_list`, `crm_field_values`, `crm_field_set`, `crm_contact_archive`, `crm_company_archive`, `crm_deal_archive`, `crm_task_archive`, `crm_contact_restore`, `crm_company_restore`, `crm_deal_restore`, `crm_task_restore`, `crm_contact_restore_values`, `crm_company_restore_values`, `crm_deal_restore_values`, `crm_task_restore_values`, `crm_note_restore_values`.
   - **Contacts and companies.** `crm_contact_create` and `crm_company_create` add a record, and `crm_contact_update` and `crm_company_update` change only the fields you name.
   - A contact needs a first name, a last name or an email address, and an email address belongs to one contact only.

Worked example (find-contacts): `crm_contact_list`.
Worked example (move-a-deal): `crm_deal_list` → `crm_pipeline_list` → `crm_deal_set_stage`.
Worked example (add-a-task): `search_crm` → `crm_task_create`.

Example request: *Show me three of my contacts, with their email addresses.*

## The person does in the app

### Find and view contacts — **Core CRM → Contacts** (/contacts)
1. In the sidebar, select **Core CRM → Contacts** (/contacts).
2. Type a name, an email address or a job title into **Search name, email, title…**.
3. To narrow the list by any field, select **Filters**.
4. Select a contact's name to open their record.
5. To add a contact by hand, select **New contact**.

### The pipeline — **Core CRM → Pipeline** (/pipeline)
1. In the sidebar, select **Core CRM → Pipeline** (/pipeline).
2. To see another pipeline, choose it in **Pipeline**.
3. To move a deal, drag its card to another column.
4. On a card in the Lead column, select **Qualify** to move the deal to Qualified.
5. To close a deal, drag it to the Won or Lost column.

If a tool refuses, read references/troubleshooting.md.
