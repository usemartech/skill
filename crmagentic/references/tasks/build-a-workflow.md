# Build a workflow

From the user guide: Build a workflow with your AI client; Follow up after someone registers.

You ask your AI client to build a workflow as a draft, change it, undo a change, read the draft in the app, and set it live yourself. Your AI client builds the same workflow that you open in **Workflows**, under **Marketing & automation** in the sidebar, but it never sets a workflow live.

## Before you start

- You need the admin role, and your AI client needs a **read + write** key.

## AI does through MCP

1. Ask what workflows you have. Tools: `crm_workflow_list`, `crm_workflow_get`.
2. Ask what a workflow can do. Tools: `crm_workflow_node_catalog`.
3. Ask for a new workflow. Tools: `crm_workflow_create_from_template`, `crm_workflow_create`.
4. Ask what still stops the workflow. Tools: `crm_workflow_check`.
5. Ask for a change. Tools: `crm_workflow_update`.
   - Your AI client cannot change a live workflow.
6. Undo a change. Tools: `crm_workflow_list_revisions`, `crm_workflow_restore_revision`.
   - Your change is never lost.
7. Ask your AI client to remove a draft that you do not need. Tools: `crm_workflow_archive`, `crm_workflow_restore`.
   - Your AI client cannot put a live workflow in the trash.
8. Ask how the workflow runs. Tools: `crm_workflow_list_runs`.

Worked example (build-a-welcome-workflow): `crm_workflow_create_from_template` → `crm_workflow_check` → `crm_workflow_update` → `crm_workflow_list_revisions` → `crm_workflow_restore_revision`.

Example request: *Build a welcome workflow for new contacts as a draft, and tell me what I still have to do before I set it live.*

## The person does in the app

- Read the draft in the app. Open the workflow in **Workflows**, look at each step, and choose an email where a step still says **Choose an email**.
- Set the workflow live yourself. Select **Save**, then **Set live**. Your AI client cannot set a workflow live, pause it, or start a run.

### Follow up after someone registers — **Marketing & automation → Workflows** (/settings/workflows)

If a tool refuses, read references/troubleshooting.md.

## Advice

- Start from a template when one fits: `crm_workflow_create_from_template` with `welcome`, `webinar` or `nurture`. Read `crm_workflow_node_catalog` before you build from nothing; it gives the settings of each step and the lists and snippets a step can use.
- A workflow is about one object: Contact, Company or Deal. A form trigger and the tag steps work on a Contact workflow only.
- The email template or form a step uses must exist first: build or find it with its own tools, then pass its id. No tool builds a list: pick one from `crm_workflow_node_catalog`, or ask the person to make it in **Core CRM → Lists & segments**.
- Before you hand the draft over, call `crm_workflow_check` and tell the person what still stops it, every email it will send, and every address an HTTP request step will call. Then give the `editUrl` and say that they set it live themselves.
- Never tell the person that a workflow is live, or that it will send, unless `crm_workflow_get` shows status `ACTIVE`.
