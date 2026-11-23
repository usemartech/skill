# If something goes wrong: Find and move contacts and deals

What a refusal means, and what to do next. Tell the person what happened in plain words.

- **Your AI client says the email address is already used.** Another contact has it, maybe one in the trash. Ask your AI client to find that contact, or to restore it, instead of adding a new one.
- **Your AI client finds the same person twice.** It cannot merge records. Merge them yourself at **Settings → Duplicates** (/settings/duplicates).
- **Your AI client cannot move a deal to Lost.** A deal moved to a lost stage needs a reason. Tell your AI client why the deal was lost.
- **Your AI client says a stage does not belong to the pipeline.** A deal moves only between the stages of its own pipeline. Ask it to read the pipeline first and to pick one of its stages.
- **A custom field is refused.** Your admin has not let the AI fill that field, or a person already typed a value. Fill it in yourself in the app.
- **Your AI client finds no contact by part of an email address.** You, the key or the agent have no contacts access, so `search_crm` matches an email address only when it is whole. Give the whole address, or the contact's name.
- **Your AI client says that the record changed after its call.** A person, an import or another key changed a field after your AI client did. The undo does not overwrite that change.
- **Your AI client cannot find a record that you can see in the app.** The record is in the trash, or your key's role does not reach that kind of record. Ask it to include records in the trash, or ask your admin about the agent's role.
