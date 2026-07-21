---
name: achievement-logger
description: Append one concise, evidence-grounded career win to the achievement log and flag possible StoryBank value without inventing impact.
---

# Achievement Logger

## Use when

Use this skill when the user shares a professional win, milestone, positive outcome, or meaningful progress they want to preserve.

Read and follow `AGENTS.md` first. `AGENTS.md` is canonical if this skill conflicts with it.

## Inputs

- The user's description of the win.
- Date or date range, context, contribution, outcome, and evidence, when known.
- Optional source file or written notes supplied by the user.
- Optional preference on whether to develop it into a StoryBank entry later.

## Source files

1. `AGENTS.md`
2. `Achievements/Achievement_Log.md`
3. `Interview_Prep/StoryBank.md` and
   `Interview_Prep/StoryBank_Pipeline.md`, for duplicate and story-candidate
   checks
4. `Resume/Master_Resume.*`, if the user says the win is already documented there
5. User-provided written notes or files

## Workflow

1. Search the achievement log for the same win. If it exists, propose an append-only clarification or enrichment instead of a duplicate.
2. Restate the grounded facts: what changed, the user's specific contribution, result, date, scope, and evidence.
3. Ask only the minimum follow-up questions needed to make the entry useful. Ask whether impact was measured, but never suggest a number.
4. If a detail remains unknown, use `[TBD]`. A qualitative result is valid when the user confirms it.
5. Draft one concise entry that matches
   `Achievements/Achievement_Log.example.md` exactly:
   - A unique `ACH-YYYYMMDD-NNN` ID, date, and outcome-focused title.
   - `Status`: `Grounded` when the core facts and source are confirmed, or
     `Draft` when a material fact remains `[TBD]`.
   - Context, the user's specific contribution, outcome, and confirmed metrics
     or `None confirmed`.
   - Sources, skills, tags, sensitivity, added date, and updates.
   - `Story link`: an existing `STORY-NNN`, `Candidate` when the user wants to
     develop it, or `None`. Never choose `Candidate` on the user's behalf.
6. Show the exact entry and target location in chat. Ask for explicit approval or corrections.
7. After approval, append the entry to `Achievements/Achievement_Log.md`. Never rewrite or reorder earlier entries.
8. If the user wants a story, propose running `storybank-builder`; do not silently add a StoryBank story.
9. Re-read the log and report the appended title and any remaining `[TBD]`.

## Approval gates

- No file change until the user approves the exact achievement entry.
- New facts introduced during review require a revised draft and renewed approval.
- An existing similar entry requires approval before appending an enrichment.
- StoryBank work is a separate approval-gated workflow.
- Follow the one-time private-data acknowledgement in `AGENTS.md` before the first real-data write.

## Outputs

- One approved appended entry in `Achievements/Achievement_Log.md`.
- A concise confirmation with the title, date, and unresolved `[TBD]`.
- An optional invitation to run `storybank-builder`.

## Edge cases

- No measurable result: record a confirmed qualitative outcome without weakening or inflating it.
- Ongoing work: label the result as interim and do not imply completion.
- Team result: state the team's result and the user's specific contribution separately.
- Confidential details: generalize only with user approval and preserve factual meaning.
- Unknown date: use `[TBD]`, not the current date, unless the user confirms the win happened today.
- Duplicate win: enrich the prior record through an append-only note rather than creating a misleading second achievement.

## Never invent

- Never invent or estimate metrics, dates, scope, ownership, collaborators, evidence, or results.
- Never treat effort as impact without a confirmed outcome.
- Never turn team ownership into sole ownership.
- Never label an item a StoryBank candidate on the user's behalf.
- Never remove `[TBD]` without user confirmation.
