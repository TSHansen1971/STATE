# Transition Contract

> **Document:** `03-how-logical/04-transition-contract.md`  
> **Title:** Transition Contract  
> **Version:** 0.6  
> **Status:** Normative Specification
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


The Transition Contract is the logical control object that makes a specific STATE Transition executable without losing the relationships among intent, authority, scope, actors, evidence and Acceptance.

It is a **contract of control**, not necessarily a legal contract and not necessarily a standalone document.

## 1. Definition

> **A Transition Contract is the authoritative logical composition of the information required to govern one STATE Transition from identified Baseline through Candidate production, verification, Acceptance and baseline establishment.**

The Transition Contract may physically exist as:

- one structured record;
- several linked Work Products;
- a repository-native issue and manifests;
- a database object;
- an automated workflow state;
- another representation established through Tailoring.

Physical form is secondary to logical completeness and traceability.

## 2. Relationship to Work Products

The Transition Contract does not add a twelfth Work Product class.

Instead, it composes or references the Work Products already defined by STATE.

At minimum, the Contract draws from:

- WP-01 Transition Intent and Specification;
- WP-02 Authority Grant;
- WP-03 Actor Assignment;
- WP-04 Baseline Record;
- WP-05 Transition Record.

As the Transition proceeds, it links to:

- WP-06 Verification Record;
- WP-07 Evidence Set;
- WP-08 Acceptance Record;
- WP-09 Baseline Establishment Record;
- conditional WP-10 Release Record;
- conditional WP-11 Deviation and Escalation Record.

## 3. Canonical Contract fields

A Transition Contract shall be capable of representing the following elements to the degree relevant to the Transition.

### TC-01 — Transition Identity

A stable identity that distinguishes the Transition from other engineering work.

Identity may be human-readable, machine-generated or both.

### TC-02 — Governing Intent

The approved outcome or change need from which the Transition derives.

### TC-03 — Baseline Identity

Reference to the Authoritative State selected as Transition input.

### TC-04 — Specification

The operational statement of intended change, constraints, non-goals, relevant invariants and Acceptance basis.

### TC-05 — Authority Basis

Applicable Authority Grants and authority source.

### TC-06 — Transition Boundary

What may change, what shall not change, and what requires escalation or amended authority.

### TC-07 — Actor and Role Assignment

Which Actors perform which logical Roles and under which applicable authority.

### TC-08 — Dependencies and Preconditions

State, system, environment, external or Work Package dependencies that must be true for execution to remain valid.

### TC-09 — Verification Basis

The claims that must be evaluated and the required or permitted verification approaches to the degree known before execution.

### TC-10 — Evidence Obligations

The Evidence Classes, identity requirements or specific Evidence Items required for the requested claims.

### TC-11 — Assurance Conditions

Required independence, review, gate evaluation or other Assurance conditions.

### TC-12 — Failure and Escalation Conditions

Conditions requiring stop, repair, return to an earlier phase, escalation or establishment of a new Transition.

### TC-13 — Work Package Structure

The bounded execution units, dependencies and integration relationships used to realize the Transition.

A Transition with no decomposition may contain one implicit or explicit Work Package.

### TC-14 — Acceptance Basis

The decision basis and Acceptance Authority required at P8.

### TC-15 — Completion Condition

The conditions under which the Transition is complete.

For a successful Transition, completion requires explicit baseline establishment at P9.

### TC-16 — Amendment History

The material authorized changes made to the Transition Contract during execution.

## 4. Contract establishment across P0–P3

The Transition Contract is not necessarily written in full before P0.

It becomes progressively established:

```text
P0
Authority + Baseline
   │
P1
Intent + Specification
   │
P2
Boundary + Authority refinement
   │
P3
Dependencies + implementation context
   │
   ▼
Executable Transition Contract
```

G3 should not pass if the Contract remains materially insufficient to control Candidate production.

## 5. Contract stability

The Transition Contract is controlled but not immutable.

Engineering discovery may reveal that a contract element must change.

The governing rule is:

> **Contract amendment is allowed; silent contract drift is not.**

A material amendment shall be:

- explicit;
- authorized at the appropriate authority level;
- traceable;
- propagated to dependent Work Packages and verification obligations;
- evaluated for whether earlier gate conditions remain valid.

## 6. Contract amendment classes

STATE distinguishes four useful amendment classes.

### CA-01 — Clarification

Improves precision without materially changing intended outcome, authority, boundary or Acceptance claim.

A clarification may not require return to an earlier phase if all prior gate conditions remain valid.

### CA-02 — Execution Amendment

Changes implementation decomposition, sequencing, Actor Assignment or Work Package organization without changing the governing intent or authorization boundary.

Requires re-evaluation of affected dependencies, Assurance and evidence obligations.

### CA-03 — Control Amendment

Changes Transition Boundary, Authority Grant, architecture permission, invariant or Acceptance basis.

Requires return to the earliest affected phase.

### CA-04 — Intent Amendment

Changes the intended outcome or governing purpose.

Requires return to P1 and may require a new Transition where continuity of the original Transition would become misleading.

## 7. No specification laundering

A failed or inconvenient Candidate does not authorize retrospective rewriting of the Contract merely to make the existing Candidate appear compliant.

An Acceptance basis may be changed only when:

- the change is legitimate on its own engineering merits;
- the applicable authority approves it;
- the change is explicit and traceable;
- prior Verification Records are not falsely represented as having tested the new claim.

> **Changing the claim is a new control event, not a way of changing the meaning of old evidence.**

## 8. Transition Boundary inheritance

Every Work Package inherits the Transition Boundary.

A Work Package may narrow its local Mutation Envelope.

It may not broaden the Transition Boundary.

If a Work Package requires broader mutation:

1. stop the out-of-bound action;
2. raise a boundary condition;
3. amend the Transition Contract through appropriate authority or establish a separate Transition;
4. re-establish affected gates.

## 9. Verification planning

The Transition Contract should identify verification intent early enough that implementation is not accepted against criteria invented after Candidate production.

This does not require every test case to be known at P1.

It requires enough verification basis to preserve the relationship between intended claims and later evidence.

## 10. Evidence planning

Evidence obligations should be proportionate.

A low-risk Transition may require only:

- Baseline identity;
- transformation evidence;
- one or more relevant verification results;
- Acceptance decision;
- resulting state identity.

A higher-assurance Transition may require:

- stronger environment identity;
- independent verification;
- security and boundary evidence;
- artifact provenance;
- reproducibility;
- retained negative evidence;
- independent Acceptance.

## 11. Contract and interruption

After interruption, a Transition Contract provides the principal logical basis for reconstructing a safe Resume Point.

Resumption should verify that:

- Contract version remains current;
- Authority Grants remain valid;
- Baseline and Candidate identities remain valid;
- Work Package state remains reconstructable;
- dependencies have not materially changed.

## 12. Contract and parallel execution

Parallel Work Packages share one governing Transition Contract unless they are explicitly separate Transitions.

Concurrency shall not create contradictory local interpretations of:

- Baseline;
- intent;
- architecture constraints;
- authority;
- Acceptance basis.

Where different Work Packages require different local conditions, those differences are represented as bounded local execution constraints under the common Contract.

## 13. Contract closure

A successful Transition Contract closes only after:

- G8 produces ACCEPT;
- G9 establishes the accepted state as the new Authoritative State;
- required Work Products and evidence are linked sufficiently for later reconstruction.

REJECT, REPAIR REQUIRED, INCONCLUSIVE, cancellation or supersession may also close or suspend a Contract, but shall not create a new Authoritative State.

## 14. Canonical Transition Contract rules

> **Every controlled Transition shall have one reconstructable governing Transition Contract.**

> **The Transition Contract composes existing STATE Work Products; it does not require a new file or a new Work Product class.**

> **Contract amendment is allowed; silent contract drift is not.**

> **Changing the claim is a new control event, not a way of changing the meaning of old evidence.**

> **A subordinate Work Package may narrow authority and scope but shall not silently broaden them.**

> **A successful Transition Contract closes only after explicit baseline establishment.**

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-SA 4.0  
Version: 0.6  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
