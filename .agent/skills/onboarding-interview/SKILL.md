---
name: onboarding-interview
description: Run a thorough, resumable interview that builds a grounded private career profile, master resume, achievement log, and StoryBank with approval before every write.
---

# Onboarding Interview

## Use when

Use this skill when the user asks to set up Career OS, start onboarding, resume
an interrupted onboarding session, or rebuild missing foundational context.

Read and follow `AGENTS.md` first. It is canonical if this skill conflicts with
it. Read `ONBOARDING.md` for the user-facing promise.

## Required behavior

- Ask one focused question at a time.
- Follow useful answers with specific grounding questions.
- Prefer the user's language over polished generic language.
- Never invent or suggest a career fact, motivation, result, or number.
- Use `[TBD]` for a material fact the user cannot currently confirm.
- Explain why a sensitive question matters and allow the user to skip it.
- Treat onboarding as intentionally thorough.
- Remind the user that this is a strong starting point that can grow later.

## Source files

Before asking questions, inspect:

1. `AGENTS.md`
2. `ONBOARDING.md`
3. `config/profile.example.md`
4. `Resume/README.md` and `Resume/Master_Resume.example.md`
5. `Achievements/Achievement_Log.example.md`
6. `Interview_Prep/StoryBank.example.md`
7. `Interview_Prep/StoryBank_Pipeline.example.md`
8. `Pipeline/Activity_Log.example.md`

Also inspect real files at the corresponding paths if they exist. Ignore all
facts under `examples/`, in `.example.md` files, and in `_TEMPLATE_` paths.

## First-run or resume detection

Before the interview:

1. Look for real files at the expected private paths.
2. If none exist, explain the interview and begin at Phase 0.
3. If one or more exist, read only what is needed and report:
   - completed phases
   - partial sections
   - unresolved `[TBD]` items
   - expected files that are still missing
4. Ask whether the user wants to continue from the first incomplete phase,
   revisit a completed phase, or stop.
5. Never restart or overwrite approved content silently.

Use this checkpoint block near the top of `config/profile.md`:

```markdown
## Onboarding status

- Status: [In progress | Complete]
- Last completed phase: [0-8]
- Last checkpoint: [YYYY-MM-DD]
- Privacy confirmation: [Confirmed YYYY-MM-DD | Not confirmed]
- Open onboarding items: [List or None]
```

The checkpoint is private data and follows the same approval rules as the rest
of the profile.

## Phase 0: Orient and confirm privacy

Explain:

- Career OS is a private working folder, not a public profile.
- Standard personal paths are ignored by Git, but `.gitignore` does not control
  how the user's AI provider processes content.
- The assistant will show proposed personal file content before writing.
- The user can skip a question, stop, or resume later.

Before the first real-data write, ask the exact one-time privacy question from
`AGENTS.md`. Do not save personal details without an explicit yes.

## Phase 1: Background and career arc

Start broadly:

> Tell me the story of how you got to where you are today.

Follow the user's path rather than forcing a resume chronology. Explore:

- current professional identity
- roles, projects, education, service, caregiving, or other relevant experience
- turning points and why the user made confirmed choices
- transitions, recurring themes, and the career throughline
- what the user wants to carry forward and leave behind

Do not infer why a transition happened. Ask.

## Phase 2: Energy, interests, and best-work conditions

Explore:

- work and problems that create energy
- topics the user returns to without being prompted
- people, customers, or communities they want to serve
- preferred balance of autonomy, structure, collaboration, pace, and ambiguity
- environments where they have done their best work
- work patterns they want less of

Separate demonstrated preferences from possibilities the user wants to explore.

## Phase 3: Strengths and evidence

Ask what the user believes they do well, then ground each important strength in
an example. Explore:

- skills and judgment
- scope and ownership
- how others rely on the user
- feedback the user has actually received
- domain knowledge, tools, methods, and transferable capabilities

If evidence is weak or missing, label the strength as developing or `[TBD]`.

## Phase 4: Achievements and StoryBank seeds

Ask for two or three accomplishments the user is proud of. For each:

1. Establish the situation and stakes.
2. Clarify the user's own task and responsibility.
3. Separate the user's actions from the team's actions.
4. Ask what changed and who benefited.
5. Ask for measurement only if one exists.
6. Identify a source: resume section, note, artifact, or dated confirmation.
7. Ask about sensitivity and where the story can be used.

Create a proposed Achievement Log entry for each grounded win. Put incomplete
stories in the StoryBank Pipeline as `Captured` or `Developing`. File a polished
StoryBank entry only when all core facts are grounded and the user approves the
framing.

Never turn vague impact into a number. "Improved the process" remains an
unquantified outcome unless the user confirms a measure.

## Phase 5: Target direction and constraints

Explore:

- roles, paths, or problems to pursue
- desired level, scope, and responsibilities
- industries, organization types, or missions
- location, work model, travel, schedule, and timing
- compensation needs if the user chooses to share them
- work authorization or other practical constraints
- non-negotiables and acceptable tradeoffs

`Not decided` is a valid answer. Do not manufacture a narrow target for a user
who is still exploring.

## Phase 6: Voice

Ask how the user wants to sound and what they want to avoid. Collect:

- three or more tone words
- phrases that sound natural to the user
- phrases, habits, and corporate language they dislike
- one short writing sample if they want to provide it

Do not erase personality in the name of professionalism.

## Phase 7: Master resume

Look for exactly one real `Resume/Master_Resume.*` file, excluding examples.

If one exists:

1. Confirm that it is the canonical master.
2. Read it if the tool can do so reliably.
3. Compare it with confirmed interview facts.
4. Surface conflicts and gaps. Do not resolve them without the user.

If the user provides a file:

- Prefer Markdown or plain text for reliable agent use.
- A PDF or DOCX may be used only if the active tool can read it reliably.
- If extraction is incomplete or uncertain, say so and ask the user to paste or
  export the text.
- Never claim to have read a file that was not successfully read.

If no resume exists:

1. Offer to draft `Resume/Master_Resume.md` from confirmed interview facts.
2. Mark missing dates or details `[TBD]`.
3. Show the complete draft for review.
4. Save only after explicit approval.

The master resume is a factual base, not a document tailored to one role.

## Phase 8: Synthesize, preview, and save

Prepare a proposed write plan using only relevant files:

- `config/profile.md`
- `Resume/Master_Resume.*`
- `Achievements/Achievement_Log.md`
- `Interview_Prep/StoryBank.md`
- `Interview_Prep/StoryBank_Pipeline.md`
- `Pipeline/Activity_Log.md`

For every proposed file:

1. Show the complete new content or a precise diff.
2. Name the exact path.
3. List sources and every `[TBD]`.
4. Identify any confidential content and its intended boundary.
5. Ask for explicit approval.

The user may approve files individually or as one clearly listed batch. Apply
only approved changes.

## Resumable checkpoints

After each completed phase:

1. Summarize what was learned.
2. Propose the corresponding profile section and updated onboarding checkpoint.
3. Ask whether to save that checkpoint.
4. If approved, update `config/profile.md` without changing other approved
   sections.

Incremental approved checkpoints allow a later assistant to resume. If the user
does not approve a checkpoint, do not write one and explain that unsaved answers
may need to be repeated in a later session.

When resuming, summarize existing approved context before asking the first new
question. Do not repeat completed phases unless the user requests a review.

## Completion

Onboarding is complete when:

- the profile captures the user's career shape, direction, constraints, and
  voice
- a master resume exists or its absence is an explicit open item
- initial achievements are grounded
- StoryBank seeds and missing details are visible
- all created personal files were approved
- remaining unknowns are listed

Set the onboarding checkpoint to `Complete`, then report:

- exact files created or changed
- achievements and stories seeded
- outstanding `[TBD]` items
- privacy-sensitive items deliberately excluded
- useful next prompts

Close by reminding the user that Career OS keeps learning. New wins, stories,
interests, and goals can be added at any time.

## Edge cases

- **User stops early:** Offer an approved checkpoint, then stop without pressure.
- **Existing partial profile:** Resume from the first incomplete phase.
- **Existing complete profile:** Ask what has changed instead of rerunning all
  phases.
- **No master resume:** Offer a grounded first draft; do not block onboarding.
- **Unreadable resume:** Ask for text; do not guess from a filename or partial
  extraction.
- **Conflicting dates or titles:** Show both sources and ask which is correct.
- **No measurable result:** Record the confirmed qualitative outcome.
- **No accomplishments come to mind:** Ask about problems solved, people helped,
  difficult decisions, repeated praise, or work made easier. Do not propose a
  fictional example as if it were theirs.
- **Multiple possible directions:** Preserve them as explorations with decision
  criteria instead of forcing one target.
- **Sensitive detail:** Ask whether a less specific version is enough, or keep
  it out of Career OS.
- **Privacy confirmation declined:** Keep work in chat and create no personal
  files.

## Never invent

Never invent employers, titles, dates, education, skills, motivations, metrics,
team size, scope, outcomes, interests, constraints, compensation, or goals.
Never use public examples as evidence about the user. Ask, use `[TBD]`, or omit
the claim.
