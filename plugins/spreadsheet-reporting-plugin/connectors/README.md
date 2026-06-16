# Spreadsheet Connector Contract

Replace this file with your spreadsheet loader, Google Sheets connector, warehouse export, or report writer.

## Required operations

- Load CSV, TSV, XLSX, or approved sheet export.
- Inspect workbook sheets, headers, formulas, dimensions, and data types.
- Produce report tables and safe evidence references.

## Optional operations

- Create a formatted workbook.
- Export charts.
- Push report summary to a dashboard or document.

## Telemetry

Emit `plugin.component.invoked` for parser, validator, chart, and export components. Do not emit cell values, workbook contents, sheet payloads, prompts, tool arguments, or model outputs.

