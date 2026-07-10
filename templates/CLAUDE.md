# CLAUDE.md — [repo-name]

> Replace all [bracketed] fields before committing. Delete this line.

## What this repo does

[One or two sentences: what this repo does, and why it exists. Include stack/hosting only if load-bearing.]

## Current state

[What exists and works today, in the current codebase — not a chronological log. Update this every session.]

## Next action

[The next concrete thing to do. One item or a short list — not a backlog dump.]

## Architecture decisions

[Standing technical decisions and constraints: stack choices, broker/data boundaries, naming/commit conventions specific to this repo, things a future session must not violate. Follow jpdecodex/playbook standards unless overridden here.]

## Origin

(Optional. Populate only for repos that started as a captured idea in Claude.ai chat before becoming a repo. Leave this section out entirely for repos where it doesn't apply — don't leave it blank-but-present.)

---

Every session closes by updating this file (What this repo does / Current state / Next action / Architecture decisions) and committing:

    docs: session close YYYY-MM-DD

`Origin` is not part of that every-session update cycle — it's written once, if at all, and left alone after.

Do not keep a session log or history section in this file — session history is `git log -p CLAUDE.md`.
