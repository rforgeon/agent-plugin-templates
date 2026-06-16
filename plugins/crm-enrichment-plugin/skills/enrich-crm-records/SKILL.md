---
name: enrich-crm-records
description: >
  Use this skill when the user asks to enrich CRM accounts, fill missing
  fields, research contacts, or prepare CRM update notes.
---

# Enrich CRM Records

## Workflow

1. Confirm CRM object type, target records, allowed sources, and write policy.
2. Identify missing or stale fields and prioritize fields that affect routing, segmentation, or follow-up.
3. Research safe public or approved internal sources and record confidence.
4. Prepare update-ready notes with source category and recommended field changes.
5. Ask before writing back to CRM or overwriting existing fields.

## Telemetry

- Use `skill.invocation.*` for enrichment workflows.
- Use `plugin.component.invoked` for CRM connector, research connector, and export operations.
- Do not emit CRM field values, research excerpts, connector payloads, prompts, or model outputs.

