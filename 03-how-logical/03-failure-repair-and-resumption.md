# Failure, Repair and Resumption

> **Document:** `03-how-logical/03-failure-repair-and-resumption.md`  
> **Title:** Failure, Repair and Resumption  
> **Version:** 0.5  
> **Status:** Normative Specification
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


STATE treats failure, uncertainty and interruption as normal engineering states that must preserve authoritative-state integrity.

The core safety invariant is:

> **The current Authoritative State remains authoritative until a new state completes Acceptance and explicit baseline establishment.**

## 1. Failure classes

STATE distinguishes several logical failure classes.

### F-01 — Authority Failure

The intended action is not supported by sufficient authority.

Examples:

- missing Authority Grant;
- conflicting authority;
- attempted implicit authority escalation;
- unknown authority boundary.

Required response:

- stop affected mutation;
- preserve Baseline;
- create or update WP-11 Deviation and Escalation Record where material;
- return to P0 or P2 after authority is resolved.

### F-02 — Specification Failure

The intended outcome or Acceptance basis is too ambiguous or internally inconsistent.

Required response:

- preserve state;
- return to P1;
- obtain authorized clarification.

### F-03 — Boundary Failure

Required implementation exceeds the authorized Transition Boundary.

Required response:

- do not silently widen scope;
- preserve discovered condition;
- escalate;
- amend authority/boundary or create a separate Transition.

### F-04 — Context Failure

Inspection shows that the actual Baseline, dependency or environment materially differs from the assumptions under which the Transition was specified.

Required response:

- stop candidate production where necessary;
- return to the earliest invalidated phase;
- do not treat prior readiness as still valid.

### F-05 — Candidate Production Failure

The Candidate cannot be produced as specified.

Required response:

- preserve the current Authoritative State;
- record relevant transformation and failure evidence;
- repair within existing authority if possible or escalate.

### F-06 — Execution Failure

The Candidate cannot execute, build, analyze or otherwise operate under the required conditions.

This may directly produce claim-level FAIL evidence.

### F-07 — Verification Failure

A required claim evaluates to FAIL.

The Candidate remains non-authoritative.

### F-08 — Verification Inconclusive

The verification basis cannot establish PASS or FAIL with sufficient confidence.

INCONCLUSIVE is not PASS.

### F-09 — Evidence Failure

Evidence is irrelevant, mismatched, incomplete, stale, unidentifiable or otherwise insufficient for the requested decision.

Required response:

- obtain valid evidence;
- repeat verification where necessary;
- do not accept merely because engineering effort has already been spent.

### F-10 — Acceptance Non-Approval

G8 results in REJECT, REPAIR REQUIRED or INCONCLUSIVE.

The prior Authoritative State remains authoritative.

### F-11 — Baseline Establishment Failure

The Candidate has an ACCEPT decision but cannot be safely or unambiguously established as the new Authoritative State.

Required response:

- preserve prior Authoritative State;
- preserve Acceptance Record;
- repair baseline-establishment conditions;
- do not pretend that Acceptance alone changed authoritative status.

### F-12 — Release Failure

An accepted and established state cannot be released as intended.

Release failure does not automatically invalidate baseline establishment.

The release decision is handled according to the applicable release governance.

## 2. Repair loop

A repair is a new controlled mutation of a non-authoritative Candidate or a new Candidate derived from the same Baseline.

Repair does not erase the failed candidate history.

```text
Candidate revision C1
        │
      VERIFY
        │
      FAIL
        │
        ▼
REPAIR REQUIRED
        │
        ▼
Candidate revision C2
        │
      RE-VERIFY
```

C2 is not entitled to inherit C1's PASS results automatically.

A prior Verification Record may be reused only where the relevant claim, state, dependency and conditions remain valid.

## 3. Earliest-invalidated-phase rule

After failure or new information, resumption shall begin at the earliest phase whose required condition is no longer valid.

Examples:

- implementation defect only → usually return to P4;
- verification method defect → return to P5 or P6;
- evidence mismatch → return to P6 or P7;
- scope expansion → return to P2;
- changed intended outcome → return to P1;
- changed Baseline or authority source → return to P0.

> **Do not restart the entire cycle unnecessarily, and do not resume later than the earliest invalidated control condition.**

## 4. Candidate revision identity

Each materially different Candidate State used for verification shall be distinguishable to the degree required by the claims.

Evidence from Candidate C1 shall not be silently attributed to C2.

Where exact identity matters, Evidence Sets and Verification Records shall reference the candidate identity directly.

## 5. Inconclusive outcome

INCONCLUSIVE means the available method or evidence is insufficient to establish the required conclusion.

Valid next actions include:

- obtain additional evidence;
- use a stronger verification method;
- repair the Candidate if the uncertainty arises from candidate behavior;
- return for specification clarification;
- request an authorized reduction or change in claim scope.

The last action is valid only when the acceptance basis is actually changed by appropriate authority.

The method shall not silently relabel the original claim as satisfied.

## 6. Boundary breach

When an actor discovers that the required or desirable action lies outside the Transition Boundary:

1. stop the out-of-bound mutation;
2. preserve the current state and discovery;
3. record the condition where material;
4. seek amended authority or establish a separate Transition;
5. resume only after the applicable gate is re-established.

Boundary discovery is useful engineering information.

It is not self-authorizing.

## 7. Interrupted execution

A Transition may be interrupted by:

- system restart;
- actor handoff;
- tool failure;
- working-session termination;
- infrastructure outage;
- scheduled pause.

Interruption does not require full restart if the last valid control state can be reconstructed.

## 8. Safe resumption

A Transition may resume from a prior point only when:

- Baseline identity remains valid;
- Candidate identity, if one exists, remains valid;
- applicable Authority Grants remain valid;
- specification and boundary remain unchanged or valid;
- required Work Products remain available;
- evidence used for later decisions still corresponds to the relevant state;
- no intervening external change invalidates the assumptions.

If these conditions cannot be established, resume from the earliest phase that can safely re-establish them.

## 9. Resume Point

A **Resume Point** is a reconstructed cycle position whose preceding gate conditions remain valid.

A Resume Point is not merely “where work stopped.”

It is where the Transition can safely continue without assuming invalid state.

## 10. Repair versus new Transition

Repair remains within the same Transition when:

- intended outcome remains the same;
- authority remains sufficient;
- boundary remains sufficient;
- Baseline relationship remains meaningful.

A new Transition should be established when repair would materially change:

- intended outcome;
- authority basis;
- Transition Boundary;
- architecture decision;
- accepted risk or invariant;
- Baseline identity.

## 11. Failed candidate preservation

STATE does not require indefinite retention of every failed intermediate artifact.

It requires preservation of enough information to support the relevant:

- traceability;
- diagnosis;
- assurance;
- Acceptance decision;
- later repair;
- provenance claim.

Tailoring determines retention depth.

## 12. No false green

The following are prohibited as uncontrolled failure handling:

- weakening a test merely to obtain PASS;
- silently narrowing a claim after failure;
- discarding negative evidence that remains decision-relevant;
- replacing the candidate without updating identity;
- expanding scope because the actor has technical access;
- accepting because schedule pressure makes repair inconvenient.

## 13. Canonical failure rules

> **FAIL and INCONCLUSIVE are valid engineering outcomes.**

> **A failed Candidate State does not replace the Authoritative State.**

> **Repair creates a new or revised Candidate and requires verification appropriate to what changed.**

> **Resumption begins at the earliest invalidated control condition, not merely where activity stopped.**

> **Boundary discovery does not create authority.**

> **Acceptance without successful baseline establishment does not change the Authoritative State.**

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-SA 4.0  
Version: 0.5  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
