# STATE Engineering — Method Positioning

> **Document:** `01-why-contextual/02-method-positioning.md`
> **Title:** STATE Engineering — Method Positioning
> **Version:** 001A
> **Status:** Current Documentation
> **Created:** 2026-08-13
> **Last modified:** 2026-08-13
> **Author:** Tor-Ståle Hansen
> **Co-authors:** None

## 1. Purpose

This document explains what STATE Engineering is and is not using STATE's own control semantics.

It is contextual and explanatory.

It does not define a comparative framework crosswalk and does not make an external method, lifecycle or compliance structure part of STATE.

## 2. Positive position

STATE Engineering is an **engineering control method for authorized transitions between sufficiently identified authoritative system states**.

Its control problem is not primarily how to maximize artifact production.

Its control problem is how to preserve legitimate intent, boundaries, Authority, identity, Verification, Evidence, Acceptance and recovery when realization can be delegated to Actors with substantial technical Capability.

STATE is therefore centered on the controlled relationship among:

- Specification;
- Transition;
- Authority;
- Traceability;
- Evidence;
- Candidate identity;
- Verification;
- Acceptance;
- Baseline Establishment.

These are STATE-native concerns.

The owner-approved canonical decomposition of the name is reserved for explicit integration under WP20. This WP13 positioning document does not pre-empt that integration.

## 3. Engineering control method

STATE controls an engineering Transition from an Authoritative Baseline through bounded realization, claim-bound Verification, Evidence and authorized Acceptance to explicit Baseline Establishment.

It makes the control chain reconstructable:

```text
AUTHORIZED BASELINE
→ SPECIFIED TRANSITION
→ BOUNDED REALIZATION
→ CANDIDATE
→ VERIFICATION
→ EVIDENCE
→ ACCEPTANCE
→ NEW AUTHORIZED BASELINE
```

The method does not assume that artifact production itself creates Authority.

## 4. Actor-independent

STATE separates logical Role, physical Actor, technical Capability, access/permission and Authority.

A Role can be performed by:

- a human;
- a team;
- deterministic automation;
- an AI system;
- an autonomous agent;
- a mixed human/AI arrangement;
- an external supplier.

Actor substitution is valid only when the replacement has sufficient Capability and legitimate Authority for the assignment.

> **Capability does not create Authority.**

## 5. Lifecycle-agnostic

STATE does not require one specific development lifecycle.

A Transition can occur inside iterative, sequential, continuous, event-driven or other engineering arrangements.

The external cadence does not replace the internal STATE controls required for the Transition.

STATE therefore governs **the controlled change**, not the organization's preferred calendar or lifecycle vocabulary.

## 6. Organizational-topology-agnostic

STATE does not depend on a particular organization chart.

Intent Authority, Architecture Authority, Transition Authority, Realization, Verification, Evidence Stewardship, Acceptance and Baseline Custodianship may be distributed across one or many organizational units when legitimate Authority and control separation remain reconstructable.

The method applies to local, distributed, supplier, automated and hybrid arrangements.

## 7. Technology-agnostic

STATE does not depend on a particular programming language, repository, build system, model provider, cloud platform or toolchain.

Physical technology matters when it affects Capability, provenance, Evidence, reproducibility, security, Verification or Assurance.

Technology does not define the logical method.

## 8. Applicable to human, automated and AI realization

AI is a realization form inside the general Actor model.

STATE does not require an AI governance overlay to explain the difference between:

- Capability and Authority;
- Candidate and authoritative state;
- self-assessment and Acceptance;
- tool use and legitimate scope;
- stochastic output and claim-bound Evidence.

The same control semantics apply across Actor classes.

## 9. What STATE is not

STATE is not:

- a lifecycle process catalogue;
- a project-management method;
- a software-development methodology;
- a compliance framework;
- an organizational maturity model;
- an AI governance overlay;
- a replacement for domain engineering knowledge.

Those categories may coexist with STATE in a real engineering environment.

They do not define STATE.

## 10. Domain knowledge remains necessary

STATE controls how authorized engineering change is specified, bounded, realized, verified, evidenced, accepted and established.

It does not replace the technical knowledge needed to decide what a correct bridge, aircraft component, cryptographic protocol, user interface, medical device, database, network or software subsystem should actually do.

Domain-specific requirements enter the Transition as scoped engineering demand, constraints, Verification needs and Tailoring context.

## 11. Secure engineering is cross-cutting

Secure engineering is part of the method's cross-cutting engineering foundation.

It is not deferred to a final compliance activity.

Security-relevant intent, architecture, boundaries, least privilege, change control, Verification, Evidence, failure behavior, provenance and Acceptance are addressed at the control points where they are materially relevant.

## 12. Positioning conclusion

STATE's distinguishing concern is controlled engineering state transition under explicit Authority and Evidence.

Its ambition is not to replace every engineering practice around the Transition.

Its ambition is to make the Transition itself governable and reconstructable.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 001A  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
