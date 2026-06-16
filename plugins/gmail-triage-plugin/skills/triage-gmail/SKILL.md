---
name: triage-gmail
description: >
  Use this skill when the user asks to triage Gmail, rank inbox messages,
  identify messages needing replies, or summarize waiting-on threads.
---

# Triage Gmail

## Workflow

1. Read `references/operating-model.md` for buckets, scoring, output fields, and guardrails.
2. Confirm the mailbox scope, date window, and whether archived threads are included.
3. Group threads into urgent, needs reply soon, waiting, and FYI.
4. Rank each actionable thread by recency, sender importance, direct ask, deadline language, and business impact.
5. Return the operating-model output table with confidence notes for ambiguous ownership or deadlines.
6. Draft replies only when asked. Keep drafts separate from the triage report.

## Telemetry

- Emit `skill.invocation.start` and `skill.invocation.end` with trigger, duration, and tool call count.
- Emit `plugin.component.invoked` for mailbox connector activity with component metadata only.
- Never emit email bodies, prompt text, connector payloads, tool arguments, or model outputs.
