---
title: "Getting started"
description: "Go from a new docs account to a working setup in one sitting, with a checkpoint after every step so you know it worked."
status: generated
version: "0.1"
---

This page takes you from nothing to a working docs setup. Every step ends with a checkpoint: something you can look at to confirm it worked before you move on. If a checkpoint fails, stop there — the next step will not fix it.

## Before you begin

- An account, and permission to create whatever docs calls a project or a workspace.
- Somewhere safe for a credential: a password manager, or your platform's secret store.
- Fifteen uninterrupted minutes.

> **Fill this in:** list the real prerequisites — a supported runtime version, a minimum plan, an admin role. Readers forgive a long list at the top; they do not forgive finding out about one halfway through.

## 1. Create a project

Sign in and create your first project. Give it the name your team already uses for this work rather than a test name — first projects have a habit of becoming production.

**Checkpoint:** the project appears in the sidebar under a name you recognise.

## 2. Connect it to something real

A product like this only becomes useful once it is pointed at your own data. Do that now, with a small, low-risk source rather than your largest one.

```bash
export API_TOKEN="paste-your-token-here"

curl -X POST "https://api.example.com/v1/projects" \
  -H "Authorization: Bearer $API_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{"name": "first-project", "source": "sandbox"}'
```

> **Fill this in:** replace the host, the path and the fields above with a request that actually works, and say what a successful response looks like.

**Checkpoint:** the response carries an id, and the project shows the connection as active.

## 3. Do the thing the product is for

Run the core workflow once, end to end, against that small source. Resist configuring anything else until you have seen one result.

**Checkpoint:** you can point at an output and say what produced it.

## When a step fails

Read the error text before changing anything — most setup errors name the field they object to. Then check the three usual suspects: the credential belongs to a different environment, the account is missing a permission, or a required field was left empty.

## Next steps

- [What docs can do](features/overview.md) — what else is available now that it runs.
- [Invite your team](guides/invite-your-team.md) — add the people who will use it daily.
- [FAQ](faq.md) — the questions that come up right after setup.
