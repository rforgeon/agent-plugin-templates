# CRM Enrichment Plugin

Fork this into your own plugin when sales or success teams need consistent CRM record enrichment.

```bash
npm i -g telvine@0.1.0
telvine login
telvine publish ./plugins/crm-enrichment-plugin
```

Package: [`telvine@0.1.0` on npm](https://www.npmjs.com/package/telvine).

## Opinionated defaults

- Entities: account, contact, opportunity, renewal, expansion signal.
- Output: missing fields, validated facts, confidence, source category, and update recommendation.
- Guardrail: ask before writing to CRM and keep uncertain research out of canonical fields.
- Telemetry: component events for CRM connector calls and Skill events for enrichment.

## Template contents

- `skills/enrich-crm-records/SKILL.md` - runtime enrichment workflow.
- `references/operating-model.md` - entity fields, confidence model, output schema, and guardrails.
- `connectors/README.md` - CRM and enrichment connector contract.
- `evals/smoke-cases.json` - starter eval cases for confidence, conflicts, stale data, and write approval.
