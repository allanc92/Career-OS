# Pipeline

`Activity_Log.md` is the source of truth for every opportunity and status
change. It is an append-only event log: one row for each meaningful update,
oldest at the top and newest at the bottom. The newest row for an Opportunity ID
is its current state.

## Setup

`Activity_Log.example.md` is tracked and contains the schema. Onboarding creates
the real, untracked `Activity_Log.md`.

## Required columns

| Column | Rule |
| --- | --- |
| Date | `YYYY-MM-DD`, the date of the event |
| Opportunity ID | Stable `OPP-YYYYMMDD-org-role` ID |
| Organization | Organization name |
| Role | Role or opportunity name |
| Status | One exact status from the list below |
| Next action | One concrete action, or `None` |
| Due | `YYYY-MM-DD`, `TBD`, or `None` |
| Application | Relative application folder, or `None` |
| Note | Brief factual context; detailed notes belong in the application folder |

## Statuses

Use exactly one:

- `Lead`: discovered, no decision yet
- `Researching`: actively evaluating fit
- `Networking`: seeking context or an introduction
- `Preparing`: preparing materials before submission
- `Applied`: submitted
- `Recruiter Screen`: first recruiting step scheduled or complete
- `Interviewing`: interview process in progress
- `Final Round`: final stage in progress
- `Offer`: written offer received
- `Negotiating`: offer terms under discussion
- `Accepted`: offer accepted
- `Rejected`: organization ended the process
- `Withdrawn`: user ended the process
- `Closed`: opportunity ended for another reason
- `Paused`: intentionally inactive but may resume

Offer analysis uses more detailed offer statuses, but its corresponding pipeline
row must use `Offer`, `Negotiating`, `Accepted`, `Withdrawn`, or `Closed`.

## Write and approval rules

A direct request such as "mark this applied" or "log this opportunity" approves
that one append. Otherwise, show the complete proposed row and wait for explicit
approval. Never silently change a prior row. Correct mistakes by appending a new
row with the corrected value and an explanatory note.

The first save of real information also requires the privacy confirmation
described in `Achievements/README.md`. Never infer a status from silence. If the
organization, role, date, or next action is unclear, ask.
