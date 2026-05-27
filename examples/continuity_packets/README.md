# Continuity Packets

Templates and examples of state snapshots used for session handoff.

## What Is a Continuity Packet

A self-contained document that captures:
- **Current state** — where things stand right now
- **Recent decisions** — what was just decided and why
- **Open questions** — what's blocking or unclear
- **Next actions** — immediate priorities for next session
- **Context snapshot** — code state, key files, references
- **Metadata** — timestamp, session ID, participants

## Packet Structure

```
# Continuity Packet: [Project Name]

## Session Info
- Date: YYYY-MM-DD
- Session ID: [UUID]
- Participants: [who worked]
- Duration: [X hours]

## Executive Summary
[1-2 sentence summary of work done and state]

## What Was Accomplished
- Item 1: description and validation status
- Item 2: description and validation status

## Current Blockers
- Blocker A: description, workaround if any
- Blocker B: description, workaround if any

## Open Questions
- Question 1: [context]
- Question 2: [context]

## Next Actions (Priority Order)
1. [Action] - [rationale]
2. [Action] - [rationale]

## Context Snapshot
- Key files changed: [list with line numbers]
- Test results: [summary]
- Token usage: [if applicable]

## References
- Related issues: #123
- Relevant docs: docs/architecture.md
- Previous packet: [link]
```

## Examples to Build
- Minimal packet (single session, straightforward work)
- Complex packet (multi-role handoff, many blockers)
- Recovery packet (restarting from interruption)

---

See `docs/continuity_protocol.md` for detailed protocol.
