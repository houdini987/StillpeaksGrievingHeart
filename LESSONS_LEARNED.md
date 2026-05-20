# Lessons Learned

Use this file as the single compact index of durable project lessons. Keep each lesson to 1-2 lines max, preserve sequential IDs forever, and do not renumber deleted or retired entries.

- LL-001 [Runtime] Treat `OPEN SESSION` as read-only until the full bootstrap stack is loaded and current session state is verified.
- LL-002 [Session Logs] Derive session numbering from repo files, not memory or assumptions.
- LL-003 [State] Keep `bootstrap/SESSION_STATE.md` aligned with the latest relevant session log.
- LL-004 [Canon] Canon placement does not imply party acquisition; check session logs before assuming items, clues, boons, or NPC relationships.
- LL-005 [Memory] GitHub connector access may block persistent memory writes; use repo documentation for durable project rules when connected.
- LL-006 [Bootstrap] Always start bootstrap loads at `bootstrap/BOOTSTRAP.md`; never repo-scan to decide the entry point.
- LL-007 [Structure] Keep lessons learned in this single file only; do not create one file per lesson.
- LL-008 [Format] Use `LL-### [Tag]` plus a short directive; keep each lesson actionable and compact.
- LL-009 [Stability] Never renumber existing lesson IDs; leave gaps if an entry is retired or removed.
- LL-010 [Session Access] Do not scan or search for session logs; always use `session-logs/LATEST_SESSION_LOG.md` as the pointer.
- LL-011 [Table Truth] Do not propose cutting, replaying, or relocating completed table beats; treat completed session-state events as history unless the user explicitly asks to retcon.
- LL-012 [Handoff] When creating a handoff `.md` file, always index it in `canon/CANON_MANIFEST.md` so bootstrap/canon navigation can surface it.
