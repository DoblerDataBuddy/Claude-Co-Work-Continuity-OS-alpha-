# Operating Rules for Claude-Co-Work Continuity OS

This document defines how work happens in this repo, what's guaranteed vs experimental, and how to maintain operational integrity.

## Core Principle
**This is a student-originated workflow system being built iteratively.** Work documented here should survive review, not require re-explanation every session. Mark everything appropriately.

## File Organization & Boundaries

### Authoritative Sources
- **CURRENT_STATE.md** — Single source of truth for project status, blockers, next actions
- **README.md** — Public-facing elevator pitch
- **CLAUDE.md** — This file. Operating rules and file contract.
- **docs/\*.md** — Philosophy, architecture, protocol specifications (write-once reference)
- **/operators/\*.md** — Role definitions, unchanged once committed
- **/validation/\*.md** — Test results, audit logs (append-only)

### Volatile / Working State
- **/state/ACTIVE/** — Current session work, expected to change
- **Session notes, scratch files** — Local only, don't commit unless finalized
- **Brainstorm/ experiments** — Mark as "(hypothesis)" until validated

### Do Not Duplicate
- Don't restate architecture decisions in commit messages — they go in `docs/`
- Don't explain "why this file exists" in comments — it belongs in `CLAUDE.md` file boundaries
- Don't keep resolved issues commented out — delete cleanly or reference in `/validation/` logs
- Don't version control temporary files (use `.gitignore`)

## Writing Standards

### Validated vs. Hypothesis
All claims must be marked:

**[VALIDATED]** — Tested, works in practice, reproducible
- Example: "restart recovery succeeds 95% of time in test suite"
- Where: docs, architecture, test results
- Changes to validated items go through review

**[HYPOTHESIS]** — Proposed, not yet tested, directional thinking
- Example: "token overhead could be reduced by 40% with smarter caching"
- Where: experiment docs, brainstorms, early proposals
- Can change freely; become validated only after evidence

**[IN PROGRESS]** — Being actively tested/built right now
- Example: "context compression strategy being benchmarked"
- Where: CURRENT_STATE.md, session notes
- Update as work progresses

### No Overclaim
- Don't say "the system does X" until X is demonstrated
- Don't claim efficiency gains without measurements
- Don't assume patterns work beyond the conditions they've been tested in (e.g., ERAU undergrad → assume not general until proven)
- Use "appears to," "suggests," "in testing" for preliminary results

## Append-Only Patterns

### Validation Logs
Files in `/validation/` are append-only unless explicitly purged:
- Each entry includes: date, test condition, result, validator
- Never delete entries retroactively
- Failed tests stay visible — they're data

### Audit Trails
- State transitions are logged with timestamp and reasoning
- Operational decisions go in `docs/decisions.md` with date and context
- If you change your mind, document the change, don't hide the old thinking

## How to Work Here

### Before Starting a Feature
1. Check `CURRENT_STATE.md` — what's actively being worked on?
2. Read relevant `docs/*.md` — what's the existing pattern?
3. Check `/operators/` — which role owns this work?
4. Look at `/validation/` — has this been tried before?

### During Development
- Commit incrementally with clear messages
- Update CURRENT_STATE.md when you shift focus
- Mark experimental code as `[HYPOTHESIS]` in comments if needed
- Append to validation logs, don't rewrite them

### Before Pushing
- Does your change fit file boundaries defined here?
- Have you updated CURRENT_STATE.md?
- Is everything marked (validated/hypothesis/in progress)?
- Did you avoid duplicating explanations between files?

## Session Continuity Contract

When a Claude instance (or human) enters this repo:
1. Read CURRENT_STATE.md — this is the state handoff
2. Review CLAUDE.md — this is the operating contract
3. Inspect `/state/ACTIVE/` — this is working context
4. Check `docs/` if clarification needed — this is history

**Responsibility:** If you change state, update CURRENT_STATE.md before you leave. The next session depends on it.

## FAQ

**Q: Can I add experimental ideas?**
A: Yes. Mark them `[HYPOTHESIS]` in a dedicated section. Keep them separate from validated patterns.

**Q: What if I need to refactor something?**
A: Document the old pattern in `docs/` first, then refactor. Don't let it vanish.

**Q: Can I delete old test results?**
A: Only if explicitly superseded. New test results append — old ones stay visible.

**Q: What about comments in code?**
A: Comments explain the "why" for non-obvious logic. Don't duplicate what the code already says. If explaining a workaround or constraint, keep it focused.

**Q: How do I mark something as "no longer applicable"?**
A: Create an entry in `docs/decisions.md` with the date and reasoning. Don't delete it from the original file.

---

**Last Updated:** 2026-05-27
**Status:** ACTIVE (these rules are live)
