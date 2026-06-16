# Browser Adapter Contract

Replace this file with your browser runtime, Playwright wrapper, MCP server, or harness adapter.

## Required operations

- Navigate to a URL.
- Read visible page state.
- Click, type, select, and press keys within approved scope.
- Capture screenshot or evidence reference.

## Approval-gated operations

- Submit forms.
- Upload files.
- Change permissions.
- Delete, purchase, publish, or send.

## Telemetry

Emit `plugin.component.invoked` for browser adapter operations with operation, duration, and outcome. Emit `plugin.component.error` for blocked, timed out, or permission-denied operations. Do not emit page content, form values, credentials, prompts, tool arguments, or model outputs.

