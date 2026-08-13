# Baseline, Release and Provenance Reference

> **Document:** `07-reference/BASELINE-RELEASE-PROVENANCE-REFERENCE.md`  
> **Title:** Baseline, Release and Provenance Reference  
> **Version:** 0.8  
> **Status:** Reference  
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


This page is the compact operational reference for P9 Baseline Establishment, Release and Provenance.

## Baseline Establishment Record fields

| ID | Field |
|---|---|
| BE-01 | Establishment Identity |
| BE-02 | Previous Authoritative State |
| BE-03 | Accepted Candidate Identity |
| BE-04 | Acceptance Record Identity |
| BE-05 | Transition Contract Identity |
| BE-06 | Authority Scope |
| BE-07 | Resulting Authoritative State Identity |
| BE-08 | Effective Condition |
| BE-09 | Supersession Relationship |
| BE-10 | Known Constraints |
| BE-11 | Provenance References |
| BE-12 | Baseline Custodian |
| BE-13 | Establishment Result |
| BE-14 | Failure or Hold Rationale |

## P9 results

```text
ESTABLISHED
HOLD
FAILED
```

Only ESTABLISHED creates the new Authoritative State.

## Authoritative State Chain

```text
A(n)
 │
 T(n+1)
 │
 C(n+1)
 │
 ACCEPT
 │
 ESTABLISH
 ▼
A(n+1)
```

## Rollback rule

```text
A5 → A6 authoritative

return to A5-like content:
A6 → new Transition → C7 → verify → accept → establish → A7
```

`A7` may be content-equivalent to `A5`.

It is not the same historical Authoritative State.

## Release Record fields

| ID | Field |
|---|---|
| RL-01 | Release Identity |
| RL-02 | Authoritative State Identity |
| RL-03 | Release Authority |
| RL-04 | Release Target |
| RL-05 | Released Object Identity |
| RL-06 | Release Transformation |
| RL-07 | Transformation Environment |
| RL-08 | Verification Basis |
| RL-09 | Provenance Evidence |
| RL-10 | Integrity Evidence |
| RL-11 | Effective Release Condition |
| RL-12 | Release Result |
| RL-13 | Release Constraints |
| RL-14 | Supersession Relationship |

## Release results

```text
RELEASED
HOLD
FAILED
```

## Provenance dimensions

| ID | Dimension |
|---|---|
| PV-01 | Source Provenance |
| PV-02 | Authority Provenance |
| PV-03 | Transformation Provenance |
| PV-04 | Actor Provenance |
| PV-05 | Environment Provenance |
| PV-06 | Evidence Provenance |
| PV-07 | Decision Provenance |
| PV-08 | Distribution Provenance |

## Source-to-artifact chain

```text
Accepted Candidate
      ↓
Authoritative State
      ↓
Release Transformation
      ↓
Released Object
      ↓
Integrity / Provenance Evidence
      ↓
Release
```

## Core distinctions

```text
ACCEPT ≠ ESTABLISHED
ESTABLISHED ≠ RELEASED
digest ≠ full provenance
old content ≠ old authority moment
```

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-SA 4.0  
Version: 0.8  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
