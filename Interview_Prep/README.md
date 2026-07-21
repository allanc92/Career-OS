# Interview Prep

This folder holds reusable, source-grounded interview material. Its core asset
is the StoryBank: approved stories that can be selected and adapted without
changing the underlying facts.

## Setup

- `StoryBank.example.md` is the tracked story schema. Onboarding creates the
  real, untracked `StoryBank.md`.
- `StoryBank_Pipeline.example.md` is the tracked development queue schema.
  Onboarding creates the real, untracked `StoryBank_Pipeline.md`.

## Story lifecycle

Use these exact pipeline states:

- `Captured`: a source or possible story has been identified
- `Developing`: facts or STAR sections are incomplete
- `Ready for review`: a grounded draft is complete and awaits user approval
- `Filed`: the user approved it and it exists in `StoryBank.md`
- `Parked`: intentionally deferred
- `Retired`: kept for history but no longer recommended

Only explicit approval moves a story to `Filed`. Filing means adding the
approved story to `StoryBank.md` and appending or updating its pipeline row.
Never delete a prior story merely because a better version exists; mark the old
one `Retired` and link its replacement.

## Grounding rules

Each factual claim must point to an Achievement ID, master resume section,
application note, artifact, or dated user confirmation. Preserve uncertainty.
Use `[TBD]` rather than filling a gap. Confidential source
material may ground private preparation, but confidential details must not be
copied into outward-facing answers.

## Reuse rules

Tags are lowercase `namespace:value` labels:

- `skill:` demonstrated capability
- `theme:` broad story theme
- `scope:` scale or ownership
- `audience:` stakeholder group
- `question:` interview question family
- `role:` relevant role family

Select stories by evidence and relevance, not by forcing a weak match. STAR
variants may shorten delivery, but Situation, Task, Action, Result, metrics, and
attribution must stay consistent.

An assistant must show a new or revised story and its proposed pipeline change
before writing. A direct request to save a displayed story approves only that
version. The first save of real information also requires the one-time privacy
confirmation.
