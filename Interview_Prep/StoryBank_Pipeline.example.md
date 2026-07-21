# StoryBank Pipeline

This tracked file is the schema only. Onboarding creates the real, untracked
`StoryBank_Pipeline.md`.

Append a row when a story is captured. For a state change, update only that
story's row after approval and refresh `Last updated`. A `Filed` or `Retired`
row must point to an approved entry in `StoryBank.md`.

| Story ID | Working title | Sources | State | Missing details | Next action | Target use | Filed entry | Last updated |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| STORY-001 | Improving a repeated team process | ACH-20260115-001 | Captured | Confirm individual actions and result | Ask grounding questions | question:improvement | None | 2026-01-15 |
| [STORY-NNN] | [Working title] | [ACH-ID, resume section, or note path] | [Captured | Developing | Ready for review | Filed | Parked | Retired] | [Missing facts or None] | [One next action or None] | [question:tag or role:tag] | [StoryBank heading or None] | [YYYY-MM-DD] |

## State transitions

`Captured` -> `Developing` -> `Ready for review` -> `Filed`

Use `Parked` from any unfinished state when work is intentionally deferred. Use
`Retired` for a filed story that should no longer be recommended. State changes
require user approval; only `Filed` and `Retired` stories belong in
`StoryBank.md`.
