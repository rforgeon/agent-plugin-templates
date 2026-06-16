# Internal Ops Operating Model

## Operating states

| State | Definition |
| --- | --- |
| Blocked | Work cannot proceed without a specific person, approval, access, or dependency. |
| At risk | Work can proceed but deadline, quality, customer, or compliance risk is elevated. |
| Waiting | Next action belongs to another team or external party. |
| On track | Owner and next action are clear and SLA is not at risk. |
| Resolved | Closure evidence exists and no follow-up remains. |

## Prioritization

Prioritize by:

1. Customer or revenue impact.
2. Compliance, finance, security, or legal impact.
3. SLA breach or due date.
4. Number of blocked downstream items.
5. Executive or incident visibility.

## Output schema

Return a handoff with:

| Field | Description |
| --- | --- |
| Priority | Ordered rank. |
| Item | Exception, task, process, or queue. |
| State | Blocked, at risk, waiting, on track, or resolved. |
| Owner | Person or team responsible. |
| Due | Due date, SLA, or review cadence. |
| Impact | Customer, revenue, compliance, operational, or internal. |
| Blocker | Specific blocker or dependency. |
| Next action | Concrete action and owner. |

## Guardrails

- Do not invent owners when source evidence is absent.
- Separate facts from inferred recommendations.
- Mark stale items when owner update is older than cadence.
- Do not emit internal records, connector payloads, prompts, or model outputs to telemetry.

