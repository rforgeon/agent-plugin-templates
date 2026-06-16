---
name: review-code
description: >
  Use this skill when the user asks for a code review, pull request review,
  bug hunt, regression check, or release risk summary.
---

# Review Code

## Workflow

1. Inspect the diff, related tests, touched contracts, and relevant runtime paths.
2. Prioritize correctness, regressions, data loss, security, operational risk, and missing tests.
3. Report findings first, ordered by severity, with tight file and line references.
4. Keep summaries secondary to actionable issues.
5. State residual risk and test gaps when no blocking findings are found.

## Telemetry

- Use `skill.invocation.*` for review runs.
- Use `plugin.component.invoked` for repository, CI, or issue tracker lookups.
- Do not emit source code, patch contents, prompts, tool arguments, or model outputs.

