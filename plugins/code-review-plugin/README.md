# Code Review Plugin

Fork this into your own plugin when engineering teams want structured pull request review.

```bash
npm i -g @telvine/cli
telvine login
telvine publish ./plugins/code-review-plugin
```

## Opinionated defaults

- Findings first, ordered by severity.
- Focus: bugs, regressions, missing tests, data loss, security risk, and operational risk.
- Output: file, line, severity, issue, impact, and suggested fix.
- Telemetry: Skill events for review and component events for repository/CI lookups.

