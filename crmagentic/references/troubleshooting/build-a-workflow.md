# If something goes wrong: Build a workflow

What a refusal means, and what to do next. Tell the person what happened in plain words.

- **Your AI client says that the workflow is not ready.** A step still needs something, such as an email or the list that the trigger watches. Ask your AI client which step, or open the workflow and fix the step in the builder.
- **Your AI client says that the workflow is live.** Your AI client cannot change or trash a live workflow. Pause it in **Workflows** first.
- **A version is not in the list.** The CRM keeps every version for 90 days, then the last 20.
- **A run stopped after a change.** A run that waited at a step that a change removed ends as failed when it resumes. The run log says that the step was removed.
- **Your AI client says that a step points at something archived.** The email template, form, tag, field or list of that step is in the trash. Ask your AI client to choose one that is live.
- **Your AI client says that it may not build workflows.** The key belongs to a member, or the key is **read only**. Ask an admin for a **read + write** key.
- **The Webinar registration template left a tag behind.** The template makes the tag *Attended*. The tag stays when the workflow goes to the trash.
- **Your AI client says that a live workflow watches the view.** Your AI client cannot put the view in the trash or change its filters while a live workflow watches it. Pause the workflow in **Workflows** first.
- **Your AI client says that you already have a view with this name.** Choose another name, or ask your AI client to change the view that you have.
- **Your AI client says that only the owner can change the view.** Someone else shared the view. Ask your AI client to save a copy of it as your own view.
- **Your AI client says that it may not read contacts.** Your role has no access to contacts. Ask an admin for access, or save a view of companies or deals.
- **A live workflow uses it.** Pause the workflow in **Workflows** first.
- **The group still holds a field.** Move each field out of the group first.
