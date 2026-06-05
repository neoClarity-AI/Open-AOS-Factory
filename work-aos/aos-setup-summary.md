---
title: AOS Setup Summary
file_type: aos_setup_summary
schema_version: 1.0.0
builder_version: 1.0.0
created_date: 2026-06-04
last_updated: 2026-06-04
status: active
---

# AOS Setup Summary

## AOS Name and Location
- **Name:** work-aos
- **Purpose:** Professional / work
- **Location:** `/work-aos` (sibling of the builder framework, inside the AOS-03 folder)

## Folders Created
`agents`, `workflows`, `memory`, `projects`, `logs`, `templates`, `configs`, `docs`, `inbox` (+ `inbox/processed`), `archive`.

## Global Files Created
29 files: `aos-manifest.md`, `aos-map.md`; 3 configs (global-permissions, agent-registry, tool-access-matrix); 6 memory files (user-profile, preferences, people, projects, decisions, agent-learnings-index); 2 logs (aos-decision-log, change-log); 9 workflows; 6 templates; and `docs/aos-user-guide.html`.

## Required Agents Built
Security / Permissions, Memory, Chief of Staff, Review / Reflection — each with the standard seven-file set.

## Optional Agents Built
Inbox / Communications, Calendar / Scheduling, Task / Commitment, Project Manager, Research — each with the standard seven-file set.

## Permissions and Tool Access Baseline
- Global three-level permission model (Safe / Approval-required / Prohibited).
- Autonomy posture: **Balanced**.
- Tool access matrix is the single source of truth; external connectors (email, calendar, web search) start **Not configured** until granted.

## Operating Rhythms Installed
All five reviews (daily startup, end-of-day shutdown, weekly, monthly, quarterly) plus inbox-to-task, project-kickoff, decision-capture, and memory-review.

## Open Questions
- Which external tools to connect first (email, calendar, web search) so Security can update the matrix.
- Role/goals/constraints to enrich the user profile.

## Suggested Next Steps
1. Ask the Chief of Staff for a daily brief to see the system run.
2. Connect a tool (e.g., calendar or email) and have Security update the tool access matrix.
3. Add the Writing Agent or any other available agent later via its builder.
