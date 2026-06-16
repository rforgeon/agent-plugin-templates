# CRM Connector Contract

Replace this file with your Salesforce, HubSpot, Attio, Dynamics, enrichment provider, or warehouse connector.

## Required operations

- Read account, contact, opportunity, or renewal records by id, owner, segment, or missing-field query.
- Fetch field metadata and allowed values.
- Resolve safe source categories for suggested enrichments.

## Optional operations

- Draft update payload.
- Write approved field changes.
- Create owner task for low-confidence enrichment.

Writes must require explicit user approval.

## Telemetry

Emit `plugin.component.invoked` for CRM reads, metadata reads, enrichment lookups, and approved writes. Do not emit field values, record payloads, prompts, tool arguments, or model outputs.

