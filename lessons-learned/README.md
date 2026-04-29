# Lessons Learned

This folder contains shared gotchas, operating lessons, and process corrections discovered while using the Stillpeak's Grieving Heart repo across the DM Runtime Project and the Ideation / Design Project.

Both projects may contribute to this folder.

## Purpose

The lessons learned layer prevents repeated mistakes across chats, sessions, and project modes.

It should capture problems such as:

- canon/session-log confusion
- repo write or read-order mistakes
- session numbering drift
- command protocol ambiguity
- AI behavior that created friction during live play
- design/process assumptions that later proved wrong

## Boot Requirement

Every project boot should scan this folder after reading the bootstrap files and before taking action.

Recommended boot order addition:

1. `bootstrap/BOOTSTRAP.md`
2. `bootstrap/PROJECT_ROLES.md`
3. `bootstrap/SESSION_PROTOCOL.md`
4. `bootstrap/SESSION_STATE.md`
5. `lessons-learned/LESSONS_INDEX.md`
6. Relevant individual lesson files
7. `canon/CANON_MANIFEST.md`
8. Latest relevant `session-logs/` file
9. Active canon packet(s)

## Lesson Numbering

Lesson files use this naming convention:

`LL-###-short-slug.md`

Examples:

- `LL-001-open-session-is-read-only.md`
- `LL-002-session-numbering-comes-from-git.md`

Lesson numbers should never be reused.

## Lesson Format

Each lesson should contain:

1. Title
2. Context
3. Gotcha / Failure Mode
4. Rule Going Forward
5. Applies To
6. Related Files

## Contribution Rules

- Keep lessons short and operational.
- Do not turn lessons into broad design essays.
- Capture the rule that prevents the mistake from recurring.
- If a lesson affects boot behavior, update `LESSONS_INDEX.md` and relevant bootstrap/protocol files.
