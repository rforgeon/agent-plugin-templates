# PDF Processing Contract

Replace this file with your PDF parser, renderer, OCR, storage connector, or document system integration.

## Required operations

- Locate approved PDF inputs.
- Extract text by page.
- Render pages when layout, signatures, or tables matter.
- Return page references for findings.

## Optional operations

- OCR scanned pages.
- Export annotated findings.
- Store review packet in a document system.

## Telemetry

Emit `plugin.component.invoked` for parser, renderer, OCR, and export steps. Emit `plugin.component.error` for unreadable, encrypted, or unsupported files. Do not emit PDF content, extracted text, file paths to user documents, prompts, or model outputs.

