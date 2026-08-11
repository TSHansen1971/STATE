# STATE Engineering

> **Document:** `README.md`  
> **Title:** STATE Engineering  
> **Version:** 0.1  
> **Status:** Working Draft  
> **Created:** 2026-08-11  
> **Last modified:** 2026-08-11  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None

STATE Engineering is a specification-driven, actor-independent, traceable and evidence-based engineering method for controlling transitions between authoritative system states.

This repository is the canonical public documentation source for the STATE Engineering method. It is intentionally structured as navigable Git documentation rather than as a conventional linear manuscript.

## Method architecture

STATE is documented through four abstraction levels:

| Level | Abstraction | Governing question |
|---|---|---|
| **WHY** | Contextual | Why does STATE Engineering exist, and what problem context makes it necessary? |
| **WHAT** | Conceptual | What is STATE Engineering, and what concepts, properties and authority structures define it? |
| **HOW** | Logical | How is a controlled STATE transition performed, governed, verified and accepted? |
| **WITH WHAT** | Physical | With what human, synthetic, hybrid, hardware and software capabilities is the logical method realized? |

These four abstraction levels are followed and governed by three method-control domains:

- **Tailoring** — how STATE is adapted to context without losing its defining properties.
- **Assurance** — how claims, transitions, evidence and conformance are evaluated.
- **Reference** — the normative terminology, records, templates, catalogues and source rationale used by the method.

## Foundational position

STATE Engineering is actor-independent. The method defines roles, responsibilities, authority, boundaries, evidence obligations and acceptance logic independently of whether execution capacity is provided by an individual human, a local team, a distributed team, a specialist supplier, an AI system, an autonomous agent, or a hybrid combination.

Artificial intelligence is therefore one realization variant within STATE Engineering. It is not a constitutive element of the method.

Secure engineering is likewise not a separate phase added after implementation. STATE is designed around **secure engineering by construction**: generally applicable, domain-neutral secure software and systems engineering principles are absorbed into the method itself and applied across specification, transition design, realization, verification, evidence and acceptance.

## Repository map

- [`00-foundation/`](00-foundation/) — method authority, architecture and canonical specification.
- [`01-why-contextual/`](01-why-contextual/) — contextual problem and rationale.
- [`02-what-conceptual/`](02-what-conceptual/) — concepts, state model, authority and foundational properties.
- [`03-how-logical/`](03-how-logical/) — logical process, transition cycle and governance.
- [`04-with-what-physical/`](04-with-what-physical/) — concrete realization through people, teams, machines, hardware and software.
- [`05-tailoring/`](05-tailoring/) — contextual adaptation and conformance boundaries.
- [`06-assurance/`](06-assurance/) — assurance, evidence sufficiency, independence and trust.
- [`07-reference/`](07-reference/) — glossary, templates, catalogues and methodological source register.

## Current public contents

The initial public documentation release establishes the method architecture, initial specification, foundational properties, actor-independence model, secure-engineering foundation and first canonical STATE cycle.

See [`CHANGELOG.md`](CHANGELOG.md) for publication history.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.1  
Initial publication: 2026-08-11  
Last modified: 2026-08-11
