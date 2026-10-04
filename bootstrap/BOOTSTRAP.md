# Stillpeak's Grieving Heart — Universal Bootstrap

This file is the shared starting point for any AI project, assistant, or human collaborator working from this repository.

It supports two working modes:

- **DM Runtime:** live table support, rulings, narration, continuity, and session-state updates.
- **Ideation / Design:** packet design, canon refinement, prep work, structural improvements, and future-session planning.

Both modes read this file before acting. In Claude Code these modes are the `/dm` and `/ideate` skills under `.claude/skills/`; the repo-level `CLAUDE.md` loads automatically.

---

## Mandatory Read Order

When beginning work, read in this order:

1. `bootstrap/BOOTSTRAP.md`
2. `bootstrap/PROJECT_ROLES.md`
3. `bootstrap/SESSION_PROTOCOL.md`
4. `bootstrap/SESSION_STATE.md`
5. `bootstrap/PARTY_ROSTER.md`
6. `session-logs/LATEST_SESSION_LOG.md`, then the session log it names
7. `LESSONS_LEARNED.md`
8. `canon/CANON_MANIFEST.md`
9. Relevant canon packet(s) from `canon/scene-packets/`
10. Supporting files from `canon/project-rules/` or `canon/appendices/` only as needed

If there is uncertainty about packet paths, file names, or current canon scope, use `canon/CANON_MANIFEST.md` first rather than guessing.

---

## Packet Handoff Rule

If resuming design work for a specific packet, check `canon/CANON_MANIFEST.md` for any packet-specific handoff file after the mandatory read order.

For Packet 8 / Throneward Descent ideation, read:

- `canon/scene-packets/packet-08-ideation-handoff.md`

Packet handoff files do not override canon. They summarize current working state, checklist position, and recommended next actions so a fresh chat can resume without relying on a large prior context window.

---

## Session Log Access Rule

Do not rely on directory listing or search to find the latest session log.

Always use:
- `session-logs/LATEST_SESSION_LOG.md` as the deterministic pointer

If the pointer is missing, stale, or conflicts with SESSION_STATE, flag immediately.

---

## Authority Model

### Canon Layer

`canon/` contains designed campaign truth.

Canon packets, appendices, and project rules define the intended module structure, encounter design, locations, tone, and mechanics.

Canon files should not be overridden by session logs for design purposes unless a later explicit canon update promotes a table event into canon.

Where a packet has patch or supplement files, the newer patch controls the specific point it addresses. `canon/CANON_MANIFEST.md` lists which files apply to which packet.

### Session Log Layer

`session-logs/` contains actual-play continuity.

Session logs record what happened at the table: player choices, deviations from canon, improvised rulings, missed discoveries, changed difficulty, character state, and pause points.

Session logs are authoritative for continuity, but not automatically authoritative for future canon design.

### Lessons Learned Layer

`LESSONS_LEARNED.md` contains compact operational rules and corrections. Read the full file during boot.

The assistant is responsible for deciding whether a newly discovered error or user callout is serious enough to become a lesson: mistakes that could cause session-state drift, canon bleed, numbering errors, write-order problems, or recurring workflow confusion.

### Bootstrap Layer

`bootstrap/` contains shared operating instructions and the current working state.

This layer tells each mode what to read, what to trust, where the party is, who is in the party, and how to coordinate without confusing designed canon with lived play.

---

## Conflict Rules

When sources disagree:

1. **For live continuity:** follow `bootstrap/SESSION_STATE.md` and the latest session log.
2. **For designed module content:** follow `canon/` files.
3. **For actual player inventory, missed items, level, or current location:** follow session logs and current session state.
4. **For live character numbers (HP, AC, slots, conditions):** Roll20 is authoritative; `bootstrap/PARTY_ROSTER.md` is a reference snapshot only.
5. **For future design:** use canon as the base, then incorporate actual-play deviations deliberately.

Never assume the party acquired an item, clue, boon, or NPC relationship merely because it exists in canon. Check session logs first.

---

## Live DM Command Contract

In DM Runtime mode, the following shorthand commands may be used:

- `BEAT` = table-ready scene beat using the BEAT format below
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

Session commands (`OPEN SESSION`, `CLOSE SESSION`, `PAUSE POINT`) are defined in `bootstrap/SESSION_PROTOCOL.md`.

---

## Session Log Expectations

Session log structure (play-by-play layer and state summary layer) is defined in `bootstrap/SESSION_PROTOCOL.md` under Closing a Session.

The most important section for cross-mode coordination is **Deviations from Canon**.

---

## Lessons Learned Expectations

Lessons must be:
- 1–2 lines max
- Actionable rules (not narrative)
- Stored only in `LESSONS_LEARNED.md`

Do not create separate files or indexes for lessons.

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
- the other mode needs a reliable actual-play handoff

Update `bootstrap/PARTY_ROSTER.md` when a character levels, changes subclass, or gains a campaign-significant item or condition.

---

## Non-Goals

This bootstrap layer is not intended to replace canon packets.

It should not become a lore dump, transcript archive, or full campaign wiki.

Keep it operational: read order, authority model, current state, workflow rules, and cross-mode handoff.
