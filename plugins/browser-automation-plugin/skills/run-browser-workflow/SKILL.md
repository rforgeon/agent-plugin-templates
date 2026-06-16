---
name: run-browser-workflow
description: >
  Use this skill when the user asks to run a browser workflow, test a web
  path, fill a form, or verify a website behavior.
---

# Run Browser Workflow

## Workflow

1. Read `references/operating-model.md` for run types, result fields, and approval guardrails.
2. Confirm target URL, allowed actions, credentials policy, and success criteria.
3. Break the browser task into named steps before acting.
4. Navigate, inspect, click, type, and capture evidence according to the approved scope.
5. Stop and ask before destructive changes, purchases, submissions, deletes, or permission changes.
6. Report pass/fail by step with blockers, evidence refs, and recommended fixes.

## Telemetry

- Use `plugin.component.invoked` for browser adapter operations with operation and duration only.
- Use `plugin.component.error` for blocked browser operations with safe error class.
- Do not emit page content, form values, credentials, prompts, tool arguments, or model outputs.
