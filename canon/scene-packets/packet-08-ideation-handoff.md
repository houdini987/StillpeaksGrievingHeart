# Packet 8 Ideation Handoff — Throneward Descent

## Purpose

Use this file when resuming Packet 8 / Chapter 8 design in a fresh chat or after context compaction.

This is a working handoff, not a replacement for canon. Canon authority remains with the `.canon.md` files and `canon/CANON_MANIFEST.md`.

---

## Current Design State

Packet 8 is the final interior chapter after Queen's Bridge. The party has not reached it yet; they are at the near side of Queen's Bridge in Packet 7 (see `bootstrap/SESSION_STATE.md`).

The chapter path is:

1. Throneward Descent
2. Advisor Records
3. Druid-Centric Reveal
4. Mining Decree / Greed Spiral
5. Implosion Threshold (the ruined public throne room)
6. King's Chamber / Crystal Boss Arena (the geode beyond the passage behind the throne)

The chapter should not become a sprawling city crawl. It is a direct final-act descent from tragedy into culpability.

---

## Locked Story Arc

Chapter 7 revealed the visible tragedy: the queen fell during a sudden tremor.

Chapter 8 reveals the hidden truth:

- Dhurak Stonevein and Veyra Deeproot were trusted Stone Druid advisors.
- They were corrupted by Abbathor-touched crystal greed and self-deception.
- They secretly induced the tremor that caused the queen's fall.
- The king's grief and denial made him vulnerable to their manipulation.
- He permitted deeper crystal mining because he believed the queen could be recovered, preserved, or restored.
- Crystal accumulation reached critical mass and imploded.
- Dhurak and Veyra became crystal-earth/root Stone Druid titans.
- The Mourning King became a throne-bound living vessel sustained by green beams.

The mountain itself is wounded, not evil. The final horror is grief, greed, denial, and preservation past mercy — not undead evil.

---

## Current Final Encounter Model

- **Dhurak Stonevein** and **Veyra Deeproot** are the two active Druid titan bosses, each with 1 legendary resistance.
- **The Mourning King** is an inert, throne-bound living vessel protected by the Druids: not undead, not a commander, no turns, no spells, 0 legendary actions, 0 legendary resistances.
- Attacks on the King while a beam is active are intercepted by a living Druid by default.
- Erny and Maelreth are over-attuned in the arena (Final Attunement Crisis, Attuned Offense Backlash, Grounded Silence).

Use `packet-08-current-stat-blocks-quick-reference.canon.md`, `packet-08-roll20-monster-prep.canon.md`, and `packet-08-mourning-king-non-undead-rule.canon.md` for monster handling.

---

## Current Ending Model

`packet-08-ending-execution.canon.md` is the single source for the ending. `packet-08-first-green-heart-artifact.canon.md` is the single source for the pendant.

- **Ending Q1 (locked):** the King's mercy plea is poetic but clear; he never bluntly says "kill me" or "end it."
- **Ending Q2 (locked, option D):** a layered, restrained release split between the characters. Erny and Maelreth feel the mountain let go; Alina, Sorin, and Bilbo see the queen's bridge procession finish its crossing. It is a completed rite, not a reunion. This also settles the former "queen memory appearance" item.
- Ending read-aloud is plainspoken; no stacked "not as / not as" fragments.
- After the release, the party can recover the First Green Heart from the King's body.

---

## Recently Completed Work

- **2026-10-03 — Ending Q2 locked as D** (split-witness release, procession completes its crossing, no reunion).
- Consolidated `packet-08-ending-style-and-relic-patch.canon.md` into `packet-08-ending-execution.canon.md` (style rules, release read-alouds, salvation cues, pendant hand-off) and `packet-08-first-green-heart-artifact.canon.md` (names, canon role), then deleted the patch.
- Removed duplicate and superseded ending text ("Not as stone. Not as thunder." cue, the "End it." plea line, second plea list) from `packet-08-final-encounter.canon.md` and `packet-08-runtime-cues.canon.md`; both now point to ending-execution.
- The First Green Heart mythic act now has one count: 6 successes before 3 failures, DC 18 (the patch's 5-success version was removed).
- Indexed `packet-08-image-briefs.md` in the manifest; added it and the throne-room patch to the overview's "Use with" list.
- Earlier (ChatGPT era): non-undead King rule, stat block quick reference, Roll20 prep, obvious Druid protection on entry, playability patch, throne-room threshold patch, First Green Heart artifact.

---

## Active Checklist / Next Actions

1. **Non-attuned spotlight pass (next).** Give Alina (Champion fighter, Protection style, longbow), Sorin (Hunter ranger, climbing kit), and lightly Bilbo (Four Elements monk, 45 ft speed; DM's own PC) distinct mechanical roles in the King's Chamber, beyond the generic ally-counterplay checks in `packet-08-attunement-affliction.canon.md`. Fold the result into the affliction and final-encounter files.
2. **Contradiction cleanup** (no new design, just alignment):
   - Main packet Beat 6, At-a-Glance, and overview spine item 6 still call the King an active boss ("All three bosses are active from the start"); the lore file calls him "still dangerous" with "grief-engine command." Align to the inert-vessel model.
   - Beat 5 location: the main packet, monsters file, and playability patch still use a generic threshold / sealed doorway with light draining "toward the throne." Fold `packet-08-throne-room-threshold-patch.canon.md` and the playability patch's Beat 5 section into the main packet and retire both patch sections.
   - Crystal Tremorborn HP: 85–95 in the main packet vs 75–85 elsewhere (Roll20 uses 80).
   - Attunement affliction references "the Mourning King's grief-resonance effects," which no longer exist.
   - First Green Heart origin: the artifact file puts the King near the source crystal before the queen's fall; the lore file says his failure began after it. Decide which is true.
   - `canon/appendices/overall-story-arc.md` still says "a natural tremor."
   - `packet-08-treasure-discoveries.canon.md` "Relic Use in Final Encounter" duplicates the salvation rules now in ending-execution; reduce to a pointer.
3. **Ending Q3 — Player-facing aftermath choices:** what the party can inspect, recover, or say before leaving the King's Chamber.
4. **Mechanical wrap-up:** remaining hazards after the release, whether Erny and Maelreth's mountain attunement ends permanently or leaves a trace, and leaving Stillpeak.
5. **Rewards / epilogue hooks:** final discoveries, First Green Heart disposition, Cinderwatch and Stillpeak consequences.
6. **Roll20 final setup check:** maps, tokens, beam tracker, handouts, macros.

### Continuity confirmation needed from Brian

- **Soot-Black Prayer Bead:** a guaranteed Exodus Landing discovery and the strongest salvation relic, but neither `SESSION_STATE.md` nor Session 07 confirms the party has it (LL-004). Confirm before working on salvation or rewards.

---

## Working Guidance for Future Sessions

- Load bootstrap normally, then read this handoff after `canon/CANON_MANIFEST.md`.
- Edit authoritative files in place. Do not add new `*-patch.canon.md` files; when a decision touches an existing patch, fold it into its authoritative file and delete it.
- Ask one checklist question at a time, with lettered options and a recommendation.
- After each accepted decision, update Recently Completed and the Active Checklist here.
