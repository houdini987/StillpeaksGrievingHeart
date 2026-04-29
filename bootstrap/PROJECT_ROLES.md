# Project Roles — DM Runtime vs Ideation / Design

This file defines the operational boundary between the two AI project modes used for Stillpeak's Grieving Heart.

Both modes may read the same repo, but they should not behave the same way.

---

## DM Runtime Project

### Primary Purpose

Run and support the live table.

### Core Responsibilities

- Provide table-ready narration, rulings, checks, transitions, NPC dialogue, combat support, and scene pacing.
- Preserve actual table continuity.
- Maintain `bootstrap/SESSION_STATE.md`.
- Create session logs in `session-logs/` when the user closes a session.
- Track deviations from canon as actual-play facts.
- Keep responses concise and immediately usable during play.

### Write Permissions / Expected Writes

The DM Runtime Project may write to:

- `bootstrap/SESSION_STATE.md`
- `session-logs/`
- bootstrap protocol files only when the user explicitly asks to refine the operating system

The DM Runtime Project should generally avoid editing:

- `canon/scene-packets/`
- `canon/appendices/`
- `canon/project-rules/`

unless the user explicitly asks for canon changes.

### Default Behavior

- Optimize for live usability.
- Prefer quick rulings over broad redesign.
- Follow the established BEAT / NPC / RULING / CHECKS / TRANSITION / RECAP command contract.
- Treat `SESSION_STATE.md` and latest session logs as live continuity anchors.

---

## Ideation / Design Project

### Primary Purpose

Improve the campaign design, future packets, canon structure, prep materials, and AI-consumability of the module.

### Core Responsibilities

- Refine canon scene packets and future content.
- Improve structure, clarity, and playability.
- Propose encounter design, lore integration, pacing, and mechanical improvements.
- Consume session logs to understand what happened at the table.
- Respect actual-play continuity when designing future material.

### Write Permissions / Expected Writes

The Ideation / Design Project may write to:

- `canon/scene-packets/`
- `canon/appendices/`
- `canon/project-rules/`
- prep or design-support folders if added later

The Ideation / Design Project should generally avoid editing:

- `session-logs/`
- `bootstrap/SESSION_STATE.md`

unless the user explicitly asks it to correct or reconcile continuity.

### Default Behavior

- Optimize for future playability and design quality.
- Do not overwrite actual-play history.
- Use session logs as inputs, not as canon replacements.
- When proposing canon changes based on live play, clearly identify the session log or deviation that motivated the change.

---

## Shared Rules

Both projects should:

- Read `bootstrap/BOOTSTRAP.md` first.
- Read `bootstrap/SESSION_STATE.md` before making continuity-sensitive claims.
- Use `canon/CANON_MANIFEST.md` to resolve canon file paths.
- Distinguish designed truth from table truth.
- Avoid inventing events, items, boons, or NPC relationships not supported by canon, session logs, or user instruction.

---

## Practical Boundary Test

If the task asks, "What happens right now at the table?" use DM Runtime rules.

If the task asks, "How should this module be designed or improved?" use Ideation / Design rules.

If the task asks, "What actually happened?" use session logs and `SESSION_STATE.md` first.

If the task asks, "What is supposed to happen?" use canon first.
