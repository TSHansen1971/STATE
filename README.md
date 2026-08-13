# STATE Engineering

> **Document:** `README.md`  
> **Title:** STATE Engineering  
> **Version:** 0.10  
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
| **HOW** | Logical | How is a controlled Transition governed from Baseline through Candidate, Verification, Acceptance and Baseline Establishment? |
| **WITH WHAT** | Physical | With what actors, hardware, software, environments, toolchains and execution mechanisms is the logical method realized? |

The four abstraction levels are governed across application by **Tailoring**, **Assurance** and **Reference**.

## Tailoring

Tailoring adapts the physical depth, representation and control intensity of STATE to the actual engineering context.

Tailoring may change:

- Work Product granularity;
- whether several logical records share one physical representation;
- whether gates are manual, automated or hybrid;
- how many physical Actors realize the logical Roles;
- verification depth;
- independence depth;
- environment identity depth;
- evidence volume and preservation depth;
- isolation mechanisms;
- Work Package decomposition;
- release controls.

Tailoring may not remove the semantics that make the method STATE.

## Semantic compression

STATE explicitly permits **Semantic Compression**:

```text
Many logical control objects
        ↓
one compact physical representation
```

provided the logical distinctions remain reconstructable.

For example, one small Transition record may physically contain:

- specification;
- Authority Grant reference;
- Actor Assignment;
- Baseline identity;
- verification result;
- evidence references;
- Acceptance decision;
- Baseline Establishment identity.

This can be fully conformant.

The opposite is **Control Deletion**: removing the underlying control obligation merely because a separate document is inconvenient.

Control Deletion is not Tailoring.

## Tailoring Envelope

The **Tailoring Envelope** is the permitted range of physical and procedural variation within which the Foundational Properties and required control semantics remain intact.

A small one-person change and a distributed high-assurance Transition may therefore look very different physically while implementing the same method.

## Scaling principle

STATE scales by changing **depth and representation**, not by changing the meaning of:

- Authority;
- Candidate;
- Verification;
- Evidence;
- Acceptance;
- Baseline Establishment;
- failure;
- provenance.

## Repository map

- [`00-foundation/`](00-foundation/) — canonical specification.
- [`01-why-contextual/`](01-why-contextual/) — contextual problem.
- [`02-what-conceptual/`](02-what-conceptual/) — conceptual models.
- [`03-how-logical/`](03-how-logical/) — logical method.
- [`04-with-what-physical/`](04-with-what-physical/) — physical realization.
- [`05-tailoring/`](05-tailoring/) — Tailoring model, decisions and scaling profiles.
- [`06-assurance/`](06-assurance/) — assurance and trust.
- [`07-reference/`](07-reference/) — compact reference.

See [`CHANGELOG.md`](CHANGELOG.md) for publication history.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.10  
Initial publication: 2026-08-11  
Last modified: 2026-08-13
