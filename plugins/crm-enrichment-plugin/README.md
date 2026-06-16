# CRM Enrichment Plugin

Fork this into your own plugin when sales or success teams need consistent CRM record enrichment.

```bash
npm i -g @telvine/cli
telvine login
telvine publish ./plugins/crm-enrichment-plugin
```

## Opinionated defaults

- Entities: account, contact, opportunity, renewal, expansion signal.
- Output: missing fields, validated facts, confidence, source category, and update recommendation.
- Guardrail: ask before writing to CRM and keep uncertain research out of canonical fields.
- Telemetry: component events for CRM connector calls and Skill events for enrichment.

