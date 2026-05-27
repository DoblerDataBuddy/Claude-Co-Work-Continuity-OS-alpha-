# Restart Tests

Test suite for validating restart recovery and state restoration.

## Test Categories

### Context Restoration
- Load previous session state
- Verify all fields present
- Check no information loss
- Validate state consistency

### Token Efficiency
- Measure token cost of state rehydration
- Compare to baseline (re-explaining from scratch)
- Track optimization improvements over time

### Determinism
- Run same restart scenario multiple times
- Verify identical outcomes
- Check no race conditions in state loading

### Integration
- Full round-trip: work → capture → restart → resume
- Multi-session workflows
- Edge cases (interrupted saves, network failures)

## Running Tests
To be documented as test suite is built.

## Test Results Log
Append new results to `audit_logs/restart_validation.log` with:
- Date and test version
- Test scenario
- Pass/fail status
- Metrics (tokens, time, accuracy)
- Notes

---

See `/CLAUDE.md` for append-only log expectations.
