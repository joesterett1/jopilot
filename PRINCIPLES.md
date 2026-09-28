# JoPilot Principles

These principles are being discovered through Patient 0 use rather than written as an up-front manifesto.

## Product

### Normal life should generate the evidence
Avoid creating a new capture habit whenever normal behavior already produces usable evidence.

### Carry the problem
> **JoPilot should carry the problem until it reaches the smallest irreducible piece that requires me.**

The goal is not simply to save minutes. It is to remove the activation, reconstruction, remembering, and context-switching burden surrounding small responsibilities.

### Human judgment is scarce
JoPilot should do the searching, remembering, connecting, deduplicating, and evidence gathering. The person should supply judgment where judgment is actually necessary.

### Sophisticated underneath, simple on top
> **The architecture should become more sophisticated so the interface can become less sophisticated.**

## Evidence and trust

### Evidence is not interpretation
Store what was observed separately from what JoPilot currently believes it means.

### Corrections append; they do not rewrite history
If JoPilot was wrong, preserve that fact and append the corrected interpretation with truthful timing.

### Preserve uncertainty
> **Correct what the evidence proves. Preserve what you don't know.**

Unknown identity, authority, or relationship information should remain unknown rather than being replaced with a plausible bridge.

### Derived insights remain traceable
A surprising insight should be inspectable through typed, directional edges back to its supporting evidence.

## Action and authorization

### Authorization is proportional to consequence
Creating a reversible internal task is not the same risk class as sending a message, spending money, deleting data, or changing permissions.

### Uncertain writes are reconciled, not repeated
If a write may have succeeded, read the canonical target before considering another mutation.

### Reversibility matters
Prefer bounded, inspectable, reversible actions when moving from recommendation into execution.

## Building

### Reality outranks fixtures
Automated tests are necessary. Production evidence can still expose assumptions the fixtures never modeled.

### Do not manufacture the acceptance test
If normal life has not produced an eligible case, the truthful state is blocked or awaiting evidence—not a weakened test.

### AI coding agents do not remove engineering responsibility
Generated code still needs architecture, acceptance criteria, tests, provenance, production verification, and judgment about risk.
