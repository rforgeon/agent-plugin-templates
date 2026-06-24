# Agent Plugin Templates

Fork this repo into your own plugin. Each starter is intentionally narrow, opinionated, and ready to publish with Telvine. These are not empty example manifests: every template includes a Skill, domain operating model, connector contract, smoke evals, and metadata-only telemetry guidance.

```bash
npm i -g telvine@0.1.0
telvine login
telvine publish ./plugins/gmail-triage-plugin
```

Package: [`telvine@0.1.0` on npm](https://www.npmjs.com/package/telvine).

## Templates

| Template | Use it when | Fork path |
| --- | --- | --- |
| Gmail triage plugin | Teams need inbox prioritization, reply queues, and follow-up extraction. | `plugins/gmail-triage-plugin` |
| Slack support plugin | Support teams triage channel threads into owner, status, and next action. | `plugins/slack-support-plugin` |
| Browser automation plugin | Operators need repeatable website checks, form flows, or QA runs. | `plugins/browser-automation-plugin` |
| PDF review plugin | Reviewers extract obligations, issues, and approval notes from PDFs. | `plugins/pdf-review-plugin` |
| Spreadsheet reporting plugin | Analysts turn CSV/XLSX inputs into repeatable management reports. | `plugins/spreadsheet-reporting-plugin` |
| Internal ops plugin | Ops teams run daily exception reviews and handoff summaries. | `plugins/internal-ops-plugin` |
| CRM enrichment plugin | Revenue teams enrich account records and flag missing data. | `plugins/crm-enrichment-plugin` |
| Code review plugin | Engineering teams run structured pull request review and risk checks. | `plugins/code-review-plugin` |

## How to fork a template

1. Fork this repository.
2. Copy one folder from `plugins/` into your plugin workspace.
3. Update `.codex-plugin/plugin.json` with your plugin name, repository, prompts, and publisher.
4. Edit `skills/*/SKILL.md` for your runtime behavior.
5. Edit `references/operating-model.md` for your domain taxonomy, prioritization rules, output fields, and guardrails.
6. Wire your real source systems using `connectors/README.md`.
7. Run or adapt the smoke cases in `evals/smoke-cases.json`.
8. Keep telemetry metadata-only: send event types, ids, durations, statuses, and safe enums. Do not send prompts, file contents, connector payloads, tool arguments, or model outputs.
9. Publish with Telvine:

```bash
npm i -g telvine@0.1.0
telvine login
telvine publish ./my-plugin
```

## Telemetry contract

Use `skill.invocation.start`, `skill.invocation.end`, and `skill.invocation.error` for `SKILL.md` capabilities. Use `plugin.component.invoked` and `plugin.component.error` for non-Skill components such as connectors, tools, browser adapters, MCP config, or scripts.

The examples in this repo intentionally describe telemetry without collecting user content.

## Folder contract

Every plugin starter follows this shape:

```text
plugin-name/
├── .codex-plugin/plugin.json
├── README.md
├── connectors/README.md
├── evals/smoke-cases.json
├── references/operating-model.md
└── skills/<capability>/SKILL.md
```

The `SKILL.md` is what the agent loads at runtime. The operating model gives the Skill durable rules. The connector notes define integration boundaries. The smoke evals give Telvine and your CI a starting quality gate before you publish.
