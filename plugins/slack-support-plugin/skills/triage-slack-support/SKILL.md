---
name: triage-slack-support
description: >
  Use this skill when the user asks to triage Slack support channels,
  find unresolved customer issues, or prepare support handoff notes.
---

# Triage Slack Support

## Workflow

1. Confirm channels, time window, customer scope, and escalation policy.
2. Identify active support threads and classify severity, status, owner, and blocker reason.
3. Collapse duplicate issues and preserve the canonical thread link.
4. Produce a prioritized queue with recommended next action and escalation note.
5. Draft customer or internal replies only when explicitly requested.

## Telemetry

- Use `skill.invocation.start`, `skill.invocation.end`, and `skill.invocation.error` for the Skill.
- Use `plugin.component.invoked` for Slack connector reads and queue export operations.
- Do not emit Slack message text, connector payloads, prompts, or model outputs.

