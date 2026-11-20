# Build a landing page

From the user guide: Build a landing page with your AI client; Funnels, blog posts and chatbots with your AI client; Build a landing page; Funnels; Blog; Chatbots.

You ask your AI client to draft a landing page from the blocks the designer has, check the draft through a preview link, and publish it when you are happy. Your AI client works on the same page you open in the designer. You ask your AI client to put your landing pages in order as a funnel, to write and publish a blog post, and to build a draft chatbot. Your AI client works on the same funnels, posts and chatbots that you open in **Funnels**, **Blog** and **Chatbots**.

## Before you start

- Connect your AI client with a **read + write** key.
- Know what the page is for and what visitors should do on it, such as sign up for an event.
- Your AI client needs an admin's **read + write** key to change a funnel, a post or a chatbot.
- Have the landing pages of the funnel ready.
- To put a chatbot on your website, the website must be a tracked site.

## AI does through MCP

1. Ask what a page can hold. Tools: `crm_page_block_catalog`.
2. Ask for a draft. Tools: `crm_page_create`, `crm_page_patch`, `crm_page_preview`, `crm_page_update`.
3. Ask for changes. Tools: `crm_page_patch`, `crm_page_get`, `crm_page_get_design`, `crm_page_set_design`, `crm_page_update`.
4. To use your own images, upload them to the Media library first. Tools: `crm_media_list`, `crm_media_upload`, `crm_media_archive`, `crm_media_restore`, `crm_media_update`, `crm_media_restore_values`, `crm_media_folder_list`, `crm_media_folder_create`, `crm_media_folder_rename`, `crm_media_folder_remove`.
   - A file that is larger than 25 MB is refused.
   - A file that a published page or a sent email shows cannot go to the trash: take the page offline or take the image out of it first.
5. Ask your AI client to publish. Tools: `crm_page_publish`, `crm_page_unpublish`.
6. To go back to an earlier version, ask your AI client. Tools: `crm_design_revision_list`, `crm_design_revision_get`, `crm_design_revision_restore`, `crm_page_list_revisions`, `crm_page_restore_revision`.
7. Ask your AI client to tidy up. Tools: `crm_page_list`, `crm_page_archive`, `crm_page_restore`, `crm_page_unpublish`.
   - A published page cannot go to the trash: your AI client takes it offline with `crm_page_unpublish` first, so it asks you before.
8. Ask for a funnel. Tools: `crm_funnel_create`, `crm_funnel_set_steps`, `crm_funnel_update`, `crm_funnel_list`, `crm_funnel_get`.
9. Ask for a blog post. Tools: `crm_blog_post_create`, `crm_blog_post_update`, `crm_blog_post_list`, `crm_blog_post_get`.
10. Publish the post only when you are ready. Tools: `crm_blog_post_publish`, `crm_blog_post_unpublish`.
11. Ask for a chatbot. Tools: `crm_chatbot_create`, `crm_chatbot_update`, `crm_chatbot_list`, `crm_chatbot_get`.
12. Undo a change. Tools: `crm_funnel_restore_values`, `crm_blog_post_restore_values`, `crm_chatbot_restore_values`.
13. Ask your AI client to remove what you do not need. Tools: `crm_funnel_archive`, `crm_blog_post_archive`, `crm_chatbot_archive`, `crm_funnel_restore`, `crm_blog_post_restore`, `crm_chatbot_restore`.

Worked example (page-block-catalog): `crm_page_block_catalog`.
Worked example (draft-a-page): `crm_page_create` → `crm_page_patch` → `crm_page_preview` → `crm_page_update`.

Example request: *What blocks can a landing page have?*
Example request: *Make a funnel called Open day from the Open day page and the Thank you page, in that order.*

## The person does in the app

- Open the preview link. It shows the draft as visitors would see it, and it works for one hour. Ask for a new link when it runs out.

### Build a landing page — **Marketing & automation → Landing pages** (/marketing/pages)
1. In the sidebar, select **Marketing & automation → Landing pages** (/marketing/pages).
2. Select **New page**.
3. Select **Open designer**.
4. Back on the page, under **Lead capture**, choose what the form asks: tick **First name**, **Last name**, **Email**, **Phone** and **Company**.
5. Select **Publish**.
6. Test the page.

### Funnels — **Marketing & automation → Funnels** (/marketing/funnels)
1. In the sidebar, select **Marketing & automation → Landing pages** (/marketing/pages), then **Funnels**.
2. Select **New funnel**.
3. Under **Steps**, choose the first page in **Add a page** and select **Add step**.
4. Select **Save steps**.
5. Publish every page of the funnel.
6. Test the funnel.

### Blog — **Marketing & automation → Blog** (/marketing/blog)
1. In the sidebar, select **Marketing & automation → Landing pages** (/marketing/pages).
2. To start a post, select **New post**.
3. Write the post.
4. When the post is ready, select **Publish**.
5. To take a live post off your blog, select **Unpublish**.
6. To put a post away, select **Archive**, in the list or on the post.

### Chatbots — **Marketing & automation → Chatbots** (/marketing/chatbots)
1. Press ⌘ K, type *chatbots* and select **Chatbots**.
2. Select **New chatbot**.
3. Build the flow.
4. Try the bot in the **Preview** on the right.
5. Put the bot live.
6. To see how the bot does, select **Report**: at the top of the builder, or beside the bot in the list.

If a tool refuses, read references/troubleshooting/build-a-landing-page.md.
