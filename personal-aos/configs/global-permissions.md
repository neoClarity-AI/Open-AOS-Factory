---
title: Global Permissions
file_type: config
schema_version: 1.0.0
builder_version: 1.0.0
created_date: 2026-06-04
last_updated: 2026-06-04
status: active
---

# Global Permissions

The three-level permission model governs every action any agent takes. The Security / Permissions Agent owns this file and is the escalation target for all permission questions.

## Level 1 — Safe (pre-authorized)
Acted on without asking. Includes:
- Reading files within approved scope.
- Drafting messages, documents, and content (without sending or publishing).
- Creating and updating AOS markdown files (memory, logs, task lists, project files).
- Moving processed inbox items into `/inbox/processed` (the single pre-authorized move).

## Level 2 — Approval-required (gate with `Proceed`)
The agent describes the action and waits for the user to type `Proceed`. Includes:
- Sending or publishing any communication (email, message, post).
- Modifying the calendar, especially events involving other people.
- Deleting or overwriting any existing file.
- Moving files into an `/archive` (global or project).
- Sharing data with any external party or new external tool.
- First use of any newly added tool.

## Level 3 — Prohibited
Refused outright and logged; escalate to the Security Agent. Includes any action the user has explicitly prohibited and anything unsafe, irreversible, or outside granted scope with no approval path.

## Autonomy posture
This instance runs at **Balanced**: agents auto-handle Level 1 work and proactively prepare Level 2 actions for one-tap approval, escalating anything important or irreversible.

## Precedence
Agent configs reference this file; they never duplicate or override it. Where an agent needs a tighter rule, it is recorded as an agent-specific note, not a looser global default.
