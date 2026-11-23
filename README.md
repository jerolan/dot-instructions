Give Dot this repository through an authorized connection and paste this request:

```text
Dot, use the guided personalization interview in README.md in the repository I
just gave you. Ask one group of questions at a time and wait for my answers.
Leave skipped choices unset. Do not run delegation tools or probe trackers or
wikis during the interview. Propose a private absolute SOUL.md path and show me
what you would save. Wait for my approval before writing or loading anything.
After approval, follow the setup steps. Resolve all three placeholders in a
private copy of Instructions.template before loading that copy.
```

# Dot instructions

## Set up Dot

Run setup only when the user explicitly requests it.

1. **Run the interview.** Use the questions below in order. Announce the proposed `SOUL.md` path and show the draft before asking for approval to save it and load the rendered instructions.
2. **Prepare `SOUL.md`.** Use the blank template below only if the file does not exist. Preserve existing content and add only authorized details. Keep private settings and secrets out of this repository. If the host cannot read the external file, leave private context unavailable. Do not bypass access controls or move the file to a shared location.
3. **Render a private copy.** In a copy of [`Instructions.template`](Instructions.template), replace `<SOUL_DIRECTORY>` with the approved absolute directory without a trailing slash, `<DOT_ISSUE_TRACKER>` with the one approved personal tracker locator, and `<PRIORITY_REVIEW_SCHEDULE>` with the approved days or custom pattern, frequency, clock times, and time zone. Use `request only (manual; no automation)` as the schedule value only if the user explicitly chooses manual review. Check that no placeholders remain before loading. If any required answer is missing, name it as pending and wait rather than loading a partial copy. Keep all three tagged blocks. Leave all placeholders in the repository template and do not commit the rendered copy.
4. **Load the rendered copy.** Use the host's supported instruction-file setting or paste the rendered text into its supported instructions field so it loads in fresh sessions. Neither the repository nor the template is auto-discovered. If Dot cannot load the copy, tell the user exactly where to load or paste it. The rendered copy already contains the pointer. Do not add a separate pointer or edit the instructions after loading to add one.
5. **Verify the tracker and review schedule.** Once the user authorizes setup, use the host's supported tooling to verify that the tracker connector can read the exact personal tracker recorded in `SOUL.md` and rendered in the instructions. If the user authorizes automation and tracker access is verified, configure the approved recurrence through the supported scheduler. Read back the scheduler configuration. Confirm that the recurrence, local clock times, and time zone match the approved schedule and that the scheduled checks use that same tracker. For manual review, verify tracker access without creating automation. If tooling or access is unavailable, name the specific pending item and why it could not be verified. Do not report it as complete or switch to manual review without the user's choice.

## Guided personalization interview

Ask one group at a time. Accept "skip" and leave unspecified fields unset. Do not write files or change settings while collecting answers.

1. **Identity and boundaries.** "What should I call you, and which role or responsibilities should I know about? How should I report progress? Which sources can I use, and for what? What should stay private, and which actions need your approval?" Do not ask for credentials or tokens.
2. **Delegation by environment.** "Where should I delegate nontrivial work? For each environment, which tool have you chosen? How should I invoke it: through a named host integration or a command you supply? If you already have a preferred profile, what is its name?" OpenCode and Codex are examples, not defaults. Do not choose a tool or profile for the user, chase skipped answers, or run setup tests. Report inability only after an actual attempt to use the tool for authorized work.
3. **Personal Dot tracker.** "Which one personal tracker should I use for Dot's own work? What is its name, and what is its URL or other exact locator?" Explain that only its **In Progress** cards count toward Dot's cap of three. Project Jira or GitHub trackers stay separate. Use them only when the project's local `AGENTS.md` or equivalent guidance calls for it and the task authorizes it. Do not register them in `SOUL.md` or count them toward Dot's limit.
4. **Priority review schedule.** "Which days or custom pattern should I use for priority checks? How often and how many checks should I run? At what local clock times and in which time zone? Or do you want manual checks on request with no automation?" Do not assume any days, frequency, times, or time zone. A skipped answer is not a choice of manual review.
5. **Wiki roots.** "Which wikis, if any, should I consult? For each one, what is its name, scope, root path, and index path? Is it private or shared, and who is the intended audience?" Keep private and shared roots separate. Each root has its own index. Record pointers, not copies of wiki pages.
6. **Projects.** "Which projects, if any, should I know about? For each one, what's its name, scope, and path? Is there project guidance I should know where to find?" Follow the project's local `AGENTS.md` or equivalent when working there. Do not copy project instructions or tracker configuration into `SOUL.md`.
7. **Private `SOUL.md` location.** Choose a private absolute directory outside this repository that Dot can reach through supported host access. State the full proposed path and ask the user to confirm or replace it. For example: "I propose `/home/example/.config/dot/SOUL.md`. Should I use that path or a different one?" Use the confirmed path when you ask for approval to save.
8. **Review before saving.** Show the proposed path and the `SOUL.md` draft or additions. Note what will stay unset and what belongs elsewhere. Accept corrections and wait for approval before continuing setup.

## Fill in `SOUL.md`

Leave unused optional fields blank. Repeat the wiki and project entries as needed, or omit either section. Keep private and shared wiki roots separate. Each wiki has its own index. Record the one personal Dot tracker and the approved priority review schedule, or the explicit manual choice. Read project-local guidance such as `AGENTS.md` for project work.

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
- Priority review schedule or explicit manual choice:

## Orchestrators

- Environment:
  - User-declared orchestrator for nontrivial work:
  - Invocation:
  - Preferred profile (optional):

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

### Fictional example

Here's how Dot would map a fictional user's answers to `SOUL.md` and the rendered instructions. Do not use these values as defaults.

| User's answer | Where it goes |
| --- | --- |
| "I'm Rowan, release coordinator. Lead with blockers. Use the team runbook for release questions. Ask before posting externally." | **Personal context:** identity and role, reporting preference, trusted source and scope, and approval boundary. |
| "On my laptop, use OpenCode through the host integration named Local OpenCode with my Review profile. Skip the remote workspace." | **Orchestrators:** laptop → OpenCode, Local OpenCode integration, Review profile. The remote workspace stays unset. |
| "Use my Dot Board at `https://tracker.example/dot`. Harbor uses Jira." | **Dot work tracker:** Dot Board and its URL. Replace `<DOT_ISSUE_TRACKER>` with that URL. Only Dot Board's **In Progress** cards count toward the cap of three. Harbor's Jira stays in project guidance. |
| "Check twice each Tuesday, Thursday, and Saturday at 08:30 and 15:45 in `America/Mexico_City`." | **Priority review schedule:** Record this in `SOUL.md` and replace `<PRIORITY_REVIEW_SCHEDULE>` with `Tuesdays, Thursdays, and Saturdays at 08:30 and 15:45 America/Mexico_City (two checks per review day)`. |
| "Personal Notes is for my planning only, at `/home/example/private/notes`. Release Runbook is for the release team, at `/srv/team/releases`. Both use `index.md` at the root." | **Wikis:** Personal Notes (private planning), `/home/example/private/notes` with `/home/example/private/notes/index.md`. Release Runbook (shared release guidance), `/srv/team/releases` with `/srv/team/releases/index.md`. |
| "Harbor handles release tooling at `/home/example/src/harbor`. Follow its `AGENTS.md`." | **Projects:** Harbor, release tooling, `/home/example/src/harbor`. Read `AGENTS.md` there when working on Harbor. |
| "Yes, use `/home/example/.config/dot/SOUL.md`." | **Rendered instructions:** replace `<SOUL_DIRECTORY>` with `/home/example/.config/dot` before loading. The path is not a separate `SOUL.md` entry. |

Leave credentials, wiki contents, project instructions, and project tracker settings out of `SOUL.md`. Keep real answers and the rendered copy out of this repository.

## Check a fresh session

Start a new session without pasting the instructions or supplying the private path again. Ask Dot:

```text
Without writing anything, tell me which tracker counts toward your
work-in-progress limit, what that limit is, and whether you can read
SOUL.md from its configured pointer. Do not quote the path or contents.
```

Expect Dot to name only its designated work tracker and a cap of three **In Progress** cards. If the pointer is missing or still contains the placeholder, Dot tells you once to request explicit setup. If the configured file is missing or unreadable, restore the file or its access. Dot does not recreate the file or rerun setup automatically. This check does not invoke an orchestrator or modify a tracker or wiki.

## Update Dot

Make personal edits in `SOUL.md`, not in the loaded instructions. To change the pointer, tracker, or review schedule, or to adopt a template revision, deliberately render a fresh copy from `Instructions.template` and update the host's instructions with that copy. Verify any authorized tracker or scheduler changes as in setup. Do not make ad hoc edits to the loaded instructions during a session.
