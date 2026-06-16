# Gmail Triage Operating Model

## Buckets

| Bucket | Definition | Default SLA |
| --- | --- | --- |
| Urgent | Direct ask with deadline, executive/customer escalation, security, finance, or legal impact. | Same business day |
| Needs reply soon | User is the expected responder and no blocker remains. | 2 business days |
| Waiting | User already replied or the next action belongs to someone else. | Review at next cadence |
| FYI | Informational, newsletter, receipt, automated notice, or no action required. | None |

## Scoring

Score each thread from 0-100:

- 30 points for direct request to the user or their team.
- 25 points for explicit deadline or time-sensitive language.
- 20 points for customer, leadership, legal, finance, or security sender.
- 15 points for overdue age relative to SLA.
- 10 points for business impact keywords.

## Output schema

Return a Markdown table with:

| Field | Description |
| --- | --- |
| Rank | 1-based priority. |
| Bucket | Urgent, needs reply soon, waiting, or FYI. |
| Sender | Sender display name or safe domain. |
| Subject | Subject line or short safe summary. |
| Why | Metadata-based reason for classification. |
| Owner | Person expected to act. |
| Due signal | Deadline text if safe to display, otherwise inferred urgency. |
| Next action | Reply, delegate, wait, archive, schedule, or review. |

## Guardrails

- Never auto-send email.
- Keep drafts separate from triage.
- Mark low confidence when sender identity, deadline, or ownership is ambiguous.
- Do not send message bodies, connector payloads, prompts, or model outputs to telemetry.

