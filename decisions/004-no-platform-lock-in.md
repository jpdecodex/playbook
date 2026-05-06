# ADR 004 — No Platform Lock-in

**Date:** 2026-05
**Status:** Active

## Decision

No third-party platforms that hold data or logic in a proprietary format. This includes Notion, Airtable, Zapier, Make, Monday.com, and similar tools.

## Context

This ecosystem is permanent infrastructure for personal and business operations. Systems dependent on a SaaS platform are implicitly dependent on that platform's pricing, availability, and API stability — none of which are in our control.

## Reasoning

- Platforms get acquired, change pricing, deprecate APIs, or shut down.
- Data in Notion or Airtable is effectively trapped in their format.
- Google Sheets + GitHub + Cloudflare + SQLite/Postgres covers every use case these platforms solve, with full ownership.

## What is allowed

- Google Sheets — clean CSV export, standard API.
- GitHub — git is portable, full repo export always available.
- Cloudflare Pages/Workers — deploying elsewhere requires config changes but no data migration.
- Anthropic (Claude) — prompts and outputs are plain text, no lock-in.

## Consequences

- Automations built in Python or Workers, not Zapier.
- Documentation lives in Markdown in repos, not Notion.
- Any exception requires explicit justification in the project's CLAUDE.md.
