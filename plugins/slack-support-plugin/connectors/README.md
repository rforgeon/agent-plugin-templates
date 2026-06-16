# Slack Connector Contract

Replace this file with your Slack connector, bot token integration, or MCP server.

## Required read operations

- List channels configured for support.
- Search messages by channel, customer, status emoji, date window, or thread activity.
- Fetch thread metadata and permalink.

## Optional write operations

- Draft reply.
- Add reaction/status marker.
- Create escalation ticket.

Writes must require explicit user approval.

## Telemetry

Emit `plugin.component.invoked` for Slack connector reads and exports. Use `plugin.component.error` for permission or channel access failures. Never emit Slack message bodies, connector payloads, prompts, or model outputs.

