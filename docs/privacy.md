# Privacy and your data

Career OS is private by default. Keep your working copy on your computer unless you deliberately choose another private storage location.

Never put a personal Career OS in a public repository.

## What the public template contains

The canonical repository should contain only reusable instructions, blank templates, documentation, modules, and clearly fictional examples. It must not contain your:

- profile or contact details
- real resume
- achievements or StoryBank
- opportunity pipeline
- applications or conversation notes
- offers or compensation details
- confidential employer or personal context

Your copy is separate from the canonical repository. The canonical repository is read-only and does not accept user contributions.

## What `.gitignore` does

The supplied `.gitignore` blocks the standard personal-data paths from Git tracking by default, including:

- `config/profile.md`
- real files in `Resume/`
- real Achievement, Pipeline, and StoryBank files
- real folders in `Applications/`
- real offer and notes files
- everything in `Private/` except its public explanatory README

Tracked `.example` files, `_TEMPLATE` paths, documentation, and reusable modules remain available.

This is a safety net, not a data vault. It does not encrypt files, control other backup software, remove files that were already tracked, or protect a file copied to an unignored location.

## What `.gitignore` does not do

**`.gitignore` protects against GitHub upload. It does not protect your data from AI vendor processing.**

A file-capable assistant must read the information you authorize it to use. Its provider may process that content under the provider's terms, account settings, retention rules, and organizational policies. Career OS cannot control those systems.

Before using personal, employer-confidential, health, financial, immigration, or other sensitive information:

1. Read the provider's current privacy and retention terms.
2. Check whether your employer allows that tool and data type.
3. Grant access only to the Career OS folder, not your whole computer.
4. Store only the minimum detail needed.
5. Put highly restricted context in `Private/` and tell the assistant when it must not use it in shareable output.
6. Review every document before sending it to another person.

Do not place secrets such as passwords, access keys, government identification numbers, or full financial account numbers in Career OS.

## First-save check

Before an assistant writes the first real personal detail, it should ask:

> This is your private copy. Real details stay on your computer and out of any public repository. Is it OK to save them here?

This check establishes intent. It is not permission to publish anything.

## Check that personal files are ignored

If your tool can run Git commands, ask:

```text
Without changing files, check whether my personal Career OS paths are ignored
by Git. List any personal path that could be tracked.
```

You can also ask it to inspect `git status` before any Git action. If a personal file appears, stop and fix `.gitignore` before continuing.

## Optional private backup

You do not need GitHub to use Career OS. A local folder is the default.

If you knowingly choose GitHub as a backup:

1. Create a new repository in your own account.
2. Set its visibility to **Private** before uploading anything.
3. Verify the repository page shows **Private**.
4. Confirm the people and applications with access.
5. Make that private repository the destination for your personal copy. A clone
   of Career OS initially points at the public canonical repository and must
   never be used as a personal-data destination.
6. Decide exactly which personal paths the private backup should contain.
   Personal paths are ignored by default, so a normal push intentionally backs
   up only the public template files.
7. Ask the assistant to show any proposed private-copy-only `.gitignore` and
   remote changes without applying them.
8. Review `git remote -v`, `git status`, and the exact file list.
9. Approve and upload only after every destination and file is correct.

Do not broadly force-add ignored files. A mistaken destination can publish the
same files the default rules are designed to protect. A safe prompt is:

```text
Help me set up a private backup for this Career OS. First verify that the
destination repository is private. Show me the proposed remote and .gitignore
changes, plus every personal file that would be included. Do not change or
upload anything until I approve. Never push personal data to the canonical
Career OS repository.
```

Repository privacy can later be changed by an owner or administrator. Organization policies and connected applications may also grant access. A private repository is controlled access, not a promise that no service processes the content.

Consider an encrypted local backup instead if online storage is not appropriate. Use a backup method you understand and can restore.

## If personal data was uploaded

1. Make the repository private immediately, if you control it.
2. Remove the exposed files from the current version.
3. Assume prior versions may still contain the data.
4. Rotate any exposed secrets.
5. Follow the hosting provider's instructions for removing sensitive data from history.
6. Contact the relevant provider or administrator when required.

Deleting a local file or adding it to `.gitignore` does not remove an earlier uploaded copy.
