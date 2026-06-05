---
title: AOS Map
file_type: aos_map
schema_version: 1.0.0
builder_version: 1.0.0
created_date: 2026-06-04
last_updated: 2026-06-04
status: active
---

# AOS Map

A live picture of the agents in this AOS and their state.

## Required core (governance) — installed
- **Security / Permissions Agent** — `installed`, active
- **Memory Agent** — `installed`, active
- **Chief of Staff Agent** — `installed`, active
- **Review / Reflection Agent** — `installed`, active

## Optional productive — installed
- **Inbox / Communications Agent** — `installed`, active
- **Calendar / Scheduling Agent** — `installed`, active
- **Task / Commitment Agent** — `installed`, active
- **Project Manager Agent** — `installed`, active
- **Research Agent** — `installed`, active

## Optional productive — available, not installed
- **Automation Agent** — `available` (builder: /builders/build-automation-agent.md)
- **Document Librarian Agent** — `available` (builder: /builders/build-document-librarian-agent.md)
- **Finance Agent** — `available` (builder: /builders/build-finance-agent.md)
- **Health & Life Logistics Agent** — `available` (builder: /builders/build-health-life-logistics-agent.md)
- **Learning Agent** — `available` (builder: /builders/build-learning-agent.md)
- **Personal CRM Agent** — `available` (builder: /builders/build-personal-crm-agent.md)
- **Writing / Content Agent** — `available` (builder: /builders/build-writing-agent.md)

## Paused / retired
- None.

## How to add an agent
Run the matching `/builders/build-[agent-name]-agent.md`. The build updates this map and `/configs/agent-registry.md`.
