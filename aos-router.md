---
title: AOS Instance Router
file_type: aos_router
schema_version: 1.0.0
builder_version: 1.0.0
created_date: 2026-06-05
last_updated: 2026-06-05
status: active
applies_to:
  - work-aos
  - personal-aos
---

# AOS Instance Router

Read this BEFORE loading any instance. AOS-03 contains two instances
(`work-aos`, `personal-aos`). Exactly one is active per request. This file
decides which, and is owned jointly by the two Chief of Staff agents.

## 1. Resolution order (stop at the first that applies)
1. **Explicit user override** — the user names an instance ("in work-aos…",
   "personal brief"). Use it.
2. **Session pin** — if the user has set an active instance this session
   (see §4), use it until they change or clear it.
3. **Signal match** — classify from the request signals in §2. Use a side
   only if it wins by the confidence bar in §3.
4. **Fallback: ASK.** If none of the above resolves it, ask the user which
   instance to use. Do NOT silently pick, and do NOT merge the two.

## 2. Classification signals
- **Default instance:** `work-aos`.
- **Work signals:** requests mentioning clients, the company, billing,
  hiring, work projects in `work-aos/projects`, or recipients/aliases tied
  to work.
- **Personal signals:** family/friends (e.g. dan@danner.org threads),
  personal admin, community/newsletter aliases (m25@, m26+*, martin+*),
  personal projects in `personal-aos/projects`.
- **Shared inbox note:** martin@neoclarity.ai feeds BOTH instances, so inbox
  alone is not a routing signal. Route on sender/alias and request intent,
  not on the fact that mail exists.

## 3. Confidence bar
- Act automatically only when one side has clear signals AND the other has
  none. Mixed or weak signals → fall through to §1.4 (ASK).
- Cross-instance requests ("brief me on everything") → run each instance
  separately and label the output by instance; never blend their memory.

## 4. Session pin
- "Use work-aos for now" or "switch to personal" sets the pin for the session.
- "Clear AOS" or "ask me each time" removes the pin.
- State the active instance in the first line of any brief or routed output
  (e.g. "**[work-aos]** Daily Brief — …").

## 5. Logging
- Record each non-trivial routing choice (chosen instance, trigger, default
  vs. asked) to the active instance's
  `agents/chief-of-staff-agent/logs/chief-of-staff-decision-log.md`.
