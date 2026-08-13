# STATE Engineering

> **Document:** `README.md`  
> **Title:** STATE Engineering  
> **Version:** 0.3  
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
| **WHAT** | Conceptual | What is STATE Engineering, and what concepts, properties, roles and authority structures define it? |
| **HOW** | Logical | How is a controlled STATE transition performed, governed, verified and accepted? |
| **WITH WHAT** | Physical | With what human, synthetic, hybrid, hardware and software capabilities is the logical method realized? |

These four abstraction levels are followed and governed by three method-control domains:

- **Tailoring** — how STATE is adapted to context without losing its defining properties.
- **Assurance** — how claims, transitions, evidence, role separation and conformance are evaluated.
- **Reference** — the normative terminology, records, templates, catalogues and source rationale used by the method.

## Foundational position

STATE Engineering is actor-independent.

The method defines logical roles, responsibilities, authority, boundaries, evidence obligations and acceptance logic independently of whether execution capacity is supplied by an individual human, a local team, an inshore or offshore team, a specialist supplier, deterministic automation, an AI system, an autonomous agent, or a hybrid arrangement.

Artificial intelligence is therefore one realization variant within STATE Engineering. It is not a constitutive element of the method.

STATE explicitly separates:

- **Role** — the function that must be performed.
- **Responsibility** — what the role must produce, preserve, evaluate or control.
- **Actor** — who or what performs the role.
- **Capability** — what that actor is technically or operationally able to do.
- **Authority** — what that actor is legitimately permitted to decide, approve or change.

Capability does not create authority.

Actor substitution does not silently change the control model.

## Authority model

The current conceptual foundation distinguishes five authority domains:

1. **Intent Authority**
2. **Architecture Authority**
3. **Transition Authority**
4. **Acceptance Authority**
5. **Release Authority**

It also defines six canonical logical execution and control roles:

1. **Specification Role**
2. **Realization Role**
3. **Verification Role**
4. **Evidence Stewardship Role**
5. **Baseline Custodianship Role**
6. **Assurance Role**

Authority domains and logical roles may be combined in one actor or distributed across several actors according to Tailoring and Assurance, but the logical distinctions remain explicit.

## Secure engineering foundation

Secure engineering is not a separate phase added after implementation. STATE is designed around **Secure Engineering by Construction** and twelve Universal Engineering Principles.

## Repository map

- [`00-foundation/`](00-foundation/) — method authority, architecture and canonical specification.
- [`01-why-contextual/`](01-why-contextual/) — contextual problem and rationale.
- [`02-what-conceptual/`](02-what-conceptual/) — concepts, state model, authority, roles, foundational properties and universal engineering principles.
- [`03-how-logical/`](03-how-logical/) — logical process, transition cycle and governance.
- [`04-with-what-physical/`](04-with-what-physical/) — concrete realization through people, teams, machines, hardware and software.
- [`05-tailoring/`](05-tailoring/) — contextual adaptation and conformance boundaries.
- [`06-assurance/`](06-assurance/) — assurance, evidence sufficiency, independence and trust.
- [`07-reference/`](07-reference/) — glossary, templates, catalogues and methodological source register.

See [`CHANGELOG.md`](CHANGELOG.md) for publication history.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.3  
Initial publication: 2026-08-11  
Last modified: 2026-08-13
