# STATE Engineering Method Specification 003A

> **Document:** `00-foundation/STATE-ENGINEERING-METHOD-SPECIFICATION-003A.md`  
> **Title:** STATE Engineering Method Specification 003A  
> **Version:** 0.3  
> **Status:** Current Foundational Specification  
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


## 1. Purpose

STATE Engineering is a method for controlled software and systems engineering in environments where realization work may be delegated across human, synthetic or hybrid execution capacity.

The method treats engineering primarily as the controlled Transition of a system from one sufficiently identified Authoritative State to another.

A change is not complete merely because code or another implementation artifact was produced, compiled or executed. A Transition is complete only when the resulting Candidate State has been evaluated against its authorized intent and the required evidence supports an explicit Acceptance decision.

This specification supersedes `STATE-ENGINEERING-METHOD-SPECIFICATION-002A.md` as the current foundational specification while retaining previous specifications as publication history.

## 2. Canonical definition

> **STATE Engineering is a specification-driven, actor-independent, human-governed, traceable and evidence-based engineering method for controlling transitions between authoritative system states.**

Human-governed means that normative authority over intended system state remains humanly established even when execution, inspection, verification or other functions are delegated through policy, organization or automation.

## 3. STATE

The method name expresses five core concepts:

- **S — Specification**
- **T — Transition**
- **A — Authority**
- **T — Traceability**
- **E — Evidence**

These concepts are mutually dependent.

## 4. Four abstraction levels

STATE is described through four abstraction levels:

### WHY — Contextual

Defines the engineering context and the control problem that makes STATE necessary.

### WHAT — Conceptual

Defines the ontology and foundational properties of STATE, including state, transition, authority, role, responsibility, actor, capability, candidate, evidence, acceptance, boundary, invariant, trust and provenance.

### HOW — Logical

Defines how STATE operates independently of a particular technical realization.

### WITH WHAT — Physical

Defines how the logical method is instantiated through concrete human capital, synthetic capital, hybrid teams, hardware, software, execution systems and verification mechanisms.

## 5. Method-control domains

Three domains operate across and after the four abstraction levels:

- **Tailoring**
- **Assurance**
- **Reference**

## 6. Foundational Properties

STATE Engineering defines twelve Foundational Properties:

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

These properties are constitutive of the method.

## 7. Universal Engineering Principles

STATE Engineering defines twelve Universal Engineering Principles:

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

## 8. Actor-independent governance model

STATE separates:

- **Role** — the function that must be performed;
- **Responsibility** — what the role must produce, preserve, evaluate, decide or control;
- **Actor** — who or what performs the role;
- **Capability** — what that actor is able to do;
- **Authority** — what that actor is legitimately permitted to decide, approve or change.

Capability does not create authority.

Actor substitution does not silently change the control model.

## 9. Canonical authority domains

STATE defines five authority domains:

### AD-01 — Intent Authority

Governs intended outcomes and intent-level trade-offs.

### AD-02 — Architecture Authority

Governs structural rules, architecture boundaries and architectural invariants.

### AD-03 — Transition Authority

Governs what is allowed to change within a specific Transition.

### AD-04 — Acceptance Authority

Governs whether a Candidate State may become authoritative.

### AD-05 — Release Authority

Governs distribution, deployment or release where release is distinct from Acceptance.

Authority domains are logical decision-right categories. They are not prescribed organizational job titles.

## 10. Canonical logical roles

STATE defines six logical roles:

### LR-01 — Specification Role

Transforms approved intent and constraints into an operational transition specification.

### LR-02 — Realization Role

Produces the Candidate State within the authorized Transition Boundary.

### LR-03 — Verification Role

Evaluates claims about the Candidate State.

### LR-04 — Evidence Stewardship Role

Preserves evidence identity, linkage, provenance and availability.

### LR-05 — Baseline Custodianship Role

Maintains Authoritative State identity and continuity.

### LR-06 — Assurance Role

Evaluates adequacy of control, verification, evidence sufficiency and independence.

These roles may be assigned to human, synthetic or hybrid actors.

## 11. Authority Grants

Authority shall be established through explicit or explicitly inherited Authority Grants.

Where relevant to control, an Authority Grant identifies:

- authority source;
- authority domain;
- role or actor assignment;
- scope;
- permitted actions;
- constraints;
- validity;
- evidence obligations;
- escalation conditions;
- delegation conditions;
- revocation conditions.

The required documentary form is subject to Tailoring. The authority boundary itself shall not be ambiguous where it matters to the Transition.

## 12. Human-established authority root

Delegated authority shall remain traceable to a human-established governance source.

Automation and synthetic actors may exercise delegated authority.

They do not become an independent normative source merely because they can make or execute decisions.

> **Machine autonomy may increase without requiring an equivalent transfer of authority.**

## 13. No implicit authority escalation

Technical capability, access, discovery, historical practice or adjacent engineering need does not silently expand an Authority Grant.

Where an action exceeds the grant, the actor must escalate, obtain an amended grant or leave the action outside the current Transition.

## 14. Role combination

STATE requires logical role separation but does not require different physical actors for every role.

Physical role combination is a Tailoring and Assurance decision.

A single actor may perform several roles when the required assurance remains defensible.

Higher-consequence transitions may require independent actors, tools, methods or Acceptance Authority.

## 15. Mandatory logical distinctions

The following distinctions remain explicit even when performed by one actor:

- production is not verification;
- verification is not acceptance;
- acceptance is not baseline establishment;
- acceptance is not necessarily release.

## 16. Separation of duties

> **No actor shall accumulate authority and execution responsibilities in a way that defeats the assurance required for the Transition.**

This rule is proportional to consequence and uncertainty.

It is not a universal requirement for a different person in every role.

## 17. Controlled transition

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

## 18. Candidate before authority

A newly produced state is a Candidate State.

Successful production, compilation, execution or plausibility does not by itself establish authority.

## 19. Traceability by construction

The relevant relationship among intent, baseline, authorization, actor assignments, transformation, verification, evidence, decision and resulting state shall be reconstructable to the degree required by the accepted claim.

## 20. Evidence-based acceptance

Acceptance is an engineering claim about a system state.

The evidence required to support that claim shall be relevant to the claim itself.

## 21. Secure Engineering by Construction

Generally applicable and domain-neutral secure software and systems engineering principles are intrinsic to STATE Engineering.

Context-bound legal, regulatory, jurisdictional, mission, organizational or sector requirements remain outside the universal method core and may be introduced through Tailoring.

## 22. Failure

FAIL and INCONCLUSIVE are valid engineering outcomes.

A failed or inconclusive candidate does not become an Authoritative State.

## 23. Secure modification

Modification of an accepted system shall preserve the degree of rigor necessary for properties and assurances intended to survive that modification.

## 24. Work-product boundary

This specification defines the logical information required by the Role, Authority and Responsibility Model.

It does not yet prescribe the final Work Product forms used to record:

- Authority Grants;
- Actor Assignments;
- Transition Records;
- Evidence Packages;
- Acceptance Records;
- Baseline Records.

Those definitions belong to the subsequent Work Product and Evidence Model.

## 25. Canonical rules

> **Capability does not create authority.**

> **Responsibilities belong to roles before they belong to actors.**

> **Actor substitution shall not silently change the control model.**

> **Delegated authority shall remain traceable to a human-established governance source.**

> **Physical role combination may be tailored; logical role separation shall remain explicit.**

> **No actor shall accumulate authority and execution responsibilities in a way that defeats the assurance required for the Transition.**

> **No generated or implemented change becomes authoritative merely because it was produced successfully.**

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.3  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
