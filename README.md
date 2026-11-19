# skill

A skill that helps an AI client use a crmagentic workspace through its MCP server: what to ask the AI to do, what to do by hand in the app, and where each setting is.

The skill is in the `crmagentic/` folder: `SKILL.md` and its `references/`. It covers six jobs: build a form, build a landing page, draft an email, find and move contacts and deals, build a workflow, and undo a mistake. It also has a map of every screen and setting, the rules the AI client follows, and what to do when a tool refuses.

This repository is generated from the crmagentic user guide and a reviewed set of opinion files. Do not edit it by hand; changes are overwritten on the next release. Report problems as issues.

## Before you install

Connect your AI client to your workspace first. In the app, go to **Settings → MCP server** and follow **Connect your AI client**. Only an admin can issue a key. A **read only** key can look things up; a **read + write** key can also make drafts and changes.

## Install

### Claude Code

For yourself, in every project:

```sh
git clone --depth 1 https://github.com/usemartech/skill.git /tmp/usemartech-skill
mkdir -p ~/.claude/skills
cp -R /tmp/usemartech-skill/crmagentic ~/.claude/skills/
```

For one project only, copy the folder to `.claude/skills/crmagentic/` in that project instead. Start a new Claude Code session, then ask, for example: *Build a welcome workflow for new contacts as a draft.*

### Claude.ai and Claude Desktop

Download `crmagentic.zip` from the latest release on this repository. In Claude, open **Settings → Capabilities** and upload the zip under **Skills**.

### Other AI clients

A client that reads skills as a folder with a `SKILL.md` takes the `crmagentic/` folder as it is. Put it where that client keeps its skills.

## Versions

The skill names the crmagentic version that it was built for. When it connects, it compares that with the version the workspace reports. If they differ, it tells you to update the skill, and it follows the tools' own descriptions where the two disagree. To update, repeat the install with the latest release.
