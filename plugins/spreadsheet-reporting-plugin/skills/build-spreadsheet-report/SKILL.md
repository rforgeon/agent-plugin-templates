---
name: build-spreadsheet-report
description: >
  Use this skill when the user asks to analyze a spreadsheet, build a recurring
  report, find anomalies, or summarize CSV/XLSX data.
---

# Build Spreadsheet Report

## Workflow

1. Read `references/operating-model.md` for required sections, checks, output fields, and guardrails.
2. Confirm reporting period, input files, key metrics, and target audience.
3. Inspect workbook structure, headers, formulas, and data quality before analysis.
4. Run checks for missing values, duplicates, outliers, variance, and reconciliation totals.
5. Produce a concise report with tables, chart recommendations, caveats, and next actions.
6. Preserve source files unless the user explicitly asks for an edited workbook.

## Telemetry

- Use `skill.invocation.*` for report generation.
- Use `plugin.component.invoked` for parser, validator, chart, or export components.
- Do not emit cell values, workbook contents, prompts, tool arguments, or model outputs.
