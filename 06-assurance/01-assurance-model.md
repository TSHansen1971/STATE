# Assurance Model

> **Document:** `06-assurance/01-assurance-model.md`  
> **Title:** Assurance Model  
> **Version:** 0.11  
> **Status:** Normative Specification
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


The Assurance Model defines how STATE evaluates the trustworthiness of the basis for engineering claims and authority decisions.

## 1. Assurance definition

> **Assurance is the structured evaluation of whether the control, verification, evidence, independence and uncertainty basis supporting a defined engineering claim or decision is sufficient for the applicable consequence and Assurance objective.**

Assurance is not a guarantee.

It is a justified confidence judgment.

## 2. Assurance object

Assurance always has a scope.

It may apply to:

- one Verification Claim;
- one Acceptance Claim Set;
- a Work Package;
- an Integrated Candidate;
- a Transition;
- a Tailoring Decision;
- Baseline Establishment;
- a Release;
- source-to-artifact provenance;
- a class of recurring Transitions.

An Assurance statement without scope is weak.

## 3. Assurance Objectives

STATE defines twelve Assurance Objectives.

Not every Transition requires every objective at the same depth.

### AO-01 — Authority Validity

Establish confidence that the relevant Authority Grants, delegations and decision scopes are legitimate and current.

### AO-02 — State Identity Integrity

Establish confidence that Baseline, Candidate, accepted state, established state and released object identities are sufficiently distinguished.

### AO-03 — Specification Adequacy

Establish confidence that the intended change and Acceptance basis are sufficiently explicit to govern implementation and decision.

### AO-04 — Boundary Adequacy

Establish confidence that the Transition Boundary and subordinate Mutation Envelopes sufficiently constrain mutation and escalation.

### AO-05 — Physical Realization Fitness

Establish confidence that assigned Actors, tools, access and environments are capable of performing their logical Roles without silently expanding Authority.

### AO-06 — Verification Adequacy

Establish confidence that Verification Claims, methods, conditions, coverage and limitations are sufficient for the assertions being made.

### AO-07 — Evidence Adequacy

Establish confidence that Evidence Items are relevant, identifiable, integral, sufficiently complete and correctly bound to the claims and state.

### AO-08 — Independence Adequacy

Establish confidence that common-cause error is challenged to the degree required by consequence and uncertainty.

### AO-09 — Tailoring Adequacy

Establish confidence that the selected Tailoring remains within the Tailoring Envelope and has not deleted required control semantics.

### AO-10 — Failure and Recovery Adequacy

Establish confidence that failure, repair, interruption, resumption and rollback preserve authoritative-state integrity.

### AO-11 — Decision Adequacy

Establish confidence that Acceptance, Baseline Establishment and Release decisions use the correct scope, Authority and evidentiary basis.

### AO-12 — Provenance Adequacy

Establish confidence that required source, transformation, Actor, environment, evidence, decision and distribution relationships remain reconstructable.

## 4. Assurance Conclusion

STATE defines exactly three canonical Assurance Conclusions.

### SUFFICIENT

The evaluated basis is sufficient for the defined Assurance Objective, scope and depth.

### INSUFFICIENT

The evaluated basis is demonstrably too weak or contains an unresolved deficiency incompatible with the required Assurance Objective.

### INCONCLUSIVE

Available information is insufficient to conclude either SUFFICIENT or INSUFFICIENT.

## 5. Assurance Conclusion is bounded

A SUFFICIENT conclusion applies only to:

- the Assurance Objective;
- scope;
- claims / decisions;
- evidence basis;
- Tailoring assumptions;
- environment and temporal context where relevant.

It is not a universal quality certificate.

## 6. Assurance versus Verification

Verification produces claim-level results:

- PASS;
- FAIL;
- INCONCLUSIVE.

Assurance produces trust-basis conclusions:

- SUFFICIENT;
- INSUFFICIENT;
- INCONCLUSIVE.

A Verification PASS can coexist with Assurance INSUFFICIENT.

Example:

```text
test result = PASS
but
target identity = ambiguous
evidence provenance = weak
independence = insufficient

therefore
Verification Result = PASS
Assurance Conclusion = INSUFFICIENT
```

The PASS is not rewritten.

The trust placed in that PASS is limited.

## 7. Assurance versus Acceptance

Acceptance Authority may use an Assurance conclusion as part of its decision basis.

Assurance does not itself decide ACCEPT.

An Assurance Actor cannot override Acceptance Authority merely by asserting confidence.

Likewise Acceptance Authority cannot declare weak Verification trustworthy simply by choosing ACCEPT.

## 8. Assurance versus Authority

> **Assurance evaluates a basis; it does not create Authority.**

A highly trusted Actor still requires valid Authority for the relevant decision.

A low-trust or insufficiently assured process cannot acquire Authority merely because the outcome appears correct.

## 9. Assurance Basis

An Assurance Basis may include:

- relevant claims;
- Verification Records;
- Evidence Sets;
- Authority Grants;
- Transition Contract;
- Tailoring Decision;
- Actor Assignments;
- environment identity;
- provenance;
- failure records;
- independent challenge;
- prior recurring evidence where legitimately reusable.

## 10. Assurance sufficiency properties

STATE defines ten Assurance Sufficiency Properties.

### ASP-01 — Scope Clarity

The Assurance scope and objective are explicit.

### ASP-02 — Identity Coherence

The claims, evidence and decisions refer to the correct state and objects.

### ASP-03 — Evidence Relevance

Evidence actually bears on the claim or decision being assured.

### ASP-04 — Evidence Integrity and Provenance

Evidence identity, integrity and origin are sufficient for the required confidence.

### ASP-05 — Method Adequacy

Verification and analytical methods can legitimately support the asserted conclusion.

### ASP-06 — Independence Adequacy

Common-cause error is challenged sufficiently.

### ASP-07 — Limitation Visibility

Known limitations and negative evidence are visible.

### ASP-08 — Residual Uncertainty Visibility

Material uncertainty is explicit rather than hidden.

### ASP-09 — Tailoring Validity

The selected control depth remains justified by the current context.

### ASP-10 — Decision Coherence

Authority, Verification, Evidence, Acceptance, Baseline Establishment and Release semantics remain consistent.

## 11. Assurance deficiency

An **Assurance Deficiency** is a weakness that reduces justified confidence.

Examples:

- ambiguous Candidate identity;
- evidence from a different revision;
- verification method unrelated to the actual claim;
- same Actor / tool combination presented as independent challenge;
- environment drift not assessed;
- hidden negative evidence;
- Tailoring profile applied outside assumptions;
- release artifact not linked to accepted state.

A deficiency may be:

- corrected;
- mitigated;
- bounded;
- accepted as residual uncertainty by appropriate authority;
- or sufficient to make the Assurance Conclusion INSUFFICIENT.

## 12. Assurance and negative evidence

Assurance actively considers decision-relevant negative evidence.

Confidence is not built by counting only supporting evidence.

A strong Assurance Basis explains why contrary evidence:

- invalidates the claim;
- requires repair;
- remains unresolved;
- or is legitimately non-governing.

## 13. Assurance and recurring controls

A recurring process may reuse prior Assurance work where:

- process identity remains valid;
- environment and toolchain remain within assumptions;
- Actors / authority remain valid;
- evidence mechanisms remain effective;
- re-tailoring triggers have not invalidated the profile.

Prior confidence is not permanent.

## 14. Canonical Assurance rules

> **Assurance evaluates whether a basis deserves trust; it does not create truth or Authority.**

> **A Verification Result and an Assurance Conclusion are different objects and shall not be substituted for one another.**

> **A SUFFICIENT Assurance Conclusion is bounded by objective, scope, evidence and assumptions.**

> **Assurance shall consider relevant negative evidence and residual uncertainty.**

> **Assurance cannot repair weak evidence by declaration.**

> **More ceremony is not more Assurance unless it strengthens the relevant trust basis.**

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-SA 4.0  
Version: 0.11  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
