# Work Package Model

> **Document:** `03-how-logical/05-work-package-model.md`  
> **Title:** Work Package Model  
> **Version:** 0.6  
> **Status:** Normative Specification
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


A Work Package is a bounded execution unit used to realize part or all of one STATE Transition.

It exists to support decomposition without fragmenting authority, traceability or system-level Acceptance.

## 1. Definition

> **A Work Package is a bounded unit of engineering execution performed under one governing Transition Contract with explicit scope, dependencies, role assignments, evidence obligations and completion conditions.**

A Work Package is not a Work Product.

```text
Work Product
= information object

Work Package
= bounded execution/control unit
```

## 2. One or many

A Transition may be realized through:

```text
Transition
   └── WPK-01
```

or:

```text
Transition
   ├── WPK-01
   ├── WPK-02
   ├── WPK-03
   └── WPK-04
```

Decomposition is based on control needs, not on a required package count.

## 3. Canonical Work Package fields

A Work Package shall be capable of representing the following elements where relevant.

### WPK-01 — Package Identity

Stable identity within the governing Transition.

### WPK-02 — Governing Transition

Reference to the parent Transition Contract.

### WPK-03 — Objective

The bounded result the package is intended to produce.

### WPK-04 — Mutation Envelope

The subset of the Transition Boundary within which the package may mutate state.

### WPK-05 — Actor Assignments

Actors and logical Roles assigned to package execution, verification or stewardship where package-local assignment is needed.

### WPK-06 — Preconditions

Conditions that must be true before execution begins.

### WPK-07 — Dependencies

Other Work Packages, components, state assumptions, external inputs or sequencing relationships.

### WPK-08 — Expected Outputs

Candidate changes, artifacts, records, observations or intermediate results expected from package execution.

### WPK-09 — Evidence Obligations

Evidence the package must produce or preserve for later Transition-level verification and Acceptance.

### WPK-10 — Local Verification

Verification that may be completed at package level.

Local verification does not replace integrated verification of Transition-level claims.

### WPK-11 — Completion Condition

Condition under which package execution is complete.

Completion does not imply Transition Acceptance.

### WPK-12 — Escalation Condition

Conditions requiring pause, return to the parent Transition Contract, amended authority or establishment of a separate Transition.

## 4. Work Package states

STATE defines the following logical package states:

- **PLANNED** — package exists but entry conditions are not yet established;
- **READY** — entry conditions are satisfied;
- **ACTIVE** — authorized execution is in progress;
- **BLOCKED** — progress requires resolution of a dependency, authority or control condition;
- **COMPLETED** — package completion condition has been satisfied;
- **FAILED** — package cannot satisfy its objective under current conditions;
- **CANCELLED** — authorized decision terminates the package without completion;
- **SUPERSEDED** — a replacement package or revised decomposition has made the package non-current.

Package state is not Candidate authority state.

A COMPLETED Work Package does not create an accepted Candidate.

## 5. Entry condition

A package may enter ACTIVE only when:

- parent Transition Contract is current;
- required Authority Grants remain valid;
- Mutation Envelope is explicit enough;
- package dependencies are satisfied to the required degree;
- assigned Actors have required capability and authority;
- required package-local evidence capture is available.

## 6. Scope inheritance

The Work Package Mutation Envelope is derived from the parent Transition Boundary.

Formally:

```text
MutationEnvelope(WPK) ⊆ TransitionBoundary(T)
```

A Work Package may be narrower.

It shall not be broader.

## 7. Authority inheritance

A Work Package may inherit authority from the parent Transition Contract or receive a narrower package-local Authority Grant.

Authority inheritance shall be reconstructable.

A Work Package cannot create additional authority merely because its actor needs additional access to complete the task.

## 8. Dependency model

Dependencies may be:

- **state dependencies** — another change must exist first;
- **information dependencies** — a specification, decision or evidence item is required;
- **execution dependencies** — another package must complete first;
- **integration dependencies** — results must be combined before verification;
- **environment dependencies** — a required runtime, toolchain or external system condition;
- **authority dependencies** — a decision or grant must exist before execution.

Dependencies should be explicit where their failure can invalidate package results.

## 9. Sequential execution

Sequential Work Packages are used when one package depends on another package's result.

```text
WPK-01 → WPK-02 → WPK-03
```

A downstream package shall not silently assume an upstream result that is FAILED, BLOCKED, SUPERSEDED or materially changed.

## 10. Concurrent execution

Concurrent Work Packages are permitted when their control relationships are explicit.

```text
        ┌─ WPK-02 ─┐
WPK-01 ─┤          ├─ Integration
        └─ WPK-03 ─┘
```

Concurrency requires sufficient control of:

- shared Baseline assumptions;
- Mutation Envelopes;
- shared resources;
- dependencies;
- integration order;
- Candidate identity;
- evidence attribution.

## 11. Concurrent mutation

Two Work Packages may mutate different parts of the same system under one Transition.

Where their Mutation Envelopes overlap, the overlap shall be explicit or prevented.

Uncontrolled overlap creates ambiguity about:

- transformation provenance;
- defect origin;
- evidence attribution;
- package completion;
- integration behavior.

## 12. Isolation

Isolation may be logical or physical.

Examples include:

- different branches;
- separate workspaces;
- isolated environments;
- bounded directories;
- component-level ownership;
- serialized mutation;
- controlled merge order.

No particular mechanism is mandatory.

The requirement is that the chosen mechanism provides sufficient control for the claim and Assurance level.

## 13. Integration

Combining Work Package outputs creates an **Integrated Candidate** or contributes to Candidate production.

Integration is not clerical assembly.

Integration can introduce:

- dependency interaction;
- merge behavior;
- configuration effects;
- emergent behavior;
- security-boundary changes;
- previously absent failure modes.

Therefore:

> **Package-level PASS does not imply integrated Candidate PASS.**

Transition-level claims that depend on interaction shall be verified on the integrated Candidate.

## 14. Integration identity

Where multiple package results are combined, the resulting Candidate shall have identity sufficient to distinguish:

- component results;
- integration order where relevant;
- merged source state;
- built artifact;
- verification target.

Evidence generated before integration remains evidence about the pre-integration object unless the claim remains valid for the integrated Candidate.

## 15. Package-local verification

A Work Package may perform local verification to:

- catch defects early;
- establish package completion;
- support integration readiness;
- generate reusable evidence.

Local verification may later contribute to P6.

It does not automatically satisfy Transition-level verification.

## 16. Package completion

A Work Package is COMPLETED when:

- its bounded objective is met;
- required outputs are identifiable;
- required package-local evidence is preserved;
- unresolved deviations are visible;
- dependencies for downstream work are sufficiently represented.

Completion means:

> **the package is ready to contribute to the Transition.**

It does not mean:

> **the Transition is accepted.**

## 17. Failed Work Package

A FAILED Work Package does not automatically fail the entire Transition if:

- an alternate package can legitimately replace it;
- the Transition Contract remains valid;
- Acceptance claims can still be satisfied.

The failure shall remain traceable where it affects decision history, Assurance or provenance.

## 18. Package revision

A Work Package may be revised when decomposition or execution assumptions change.

A material revision shall preserve enough identity to distinguish the old and new package state.

Where revision changes:

- Mutation Envelope;
- authority;
- dependency;
- verification obligation;
- integration behavior;

affected gate and Contract conditions shall be re-evaluated.

## 19. Package supersession

SUPERSEDED is used when a Work Package is replaced without pretending the previous package completed successfully.

This supports explicit evolution of the execution plan.

## 20. Cross-package evidence

Evidence may be:

- package-local;
- shared;
- integration-level;
- Transition-level.

Evidence ownership shall not obscure what state or claim the evidence describes.

## 21. System-level claims

Decomposition shall not fragment a system-level claim into component claims that no longer prove the original assertion.

For example:

```text
WPK-A PASS
WPK-B PASS
```

does not prove:

```text
Integrated system PASS
```

unless the relevant system-level interaction claim is separately verified.

## 22. Actor independence

Work Package structure is actor-independent.

The same logical package may be assigned to:

- one local developer;
- a team;
- an inshore or offshore supplier;
- deterministic automation;
- an AI or autonomous agent;
- a hybrid team.

Actor-specific controls belong to Actor Assignment, Tailoring and Assurance.

## 23. Work Packages and the STATE Cycle

Work Packages primarily realize P3 through P7 activity under one Transition Contract.

They do not each need their own full P0–P9 cycle unless they are established as independent Transitions.

A package may have local readiness, execution, verification and completion controls without becoming a nested full STATE Transition.

## 24. When a Work Package should become a separate Transition

A Work Package should be promoted to a separate Transition when it requires a materially independent:

- governing intent;
- Authority Grant;
- Baseline;
- Transition Boundary;
- Acceptance decision;
- Authoritative State.

This prevents hiding independent governance decisions inside implementation decomposition.

## 25. Canonical Work Package rules

> **A Work Package is an execution unit, not a Work Product.**

> **Every Work Package is subordinate to one governing Transition Contract.**

> **A Work Package may narrow inherited authority and scope but shall not silently broaden them.**

> **Package completion does not imply Candidate Acceptance.**

> **Package-level PASS does not imply integrated Candidate PASS.**

> **Integration is an engineering transformation and shall be verified where integration affects the accepted claim.**

> **Decomposition shall not fragment a system-level claim into weaker component claims and present them as equivalent evidence.**

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-SA 4.0  
Version: 0.6  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
