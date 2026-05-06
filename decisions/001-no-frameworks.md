# ADR 001 — No JavaScript Frameworks

**Date:** 2026-05
**Status:** Active

## Decision

Vanilla JS (ES6+) by default. No React, Vue, Next.js unless explicitly justified per project.

## Context

Dashboards in this ecosystem are personal tools: single user, low traffic, no complex state management. The overhead of a framework adds complexity without adding value at this scale. Target hosting is Cloudflare Pages — frameworks requiring a build step or Node server are incompatible.

## Reasoning

- Vanilla JS loads faster, has zero dependencies, and is readable without framework knowledge.
- Frameworks solve problems of scale and team coordination. A solo builder with AI tooling does not have those problems.
- If a project outgrows vanilla JS, migration to a framework is straightforward. The reverse is not.

## Consequences

- All frontend code must run without a build step.
- External libraries loaded via CDN when needed, not bundled.
- Any project that overrides this must document the justification in its own CLAUDE.md.
