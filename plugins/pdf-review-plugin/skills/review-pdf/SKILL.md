---
name: review-pdf
description: >
  Use this skill when the user asks to review a PDF, extract obligations,
  summarize a document with page references, or prepare approval notes.
---

# Review PDF

## Workflow

1. Read `references/operating-model.md` for finding types, severity, output fields, and guardrails.
2. Confirm review objective, document type, and required output format.
3. Extract text and render pages when layout or tables matter.
4. Identify obligations, risks, inconsistencies, missing information, and approval notes.
5. Cite page references for every material finding.
6. Separate facts from recommendations and mark low-confidence extraction.

## Telemetry

- Use `skill.invocation.*` for the review Skill.
- Use `plugin.component.invoked` for parser, renderer, or OCR components.
- Do not emit PDF contents, extracted text, prompts, tool arguments, or model outputs.
