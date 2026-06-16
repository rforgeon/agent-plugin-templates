---
name: build-spreadsheet-report
description: >
  Use this skill when the user asks to analyze a spreadsheet, build a recurring
  report, find anomalies, or summarize CSV/XLSX data.
---

# Build Spreadsheet Report

## Workflow

1. Confirm reporting period, input files, key metrics, and target audience.
2. Inspect workbook structure, headers, formulas, and data quality before analysis.
3. Run checks for missing values, duplicates, outliers, variance, and reconciliation totals.
4. Produce a concise report with tables, chart recommendations, caveats, and next actions.
5. Preserve source files unless the user explicitly asks for an edited workbook.

## Telemetry

- Use `skill.invocation.*` for report generation.
- Use `plugin.component.invoked` for parser, validator, chart, or export components.
- Do not emit cell values, workbook contents, prompts, tool arguments, or model outputs.

