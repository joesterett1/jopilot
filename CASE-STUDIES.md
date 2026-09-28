# Patient 0 Case Studies

These cases are intentionally sanitized. They describe the product and engineering lesson without exposing private source data.

## Reality outranks fixtures

A live evidence-capture canary encountered a real attributed-message representation that the offline fixtures did not model correctly. A framing byte could survive a heuristic decoder and become a literal character in captured text.

JoPilot remained unverified while the defect was investigated. The repair replaced heuristic scanning with structure-aware decoding, preserved the original bad capture, appended a correction with truthful observation time, and revalidated against naturally arriving evidence.

**Lesson:** a green test suite is evidence, not reality. Production canaries should be designed to falsify assumptions rather than merely confirm deployment.

## The missing intermediary

A relationship insight compressed a multi-step referral chain into an apparent direct connection. The source evidence supported something weaker: information had passed through an unresolved intermediary. A later real-world interaction falsified the stronger claim.

The unsupported canonical state was corrected while preserving the original evidence, unknown intermediary, directionality, later corrective observation, and the still-unresolved runtime defect.

**Lesson:**
> **Correct what the evidence proves. Preserve what you don't know.**

An unknown node is still information. Removing it is an inference.

## The two-minute task that never gets done

A small administrative message required only a few minutes of manual work but substantially more cognitive activation: notice it, reconstruct context, investigate, decide, act, and remember to return.

JoPilot interpreted the request, gathered most of the needed context, resolved what the evidence supported, isolated one missing fact, and prepared a reversible response.

The desired interaction became:

```text
JoPilot carries the problem
        ↓
one fact remains outside its senses
        ↓
ask for exactly that fact
        ↓
resume from the checkpoint
        ↓
close the loop
```

**Lesson:**
> **JoPilot should carry the problem until it reaches the smallest irreducible piece that requires me.**

The product value may be better measured by open loops prevented and context reconstruction avoided than by minutes automated.
