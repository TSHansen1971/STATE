# STATE Conformance Model

> **Document:** `07-reference/CONFORMANCE-MODEL.md`  
> **Title:** STATE Conformance Model  
> **Version:** 0.12  
> **Status:** Normative Specification
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


The STATE Conformance Model defines the minimum semantic conditions required before a declared scope may legitimately be described as conformant with STATE Engineering.

## 1. Conformance definition

> **STATE Conformance is the demonstrated preservation of the applicable non-tailorable STATE control semantics within an explicitly declared scope.**

Conformance is internal to the method.

It is not certification.

## 2. Conformance is not success

Conformance evaluates method behavior, not whether the requested engineering outcome succeeded.

The following can all occur in a conformant Transition:

- Verification FAIL;
- Verification INCONCLUSIVE;
- Acceptance REJECT;
- Acceptance REPAIR REQUIRED;
- Acceptance INCONCLUSIVE;
- Baseline Establishment HOLD;
- Baseline Establishment FAILED;
- Release HOLD;
- Release FAILED.

A process that exposes failure correctly may be more conformant than one that hides failure and reports success.

> **STATE Conformance requires truthful control semantics, not a green outcome.**

## 3. Conformance scopes

### CS-01 — Transition Conformance

Applies to one actual Transition from identified Baseline through its terminal or current controlled state.

### CS-02 — Realization Conformance

Applies to a recurring physical workflow, pipeline, toolchain or execution pattern intended to realize STATE semantics.

Realization Conformance establishes capability to support conformant execution under declared assumptions.

It does not prove every execution conformant.

### CS-03 — Implementation Conformance

Applies to a defined project, engineering system or method implementation that establishes recurring STATE control structures.

Implementation Conformance does not certify an organization or product.

## 4. Scope declaration

A Conformance claim shall identify:

- conformance scope type;
- object or process in scope;
- applicable Tailoring;
- assumptions;
- conditional features such as Release;
- evidence basis;
- assessment identity.

Conformance claims shall not be broader than the evidence.

## 5. Canonical Conformance Requirements

STATE defines sixteen Conformance Requirements.

All applicable requirements shall be satisfied for an overall CONFORMANT status.

### CON-01 — Authoritative Starting State

The Transition or recurring realization establishes a sufficiently identified Authoritative State / Baseline before governed mutation.

### CON-02 — Specification before governed mutation

Intent, required change and sufficient Acceptance basis are established before controlled Candidate production.

### CON-03 — Explicit and bounded Authority

Relevant Authority is explicit or explicitly inherited, and bounded to the legitimate scope.

### CON-04 — Role / Actor / Capability / Authority distinction

Physical Actor arrangement does not collapse or confuse these concepts.

Capability and access do not create Authority.

### CON-05 — Bounded Transition

The Transition Boundary is explicit enough to distinguish authorized mutation from escalation.

Subordinate Work Package Mutation Envelopes do not silently exceed it.

### CON-06 — Candidate non-authority

Produced state remains Candidate until authorized Acceptance and successful Baseline Establishment.

Build success, test success, merge, deployment or Actor assertion alone does not create Authoritative State.

### CON-07 — Claim-bound Verification

Verification identifies the claim, target and basis sufficiently to distinguish what was actually established.

### CON-08 — Evidence binding and visibility

Decision-relevant Evidence is bound to the relevant claims and state identity.

Relevant negative evidence and limitations are not silently removed.

### CON-09 — Verification / Acceptance separation

Verification Results are not substituted for Acceptance decisions.

Acceptance Authority does not rewrite Verification Results.

### CON-10 — Canonical Acceptance semantics

G8 uses the established Acceptance semantics:

- ACCEPT;
- REJECT;
- REPAIR REQUIRED;
- INCONCLUSIVE.

Unmet Required Claims are not hidden through an invented success state.

### CON-11 — Acceptance / Baseline Establishment separation

ACCEPT authorizes progression.

Only successful P9 Baseline Establishment creates the next Authoritative State.

### CON-12 — Explicit failure, repair and resumption

Failure, repair, interruption, recovery and resumption preserve the earliest-invalidated-phase rule and do not silently manufacture success.

### CON-13 — Traceability and provenance

Relevant relationships among Baseline, Contract, Candidate, Verification, Evidence, Acceptance, resulting state and Release where applicable remain reconstructable to the depth required by the claim.

### CON-14 — Secure Engineering by Construction

Security-relevant effects are handled as ordinary engineering properties and are not excluded merely for convenience.

### CON-15 — Tailoring integrity

Tailoring remains inside the Tailoring Envelope.

Semantic Compression may be used.

Control Deletion is not used.

### CON-16 — Assurance integrity

Assurance Conclusions remain distinct from Verification Results, Acceptance decisions and Authority.

Relevant uncertainty, deficiency and common-cause weakness remain visible to the required depth.

## 6. Conditional requirements

Some STATE elements are conditional by design.

Examples include:

- WP-10 Release Record where no Release occurs;
- release-specific provenance where nothing is released;
- Work Package decomposition where one undivided package is sufficient;
- strong independent Verification where Tailoring does not require it.

A conditionally absent element is not a nonconformance when:

- its triggering condition does not exist;
- the rationale is legitimate;
- no non-tailorable semantic is lost.

## 7. Criterion dispositions

Each applicable Conformance Requirement may receive one of four criterion dispositions:

### SATISFIED

Evidence sufficiently demonstrates the requirement.

### NOT SATISFIED

Evidence demonstrates that the requirement is violated or missing.

### INCONCLUSIVE

Available evidence cannot determine whether the requirement is satisfied.

### NOT APPLICABLE

The requirement or conditional element genuinely does not apply to the declared scope.

NOT APPLICABLE requires a legitimate scope rationale.

It is not a mechanism for avoiding an inconvenient requirement.

## 8. Overall Conformance Status

### CONFORMANT

All applicable CON-01 through CON-16 requirements are SATISFIED.

Any NOT APPLICABLE disposition is legitimate and documented to the degree required by the scope.

### NONCONFORMANT

At least one applicable Conformance Requirement is NOT SATISFIED.

### INCONCLUSIVE

No applicable requirement is known to be NOT SATISFIED, but one or more applicable requirements remain INCONCLUSIVE such that CONFORMANT cannot be established.

## 9. No partial conformance status

STATE does not define:

- PARTIALLY CONFORMANT;
- MOSTLY CONFORMANT;
- CONFORMANT WITH EXCEPTIONS;

as canonical overall statuses.

A scoped claim should instead be narrowed legitimately.

Example:

```text
NONCONFORMANT:
"the whole release process is STATE-conformant"

may coexist with

CONFORMANT:
"the source-transition portion through P9 is STATE-conformant"
```

if the scopes are explicit and evidence supports them.

## 10. Conformance evidence

Conformance evidence may reuse ordinary STATE Evidence.

A separate evidence universe is not required.

Relevant sources may include:

- Transition Contract;
- Authority Grants;
- Actor Assignments;
- Baseline Record;
- Transition Record;
- Verification Records;
- Evidence Set;
- Acceptance Record;
- Baseline Establishment Record;
- Release Record;
- Tailoring Decision;
- Assurance Case;
- logs, diffs, manifests and provenance records.

## 11. Conformance Assessment Record

A Conformance assessment is a logical record and does not create WP-12.

Where explicit representation is needed, it shall be capable of representing:

### CAR-01 — Assessment Identity

Identity of the assessment.

### CAR-02 — Conformance Scope Type

CS-01, CS-02 or CS-03.

### CAR-03 — Assessed Object

The Transition, Realization or Implementation in scope.

### CAR-04 — Baseline / Version Identity

The method and assessed-object version or state to which the assessment applies.

### CAR-05 — Applicable Tailoring

Tailoring profile, decision and assumptions relevant to the assessment.

### CAR-06 — Requirement Dispositions

Disposition for applicable CON-01 through CON-16 requirements.

### CAR-07 — Evidence References

Evidence supporting the criterion dispositions.

### CAR-08 — Nonconformities

Explicit NOT SATISFIED requirements and rationale.

### CAR-09 — Inconclusive Items

Applicable requirements that cannot yet be resolved.

### CAR-10 — Not-Applicable Rationale

Rationale for material NOT APPLICABLE dispositions.

### CAR-11 — Overall Status

CONFORMANT, NONCONFORMANT or INCONCLUSIVE.

### CAR-12 — Assessment Rationale

Why the criterion dispositions support the overall status.

### CAR-13 — Assessor Identity

Actor / Role performing the assessment.

### CAR-14 — Assessment Independence

Any relevant independence or common-cause relationship.

### CAR-15 — Temporal Validity

When or under which state / assumptions the assessment remains applicable.

### CAR-16 — Supersession / Reassessment Trigger

What change invalidates or supersedes the assessment.

## 12. Conformance and Tailoring

A Tailored Transition can be fully conformant.

Conformance evaluates whether the Tailoring preserved the invariants.

It does not compare every implementation against a maximum-control profile.

## 13. Conformance and Assurance

Conformance and Assurance are orthogonal but related.

Examples:

### Conformant + Assurance SUFFICIENT

The process preserved STATE semantics and the trust basis is sufficient.

### Conformant + Assurance INSUFFICIENT

The process preserved STATE semantics and correctly exposed that the trust basis is too weak.

This may lead to REPAIR REQUIRED, REJECT or INCONCLUSIVE.

### Nonconformant + technically successful result

The implementation may work, but the process cannot legitimately be described as a STATE-conformant Transition.

## 14. Conformance and physical realization

No Actor type, geography, sourcing arrangement, hardware platform, operating system, programming language, development environment or AI system is inherently conformant or nonconformant.

Conformance depends on how the physical realization preserves the logical method.

## 15. Conformance and automation

A fully automated workflow may be conformant when:

- Authority delegation is valid;
- state identity remains explicit;
- gate semantics are preserved;
- Verification and Evidence remain claim-bound;
- failure is explicit;
- Acceptance and Baseline Establishment semantics remain intact.

Manual human interaction is not a universal conformance condition.

Human-established governance remains the normative source of delegated authority.

## 16. Conformance and unsuccessful transitions

A conformant Transition may terminate without new Authoritative State.

Example:

```text
Baseline known
Specification valid
Authority bounded
Candidate produced
Verification FAIL
Evidence preserved
Acceptance REJECT
Previous Baseline remains authoritative
```

This is methodologically successful control of an unsuccessful Candidate.

## 17. Nonconformity correction

Correcting a nonconformity does not rewrite history.

A later conformant Transition or reassessment may supersede an earlier NONCONFORMANT status for a new scope or state.

The earlier assessment remains part of provenance where material.

## 18. Reassessment triggers

A Conformance assessment shall be reconsidered when material changes affect:

- method specification version;
- Tailoring;
- logical control semantics;
- Actor / Authority structure;
- automation;
- toolchain or environment where relevant;
- evidence mechanisms;
- Acceptance logic;
- Baseline Establishment logic;
- release handling;
- assessment scope.

## 19. No certification inference

An internal CONFORMANT status does not mean:

- certified organization;
- certified product;
- certified tool;
- externally accredited process;
- legal or regulatory compliance.

Those are separate claims outside this internal Conformance Model.

## 20. Canonical Conformance rules

> **STATE Conformance measures preservation of required control semantics, not engineering success.**

> **A conformant Transition may end in FAIL, REJECT, REPAIR REQUIRED, INCONCLUSIVE, HOLD or FAILED without losing Conformance.**

> **A technically successful result is not STATE-conformant merely because it works.**

> **All applicable Conformance Requirements shall be satisfied for CONFORMANT status.**

> **Semantic Compression may preserve Conformance; Control Deletion cannot.**

> **No partial-conformance status is used to hide an applicable unsatisfied requirement.**

> **A Conformance claim shall not be broader than its evidence and declared scope.**

> **Internal STATE Conformance is not organizational, product or tool certification.**

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.12  
Initial publication: 2026-08-13  
Last modified: 2026-08-13