# Activity Log

This tracked file is the schema only. Onboarding creates the real, untracked
`Activity_Log.md`.

The newest row for an Opportunity ID is its current state.

| Date | Opportunity ID | Organization | Role | Status | Next action | Due | Application | Note |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 2026-01-08 | OPP-20260108-example-researcher | Example Organization | Researcher | Lead | Review role requirements | 2026-01-10 | None | Neutral example only |
| 2026-01-10 | OPP-20260108-example-researcher | Example Organization | Researcher | Preparing | Draft tailored materials | 2026-01-12 | Applications/Example_Organization_2026-01-10 | Fit approved; preparing submission |
| [YYYY-MM-DD] | [OPP-YYYYMMDD-org-role] | [Organization] | [Role] | [Exact status] | [Next action or None] | [YYYY-MM-DD, TBD, or None] | [Relative folder or None] | [Brief factual note] |

Valid statuses: `Lead`, `Researching`, `Networking`, `Preparing`, `Applied`,
`Recruiter Screen`, `Interviewing`, `Final Round`, `Offer`, `Negotiating`,
`Accepted`, `Rejected`, `Withdrawn`, `Closed`, `Paused`.
