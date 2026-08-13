# The STATE Model

> **Document:** `02-what-conceptual/01-the-state-model.md`  
> **Title:** The STATE Model  
> **Version:** 0.1  
> **Status:** Current Documentation
> **Created:** 2026-08-11  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None

## Authoritative state

An **Authoritative State** is a system state accepted as valid for a defined purpose and suitable to serve as the basis for further controlled work.

An authoritative state must be sufficiently identifiable for the claims and transitions that depend on it.

## Baseline

A **Baseline** is the specific authoritative state selected as the input state for a defined transition.

A baseline answers:

> **What exact system state are we claiming to change?**

## Candidate state

A **Candidate State** is a produced state that has not yet been accepted as authoritative.

Generation, compilation, execution or apparent correctness does not change its candidate status.

## Accepted state

An **Accepted State** is a candidate state for which an authorized acceptance process has concluded that the required claims are sufficiently supported.

An accepted state may then become the next authoritative baseline.

## Rejected and inconclusive states

A **Rejected State** is a candidate that does not satisfy the required acceptance basis.

An **Inconclusive State** is a candidate for which available evidence is insufficient to justify acceptance or rejection with the required confidence.

Neither becomes authoritative by default.

## Fundamental transition

```text
AUTHORITATIVE STATE S0
        │
        ▼
AUTHORIZED TRANSITION
        │
        ▼
CANDIDATE STATE
        │
        ▼
VERIFICATION + EVIDENCE
        │
        ▼
ACCEPTANCE DECISION
     ┌──┴───┐
   ACCEPT  REJECT / INCONCLUSIVE
     │
     ▼
AUTHORITATIVE STATE S1
```

Production and acceptance are deliberately separate.

This separation allows the realization actor to be replaced without silently redefining the authority model.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.1  
Initial publication: 2026-08-11  
Last modified: 2026-08-13