# Build a landing page

From the user guide: Build a landing page with your AI client; Build a landing page.

You ask your AI client to draft a landing page from the blocks the designer has, check the draft through a preview link, and publish it when you are happy. Your AI client works on the same page you open in the designer.

## Before you start

- Connect your AI client with a **read + write** key.
- Know what the page is for and what visitors should do on it, such as sign up for an event.

## AI does through MCP

1. Ask what a page can hold. Tools: `crm_page_block_catalog`.
2. Ask for a draft. Tools: `crm_page_create`, `crm_page_patch`, `crm_page_preview`, `crm_page_update`.
3. Ask for changes. Tools: `crm_page_patch`, `crm_page_get`, `crm_page_get_design`, `crm_page_set_design`, `crm_page_update`.
4. To use your own images, upload them to the Media library first. Tools: `crm_media_list`, `crm_media_upload`, `crm_media_archive`, `crm_media_restore`.
   - A file that is larger than 25 MB is refused.
   - A file that a published page or a sent email shows cannot go to the trash: take the page offline or take the image out of it first.
5. Ask your AI client to publish. Tools: `crm_page_publish`, `crm_page_unpublish`.
6. To go back to an earlier version, ask your AI client. Tools: `crm_design_revision_list`, `crm_design_revision_get`, `crm_design_revision_restore`.

Worked example (page-block-catalog): `crm_page_block_catalog`.
Worked example (draft-a-page): `crm_page_create` → `crm_page_patch` → `crm_page_preview` → `crm_page_update`.

Example request: *What blocks can a landing page have?*

## The person does in the app

- Open the preview link. It shows the draft as visitors would see it, and it works for one hour. Ask for a new link when it runs out.

### Build a landing page — **Marketing & automation → Landing pages** (/marketing/pages)
1. In the sidebar, select **Marketing & automation → Landing pages** (/marketing/pages).
2. Select **New page**.
3. Select **Open designer**.
4. Back on the page, under **Lead capture**, choose what the form asks: tick **First name**, **Last name**, **Email**, **Phone** and **Company**.
5. Select **Publish**.
6. Test the page.

If a tool refuses, read references/troubleshooting.md.
