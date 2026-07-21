---
name: weekly-review
description: Produce a source-grounded weekly view of the opportunity pipeline, recent wins, missing context, and next actions without changing status or inventing progress.
---

# Weekly Review

## Use when

Use this skill when the user asks where their search stands, requests a weekly review, or wants grounded priorities for the next week.

Read and follow `AGENTS.md` first. `AGENTS.md` is canonical if this skill conflicts with it.

## Inputs

- Review period. Default to the seven calendar days ending on the current local date, and state the exact range.
- Optional priorities, capacity, deadlines, or opportunities the user wants emphasized.
- Optional corrections to stale or incomplete source entries.

## Source files

1. `AGENTS.md`
2. `Pipeline/Activity_Log.md`
3. `Achievements/Achievement_Log.md`
4. `Interview_Prep/StoryBank_Pipeline.md`
5. `Interview_Prep/StoryBank.md`, only when story details are needed
6. Relevant `Applications/*/ApplicationNotes.md` and `ConversationLog.md`
7. `config/profile.md`, for goals and constraints, if it exists

Use file dates only for locating possible material, not as proof that an event happened on that date.

## Workflow

1. State the review period and files being read. If a source file is missing, continue with available sources and name the limitation.
2. Build the current pipeline from the latest explicit status for each organization and role. Preserve the log's status wording. Do not infer a newer status from elapsed time or folder contents.
3. Summarize:
   - Active opportunities by current status.
   - Explicit movement during the review period.
   - Confirmed wins added during the period.
   - StoryBank items whose pipeline state is not yet `Filed`.
   - Deadlines and follow-ups explicitly recorded.
4. Identify outstanding `[TBD]` context, conflicting entries, and stale items. Describe a stale item as "no recorded update since [date]," not as abandoned or rejected.
5. Propose a short, prioritized next-action list. Tie every action to a source, user goal, explicit deadline, or missing fact. Label general suggestions as suggestions.
6. Present the review in chat with sections:
   - Snapshot
   - Movement this period
   - Wins
   - Outstanding `[TBD]` context
   - Risks and stale items
   - Next actions
7. Ask the user to confirm corrections and choose whether any proposed log updates should be saved.
8. Do not write by default. If the user requests updates, show the exact append-only lines or edits and obtain explicit approval before changing any file.
9. After approved updates, re-read affected files and regenerate only the sections changed by the new facts.

## Approval gates

- Reading and presenting a chat summary needs no approval.
- Any pipeline status, deadline, achievement, story status, or application-file change requires an exact proposal and explicit approval.
- Never silently clean up, normalize, deduplicate, or reorder source logs.
- Follow the one-time private-data acknowledgement in `AGENTS.md` before the first real-data write.

## Outputs

- A dated weekly review in chat.
- A current pipeline snapshot based on latest explicit entries.
- Confirmed wins and StoryBank work in progress.
- A consolidated list of outstanding `[TBD]` context.
- Prioritized next actions with source-based reasons.
- Optional approved append-only source updates.

## Edge cases

- Empty pipeline: report that no opportunities are recorded and suggest adding only opportunities the user confirms.
- Duplicate organization and role: use dates and application folders to distinguish them; ask if still ambiguous.
- Conflicting latest statuses: show both entries and ask for correction.
- No wins this period: say none were recorded; do not say none occurred.
- Missing dates: place the item under `[TBD]` rather than inside the review period.
- Overdue follow-up: report the recorded due date and lack of a later update, not the reason.
- Large pipeline: summarize by status, then list the few items with explicit deadlines, recent movement, or missing decisions.

## Never invent

- Never invent progress, wins, dates, deadlines, priorities, status changes, responses, or reasons for inactivity.
- Never infer rejection, withdrawal, advancement, or completion from silence.
- Never treat a planned action as completed.
- Never turn a file modification time into a career event date.
- Never fill missing context from patterns in other applications. Keep `[TBD]` until the user confirms it.
