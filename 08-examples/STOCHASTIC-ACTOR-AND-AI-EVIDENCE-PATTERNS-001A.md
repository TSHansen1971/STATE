# STATE Engineering — Stochastic Actor and AI Evidence Patterns

> **Document:** `08-examples/STOCHASTIC-ACTOR-AND-AI-EVIDENCE-PATTERNS-001A.md`
> **Title:** STATE Engineering — Stochastic Actor and AI Evidence Patterns
> **Version:** 001A
> **Status:** Current Documentation
> **Created:** 2026-08-13
> **Last modified:** 2026-08-13
> **Author:** Tor-Ståle Hansen
> **Co-authors:** None

## 1. Nature

This document is **non-normative operational guidance** derived from existing STATE semantics.

It does not create an AI-specific Authority Domain, logical Role, Work Product class, Transition Gate, Acceptance rule or governance exception.

## 2. Stochastic output does not imply stochastic Authority

A stochastic Actor may produce different outputs from materially similar inputs.

Its Authority remains bounded by the same legitimate Authority source, Authority Grant and Transition Boundary.

> **Stochastic output does not imply stochastic Authority.**

Randomness, sampling parameters, model confidence, tool access and agent autonomy do not enlarge Authority.

## 3. Evidence for AI-generated Candidate artifacts

A practical claim-bound Evidence Set may preserve, where relevant:

- Baseline identity;
- exact Candidate identity;
- transformation diff;
- relevant prompt or instruction identity;
- model and runtime identity;
- material generation parameters;
- material tool actions;
- execution environment identity;
- generated-artifact provenance;
- Verification Record;
- negative Evidence;
- known limitations.

The objective is not indiscriminate retention of every interaction.

> **STATE requires claim-relevant Evidence, not indiscriminate conversation retention.**

## 4. Prompts and instructions where evidentially relevant

Prompt or instruction preservation becomes relevant when it materially affects authorization, constraints, Candidate production, reproducibility, failure investigation or provenance.

A controlled immutable reference may be used where full prompt content should not be repeated in every record.

## 5. Model and runtime identification

Model/runtime identity is recorded to the depth needed by the claim.

Potentially material identity may include model family/version, provider or host, inference runtime, generation parameters, tool configuration, dependency state and relevant external services.

> **This information does not guarantee reproducibility.**

Candidate identity may be more important than the theoretical ability to regenerate the same stochastic output.

## 6. Deterministic versus non-deterministic Verification

A non-deterministically generated Candidate may be verified by deterministic methods.

```text
STOCHASTIC REALIZATION
→ EXACT CANDIDATE
→ DETERMINISTIC OR CLAIM-APPROPRIATE VERIFICATION
→ PASS / FAIL / INCONCLUSIVE
```

Where Verification itself is non-deterministic, the Verification Record should expose the run/scenario strategy, criteria, observed variability, aggregation rule, limitations and the basis for PASS, FAIL or INCONCLUSIVE.

More stochastic runs are not automatically stronger Evidence.

## 7. Independent Verification

Independent Verification is separation from the failure source relevant to the claim.

Useful separation may involve a different Actor, model family, deterministic oracle, tool, environment, independently maintained test suite or human/domain review.

A second invocation of the same model may add challenge but is not automatically independent.

> **Actor count is not a proxy for independence.**

## 8. Confidence is not Acceptance

Model confidence or natural-language certainty may be an observation.

It is not Acceptance.

Confidence does not change FAIL or INCONCLUSIVE to PASS, create Acceptance Authority or establish a new Authoritative State.

> **Confidence is not Acceptance.**

## 9. Model self-assessment is not Acceptance Authority

A producing model may review its own Candidate.

That can be supporting Evidence if limitations are visible.

It does not make the model Acceptance Authority.

Production, Verification, Assurance and Acceptance remain logically distinct even when one physical Actor performs several activities under legitimate Tailoring.

## 10. AI tool use remains inside the Actor's Authority boundary

Shells, compilers, repository tools, web tools, deployment tools, database tools and subordinate agents do not widen the invoking Actor's Authority.

```text
ACTOR AUTHORITY
→ PERMITTED TOOL USE
→ MATERIAL ACTION
→ EVIDENCE
```

not:

```text
TOOL CAN DO IT
→ THEREFORE THE ACTOR MAY DO IT
```

An Actor cannot delegate Authority it does not possess or is not authorized to delegate.

## 11. Provenance for generated and transformed artifacts

A useful provenance chain may be:

```text
BASELINE
→ AUTHORIZED INSTRUCTION
→ ACTOR / MODEL / TOOL CONTEXT
→ GENERATION OR TRANSFORMATION
→ CANDIDATE IDENTITY
→ VERIFICATION
→ EVIDENCE SET
→ ACCEPTANCE DECISION
```

A digest can identify an artifact strongly.

A digest alone does not establish the complete origin, Authority chain or transformation history of that artifact.

## 12. INCONCLUSIVE Verification

INCONCLUSIVE is a valid engineering result when the available basis cannot justify PASS or FAIL.

Examples include conflicting stochastic observations, unavailable provenance required by the claim, inadequate independence, incomplete tool output or environmental variability outside the Verification assumptions.

A Required Claim that remains INCONCLUSIVE prevents ACCEPT under the unchanged Acceptance basis.

The result is not converted to “probably PASS”.

## 13. Operational patterns

### Pattern A — stochastic Realization, deterministic Verification

An LLM generates Candidate `C17`. Candidate identity is fixed. Deterministic compilation, tests and API-signature checks verify the stated claims. Acceptance concerns `C17`, not every artifact the model might have produced.

### Pattern B — stochastic behavior requires repeated observation

A behavior claim is evaluated across an authorized scenario/run strategy. Runs, criteria, variability, failures and limitations remain visible. The threshold is established before it is relied upon for PASS.

### Pattern C — self-review is supporting Evidence, not independent Acceptance

A second model pass reviewing its own Candidate may support Assurance. It is neither automatically independent Verification nor Acceptance Authority.

### Pattern D — tool-mediated transformation

Evidence distinguishes AI-produced source delta, formatter transformation, generated-source transformation and compiled artifact so provenance is not flattened into the label “AI-generated”.

## 14. Compact checklist

For claim-relevant stochastic Realization, ask:

1. Is the exact Candidate identified?
2. Is the Baseline identified?
3. Is the relevant prompt/instruction preserved or referenced?
4. Is model/runtime identity captured to the needed depth?
5. Are material tool actions reconstructable?
6. Is environment identity captured where relevant?
7. Does the Verification method match the claim?
8. Is deterministic/non-deterministic Verification distinguished?
9. If non-deterministic, are repetitions, criteria, variability and limitations visible?
10. Is claimed independence real failure-source separation?
11. Is confidence being mistaken for Acceptance?
12. Is self-review being mistaken for Acceptance Authority?
13. Did tool use remain inside the Authority boundary?
14. Is provenance sufficient?
15. Is negative Evidence preserved?
16. Is INCONCLUSIVE used when support is inadequate?

This checklist is operational guidance.

It is not a new Work Product class.

## 15. What does not change because an Actor is AI

- Authority still requires a legitimate source.
- Capability still does not create Authority.
- Candidate still precedes authoritative status.
- Verification remains claim-bound.
- PASS, FAIL and INCONCLUSIVE retain their meanings.
- Evidence remains claim-relative.
- Acceptance Authority decides Acceptance.
- Acceptance does not rewrite Verification.
- P9 remains explicit.
- negative Evidence remains visible where decision-relevant.
- repair resumes from the earliest invalidated control condition.

AI changes realization characteristics.

It does not create a separate STATE method.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 001A  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
