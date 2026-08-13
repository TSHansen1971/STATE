# Role, Authority and Responsibility Model

> **Document:** `02-what-conceptual/06-role-authority-responsibility-model.md`  
> **Title:** Role, Authority and Responsibility Model  
> **Version:** 0.3  
> **Status:** Foundational Working Specification  
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


The Role, Authority and Responsibility Model defines the logical governance structure through which STATE Engineering assigns engineering functions without making those functions dependent on a particular actor type or organizational topology.

## 1. Model rule

> **STATE assigns functions to roles, responsibilities to those roles, and authority through explicit grants. Actors are assigned to roles only after the logical control structure has been defined.**

This ordering prevents organizational convenience or technical capability from silently becoming the source of engineering authority.

## 2. Authority domains

STATE distinguishes five canonical authority domains.

An authority domain is a category of legitimate decision right. It is not necessarily a job title and does not require a separate person.

### AD-01 — Intent Authority

**Purpose:** govern what the system is intended to achieve and which outcomes are worth pursuing.

Typical authority includes:

- establishing or approving product intent;
- defining desired outcomes;
- setting priorities;
- accepting changes to intended outcome;
- establishing acceptable trade-offs at the intent level.

Intent Authority does not automatically include authority to redesign architecture or accept an implementation.

### AD-02 — Architecture Authority

**Purpose:** govern structural rules, boundaries and architectural invariants.

Typical authority includes:

- establishing architectural constraints;
- approving changes to architectural boundaries;
- approving changes to architectural invariants;
- defining which structural decisions require escalation.

Architecture Authority may be narrow or broad. It shall be bounded explicitly.

### AD-03 — Transition Authority

**Purpose:** authorize a specific controlled change from an identified baseline.

Typical authority includes:

- authorizing transition scope;
- approving the transition boundary;
- authorizing relevant mutation classes;
- defining escalation conditions;
- suspending or revoking the transition authorization.

Transition Authority answers:

> **What is allowed to change in this transition?**

### AD-04 — Acceptance Authority

**Purpose:** decide whether a Candidate State has sufficient basis to become authoritative.

Typical authority includes:

- accepting a candidate;
- rejecting a candidate;
- requiring repair;
- declaring evidence inconclusive;
- requiring additional verification before decision.

Acceptance Authority shall not be inferred from the fact that an actor produced the candidate.

### AD-05 — Release Authority

**Purpose:** authorize distribution, deployment or other release of an accepted state when release is a distinct act.

Release Authority is relevant only when establishing an Authoritative State and releasing that state are separate decisions.

Acceptance does not necessarily imply release.

Release Authority may be combined with Acceptance Authority where Tailoring explicitly permits it.

## 3. Canonical logical roles

STATE defines six canonical logical roles at this stage of the method.

The roles are functions. They do not prescribe organizational positions.

### LR-01 — Specification Role

**Primary responsibility:** transform approved intent and constraints into a sufficiently operational specification for a transition.

Responsibilities include, as applicable:

- expressing intended outcomes;
- identifying relevant constraints;
- identifying known invariants;
- defining an acceptance basis;
- recording unresolved assumptions.

The Specification Role may propose clarification. It does not gain Intent Authority merely by writing the specification.

### LR-02 — Realization Role

**Primary responsibility:** produce the Candidate State within the authorized Transition Boundary.

Responsibilities include:

- acquiring sufficient implementation context;
- performing authorized mutation;
- preserving declared invariants to the extent required by the transition;
- reporting discovered conditions that exceed authority;
- producing implementation-level traceability and evidence required by the transition.

The Realization Role does not automatically receive Transition Authority, Architecture Authority or Acceptance Authority.

### LR-03 — Verification Role

**Primary responsibility:** evaluate claims about the Candidate State using verification methods appropriate to those claims.

Responsibilities include:

- applying the defined verification basis;
- distinguishing observation from conclusion;
- producing PASS, FAIL or INCONCLUSIVE outcomes where applicable;
- identifying limitations in the verification basis;
- preserving verification evidence.

The Verification Role must remain logically separate from the Realization Role even when one actor performs both.

### LR-04 — Evidence Stewardship Role

**Primary responsibility:** preserve the integrity, identity, linkage and availability of evidence required to support transition decisions.

Responsibilities include:

- associating evidence with the correct baseline and candidate;
- preserving relevant evidence identity;
- maintaining evidence provenance;
- preventing evidence from being silently substituted or detached from its claim.

Evidence Stewardship does not determine acceptance merely by holding the evidence.

### LR-05 — Baseline Custodianship Role

**Primary responsibility:** maintain the identity and continuity of Authoritative States and Baselines.

Responsibilities include:

- identifying the current authoritative state;
- preventing an unaccepted candidate from silently replacing it;
- recording the identity of a newly accepted baseline;
- preserving the relationship between successive authoritative states.

Baseline Custodianship does not create Acceptance Authority.

### LR-06 — Assurance Role

**Primary responsibility:** evaluate whether the control process, verification basis, evidence sufficiency and chosen degree of independence are appropriate to the claim and consequence.

Responsibilities include:

- evaluating the adequacy of role separation;
- evaluating evidence sufficiency;
- identifying assurance gaps;
- challenging unsupported claims;
- determining whether additional assurance activity is required under the applicable Tailoring.

The Assurance Role is distinct from Acceptance Authority. Assurance informs acceptance; it does not automatically make the acceptance decision.

## 4. Role–authority relationship

Roles and authority domains are deliberately separate.

A role may carry no decision authority beyond what is necessary to perform its responsibility.

An actor may be assigned multiple roles and one or more authority domains, but each assignment remains explicit.

Examples:

- a Specification Role may also hold Intent Authority in a small project;
- a Realization Role may also hold Architecture Authority for a bounded component;
- a Verification Role may have no mutation authority;
- an Acceptance Authority may be performed by an actor that performed no implementation activity;
- a Baseline Custodian may record an accepted baseline without possessing authority to accept it.

## 5. Authority grants

Authority shall be established through an explicit or explicitly inherited **Authority Grant**.

An Authority Grant should define, to the degree relevant:

1. **Authority source** — where the legitimacy of the grant originates.
2. **Authority domain** — which decision rights are granted.
3. **Actor or role assignment** — who or what may exercise the grant.
4. **Scope** — which system, component, transition or decision is covered.
5. **Permitted actions** — what may be decided, approved or changed.
6. **Constraints** — limits, invariants or conditions that remain binding.
7. **Validity** — duration, transition, version or condition under which the grant applies.
8. **Evidence obligation** — what evidence must accompany exercise of the authority.
9. **Escalation condition** — when the actor must stop and seek additional authority.
10. **Delegation condition** — whether onward delegation is allowed.
11. **Revocation condition** — how the grant can be withdrawn.

Not every low-risk transition requires a bureaucratic form containing eleven fields. The logical properties, however, shall not be ambiguous where they matter to control.

## 6. Authority chain

Delegated authority shall remain traceable to a human-established governance source.

Automation, policy engines and synthetic actors may exercise delegated authority where this has been explicitly established.

They do not become an independent normative source merely because they can make or execute decisions.

> **Machine autonomy may increase without requiring an equivalent transfer of authority.**

## 7. No implicit authority escalation

An actor shall not infer broader authority merely because:

- the authorized implementation exposes a larger problem;
- broader technical access is available;
- a different architectural solution appears preferable;
- an automated tool can perform additional mutation;
- the actor has historically performed similar work;
- verification reveals an adjacent defect.

Such findings may trigger escalation or a new Authority Grant.

They do not silently expand the existing grant.

## 8. Role combination

STATE preserves **logical separation** even when roles are physically combined in one actor.

Role combination is a Tailoring and Assurance decision.

A single developer in a small project may perform Specification, Realization, Verification, Evidence Stewardship and Baseline Custodianship.

A high-assurance environment may require separate actors, separate tools, independent verification or independent acceptance.

The method does not prescribe one universal staffing topology.

## 9. Mandatory logical separations

Regardless of physical actor assignment:

### Production and verification are distinct claims

The fact that an actor produced a candidate is not verification of that candidate.

### Verification and acceptance are distinct decisions

A PASS verification result is evidence for acceptance. It is not automatically an acceptance decision.

### Acceptance and baseline establishment are distinct acts

A candidate becomes a new baseline only after an authorized acceptance decision and explicit baseline establishment.

### Acceptance and release may be distinct

An accepted state may remain unreleased.

## 10. Physical separation and independence

Physical separation becomes necessary when the required Assurance level cannot be achieved through logical separation alone.

Independence may be increased by:

- a different human actor;
- a different team;
- an organizationally independent verifier;
- a different tool;
- an independent analytical method;
- a deterministic verifier;
- a separate model or agent;
- independent reproduction;
- a separate Acceptance Authority.

The degree of independence is determined through Tailoring and Assurance according to consequence, uncertainty and cost of error.

## 11. Separation-of-duties rule

> **No actor shall accumulate authority and execution responsibilities in a way that defeats the assurance required for the transition.**

This is a risk-proportional rule, not a universal requirement for different people in every role.

The method requires that the chosen role combination remain explicit and defensible.

## 12. Actor assignment

An **Actor Assignment** binds an actual actor to one or more logical roles and, where applicable, authority grants.

An Actor Assignment should establish:

- actor identity or actor class;
- assigned role or roles;
- required capability;
- granted authority;
- transition scope;
- evidence obligations;
- applicable separation or independence requirements.

Human sourcing topology does not change the logical role:

```text
Specification Role
        │
        ├── Local employee
        ├── Inshore team
        ├── Nearshore team
        ├── Offshore team
        ├── Specialist supplier
        ├── Synthetic actor
        └── Hybrid actor arrangement
```

The same applies to Realization, Verification and other logical roles.

## 13. Synthetic and automated actors

Synthetic or automated actors are governed by the same role model.

Additional controls may be necessary because actor characteristics differ.

Examples include:

- constrained tool access;
- bounded repository access;
- explicit command authorization;
- independent verification;
- deterministic acceptance gates;
- stronger evidence capture;
- human escalation on boundary conditions.

These controls arise from actor characteristics and assurance needs, not from a separate AI-specific STATE method.

## 14. Human actors and teams

Human actors are also subject to bounded authority.

Seniority, organizational position, expertise, supplier status or historical practice does not remove the need to understand who is authorized to make which engineering decision.

Distributed sourcing changes actor placement.

It does not change the logical definition of STATE roles.

## 15. Authority conflict

Where two valid authority grants conflict, the transition shall not resolve the conflict through implementation.

The conflict must be escalated to the governance source capable of reconciling it.

Implementation is not an authority-resolution mechanism.

## 16. Authority uncertainty

If an actor cannot determine whether an intended action lies within its Authority Grant, the correct STATE outcome is not to guess.

The actor shall:

1. preserve the current authoritative state;
2. report the uncertainty;
3. request clarification or expanded authority;
4. continue only when the authority boundary is sufficiently resolved.

## 17. Relationship to Work Products

This model defines the logical information that later Work Product specifications must be able to represent.

It does **not** yet prescribe the final forms of:

- Authority Grant records;
- Actor Assignment records;
- Transition Records;
- Acceptance Records;
- Evidence Packages;
- Baseline Records.

Those artifacts belong to the subsequent Work Product and Evidence Model.

## 18. Canonical rules

> **Capability does not create authority.**

> **Responsibilities belong to roles before they belong to actors.**

> **Actor substitution shall not silently change the control model.**

> **Delegated authority shall remain traceable to a human-established governance source.**

> **Physical role combination may be tailored; logical role separation shall remain explicit.**

> **No actor shall accumulate authority and execution responsibilities in a way that defeats the assurance required for the transition.**

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.3  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
