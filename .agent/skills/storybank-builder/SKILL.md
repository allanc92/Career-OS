---
name: storybank-builder
description: Turn a real accomplishment into a reusable STAR story through grounded follow-up questions, explicit unknowns, and approval-gated StoryBank updates.
---

# StoryBank Builder

## Use when

Use this skill when the user wants to add, develop, or improve an interview story based on a real experience.

Read and follow `AGENTS.md` first. `AGENTS.md` is canonical if this skill conflicts with it.

## Inputs

- A user-provided accomplishment, event, or existing story.
- Any written notes or files the user points to.
- Optional target competency, role, or interview question.
- User answers to grounded follow-up questions.

## Source files

1. `AGENTS.md`
2. `Interview_Prep/StoryBank.md`
3. `Interview_Prep/StoryBank_Pipeline.md`
4. `Achievements/Achievement_Log.md`
5. `Resume/Master_Resume.*`, when relevant
6. `config/profile.md`, for voice only, if it exists
7. User-provided written notes

Treat the user's statements as sources. Do not use example-persona content as evidence for the user.

## Workflow

1. Identify whether the experience already appears in the StoryBank or pipeline. If it does, propose enrichment instead of creating a duplicate.
2. Restate the known facts and label unknowns. Ask the user to correct the restatement before expanding the story.
3. Ask focused follow-ups in small groups:
   - Situation: context, stakes, constraints, and timing.
   - Task: the user's responsibility and what success meant.
   - Action: decisions, sequence, collaborators, tradeoffs, and the user's specific contribution.
   - Result: observed outcome, evidence, timing, and who measured it.
   - Reflection: lesson, what changed afterward, and when this story is useful.
4. Ask for metrics only as open questions such as "Was the result measured?" Never propose a value or range. If a fact is unavailable, write `[TBD]`.
5. Draft a story with:
   - Title and one-line takeaway.
   - Competencies demonstrated.
   - STAR sections.
   - A concise spoken-answer outline.
   - Evidence and source notes.
   - Honest `[TBD]` fields.
6. Classify the draft using the states defined in
   `Interview_Prep/StoryBank_Pipeline.example.md`:
   - `Developing`: a material fact needed for an accurate STAR story is still
     `[TBD]`. Propose a pipeline row, not a canonical StoryBank entry.
   - `Ready for review`: the story is verified, coherent, and has no material
     `[TBD]`. Propose the exact canonical StoryBank entry and the pipeline
     transition for review.
7. Ask for explicit approval or corrections before writing.
8. After approval, create or update that story's single row in
   `Interview_Prep/StoryBank_Pipeline.md`. If the user approves the canonical
   story, append it to `Interview_Prep/StoryBank.md`, set the pipeline state to
   `Filed`, and add the filed-entry link. Otherwise leave it `Developing` or
   `Ready for review`. Preserve every other story and row.
9. Re-read each changed file and report the title, status, sources used, and remaining `[TBD]` fields.

## Approval gates

- Confirm the initial factual restatement before developing the story.
- Show the complete proposed entry and pipeline status before any file change.
- If approval introduces new facts or changes meaning, revise and request approval again.
- Ask before replacing or materially rewriting an existing story.
- Follow the one-time private-data acknowledgement in `AGENTS.md` before the first real-data write.

## Outputs

- A grounded STAR story proposal.
- An approved entry in `Interview_Prep/StoryBank.md` when the story is filed.
- An approved pipeline row using `Developing`, `Ready for review`, or `Filed`.
- A list of sources and unresolved `[TBD]` fields.

## Edge cases

- Thin input: propose a `Developing` pipeline row with `[TBD]` only if the user
  approves; do not add the stub to the canonical StoryBank.
- No measurable outcome: use a confirmed qualitative result. Do not force a metric.
- Shared work: distinguish the team's outcome from the user's actions.
- Confidential details: generalize only with the user's approval and preserve truth.
- Conflicting versions: show the conflict and ask the user which version is correct.
- Duplicate story: enrich the existing entry or cross-reference it instead of appending a second copy.
- Unsupported competency: omit it or label it `[TBD]`.

## Never invent

- Never invent metrics, dates, stakes, constraints, actions, feedback, results, lessons, or competencies.
- Never infer the user's contribution from a team result.
- Never convert an estimate into a measured fact.
- Never remove `[TBD]` until the user supplies or confirms the missing fact.
- Never make a story sound more senior, certain, or successful than its sources support.
