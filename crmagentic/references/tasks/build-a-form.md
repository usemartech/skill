# Build a form

From the user guide: Build a form with your AI client; Build a form.

You ask your AI client to build a form with the questions you want, check the draft in the app, and put the form live. Your AI client builds the same form that you open in **Forms**, and a landing page can show it.

## Before you start

- You need the admin role to build or publish a form, and your AI client needs a **read + write** key.

## AI does through MCP

1. Ask what forms you have. Tools: `crm_form_list`, `crm_form_get`.
2. Ask for a new form. Tools: `crm_form_create`.
   - Only an email question can fill in the email address.
3. Ask for changes. Tools: `crm_form_set_fields`, `crm_form_update`.
   - To change only the texts or the confirmation email, `crm_form_update` changes the title, introduction, button text, thank-you message and the email template that each person gets after they send the form.
   - It never changes the questions, so it works on a live form that has responses too.
4. Ask your AI client to put the form live. Tools: `crm_form_publish`, `crm_form_unpublish`.
5. Ask your AI client to remove a draft that you do not need, such as a test form. Tools: `crm_form_archive`, `crm_form_restore`, `crm_form_unpublish`.
   - Your AI client cannot put a live form in the trash: it must take the form offline with `crm_form_unpublish` first.
6. Ask your AI client to undo a change to the questions or the texts. Tools: `crm_form_list_revisions`, `crm_form_restore_revision`.
   - On a live form that has responses, it puts back only the texts and keeps the questions.

Example request: *Build a registration form for our open day with first name, email, the session they want (morning or afternoon) and a consent box. Show "See you there!" after they send it. Keep it as a draft.*

## The person does in the app

- Check the draft in the app. Open the form in **Forms** and look at it in the builder before it goes live.

### Build a form — **Marketing & automation → Forms** (/forms)
1. In the sidebar, select **Marketing & automation → Forms** (/forms).
2. Select **New form**.
3. The form opens on its **Build** tab.
4. Select the **Settings** tab.
5. Select **Save**, then **Publish**.
6. Select the **Share** tab.
7. Test the form.

If a tool refuses, read references/troubleshooting/build-a-form.md.
