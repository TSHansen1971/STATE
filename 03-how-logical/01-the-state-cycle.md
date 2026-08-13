# The STATE Cycle

> **Document:** `03-how-logical/01-the-state-cycle.md`  
> **Title:** The STATE Cycle  
> **Version:** 0.6  
> **Status:** Normative Working Specification  
> **Created:** 2026-08-11  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None

The STATE Cycle is the canonical logical process for moving from one Authoritative State to another.

It contains ten phases, identified P0 through P9.

The cycle is invariant at the logical level. Tailoring may combine physical activities, automate gates, consolidate Work Products or omit non-applicable optional detail, but it shall preserve the required control semantics.

## Canonical cycle

```text
CURRENT AUTHORITATIVE STATE
          │
          ▼
P0  Establish Authority and Baseline
          │  G0 Authority & Baseline Gate
          ▼
P1  Specify Intent
          │  G1 Specification Gate
          ▼
P2  Define Transition Boundary
          │  G2 Boundary Gate
          ▼
P3  Inspect Baseline and Establish Context
          │  G3 Readiness Gate
          ▼
P4  Produce Candidate
          │  G4 Candidate Identity Gate
          ▼
P5  Execute and Observe
          │  G5 Observation Gate
          ▼
P6  Verify Claims
          │  G6 Verification Gate
          ▼
P7  Assemble Evidence
          │  G7 Evidence Gate
          ▼
P8  Decide Acceptance
          │  G8 Acceptance Gate
          ▼
P9  Establish New Baseline
          │  G9 Baseline Establishment Gate
          ▼
NEW AUTHORITATIVE STATE
```

Release may follow P9 as a separate authorized act when deployment or distribution is distinct from baseline establishment.

## P0 — Establish Authority and Baseline

### Purpose

Establish the legitimate starting point and governance basis for the Transition.

### Minimum inputs

- governing intent or change need;
- current authoritative-state information;
- applicable authority source.

### Required activities

- identify the Authoritative State that will serve as Baseline;
- establish or reference applicable Authority Grants;
- establish required Actor Assignments to the degree needed to begin specification;
- identify known architecture or governance constraints.

### Primary Work Products

- WP-02 Authority Grant;
- WP-03 Actor Assignment;
- WP-04 Baseline Record;
- initial WP-05 Transition Record.

### Primary roles / authority

- Baseline Custodianship Role;
- applicable Intent, Architecture or Transition Authority.

### Output

A sufficiently identified and authorized starting condition.

### Gate

**G0 — Authority & Baseline Gate**

Progress requires sufficient identity of the Baseline and sufficient authority to define the intended Transition.

## P1 — Specify Intent

### Purpose

Convert governing intent into an operational statement of the desired Transition.

### Required activities

- define intended outcome;
- define relevant non-goals;
- identify constraints;
- identify known invariants;
- identify acceptance claims or acceptance basis;
- record material assumptions and unresolved questions.

### Primary Work Products

- WP-01 Transition Intent and Specification;
- WP-05 Transition Record.

### Primary role

- Specification Role.

### Output

An operational Transition specification.

### Gate

**G1 — Specification Gate**

Progress requires sufficient clarity to distinguish intended change from unintended change and to define the basis for later verification and acceptance.

## P2 — Define Transition Boundary

### Purpose

Translate the specification into a bounded authorization for mutation.

### Required activities

- identify what may change;
- identify what shall not change;
- identify relevant architecture and security boundaries;
- establish permitted mutation classes;
- establish escalation conditions;
- confirm or amend Transition Authority.

### Primary Work Products

- WP-01 Transition Intent and Specification;
- WP-02 Authority Grant;
- WP-05 Transition Record;
- WP-11 Deviation and Escalation Record if unresolved conditions arise.

### Primary role / authority

- Specification Role;
- Transition Authority;
- Architecture Authority where architectural boundaries are implicated.

### Output

Authorized Transition Boundary.

### Gate

**G2 — Boundary Gate**

Progress requires a boundary sufficiently explicit to determine whether a proposed action is inside, outside or uncertain relative to authority.

## P3 — Inspect Baseline and Establish Context

### Purpose

Acquire enough factual implementation context to act without replacing implementation with indefinite inspection.

### Required activities

- inspect the Baseline within authorized read scope;
- confirm relevant dependency, environment and architecture facts;
- identify implementation surfaces;
- test material assumptions;
- identify conditions that invalidate specification or boundary assumptions.

### Primary Work Products

- WP-05 Transition Record;
- environment and identity Evidence Items;
- WP-11 where a discovered condition requires escalation.

### Primary roles

- Realization Role;
- Specification Role where clarification is needed.

### Output

Sufficient implementation context.

### Governing rule

> **Inspect enough to act; do not inspect instead of acting.**

### Gate

**G3 — Readiness Gate**

Progress requires enough reliable context to produce a Candidate within the existing authority and boundary.

If inspection invalidates authority, scope or specification, return to P0, P1 or P2 as appropriate.

## P4 — Produce Candidate

### Purpose

Perform the authorized mutation and produce an identifiable Candidate State.

### Required activities

- implement within the Transition Boundary;
- preserve required invariants;
- capture transformation identity;
- report out-of-bound conditions rather than silently expanding scope;
- establish Candidate State identity.

### Primary Work Products

- WP-05 Transition Record;
- transformation Evidence Items;
- Candidate State identity;
- WP-11 where deviations occur.

### Primary role

- Realization Role.

### Output

Identifiable Candidate State.

### Gate

**G4 — Candidate Identity Gate**

Progress requires an identifiable candidate whose origin and relevant transformation from Baseline can be reconstructed.

A produced candidate is not authoritative.

## P5 — Execute and Observe

### Purpose

Expose the Candidate State to the relevant execution or analytical conditions and capture observations.

### Required activities

- execute, build, analyze or otherwise exercise the candidate as required by the claims;
- capture relevant conditions;
- preserve observations as Evidence Items;
- distinguish observations from conclusions.

### Primary Work Products

- WP-06 Verification Record, initiated;
- WP-07 Evidence Set, initiated;
- construction, behavioral, environment or security Evidence Items as applicable.

### Primary roles

- Verification Role;
- Realization Role may support execution without owning the verification conclusion.

### Output

Execution and observation evidence.

### Gate

**G5 — Observation Gate**

Progress requires sufficient observable information to evaluate the claims scheduled for verification.

An execution failure may immediately support FAIL for one or more claims.

## P6 — Verify Claims

### Purpose

Evaluate specified claims about the Candidate State.

### Required activities

For each relevant claim, record:

- claim;
- verification method;
- conditions;
- observation;
- Evidence Items;
- conclusion;
- limitations.

### Valid outcomes

- PASS;
- FAIL;
- INCONCLUSIVE;
- another explicitly specified claim outcome where the verification model requires it.

### Primary Work Products

- WP-06 Verification Record;
- WP-07 Evidence Set.

### Primary role

- Verification Role.

### Output

Verification results bound to evidence.

### Gate

**G6 — Verification Gate**

Progress to evidence assembly requires that required claims have explicit outcomes and that unverified claims are visible rather than silently assumed.

FAIL does not become PASS by weakening the claim after execution without authorized specification change.

## P7 — Assemble Evidence

### Purpose

Create a decision-ready evidentiary basis.

### Required activities

- bind Evidence Items to the correct Baseline, Candidate, claims and Verification Records;
- evaluate evidence quality;
- preserve relevant negative evidence;
- identify residual limitations;
- establish Evidence Set identity.

### Primary Work Products

- WP-07 Evidence Set;
- completed WP-06 Verification Records;
- WP-11 where material limitations require escalation.

### Primary roles

- Evidence Stewardship Role;
- Assurance Role where required.

### Output

Decision-ready Evidence Set.

### Gate

**G7 — Evidence Gate**

Progress requires evidence sufficient for the decision being requested.

Evidence volume is not the gate criterion. Claim relevance and sufficiency are.

## P8 — Decide Acceptance

### Purpose

Make the authorized decision about the Candidate State.

### Required decision basis

- Candidate identity;
- acceptance claims;
- Verification Records;
- Evidence Set;
- known deviations and limitations;
- applicable Assurance assessment.

### Valid decisions

- **ACCEPT**
- **REJECT**
- **REPAIR REQUIRED**
- **INCONCLUSIVE**

### Primary Work Products

- WP-08 Acceptance Record;
- WP-11 where decision conditions require escalation or accepted deviation.

### Primary authority

- Acceptance Authority.

### Output

Explicit Acceptance decision.

### Gate

**G8 — Acceptance Gate**

Only ACCEPT permits progression to P9.

REJECT, REPAIR REQUIRED and INCONCLUSIVE leave the previous Authoritative State unchanged.

## P9 — Establish New Baseline

### Purpose

Convert an accepted Candidate State into the next Authoritative State.

### Required activities

- verify the accepted Candidate identity;
- establish resulting authoritative-state identity;
- link previous Baseline, Transition and Acceptance Record;
- record effective baseline status;
- preserve authoritative-state continuity.

### Primary Work Products

- WP-09 Baseline Establishment Record;
- completed WP-05 Transition Record.

### Primary role

- Baseline Custodianship Role.

### Output

New Authoritative State.

### Gate

**G9 — Baseline Establishment Gate**

The Transition completes only when the accepted state has been explicitly established as authoritative.

If baseline establishment fails, the previous Authoritative State remains authoritative even though the Candidate may already have an ACCEPT decision.

## Optional post-cycle release

Release is not part of the invariant P0–P9 cycle.

Where distribution, deployment or publication requires a distinct decision:

- Release Authority acts on the accepted and established state;
- WP-10 Release Record is created;
- released artifact or deployed state is traced back to the accepted state to the degree required by the release claim.

A release failure does not retroactively erase Acceptance or baseline establishment unless the applicable governance model explicitly defines such coupling.

## Phase progression rule

Phases define logical dependencies, not mandatory wall-clock sequencing.

Activities may overlap physically when this does not violate dependency, authority, evidence or assurance constraints.

For example, evidence capture may begin during P3 or P4 even though the decision-ready Evidence Set is assembled at P7.

The invariant is not “one phase at a time.”

The invariant is that no later claim assumes an earlier control condition that has not actually been established.


## Transition Contract relationship

The P0–P3 sequence progressively establishes the governing Transition Contract.

P4–P7 execute and evidence the authorized Contract.

P8 decides whether the Candidate satisfies the Contract's authorized Acceptance basis.

P9 establishes the resulting accepted state as authoritative.

Where execution is decomposed into multiple Work Packages, all packages remain subordinate to the same Transition Contract unless they are explicitly established as separate Transitions.

Package-level completion and verification shall not be substituted for Transition-level Acceptance.

## Canonical cycle rule

> **A Candidate State shall not become authoritative by implementation success, verification success, evidence accumulation or Acceptance alone. The state becomes authoritative only after explicit baseline establishment at P9.**

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.6  
Initial publication: 2026-08-11  
Last modified: 2026-08-13
