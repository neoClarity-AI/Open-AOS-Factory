---
title: Tool Access Matrix
file_type: config
schema_version: 1.0.0
builder_version: 1.0.0
created_date: 2026-06-04
last_updated: 2026-06-04
status: active
---

# Tool Access Matrix

Single source of truth for which agents may use which tools, and at what level. Owned by the Security / Permissions Agent. Values: **Allowed** (Level 1) | **Approval** (Level 2, gate with `Proceed`) | **Not configured** (no access until granted).

| Tool / Capability | Security | Memory | Chief of Staff | Review | Inbox | Calendar | Task | Project Mgr | Research |
|---|---|---|---|---|---|---|---|---|---|
| Read AOS files | Allowed | Allowed | Allowed | Allowed | Allowed | Allowed | Allowed | Allowed | Allowed |
| Write AOS files | Allowed | Allowed | Allowed | Allowed | Allowed | Allowed | Allowed | Allowed | Allowed |
| Delete / overwrite files | Approval | Approval | Approval | Approval | Approval | Approval | Approval | Approval | Approval |
| Move to /inbox/processed | — | — | — | — | Allowed | — | — | — | — |
| Move to /archive | Approval | Approval | Approval | Approval | Approval | Approval | Approval | Approval | Approval |
| Email / message read | Not configured | — | — | — | Not configured | — | — | — | — |
| Email / message send | — | — | — | — | Approval | — | — | — | — |
| Calendar read | — | — | — | — | — | Not configured | — | — | — |
| Calendar modify | — | — | — | — | — | Approval | — | — | — |
| Web search | — | — | — | — | — | — | — | — | Not configured |

**Notes**
- "Not configured" means the capability exists in principle but no external connector/scope has been granted yet. Connect the tool, then the Security Agent updates this matrix.
- New tools default to **Not configured** until explicitly granted.
- Agent configs reference this matrix; they do not restate or override it.
