# Transition Gates

> **Document:** `03-how-logical/02-transition-gates.md`  
> **Title:** Transition Gates  
> **Version:** 0.5  
> **Status:** Normative Specification
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


Transition Gates define the logical conditions required to progress through the STATE Cycle.

A gate is **not** necessarily:

- a meeting;
- a manual approval;
- a committee;
- a separate document;
- a human click.

A gate may be evaluated through explicit human decision, deterministic automation, delegated policy, synthetic evaluation, hybrid control or another mechanism appropriate to the Authority and Assurance model.

## Gate rule

> **A gate establishes that the control conditions required by the next phase are sufficiently true. It does not merely establish that the previous activity happened.**

## G0 — Authority & Baseline Gate

### Question

Do we know what authoritative state we are changing, and do we have sufficient authority to define the Transition?

### Minimum PASS condition

- Baseline sufficiently identified;
- authority source established or referenced;
- no unresolved authority contradiction that prevents specification.

### FAIL / HOLD examples

- baseline identity ambiguous;
- no legitimate authority source;
- competing authority claims unresolved.

## G1 — Specification Gate

### Question

Is the intended change sufficiently specified to guide bounded implementation and later acceptance?

### Minimum PASS condition

- intended outcome explicit;
- relevant constraints and invariants known to the required degree;
- acceptance basis sufficiently defined;
- material unknowns visible.

### FAIL / HOLD examples

- purpose remains ambiguous;
- acceptance would depend on unstated expectations;
- conflicting requirements remain unresolved.

## G2 — Boundary Gate

### Question

Is it sufficiently clear what may change and what requires additional authority?

### Minimum PASS condition

- Transition Boundary explicit;
- escalation conditions explicit where needed;
- Architecture Authority involved where required.

### FAIL / HOLD examples

- implementation scope cannot be distinguished from adjacent unauthorized scope;
- required mutation exceeds current Authority Grant.

## G3 — Readiness Gate

### Question

Has inspection established enough reliable context to produce a candidate without guessing across material boundaries?

### Minimum PASS condition

- relevant implementation surfaces identified;
- material assumptions tested to the required degree;
- discovered conditions do not invalidate specification or authority.

### FAIL / HOLD examples

- baseline differs materially from assumed baseline;
- dependency or architecture discovery invalidates the planned transition;
- further read-only inspection is required.

## G4 — Candidate Identity Gate

### Question

Do we have an identifiable Candidate State whose relevant transformation from Baseline is reconstructable?

### Minimum PASS condition

- candidate identity established;
- mutation remains within authority or documented authorized deviation;
- relevant transformation evidence exists.

### FAIL / HOLD examples

- candidate cannot be distinguished from unrelated changes;
- unauthorized mutation detected;
- provenance too weak for later verification.

## G5 — Observation Gate

### Question

Do we have sufficient observations under relevant conditions to evaluate the scheduled claims?

### Minimum PASS condition

- required execution or analysis occurred;
- relevant conditions captured;
- observations preserved.

### FAIL / HOLD examples

- candidate cannot execute under required conditions;
- environment identity is materially uncertain;
- observation mechanism failed.

A direct failure may already support a claim-level FAIL without forcing artificial continuation.

## G6 — Verification Gate

### Question

Do all required claims have explicit verification outcomes and visible limitations?

### Minimum PASS condition

- required claims enumerated;
- methods recorded;
- Evidence Items referenced;
- outcomes explicit;
- limitations visible.

### Gate interpretation

G6 can pass as a **process gate** even when one or more claim outcomes are FAIL or INCONCLUSIVE.

Passing G6 means verification is complete enough for decision, not that the Candidate passed.

## G7 — Evidence Gate

### Question

Is the evidentiary basis decision-ready for the Acceptance decision being requested?

### Minimum PASS condition

- evidence bound to correct candidate and claims;
- evidence identity sufficient;
- material negative evidence preserved;
- residual uncertainty explicit;
- Assurance requirements met to the required degree.

### FAIL / HOLD examples

- evidence belongs to a different candidate revision;
- critical claim relies only on assertion;
- integrity or provenance is insufficient for the requested claim.

## G8 — Acceptance Gate

### Question

What authorized decision applies to this Candidate State?

### Valid gate outcomes

- ACCEPT → proceed to P9;
- REJECT → terminate current candidate path;
- REPAIR REQUIRED → enter repair loop;
- INCONCLUSIVE → obtain additional basis or revise the authorized claim.

G8 is not a binary test gate. It is an authority gate.

## G9 — Baseline Establishment Gate

### Question

Has the accepted state actually been established as the next Authoritative State?

### Minimum PASS condition

- accepted Candidate identity confirmed;
- Baseline Establishment Record completed;
- authoritative-state continuity preserved.

### FAIL / HOLD examples

- accepted candidate cannot be matched to the intended resulting state;
- baseline record creation fails;
- repository or state authority cannot be updated safely.

Until G9 passes, the prior Authoritative State remains authoritative.

## Sufficiency Governance

Terms such as *sufficient*, *sufficiently specified*, *sufficient evidence* and equivalent expressions do not create discretionary authority outside the existing STATE control model.

The governing rules are:

1. **Threshold attachment.** Every sufficiency threshold belongs to the Acceptance basis or to the specific gate condition in which the threshold is used. A threshold is not an independent permission to progress.
2. **Authority ownership.** Establishing or changing a sufficiency threshold requires the Authority already responsible for establishing the governing Acceptance basis, Contract condition or gate-relevant control decision. No separate Sufficiency Authority is created.
3. **Prospective knowability.** A threshold shall be knowable to the degree required before it is relied upon to produce PASS. A threshold may be qualitative, quantitative or policy-derived, but it shall not be invented retrospectively from the observed Candidate or available evidence merely to justify progression.
4. **Controlled weakening.** Weakening an established threshold changes the governing Acceptance basis or gate condition. Where that basis is part of the Transition Contract, the weakening is a controlled Contract amendment and shall be explicit, authorized, traceable and followed by re-evaluation of affected gates and claims.
5. **No evidence-driven redefinition.** Weak evidence, incomplete evidence, an inconvenient FAIL or an INCONCLUSIVE result does not authorize a Realization Actor or evaluating mechanism to redefine what counts as sufficient.
6. **Failure to establish sufficiency.** Where the applicable threshold cannot be established or evaluated under existing Authority, the gate shall not manufacture PASS. The Transition shall HOLD, fail, remain INCONCLUSIVE where that outcome applies, or return to the earliest phase required to establish the missing control basis.

This rule does not create a new Gate, Authority Domain, Role, Work Product or method identifier.

A physical Actor may participate in defining, evaluating or automating a threshold only within the Authority already granted for the underlying decision.

> **Sufficiency is a property of an authorized decision basis, not a discretionary power created by the Actor evaluating available evidence.**

## Automated gates

A gate may be automated when:

- evaluation conditions are sufficiently specified;
- the evaluating mechanism has appropriate capability;
- the mechanism has explicitly delegated authority where the gate exercises authority;
- evidence is retained to the required degree;
- escalation behavior is defined for ambiguity or failure.

Automation of a gate does not erase the logical gate.

## Gate composition

Several gates may be physically evaluated by one pipeline or one actor.

This does not merge their meanings.

For example:

```text
one CI/CD pipeline
    ├── evaluates G4 candidate identity
    ├── evaluates G5 execution readiness
    ├── evaluates G6 verification completion
    └── prepares evidence for G7
```

Acceptance at G8 may still remain a separate authority decision.

## Gate bypass

A required gate condition shall not be bypassed merely because later activity is technically possible.

Technical ability to continue is not evidence that progression is authorized or justified.

## Canonical gate rule

> **Progression through STATE is controlled by established conditions, not by the mere availability of the next technical action.**

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.5  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
