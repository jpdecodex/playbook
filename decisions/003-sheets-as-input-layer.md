# ADR 003 — Google Sheets as the Input Layer

**Date:** 2026-05
**Status:** Active

## Decision

Google Sheets is the primary interface for manual data entry across all projects.

## Context

Systems require regular manual entry. The interface needs to be: accessible from any device (especially mobile), low-friction, and not require a custom-built form to maintain.

## Reasoning

- Sheets is already part of daily workflow. No new tool to learn.
- Mobile entry via the Sheets app is faster than any custom form.
- The Sheets API allows read/write from any backend — practical database for human-curated data.
- Building a custom input UI adds development and maintenance overhead for zero functional improvement at this scale.

## Consequences

- Sheets is source of truth for all manually entered data.
- Dashboards read from Sheets via the API (directly or through a Workers proxy).
- No raw Sheets data is committed to repos. Only schema documentation lives in docs/.
