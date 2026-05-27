# STARTUP State

Initial context for resuming work after session restart.

## What Goes Here
- Continuity packets from previous sessions
- Snapshot of state before session ended
- Key context needed for immediate restart
- Pointer to relevant ARCHIVE entries

## Structure
Each continuity packet should include:
- Timestamp and session ID
- Summary of work completed
- Current blockers or open questions
- Pointer to next actions
- Relevant code or state snapshots

## Session Restart Protocol
1. Read CURRENT_STATE.md
2. Check `/state/STARTUP/` for previous session context
3. Load continuity packet
4. Review CURRENT_STATE.md again for any updates
5. Begin work

---

See `docs/continuity_protocol.md` for detailed protocol.
