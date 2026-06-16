# Spreadsheet Reporting Operating Model

## Report sections

1. Executive summary.
2. Metric table.
3. Variance and anomaly notes.
4. Data quality findings.
5. Recommended next actions.

## Checks

| Check | Purpose |
| --- | --- |
| Schema | Confirm required columns, tabs, and types exist. |
| Completeness | Identify missing values in required fields. |
| Duplicate | Detect duplicate ids, invoices, customers, or periods. |
| Reconciliation | Compare totals to expected control totals. |
| Variance | Compare current period to baseline, forecast, or prior period. |
| Outlier | Flag values outside expected range or distribution. |

## Output schema

Return:

- `summary`: 3-5 bullets for decision makers.
- `metrics`: table of key figures, period, baseline, delta, and delta percent.
- `exceptions`: table of issue, row/sheet reference, severity, and owner.
- `chart_recommendations`: chart type, metric, and reason.
- `data_quality`: completeness, duplicates, formula, and schema notes.

## Guardrails

- Never overwrite source workbooks unless explicitly requested.
- Preserve formulas when creating edited workbooks.
- Mark inferred column mappings.
- Do not emit cell values, workbook contents, prompts, or model outputs to telemetry.

