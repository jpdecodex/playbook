# ADR 006 — Common Project Methodology

**Status:** Active
**Date:** 2026-09-05

## Context

Every repo/project in this workspace ended up with its own ad-hoc structure
— `es-core-vol-targeting`'s `CLAUDE.md`+`docs/history.md` pattern is the
most disciplined, but it was never named as a standard and never applied
on purpose elsewhere. The vault's `Historial de decisiones.md`,
`digital-life-os/MILESTONES.md`, and Nodo20's `Plan de Accion 2026.xlsx`
independently converged on roughly the same shape without anyone deciding
that on purpose either.

This generalizes the "Regla de Oro" flagged as a candidate ADR in this
repo's own `CLAUDE.md` since 2026-08-28 ("nothing gets published/sent/
applied without being defensible with real criteria and citations") —
deferred until the projects-root reorganization settled. It settled
2026-09-05.

## Decision

Every project in this workspace — repo or not — follows the same
five-element skeleton, adapted in *format* per project, never dropped in
*role*:

1. **Current State** — one paragraph, always overwritten, never appended.
   What's true right now, nothing more.
2. **Next Action** — a single next concrete step, not a backlog dump.
3. **Decision Log** — append-only, dated entries: what was decided, why,
   what was rejected and why. Corrections are new dated entries, never
   rewrites of a past one.
4. **Evidence/Research** — wherever the real work product lives (a repo's
   `docs/`, a notebook, an Excel workbook, a Drive folder). The role is
   fixed; the format follows the project's real nature — don't force a
   markdown file on a project whose actual collaborators use Excel/Drive.
5. **Target Impression** — one line: the specific, calibrated judgment a
   *qualified* outsider should reach after actually looking closely at
   this project's evidence. Not a vanity/audience metric — a professional
   one, aimed at whoever would really evaluate that domain (a quant, a
   client, a collaborator). Optional for projects nobody external
   evaluates (personal infra, a deliberately light personal-vlog track).

`templates/CLAUDE.md` (this repo) is the reference implementation for
code repos — 5 sections, updated every session close.

## Consequences

- No project gets to stay structurally ad-hoc going forward — but the
  *format* adapts freely; only the five roles are fixed.
- This does not mean over-organizing before starting real work. The
  skeleton is maintained *as* work happens, not built as a prerequisite.
- Existing projects already partially compliant (Revolución Dulce's
  `MANERA_DE_TRABAJAR.md`/`PROXIMOS_PASOS.md`, digital-life-os's
  `MILESTONES.md`) don't need new files — just recognize they already
  fit and add what's missing (mainly Target Impression, where relevant).
