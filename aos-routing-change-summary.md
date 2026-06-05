---
title: AOS Change Summary — Instance Routing
file_type: change_summary
schema_version: 1.0.0
builder_version: 1.0.0
created_date: 2026-06-05
last_updated: 2026-06-05
status: handoff
purpose: Starting point for a new conversation to fold these changes into the builder files.
---

# AOS Change Summary — Instance Routing

## Context / motivation
AOS-03 holds two parallel instances (`work-aos`, `personal-aos`) that share one
Gmail inbox (martin@neoclarity.ai). A daily-brief request surfaced that nothing
designated an active instance, so routing was ambiguous and an agent could
silently pick or blend the two. These changes add an explicit, model-robust
routing layer (ask-don't-guess) so the arrangement holds up even on a lighter
model such as Sonnet 4.6. Default instance is **work-aos**.

## Files created

### 1. `/claude.md` (project root) — NEW
Root project instruction file; now serves as the session-start instruction file
(it replaces `nc-common-instructions.md`, so the router is wired into the
session-start chain here — no external edit needed). Contains AOS frontmatter
(`file_type: project_instructions`) plus two sections:
- **Planning mode** — on "Planning mode"/"pmode", make no file changes until the
  user says "Proceed"; display proposed changes and ask first.
- **Instance routing** — "read `/aos-router.md` and resolve the active instance
  before running any workflow."
(Note: a `clod.md` was created earlier in the session and then deleted; net new
file is `claude.md` only.)

### 2. `/aos-router.md` (project root) — NEW
New file type `aos_router`. Top-level router read before any instance loads.
Sections:
- **§1 Resolution order:** explicit user override → session pin → signal match →
  fallback ASK (never silently pick or merge).
- **§2 Classification signals:** default = `work-aos`; work vs. personal signal
  lists; note that the shared inbox is not itself a routing signal.
- **§3 Confidence bar:** auto-route only on clear one-sided signals; cross-
  instance requests run each instance separately and stay labeled.
- **§4 Session pin:** set/clear an active instance for the session; state the
  active instance on the first line of routed output.
- **§5 Logging:** record non-trivial routing choices to the active instance's
  `agents/chief-of-staff-agent/logs/chief-of-staff-decision-log.md`.

## Files edited

### 3. `personal-aos/aos-manifest.md` and `work-aos/aos-manifest.md`
Added a pointer blockquote directly under `# AOS Manifest`:
> Instance selection is governed by `/aos-router.md`. Do not assume this
> instance is active.

## Not yet done — for the builder pass to formalize
- **Schema registration:** new `file_type` values `aos_router` and
  `project_instructions` should be added to whatever the builder validates
  file types against.
- **Chief of Staff ownership:** the router is described as jointly owned by the
  two Chief of Staff agents — reflect router resolution/ownership in the
  chief-of-staff agent definitions and `configs/agent-registry.md`.
- **Daily startup workflow:** `daily-startup-workflow.md` is currently identical
  in both instances and has no instance-resolution step; add a step that resolves
  via the router before gathering inputs.
- **Differentiated content:** routing only produces different results once
  work vs. personal memory/projects diverge; the builder should ensure
  instance-specific signals (aliases, project lists) are populated.

## Decisions made by the user this session
- Default instance set to **work-aos**.
- Safety posture: ASK on weak/mixed signals rather than auto-select.
- Planning-mode rule added to root instructions.
