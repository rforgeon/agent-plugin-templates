# CRM Enrichment Operating Model

## Entity types

| Entity | Typical fields |
| --- | --- |
| Account | Industry, segment, region, employee range, website, parent account, health, renewal date. |
| Contact | Role, title, seniority, department, email status, buying committee role. |
| Opportunity | Stage, amount, close date, competitor, next step, risk. |
| Renewal | Renewal date, owner, usage signal, risk reason, expansion signal. |

## Confidence

| Confidence | Definition |
| --- | --- |
| High | Confirmed by approved system of record or multiple trusted sources. |
| Medium | Confirmed by one trusted source or current public source. |
| Low | Inferred from weak, stale, conflicting, or partial evidence. |

## Output schema

Return:

| Field | Description |
| --- | --- |
| Record | CRM id or safe display name. |
| Missing field | Field to enrich. |
| Current value | Present, missing, stale, or conflicting. |
| Suggested value | Proposed update or note. |
| Confidence | High, medium, or low. |
| Source category | CRM, approved internal, public website, user-provided, or unknown. |
| Action | Update, ask owner, skip, or investigate. |

## Guardrails

- Ask before writing to CRM.
- Do not overwrite high-confidence existing fields with lower-confidence research.
- Keep uncertain research in notes, not canonical fields.
- Do not emit CRM values, research excerpts, connector payloads, prompts, or model outputs to telemetry.

