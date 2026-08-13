# HOW — Logical Layer

> **Document:** `03-how-logical/README.md`  
> **Title:** HOW — Logical Layer  
> **Version:** 0.5  
> **Status:** Working Draft  
> **Created:** 2026-08-11  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


The Logical layer defines how STATE Engineering operates independently of physical actors, tools, organizations or implementation technology.

Its governing question is:

> **How is an authorized system change carried from a known baseline to a justified new authoritative state without allowing production success to substitute for verification, evidence or acceptance?**

## Contents

1. [`01-the-state-cycle.md`](01-the-state-cycle.md) — the canonical ten-phase STATE Cycle with phase inputs, activities, outputs and role relationships.
2. [`02-transition-gates.md`](02-transition-gates.md) — logical gate conditions controlling progression between phases.
3. [`03-failure-repair-and-resumption.md`](03-failure-repair-and-resumption.md) — failure semantics, repair loops, boundary breach, inconclusive outcomes and safe resumption.

## Logical independence

The HOW layer does not require:

- a particular development methodology;
- a particular ticket system;
- a particular source-control platform;
- command-line execution;
- a particular organizational topology;
- artificial intelligence;
- different physical people for every logical role.

It requires that the logical control relationships remain explicit.

## Core rule

> **Production changes state. Verification evaluates claims about state. Evidence supports or challenges those claims. Acceptance authorizes state. Baseline establishment makes accepted state authoritative.**

These are distinct logical acts even when one physical actor or one automated pipeline performs several of them.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.5  
Initial publication: 2026-08-11  
Last modified: 2026-08-13
