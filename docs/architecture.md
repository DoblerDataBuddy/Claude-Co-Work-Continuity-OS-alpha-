# Architecture: System Components and Boundaries

[VALIDATED] This section documents how system components interact and data flows between them.

## Component Overview

- **Operators** — Role-based modules (architect, executor, auditor, archivist)
- **State** — Working state (ACTIVE), startup context (STARTUP), historical archive (ARCHIVE)
- **Continuity Packets** — Serialized state for session handoff
- **Validation** — Restart testing and audit trails

## To Be Completed
- Component interaction diagrams
- State transition protocols
- Context compression strategy
- Serialization formats for continuity packets
- Restart recovery flow

---

See CLAUDE.md for authorship and update protocols.
