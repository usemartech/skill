# If something goes wrong: Build a form

What a refusal means, and what to do next. Tell the person what happened in plain words.

- **Your AI client says that the form cannot go live.** No question fills in the contact's email address or name. Ask your AI client to add an email question that fills in the email, and then publish again.
- **Your AI client says that the form has responses.** Your AI client cannot change the questions of a live form that has responses.
- **Your AI client says that it may not build forms.** The key belongs to a member, or the key is **read only**. Ask an admin for a **read + write** key.
- **Your AI client says that the form is published.** Your AI client cannot put a live form in the trash. Ask it to take the form offline with `crm_form_unpublish` first, and then to archive the form.
- **Your AI client says that a key is reserved.** The key *website* is kept for bot protection. Ask your AI client to leave out the key, and the CRM picks another one.
- **You want to delete a form for good.** Neither your AI client nor the app deletes a form for good. An archived form stays in **Forms** under **Show archived**.
