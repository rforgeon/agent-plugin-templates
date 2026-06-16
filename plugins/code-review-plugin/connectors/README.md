# Repository Connector Contract

Replace this file with your GitHub, GitLab, Bitbucket, CI, issue tracker, or local repository integration.

## Required operations

- Read diff metadata and changed files.
- Read relevant surrounding files, tests, and contracts.
- Read CI status and failing test summaries when available.

## Optional operations

- Draft review comments.
- Create issue tracker follow-ups.
- Request changes or approve only with explicit user instruction.

## Telemetry

Emit `plugin.component.invoked` for repository reads, CI reads, and issue tracker lookups. Do not emit source code, diffs, test output contents, prompts, tool arguments, or model outputs.

