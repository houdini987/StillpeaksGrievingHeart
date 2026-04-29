# Session Open / Close Protocol

This file defines the standard commands and repo actions for opening and closing live Stillpeak's Grieving Heart sessions.

---

## Core Principle

The repo should always make it possible to answer two questions quickly:

1. Where is the party right now?
2. What actually happened at the table last time?

---

## Opening a New Session (Enhanced Behavior)

### User Command

`OPEN SESSION`

### Required Assistant Actions

When opening a session, the assistant MUST:

1. Read `bootstrap/BOOTSTRAP.md`.
2. Read `bootstrap/SESSION_STATE.md`.
3. Read `canon/CANON_MANIFEST.md`.
4. Scan the `session-logs/` directory to determine:
   - the most recent session file
   - the highest session number
5. Read the most recent session log file.
6. Read the active canon packet and segment from SESSION_STATE.

### Derived State Requirements

The assistant MUST:

- Determine the **next session number** (do not create the file yet)
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

1. Use the repo-derived next session number.
2. Build the session log using the standard structure.
3. Write the new file to `session-logs/`.
4. Update `bootstrap/SESSION_STATE.md`.
5. Confirm both writes.

---

## Mid-Session Pause Command

### User Command

`PAUSE POINT`

### Required Assistant Actions

- Update `SESSION_STATE.md`
- Do NOT create a new session log

---

## Critical Rules

- Session numbering MUST be derived from repo, never memory
- SESSION_STATE MUST reflect repo truth, not chat assumptions
- OPEN SESSION = read-only
- CLOSE SESSION = write + persist

---

## Cross-Project Rules

- DM Runtime writes session logs and SESSION_STATE
- Ideation reads but does not modify them

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
