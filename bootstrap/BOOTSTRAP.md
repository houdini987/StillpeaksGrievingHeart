# Stillpeak's Grieving Heart — Universal Bootstrap

This file is the shared starting point for any AI project, assistant, or human collaborator working from this repository.

It is intended to support two working modes:

- **DM Runtime Project:** live table support, rulings, narration, continuity, and session-state updates.
- **Ideation / Design Project:** packet design, canon refinement, prep work, structural improvements, and future-session planning.

Both projects should read this file before acting.

---

## Mandatory Read Order

When beginning work, read in this order:

1. `bootstrap/BOOTSTRAP.md`
2. `bootstrap/PROJECT_ROLES.md`
3. `bootstrap/SESSION_PROTOCOL.md`
4. `bootstrap/SESSION_STATE.md`
5. `lessons-learned/LESSONS_INDEX.md`
6. All active lesson files referenced in `lessons-learned/LESSONS_INDEX.md`
7. `canon/CANON_MANIFEST.md`
8. Most recent relevant file in `session-logs/`
9. Relevant canon packet(s) from `canon/scene-packets/`
10. Supporting files from `canon/project-rules/` or `canon/appendices/` only as needed

If there is uncertainty about packet paths, file names, or current canon scope, use `canon/CANON_MANIFEST.md` first rather than guessing.

---

## Authority Model

### Canon Layer

`canon/` contains designed campaign truth.

Canon packets, appendices, and project rules define the intended module structure, encounter design, locations, tone, and mechanics.

Canon files should not be overridden by session logs for design purposes unless a later explicit canon update promotes a table event into canon.

### Session Log Layer

`session-logs/` contains actual-play continuity.

Session logs record what happened at the table: player choices, deviations from canon, improvised rulings, missed discoveries, changed difficulty, character state, and pause points.

Session logs are authoritative for continuity, but not automatically authoritative for future canon design.

### Lessons Learned Layer

`lessons-learned/` contains operational gotchas and process corrections discovered while using the repo across both projects.

Both the DM Runtime Project and the Ideation / Design Project should scan active lessons during boot.

The assistant is responsible for determining whether a newly discovered error or user callout is serious enough to become a lesson. Serious issues include mistakes that could cause session-state drift, canon bleed, numbering errors, write-order problems, or recurring workflow confusion.

### Bootstrap Layer

`bootstrap/` contains shared operating instructions and the current working state.

This layer tells each project what to read, what to trust, where the party is, and how to coordinate without confusing designed canon with lived play.

---

## Conflict Rules

When sources disagree:

1. **For live continuity:** follow `bootstrap/SESSION_STATE.md` and the latest relevant `session-logs/` file.
2. **For designed module content:** follow `canon/` files.
3. **For actual player inventory, missed items, level, or current location:** follow session logs and current session state.
4. **For future design:** use canon as the base, then incorporate actual-play deviations deliberately.

Never assume the party acquired an item, clue, boon, or NPC relationship merely because it exists in canon. Check session logs first.

---

## Project Role Split

For full role boundaries, read `bootstrap/PROJECT_ROLES.md`.

### DM Runtime Project

Primary responsibilities:

- Support live play at the table.
- Generate concise narration, rulings, checks, transitions, NPC dialogue, and combat guidance.
- Preserve actual session state.
- Update `session-logs/` after sessions or major pause points.
- Update `bootstrap/SESSION_STATE.md` when the live baseline changes.
- Avoid broad redesign unless explicitly asked.

### Ideation / Design Project

Primary responsibilities:

- Improve canon packets and future prep.
- Use session logs as actual-play context.
- Propose structural improvements, better handoff content, future encounters, and canon refinements.
- Avoid rewriting actual-play history.
- Avoid treating session improvisation as canon unless explicitly promoted.

---

## Session Log Expectations

Each session log should be concise and structured.

Recommended format:

1. High-Level Summary
2. Key Events
3. Combat Event
4. State at End of Session
5. Advancement
6. Outstanding Threads
7. Deviations from Canon
8. Pause Point

The most important section for cross-project coordination is **Deviations from Canon**.

---

## Lessons Learned Expectations

Lessons learned are not a dumping ground.

Create a new lesson only when a mistake, gotcha, or user correction is serious enough that the system should not repeat it.

Examples of lesson-worthy issues:

- Accidental writes during read-only workflows
- Session numbering drift
- SESSION_STATE mismatch with latest session log
- Canon/session-log confusion
- Incorrect project-role behavior
- Repeated live-play friction caused by ambiguous protocol

When a new lesson is created:

1. Add a new `LL-###-short-slug.md` file.
2. Update `lessons-learned/LESSONS_INDEX.md`.
3. Update bootstrap or protocol files if the lesson changes boot behavior.

---

## Live DM Command Contract

In the DM Runtime Project, the following shorthand commands may be used:

- `BEAT` = table-ready scene beat using the established BEAT format
- `NPC` = spoken dialogue only
- `RULING` = fast adjudication only
- `CHECKS` = only relevant DCs and checks for the current moment
- `TRANSITION` = move from one scene into the next
- `RECAP` = short DM-only reminder of current scene state

### BEAT Output Format

When the user types `BEAT`, respond in this order:

1. A larger DM-spoken segment that can be read or paraphrased at the table.
2. Three one-sentence bullets:
   - likely continuation
   - escalation / complication
   - optional branch / discovery
3. Relevant canon checks only, with DCs and character fit where canon gives them.
4. If no canon checks are timely, say: `No immediate canon check pressure.`

Do not change this contract unless the user explicitly changes it.

---

## Current Campaign Status Snapshot

For the latest state, read `bootstrap/SESSION_STATE.md`.

As of the creation of this bootstrap layer:

- Active packet: Packet 05 — The Mid-Slopes of Stillpeak
- Active segment: Segment II — Wind-Carved Spine
- Party level: 7
- Last major event: one vibration-maddened hill giant defeated on the Stonefold Ramps
- Current pause point: short rest at the base / entry of the Wind-Carved Spine

---

## Maintenance Rules

Update `bootstrap/SESSION_STATE.md` whenever:

- the party reaches a new packet or segment
- the party gains a level
- a major item, clue, or boon is gained or missed
- a canon encounter is materially changed in play
- the session pauses in a new location

Create or update a `session-logs/` file whenever:

- a session ends
- a major live-play milestone occurs
- the table diverges materially from canon
- the other project needs a reliable actual-play handoff

---

## Non-Goals

This bootstrap layer is not intended to replace canon packets.

It should not become a lore dump, transcript archive, or full campaign wiki.

Keep it operational: read order, authority model, current state, workflow rules, and cross-project handoff.
