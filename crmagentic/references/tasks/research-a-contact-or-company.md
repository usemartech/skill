# Research a contact or company

From the user guide: Research a contact or company.

You ask your AI client to find out more about a company or a contact: what a company does, who a contact is and where they work now. It writes what it finds into the CRM with the evidence for it, so a rep can trust it or check it.

## Before you start

- Connect your AI client with a **read + write** key.
- These tools are there only while the AI agent is on in your workspace.
- Some of these tools reach the internet.

## AI does through MCP

1. Ask what is left to research. Tools: `list_outstanding_work`.
   - `list_outstanding_work` lists the open research tasks and the records nobody has asked about yet: contacts with no background, contacts with no photo and companies that were never looked up.
   - It reads only.
2. Ask your AI client to look a company up. Tools: `enrich_company`, `research_web`.
   - It never overwrites what a person typed.
3. Ask your AI client to check who a contact is. Tools: `identify_contact`, `record_fact`, `resolve_linkedin_profile`, `cross_check_social`, `fetch_contact_photo`.
   - It never opens LinkedIn: your AI client passes it what it read on the page.
   - It never searches for a photo by name.
4. Ask your AI client to note a job change. Tools: `record_job_change`.
5. Ask for a background. Tools: `write_contact_background`.
6. Tell your AI client what your company sells. Tools: `write_workspace_profile`.
7. Ask for another look later. Tools: `schedule_recheck`, `crm_recheck_cancel`.
8. Undo a research step. Tools: `crm_company_restore_values`, `crm_contact_restore_values`, `crm_photo_undo`.

Worked example (list-outstanding-work): `search_crm` → `list_outstanding_work`.

Example request: *What research is still open on Koss Group?*

## The person does in the app

If a tool refuses, read references/troubleshooting/research-a-contact-or-company.md.
