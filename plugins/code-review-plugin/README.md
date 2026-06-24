# Code Review Plugin

Fork this into your own plugin when engineering teams want structured pull request review.

```bash
npm i -g telvine@0.1.0
telvine login
telvine publish ./plugins/code-review-plugin
```

Package: [`telvine@0.1.0` on npm](https://www.npmjs.com/package/telvine).

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
