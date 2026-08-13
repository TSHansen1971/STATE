# Assurance

> **Document:** `06-assurance/README.md`  
> **Title:** Assurance  
> **Version:** 0.11  
> **Status:** Working Draft  
> **Created:** 2026-08-11  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


Assurance defines how STATE evaluates whether claims, controls, evidence, decisions and resulting state transitions deserve the required degree of trust.

Its governing question is:

> **Is the basis for this claim or decision sufficiently strong for the consequence and uncertainty involved?**

## Contents

1. [`01-assurance-model.md`](01-assurance-model.md) — Assurance Objectives, Assurance Conclusions and the relationship among Verification, Evidence, Acceptance and Assurance.
2. [`02-assurance-case-and-confidence.md`](02-assurance-case-and-confidence.md) — Assurance Case structure, confidence reasoning, weaknesses, challenge and residual uncertainty.
3. [`03-independence-and-assurance-depth.md`](03-independence-and-assurance-depth.md) — independence, common-cause failure, Assurance Depth and proportional strengthening.

## Core distinctions

```text
Verification
= evaluates an explicit engineering claim

Acceptance
= makes an authorized decision about a Candidate

Assurance
= evaluates whether the basis for the claim or decision deserves the required trust
```

Assurance does not grant Authority.

Assurance does not rewrite Verification Results.

Assurance does not convert insufficient evidence into sufficient evidence by declaration.

## Cross-cutting scope

Assurance may evaluate:

- specification;
- Authority;
- Transition Boundary;
- Physical Realization;
- Tailoring;
- Verification;
- Evidence;
- Acceptance;
- Baseline Establishment;
- Release;
- provenance;
- recovery and failure handling.

Assurance is therefore cross-cutting rather than an additional P10 phase.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.11  
Initial publication: 2026-08-11  
Last modified: 2026-08-13
