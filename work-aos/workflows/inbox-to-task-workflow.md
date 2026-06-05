---
title: Inbox-to-Task Workflow
file_type: workflow
schema_version: 1.0.0
builder_version: 1.0.0
created_date: 2026-06-04
last_updated: 2026-06-04
status: active
---

# Inbox-to-Task Workflow

Primary owner: Inbox Agent, in collaboration with Task, Calendar, Project Manager, and Memory.

1. For each triaged item, decide its destination: task, project, calendar item, memory, decision, or archive.
2. Promote to the owning agent (e.g., create a task via the Task Agent).
3. Move the processed source item to `/inbox/processed` (the only pre-authorized move).
4. Anything requiring a send/publish is gated by `Proceed`.
5. Log promotion decisions.
