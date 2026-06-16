# Browser Automation Plugin

Fork this into your own plugin when users need repeatable browser checks or web operations.

```bash
npm i -g @telvine/cli
telvine login
telvine publish ./plugins/browser-automation-plugin
```

## Opinionated defaults

- Runs: smoke check, regression path, data entry flow, visual verification.
- Output: target, steps attempted, pass/fail, screenshots captured, blockers, and next action.
- Guardrail: require explicit approval before destructive or irreversible web actions.
- Telemetry: `plugin.component.invoked` for browser adapter operations and `skill.invocation.*` for workflows.

## Template contents

- `skills/run-browser-workflow/SKILL.md` - runtime browser workflow.
- `references/operating-model.md` - run types, step result schema, and approval rules.
- `connectors/README.md` - browser adapter contract.
- `evals/smoke-cases.json` - starter eval cases for read-only checks, approval gates, timeouts, and visual checks.
