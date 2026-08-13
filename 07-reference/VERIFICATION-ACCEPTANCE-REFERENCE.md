# Verification and Acceptance Reference

> **Document:** `07-reference/VERIFICATION-ACCEPTANCE-REFERENCE.md`  
> **Title:** Verification and Acceptance Reference  
> **Version:** 0.7  
> **Status:** Reference  
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


This page is the compact operational reference for STATE Verification and Acceptance.

## Claim Classes

| ID | Claim Class |
|---|---|
| CC-01 | Identity Claim |
| CC-02 | Transformation Claim |
| CC-03 | Construction Claim |
| CC-04 | Behavioral Claim |
| CC-05 | Preservation and Invariant Claim |
| CC-06 | Integration and Interaction Claim |
| CC-07 | Security and Boundary Claim |
| CC-08 | Environment and Compatibility Claim |
| CC-09 | Performance and Resource Claim |
| CC-10 | Provenance and Integrity Claim |
| CC-11 | Recoverability and Failure-Behavior Claim |
| CC-12 | Intent and Outcome Claim |

## Verification Method Classes

| ID | Method |
|---|---|
| VM-01 | Inspection |
| VM-02 | Static Analysis |
| VM-03 | Construction Verification |
| VM-04 | Test Execution |
| VM-05 | Measurement |
| VM-06 | Runtime Observation |
| VM-07 | Comparison and Differential Analysis |
| VM-08 | Simulation or Emulation |
| VM-09 | Analytical Reasoning or Proof |
| VM-10 | Reproduction or Independent Re-execution |
| VM-11 | Review and Expert Judgment |

## Verification Record fields

| ID | Field |
|---|---|
| VR-01 | Claim Identity |
| VR-02 | Target Identity |
| VR-03 | Method |
| VR-04 | Conditions |
| VR-05 | Observation |
| VR-06 | Evidence References |
| VR-07 | Result |
| VR-08 | Limitations |
| VR-09 | Verifier |
| VR-10 | Time or Sequence Identity |
| VR-11 | Dependency |

## Verification results

```text
PASS
FAIL
INCONCLUSIVE
```

`NOT EXECUTED`, `NOT YET EVALUATED`, `NOT APPLICABLE` and `BLOCKED` are not PASS/FAIL verification results.

## Verification Adequacy Properties

| ID | Property |
|---|---|
| VA-01 | Claim Precision |
| VA-02 | Target Identity |
| VA-03 | Method Fitness |
| VA-04 | Condition Representativeness |
| VA-05 | Coverage |
| VA-06 | Evidence Quality |
| VA-07 | Independence |
| VA-08 | Reproducibility |
| VA-09 | Limitation Visibility |
| VA-10 | Integration Depth |
| VA-11 | Security-Relevant Depth |

## Independence Dimensions

| ID | Dimension |
|---|---|
| VI-01 | Actor Independence |
| VI-02 | Method Independence |
| VI-03 | Tool Independence |
| VI-04 | Environment Independence |
| VI-05 | Organizational Independence |
| VI-06 | Decision Independence |

## Acceptance Claim Set classes

| ID | Class |
|---|---|
| ACS-01 | Required Claim |
| ACS-02 | Supporting Claim |
| ACS-03 | Informational Claim |

## Acceptance Record fields

| ID | Field |
|---|---|
| AR-01 | Candidate Identity |
| AR-02 | Transition Contract Identity |
| AR-03 | Acceptance Scope |
| AR-04 | Acceptance Claim Set |
| AR-05 | Verification Basis |
| AR-06 | Evidence Basis |
| AR-07 | Deviations |
| AR-08 | Residual Uncertainty |
| AR-09 | Assurance Basis |
| AR-10 | Acceptance Authority |
| AR-11 | Decision |
| AR-12 | Decision Rationale |
| AR-13 | Effective Constraints |
| AR-14 | Decision Identity |

## Acceptance Sufficiency Conditions

| ID | Condition |
|---|---|
| AS-01 | Candidate Identity |
| AS-02 | Contract Identity |
| AS-03 | Required Claim Resolution |
| AS-04 | Evidence Sufficiency |
| AS-05 | Deviation Resolution |
| AS-06 | Residual Uncertainty Visibility |
| AS-07 | Authority Validity |
| AS-08 | Assurance Sufficiency |
| AS-09 | State Coherence |
| AS-10 | Baseline Establishment Readiness |

## Sufficiency Governance

Sufficiency uses existing STATE control semantics.

- a threshold belongs to the governing Acceptance basis or gate condition;
- the Authority responsible for that basis or condition owns establishment and authorized change of the threshold;
- the threshold shall be knowable before it is used to justify PASS;
- weakening an established threshold is a controlled change to the governing basis;
- weak or inconvenient evidence does not authorize a Realization Actor to redefine sufficiency;
- absent an evaluable authorized threshold, PASS shall not be manufactured.

No separate Sufficiency Authority, Gate, Role, Work Product or method identifier exists.

## G8 outcomes

```text
ACCEPT
REJECT
REPAIR REQUIRED
INCONCLUSIVE
```

No fifth conditional-acceptance outcome exists.

## Core rules

```text
Build PASS ≠ Behavior PASS
Behavior PASS ≠ Security PASS
Package PASS ≠ Integrated Candidate PASS
Verification PASS ≠ Acceptance
Acceptance ≠ Baseline Establishment
```

A Required Claim that remains FAIL or INCONCLUSIVE prevents ACCEPT under the unchanged Acceptance basis.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.7  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
