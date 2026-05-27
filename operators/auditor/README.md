# Auditor Operator

**Role:** Validation, testing, finding deviations from spec

## Responsibilities
- Design and run validation tests (restart recovery, state persistence)
- Audit code changes against CLAUDE.md rules
- Check for file boundary violations
- Maintain audit logs in `/validation/`
- Flag assumptions or overclaims
- Report gaps between specification and implementation

## Who Fills This Role
QA/testing persona ensuring system behaves as documented

## Output Artifacts
- Test plans and results (append-only in `/validation/`)
- Audit reports
- Issue tracking
- Specification gaps

---

See `/CLAUDE.md` for append-only log expectations.
