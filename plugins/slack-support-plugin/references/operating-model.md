# Slack Support Operating Model

## Statuses

| Status | Definition |
| --- | --- |
| New | Customer issue has no owner or first response. |
| Investigating | Owner is assigned and actively diagnosing. |
| Waiting on customer | Customer must provide information or confirmation. |
| Waiting on team | Internal team owns the next action. |
| Resolved | Customer confirmed resolution or support team closed with evidence. |

## Severity

| Severity | Definition |
| --- | --- |
| Blocker | Production outage, payment failure, security issue, or all users blocked. |
| High | Major workflow degraded, customer deadline at risk, or executive escalation. |
| Normal | Standard support issue with workaround or limited impact. |
| Low | Question, cosmetic issue, or non-urgent request. |

## Output schema

Return a Markdown table with:

| Field | Description |
| --- | --- |
| Priority | Ordered issue rank. |
| Customer | Customer or account identifier safe to display. |
| Channel/thread | Link or stable thread reference. |
| Severity | Blocker, high, normal, or low. |
| Status | One of the statuses above. |
| Owner | Individual or team responsible for next action. |
| Blocker | What prevents closure. |
| Next action | Concrete support, engineering, or customer action. |

## Guardrails

- Do not post to Slack unless the user explicitly asks.
- Do not summarize private channel content into public channels.
- Preserve thread links for auditability.
- Mark stale threads when no owner update appears within SLA.

