---
name: review-ops-exceptions
description: >
  Use this skill when the user asks for an internal operations review,
  exception queue, handoff summary, or blocked-work report.
---

# Review Ops Exceptions

## Workflow

1. Read `references/operating-model.md` for states, prioritization, output fields, and guardrails.
2. Confirm operating area, sources, date window, and escalation rules.
3. Gather open items and classify each as blocked, at risk, waiting, on track, or resolved.
4. Identify owner, due date, impact, blocker reason, and recommended next action.
5. Produce a handoff summary optimized for scanability and accountability.
6. Separate source facts from inferred recommendations.

## Telemetry

- Use `skill.invocation.*` for the exception review Skill.
- Use `plugin.component.invoked` for source system reads and handoff export.
- Do not emit internal records, connector payloads, prompts, tool arguments, or model outputs.
