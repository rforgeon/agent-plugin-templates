# Spreadsheet Reporting Plugin

Fork this into your own plugin when spreadsheet work needs a repeatable report instead of ad hoc analysis.

```bash
npm i -g @telvine/cli
telvine login
telvine publish ./plugins/spreadsheet-reporting-plugin
```

## Opinionated defaults

- Inputs: CSV, TSV, XLSX, or exported Google Sheets files.
- Checks: missing values, duplicates, outliers, variance, and reconciliation totals.
- Output: report table, chart suggestions, executive summary, and data quality notes.
- Telemetry: `skill.invocation.*` plus component events for parser and report export steps.

## Template contents

- `skills/build-spreadsheet-report/SKILL.md` - runtime reporting workflow.
- `references/operating-model.md` - report sections, checks, output schema, and guardrails.
- `connectors/README.md` - spreadsheet parser and export contract.
- `evals/smoke-cases.json` - starter eval cases for schema, variance, duplicates, and reconciliation.
