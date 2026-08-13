# Transition Contract and Work Package Reference

> **Document:** `07-reference/TRANSITION-CONTRACT-REFERENCE.md`  
> **Title:** Transition Contract and Work Package Reference  
> **Version:** 0.6  
> **Status:** Reference  
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


This page is the compact operational reference for establishing and controlling a STATE Transition Contract and its Work Packages.

## Transition Contract fields

| ID | Field | Core question |
|---|---|---|
| TC-01 | Transition Identity | Which Transition is this? |
| TC-02 | Governing Intent | Why does the Transition exist? |
| TC-03 | Baseline Identity | Which Authoritative State is being changed? |
| TC-04 | Specification | What is intended to change and what must remain true? |
| TC-05 | Authority Basis | Under whose authority is the Transition performed? |
| TC-06 | Transition Boundary | What may and may not change? |
| TC-07 | Actor and Role Assignment | Who or what performs each logical Role? |
| TC-08 | Dependencies and Preconditions | What must be true for execution to remain valid? |
| TC-09 | Verification Basis | Which claims must be evaluated? |
| TC-10 | Evidence Obligations | What evidence is required? |
| TC-11 | Assurance Conditions | What independence or assurance controls apply? |
| TC-12 | Failure and Escalation Conditions | When must execution stop or escalate? |
| TC-13 | Work Package Structure | How is execution decomposed? |
| TC-14 | Acceptance Basis | On what basis will P8 decide? |
| TC-15 | Completion Condition | When is the Transition complete? |
| TC-16 | Amendment History | Which material Contract changes occurred? |

## Contract build-up through the cycle

```text
P0 → baseline + authority
P1 → intent + specification
P2 → boundary + control refinement
P3 → dependencies + implementation context
      │
      ▼
Executable Transition Contract
```

## Work Package fields

| ID | Field |
|---|---|
| WPK-01 | Package Identity |
| WPK-02 | Governing Transition |
| WPK-03 | Objective |
| WPK-04 | Mutation Envelope |
| WPK-05 | Actor Assignments |
| WPK-06 | Preconditions |
| WPK-07 | Dependencies |
| WPK-08 | Expected Outputs |
| WPK-09 | Evidence Obligations |
| WPK-10 | Local Verification |
| WPK-11 | Completion Condition |
| WPK-12 | Escalation Condition |

## Work Package state model

```text
PLANNED
   │
   ▼
 READY
   │
   ▼
 ACTIVE
  / | \
 /  |  \
▼   ▼   ▼
COMPLETED  BLOCKED  FAILED
              │
              └── may resume when control condition is restored

At any appropriate authority point:
CANCELLED or SUPERSEDED
```

## Scope invariant

```text
MutationEnvelope(WPK) ⊆ TransitionBoundary(T)
```

## Integration rule

```text
WPK-A PASS + WPK-B PASS
          ≠
Integrated Candidate PASS
```

unless the relevant integrated claims have actually been verified.

## Contract amendment rule

```text
Clarification
Execution Amendment
Control Amendment
Intent Amendment
```

The deeper the amendment affects intent, authority, boundary or Acceptance basis, the earlier the cycle phase that must be re-established.

## Core distinction

```text
Work Product = information object
Work Package = execution/control unit
```

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-SA 4.0  
Version: 0.6  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
