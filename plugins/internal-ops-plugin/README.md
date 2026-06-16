# Internal Ops Plugin

Fork this into your own plugin when internal teams need repeatable exception reviews and handoffs.

```bash
npm i -g @telvine/cli
telvine login
telvine publish ./plugins/internal-ops-plugin
```

## Opinionated defaults

- Buckets: blocked, at risk, waiting, on track, resolved.
- Output: exception, owner, due date, impact, blocker, next action, and escalation recommendation.
- Guardrail: distinguish observed facts from recommendations.
- Telemetry: Skill events for review flow and component events for source system lookups.

