# PDF Review Operating Model

## Finding types

| Type | Definition |
| --- | --- |
| Obligation | A required action, payment, deadline, approval, notice, or compliance step. |
| Risk | Ambiguous, unfavorable, missing, inconsistent, or high-impact language. |
| Inconsistency | Conflict between sections, exhibits, amounts, names, or dates. |
| Missing information | Required field, signature, appendix, exhibit, or data point absent. |
| Approval note | Item a reviewer should approve, reject, or escalate. |

## Severity

- High: financial, legal, security, customer, or deadline impact.
- Medium: operational impact or material ambiguity.
- Low: formatting, minor inconsistency, or informational note.

## Output schema

Return a table with:

| Field | Description |
| --- | --- |
| Finding | Concise issue or obligation. |
| Type | Obligation, risk, inconsistency, missing information, or approval note. |
| Severity | High, medium, or low. |
| Page | Page number or range. |
| Evidence | Short paraphrase, not long copied text. |
| Owner | Legal, finance, ops, customer, vendor, or unknown. |
| Recommendation | Approve, revise, reject, escalate, or request information. |

## Guardrails

- Cite page references for every material finding.
- Do not provide legal advice; frame legal items as review flags.
- Mark OCR/table extraction uncertainty.
- Do not emit document contents or extracted text to telemetry.

