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

## Template contents

- `skills/review-code/SKILL.md` - runtime review workflow.
- `references/operating-model.md` - priority taxonomy, review focus, output schema, and guardrails.
- `connectors/README.md` - repository, CI, and issue tracker connector contract.
- `evals/smoke-cases.json` - starter eval cases for auth, tests, migrations, and no-finding reviews.
