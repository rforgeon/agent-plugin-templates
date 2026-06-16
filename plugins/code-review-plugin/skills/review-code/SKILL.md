---
name: review-code
description: >
  Use this skill when the user asks for a code review, pull request review,
  bug hunt, regression check, or release risk summary.
---

# Review Code

## Workflow

1. Read `references/operating-model.md` for finding priorities, review focus, output fields, and guardrails.
2. Inspect the diff, related tests, touched contracts, and relevant runtime paths.
3. Prioritize correctness, regressions, data loss, security, operational risk, and missing tests.
4. Report findings first, ordered by severity, with tight file and line references.
5. Keep summaries secondary to actionable issues.
6. State residual risk and test gaps when no blocking findings are found.

## Telemetry

- Use `skill.invocation.*` for review runs.
- Use `plugin.component.invoked` for repository, CI, or issue tracker lookups.
- Do not emit source code, patch contents, prompts, tool arguments, or model outputs.
