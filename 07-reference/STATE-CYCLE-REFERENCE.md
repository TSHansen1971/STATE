# STATE Cycle Reference

> **Document:** `07-reference/STATE-CYCLE-REFERENCE.md`  
> **Title:** STATE Cycle Reference  
> **Version:** 0.5  
> **Status:** Reference  
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


This page is the compact operational reference for the canonical STATE Cycle.

## Cycle reference

| Phase | Name | Primary output | Gate |
|---|---|---|---|
| P0 | Establish Authority and Baseline | Authorized starting condition | G0 Authority & Baseline Gate |
| P1 | Specify Intent | Operational Transition specification | G1 Specification Gate |
| P2 | Define Transition Boundary | Authorized Transition Boundary | G2 Boundary Gate |
| P3 | Inspect Baseline and Establish Context | Sufficient implementation context | G3 Readiness Gate |
| P4 | Produce Candidate | Identifiable Candidate State | G4 Candidate Identity Gate |
| P5 | Execute and Observe | Execution / observation evidence | G5 Observation Gate |
| P6 | Verify Claims | Claim-bound Verification Results | G6 Verification Gate |
| P7 | Assemble Evidence | Decision-ready Evidence Set | G7 Evidence Gate |
| P8 | Decide Acceptance | Acceptance Record | G8 Acceptance Gate |
| P9 | Establish New Baseline | New Authoritative State | G9 Baseline Establishment Gate |

## Work Product relationship

| Phase | Principal Work Products |
|---|---|
| P0 | WP-02, WP-03, WP-04, WP-05 |
| P1 | WP-01, WP-05 |
| P2 | WP-01, WP-02, WP-05, conditional WP-11 |
| P3 | WP-05, Evidence Items, conditional WP-11 |
| P4 | WP-05, Candidate identity, Transformation Evidence |
| P5 | WP-06 initiated, WP-07 initiated |
| P6 | WP-06, WP-07 |
| P7 | WP-06, WP-07, conditional WP-11 |
| P8 | WP-08, conditional WP-11 |
| P9 | WP-09, completed WP-05 |

WP-10 is used after P9 where Release is a distinct authorized act.

## Gate semantics

- G0 establishes authority and Baseline identity.
- G1 establishes specification sufficiency.
- G2 establishes mutation boundary.
- G3 establishes implementation readiness.
- G4 establishes Candidate identity.
- G5 establishes sufficient observations.
- G6 establishes explicit verification outcomes.
- G7 establishes decision-ready evidence.
- G8 establishes the Acceptance decision.
- G9 establishes authoritative baseline status.

## Acceptance outcomes

```text
G8
├── ACCEPT ───────────────► P9
├── REJECT ───────────────► terminate candidate path
├── REPAIR REQUIRED ──────► repair loop
└── INCONCLUSIVE ─────────► obtain basis / clarify / re-verify
```

## Resumption rule

Resume at the earliest phase whose gate condition must be re-established.

Do not restart earlier than necessary.

Do not resume later than is justified.

## Authority rule

A technical action may be possible and still be unauthorized.

## State rule

Before G9 passes:

```text
previous Authoritative State = authoritative
Candidate State              = non-authoritative
```

After successful G9:

```text
accepted Candidate State = new Authoritative State
```

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.5  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
