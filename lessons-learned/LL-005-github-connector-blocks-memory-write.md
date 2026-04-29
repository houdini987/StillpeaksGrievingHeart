# LL-005 — GitHub connector may block persistent memory writes

## Context

While working with the GitHub connector in the same conversation, an attempt to write a durable personal memory failed because the memory tool was disabled after another incompatible tool had been used.

## Gotcha / Failure Mode

The assistant may assume it can persist shortcut behavior such as `load bootstrap`, but memory writes can fail once GitHub tooling is active. If this is not recognized, future chats may not know the shortcut mapping.

## Rule Going Forward

Do not rely on persistent memory being writable from a GitHub-connected repo-maintenance conversation. Critical boot shortcuts must be encoded in repo files and/or included explicitly in the user's new-chat instruction.

## Applies To

- DM Runtime Project
- Ideation / Design Project

## Related Files

- bootstrap/PROJECT_START_PROMPTS.md
- bootstrap/BOOTSTRAP.md
