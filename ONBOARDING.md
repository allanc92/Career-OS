# Build your Career OS

Your first session is a guided interview, not a form and not a quick setup.
The goal is to give your assistant enough grounded context to understand the
shape of your career: where you have been, what you are good at, what energizes
you, what you want next, and how you naturally communicate.

More context can always be added later. This interview builds a strong
foundation, and Career OS keeps improving as you capture new wins, stories,
interests, and decisions.

## Start here

Open this folder in a file-capable AI assistant, then paste:

```text
Read AGENTS.md and ONBOARDING.md. Follow the onboarding-interview skill and
start onboarding me. Ask one focused question at a time.
```

The assistant must read:

1. `AGENTS.md`
2. `.agent/skills/onboarding-interview/SKILL.md`
3. the public `.example.md` schemas it will use
4. any existing private onboarding files, if this is a resumed session

Files under `examples/` describe a fictional person. They are never facts about
you.

## What to expect

The interview covers:

1. Privacy and permission to save personal details
2. Your background, career arc, and turning points
3. Work that energizes you, interests, values, and best-work conditions
4. Strengths, accomplishments, evidence, and stories
5. Target directions, constraints, and decision criteria
6. Your writing voice and communication preferences
7. Your master resume
8. A review of everything before files are created or changed

The assistant asks follow-up questions when a detail matters. It never invents
an employer, title, date, skill, motivation, result, or metric. If something is
unknown, it asks or records `[TBD]`.

## Your master resume

Your master resume is the starting point for every role-specific resume. During
onboarding, you can:

- place an existing resume in `Resume/`
- paste its text for the assistant to organize
- ask the assistant to build `Resume/Master_Resume.md` from facts confirmed in
  the interview

Markdown or plain text is the most reliable format. A file-capable assistant
may also be able to read PDF or DOCX. If it cannot read a file reliably, it must
say so and ask you to paste or export the text. It must never pretend that a
file was read.

If you do not have a resume yet, that does not block onboarding. The assistant
can propose a first master resume from confirmed facts, mark gaps as `[TBD]`,
and wait for your approval before saving it.

## Your StoryBank

The interview also starts your StoryBank. This is the trusted collection of
your strongest accomplishment stories in Situation, Task, Action, Result form.
It lets the assistant reuse the same accurate evidence across applications and
interview preparation instead of reconstructing your career from memory.

Initial stories can remain incomplete. Missing context goes into
`Interview_Prep/StoryBank_Pipeline.md` so you can develop it over time. A story
is not filed as ready until you approve its facts and framing.

## Privacy and approval

Before the first personal detail is saved, the assistant asks:

> This is your private copy. Personal files should stay local or in your own
> private repository. Your AI provider may process content you share. OK to
> save these details?

The assistant previews every proposed personal file or change and names the
exact paths before writing. You can approve, request edits, skip a section, or
stop at any time.

## Stop and resume

Onboarding is designed to survive interruptions. After an approved phase, the
assistant records an onboarding checkpoint in `config/profile.md`. When you
return, use:

```text
Read AGENTS.md and ONBOARDING.md. Inspect my existing Career OS and resume
onboarding from the first incomplete phase. Summarize what is already complete
before asking the next question.
```

The assistant must not restart completed sections or overwrite approved
content. It should identify unresolved `[TBD]` items and continue from the next
unfinished phase.

## What onboarding creates

After you approve the proposed content, the assistant creates or updates:

- `config/profile.md`
- `Resume/Master_Resume.*`
- `Achievements/Achievement_Log.md`
- `Interview_Prep/StoryBank.md`
- `Interview_Prep/StoryBank_Pipeline.md`
- `Pipeline/Activity_Log.md`

Only relevant files are created. For example, the pipeline can remain an empty
schema if you have not shared an active opportunity.

At the end, the assistant shows what it saved, lists every remaining `[TBD]`,
and explains useful next prompts. It also reminds you that onboarding is the
beginning, not the limit, of what Career OS can learn.
