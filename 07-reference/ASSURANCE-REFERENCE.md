# Assurance Reference

> **Document:** `07-reference/ASSURANCE-REFERENCE.md`  
> **Title:** Assurance Reference  
> **Version:** 0.11  
> **Status:** Reference  
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


This page is the compact reference for STATE Assurance.

## Assurance Objectives

| ID | Objective |
|---|---|
| AO-01 | Authority Validity |
| AO-02 | State Identity Integrity |
| AO-03 | Specification Adequacy |
| AO-04 | Boundary Adequacy |
| AO-05 | Physical Realization Fitness |
| AO-06 | Verification Adequacy |
| AO-07 | Evidence Adequacy |
| AO-08 | Independence Adequacy |
| AO-09 | Tailoring Adequacy |
| AO-10 | Failure and Recovery Adequacy |
| AO-11 | Decision Adequacy |
| AO-12 | Provenance Adequacy |

## Assurance Conclusions

```text
SUFFICIENT
INSUFFICIENT
INCONCLUSIVE
```

## Assurance Sufficiency Properties

| ID | Property |
|---|---|
| ASP-01 | Scope Clarity |
| ASP-02 | Identity Coherence |
| ASP-03 | Evidence Relevance |
| ASP-04 | Evidence Integrity and Provenance |
| ASP-05 | Method Adequacy |
| ASP-06 | Independence Adequacy |
| ASP-07 | Limitation Visibility |
| ASP-08 | Residual Uncertainty Visibility |
| ASP-09 | Tailoring Validity |
| ASP-10 | Decision Coherence |

## Assurance Case fields

| ID | Field |
|---|---|
| ACASE-01 | Case Identity |
| ACASE-02 | Assurance Objective |
| ACASE-03 | Scope |
| ACASE-04 | Required Assurance Depth |
| ACASE-05 | Primary Claim or Decision |
| ACASE-06 | Supporting Control Basis |
| ACASE-07 | Verification Basis |
| ACASE-08 | Evidence Basis |
| ACASE-09 | Independence / Challenge |
| ACASE-10 | Known Weaknesses |
| ACASE-11 | Negative Evidence |
| ACASE-12 | Residual Uncertainty |
| ACASE-13 | Assumptions |
| ACASE-14 | Conclusion |
| ACASE-15 | Conclusion Rationale |
| ACASE-16 | Assurer Identity |

## Assurance Independence Patterns

| ID | Pattern |
|---|---|
| AIP-01 | Independent Actor Challenge |
| AIP-02 | Independent Method Challenge |
| AIP-03 | Independent Tool Challenge |
| AIP-04 | Independent Environment Challenge |
| AIP-05 | Independent Data / Oracle Challenge |
| AIP-06 | Organizational Challenge |
| AIP-07 | Decision Separation |
| AIP-08 | Adversarial Challenge |

## Assurance Depth Dimensions

| ID | Dimension |
|---|---|
| ADD-01 | Claim Precision Depth |
| ADD-02 | Verification Depth |
| ADD-03 | Evidence Depth |
| ADD-04 | Independence Depth |
| ADD-05 | Environment Control Depth |
| ADD-06 | Reproducibility Depth |
| ADD-07 | Security Challenge Depth |
| ADD-08 | Provenance Depth |
| ADD-09 | Failure / Recovery Depth |
| ADD-10 | Decision Review Depth |

## Core distinctions

```text
Verification PASS
    ≠
Assurance SUFFICIENT
    ≠
Acceptance ACCEPT
    ≠
Baseline ESTABLISHED
```

## Core rule

```text
Assurance
= justified confidence in the basis

not
= more documents
= more reviewers
= more tests
= more ceremony
```

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-SA 4.0  
Version: 0.11  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
