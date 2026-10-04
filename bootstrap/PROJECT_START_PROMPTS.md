# Project Start Notes

This file intentionally does not contain long copy-paste prompts.

## Claude Code (current)

Open the repo folder in Claude Code. `CLAUDE.md` loads automatically.

- `/dm`: DM Runtime mode. `load bootstrap` is equivalent to invoking `/dm` without opening a session.
- `/ideate`: Ideation / Design mode.

The skill definitions live in `.claude/skills/dm/SKILL.md` and `.claude/skills/ideate/SKILL.md`.

## Legacy chat-project shortcut

The preferred shortcut for a chat-based DM Runtime Project was:

`load bootstrap`

When the user says `load bootstrap`, the assistant should resolve that as:

- Repo: `houdini987/StillpeaksGrievingHeart`
- Mode: DM Runtime Project
- Action: read the Stillpeak bootstrap stack according to `bootstrap/BOOTSTRAP.md`
- Constraint: do not open a session unless the user explicitly says `OPEN SESSION`

For the Ideation / Design Project, the user should explicitly say they want ideation/design mode or provide an equivalent instruction.

## Durable rules

This file is only a reminder of the intended shortcut behavior. The durable operating rules live in:

- `bootstrap/BOOTSTRAP.md`
- `bootstrap/PROJECT_ROLES.md`
- `bootstrap/SESSION_PROTOCOL.md`
- `LESSONS_LEARNED.md`
