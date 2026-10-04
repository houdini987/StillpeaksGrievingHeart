# Stillpeak's Grieving Heart — Claude Code Project

Homebrew D&D 5e campaign (eastern Spine of the World) run by Brian on Roll20 for Mikey, Carter, Chelsea, and Kathleen. Brian is the human DM; Claude supports him. Claude never runs the game for the players directly.

This repo is the campaign's source of truth. It was built with ChatGPT; its operating system lives in `bootstrap/`, and Claude follows it as written.

## Two modes

| Mode | Skill | Use when |
|---|---|---|
| DM Runtime | `/dm` | At or near the table: OPEN SESSION, BEAT, NPC, RULING, CHECKS, TRANSITION, RECAP, PAUSE POINT, CLOSE SESSION |
| Ideation / Design | `/ideate` | Designing or refining canon, prep, maps, image briefs, Roll20 setup |

`load bootstrap` means `/dm` without opening a session. If the user just asks a question, use PROJECT_ROLES' boundary test: "what happens right now at the table" → DM rules; "how should this be designed" → ideation rules; "what actually happened" → session logs and `SESSION_STATE.md`; "what is supposed to happen" → canon.

## Ground rules (both modes)

- Read `bootstrap/BOOTSTRAP.md` for the full read order, authority model, conflict rules, and the BEAT command contract.
- **Designed truth ≠ table truth.** Canon says what could happen; session logs and `bootstrap/SESSION_STATE.md` say what did. Never assume the party acquired an item, clue, or boon just because canon placed it (LL-004).
- **Reveal boundaries are hard.** During Chapter 7 play, never expose the Druid sabotage, Abbathor, the king's immortality mechanism, or the ending solution. Each packet overview lists its "must not reveal yet" items.
- Find the latest session log only through `session-logs/LATEST_SESSION_LOG.md` (LL-010).
- Roll20 is authoritative for live HP, AC, slots, and conditions. `bootstrap/PARTY_ROSTER.md` is a reference snapshot.
- Tone: restrained, environmental pressure first, explicit DCs. Preserve exact rules language from canon.
- Lessons go in `LESSONS_LEARNED.md` only, as one-line `LL-### [Tag]` entries; never renumber.

## Context economy

The repo is about 180k tokens; Packets 7 and 8 alone are about 85k. Load only what the current beat needs:
- Always: the bootstrap stack (small).
- For runtime: the active packet's main file plus the specific supplements `canon/CANON_MANIFEST.md` lists for the current beat.
- Don't preload Packet 8 while the party is still on Packet 7, beyond the overview's reveal boundaries.

## Assets

Maps, scene images, portraits, and character sheet PDFs live outside the repo in `C:\Users\Houdi\OneDrive\Documents\Stillpeaks Grieving Heart\`. Do not copy them into git. `assets/ASSET_INDEX.md` maps each file to its packet and beat.

## Git

- This is a public GitHub repo (`houdini987/StillpeaksGrievingHeart`). Commit as the user's git identity, with clear messages in the existing style ("Add …", "Index …", "Advance session state to …").
- DM mode: CLOSE SESSION and PAUSE POINT end with a commit and push of exactly the files the protocol writes.
- Ideation mode: commit each accepted change; push when the user approves or at the end of a design sitting.
- Never rewrite history or force-push.
