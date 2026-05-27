# Audit Logs

Append-only record of system behavior, validation results, and state transitions.

## Log Files

### restart_validation.log
Test results from restart recovery scenarios. Each entry includes:
- ISO timestamp
- Test scenario name
- Result (PASS/FAIL)
- Relevant metrics
- Any anomalies

### state_transitions.log
Record of significant state changes:
- When state moves from ACTIVE → STARTUP → ARCHIVE
- What was captured
- Any validation done
- Session ID and validator

### decisions.log
High-level decisions made in the system:
- What was decided
- By whom / which operator
- Reasoning
- Date
- Link to relevant documentation

## Format Standard
```
YYYY-MM-DD HH:MM:SS | [LEVEL] | [CATEGORY] | Message with details
```

Example:
```
2026-05-27 14:30:00 | PASS | restart_validation | Scenario: 3-session workflow. All context restored, token cost 15% vs baseline.
```

## Never Delete
Entries are append-only. If an entry is superseded, add a new entry noting the change, don't remove the old one.

---

See `/CLAUDE.md` for append-only and audit expectations.
