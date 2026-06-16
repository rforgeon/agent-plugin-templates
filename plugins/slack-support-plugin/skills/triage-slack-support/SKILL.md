---
name: triage-slack-support
description: >
  Use this skill when the user asks to triage Slack support channels,
  find unresolved customer issues, or prepare support handoff notes.
---

# Triage Slack Support

## Workflow

1. Read `references/operating-model.md` for severity, status, output fields, and guardrails.
2. Confirm channels, time window, customer scope, and escalation policy.
3. Identify active support threads and classify severity, status, owner, and blocker reason.
4. Collapse duplicate issues and preserve the canonical thread link.
5. Produce the operating-model queue with recommended next action and escalation note.
6. Draft customer or internal replies only when explicitly requested.

## Telemetry

- Use `skill.invocation.start`, `skill.invocation.end`, and `skill.invocation.error` for the Skill.
- Use `plugin.component.invoked` for Slack connector reads and queue export operations.
- Do not emit Slack message text, connector payloads, prompts, or model outputs.
