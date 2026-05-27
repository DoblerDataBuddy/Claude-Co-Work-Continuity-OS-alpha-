# Sample Sessions

Example workflows showing how continuity system works in practice.

## Session Examples

### Single-Session Workflow
- Start → work → capture → end
- Shows minimal continuity overhead
- Example: quick bug fix or small feature

### Multi-Session Development
- Session 1: architect decides design
- Session 2: executor implements component 1
- Session 3: executor completes component 2
- Session 4: auditor validates
- Shows state handoff between roles and sessions

### Interrupted Recovery
- Session interrupted unexpectedly
- Restart from STARTUP state
- Verify no work lost
- Demonstrate recovery time

### Long-Running Project
- Multiple weeks of development
- ARCHIVE grows, ACTIVE stays focused
- Shows continuity scaling to longer timescales

## Format
Each example includes:
- Session transcript or outline
- Initial state snapshot
- Continuity packets at handoff
- Final outcomes
- Lessons learned

---

See `docs/continuity_protocol.md` for protocol details.
