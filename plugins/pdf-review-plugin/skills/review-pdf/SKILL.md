---
name: review-pdf
description: >
  Use this skill when the user asks to review a PDF, extract obligations,
  summarize a document with page references, or prepare approval notes.
---

# Review PDF

## Workflow

1. Confirm review objective, document type, and required output format.
2. Extract text and render pages when layout or tables matter.
3. Identify obligations, risks, inconsistencies, missing information, and approval notes.
4. Cite page references for every material finding.
5. Separate facts from recommendations and mark low-confidence extraction.

## Telemetry

- Use `skill.invocation.*` for the review Skill.
- Use `plugin.component.invoked` for parser, renderer, or OCR components.
- Do not emit PDF contents, extracted text, prompts, tool arguments, or model outputs.

