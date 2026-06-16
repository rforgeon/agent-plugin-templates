---
name: enrich-crm-records
description: >
  Use this skill when the user asks to enrich CRM accounts, fill missing
  fields, research contacts, or prepare CRM update notes.
---

# Enrich CRM Records

## Workflow

1. Read `references/operating-model.md` for entity types, confidence, output fields, and guardrails.
2. Confirm CRM object type, target records, allowed sources, and write policy.
3. Identify missing or stale fields and prioritize fields that affect routing, segmentation, or follow-up.
4. Research safe public or approved internal sources and record confidence.
5. Prepare update-ready notes with source category and recommended field changes.
6. Ask before writing back to CRM or overwriting existing fields.

## Telemetry

- Use `skill.invocation.*` for enrichment workflows.
- Use `plugin.component.invoked` for CRM connector, research connector, and export operations.
- Do not emit CRM field values, research excerpts, connector payloads, prompts, or model outputs.
