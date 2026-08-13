# STATE Engineering Method Specification 001A

> **Document:** `00-foundation/STATE-ENGINEERING-METHOD-SPECIFICATION-001A.md`  
> **Title:** STATE Engineering Method Specification 001A  
> **Version:** 0.1  
> **Status:** Historical Superseded Specification
> **Created:** 2026-08-11  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None

## 1. Purpose

STATE Engineering is a method for controlled software and systems engineering in environments where realization work may be delegated across human, synthetic or hybrid execution capacity.

The method treats engineering primarily as the controlled transition of a system from one sufficiently identified authoritative state to another.

A change is not complete merely because code was written, generated, compiled or executed. A transition is complete only when the resulting candidate state has been evaluated against its authorized intent and the required evidence supports an explicit acceptance decision.

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

Defines the ontology of STATE: state, transition, authority, candidate, evidence, acceptance, role, actor, capability, boundary, invariant, provenance and related concepts.

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

## 6. Actor independence

STATE roles are defined independently of the nature of the actor performing them.

A role may be realized by:

- an individual human;
- a local human team;
- a distributed or externally sourced team;
- a specialist supplier;
- an automated system;
- an AI model;
- an autonomous agent;
- a multi-agent system;
- a hybrid human–synthetic arrangement.

Actor substitution does not silently alter the authority or control model.

## 7. Role, actor, capability and authority

STATE separates four concepts:

**Role** — the function that must be performed.

**Actor** — the human or synthetic entity performing the role.

**Capability** — what the actor is technically able to do.

**Authority** — what the actor is permitted to decide, approve or change.

Capability does not create authority.

## 8. Controlled transition

A STATE transition begins from an identifiable authoritative state.

It then establishes:

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

## 9. Candidate before authority

A newly produced state is a candidate.

Successful generation, compilation, execution or local plausibility does not by itself establish authority.

The candidate becomes authoritative only through an authorized acceptance process supported by relevant evidence.

## 10. Traceability by construction

The relevant relationship between the following elements shall be reconstructable:

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

## 11. Evidence-based acceptance

Acceptance is an engineering claim about a system state.

The evidence required to support that claim shall be relevant to the claim itself.

A successful build is evidence of successful build behavior. It is not automatically evidence that all intended product behavior, security properties, invariants or release-integrity claims are satisfied.

## 12. Secure engineering by construction

Secure engineering is intrinsic to STATE.

Generally applicable and domain-neutral secure software and systems engineering principles shall be incorporated through specification, architecture, transition design, implementation, modification, verification, evidence and acceptance.

Security is therefore not treated as a separate lifecycle appended to the method.

Domain-specific legal, regulatory, jurisdictional, mission or sector obligations are not part of the universal STATE core. Such requirements may be introduced through tailoring when applicable.

## 13. Failure

FAIL and INCONCLUSIVE are valid engineering outcomes.

A failed or inconclusive candidate does not become an authoritative baseline merely because engineering work has already been performed.

Acceptance criteria, scope or claims shall not be silently weakened to convert failure into success.

## 14. Secure modification

Modification of an accepted system shall preserve the degree of rigor necessary for the properties and assurances intended to survive that modification.

A change that affects a relevant security property, authority boundary, trust relationship, dependency, exposed interface, execution environment or provenance chain requires verification appropriate to that effect.

## 15. Canonical acceptance rule

> **No generated or implemented change becomes authoritative merely because it was produced successfully. A candidate state becomes authoritative only when its relevant origin, scope, effects and required properties have been sufficiently verified against an identified baseline and accepted through an authorized decision process.**

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.1  
Initial publication: 2026-08-11  
Last modified: 2026-08-13