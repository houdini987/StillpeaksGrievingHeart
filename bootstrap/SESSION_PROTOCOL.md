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

---

## Closing a Session

### User Command

`CLOSE SESSION`

### Required Assistant Actions

When closing a session, the assistant MUST:

1. Use the repo-derived next session number from `session-logs/LATEST_SESSION_LOG.md`.

2. Build the session log with BOTH layers:

   **Play-by-Play Layer (required):**
   - Scene-organized sequence of player actions and outcomes
   - Capture meaningful decisions, interactions, checks, and activations
   - Include tactical setups that impact future play
   - Do NOT include fluff narration or full dialogue transcripts

   **State Summary Layer (required):**
   - Location (packet, segment, position)
   - Completed beat/segment and new current beat/segment
   - Party condition and level
   - Tactical carryovers
   - Gained or missed items/clues
   - Deviations from canon
   - Immediate next beat

3. Write the new file to `session-logs/`.

4. Update `session-logs/LATEST_SESSION_LOG.md` to point at the new file.

5. Update `bootstrap/SESSION_STATE.md` so it reflects the live baseline for the NEXT session, not the start of the session that just ended.

6. Cross-check consistency:
   - `SESSION_STATE.md`
   - `LATEST_SESSION_LOG.md`
   - New session log

   All must agree on:
   - packet
   - segment
   - position
   - party level
   - condition
   - immediate next beat

7. Confirm all writes. If anything is uncertain, flag it instead of guessing.

---

## Close-Session State Advancement Rule

`CLOSE SESSION` must advance repo state to the party's actual ending position.

If the party completed a segment or beat during play:
- Move `SESSION_STATE.md` forward to the new current beat/segment

Do NOT leave state pointing at the session’s starting beat unless that is where the party actually ended.

---

## Mid-Session Pause Command

### User Command

`PAUSE POINT`

### Required Assistant Actions

- Update `SESSION_STATE.md`
- Do NOT create a new session log
- Do NOT update `LATEST_SESSION_LOG.md` unless a new session log is created

---

## Critical Rules

- Session log discovery MUST use `session-logs/LATEST_SESSION_LOG.md`
- NEVER scan directories or rely on search
- Session numbering MUST be derived from the pointer
- SESSION_STATE MUST reflect repo truth, not chat assumptions
- OPEN SESSION = read-only
- CLOSE SESSION = write + persist
- CLOSE SESSION must advance state to the next live baseline

---

## Cross-Project Rules

- DM Runtime writes session logs, LATEST_SESSION_LOG, and SESSION_STATE
- Ideation reads and analyzes, does not mutate state unless explicitly asked

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
