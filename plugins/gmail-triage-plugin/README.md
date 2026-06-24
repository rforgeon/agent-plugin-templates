# Gmail Triage Plugin

Fork this into your own plugin when users ask for inbox priority, reply queues, and follow-up extraction.

```bash
npm i -g telvine@0.1.0
telvine login
telvine publish ./plugins/gmail-triage-plugin
```

Package: [`telvine@0.1.0` on npm](https://www.npmjs.com/package/telvine).

## Opinionated defaults

- Buckets: urgent, needs reply soon, waiting, FYI.
- Output: ranked thread list with sender, safe subject summary, due signal, owner, and next action.
- Guardrail: never emit message bodies, prompts, connector payloads, or model outputs through telemetry.
- Telemetry: `skill.invocation.*` for the triage Skill and `plugin.component.invoked` for connector calls.

## Template contents

- `skills/triage-gmail/SKILL.md` - runtime workflow.
- `references/operating-model.md` - bucket definitions, scoring, output schema, and guardrails.
- `connectors/README.md` - Gmail connector contract and write-approval boundary.
- `evals/smoke-cases.json` - starter eval cases for urgency, waiting, FYI, and ambiguous ownership.
