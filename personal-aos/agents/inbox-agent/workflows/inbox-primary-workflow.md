---
title: Inbox Primary Workflow
file_type: workflow
schema_version: 1.0.0
builder_version: 1.0.0
created_date: 2026-06-04
last_updated: 2026-06-04
status: active
---

# Inbox Primary Workflow

Primary workflow for the Inbox / Communications Agent.

1. Read incoming items and classify each (urgent / waiting / FYI / archive).
2. Draft responses where useful.
3. Promote items to the owning agent via inbox-to-task; move the source to `/inbox/processed`.
4. Send only after `Proceed`. Log promotion and send decisions.
