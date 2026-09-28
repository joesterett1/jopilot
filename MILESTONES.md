# Milestones

A sanitized timeline of JoPilot's Patient 0 development.

## Durable operating state
JoPilot moved from conversational memory toward durable task, relationship, rule, command, and development state. Important state became inspectable and reconcilable rather than merely remembered by a model.

## Provenance-first message evidence
Message ingestion evolved from text extraction into an evidence model preserving message identity, conversation provenance, sender information, timing, and source relationships.

A core distinction emerged: **when something happened is not necessarily when JoPilot learned it.**

## Production evidence capture
Live evidence capture was deployed forward-only against naturally arriving data. Historical messages were deliberately not backfilled with invented availability.

## Reality found the decoder bug
The first natural production messages exposed a decoding defect that offline fixtures had not modeled. JoPilot remained unverified, the decoder was repaired structurally, the original incorrect capture was preserved, a correction was appended, and later natural evidence validated the repaired path.

## Correction-aware reasoning
Downstream consumers were given both immutable original observations and current effective interpretations with correction history and revision identity. Material corrections invalidate downstream reasoning; fresh readback alone does not.

## Forward-only live interpretation
Candidate extraction was deployed behind a second production activation boundary. Only evidence eligible after that boundary can be considered automatically. Legacy candidates remain legacy rather than being silently rebound.

The honest state remains **awaiting natural candidate** until a naturally occurring eligible case passes end-to-end acceptance.

## Ongoing
Attribution, human judgment, promotion, and action are being activated separately.

> **Prove the primitive before expanding the architecture.**
