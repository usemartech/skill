# Troubleshooting

What a refusal means, and what to do next. Tell the person what happened in plain words.

## Build a form
- **Your AI client says that the form cannot go live.** No question fills in the contact's email address or name. Ask your AI client to add an email question that fills in the email, and then publish again.
- **Your AI client says that the form has responses.** Your AI client cannot change the questions of a live form that has responses.
- **Your AI client says that it may not build forms.** The key belongs to a member, or the key is **read only**. Ask an admin for a **read + write** key.
- **Your AI client says that the form is published.** Your AI client cannot put a live form in the trash. Ask it to take the form offline with `crm_form_unpublish` first, and then to archive the form.
- **Your AI client says that a key is reserved.** The key *website* is kept for bot protection. Ask your AI client to leave out the key, and the CRM picks another one.
- **You want to delete a form for good.** Neither your AI client nor the app deletes a form for good. An archived form stays in **Forms** under **Show archived**.

## Build a landing page
- **Your AI client says a page already uses this address.** Each address belongs to one page, even an archived one. Ask for another address.
- **The publish is refused.** The page has no blocks yet. Ask your AI client to add blocks first.
- **Your AI client says the design changed since it read it.** Someone saved the page in the meantime. Ask your AI client to read the page again and to change only the blocks it needs, with `crm_page_patch`.
- **Your AI client says a block is not valid.** The answer names the block and the setting that is wrong. Ask your AI client to read the block catalogue and to try again.
- **The preview link does not open.** It is more than one hour old. Ask for a new one.

## Draft an email
- **The render lists warnings.** The warnings say what to fix in the design. Ask your AI client to fix it and to render the template again.
- **The test is refused.** Outgoing mail is not set up on your CRM, or the address is not valid. Check the address, or ask your admin about outgoing mail.
- **Your AI client says the design changed since it read it.** Someone saved the template in the meantime. Ask your AI client to read it again and to change only the blocks it needs, with `crm_email_template_patch`.
- **Your AI client cannot find a template.** The template is archived. Ask your AI client to include archived templates, and to restore the one you want.

## Find and move contacts and deals
- **Your AI client says the email address is already used.** Another contact has it, maybe one in the trash. Ask your AI client to find that contact, or to restore it, instead of adding a new one.
- **Your AI client cannot move a deal to Lost.** A deal moved to a lost stage needs a reason. Tell your AI client why the deal was lost.
- **Your AI client says a stage does not belong to the pipeline.** A deal moves only between the stages of its own pipeline. Ask it to read the pipeline first and to pick one of its stages.
- **A custom field is refused.** Your admin has not let the AI fill that field, or a person already typed a value. Fill it in yourself in the app.
- **Your AI client finds no contact by part of an email address.** You, the key or the agent have no contacts access, so `search_crm` matches an email address only when it is whole. Give the whole address, or the contact's name.
- **Your AI client says that the record changed after its call.** A person, an import or another key changed a field after your AI client did. The undo does not overwrite that change.
- **Your AI client cannot find a record that you can see in the app.** The record is in the trash, or your key's role does not reach that kind of record. Ask it to include records in the trash, or ask your admin about the agent's role.

## Build a workflow
- **Your AI client says that the workflow is not ready.** A step still needs something, such as an email. Ask your AI client which step, or open the workflow and fix the step in the builder.
- **Your AI client says that the workflow is live.** Your AI client cannot change or trash a live workflow. Pause it in **Workflows** first.
- **A version is not in the list.** The CRM keeps every version for 90 days, then the last 20.
- **A run stopped after a change.** A run that waited at a step that a change removed ends as failed when it resumes. The run log says that the step was removed.
- **Your AI client says that a step points at something archived.** The email template, form, tag, field or list of that step is in the trash. Ask your AI client to choose one that is live.
- **Your AI client says that it may not build workflows.** The key belongs to a member, or the key is **read only**. Ask an admin for a **read + write** key.
- **The Webinar registration template left a tag behind.** The template makes the tag *Attended*. The tag stays when the workflow goes to the trash.
