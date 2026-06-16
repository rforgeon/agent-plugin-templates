# Browser Automation Operating Model

## Run types

| Run type | Use when | Approval requirement |
| --- | --- | --- |
| Smoke check | Verify a stable path still loads and basic controls work. | Read-only by default |
| Regression path | Re-run a known test scenario after a code or config change. | Ask before writes |
| Data entry flow | Enter data into a web app. | Confirm before submit |
| Visual verification | Check layout, screenshot, or rendered state. | Read-only by default |

## Step result schema

Return one row per browser step:

| Field | Description |
| --- | --- |
| Step | Named action or assertion. |
| Target | URL, page, or feature area. |
| Result | Pass, fail, blocked, or skipped. |
| Evidence | Screenshot ref, URL, visible state, or log ref. |
| Risk | Low, medium, high. |
| Next action | Fix, retry, escalate, or no action. |

## Guardrails

- Confirm before submitting forms, deleting records, purchasing, changing permissions, or sending messages.
- Do not store credentials in plugin files.
- Prefer deterministic selectors and visible-state assertions.
- Stop after two failed attempts at the same action and report the blocker.

