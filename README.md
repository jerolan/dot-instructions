Give Dot this repository through an authorized connection and paste this request:

```text
Dot, follow README.md in the repository I just gave you and configure yourself.
```

# Dot instructions

## Set up Dot

Run setup only when the user explicitly requests it.

1. **Choose a private directory.** Use an absolute directory outside this repository that Dot can reach through supported host access. Announce the chosen absolute path to `SOUL.md` before creating it. Give the user a chance to choose a different path.
2. **Prepare `SOUL.md`.** Use the blank template below only if the file does not exist. Preserve existing content and add only authorized details. Keep private settings and secrets out of this repository. If the host cannot read the external file, leave private context unavailable. Do not bypass access controls or move the file to a shared location.
3. **Render a private copy.** In a copy of [`Instructions.template`](Instructions.template), replace only `<SOUL_DIRECTORY>` with the chosen absolute directory, without a trailing slash. For example, `/home/example/.config/dot` gives `/home/example/.config/dot/SOUL.md`. Keep all three tagged blocks. Leave the placeholder in the repository and do not commit the rendered copy.
4. **Load the rendered copy.** Use the host's supported instruction-file setting or paste the rendered text into its supported instructions field so it loads in fresh sessions. Neither the repository nor the template is auto-discovered. If Dot cannot load the copy, tell the user exactly where to load or paste it. The rendered copy already contains the pointer. Do not add a separate pointer or edit the instructions after loading to add one.

Record only the orchestrator the user declares for each environment. OpenCode and Codex are examples, not defaults. Do not choose or test an orchestrator or follow up about it during setup. Report inability only after an actual attempt to use it for work.

## Fill in `SOUL.md`

Leave unused fields blank. Repeat the wiki and project entries as needed, or omit either section. Keep private and shared wiki roots separate. Each wiki has its own index. Register only the one designated Dot work tracker, not any project trackers. Read project-local guidance such as `AGENTS.md` for project work.

```markdown
# SOUL

## Personal context

- Identity and role:
- Preferences:
- Trusted sources and scope:
- Actions that need approval:

## Dot work tracker

- Name:
- Location:

## Orchestrators

- Environment:
  - User-declared orchestrator for nontrivial work:

## Wikis (optional)

- Name:
  - Scope:
  - Root path:
  - Path to this wiki's index:
  - Visibility (private or shared):

## Projects (optional)

- Name:
  - Scope:
  - Path:
```

## Check a fresh session

Start a new session without pasting the instructions or supplying the private path again. Ask Dot:

```text
Without writing anything, tell me which tracker counts toward your
work-in-progress limit, what that limit is, and whether you can read
SOUL.md from its configured pointer. Do not quote the path or contents.
```

Expect Dot to name only its designated work tracker and a cap of three **In Progress** cards. If the pointer is missing or still contains the placeholder, Dot tells you once to request explicit setup. If the configured file is missing or unreadable, restore the file or its access. Dot does not recreate the file or rerun setup automatically. This check does not invoke an orchestrator or modify a tracker or wiki.

## Update Dot

Make personal edits in `SOUL.md`, not in the loaded instructions. To change the pointer or adopt a template revision, deliberately render a fresh copy from `Instructions.template` and update the host's instructions with that copy. This keeps the loaded instructions aligned with the template. Do not make ad hoc edits to the loaded instructions during a session.
