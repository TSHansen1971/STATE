# Assurance Case and Confidence

> **Document:** `06-assurance/02-assurance-case-and-confidence.md`  
> **Title:** Assurance Case and Confidence  
> **Version:** 0.11  
> **Status:** Normative Specification
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


The Assurance Case provides the structured reasoning by which STATE connects an Assurance Objective to an Assurance Conclusion.

## 1. Assurance Case definition

> **An Assurance Case is the reconstructable structured argument connecting an Assurance Objective and scope to the claims, control basis, evidence, challenge, weaknesses, residual uncertainty and conclusion used to justify confidence.**

An Assurance Case is not a new Work Product class.

It may be embedded in existing STATE records or represented separately where useful.

## 2. Minimal reasoning chain

```text
ASSURANCE OBJECTIVE
        ↓
WHAT MUST BE TRUSTED?
        ↓
WHY SHOULD IT BE TRUSTED?
        ↓
WHAT EVIDENCE SUPPORTS THAT?
        ↓
WHAT COULD MAKE THIS WRONG?
        ↓
HOW WAS THAT CHALLENGED?
        ↓
WHAT UNCERTAINTY REMAINS?
        ↓
ASSURANCE CONCLUSION
```

## 3. Assurance Case fields

Where explicit representation is required, an Assurance Case shall be capable of representing the following.

### ACASE-01 — Case Identity

Identity of the Assurance Case or Assurance evaluation.

### ACASE-02 — Assurance Objective

Which AO objective or equivalent defined assurance purpose is being evaluated.

### ACASE-03 — Scope

Which Transition, Candidate, claim, decision, Release or recurring process is in scope.

### ACASE-04 — Required Assurance Depth

The expected strength of the trust basis selected through Tailoring.

### ACASE-05 — Primary Claim or Decision

The engineering assertion or authority decision whose basis is being assured.

### ACASE-06 — Supporting Control Basis

Relevant Authority, specification, boundary, role assignment, process and environment controls.

### ACASE-07 — Verification Basis

Relevant Verification Claims, methods and results.

### ACASE-08 — Evidence Basis

Relevant Evidence Items and Evidence Sets.

### ACASE-09 — Independence / Challenge

How the basis was challenged for common-cause error.

### ACASE-10 — Known Weaknesses

Material Assurance Deficiencies or limitations.

### ACASE-11 — Negative Evidence

Decision-relevant contrary observations or failures.

### ACASE-12 — Residual Uncertainty

What remains unknown or uncertain.

### ACASE-13 — Assumptions

Material assumptions on which confidence depends.

### ACASE-14 — Conclusion

SUFFICIENT, INSUFFICIENT or INCONCLUSIVE.

### ACASE-15 — Conclusion Rationale

Why the basis supports the conclusion at the selected depth.

### ACASE-16 — Assurer Identity

The Role / Actor responsible for the Assurance conclusion where explicit assignment is required.

## 4. Assurance argument

An Assurance argument is not stronger because it is longer.

It is stronger when the relationship between:

- claim;
- method;
- evidence;
- challenge;
- limitation;
- uncertainty;

is more justified.

## 5. Confidence

STATE uses **confidence** as a property of justified belief in the adequacy of the assurance basis.

Confidence is not a numeric probability unless a Tailoring context legitimately defines one.

STATE does not require universal quantitative confidence scoring.

## 6. Confidence contributors

Confidence may be strengthened by:

- precise claims;
- strong state identity;
- fit-for-purpose Verification Methods;
- high-quality Evidence;
- reproducibility;
- independent challenge;
- coherent provenance;
- explicit limitations;
- successful recovery / failure tests;
- stable recurring process evidence.

## 7. Confidence reducers

Confidence may be reduced by:

- ambiguous target identity;
- weak evidence provenance;
- untested interaction;
- hidden environment dependency;
- common-cause tool failure;
- stale evidence;
- unexplained negative evidence;
- unjustified Tailoring reduction;
- Actor substitution without reassessment;
- unresolved residual uncertainty.

## 8. Confidence is not transitive by default

If claim A is well assured and claim B depends on A, B is not automatically well assured.

The dependency and additional basis for B must be evaluated.

Likewise:

```text
Component A assured
Component B assured
≠
Integrated system assured
```

unless the integration relationship is itself assured.

## 9. Assurance challenge

**Assurance Challenge** is the deliberate attempt to identify why a claim or confidence argument may be wrong.

Challenge may use:

- independent review;
- alternate Verification Method;
- alternate tool;
- alternate environment;
- counterexample search;
- negative testing;
- provenance reconstruction;
- assumption review;
- failure injection;
- adversarial reasoning.

The selected challenge should target the relevant failure source.

## 10. Confidence without independence

Independence is not mandatory at maximum strength for every Transition.

A compact low-consequence Transition may legitimately rely on one Actor.

Confidence can still be justified through:

- reproducible evidence;
- deterministic checks;
- clear state identity;
- narrow scope;
- strong reversibility;
- low consequence.

The Tailoring basis should make this proportionality credible.

## 11. Residual uncertainty

Residual uncertainty remains after all practical Verification and Assurance.

The Assurance Case shall distinguish between:

- uncertainty known and bounded;
- uncertainty known but not bounded;
- uncertainty discovered through negative evidence;
- uncertainty created by environment, Actor or external dependency;
- uncertainty that materially blocks a conclusion.

## 12. Assumption visibility

An assurance argument that depends on an assumption should identify it when failure of the assumption would materially change the conclusion.

Assumptions are not Evidence.

They are conditions on the validity of the argument.

## 13. Assurance Case compression

A low-consequence Assurance Case may be compact:

```text
Objective: AO-06 Verification Adequacy
Scope: Candidate C4 documentation rendering
Basis: exact diff + rendered inspection
Challenge: independent visual review
Uncertainty: none material identified
Conclusion: SUFFICIENT
```

A high-consequence case may require extensive structured evidence.

Both can implement the same logical model.

## 14. Assurance Case update

A prior Assurance Case shall be reconsidered when:

- Candidate changes materially;
- Contract changes;
- Tailoring changes;
- Actor / tool / environment changes materially;
- evidence changes;
- new negative evidence appears;
- Release representation changes;
- re-tailoring trigger occurs.

## 15. Canonical Assurance Case rules

> **An Assurance Case is a structured confidence argument, not a document-count requirement.**

> **Assumptions are not Evidence.**

> **Confidence is claim- and scope-relative.**

> **Confidence does not automatically compose from parts to system.**

> **Assurance Challenge should target plausible common-cause or decision-relevant failure.**

> **Residual uncertainty shall remain visible when it is material to the conclusion.**

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.11  
Initial publication: 2026-08-13  
Last modified: 2026-08-13