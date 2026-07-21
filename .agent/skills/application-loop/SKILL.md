---
name: application-loop
description: Assess a role, draft three evidence-backed resume bullets, prepare optional application materials, and track the opportunity without inventing career facts.
---

# Application Loop

## Use when

Use this skill when the user shares a job description or asks for help applying to a specific role.

Do not use it for general resume rewriting without a specific role. Read and follow `AGENTS.md` first. `AGENTS.md` is canonical if this skill conflicts with it.

## Inputs

- The complete job description, pasted by the user or provided as a file.
- Organization, role title, and application date. Ask for any value that cannot be read from the job description. Use the current local date only after telling the user.
- `Resume/Master_Resume.*`. This is required and is the starting point.
- The user's answer to whether a cover letter is needed.
- User answers to gap questions and any corrections to the proposal.

## Source files

Read only the files needed for this application:

1. `AGENTS.md`
2. `Resume/Master_Resume.*`
3. `Interview_Prep/StoryBank.md`
4. `config/profile.md`, if it exists
5. `Achievements/Achievement_Log.md`
6. `Pipeline/Activity_Log.md`
7. `Applications/_TEMPLATE_Org_YYYY-MM-DD/`
8. Any existing `Applications/[Org]_[YYYY-MM-DD]/` files for this opportunity

Do not treat the job description as evidence that the user has a skill or result. Do not read `Private/` unless the user explicitly asks and the use is allowed by `AGENTS.md`.

## Workflow

1. Confirm the job description, organization, role, and date. Locate exactly one real master resume. Ignore example files. If no real master resume exists, stop and ask the user to add one.
2. Read the master resume and StoryBank before drafting. Keep a claim-to-source map for every proposed change.
3. Perform a fit read:
   - Summarize the role's core outcomes and requirements.
   - Identify strong matches with exact source references.
   - Separate partial matches, unknowns, and clear gaps.
   - Give a concise fit assessment without claiming a hiring probability.
4. Ask focused gap questions only where an answer could materially improve accuracy or fit. Ask about scope, actions, tools, outcomes, metrics, constraints, and the user's genuine motivation, but never suggest an answer or number. If the user does not know, keep `[TBD]` in internal notes or omit the claim from application materials.
5. Ask, "Is a cover letter needed for this application?" Do this before drafting application materials. If the user is unsure, do not create one unless they request it.
6. Draft exactly three tailored resume bullets:
   - Ground each bullet in the master resume, StoryBank, or a fact the user confirmed in this conversation.
   - Preserve the original scope, ownership, dates, tools, and measurement basis.
   - Improve relevance and clarity without adding unsupported keywords or capabilities.
   - Show the source for each bullet in the proposal, but do not place source notes in the resume.
7. Prepare a proposal in chat containing:
   - Fit read and unresolved gaps.
   - The original and proposed version of each of the three bullets.
   - A cover letter draft only if requested.
   - Planned folder and file names.
   - The exact proposed pipeline line and its status.
8. Ask for explicit approval or edits. Do not create a folder, save a draft, alter the master resume, or update the pipeline before approval.
9. After approval:
   - Create `Applications/[Org]_[YYYY-MM-DD]/`, replacing filesystem-unsafe characters in `[Org]` with safe separators.
   - Copy the master resume into the folder and apply only the three approved bullet changes. Never modify `Resume/Master_Resume.*`.
   - Create or populate `ApplicationNotes.md` with the fit assessment, gaps, tailoring decisions, and source map.
   - Create `ConversationLog.md` from the template if it does not exist.
   - Save the approved cover letter only if requested.
   - Append one row matching the full schema in
     `Pipeline/Activity_Log.example.md`, including date, Opportunity ID,
     organization, role, status, next action, due date, application path, and
     note. Use `Preparing` unless the user has confirmed another valid status.
     Never infer `Applied`.
10. Re-read every written file. Report what changed and list any remaining `[TBD]` items.

## Approval gates

- Gate 1: The user approves the three bullets, optional letter, file plan, and pipeline line before any write.
- Gate 2: If the user changes facts during approval, revise the proposal and request approval again.
- Gate 3: If the target folder already exists or a file would be overwritten, stop and ask whether to update the existing application or use a different folder. Never overwrite silently.
- Follow the one-time private-data acknowledgement in `AGENTS.md` before the first real-data write.

## Outputs

- A fit read with sourced matches, gaps, and questions.
- Exactly three approved, grounded tailored resume bullets.
- `Applications/[Org]_[YYYY-MM-DD]/` containing the tailored resume, `ApplicationNotes.md`, `ConversationLog.md`, and an optional cover letter.
- One appended `Pipeline/Activity_Log.md` entry.
- A final list of created or changed files and unresolved `[TBD]` items.

## Edge cases

- Missing or multiple master resumes: stop and ask the user which real file is canonical.
- Incomplete job description: perform only a provisional fit read and ask for the missing text before drafting.
- No grounded match for a requirement: label it as a gap. Do not manufacture a bridge.
- Unknown organization, role, date, metric, or status: ask; if still unknown, use `[TBD]` in notes and omit unsupported claims from public-facing materials.
- Existing application folder: update only after explicit approval and preserve existing history.
- Master resume format cannot be edited safely: propose an editable derived filename and format, such as `Tailored_Resume.md`, and wait for approval. Do not alter or pretend to convert the source.
- User requests more than three bullets: complete this skill's three-bullet proposal first, then offer a separately approved second pass.
- Source files disagree: surface the conflict and wait for the user to resolve it.

## Never invent

- Never invent employers, titles, dates, responsibilities, skills, tools, motivations, metrics, team size, scope, outcomes, or application status.
- Never copy a requirement from the job description into the resume unless a source proves the user has it.
- Never turn a team result into sole ownership.
- Never strengthen causation, precision, or seniority beyond the source.
- Never replace an unknown with a plausible value. Ask, use `[TBD]` in notes, or omit it.
