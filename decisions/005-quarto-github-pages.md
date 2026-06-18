# ADR 005 — Quarto + GitHub Pages for Static Dashboards

**Date:** 2026-06
**Status:** Active
**Supersedes:** [ADR 002](002-cloudflare-stack.md) for static site deployments

## Decision

Quarto + GitHub Pages is the standard for all static dashboard and site deployments.

## Context

ADR 002 established Cloudflare Pages as the hosting standard. In practice, static dashboards in this ecosystem (Life OS, dog-capitals, brand pages) require no edge compute, no serverless logic, and no Cloudflare-specific features. Quarto is already in use for dog-capitals and produces the same result with a simpler stack and no vendor account dependency.

## Reasoning

- Quarto is already the tool for dog-capitals — reusing the same pattern costs nothing.
- GitHub Pages deploys directly from the `docs/` folder on push to main — same flow as Cloudflare Pages, zero additional config.
- No vendor account needed beyond GitHub, which is already required.
- Quarto outputs standard HTML/CSS/JS — no lock-in, fully portable.
- Daily data refresh via GitHub Actions (rebuild on schedule) is sufficient for personal dashboards.

## Consequences

- All static dashboards use Quarto with `output-dir: docs` and GitHub Pages serving from `docs/`.
- Deploy trigger: push to `main` (GitHub Pages auto-deploys) or scheduled GitHub Actions rebuild for data freshness.
- Data refresh: GitHub Actions fetches from Google Sheets API daily, writes CSVs to `data/`, runs `quarto render`, commits and pushes.
- Cloudflare Workers remains available for dynamic API endpoints if real-time data is required in the future.
- ADR 001 (no JS frameworks) still applies inside Quarto pages — vanilla JS for any custom interactivity.

## What uses this standard

- life-os — migrating from Cloudflare Pages
- dog-capitals — already on this stack
- Any future brand page or static dashboard
