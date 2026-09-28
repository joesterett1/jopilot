# JoPilot Architecture

This is the public conceptual architecture of JoPilot. It intentionally omits private implementation details, personal data, credentials, and production configuration.

## Design objective

JoPilot is intended to carry cognitive and administrative state while preserving human judgment.

```text
Sources from normal life
        ↓
Evidence — provenance + time
        ↓
State — durable world model
        ↓
Reconciliation & intelligence
        ↓
Judgment — human where needed
        ↓
Action — bounded + reversible
```

## Evidence

Evidence answers: What was observed? From which source? When did the event occur? When did JoPilot first have access to it? Has the interpretation changed since capture?

A central design choice is separating **immutable original evidence** from **effective interpretation**. If an interpretation later proves wrong, JoPilot should preserve the original observation and append the correction rather than rewrite history.

## State

Evidence is reconciled into higher-level concepts such as people, typed relationships, commitments, tasks, decisions, rules, and open loops. Canonical state should be deduplicated, inspectable, and traceable back to evidence.

## Reconciliation and intelligence

This layer asks what evidence means **without erasing uncertainty**.

Examples include identity resolution, commitment detection, relationship direction, lifecycle changes, contradictions, and invalidation of earlier interpretations.

A useful insight is only as trustworthy as the evidence chain beneath it.

## Judgment

JoPilot should not turn every uncertainty into another inbox.

The emerging interaction grammar includes **Judgment Cards** when evidence exists but a decision is needed, and **Missing Evidence Cards** when the reasoning is complete but one fact remains outside the system's senses.

## Action

Actions are downstream of evidence, state, reconciliation, and judgment. Reversible internal state can use tightly allowlisted confirmation. Higher-consequence actions require stronger authorization.

## Reliability patterns

**Fail closed.** Missing provenance, ambiguous identity, conflicting evidence, or uncertain authorization blocks consequential changes rather than inviting a guess.

**Read back uncertain writes.** If a remote write may have happened but the response is lost, inspect the canonical target rather than blindly retry.

**Append corrections.** A corrected interpretation references the original evidence and records when the correction was actually learned.

**Preserve graph uncertainty.** `A supplied information about B` must not silently become `A knows B`. Unknown intermediary nodes remain unknown.

**Separate activation boundaries.** Observation, interpretation, promotion, and action become live independently.

## Product principle

> **The architecture should become more sophisticated so the interface can become less sophisticated.**

The user should encounter context and judgment—not databases, hashes, receipts, reconciliation jobs, or provenance machinery.
