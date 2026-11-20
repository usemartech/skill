# Build a list

From the user guide: Build a list with your AI client; Lead scoring, website tracking and dynamic content with your AI client; Lists you fill by hand; Build a dynamic list; Lead scoring; Dynamic content.

You ask your AI client to make a list in **Lists & segments**, add people to it or take them off, change it, undo a change, and put it in the trash. A static list holds the records that you add by hand. A dynamic list, or segment, holds the records that match its rules. An email campaign sends to a list of contacts, and a workflow can start when someone joins or leaves a list. You ask your AI client to set up the rules of the lead score, to add a website to track, and to write a dynamic content block. Your AI client works on the same rules, websites and blocks that you open in **Lead scoring**, **Website tracking** and **Dynamic content**.

## Before you start

- Your AI client needs a **read + write** key.
- To read who is on a list of contacts, you need access to contacts.
- Your AI client needs an admin's **read + write** key to change a rule, a website or a block.
- Know what makes a contact worth a call.
- To show a block to some people only, have the contact list ready.

## AI does through MCP

1. Ask what lists you have. Tools: `crm_list_list`, `crm_list_get`, `crm_list_records`.
2. Ask for a new list. Tools: `crm_list_create`.
   - The name must be new among your lists.
   - The list belongs to you, and only you see it until you share it.
3. Add people to a static list, or take them off. Tools: `crm_list_add_members`, `crm_list_remove_members`.
   - A dynamic list takes its members from its rules, so your AI client adds people to a static list only.
4. Ask for a change. Tools: `crm_list_update`.
   - Only the person who owns a list can change it.
5. Undo a change. Tools: `crm_list_restore_values`.
6. Ask your AI client to remove a list that you do not need. Tools: `crm_list_archive`, `crm_list_restore`.
   - Your AI client cannot put a list in the trash while a scheduled campaign sends to it, or while a live workflow watches it or reads it.
7. Ask for a lead scoring rule. Tools: `crm_score_rule_create`, `crm_score_rule_update`, `crm_score_rule_list`, `crm_score_rule_get`.
8. Ask for a website to track. Tools: `crm_tracking_site_create`, `crm_tracking_site_update`.
9. Ask for a dynamic content block. Tools: `crm_tracked_content_create`.
10. Undo a change. Tools: `crm_score_rule_restore_values`, `crm_tracking_site_restore_values`, `crm_tracked_content_restore_values`.
11. Ask your AI client to remove what you do not need. Tools: `crm_score_rule_archive`, `crm_tracking_site_archive`, `crm_tracked_content_archive`, `crm_score_rule_restore`, `crm_tracking_site_restore`, `crm_tracked_content_restore`.

Example request: *Make a list called Webinar guests and add the contacts who registered for the webinar.*
Example request: *Add an engagement rule that gives 10 points for each chatbot conversation, up to 30 points.*

## The person does in the app

### Lists you fill by hand — **Core CRM → Lists & segments** (/lists)
1. In the sidebar, select **Core CRM → Lists & segments** (/lists).
2. Select **New list**.
3. The app opens your new list.
4. Select **Add contacts**.
5. To take a record off the list, select **Remove** on its row.

### Build a dynamic list — **Core CRM → Lists & segments** (/lists)
1. In the sidebar, select **Core CRM → Lists & segments** (/lists), then select **New dynamic list**.
2. Enter a **Name**, for example *Registered through a landing page*.
3. Build the rule from its three parts.
4. To leave people out, use **is not** as the test.
5. Select **Share with everyone** if your team should see the segment, then select **Create**.
6. To change the rules later, select **Filters** in the **Definition** card.
7. You can also start from the **Contacts** page.

### Lead scoring — **Settings → Lead scoring** (/settings/scoring)
1. Go to **Settings**, then **Lead scoring**.
2. To move the ranges, change **Warm from** and **Hot from**, then select **Save ranges**.
3. Scroll down to the rules.
4. To add a rule that counts what people do, select **New engagement rule**.
5. To add a rule on the contact record, select **New fit rule**.
6. To stop a rule for a while, switch it off in the **State** column.
7. The rules that you moved to the trash show under **Trash**.

### Dynamic content — **Marketing & automation → Dynamic content** (/marketing/content)
1. Press ⌘ K (Ctrl K on Windows), or select **Go to…** at the top of the sidebar.
2. To make a block, select **New block**.
3. Under **Default**, change the **Text** if you need to.
4. To add a version, select **Add a version**.
5. Select **Save**.
6. To use the block, look under **Use it** on the right.

If a tool refuses, read references/troubleshooting.md.
