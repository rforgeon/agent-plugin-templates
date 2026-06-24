# PDF Review Plugin

Fork this into your own plugin when users review PDF files and need structured findings.

```bash
npm i -g telvine@0.1.0
telvine login
telvine publish ./plugins/pdf-review-plugin
```

Package: [`telvine@0.1.0` on npm](https://www.npmjs.com/package/telvine).

## Opinionated defaults

- Findings: obligation, risk, inconsistency, missing information, approval note.
- Output: finding, severity, page reference, owner, and recommended next action.
- Guardrail: cite page references and flag low-confidence extraction.
- Telemetry: `skill.invocation.*` for review and `plugin.component.invoked` for parser/render steps.

## Template contents

- `skills/review-pdf/SKILL.md` - runtime PDF review workflow.
- `references/operating-model.md` - finding taxonomy, severity, output schema, and guardrails.
- `connectors/README.md` - parser, renderer, OCR, and export contract.
- `evals/smoke-cases.json` - starter eval cases for signatures, date conflicts, obligations, and OCR uncertainty.
