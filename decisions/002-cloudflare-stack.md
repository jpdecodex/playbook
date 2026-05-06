# ADR 002 — Cloudflare as Primary Infrastructure

**Date:** 2026-05
**Status:** Active

## Decision

Cloudflare Pages for hosting, Cloudflare Workers for serverless backend logic.

## Context

Need hosting that is: free at personal scale, globally distributed, no server management, supports both static files and lightweight backend logic.

## Reasoning

- Pages deploys directly from GitHub. Push to main, it's live.
- Workers provides serverless functions at the edge with a generous free tier — replaces a backend server for API proxying and data endpoints.
- Together they cover the full stack without complex pricing or lock-in.
- Alternatives (Vercel, Netlify, Railway) introduce vendor-specific config that creates migration friction.

## Consequences

- No code should require a persistent server process.
- Backend logic lives in Workers or is handled client-side.
- Scheduled jobs use Workers Cron Triggers, not external schedulers.
