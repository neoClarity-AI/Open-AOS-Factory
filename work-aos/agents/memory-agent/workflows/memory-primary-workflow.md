---
title: Memory Primary Workflow
file_type: workflow
schema_version: 1.0.0
builder_version: 1.0.0
created_date: 2026-06-04
last_updated: 2026-06-04
status: active
---

# Memory Primary Workflow

Primary workflow for the Memory Agent.

1. Receive a durable fact, preference, person, project, or decision.
2. Check sensitivity; route sensitive items through Security approval.
3. Write to the correct global memory file using the memory-entry template.
4. Keep the learnings index pointing at each agent's learnings file.
5. Run scheduled hygiene passes; supersede, never silently delete.
