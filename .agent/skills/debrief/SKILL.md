---
name: debrief
description: Process only the user's existing written notes after a career conversation, capture lessons, update the pipeline, and propose grounded StoryBank enrichment.
---

# Debrief

## Use when

Use this skill after an interview, networking conversation, recruiter exchange, or similar event when the user already has written notes to review.

Accept only notes the user has already written. If no notes exist, ask the user
to write what they remember in their own words. Do not request source media or
conversion of other material into text. Read and follow `AGENTS.md` first.
`AGENTS.md` is canonical if this skill conflicts with it.

## Inputs

- The user's existing written notes, pasted in chat or identified by file path.
- Organization, role, event type or round, and date.
- Optional application folder and prep document.
- Optional user corrections to ambiguous wording in the notes.

## Source files

1. `AGENTS.md`
2. The user's existing written notes
3. The relevant `Applications/[Org]_[YYYY-MM-DD]/ApplicationNotes.md`
4. The relevant prep document, if one exists
5. The relevant `Applications/[Org]_[YYYY-MM-DD]/ConversationLog.md`
6. `Pipeline/Activity_Log.md`
7. `Interview_Prep/StoryBank.md`
8. `Interview_Prep/StoryBank_Pipeline.md`

Do not search for or create other forms of event capture. Do not use memory, generic interview patterns, or outside sources as evidence of what happened.

## Workflow

1. Verify that existing user-written notes were provided. If not, stop and ask the user to paste or point to notes they already wrote.
2. Confirm organization, role, event, and date from the notes or user. Mark unresolved context `[TBD]`; do not guess.
3. Read the relevant application and prep files if available. If either is missing, continue from the notes and label the comparison unavailable.
4. Extract only what the notes support:
   - One-line factual verdict.
   - Topics covered and signals explicitly observed.
   - The user's impressions, kept separate from observed facts.
   - Agent interpretation, clearly labeled and tied to note evidence.
   - What landed, according to evidence in the notes.
   - What was unclear or should be watched.
   - Lessons for future preparation.
   - Follow-up actions, owners, and dates explicitly stated.
5. Compare the notes with the prep plan. Distinguish planned topics from topics that the notes show were actually covered.
6. Check whether the notes add grounded detail to an existing StoryBank entry, such as a clearer action, result, lesson, or question fit. Draft enrichment only from those notes. Use `[TBD]` where context is missing.
7. Prepare one bundled proposal in chat:
   - ConversationLog entry.
   - Lessons and next actions.
   - Exact pipeline line with a user-confirmed status.
   - Exact StoryBank enrichment and pipeline status change, if any.
8. Ask for explicit approval or corrections. Do not write any file before approval.
9. After approval:
   - Append the approved entry to the relevant `ConversationLog.md`.
   - Append the approved line to `Pipeline/Activity_Log.md`.
   - Apply the approved StoryBank enrichment and update `StoryBank_Pipeline.md`, if proposed.
   - Preserve prior entries and do not silently change earlier interpretations.
10. Re-read changed files and report captured lessons, next actions, StoryBank changes, and unresolved `[TBD]` items.

## Approval gates

- Show all proposed file content and pipeline status before writing.
- Require explicit approval for StoryBank enrichment, even when the detail appears clear.
- If no relevant StoryBank detail exists, say so and make no StoryBank change.
- If a target file does not exist, include its creation in the proposal and wait for approval.
- Follow the one-time private-data acknowledgement in `AGENTS.md` before the first real-data write.

## Outputs

- A concise debrief grounded only in the user's written notes.
- An approved appended `ConversationLog.md` entry.
- An approved appended `Pipeline/Activity_Log.md` line.
- Optional approved enrichment to `Interview_Prep/StoryBank.md` and `StoryBank_Pipeline.md`.
- A list of lessons, next actions, and outstanding `[TBD]` context.

## Edge cases

- No written notes: do not reconstruct the event; leave files unchanged.
- Sparse notes: produce a limited draft, use `[TBD]`, and state what cannot be concluded.
- No application folder: propose a safe target folder or a notes-only chat summary before writing.
- Notes report mixed signals: preserve the ambiguity.
- Status is not explicit: ask the user; never infer advancement or rejection.
- Notes conflict with an existing story: surface the conflict and wait for the user to resolve it.
- Sensitive details: include only what is necessary and follow `AGENTS.md` privacy rules.

## Never invent

- Never invent questions, answers, reactions, feedback, sentiment, decisions, outcomes, or next steps.
- Never infer that something landed from silence or vague wording.
- Never infer pipeline status from the event type.
- Never turn a planned talking point into one that was actually discussed.
- Never fill missing context with common interview advice. Use `[TBD]` or omit it.
