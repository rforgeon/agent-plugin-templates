# Code Review Operating Model

## Finding priorities

| Priority | Definition |
| --- | --- |
| P0 | Data loss, security break, outage, or severe production regression likely. |
| P1 | Correctness bug, broken workflow, migration risk, or missing guardrail. |
| P2 | Edge case, test gap, maintainability issue with plausible user impact. |
| P3 | Style, clarity, or cleanup that does not block merge. |

## Review focus

1. Behavioral regressions.
2. Data integrity and persistence.
3. Security and authorization.
4. Error handling and retries.
5. Contract/API compatibility.
6. Tests for changed behavior.
7. Operational visibility and rollback.

## Output schema

Lead with findings:

| Field | Description |
| --- | --- |
| Priority | P0-P3. |
| File/line | Tight reference to changed code. |
| Issue | What is wrong. |
| Impact | User, data, security, or operational consequence. |
| Fix | Concrete suggested correction. |

Then include:

- Open questions.
- Test gaps.
- Short change summary only after findings.

## Guardrails

- Do not invent findings without code evidence.
- Do not bury real issues under praise.
- If no findings, state that clearly and list residual risk.
- Do not emit source code, patches, prompts, or model outputs to telemetry.

