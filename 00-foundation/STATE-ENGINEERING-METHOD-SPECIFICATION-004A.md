# STATE Engineering Method Specification 004A

> **Document:** `00-foundation/STATE-ENGINEERING-METHOD-SPECIFICATION-004A.md`  
> **Title:** STATE Engineering Method Specification 004A  
> **Version:** 0.4  
> **Status:** Historical Superseded Specification
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


## 1. Purpose

STATE Engineering is a method for controlled software and systems engineering in environments where realization work may be delegated across human, synthetic or hybrid execution capacity.

The method treats engineering primarily as the controlled Transition of a system from one sufficiently identified Authoritative State to another.

This specification supersedes `STATE-ENGINEERING-METHOD-SPECIFICATION-003A.md` as the current foundational specification while retaining previous specifications as publication history.

## 2. Canonical definition

> **STATE Engineering is a specification-driven, actor-independent, human-governed, traceable and evidence-based engineering method for controlling transitions between authoritative system states.**

## 3. STATE

The method name expresses five core concepts:

- **S — Specification**
- **T — Transition**
- **A — Authority**
- **T — Traceability**
- **E — Evidence**

## 4. Four abstraction levels

### WHY — Contextual

Defines the engineering context and control problem.

### WHAT — Conceptual

Defines state, transition, authority, role, responsibility, actor, capability, Work Products, evidence, acceptance, boundaries, invariants, trust and provenance.

### HOW — Logical

Defines how STATE operates independently of a particular technical realization.

### WITH WHAT — Physical

Defines concrete realization through human capital, synthetic capital, hybrid arrangements, hardware and software.

## 5. Method-control domains

STATE uses:

- **Tailoring**
- **Assurance**
- **Reference**

across and after the four abstraction levels.

## 6. Foundational Properties

STATE defines twelve Foundational Properties:

1. Controlled State Transition
2. Known Authoritative State
3. Specification before Mutation
4. Explicit and Bounded Authority
5. Actor Independence
6. Separation of Role, Actor, Capability and Authority
7. Candidate before Authority
8. Traceability by Construction
9. Evidence-Based Acceptance
10. Secure Engineering by Construction
11. Explicit Failure
12. Secure Modification

## 7. Universal Engineering Principles

STATE defines twelve Universal Engineering Principles:

1. Clear and Controlled Abstraction
2. Minimize Unnecessary Coupling, Sharing and Surface
3. Least Authority
4. Explicit Mediation and Permission
5. Structured Trust
6. Secure Evolvability and Continuous Protection
7. Secure Failure and Recoverability
8. Accountability, Traceability and Provenance
9. Verification by Design
10. Security-Relevant Change Requires Security-Relevant Verification
11. Actor-Appropriate Engineering Controls
12. Proportional and Explicit Rigor

## 8. Role / Actor / Capability / Authority model

STATE separates:

- Role;
- Responsibility;
- Actor;
- Capability;
- Authority.

Capability does not create authority.

Actor substitution does not silently change the control model.

## 9. Authority domains

STATE defines:

1. Intent Authority
2. Architecture Authority
3. Transition Authority
4. Acceptance Authority
5. Release Authority

## 10. Logical roles

STATE defines:

1. Specification Role
2. Realization Role
3. Verification Role
4. Evidence Stewardship Role
5. Baseline Custodianship Role
6. Assurance Role

## 11. Authority Grants and Actor Assignments

Authority shall be explicit or explicitly inherited.

Actor Assignments bind actual Actors to logical Roles and applicable Authority Grants.

Delegated authority remains traceable to a human-established governance source.

## 12. Work Product model

STATE defines logical Work Products as information obligations.

A logical Work Product does not imply a mandatory separate physical document.

STATE currently defines:

### WP-01 — Transition Intent and Specification

Defines intended outcome, constraints, invariants, non-goals and Acceptance basis.

### WP-02 — Authority Grant

Establishes bounded authority for decision, approval or mutation.

### WP-03 — Actor Assignment

Binds actual Actors to logical Roles and authority.

### WP-04 — Baseline Record

Identifies the Authoritative State used as Transition input.

### WP-05 — Transition Record

Provides the central traceability relationship among baseline, specification, authority, actors, mutation, verification, evidence, decision and resulting state.

### WP-06 — Verification Record

Records claim, method, observation, evidence, conclusion and limitations.

### WP-07 — Evidence Set

Binds Evidence Items to engineering claims.

### WP-08 — Acceptance Record

Records ACCEPT, REJECT, REPAIR REQUIRED or INCONCLUSIVE decision.

### WP-09 — Baseline Establishment Record

Establishes an accepted state as the next Authoritative State.

### WP-10 — Release Record

Records release when release is a distinct act.

### WP-11 — Deviation and Escalation Record

Records material deviation, escalation, authority uncertainty or accepted exception when applicable.

## 13. Physical representation rule

Logical Work Products define required information, not mandatory file counts.

Multiple Work Products may share one physical representation when required distinctions and traceability remain reconstructable.

One Work Product may also be distributed across multiple controlled physical records.

Tailoring determines representation depth.

## 14. Evidence Item

An Evidence Item is an identifiable observation, artifact, record or measurement used to support or challenge an engineering claim.

Evidence is claim-bound.

Its presence alone does not establish sufficiency.

## 15. Evidence classes

STATE defines ten Evidence Classes:

1. Identity Evidence
2. Authority Evidence
3. Transformation Evidence
4. Construction and Build Evidence
5. Behavioral Evidence
6. Regression and Preservation Evidence
7. Security and Boundary Evidence
8. Environment Evidence
9. Provenance and Integrity Evidence
10. Decision Evidence

## 16. Evidence-quality properties

Evidence is evaluated, where relevant, through:

1. Relevance
2. Identity
3. Integrity
4. Provenance
5. Sufficiency
6. Reproducibility
7. Independence
8. Timeliness
9. Preservation

Not every claim requires equal depth across every property.

## 17. Claim–Evidence Binding

A Verification Record should establish:

- claim;
- method;
- observation;
- Evidence Items;
- conclusion;
- limitations.

> **Evidence shall be bound to claims, states and decisions rather than accumulated without purpose.**

## 18. Evidence sufficiency

Evidence sufficiency is proportional to:

- claim strength;
- consequence of error;
- uncertainty;
- reversibility;
- applicable Assurance objective.

A large quantity of irrelevant evidence is not sufficient evidence.

## 19. Negative evidence

Evidence that supports FAIL or INCONCLUSIVE outcomes remains valid engineering evidence.

Relevant negative evidence shall not be discarded merely because it does not support Acceptance.

## 20. Minimal Transition information set

A STATE Transition shall be capable of answering:

1. What was the authoritative input state?
2. What was intended to change?
3. What was authorized to change?
4. Which Actors performed which logical Roles?
5. What actually changed?
6. What claims were verified?
7. What evidence supports or challenges those claims?
8. What was the decision?
9. What state, if any, became the new authoritative baseline?

## 21. Controlled transition

A STATE Transition begins from an identifiable Authoritative State and establishes, as applicable:

1. intended change;
2. authorized Transition Boundary;
3. relevant invariants;
4. implementation context;
5. Candidate State;
6. execution observations;
7. verification result;
8. evidence;
9. Acceptance decision;
10. resulting Authoritative State, if accepted.

## 22. Candidate before authority

A newly produced state is a Candidate State.

Successful production, compilation, execution or plausibility does not by itself establish authority.

## 23. Acceptance and baseline establishment

Acceptance and baseline establishment are separate logical acts.

> **An accepted Candidate State does not become the next Authoritative State until baseline establishment is explicit.**

## 24. Release integrity

Where release is distinct from Acceptance, the released artifact or deployed state shall be traceable to the accepted state to the degree required by the release claim.

## 25. Secure Engineering by Construction

Generally applicable and domain-neutral secure software and systems engineering principles remain intrinsic to STATE Engineering.

Security-relevant claims require security-relevant verification and evidence.

## 26. Domain boundary

Jurisdiction-, sector-, mission-, organization- and contract-specific obligations remain outside the universal STATE core and may be introduced through Tailoring.

## 27. Canonical rules

> **Capability does not create authority.**

> **Responsibilities belong to Roles before they belong to Actors.**

> **Actor substitution shall not silently change the control model.**

> **Logical Work Products define information obligations, not mandatory file counts.**

> **Evidence shall be bound to claims, states and decisions rather than accumulated without purpose.**

> **A verification result shall identify what was verified and the evidence on which the result depends.**

> **Evidence sufficiency is proportional to claim strength, consequence and residual uncertainty.**

> **An accepted Candidate State does not become a baseline until baseline establishment is explicit.**

> **A released artifact shall be traceable to the accepted state when release integrity is part of the claim.**

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.4  
Initial publication: 2026-08-13  
Last modified: 2026-08-13