# STATE Engineering

> **Document:** `README.md`  
> **Title:** STATE Engineering  
> **Version:** 0.6  
> **Status:** Working Draft  
> **Created:** 2026-08-11  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


STATE Engineering is a specification-driven, actor-independent, traceable and evidence-based engineering method for controlling transitions between authoritative system states.

This repository is the canonical public documentation source for the STATE Engineering method.

## Method architecture

STATE is documented through four abstraction levels:

| Level | Abstraction | Governing question |
|---|---|---|
| **WHY** | Contextual | Why does STATE Engineering exist, and what control problem makes it necessary? |
| **WHAT** | Conceptual | What concepts, properties, roles, authority structures, Work Products and evidence relationships define STATE? |
| **HOW** | Logical | How is a controlled Transition contracted, decomposed, executed, verified, evidenced, accepted and established? |
| **WITH WHAT** | Physical | With what human, synthetic, hybrid, hardware and software capabilities is the logical method realized? |

The method is governed across implementation by Tailoring, Assurance and Reference.

## Canonical STATE Cycle

STATE uses the ten-phase P0–P9 cycle:

```text
P0 Authority & Baseline
P1 Specification
P2 Transition Boundary
P3 Bounded Inspection & Context
P4 Candidate Production
P5 Execution & Observation
P6 Verification
P7 Evidence Assembly
P8 Acceptance
P9 Baseline Establishment
```

## Transition Contract

A concrete STATE Transition is governed through a **Transition Contract**.

The Transition Contract is a logical control object that binds together the information needed to answer:

- what authoritative state is being changed;
- why and toward what intended outcome;
- under whose authority;
- within what boundary;
- by which assigned roles and actors;
- subject to which invariants and dependencies;
- using which verification and evidence obligations;
- under which Acceptance basis;
- with which failure, escalation and completion rules.

The Transition Contract is not a new mandatory file type. It may be represented through one or more existing Work Products, provided the required control information remains explicit and traceable.

## Work Packages

A Transition may be executed as one Work Package or decomposed into multiple Work Packages.

A **Work Package** is a bounded execution unit inside an authorized Transition.

A Work Package may narrow inherited scope. It may not silently broaden:

- Transition intent;
- Authority Grant;
- Transition Boundary;
- architectural permission;
- Acceptance basis.

Work Packages are not Work Products.

A Work Product is an information object. A Work Package is an execution/control unit.

## Concurrency and integration

Work Packages may execute sequentially or concurrently when dependencies, mutation boundaries, integration rules and evidence obligations are explicit.

Parallel execution does not create parallel authority universes.

Integration of Work Package results is itself part of Candidate production and can create new behavior requiring integrated verification.

## Repository map

- [`00-foundation/`](00-foundation/) — canonical method specification and architecture.
- [`01-why-contextual/`](01-why-contextual/) — contextual problem and rationale.
- [`02-what-conceptual/`](02-what-conceptual/) — conceptual models.
- [`03-how-logical/`](03-how-logical/) — cycle, gates, failure handling, Transition Contract and Work Package model.
- [`04-with-what-physical/`](04-with-what-physical/) — physical realization.
- [`05-tailoring/`](05-tailoring/) — contextual adaptation.
- [`06-assurance/`](06-assurance/) — assurance and evidence sufficiency.
- [`07-reference/`](07-reference/) — glossary, catalogues and compact reference.

See [`CHANGELOG.md`](CHANGELOG.md) for publication history.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.6  
Initial publication: 2026-08-11  
Last modified: 2026-08-13
