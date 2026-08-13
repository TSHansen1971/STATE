# HOW — Logical Layer

> **Document:** `03-how-logical/README.md`  
> **Title:** HOW — Logical Layer  
> **Version:** 0.7  
> **Status:** Working Draft  
> **Created:** 2026-08-11  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


The Logical layer defines how STATE Engineering operates independently of physical actors, tools, organizations or implementation technology.

Its governing question is:

> **How is an authorized system change transformed into a bounded, executable, verifiable, acceptable and authoritative Transition?**

## Contents

1. [`01-the-state-cycle.md`](01-the-state-cycle.md) — canonical P0–P9 STATE Cycle.
2. [`02-transition-gates.md`](02-transition-gates.md) — G0–G9 gate conditions.
3. [`03-failure-repair-and-resumption.md`](03-failure-repair-and-resumption.md) — failure semantics, repair loops and safe resumption.
4. [`04-transition-contract.md`](04-transition-contract.md) — the governing logical Transition Contract.
5. [`05-work-package-model.md`](05-work-package-model.md) — bounded execution, dependencies, concurrency and integration.
6. [`06-verification-model.md`](06-verification-model.md) — Claim Classes, Verification Method Classes, adequacy, independence and result semantics.
7. [`07-acceptance-model.md`](07-acceptance-model.md) — Acceptance Claim Set, decision basis, deviation handling and G8 decision semantics.

## Logical independence

The HOW layer does not require:

- a particular project-management methodology;
- a particular ticket system;
- a particular source-control platform;
- command-line execution;
- a particular sourcing topology;
- artificial intelligence;
- one physical document per control object;
- different physical people for every logical role.

## Core control chain

```text
Transition Contract
        │
        ▼
Candidate State
        │
        ▼
Explicit Claims
        │
        ▼
Verification
        │
        ▼
Claim-bound Evidence
        │
        ▼
Acceptance Decision
        │
        ▼
Baseline Establishment
```

Verification and Acceptance are distinct.

Verification evaluates claims.

Acceptance decides whether the identified Candidate, under the authorized Acceptance basis and residual uncertainty, may progress to baseline establishment.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.7  
Initial publication: 2026-08-11  
Last modified: 2026-08-13
