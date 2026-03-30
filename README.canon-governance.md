# Stillpeaks Grieving Heart — Canon Governance

## Source of Truth

Files ending in `.canon.md` are the authoritative source of truth in this repository.

- `canon/scene-packets/*.canon.md` are the live packet canon.
- `canon/appendices/*.md` are live supporting canon unless explicitly marked otherwise.
- Exported `.docx` and `.pdf` files are derived artifacts, not source canon.
- Image placeholders may remain in canon until standalone assets are linked under `assets/images/`.

## DM Project Consumption Rules

This repository is intended to support a separate DM-facing project used during live gameplay.

The DM project should consume this repo with the following assumptions:

- Treat `.canon.md` packet files as the operational narrative and mechanics source.
- Preserve exact mechanical language where packet text defines rules, DCs, conditions, rewards, or encounter logic.
- Do not summarize away systemic truths such as Tremorscope behavior, Karagvorn Line reinterpretation, encumbrance pressure, or grief-field logic.
- Where live gameplay state changes, the DM project may reason from current session facts, but it should not overwrite packet canon unless those changes are intentionally promoted back into this repository.
- Character state, initiative, HP, inventory drift, and token conditions remain live-play state, not packet canon, unless deliberately canonized later.

## Future Packet Authoring Rules

All future scene packets should follow the same standardized format and ordering:

1. At-a-Glance Summary
2. Narrative Setup (Canonical Text)
3. Read-Aloud Scene Introduction
4. Environment Overview
5. Running the Location
6. Encounter Modules
7. Player Curiosity Hooks
8. Escalation Signal
9. Rewards / Discoveries
10. DM Reference Sidebar
11. Map Reference

### Scene Packet Section Anchors (Required Standard)

All Scene Packets must include explicit section anchors to ensure precise, low-risk updates.

Each major section header must follow this format:

## [SP-#] Section Name

Example:

## [SP-1] At-a-Glance Summary
## [SP-2] Narrative Setup
## [SP-3] Read-Aloud Scene Introduction
## [SP-4] Environment Overview
## [SP-5] Running the Location
## [SP-6] Encounter Modules
## [SP-7] Player Curiosity Hooks
## [SP-8] Escalation Signal
## [SP-9] Rewards / Discoveries
## [SP-10] DM Reference Sidebar
## [SP-11] Map Reference

Rules:
- Anchors must remain stable once created
- Section names must not be changed without explicit refactor
- All future edits must reference section anchors, not just titles

## Authoring Standards

- Preserve restrained tone and avoid melodramatic escalation.
- Keep environmental pressure primary; creatures are usually expressions of the mountain’s condition, not the central point.
- Preserve the Tremorscope as the most reliable directional truth source.
- Treat the Karagvorn Line as reinterpretation of rules, not blanket magic negation.
- Keep checks, DCs, and reward language explicit.
- Prefer modular, segment-based scene design when pressure escalates.

## Repository Discipline

- If a packet is revised, update the corresponding `.canon.md` file rather than creating parallel alternate packet files.
- Avoid duplicate canon layers.
- Use standalone image assets when available; do not rely on embedded-document-only visuals.
- Add future appendices when a rule system, monster set, loot layer, or visual progression model becomes cross-packet canon.
