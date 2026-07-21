# Achievements

This folder is the source of truth for concrete career wins. It is a living,
append-only ledger used to ground resume bullets, application claims, and
interview stories.

## Setup

`Achievement_Log.example.md` is a tracked schema with neutral placeholders.
During onboarding, the assistant creates `Achievement_Log.md` from it. The real
file contains personal information and should remain untracked.

Before saving real information for the first time, the assistant must ask:

> This is your private copy. Real details stay on your computer and out of any
> public repository. Your AI provider may process content you share with it.
> OK to save?

The assistant must receive an explicit yes. For later changes, a direct request
such as "log this win" is approval for that win only. Otherwise, the assistant
must show the proposed entry and wait for approval before writing.

## Entry schema

Every achievement uses these fields:

- `ID`: stable ID in the form `ACH-YYYYMMDD-NNN`
- `Date`: when the result happened, or the best known month
- `Title`: short outcome-focused label
- `Status`: `Draft`, `Grounded`, or `Archived`
- `Context`: situation and why it mattered
- `Contribution`: what the user personally did
- `Outcome`: result and who benefited
- `Metrics`: confirmed numbers, or `None confirmed`
- `Sources`: resume section, note path, artifact, or `User confirmed YYYY-MM-DD`
- `Skills`: demonstrated capabilities
- `Tags`: reusable lowercase labels
- `Story link`: StoryBank ID, `Candidate`, or `None`
- `Sensitivity`: `Shareable`, `Internal`, or `Confidential`
- `Added`: date added to the ledger
- `Updates`: dated corrections or added evidence

## Status rules

- `Draft`: useful details or source grounding are still missing.
- `Grounded`: the user approved the wording and every factual claim has a source.
- `Archived`: retained for history but not recommended for reuse.

Never guess a metric, date, scope, employer detail, or personal contribution.
Use `[TBD]` and ask. Append new entries at the bottom. Preserve old
content; place corrections in `Updates` and change status only with approval.
