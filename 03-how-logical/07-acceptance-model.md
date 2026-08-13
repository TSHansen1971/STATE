# Acceptance Model

> **Document:** `03-how-logical/07-acceptance-model.md`  
> **Title:** Acceptance Model  
> **Version:** 0.7  
> **Status:** Normative Specification
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


The Acceptance Model defines how STATE decides whether an identified Candidate State may progress from verified candidate status toward Authoritative State.

Acceptance occurs at P8 / G8.

Acceptance is an authority decision informed by verification, evidence and Assurance.

It is not itself a verification method.

## 1. Acceptance object

Acceptance applies to:

- an identified Candidate State;
- an explicit Acceptance Claim Set;
- an identified Transition Contract revision;
- an applicable Evidence Set;
- known deviations and residual uncertainty;
- an authorized decision scope.

> **Acceptance is claim-bound and scope-bound.**

## 2. Acceptance Claim Set

The **Acceptance Claim Set** is the set of claims that must be resolved for the requested Acceptance decision.

Claims may be classified operationally as:

### ACS-01 — Required Claim

Must be satisfied for ACCEPT under the current Acceptance basis.

### ACS-02 — Supporting Claim

Provides evidence or context but is not independently sufficient or necessary for ACCEPT.

### ACS-03 — Informational Claim

Recorded for awareness, diagnosis or future engineering but does not govern the present Acceptance decision.

The classification shall not be manipulated after failure merely to remove an inconvenient Required Claim.

Changing Required Claim status is a Contract amendment and authority event.

## 3. Acceptance Record structure

WP-08 Acceptance Record shall be capable of representing:

### AR-01 — Candidate Identity

The exact Candidate State being decided.

### AR-02 — Transition Contract Identity

The governing Contract revision.

### AR-03 — Acceptance Scope

Which system, component, artifact or state scope the decision covers.

### AR-04 — Acceptance Claim Set

The Required, Supporting and Informational Claims relevant to the decision.

### AR-05 — Verification Basis

The Verification Records used by the decision.

### AR-06 — Evidence Basis

The Evidence Set and critical Evidence Items relied upon.

### AR-07 — Deviations

Known deviations, failed historical claims, accepted exceptions or departures relevant to the decision.

### AR-08 — Residual Uncertainty

Material uncertainty that remains after verification.

### AR-09 — Assurance Basis

Applicable Assurance assessment, independence or review condition.

### AR-10 — Acceptance Authority

The Actor and Authority Grant under which the decision is made.

### AR-11 — Decision

ACCEPT, REJECT, REPAIR REQUIRED or INCONCLUSIVE.

### AR-12 — Decision Rationale

Why the evidence and authority basis support the recorded decision.

### AR-13 — Effective Constraints

Constraints that bound the meaning of ACCEPT, such as environment, configuration or intended scope.

### AR-14 — Decision Identity

Time, sequence, signature, commit, record identity or another mechanism sufficient to distinguish the decision.

## 4. Canonical G8 outcomes

STATE preserves exactly four canonical outcomes.

### ACCEPT

ACCEPT means:

> **The Acceptance Authority has determined that the identified Candidate satisfies the Required Acceptance Claims, within the explicit Acceptance scope and constraints, with evidence and residual uncertainty sufficient for the applicable Assurance objective.**

ACCEPT permits progression to P9.

It does not itself establish the new Baseline.

### REJECT

REJECT means:

> **The Candidate shall not progress toward authoritative status under the current Transition path.**

The previous Authoritative State remains authoritative.

### REPAIR REQUIRED

REPAIR REQUIRED means:

> **The Candidate is not acceptable in its current state, but the Transition may continue through authorized repair.**

Repair creates a new or revised Candidate and requires re-verification appropriate to what changed.

### INCONCLUSIVE

INCONCLUSIVE means:

> **Acceptance Authority lacks sufficient basis to decide ACCEPT or REJECT under the current Acceptance basis.**

The next action may be additional verification, stronger evidence, clarification or authorized Contract amendment.

## 5. No conditional-acceptance outcome

STATE does not define **ACCEPT WITH CONDITIONS** as a fifth canonical G8 outcome.

If a condition must be satisfied before the Candidate can legitimately become authoritative, the condition is part of the current Acceptance basis.

Until satisfied, the correct outcome is normally:

- REPAIR REQUIRED; or
- INCONCLUSIVE.

If the future action is genuinely outside the current Acceptance basis, it should be represented as a separate obligation or Transition rather than as an unresolved condition hidden inside ACCEPT.

## 6. Required Claim rule

For ACCEPT under the current Acceptance basis:

- every Required Claim shall have an outcome sufficient for Acceptance;
- no unresolved Required Claim may remain FAIL;
- no unresolved Required Claim may remain INCONCLUSIVE;
- required target identity shall match the Candidate being accepted.

If a Required Claim is legitimately removed or changed, that change must occur through an authorized Contract amendment and remain traceable.

The historical Verification Result is not rewritten.

## 7. Accepted deviation

A Candidate may differ from an earlier expectation without falsifying the record.

A deviation may be accepted only when:

- the deviation is explicit;
- the applicable authority can legitimately accept it;
- the Acceptance basis or governing Contract is amended where required;
- relevant claims are re-evaluated;
- historical FAIL or deviation evidence remains preserved.

An accepted deviation is not a retroactive PASS.

## 8. Residual uncertainty

No engineering decision removes all uncertainty.

Acceptance therefore considers whether residual uncertainty is:

- explicit;
- bounded to the degree required;
- supported by evidence;
- compatible with the Acceptance Authority's legitimate decision scope;
- acceptable under the applicable Assurance objective.

Unidentified uncertainty cannot be accepted merely by being ignored.

## 9. Acceptance sufficiency conditions

STATE defines ten Acceptance Sufficiency Conditions.

### AS-01 — Candidate Identity

The Candidate being accepted is sufficiently identified.

### AS-02 — Contract Identity

The governing Transition Contract revision is explicit.

### AS-03 — Required Claim Resolution

Required Acceptance Claims have sufficient outcomes.

### AS-04 — Evidence Sufficiency

Evidence is sufficient for the Required Claims and decision consequence.

### AS-05 — Deviation Resolution

Material deviations are explicitly resolved.

### AS-06 — Residual Uncertainty Visibility

Material uncertainty is explicit.

### AS-07 — Authority Validity

Acceptance Authority is valid for the scope and decision.

### AS-08 — Assurance Sufficiency

Required independence, review or Assurance conditions are satisfied.

### AS-09 — State Coherence

The Candidate identity, Work Package integration state and verification target are coherent.

### AS-10 — Baseline Establishment Readiness

There is sufficient identity and control basis to proceed to P9 if ACCEPT is recorded.

## 10. Acceptance is not universal correctness

> **ACCEPT means that the Candidate is accepted for the defined scope, claims, conditions and purpose. It does not assert that every possible property of the Candidate is known or correct.**

Examples:

- Acceptance for one supported operating environment does not prove compatibility with all environments.
- Acceptance of functional claims does not silently establish an unverified security claim.
- Acceptance of a component does not prove the integrated system.
- Acceptance of source state does not prove release-artifact provenance unless that claim is included and evidenced.

## 11. Acceptance and verification disagreement

Acceptance Authority does not have authority to rewrite Verification Results.

If a required Verification Claim is FAIL:

- the Candidate cannot receive ACCEPT under the unchanged Acceptance basis;
- Acceptance Authority may REJECT;
- require repair;
- or authorize a legitimate Contract amendment if it has or obtains the appropriate governing authority.

The original FAIL remains part of the record.

## 12. Acceptance and INCONCLUSIVE verification

An INCONCLUSIVE Required Claim cannot be silently treated as “good enough.”

The correct path is to:

- strengthen verification;
- gather additional evidence;
- clarify the claim;
- or explicitly amend the Acceptance basis through appropriate authority.

## 13. Negative evidence

Acceptance shall consider decision-relevant negative evidence.

Evidence Stewardship or Acceptance shall not omit relevant failure evidence merely because positive evidence also exists.

A decision may explain why particular negative evidence is non-governing.

It may not pretend the evidence does not exist.

## 14. Acceptance independence

The required degree of decision independence is selected through Tailoring and Assurance.

Possible controls include:

- separate Acceptance Actor;
- separate organization;
- independent Verification Role;
- deterministic Acceptance gate for defined claims;
- multi-method evidence;
- human authority over synthetic execution.

Physical independence is proportional, not universally maximal.

## 15. Acceptance and Actor Independence

Any authorized Actor type may support the Acceptance process.

However, normative Acceptance Authority remains traceable to a human-established governance source.

A synthetic system may exercise delegated Acceptance logic only where that delegation is explicit.

Capability does not create Acceptance Authority.

## 16. Acceptance and Work Packages

Work Package completion is not Acceptance.

Even if every package is COMPLETED and locally PASS:

- integration may remain unverified;
- system-level Required Claims may remain unresolved;
- the Candidate may not yet exist in final integrated identity;
- Acceptance Authority may lack sufficient evidence.

## 17. Acceptance and release

ACCEPT does not imply Release Authority.

P9 establishes the new Authoritative State.

Release, when separate, follows under its own authority and provenance requirements.

## 18. Acceptance and baseline establishment

Acceptance is necessary but not sufficient for a new Authoritative State.

```text
Candidate
   │
   ▼
G8 ACCEPT
   │
   ▼
Accepted Candidate
   │
   ▼
P9 / G9
Baseline Establishment
   │
   ▼
New Authoritative State
```

If P9 fails, the previous Authoritative State remains authoritative.

## 19. Decision supersession

A later Acceptance decision may supersede an earlier decision for a revised Candidate or amended Contract.

The earlier decision remains part of provenance.

Decision supersession shall not make historical records appear as though the later state had been accepted earlier.

## 20. Canonical Acceptance rules

> **Acceptance is claim-bound, scope-bound and Candidate-bound.**

> **Acceptance Authority decides; it does not rewrite Verification Results.**

> **A Required Claim that remains FAIL or INCONCLUSIVE prevents ACCEPT under the unchanged Acceptance basis.**

> **An accepted deviation is not a retroactive PASS.**

> **STATE does not use a fifth conditional-acceptance outcome to hide unmet Acceptance conditions.**

> **ACCEPT permits progression to P9; it does not itself create the new Authoritative State.**

> **Acceptance establishes only the claims and scope actually covered by the Acceptance basis.**

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-SA 4.0  
Version: 0.7  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
