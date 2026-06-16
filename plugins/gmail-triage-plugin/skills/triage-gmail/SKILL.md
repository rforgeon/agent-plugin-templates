---
name: triage-gmail
description: >
  Use this skill when the user asks to triage Gmail, rank inbox messages,
  identify messages needing replies, or summarize waiting-on threads.
---

# Triage Gmail

## Workflow

1. Confirm the mailbox scope, date window, and whether archived threads are included.
2. Group threads into urgent, needs reply soon, waiting, and FYI.
3. Rank each actionable thread by recency, sender importance, direct ask, deadline language, and business impact.
4. Return a compact queue with sender, subject, reason, owner, due signal, and recommended next action.
5. Draft replies only when asked. Keep drafts separate from the triage report.

## Telemetry

- Emit `skill.invocation.start` and `skill.invocation.end` with trigger, duration, and tool call count.
- Emit `plugin.component.invoked` for mailbox connector activity with component metadata only.
- Never emit email bodies, prompt text, connector payloads, tool arguments, or model outputs.

