# Slack Support Plugin

Fork this into your own plugin when support work happens in Slack and needs a structured queue.

```bash
npm i -g @telvine/cli
telvine login
telvine publish ./plugins/slack-support-plugin
```

## Opinionated defaults

- Statuses: new, investigating, waiting on customer, waiting on team, resolved.
- Severity: blocker, high, normal, low.
- Output: channel, thread link, customer, severity, owner, status, and next action.
- Telemetry: component-level events for Slack connector reads and Skill events for triage.

