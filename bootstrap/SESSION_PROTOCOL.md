# Session Open / Close Protocol

This file defines the standard commands and repo actions for opening and closing live Stillpeak's Grieving Heart sessions.

It is intended primarily for the DM Runtime Project, but the Ideation / Design Project may also read it to understand how session state is maintained.

---

## Core Principle

The repo should always make it possible to answer two questions quickly:

1. Where is the party right now?
2. What actually happened at the table last time?

`bootstrap/SESSION_STATE.md` answers the first question.

`session-logs/` answers the second question.

---

## Opening a New Session

### User Command

Recommended command:

`OPEN SESSION`

Equivalent phrasing is acceptable if the user clearly says they are starting, opening, resuming, or initiating a new live session.

### Required Assistant Actions

When opening a session, the assistant should:

1. Read `bootstrap/BOOTSTRAP.md`.
2. Read `bootstrap/SESSION_STATE.md`.
3. Read `canon/CANON_MANIFEST.md`.
4. Read the most recent relevant `session-logs/` file.
5. Read the active canon packet and segment referenced by `SESSION_STATE.md`.
6. Return a short readiness brief.

### Readiness Brief Format

The readiness brief should include:

- Current location / segment
- Party level and condition
- Immediate next beat
- Active systems or hazards
- Known deviations from canon
- One sentence confirming DM-command mode is ready

Do not over-explain unless asked.

### Optional Repo Action on Open

If the user asks for it, the assistant may create a new draft session log placeholder for the upcoming session.

Do not create a new session log automatically unless the user wants pre-session scaffolding. Session logs are normally written at close.

---

## Closing a Session

### User Command

Recommended command:

`CLOSE SESSION`

Equivalent phrasing is acceptable if the user clearly says they are ending, closing, pausing, or wrapping the live session and wants repo state updated.

### Required Assistant Actions

When closing a session, the assistant should:

1. Summarize the actual-play events from the current chat/session.
2. Identify:
   - current location
   - party condition
   - major events
   - combat outcomes
   - items/clues/boons gained or missed
   - deviations from canon
   - advancement changes
   - immediate next beat
   - pause point
3. Create the next numbered session log in `session-logs/`.
4. Update `bootstrap/SESSION_STATE.md` to match the new pause point.
5. Confirm the files written.

### Required Session Log Format

Each closeout log should use this structure:

1. High-Level Summary
2. Key Events
3. Combat Event
4. State at End of Session
5. Advancement
6. Outstanding Threads
7. Deviations from Canon
8. Pause Point

### Session Numbering

Use the next available session number in `session-logs/`.

File naming convention:

`session-###-short-descriptive-slug.md`

Examples:

- `session-005-wind-carved-spine.md`
- `session-006-shattered-moraine.md`
- `session-007-ice-locked-shelf.md`

### SESSION_STATE Update Requirements

At close, update `bootstrap/SESSION_STATE.md` with:

- packet and segment
- current location and position
- party level
- party condition
- recent events
- known deviations from canon
- active systems
- immediate next beat
- open threads
- DM operational notes

---

## Mid-Session Pause Command

### User Command

Recommended command:

`PAUSE POINT`

Use this when the table pauses but the session is not fully complete.

### Required Assistant Actions

When the user declares a pause point, the assistant should:

1. Capture the new location and current state.
2. Update `bootstrap/SESSION_STATE.md`.
3. Optionally append a short note to the current session log if one exists and the user asks for it.

---

## Continuity Rules

- Do not invent session events to fill gaps.
- If a closeout is incomplete, explicitly mark uncertain details as uncertain.
- Session logs should be concise operational records, not transcripts.
- Deviations from Canon are required whenever the table changed encounter count, item acquisition, puzzle outcome, difficulty, location sequence, or major NPC behavior.
- Missed canon content remains missed unless later recovered in play.
- `SESSION_STATE.md` should reflect live table reality even when it differs from canon.

---

## Cross-Project Handoff Rules

The DM Runtime Project should maintain:

- `bootstrap/SESSION_STATE.md`
- `session-logs/`

The Ideation / Design Project should consume those files before proposing future content.

The Ideation / Design Project should not rewrite actual-play history unless the user explicitly instructs it to correct an error.

If the Ideation / Design Project proposes canon updates based on session outcomes, those updates should be made in `canon/` and should reference the relevant session log in the commit or PR summary.

---

## Recommended User Commands

Use these exact commands when possible:

- `OPEN SESSION`
- `CLOSE SESSION`
- `PAUSE POINT`
- `RECAP`
- `BEAT`
- `CHECKS`
- `RULING`
- `TRANSITION`
- `NPC`

These commands keep live support predictable and reduce context drift.
