# ACTIVE State

Working directory for current session. Contents are expected to change.

## What Goes Here
- Session context and current focus
- Working notes and intermediate results
- Current work-in-progress state
- Temporary files related to active work

## Expectations
- Updated frequently during active development
- Cleaned or moved to ARCHIVE at session end
- Not the source of truth (that's in `/docs/` and operational files)
- Expected to be volatile

## Session Handoff
Before ending a session, review ACTIVE state and decide:
- Keep as continuity packet? → move to `/examples/continuity_packets/`
- Archive? → move to `/state/ARCHIVE/`
- Discard? → clean up

---

Update CURRENT_STATE.md before leaving.
