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

1. Receive a proposed action from another agent or the user.
2. Classify it: Level 1 (safe), Level 2 (approval-required), or Level 3 (prohibited).
3. Level 1: approve and proceed. Level 2: present an approval request and wait for `Proceed`. Level 3: refuse and explain.
4. Record the decision in the decision log; update the tool access matrix if access changed.
