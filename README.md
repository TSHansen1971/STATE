# STATE Engineering

> **Document:** `README.md`  
> **Title:** STATE Engineering  
> **Version:** 0.4  
> **Status:** Working Draft  
> **Created:** 2026-08-11  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


STATE Engineering is a specification-driven, actor-independent, traceable and evidence-based engineering method for controlling transitions between authoritative system states.

This repository is the canonical public documentation source for the STATE Engineering method. It is intentionally structured as navigable Git documentation rather than as a conventional linear manuscript.

## Method architecture

STATE is documented through four abstraction levels:

| Level | Abstraction | Governing question |
|---|---|---|
| **WHY** | Contextual | Why does STATE Engineering exist, and what problem context makes it necessary? |
| **WHAT** | Conceptual | What is STATE Engineering, and what concepts, properties, roles, authority structures and information objects define it? |
| **HOW** | Logical | How is a controlled STATE transition performed, governed, verified and accepted? |
| **WITH WHAT** | Physical | With what human, synthetic, hybrid, hardware and software capabilities is the logical method realized? |

These four abstraction levels are followed and governed by three method-control domains:

- **Tailoring** — how STATE is adapted to context without losing its defining properties.
- **Assurance** — how claims, transitions, evidence, role separation and conformance are evaluated.
- **Reference** — the normative terminology, work products, evidence classes, templates, catalogues and source rationale used by the method.

## Foundational position

STATE Engineering is actor-independent.

The method defines logical roles, responsibilities, authority, work products, evidence obligations and acceptance logic independently of whether execution capacity is supplied by an individual human, a local team, an inshore or offshore team, a specialist supplier, deterministic automation, an AI system, an autonomous agent, or a hybrid arrangement.

Artificial intelligence is one realization variant within STATE Engineering. It is not a constitutive element of the method.

## Work-product model

STATE now defines a set of **canonical logical work products**. A work product is an information object required to carry, control or evidence a Transition.

Logical work products do **not** imply one physical file per work product.

Through Tailoring, several logical work products may be represented in one physical document, ticket, database record, repository object or automated record, provided their required information and traceability remain distinguishable.

The current catalogue includes:

1. Transition Intent and Specification
2. Authority Grant
3. Actor Assignment
4. Baseline Record
5. Transition Record
6. Verification Record
7. Evidence Set
8. Acceptance Record
9. Baseline Establishment Record
10. Release Record, when release is a distinct act
11. Deviation and Escalation Record, when required

## Evidence model

Evidence is treated as claim-bound engineering information.

STATE distinguishes evidence classes for:

- identity;
- authority;
- transformation;
- construction and build;
- behavior;
- regression and preservation;
- security and boundary properties;
- environment;
- provenance and integrity;
- decision and acceptance.

Evidence is evaluated through properties including relevance, identity, integrity, provenance, sufficiency, reproducibility, independence, timeliness and preservation.

## Secure engineering foundation

Secure engineering remains a cross-cutting property through **Secure Engineering by Construction** and the Universal Engineering Principles.

## Repository map

- [`00-foundation/`](00-foundation/) — method authority, architecture and canonical specification.
- [`01-why-contextual/`](01-why-contextual/) — contextual problem and rationale.
- [`02-what-conceptual/`](02-what-conceptual/) — concepts, state model, authority, roles, work products, evidence, foundational properties and universal engineering principles.
- [`03-how-logical/`](03-how-logical/) — logical process, transition cycle and governance.
- [`04-with-what-physical/`](04-with-what-physical/) — concrete realization through people, teams, machines, hardware and software.
- [`05-tailoring/`](05-tailoring/) — contextual adaptation and conformance boundaries.
- [`06-assurance/`](06-assurance/) — assurance, evidence sufficiency, independence and trust.
- [`07-reference/`](07-reference/) — glossary, work-product catalogue, evidence catalogue, templates and methodological source register.

See [`CHANGELOG.md`](CHANGELOG.md) for publication history.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.4  
Initial publication: 2026-08-11  
Last modified: 2026-08-13
