# Session Open / Close Protocol

This file defines the standard commands and repo actions for opening and closing live Stillpeak's Grieving Heart sessions.

---

## Core Principle

The repo should always make it possible to answer two questions quickly:

1. Where is the party right now?
2. What actually happened at the table last time?

---

## Opening a New Session

### User Command

`OPEN SESSION`

### Required Assistant Actions

When opening a session, the assistant MUST:

1. Read `bootstrap/BOOTSTRAP.md`.
2. Follow the bootstrap read order.
3. Read `bootstrap/SESSION_STATE.md`.
4. Read `session-logs/LATEST_SESSION_LOG.md`.
5. Read the latest session log file named by that pointer.
6. Read `canon/CANON_MANIFEST.md`.
7. Read the active canon packet and segment from SESSION_STATE.

Do not scan or list the `session-logs/` directory to discover the latest session log. The pointer file is the deterministic discovery mechanism.

### Derived State Requirements

The assistant MUST:

- Determine the **next session number** from the latest session log pointer, not memory
- Validate SESSION_STATE against the latest session log
- Detect any mismatch between SESSION_STATE and session logs

If mismatch exists, flag it immediately before continuing.

### Output (Readiness Brief)

Return a concise readiness brief:

- Current location / segment
- Party level and condition
- Immediate next beat
- Active systems
- Known deviations from canon
- Next session number (pre-calculated)

### Critical Constraint

OPEN SESSION is strictly **read-only + inference**.

It must NOT:

- create files
- modify session logs
- modify SESSION_STATE

---

## Closing a Session

### User Command

`CLOSE SESSION`

### Required Assistant Actions

When closing a session, the assistant MUST:

1. Use the repo-derived next session number from `session-logs/LATEST_SESSION_LOG.md`.
2. Build the session log using the standard structure.
3. Include current table reality: location, completed beat/segment, current beat/segment, party condition, tactical carryovers, gained/missed items, deviations from canon, and immediate next beat.
4. Write the new file to `session-logs/`.
5. Update `session-logs/LATEST_SESSION_LOG.md` to point at the new file.
6. Update `bootstrap/SESSION_STATE.md` so it reflects the live baseline for the next session, not the beginning of the session that just ended.
7. Cross-check that `SESSION_STATE.md`, `LATEST_SESSION_LOG.md`, and the newly written session log agree on packet, segment, position, party level, condition, and immediate next beat.
8. Confirm all writes and flag any unresolved uncertainty instead of silently guessing.

### Close-Session State Advancement Rule

`CLOSE SESSION` must advance repo state to the party's actual ending position. If the party completed a segment or beat during play, `SESSION_STATE.md` must be moved forward to the next current beat/segment.

Do not leave `SESSION_STATE.md` pointing at the session's starting beat unless the party actually ended there.

---

## Mid-Session Pause Command

### User Command

`PAUSE POINT`

### Required Assistant Actions

- Update `SESSION_STATE.md`
- Do NOT create a new session log
- Do NOT update `session-logs/LATEST_SESSION_LOG.md` unless a new session log is also created

---

## Critical Rules

- Session log discovery MUST use `session-logs/LATEST_SESSION_LOG.md`, never directory scan/search
- Session numbering MUST be derived from the latest session log pointer, never memory
- SESSION_STATE MUST reflect repo truth, not chat assumptions
- OPEN SESSION = read-only
- CLOSE SESSION = write + persist
- CLOSE SESSION must advance state to the next actual live-play baseline

---

## Cross-Project Rules

- DM Runtime writes session logs, LATEST_SESSION_LOG, and SESSION_STATE
- Ideation reads but does not modify them unless explicitly asked to perform repo maintenance

---

## Recommended Commands

- OPEN SESSION
- CLOSE SESSION
- PAUSE POINT
- BEAT
- CHECKS
- RULING
- TRANSITION
- NPC
