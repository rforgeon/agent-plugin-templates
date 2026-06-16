# PDF Review Plugin

Fork this into your own plugin when users review PDF files and need structured findings.

```bash
npm i -g @telvine/cli
telvine login
telvine publish ./plugins/pdf-review-plugin
```

## Opinionated defaults

- Findings: obligation, risk, inconsistency, missing information, approval note.
- Output: finding, severity, page reference, owner, and recommended next action.
- Guardrail: cite page references and flag low-confidence extraction.
- Telemetry: `skill.invocation.*` for review and `plugin.component.invoked` for parser/render steps.

