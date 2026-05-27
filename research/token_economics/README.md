# Token Economics Research

Analysis of token cost vs. benefit tradeoffs in continuity patterns.

## Research Questions

### Current Baseline
- How many tokens are needed to re-explain a project from scratch?
- What's the distribution (context recovery vs. new work)?
- How does this scale with project complexity?

### Continuity Overhead
- Token cost of creating a continuity packet?
- Token cost of loading and rehydrating state?
- Token cost savings from NOT re-explaining?
- Break-even point (when is continuity cheaper than fresh explain)?

### Optimization Directions
- Which parts of state are most expensive to transmit?
- What context can be safely dropped without losing continuity?
- Can context be compressed without losing information?
- How does serialization format affect token cost?

## Experiments to Run
1. Baseline re-explanation across session lengths (1h, 4h, 8h project)
2. Continuity overhead measurement on real workflows
3. Context compression strategies and token savings
4. Serialization format comparison

## Findings
[HYPOTHESIS] — Token economics will show 30-50% savings with mature continuity system
- Hypothesis based on: preliminary observation that re-explanation dominates token cost
- Test in progress: baseline measurements being collected

---

See `CLAUDE.md` for [VALIDATED] vs [HYPOTHESIS] distinction.
