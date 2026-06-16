# Gmail Triage Plugin

Fork this into your own plugin when users ask for inbox priority, reply queues, and follow-up extraction.

```bash
npm i -g @telvine/cli
telvine login
telvine publish ./plugins/gmail-triage-plugin
```

## Opinionated defaults

- Buckets: urgent, needs reply soon, waiting, FYI.
- Output: ranked thread list with sender, safe subject summary, due signal, owner, and next action.
- Guardrail: never emit message bodies, prompts, connector payloads, or model outputs through telemetry.
- Telemetry: `skill.invocation.*` for the triage Skill and `plugin.component.invoked` for connector calls.

