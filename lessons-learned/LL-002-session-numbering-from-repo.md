# LL-002 — Session numbering must come from repo

## Context

Session numbering was previously inferred from chat memory.

## Gotcha / Failure Mode

Chat-based numbering can drift, duplicate, or skip numbers when sessions span multiple chats or restarts.

## Rule Going Forward

Session numbering must always be derived by scanning the `session-logs/` directory in the repo.

## Applies To

- DM Runtime Project

## Related Files

- bootstrap/SESSION_PROTOCOL.md
