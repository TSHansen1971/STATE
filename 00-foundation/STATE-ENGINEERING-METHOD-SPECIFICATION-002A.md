# STATE Engineering Method Specification 002A

> **Document:** `00-foundation/STATE-ENGINEERING-METHOD-SPECIFICATION-002A.md`  
> **Title:** STATE Engineering Method Specification 002A  
> **Version:** 0.2  
> **Status:** Historical Superseded Specification
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


## 1. Purpose

STATE Engineering is a method for controlled software and systems engineering in environments where realization work may be delegated across human, synthetic or hybrid execution capacity.

The method treats engineering primarily as the controlled transition of a system from one sufficiently identified authoritative state to another.

A change is not complete merely because code was written, generated, compiled or executed. A transition is complete only when the resulting candidate state has been evaluated against its authorized intent and the required evidence supports an explicit acceptance decision.

This specification supersedes `STATE-ENGINEERING-METHOD-SPECIFICATION-001A.md` as the current foundational specification while retaining the earlier file as public publication history.

## 2. Canonical definition

> **STATE Engineering is a specification-driven, actor-independent, human-governed, traceable and evidence-based engineering method for controlling transitions between authoritative system states.**

Human-governed means that normative authority over intended system state remains humanly established even when execution, inspection, verification or other roles are delegated through policy or automation.

## 3. STATE

The method name expresses five core concepts:

- **S — Specification**
- **T — Transition**
- **A — Authority**
- **T — Traceability**
- **E — Evidence**

These concepts are mutually dependent. A transition without specification cannot be evaluated against intent. Specification without authority cannot define an authorized change. Authority without traceability cannot be reliably reconstructed. Traceability without evidence cannot support acceptance.

## 4. Four abstraction levels

STATE is described through four abstraction levels:

### WHY — Contextual

Defines the engineering context and the control problem that makes STATE necessary.

### WHAT — Conceptual

Defines the ontology and foundational properties of STATE, including state, transition, authority, candidate, evidence, acceptance, role, actor, capability, boundary, invariant, trust and provenance.

### HOW — Logical

Defines how STATE operates independently of a particular technical realization.

### WITH WHAT — Physical

Defines how the logical method is instantiated through concrete human capital, synthetic capital, hybrid teams, hardware, software, development environments, execution systems and verification mechanisms.

## 5. Method-control domains

Three domains operate across and after the four abstraction levels:

- **Tailoring**
- **Assurance**
- **Reference**

Tailoring adapts implementation while preserving defining method properties. Assurance establishes whether claims and transitions deserve trust. Reference preserves the normative vocabulary, records, templates and methodological rationale.

## 6. Foundational Properties

STATE Engineering currently defines twelve Foundational Properties:

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

STATE Engineering currently defines twelve Universal Engineering Principles:

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

These principles apply across the four abstraction levels and provide general engineering guidance for preserving the Foundational Properties.

## 8. Actor independence

STATE roles are defined independently of the nature of the actor performing them.

A role may be realized by an individual human, a local or distributed team, a specialist supplier, an automated system, an AI model, an autonomous agent, a multi-agent system or a hybrid arrangement.

Actor substitution does not silently alter the authority or control model.

## 9. Role, actor, capability and authority

STATE separates four concepts:

**Role** — the function that must be performed.

**Actor** — the human, synthetic or hybrid entity performing the role.

**Capability** — what the actor is technically or operationally able to do.

**Authority** — what the actor is permitted to decide, approve or change.

Capability does not create authority.

## 10. Controlled transition

A STATE transition begins from an identifiable authoritative state and establishes, as applicable:

1. intended change;
2. authorized transition boundary;
3. relevant invariants;
4. implementation context;
5. candidate state;
6. execution observations;
7. verification result;
8. evidence;
9. acceptance decision;
10. resulting authoritative state, if accepted.

Production and acceptance are separate operations.

## 11. Candidate before authority

A newly produced state is a candidate.

Successful generation, compilation, execution or local plausibility does not by itself establish authority.

The candidate becomes authoritative only through an authorized acceptance process supported by relevant evidence.

## 12. Traceability by construction

The relevant relationship among the following elements shall be reconstructable:

```text
Intent
  ↓
Specification
  ↓
Authoritative baseline
  ↓
Authorized transition
  ↓
Candidate
  ↓
Verification
  ↓
Evidence
  ↓
Acceptance decision
  ↓
Resulting authoritative state
```

The required degree of traceability is proportionate to the strength and consequence of the claim being accepted.

## 13. Evidence-based acceptance

Acceptance is an engineering claim about a system state.

The evidence required to support that claim shall be relevant to the claim itself.

A successful build is evidence of successful build behavior. It is not automatically evidence that all intended product behavior, security properties, invariants or release-integrity claims are satisfied.

## 14. Secure Engineering by Construction

Generally applicable and domain-neutral secure software and systems engineering principles are intrinsic to STATE Engineering.

They apply through specification, design, transition definition, realization, verification, modification, evidence and acceptance.

Security is not treated as a separate lifecycle appended after functional engineering.

Context-bound legal, regulatory, jurisdictional, mission, organizational or sector requirements are outside the universal method core and may be introduced through Tailoring when applicable.

## 15. Security-relevant transitions

A transition that can materially affect authority, privilege, trust, exposure, dependency, protected communication, execution environment, failure behavior, auditability, provenance or release integrity shall include verification appropriate to the affected security claim.

Functional success does not establish preservation of unrelated security properties.

## 16. Failure

FAIL and INCONCLUSIVE are valid engineering outcomes.

A failed or inconclusive candidate does not become an authoritative baseline merely because engineering work has already been performed.

Acceptance criteria, scope or claims shall not be silently weakened to convert failure into success.

## 17. Secure modification

Modification of an accepted system shall preserve the degree of rigor necessary for properties and assurances intended to survive that modification.

The verification burden is therefore a function not only of what is added, but also of what the transition claims to preserve.

## 18. Source discipline

STATE uses directly relevant authoritative engineering knowledge as methodological input while retaining its own native structure.

The method shall not be organized as a compliance crosswalk.

The Methodological Source Register records source provenance and rationale for principles absorbed into STATE.

## 19. Canonical acceptance rule

> **No generated or implemented change becomes authoritative merely because it was produced successfully. A candidate state becomes authoritative only when its relevant origin, scope, effects and required properties have been sufficiently verified against an identified baseline and accepted through an authorized decision process.**

## 20. Canonical governance rule

> **Capability does not create authority, and actor substitution does not silently change the control model.**

## 21. Canonical secure-modification rule

> **A transition shall be verified not only for the behavior it intends to add or change, but also for the relevant properties it claims to preserve.**

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.2  
Initial publication: 2026-08-13  
Last modified: 2026-08-13