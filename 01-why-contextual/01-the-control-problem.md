# The Control Problem

> **Document:** `01-why-contextual/01-the-control-problem.md`  
> **Title:** The Control Problem  
> **Version:** 0.1  
> **Status:** Working Draft  
> **Created:** 2026-08-11  
> **Last modified:** 2026-08-11  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None

Software engineering has historically devoted substantial attention to the production of program artifacts: source code, configuration, tests, build definitions and release packages.

STATE Engineering begins from a different control question:

> **How can an organization know and govern what a system is allowed to become when realization can be delegated to actors whose implementation capacity may exceed the direct production or inspection capacity of the authority that owns the system?**

This problem is not specific to artificial intelligence.

The realization actor may be an internal team, an externally sourced team, a specialist contractor, an automated transformation system, an AI-enabled engineering system, or a combination of these.

The common structural condition is **delegated realization**.

## Production is not control

An actor may be able to produce a valid-looking change without having authority to define:

- the product intent;
- architectural boundaries;
- acceptable risk;
- required invariants;
- acceptance criteria;
- the authoritative resulting state.

STATE therefore separates realization capability from normative authority.

## The state-transition perspective

The fundamental engineering object is not the code fragment being written.

It is the transition:

```text
Known authoritative state
        ↓
Authorized change
        ↓
Candidate state
        ↓
Verification and evidence
        ↓
Acceptance decision
        ↓
New authoritative state
```

This perspective remains valid regardless of who or what performs the implementation.

## The scaling asymmetry

As realization capacity increases, uncontrolled change can be produced faster than direct manual inspection can scale.

The response cannot simply be to slow all realization to the speed at which one person can read every line.

The engineering control system must instead make authority, scope, identity, verification, evidence and acceptance explicit enough that higher realization capacity can remain governable.

STATE Engineering is intended to provide that control model.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.1  
Initial publication: 2026-08-11  
Last modified: 2026-08-11
