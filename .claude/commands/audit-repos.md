---
description: Full reporting-only audit of every repo in the projects root — status, CLAUDE.md accuracy, structure quality, next actions. Fixes nothing.
---

Full repo audit. This is a reporting session only — do not fix, restructure,
rename, or delete anything. Just produce the report.

For every repo in this projects root:
1. Name, last commit date + message, current branch, uncommitted changes (yes/no)
2. Read CLAUDE.md — is "Next action" still accurate given git log? Flag if missing.
3. Classify ACTIVE (commits in last 14 days) / STALE (14-30 days, no "parked"
   note) / PARKED (explicitly marked dormant in its own CLAUDE.md)
4. Flag DEAD candidates: 30+ days, not marked parked, no clear reason to keep
5. Flag clutter: stale branches, huge untracked files, committed secrets,
   duplicate logic across repos
6. For ACTIVE/STALE repos: single next physical action, one line

Output as a table: repo | status | CLAUDE.md accurate? | next action | flag

7. Professional-structure check for every repo: README quality, dependency
   manifest present/current, .gitignore coverage, no committed secrets,
   tests present or not, sane folder layout, LICENSE, commit message quality.
   Add columns: structure score (solid/needs-work/messy), highest-value fix.

Then a summary: safe-to-archive repos, repos needing a CLAUDE.md fix, most
obvious next thing to work on, and which repos aren't presentable if shown
to another developer or made public.
