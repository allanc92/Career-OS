# Customize Career OS

Career OS is a read-only template that you copy and own. Customize only your private copy. The canonical repository does not accept personal changes.

No code knowledge is required. These are ordinary folders and Markdown files. Markdown is plain text with simple headings and lists.

## Start with the onboarding interview

Let onboarding create `config/profile.md`, seed your achievements and StoryBank, and connect your master resume. Do not rush this step. Career OS works better when it understands your career arc, interests, energy, evidence, voice, goals, and constraints.

Then make small changes as real needs appear.

## Change your profile

Ask:

```text
Read config/profile.md. Interview me about what has changed, then show proposed edits before saving.
```

Useful updates include:

- a new target role or direction
- work you want more or less of
- location, schedule, or compensation constraints
- strengths you have better evidence for
- words or tones that do not sound like you

Keep facts concrete. Use `Not decided` or `Unknown` instead of guessing.

## Adapt it to any field

The core system is role-agnostic. A nurse, designer, salesperson, researcher, teacher, tradesperson, operator, or executive can use the same profile, achievement, pipeline, resume, and story structure.

Field-specific material belongs in an optional module under `Interview_Prep/modules/`. A module may contain:

- common interview themes
- role-specific practice prompts
- evaluation rubrics
- terminology or portfolio guidance
- questions to ask an employer

The included `pm-tech` module is only an example. If it is not relevant, delete that module from your private copy. Nothing in the core system should depend on it.

To create a module, ask:

```text
Create a private interview-prep module for [field or role].
First ask what interview formats and skills matter. Reuse the structure of
Interview_Prep/modules/pm-tech only as a structural example. Show the plan
before writing files, and do not invent requirements.
```

## Add a folder only when it has a clear owner

Before adding a new area, decide:

1. What question does this folder answer?
2. Which file is its source of truth?
3. When should the assistant update it?
4. Is it personal and therefore covered by `.gitignore`?
5. Does it duplicate an existing file?

Prefer a few dependable sources over many overlapping documents.

## Change a workflow

Reusable workflows live in `.agent/skills/`. Tell the assistant what outcome or approval step should change. Preserve these rules:

- use real sources and ask about missing facts
- show consequential drafts before saving
- append history rather than erasing it
- keep personal output private
- use only the user's own written notes about conversations

Example:

```text
Read AGENTS.md and the weekly-review skill. Propose a new weekly review section
for networking follow-ups. Explain which source file it uses. Wait for my
approval before changing the skill.
```

## Keep custom files private

The supplied `.gitignore` is designed to ignore real profile, resume, achievement, pipeline, StoryBank, application, offer, notes, and Private content while allowing examples, templates, modules, and documentation.

If you add a new personal-data path, update `.gitignore` before adding real data. Check with:

```text
Review .gitignore and confirm that [new path] cannot be added to Git.
Do not change any files yet.
```

Never publish a personal Career OS in a public repository. For backup choices, read [Privacy and your data](privacy.md).
