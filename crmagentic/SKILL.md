---
name: crmagentic
description: "How to work in a crmagentic CRM workspace through its MCP server (the crm_* tools): build a form, build a landing page, draft an email, find and move contacts and deals, build a list, build a workflow, set up a pipeline, set up webhooks and background jobs, research a contact or company, do design work handed to you, undo a mistake, and where each screen and setting is in the app. Use it when the person asks for one of these jobs, or asks where something is."
metadata:
  version: "0.1.0"
---
# crmagentic

This skill is built from the user guide of crmagentic 0.1.0. It says in what order to call the tools, what only the person can do in the app, and where that is. The tools' own descriptions stay the truth for their inputs.

## First, compare the versions

The MCP handshake answers `serverInfo.version`. This skill is version 0.1.0. When the two differ, tell the person: "This skill is for crmagentic 0.1.0, and the workspace runs <server version>: update the skill." Then go on, and where the skill and a tool's description differ, follow the tool.

## Find the reference

Read only the references that match the request; one request can match more than one. A request that matches none: say that the skill has no guidance for it, and work from the tools' own descriptions.

| The person says | Read |
| --- | --- |
| form, lead form, signup form, registration form, survey, questions | references/tasks/build-a-form.md |
| landing page, page, website page, signup page, event page, funnel, blog, blog post, chatbot, media folder | references/tasks/build-a-landing-page.md |
| email, newsletter, email template, mailer, announcement, campaign, draft campaign, a/b test, subject test, template folder, content calendar, social post, source, utm | references/tasks/draft-an-email.md |
| find a contact, lead, company, deal, move a deal, stage, owner, task, note, product, service, catalog, persona | references/tasks/find-and-move-records.md |
| list, segment, static list, dynamic list, audience, add to a list, remove from a list, who gets the campaign, lead score, scoring rule, website tracking, dynamic content | references/tasks/build-a-list.md |
| workflow, automation, automate, drip, nurture, sequence, follow-up, welcome series, when someone signs up, trigger, saved view, list to watch, custom field, date field, rename a tag, snippet, email sequence, onboarding emails, after a form is sent, after someone registers | references/tasks/build-a-workflow.md |
| pipeline, new pipeline, sales process, stage, add a stage, rename a stage, won stage, lost stage, probability | references/tasks/set-up-a-pipeline.md |
| webhook, tell another system, send events to another system, integration, background job, job schedule, run every | references/tasks/set-up-webhooks-and-jobs.md |
| research, look up, enrich, who is, linkedin, job change, background, photo, recheck, what we sell, who we are | references/tasks/research-a-contact-or-company.md |
| work item, design work, my work, assigned to me, what should I work on, mark it done | references/tasks/do-design-work.md |
| undo, revert, put it back, restore, trash, delete, last change | references/tasks/undo-a-mistake.md |
| where is, which screen, which setting, how do I get to | references/ui-map.md |
| key, role, access, draft, published, workspace | references/concepts.md |
| delete, publish, send, go live, what you will not do | references/rules.md |
| an error or a refusal from a tool | references/troubleshooting.md, then the file it names for the job |

## Rules in short

- Make drafts. Publish a form or a page only after the person says yes, and never set a workflow live, pause it or start a run (there is no tool for it; the person does it in the app).
- Never delete for good. Archive puts an item in the trash, and restore brings it back.
- A published form or page goes to the trash only after `crm_*_unpublish`, and that takes it offline for visitors, so ask first. A live workflow is paused by the person in the app.
- After each change, say what you changed and how to undo it.
- You act as the person who connected you. A refusal for role or access is final; do not try another tool to get round it.
- Search first and pass the ids that a result gave you; never guess an id or a path.

references/rules.md has them in full.

## Hand a step back to the person

When a step has no tool, tell the person exactly where to go, with the path as references/ui-map.md writes it, say what to look for, and ask them to tell you when it is done. Then go on. Never guess a path that is not in the map. Publish, send or change a live item only after the person says yes.
