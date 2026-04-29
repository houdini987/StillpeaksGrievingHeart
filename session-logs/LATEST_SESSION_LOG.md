# Latest Session Log Pointer

This file exists so AI projects can deterministically locate the latest session log even when connector search or directory listing is unavailable.

- Latest session log: `session-logs/SESSION_04.md`
- Status: pointer must be updated whenever a newer session log is created.

If this pointer disagrees with `bootstrap/SESSION_STATE.md`, stop and flag the mismatch before runtime use.
