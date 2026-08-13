# Foundational Properties

> **Document:** `02-what-conceptual/02-foundational-properties.md`  
> **Title:** Foundational Properties  
> **Version:** 0.2  
> **Status:** Foundational Working Specification  
> **Created:** 2026-08-11  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


The Foundational Properties define characteristics that are constitutive of STATE Engineering. Detailed practices may be tailored, but these properties cannot be silently removed without changing the nature of the method.

## FP-01 — Controlled State Transition

> **Software and systems engineering are governed as controlled transitions between sufficiently identified system states.**

The primary methodological unit is the authorized transition, not the production of a code fragment or other implementation artifact.

## FP-02 — Known Authoritative State

> **Every controlled transition begins from a sufficiently identified authoritative state.**

The required identity depth is proportionate to the claim being made. A source commit may be sufficient for one transition; another may require configuration, environment, dependency or artifact identity in addition.

## FP-03 — Specification before Mutation

> **The intended change, relevant constraints, invariants and acceptance basis are established before the resulting mutation is accepted as authoritative.**

Implementation may legitimately refine understanding. It may not silently redefine the purpose against which it will later be judged.

## FP-04 — Explicit and Bounded Authority

> **Every transition operates within established authority and explicit boundaries.**

Discovery outside the boundary does not create authorization to mutate outside it.

## FP-05 — Actor Independence

> **Roles and responsibilities are defined independently of whether the performing actor is human, synthetic or hybrid.**

The method remains logically stable when execution capacity is reassigned, provided the replacement satisfies the role's capability, authority, traceability and assurance requirements.

## FP-06 — Separation of Role, Actor, Capability and Authority

> **Function, performer, capability and permission are distinct engineering concepts.**

Capability does not create authority. Technical access does not by itself establish legitimate decision rights.

## FP-07 — Candidate before Authority

> **A produced state remains a candidate until an authorized acceptance process establishes it as authoritative.**

Successful generation, compilation, execution or local plausibility does not itself establish authority.

## FP-08 — Traceability by Construction

> **The relevant relationship among intent, baseline, authorization, transformation, verification, evidence, decision and resulting state shall be reconstructable.**

Traceability is a property of the method, not an optional documentation exercise performed only after problems occur.

## FP-09 — Evidence-Based Acceptance

> **Acceptance shall be supported by evidence appropriate to the claim being accepted.**

Evidence sufficiency depends on the strength, scope, consequence and uncertainty of the claim.

## FP-10 — Secure Engineering by Construction

> **Generally applicable secure software and systems engineering principles are intrinsic to STATE Engineering and operate across all abstraction levels.**

Security-relevant requirements, boundaries, trust assumptions, failure behavior and verification obligations are considered as part of ordinary engineering rather than as a separate late lifecycle.

## FP-11 — Explicit Failure

> **FAIL and INCONCLUSIVE are valid engineering outcomes and shall not be silently transformed into PASS.**

Tests, scope, evidence thresholds or claims shall not be weakened without an explicit authorized change to the acceptance basis.

## FP-12 — Secure Modification

> **Modification shall preserve the degree of rigor required for properties and assurances intended to survive the transition.**

A change that affects authority, trust, privilege, dependency, external exposure, failure behavior, provenance or another security-relevant property requires verification appropriate to that effect.

## Relationship to the Universal Engineering Principles

The Foundational Properties define what must remain true about the method.

The **Universal Engineering Principles (UEP)** define general engineering behavior that supports those properties across the Contextual, Conceptual, Logical and Physical layers.

Foundational Properties are therefore constitutive. Universal Engineering Principles are normative engineering guidance used to realize and preserve them.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.2  
Initial publication: 2026-08-11  
Last modified: 2026-08-13
