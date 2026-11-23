# Find and move contacts and deals

From the user guide: Find and update records; Products and personas with your AI client; Find and view contacts; The pipeline; Products and services; Personas.

You ask your AI client to find contacts, companies and deals, read what happened with them, and change them for you: add a contact, move a deal to another stage, add a task or a note, or fill in a custom field. You ask your AI client to keep your catalog of products and services, and your personas. Your AI client works on the same products that you open in **Products** and the same personas that you open in **Personas**, both under **Settings**.

## Before you start

- Connect your AI client.
- To change records, your key needs **read + write**.
- You need the admin role, and your AI client needs a **read + write** key.

## AI does through MCP

1. Ask for the records you want. Tools: `crm_contact_list`, `crm_company_list`, `crm_deal_list`, `search_crm`.
2. Ask what happened with a record. Tools: `read_contact_history`, `read_company_history`, `read_deal_history`, `crm_contact_get`, `crm_company_get`, `crm_deal_get`.
3. Ask your AI client to move a deal. Tools: `crm_pipeline_list`, `crm_deal_set_stage`.
4. Ask for a task. Tools: `crm_task_create`, `crm_user_list`, `crm_task_list`, `crm_task_get`, `crm_task_complete`, `crm_task_reopen`, `crm_task_update`, `crm_task_archive`, `crm_task_restore`.
5. Ask for other changes in the same way: Tools: `crm_contact_create`, `crm_company_create`, `crm_contact_update`, `crm_company_update`, `crm_deal_create`, `crm_deal_update`, `crm_note_create`, `crm_note_list`, `crm_note_get`, `crm_note_update`, `crm_note_archive`, `crm_note_restore`, `crm_contact_tag_list`, `crm_contact_tag_add`, `crm_contact_tag_remove`, `crm_field_list`, `crm_field_values`, `crm_field_set`, `crm_contact_archive`, `crm_company_archive`, `crm_deal_archive`, `crm_task_archive`, `crm_contact_restore`, `crm_company_restore`, `crm_deal_restore`, `crm_task_restore`, `crm_contact_restore_values`, `crm_company_restore_values`, `crm_deal_restore_values`, `crm_task_restore_values`, `crm_note_restore_values`.
   - **Contacts and companies.** `crm_contact_create` and `crm_company_create` add a record, and `crm_contact_update` and `crm_company_update` change only the fields you name.
   - A contact needs a first name, a last name or an email address, and an email address belongs to one contact only.
6. Ask for a product or a service. Tools: `crm_product_create`, `crm_product_list`, `crm_product_get`.
7. Ask for a change. Tools: `crm_product_update`, `crm_product_restore_values`.
8. Ask for a persona. Tools: `crm_persona_create`, `crm_persona_list`, `crm_persona_get`.
9. Change a persona. Tools: `crm_persona_update`, `crm_persona_restore_values`.
10. Ask your AI client to remove what you do not need. Tools: `crm_product_archive`, `crm_persona_archive`, `crm_product_restore`, `crm_persona_restore`.

Worked example (find-contacts): `crm_contact_list`.
Worked example (move-a-deal): `crm_deal_list` → `crm_pipeline_list` → `crm_deal_set_stage`.
Worked example (add-a-task): `search_crm` → `crm_task_create`.

Example request: *Show me three of my contacts, with their email addresses.*
Example request: *Add a service called Onboarding at 1,500 MYR, then show me the catalog.*

## The person does in the app

- For the emails, meetings or calls of the whole workspace, or for a spreadsheet of contacts, your AI client sends you to the screen. In the sidebar, select **Engagement → Emails** (/emails), **Meetings**, **Calls** or **Import**.

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

### Products and services — **Settings → Products and services** (/settings/products)
1. In the sidebar, select **Settings**.
2. Select **New product**.
3. To change a product, select **Edit** on its row, change what you need and select **Save product**.
4. To put a product on a deal, open the deal and select the **Products** tab.
5. On the deal's **Products** tab, select **Edit** on a line to change its quantity, price or discount, or **Remove** to take the product off the deal.

### Personas — **Settings → Personas** (/settings/personas)
1. Go to **Settings**, then **Personas**.
2. Select **New persona**.
3. Under **Job-title match**, enter the words or phrases that point to this persona, separated by commas.
4. To see the contacts of a persona, select the number in its **Leads** column.
5. To give a contact a persona, open the contact.

If a tool refuses, read references/troubleshooting/find-and-move-records.md.
