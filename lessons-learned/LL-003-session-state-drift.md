# LL-003 — SESSION_STATE must not drift

## Context

SESSION_STATE and session logs can become inconsistent if updates are missed or done out of order.

## Gotcha / Failure Mode

The system begins operating on incorrect assumptions about location, party state, or next beat.

## Rule Going Forward

SESSION_STATE.md must always match the latest session log and confirmed table reality.

## Applies To

- DM Runtime Project
- Ideation / Design Project (read-only validation)

## Related Files

- bootstrap/SESSION_STATE.md
- session-logs/
