# Set up a pipeline

From the user guide: Pipelines and stages with your AI client; The pipeline.

You ask your AI client to set up the pipelines that your deals move through: make a pipeline, add and change its stages, and put a pipeline or a stage that you no longer use in the trash. Your AI client works on the same pipelines that you see on the board in **Core CRM** → **Pipeline**.

## Before you start

- You need the admin role, and your AI client needs a **read + write** key.
- A pipeline and its stages belong to the whole workspace.

## AI does through MCP

1. Ask what pipelines you have. Tools: `crm_pipeline_list`, `crm_pipeline_get`.
2. Ask for a new pipeline. Tools: `crm_pipeline_create`.
3. Rename a pipeline. Tools: `crm_pipeline_update`, `crm_pipeline_restore_values`.
4. Change the stages. Tools: `crm_pipeline_stage_create`, `crm_pipeline_stage_update`, `crm_pipeline_stage_restore_values`.
   - A stage that holds deals cannot change its kind.
5. Ask your AI client to remove what you no longer use. Tools: `crm_pipeline_stage_archive`, `crm_pipeline_stage_restore`, `crm_pipeline_archive`, `crm_pipeline_restore`.
   - A stage that still holds deals, also deals in the trash, is refused, and so is the default pipeline.

Example request: *Make a pipeline called Partnerships with the stages Intro, Proposal, Signed and Lost.*

## The person does in the app

### The pipeline — **Core CRM → Pipeline** (/pipeline)
1. In the sidebar, select **Core CRM → Pipeline** (/pipeline).
2. To see another pipeline, choose it in **Pipeline**.
3. To move a deal, drag its card to another column.
4. On a card in the Lead column, select **Qualify** to move the deal to Qualified.
5. To close a deal, drag it to the Won or Lost column.

If a tool refuses, read references/troubleshooting/set-up-a-pipeline.md.
