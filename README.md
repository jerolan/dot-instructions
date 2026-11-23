Give Dot this repository through an authorized connection and paste this request:

```text
Dot, follow README.md in the repository I just gave you and configure yourself.
```

# Dot instructions

## Set up Dot

1. **Load the instructions.** Only run setup when the user explicitly requests it. Use a host-supported instruction-file setting to load [`Instructions.template`](Instructions.template) explicitly, or paste its raw text into the host's supported instructions field. Keep all three tagged blocks. Neither the repository nor the template is auto-discovered. If Dot cannot change its instructions, tell the user where to load or paste them.
2. **Propose the private file.** Before creating `SOUL.md`, announce the proposed path outside this repository and give the user a chance to choose another path. Use a private location that the intended Dot can reach through supported access. Start from the blank template below only if the file does not exist. Preserve existing content and add only authorized details. Keep private settings and secrets out of this repository.
3. **Save the pointer.** In a supported profile or setting that loads in fresh sessions, persist an explicit instruction such as `Read SOUL.md at <private path> when the session starts.` If Dot cannot save it, give the user the exact pointer to add and the supported place to add it. If the host cannot read the external file, leave private context unavailable. Do not bypass access controls or move the file to a shared location.

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

Start a new session without pasting the template or supplying the private path again. Ask Dot:

```text
Without writing anything, tell me which tracker counts toward your
work-in-progress limit, what that limit is, and whether you can read
SOUL.md from its configured pointer. Do not quote the path or contents.
```

Expect Dot to name only its designated work tracker and a cap of three **In Progress** cards. If the pointer or file is missing or unreadable, Dot tells you to configure `SOUL.md` or restore access. It does not recreate the file or rerun setup. This check does not invoke an orchestrator or modify a tracker or wiki.
