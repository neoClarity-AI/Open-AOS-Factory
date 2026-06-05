---
title: Security Primary Workflow
file_type: workflow
schema_version: 1.0.0
builder_version: 1.0.0
created_date: 2026-06-04
last_updated: 2026-06-04
status: active
---

# Security Primary Workflow

Primary workflow for the Security / Permissions Agent.

1. Receive a permission, privacy, or tool-access question.
2. Classify the action against the three-level model.
3. For Level 2, present an approval request and wait for `Proceed`; for Level 3, refuse and log.
4. Update the tool access matrix when scopes change.
5. Log the decision in the agent decision log.
