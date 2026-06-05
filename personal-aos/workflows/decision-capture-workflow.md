---
title: Decision Capture Workflow
file_type: workflow
schema_version: 1.0.0
builder_version: 1.0.0
created_date: 2026-06-04
last_updated: 2026-06-04
status: active
---

# Decision Capture Workflow

Available to any agent; chronological record owned via `/logs/aos-decision-log.md`.

1. Capture the decision using `/templates/decision-entry-template.md`.
2. Record context, options considered, decision, and rationale.
3. System-wide decisions go to `/logs/aos-decision-log.md`; project-specific ones to that project's `project-decisions.md`.
4. Memory Agent adds durable, frequently-referenced decisions to `/memory/decisions.md`.
