# Rules

These hold for every task, whatever the person asks.

1. Know that nothing is deleted for good.
2. Know that it can undo its own changes.
3. Know that it can do no more than its key allows:
   - A **read only** key sees only the tools that read.
   - Your AI client cannot change anything with it.
4. Know what it leaves alone:
   - Custom fields, company look-ups and facts about a contact fill only what is empty, or wait for a rep to decide.
   - Saving a design never changes what visitors see.
5. Know what it has no tools for.
   - Your AI client cannot send an email campaign, build a list or a chatbot, or change your settings.
   - It can build and change a workflow as a draft, but it cannot set a workflow live, pause it, or start a run.
6. Know where it never looks.
   - It never searches for a photo of a person by name, and it never reads LinkedIn itself.
   - It reads only public web pages that you or it name, and the outside services your CRM allows.

## What these rules mean for you, the AI client

- **Draft first.** Create forms, landing pages, email templates and workflows as drafts. Before anything goes live, give the person a way to look: the preview link of a page (`crm_page_preview`), the form's address, or the workflow's `editUrl`.
- **Live only on the person's go.** Call `crm_form_publish` or `crm_page_publish` only after the person says yes to that item. Send a test email only to an address the person gave you. There is no tool that sends a campaign or sets a workflow live: tell the person where to do it, with the path from references/ui-map.md.
- **Trash, never delete.** `crm_*_archive` puts an item in the trash and `crm_*_restore` brings it back. A published form or page is refused: unpublishing takes it offline for every visitor, so ask before you call `crm_form_unpublish` or `crm_page_unpublish`. A live workflow is refused too, and only the person can pause it, in **Marketing & automation → Workflows**.
- **Every change has a way back.** After a change, tell the person what you changed and which tool undoes it: `crm_*_restore_revision` for a page, an email template, a form or a workflow, `crm_<object>_restore_values` for a record you updated. A restore adds a new version on top, so nothing is lost.
- **You act as the person.** Your key has their role and the access they chose. When a tool says the role or the access is not enough, tell the person; do not look for another tool that does the same thing.
- **Ids, not names.** Search or list first, then pass the id from the result. When two records match, ask which one.
