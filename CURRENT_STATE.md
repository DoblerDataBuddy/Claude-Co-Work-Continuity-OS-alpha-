# CURRENT_STATE

## What This Is
Claude-Co-Work Continuity OS: an alpha system for maintaining AI/human workflow state across sessions, with emphasis on:
- **Local-first operation** — no external state dependencies
- **Restart recovery** — resume work after session interruption
- **Context persistence** — carry reasoning and decisions forward
- **Token efficiency** — minimize re-explanation overhead

Built from student workflow optimization work at ERAU. Still evolving.

## Project Status
**Phase:** Alpha structural development
**Focus:** Establishing operational patterns and file organization
**Maturity:** Pre-release. Patterns are being validated; interfaces may change.

## Immediate Objectives
- [ ] Finalize repo structure and boundaries
- [ ] Document restart protocol and state restoration mechanics
- [ ] Validate context compression and rehydration
- [ ] Establish append-only audit trail patterns
- [ ] Create first continuity packet example

## Known Limitations
- No state validation suite yet
- Context compression strategy still experimental
- Token overhead not yet benchmarked against baselines
- Integration with Claude Code harness incomplete

## How to Navigate This Repo

**START HERE:**
- `CLAUDE.md` — operating rules, file boundaries, what's validated vs speculative
- `docs/philosophy.md` — why this system exists and what problem it solves
- `docs/architecture.md` — how components talk to each other

**If you're implementing:**
- `/operators/` — modular role definitions (architect, executor, auditor, archivist)
- `/validation/` — restart tests, audit logs, state checks
- Check `CLAUDE.md` for file boundary rules before editing

**If you're testing:**
- `/validation/restart_tests/` — how state restoration is validated
- `/state/ACTIVE/` — current working state
- `/examples/continuity_packets/` — sample state transfer objects

## Current Blockers
None blocking work yet. Repo structure still being established.

## Last Updated
2026-05-27 — Initial state capture
