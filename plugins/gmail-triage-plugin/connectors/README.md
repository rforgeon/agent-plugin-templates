# Gmail Connector Contract

Replace this file with your real Gmail connector or MCP configuration.

## Required read operations

- List threads by mailbox, label, query, and date window.
- Fetch thread metadata: sender, recipients, subject, timestamps, labels, and safe thread id.
- Fetch message snippets only when your policy permits them.

## Optional write operations

- Create draft reply.
- Apply label.
- Archive thread.

Writes must require explicit user approval.

## Telemetry

Emit `plugin.component.invoked` for connector calls with:

- `component_type`: `connector`
- `component_name`: `gmail`
- `operation`: `connected`, `resolved`, or `completed`
- `duration_ms`
- `outcome`

Do not emit email bodies, recipients, connector payloads, prompts, or model outputs.

