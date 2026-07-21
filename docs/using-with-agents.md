# Using Career OS with AI agents

Career OS needs a tool that can read AND write files in one folder. You do not need to write code.

## The capability check

Before setup, confirm all three:

1. The tool can open or work inside a local folder.
2. The tool can read several files in that folder.
3. The tool can create and update files in that folder with your approval.

A plain web chat is not enough. Uploading a few files to ChatGPT, Claude.ai chat, or Gemini chat does not give the assistant a persistent folder it can maintain.

## Two equal ways to get Career OS

### Ask a cloning tool

Use this with a local tool that supports cloning:

```text
Clone https://github.com/allanc92/Career-OS to my computer.
Then open that folder, read AGENTS.md and ONBOARDING.md, and start onboarding me.
```

### Download ZIP

1. Open [the canonical Career OS repository](https://github.com/allanc92/Career-OS).
2. Select **Code**, then **Download ZIP**.
3. Extract the ZIP.
4. Open or share the extracted `Career-OS` folder with your file-capable tool.
5. Paste:

```text
Read AGENTS.md and ONBOARDING.md in this folder, then start onboarding me.
Interview me to set up my Career OS.
```

Neither path changes the canonical repository. You are creating a private copy you own.

## Tool compatibility

| Tool | Required mode | Reads folder | Writes folder | Get-files path |
| --- | --- | :---: | :---: | --- |
| Claude Cowork | Cowork in Claude Desktop with folder access | Yes | Yes | Download ZIP |
| Claude Code | Run in the Career OS folder | Yes | Yes | Clone |
| GitHub Copilot | Agent mode in a supported editor, or Copilot CLI | Yes | Yes | Clone |
| OpenAI Codex | Local Codex agent in the Career OS folder | Yes | Yes | Clone |
| Cursor | Folder open, Agent mode | Yes | Yes | Clone or Download ZIP |
| Gemini CLI | Run in the Career OS folder | Yes | Yes | Clone |
| Windsurf | Folder open, Cascade | Yes | Yes | Clone or Download ZIP |

These are examples, not a permanent allowlist. Features, names, and plans change. Check the tool's current documentation if its interface differs.

## Claude Cowork

1. Download and extract the ZIP.
2. Open Claude Desktop and start Cowork.
3. Grant Cowork access to the extracted `Career-OS` folder only.
4. Paste the onboarding message.
5. Review file changes before approving them.

Cowork folder access is different from a normal Claude.ai chat.

## Claude Code

Ask Claude Code to clone the canonical URL, or clone it with a tool you already use. Start Claude Code inside the resulting folder and paste the onboarding message. If asked to trust the folder or approve file access, review the path first.

## GitHub Copilot

Open the folder in an editor with Copilot agent mode, or run Copilot CLI from the folder. Use agent mode, not suggestion-only completion and not a web chat. Paste the onboarding message and approve only expected file operations.

## OpenAI Codex

Use the local Codex agent in the Career OS folder. Ask it to clone the canonical URL if needed, then paste the onboarding message. Confirm its workspace is the private copy before allowing writes.

## Cursor

Clone the canonical URL or download and extract the ZIP. Open the folder in Cursor, choose Agent mode, and paste the onboarding message. Review proposed edits in Cursor before accepting them.

## Gemini CLI

Ask Gemini CLI to clone the canonical URL, then run it from the Career OS folder. Paste the onboarding message. Gemini's normal web chat is not a substitute for Gemini CLI folder access.

## Windsurf

Clone the canonical URL or download and extract the ZIP. Open the folder in Windsurf and use Cascade. Paste the onboarding message and review edits before accepting them.

## What a correct first run looks like

The assistant should:

1. Read `AGENTS.md` and `ONBOARDING.md`.
2. Explain that your copy is private.
3. Ask before saving the first real detail.
4. Run the full onboarding interview rather than a short setup.
5. Ask for your master resume.
6. Explain and seed the StoryBank.
7. Show proposed content before writing.
8. Remind you that the system keeps growing.

If the assistant starts inventing details, writing without approval, or skipping the interview, say:

```text
Stop. Re-read AGENTS.md and ONBOARDING.md. Use only facts I provide, ask about
anything missing, and show proposed changes before saving.
```

## Everyday use

Always open the same Career OS folder. Then use requests such as:

```text
Capture a new win. Ask me for the result and evidence before writing.
```

```text
Use my master resume and StoryBank to assess this role: [paste job description].
```

```text
Prepare me for my next interview using only verified stories.
```

```text
Use my written notes to update this application after showing me the changes.
```

```text
Run my weekly career review and tell me what needs attention.
```

For data boundaries and optional backup guidance, read [Privacy and your data](privacy.md).
