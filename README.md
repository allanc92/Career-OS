# Stop re-explaining your career to AI.

Career OS is a personal career context engine: a folder your AI assistant can use to remember your real experience, track your search, prepare you for interviews, and help with applications and offers.

Set it up once, keep adding to it, and stop starting every conversation from a blank page.

## AI that won't invent your career

Career OS tells your assistant to work from facts in your files. If a fact is missing, it asks. It does not fill gaps with plausible-sounding claims, so unsupported details do not end up in a resume or interview answer.

You do not need to know how to code, use Git, or work in a terminal. You only need to open a folder and paste a message.

## What you need

The full experience requires an AI tool that can **read AND write a folder**. Reading lets it understand your career. Writing lets it keep your profile, wins, stories, applications, and pipeline current.

A plain chat page cannot keep this folder updated. ChatGPT on the web, Claude.ai chat, and Gemini chat are not the setup described here. Use a file-capable desktop, editor, or terminal agent instead.

| Tool | Reads a folder | Writes back | Best fit |
| --- | :---: | :---: | --- |
| Claude Cowork | Yes | Yes | You want a desktop tool and no terminal |
| Claude Code | Yes | Yes | You are comfortable opening a terminal |
| GitHub Copilot | Yes, in agent mode | Yes, in agent mode | You use a supported editor or Copilot CLI |
| OpenAI Codex | Yes, in its local agent | Yes, in its local agent | You want a terminal-based agent |
| Cursor | Yes, with the folder open | Yes, in agent mode | You want an AI-first editor |
| Gemini CLI | Yes | Yes | You want a terminal-based Google agent |
| Windsurf | Yes, with the folder open | Yes, with Cascade | You want an AI-first editor |

Product features and plans change. The brand is not the requirement. The test is simple: can the tool read and write files in a folder you choose? Use a paid or free option you already trust.

See [Using Career OS with agents](docs/using-with-agents.md) for tool-specific steps.

## Get the files

Choose either path. They are equal ways to get the same folder.

### Path A: Ask a cloning tool to get the folder

Use this with Claude Code, GitHub Copilot, OpenAI Codex, Cursor, Gemini CLI, Windsurf, or another tool that can clone a repository. Paste:

```text
Clone https://github.com/allanc92/Career-OS to my computer.
Then open that folder, read AGENTS.md and ONBOARDING.md, and start onboarding me.
```

The tool may ask where to save the folder or for permission to use files. Approve only the Career OS folder.

### Path B: Download the folder

Use this with Claude Cowork or any file-capable tool that opens an existing folder.

1. Open [https://github.com/allanc92/Career-OS](https://github.com/allanc92/Career-OS).
2. Select the green **Code** button.
3. Select **Download ZIP**.
4. Open the downloaded ZIP file and extract it.
5. In your AI tool, open or grant access to the extracted `Career-OS` folder.
6. Paste:

```text
Read AGENTS.md and ONBOARDING.md in this folder, then start onboarding me.
Interview me to set up my Career OS.
```

## Your copy is private and yours to own

This repository is a read-only template. Copy the files, then make your copy your own. You cannot push personal changes to the canonical repository, and it does not accept user contributions.

Keep your personal Career OS on your computer by default. Never put a personal Career OS in a public repository. If you later choose an online backup, use a repository that you have verified is private and understand that this is an optional choice, not a setup step.

Before saving your first real details, your assistant should confirm:

> This is your private copy. Real details stay on your computer and out of any public repository. Is it OK to save them here?

Read [Privacy and your data](docs/privacy.md) before adding sensitive information.

## The onboarding interview

Onboarding is intentionally thorough. It is not a quick form. Your assistant asks about:

- your career arc and the path that brought you here
- the work that interests and energizes you
- strengths, skills, values, and constraints
- accomplishments and the evidence behind them
- roles, organizations, and directions you may want next
- your natural writing voice and phrases to avoid
- the master resume that grounds your employment and education facts

Your answers become `config/profile.md`, your first achievement entries, and early StoryBank material. Your assistant shows proposed content for approval before saving it.

Depth is a feature. Rich context helps the assistant reason about fit, write in your voice, and ask better follow-up questions. Onboarding is still only a starting point. Your interests, goals, wins, and stories can change, and Career OS becomes more useful as you update it.

## Your master resume

Put your complete current resume in `Resume/`. It is the canonical source for roles, dates, education, and other experience facts, and it is the starting point for every job-specific resume. See [Resume setup](Resume/README.md).

A tailored resume is an output for one opportunity. It does not replace the master.

## How the StoryBank compounds

`Interview_Prep/StoryBank.md` is the trusted collection of your strongest accomplishment stories in Situation, Task, Action, Result form.

1. **Seed:** onboarding turns your first wins into story outlines.
2. **Develop:** the StoryBank builder asks for missing facts and strengthens each outline without inventing details.
3. **Track:** `Interview_Prep/StoryBank_Pipeline.md` shows which stories need work and which are ready.
4. **Use:** application and interview workflows choose relevant, verified stories.
5. **Improve:** after a conversation, your own written notes can reveal useful details or gaps. Approved updates make the story stronger next time.

The result is consistent evidence across resumes, letters, interview preparation, and answers.

## Everyday prompts

Open your Career OS folder in the same file-capable tool, then ask naturally:

```text
I just finished an important project. Ask me the questions needed to log it as a win.
```

```text
Here is a job description: [paste it]. Assess the fit and help me apply.
```

```text
I have an interview with [organization] for [role]. Build a preparation plan from my real StoryBank.
```

```text
Here are my written notes from today's conversation: [paste them]. Update the relevant application and pipeline after showing me the changes.
```

```text
Where does my job search stand? Run my weekly review.
```

```text
My goals have changed. Interview me about the change and propose updates to my profile.
```

## What is in the folder

| Path | Purpose |
| --- | --- |
| `AGENTS.md` | The main operating instructions for file-capable AI tools |
| `ONBOARDING.md` | The first-run interview |
| `config/profile.md` | Your private professional context, created during onboarding |
| `Resume/` | Your private master resume and tailored resume work |
| `Achievements/` | Your running record of verified wins |
| `Pipeline/` | Opportunity status history |
| `Applications/` | One private folder per real application |
| `Interview_Prep/` | StoryBank, preparation, and optional role modules |
| `Offers/` | Private offer analysis |
| `Notes/` | Your own written notes |
| `Private/` | Confidential context that must stay local |
| `.agent/skills/` | Reusable workflows your assistant can follow |
| `examples/` | Fictional examples, never your personal data |

## Learn more

- [Why Career OS works](docs/philosophy.md)
- [Customize it for your career](docs/customizing.md)
- [Privacy and your data](docs/privacy.md)
- [Set up your AI tool](docs/using-with-agents.md)

## Share feedback

Trying Career OS in a real job search? [Leave a comment in the feedback
thread](https://github.com/allanc92/Career-OS/discussions/1), or [start a new
idea](https://github.com/allanc92/Career-OS/discussions/new?category=ideas).
Share what worked, what felt confusing, and what would make the system more
useful. Do not post your resume, application materials, employer-confidential
information, or other personal career data.

## License and contributions

The reusable template is available under the [MIT License](LICENSE). Your personal data remains yours.

The canonical repository is published as a read-only template and does not
accept code contributions. Feedback is welcome through Discussions. See
[CONTRIBUTING.md](CONTRIBUTING.md).
