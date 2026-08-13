# Baseline Establishment Model

> **Document:** `03-how-logical/08-baseline-establishment-model.md`  
> **Title:** Baseline Establishment Model  
> **Version:** 0.8  
> **Status:** Normative Working Specification  
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


The Baseline Establishment Model defines the P9 act by which an accepted Candidate State becomes the next Authoritative State.

P9 is the final invariant phase of the canonical STATE Cycle.

## 1. Baseline establishment definition

> **Baseline Establishment is the explicit authorized act that assigns authoritative status to an accepted Candidate State for a defined purpose and preserves its continuity relationship to the prior Authoritative State.**

Acceptance and Baseline Establishment are separate.

Acceptance says:

> this Candidate may progress toward authoritative status.

Baseline Establishment says:

> this identified accepted Candidate is now the Authoritative State for the defined scope and purpose.

## 2. Preconditions

P9 requires, to the degree applicable:

- G8 outcome = ACCEPT;
- exact accepted Candidate identity;
- governing Transition Contract identity;
- Acceptance Record identity;
- no unresolved mismatch between accepted target and establishment target;
- sufficient authority to establish the baseline;
- sufficient state identity to support future Transitions.

## 3. Baseline Establishment Record

WP-09 shall be capable of representing the following fields.

### BE-01 — Establishment Identity

Identity of the Baseline Establishment act.

### BE-02 — Previous Authoritative State

Reference to the state authoritative immediately before establishment.

### BE-03 — Accepted Candidate Identity

Identity of the exact Candidate authorized by G8.

### BE-04 — Acceptance Record Identity

Reference to the Acceptance decision authorizing progression to P9.

### BE-05 — Transition Contract Identity

Reference to the governing Transition and Contract revision.

### BE-06 — Authority Scope

The scope and purpose for which the new state becomes authoritative.

### BE-07 — Resulting Authoritative State Identity

The identity by which the new Authoritative State will be referenced.

### BE-08 — Effective Condition

Time, sequence, event or other condition at which authority becomes effective.

### BE-09 — Supersession Relationship

Which prior baseline or authority status is superseded for the defined scope.

### BE-10 — Known Constraints

Material constraints limiting the meaning or applicability of the established baseline.

### BE-11 — Provenance References

References sufficient to reconstruct the Transition, Candidate, Verification, Evidence and Acceptance basis.

### BE-12 — Baseline Custodian

The Role / Actor recording or maintaining authoritative-state continuity.

### BE-13 — Establishment Result

ESTABLISHED, HOLD or FAILED.

### BE-14 — Failure or Hold Rationale

Reason establishment did not complete where result is not ESTABLISHED.

## 4. P9 result semantics

### ESTABLISHED

The exact accepted Candidate has become the new Authoritative State for the defined scope.

### HOLD

The Candidate remains accepted, but an establishment condition is unresolved.

The previous Authoritative State remains authoritative.

### FAILED

Baseline Establishment cannot be completed safely or unambiguously.

The previous Authoritative State remains authoritative.

P9 HOLD or FAILED does not rewrite the earlier ACCEPT decision.

## 5. State identity

Authoritative-state identity shall be sufficient for the claims and future control needs.

Identity may include one or more of:

- source revision;
- configuration identity;
- dependency identity;
- environment identity;
- artifact identity;
- data or schema identity;
- deployment identity;
- sequence or temporal identity.

No one identity mechanism is mandatory.

The required identity depth is proportional to the state claim.

## 6. Baseline scope

An Authoritative State is authoritative **for a defined scope and purpose**.

Examples may include:

- authoritative source state;
- authoritative build configuration;
- authoritative release artifact;
- authoritative deployed configuration;
- authoritative combined system state.

STATE does not require every project to use all of these.

It requires that the relevant scope not be ambiguous.

## 7. Authoritative State Chain

STATE preserves authoritative continuity as a chain:

```text
A0
 │
 T1
 │
 C1
 │
 Accept
 │
 Establish
 ▼
A1
 │
 T2
 │
 C2
 │
 Accept
 │
 Establish
 ▼
A2
```

The chain may branch in exploratory or Candidate work.

Authoritative continuity does not branch silently.

Where multiple baselines are intentionally authoritative for different scopes or variants, those scopes shall be explicit.

## 8. Supersession

When A2 becomes authoritative for the same scope as A1, A1 is superseded for active authority.

Superseded does not mean deleted, invalidated historically or forgotten.

The prior state remains part of provenance.

## 9. No retrospective authority

A later Acceptance or Baseline Establishment shall not be represented as though the new state had been authoritative before its actual Effective Condition.

Historical authority status is part of state provenance.

## 10. Rollback of a non-authoritative Candidate

Discarding or reversing a non-authoritative Candidate does not require a new authoritative-state Transition if the Authoritative State itself never changed.

Example:

```text
A5
 │
 ├── C6 FAIL
 │
 └── discard C6
 │
 ▼
A5 remains authoritative
```

This is candidate repair or abandonment.

It is not rollback of an Authoritative State.

## 11. Rollback of an Authoritative State

Once A6 has become authoritative, returning operational or authoritative state to something equivalent to A5 is a **new Transition**.

```text
A5
 │
 T6
 ▼
A6  authoritative
 │
 T7  controlled reversal / restoration
 ▼
C7  equivalent to or derived from A5
 │
 Verify / Accept / Establish
 ▼
A7  new Authoritative State
```

A7 may be content-equivalent to A5.

It is not historically identical to A5 because it exists after different transitions, decisions and context.

> **Rollback of an Authoritative State is forward-moving governance toward a new state, not time travel to an old authority moment.**

## 12. Baseline correction

If P9 mistakenly points authority at the wrong Candidate or identity, correction is itself a controlled authority event.

The record shall not be silently edited to erase the mistake if the incorrect establishment was materially effective.

Assurance and Tailoring determine the required correction mechanism.

## 13. Concurrent Transitions and baseline establishment

When several Transitions are based on the same earlier Baseline, P9 shall account for intervening authoritative changes.

A Candidate verified against A10 shall not silently become A12 if A11 became authoritative in the meantime and materially changes the relevant state basis.

The Transition must:

- rebase or otherwise reconcile;
- re-establish affected claims;
- or demonstrate that the intervening state is irrelevant to the accepted scope.

## 14. Baseline establishment and evidence freshness

Evidence used for P9 shall still correspond to:

- the accepted Candidate;
- the relevant Contract revision;
- the actual state being established.

Identity mismatch is a G9 failure condition.

## 15. Baseline establishment and release

P9 does not require external Release.

A project may establish an Authoritative State and release it later.

This supports:

- controlled release windows;
- separate distribution authority;
- multiple release channels;
- delayed publication;
- operational staging.

## 16. Canonical Baseline Establishment rules

> **Acceptance authorizes progression; Baseline Establishment assigns authoritative status.**

> **Only the exact accepted Candidate may be established under the corresponding Acceptance decision.**

> **P9 HOLD or FAILED leaves the previous Authoritative State unchanged.**

> **Authoritative history is preserved as a chain of state transitions, not overwritten as if earlier states never existed.**

> **Rollback of an Authoritative State is a new controlled Transition, not time travel.**

> **A state may be content-equivalent to an earlier state without being the same historical Authoritative State.**

> **Baseline identity depth is proportional to the claims and future control needs.**

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.8  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
