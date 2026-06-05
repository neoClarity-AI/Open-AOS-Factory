---
title: Chief of Staff Agent — Config
file_type: config
schema_version: 1.0.0
builder_version: 1.0.0
created_date: 2026-06-04
last_updated: 2026-06-04
status: active
---

# Chief of Staff Agent — Config

## Inherited Rules
References `/configs/global-permissions.md`. This agent does not duplicate or override global rules.

## Tool Access
References `/configs/tool-access-matrix.md` (authoritative). Agent-specific note: References global permissions and the tool access matrix.

## Memory Access
Reads global memory as needed; writes durable facts via the Memory Agent. Owns its folder's `memory/` files.

## Escalation
Permission/privacy -> Security Agent. Cross-agent routing/priority -> Chief of Staff Agent.
