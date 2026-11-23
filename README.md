# Dot Instructions

Use [AGENTS.md](AGENTS.md) for reusable ways of working. Keep identity, preferences, and private destinations in an external `SOUL.md` that you configure. The defaults in this repository describe no particular person.

## Set up your agent

1. Choose an explicit location for `SOUL.md` outside this repository. Copy the blank template there and restrict access to the people and tools you intend to use it. Leave the file unconfigured if you do not need personalized context.
2. Choose private destinations for personal records and private wiki content. If you use shared wiki roots, register them separately. Give each root its own `index.md` and record that index's location in `SOUL.md`. The registry points to the indexes. It is not a global index of their contents.
3. Review what the target agent harness will receive. Remove secrets and anything that should not reach that harness or the audience of its outputs. Paste only the instructions you intend it to use. If it needs `SOUL.md`, configure an explicit pointer and grant only the access it needs. Point to an optional machine profile from `SOUL.md`, not from these generic instructions.
4. Start a fresh session and verify that the intended instructions are active with a harmless behavior check. If you configured a private pointer, check that the session can read the intended file without quoting private contents. Confirm the selected destination before any real write. If loading or access fails, treat the private context as unavailable until you fix the configuration.

## Configure Dots manually

Dots do not automatically load this repository's `AGENTS.md` or your external `SOUL.md`. Paste only the instructions intended for the Dot into its configuration. If it needs an external file, configure the pointer manually and verify that the Dot has explicit access. If the Dot cannot reach the private file, leave that context unavailable rather than moving the file to a shared place.

## Blank `SOUL.md` template

Copy this block into your external private file. Leave unused fields blank and repeat the wiki root block for each authorized root. The optional machine profile can be an explicitly selected file in a private directory or a profile file in a private wiki. Nothing discovers it automatically.

```markdown
# SOUL

## Personal context

- Identity and role:
- Preferences:
- Workflows:
- Destinations and intended audiences:

## Boundaries

- Trusted sources and their scope:
- Permissions and actions that need approval:
- Private and shared separation rules:

## Wiki root registry

### <root label>

- Location:
- Scope:
- Visibility (private or shared):
- Access rules (read, write, share):
- Location of this root's `index.md`:

## Optional machine profile

- Explicit pointer to the selected private profile file:
```

## Attribution

These instructions are a reusable, paraphrased adaptation, not the original upstream text. Matt Pocock's chief-of-staff guidance inspired the approach to coordination. `i-have-adhd` inspired the readability defaults.
