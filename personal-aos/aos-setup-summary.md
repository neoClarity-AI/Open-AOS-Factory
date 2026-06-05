---
title: AOS Setup Summary
file_type: setup_summary
schema_version: 1.0.0
builder_version: 1.0.0
created_date: 2026-06-04
last_updated: 2026-06-04
status: active
---

# AOS Setup Summary

## AOS Name and Location
- **Name:** personal-aos
- **Purpose:** Personal · **Autonomy:** Balanced
- **Location:** `AOS-03/personal-aos/` (created inside the connected framework folder; can be relocated to a true sibling if the parent folder is connected)

## Folders Created
`agents/`, `workflows/`, `memory/`, `projects/`, `logs/`, `templates/`, `configs/`, `docs/`, `inbox/processed/`, `archive/` — plus a 7-file folder set per agent.

## Global Files Created (29)
Manifest + map; 3 configs (global-permissions, agent-registry, tool-access-matrix); 6 memory files; 2 logs; 9 workflows; 6 templates; the AOS User Guide (`docs/aos-user-guide.html`).

## Required Agents Built (4)
Security / Permissions · Memory · Chief of Staff · Review / Reflection — all active.

## Optional Agents Built (6)
Inbox · Calendar · Task · Project Manager · Research · Writing — all active.
Available but not installed: Automation, Document Librarian, Finance, Health & Life Logistics, Learning, Personal CRM.

## Permissions and Tool Access Baseline
Global three-level permission model. Sending, calendar-modify, delete/overwrite, archive-moves, and new-tool use are approval-gated (`Proceed`). External connectors (email, calendar, web search) are **Not configured** until granted — the Security Agent updates the matrix when you connect a tool.

## Operating Rhythms Installed
All 9 workflows: daily startup, end-of-day shutdown, weekly/monthly/quarterly review, inbox-to-task, project kickoff, decision capture, memory review.

## Open Questions
- ~~Name vs. the Personal purpose~~ — resolved 2026-06-04: renamed from `work-aos` to `personal-aos`.
- Connect real tools (email, calendar, web search) so Inbox/Calendar/Research can act beyond drafting/proposing?
- Add Automation and/or Learning now, or leave available?

## Suggested Next Steps
1. Open the AOS User Guide for the full invocation reference.
2. Connect email/calendar/web-search tools, then have the Security Agent grant access in the matrix.
3. Try it: ask the Chief of Staff "What should I focus on today?" or start a project via the Project Manager.
