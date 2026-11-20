# Build a workflow

From the user guide: Build a workflow with your AI client; Save a view with your AI client; Set up fields, tags and snippets with your AI client; Follow up after someone registers.

You ask your AI client to build a workflow as a draft, change it, undo a change, read the draft in the app, and set it live yourself. Your AI client builds the same workflow that you open in **Workflows**, under **Marketing & automation** in the sidebar, but it never sets a workflow live. You ask your AI client to save a view of your contacts, companies or deals, share it with your team, change it, undo a change, and put it in the trash. A saved view is the list that a workflow watches, so your AI client can make the list before it builds the workflow. You ask your AI client to set up what a workflow uses: a custom field such as an event date, the tags on contacts, and snippets, short lists of actions that a workflow runs.

## Before you start

- You need the admin role, and your AI client needs a **read + write** key.
- Your AI client needs a **read + write** key.
- A view of contacts needs access to contacts.
- You need the admin role, and your AI client needs a **read + write** key.
- Tags are on contacts, so your key also needs access to contacts.

## AI does through MCP

1. Ask what workflows you have. Tools: `crm_workflow_list`, `crm_workflow_get`.
2. Ask what a workflow can do. Tools: `crm_workflow_node_catalog`, `crm_list_list`, `crm_list_create`, `crm_view_list`, `crm_view_create`.
3. Ask for a new workflow. Tools: `crm_workflow_create_from_template`, `crm_workflow_create`.
4. Ask what still stops the workflow. Tools: `crm_workflow_check`.
5. Ask for a change. Tools: `crm_workflow_update`.
   - Your AI client cannot change a live workflow.
6. Undo a change. Tools: `crm_workflow_list_revisions`, `crm_workflow_restore_revision`.
   - Your change is never lost.
7. Ask your AI client to remove a draft that you do not need. Tools: `crm_workflow_archive`, `crm_workflow_restore`.
   - Your AI client cannot put a live workflow in the trash.
8. Ask how the workflow runs. Tools: `crm_workflow_list_runs`.
9. Ask what views you have. Tools: `crm_view_list`, `crm_view_get`.
10. Ask for a new view. Tools: `crm_view_create`.
   - The view belongs to you, and only you see it until you share it.
11. Ask for a change. Tools: `crm_view_update`.
   - Only the person who owns a view can change it.
12. Undo a change. Tools: `crm_view_restore_values`.
13. Ask your AI client to remove a view that you do not need. Tools: `crm_view_archive`, `crm_view_restore`.
14. Ask for a custom field. Tools: `crm_field_create`, `crm_field_list`.
15. Ask for a change. Tools: `crm_field_update`, `crm_field_restore_values`.
16. Put fields in groups. Tools: `crm_field_group_list`, `crm_field_group_create`, `crm_field_group_update`, `crm_field_group_remove`.
   - `crm_field_group_remove` removes a group only when no field is in it.
17. Rename a tag. Tools: `crm_contact_tag_rename`.
18. Ask for a snippet. Tools: `crm_workflow_snippet_create`, `crm_workflow_snippet_list`, `crm_workflow_snippet_update`, `crm_workflow_snippet_restore_values`.
19. Ask your AI client to remove what you do not need. Tools: `crm_field_archive`, `crm_contact_tag_archive`, `crm_workflow_snippet_archive`, `crm_field_restore`, `crm_contact_tag_restore`, `crm_workflow_snippet_restore`.

Worked example (build-a-welcome-workflow): `crm_workflow_create_from_template` → `crm_workflow_check` → `crm_workflow_update` → `crm_workflow_list_revisions` → `crm_workflow_restore_revision`.

Example request: *Build a welcome workflow for new contacts as a draft, and tell me what I still have to do before I set it live.*
Example request: *Save a view of the contacts who have an email address, share it with the team, and build a three-day nurture workflow on it as a draft.*
Example request: *Add a date field called Event date to contacts, then build the webinar workflow as a draft that waits for it.*

## The person does in the app

- Read the draft in the app. Open the workflow in **Workflows**, look at each step, and choose an email where a step still says **Choose an email**, and a list where the trigger still says **Choose the list this trigger watches**.
- Set the workflow live yourself. Select **Save**, then **Set live**. Your AI client cannot set a workflow live, pause it, or start a run.
- Share the view when a workflow will watch it. Ask your AI client to set the view to **WORKSPACE**, so your team can see which records the workflow counts. A view counts the records that you can see.

### Follow up after someone registers — **Marketing & automation → Workflows** (/settings/workflows)

If a tool refuses, read references/troubleshooting.md.

## Advice

- Start from a template when one fits: `crm_workflow_create_from_template` with `welcome`, `webinar` or `nurture`. Read `crm_workflow_node_catalog` before you build from nothing; it gives the settings of each step and the lists and snippets a step can use.
- A workflow is about one object: Contact, Company or Deal. A form trigger and the tag steps work on a Contact workflow only.
- The email template or form a step uses must exist first: build or find it with its own tools, then pass its id.
- A list trigger watches one list (`listId`) or one saved view (`savedViewId`). Prefer a list: `crm_list_list` finds it, `crm_list_create` makes it, shared. The `nurture` template takes a view only: create it without one, then set `listId` with `crm_workflow_update`.
- Before you hand the draft over, call `crm_workflow_check` and tell the person what still stops it, every email it will send, and every address an HTTP request step will call. Then give the `editUrl` and say that they set it live themselves.
- Never tell the person that a workflow is live, or that it will send, unless `crm_workflow_get` shows status `ACTIVE`.
