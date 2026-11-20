# If something goes wrong: Set up a pipeline

What a refusal means, and what to do next. Tell the person what happened in plain words.

- **Your AI client says that deals sit in the stage.** Move the deals to another stage first, also the deals in the trash. Your AI client can move them with `crm_deal_set_stage`, or you drag them on the board.
- **Your AI client says that it is the last open stage.** A pipeline keeps at least one open stage. Add another open stage first.
- **Your AI client says that it is the default pipeline.** Choose another default pipeline in **Settings → Pipelines** (/settings/pipelines) first.
- **Your AI client says that a workflow or a page uses it.** Pause the workflow in **Workflows**, or take the page offline, and ask again.
- **Your AI client says that it may not change pipelines.** The key belongs to a member, or the key is **read only**. Ask an admin for a **read + write** key.
