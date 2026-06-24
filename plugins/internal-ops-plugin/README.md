# Internal Ops Plugin

Fork this into your own plugin when internal teams need repeatable exception reviews and handoffs.

```bash
npm i -g telvine@0.1.0
telvine login
telvine publish ./plugins/internal-ops-plugin
```

Package: [`telvine@0.1.0` on npm](https://www.npmjs.com/package/telvine).

## Opinionated defaults

- Buckets: blocked, at risk, waiting, on track, resolved.
- Output: exception, owner, due date, impact, blocker, next action, and escalation recommendation.
- Guardrail: distinguish observed facts from recommendations.
- Telemetry: Skill events for review flow and component events for source system lookups.

## Template contents

- `skills/review-ops-exceptions/SKILL.md` - runtime exception review workflow.
- `references/operating-model.md` - states, prioritization, output schema, and guardrails.
- `connectors/README.md` - task, queue, incident, or warehouse connector contract.
- `evals/smoke-cases.json` - starter eval cases for blocked, at-risk, waiting, and resolved items.
