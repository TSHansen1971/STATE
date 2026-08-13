# STATE Engineering

> **Document:** `README.md`  
> **Title:** STATE Engineering  
> **Version:** 0.9  
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

The method is governed across implementation by Tailoring, Assurance and Reference.

## Physical realization

The Physical layer binds logical STATE structures to concrete execution capacity.

The binding is:

```text
Logical Role
    │
    ▼
Actor Assignment
    │
    ├── Actor capability
    ├── Authority Grant
    ├── Execution Environment
    ├── Tool capability
    ├── Access / credentials
    ├── Evidence mechanisms
    └── Assurance controls
```

No physical actor class, hardware platform, operating system, programming language, development environment, repository product, cloud service, local execution model or AI system is constitutive of STATE Engineering.

## Actor realization

A STATE Role may be realized by, among other patterns:

- an individual human;
- a co-located human team;
- a distributed, inshore, nearshore or offshore team;
- a specialist supplier;
- deterministic automation;
- an AI model used as a bounded execution actor;
- an autonomous agent or agentic system;
- a multi-agent system;
- a hybrid human–synthetic arrangement.

These are physical realization patterns, not different STATE methods.

## Capability and authority

Physical reach is not authority.

STATE distinguishes the actor's **Effective Capability Envelope** from the **Authorized Execution Envelope**.

```text
Effective Capability Envelope
= what the assigned actor + tools + environment + access can actually do

Authorized Execution Envelope
= the subset the actor is permitted to exercise for the Transition
```

Therefore:

```text
AuthorizedExecutionEnvelope
    ⊆ EffectiveCapabilityEnvelope
    ∩ TransitionBoundary
```

Technical ability to mutate more of the system does not widen the Transition Boundary.

## Execution Environment

The Execution Environment includes the relevant hardware, operating system or runtime, toolchain, dependencies, workspace, configuration, credentials, network dependencies, external services and evidence-capture mechanisms under which a STATE activity occurs.

Environment identity is claim-relative. STATE does not require exhaustive capture of irrelevant machine details.

It requires enough identity to support the claims being made.

## Synthetic actors

AI and agentic systems are treated as physical Actor realizations.

Where their characteristics matter, the Actor Assignment may identify:

- model or system identity;
- provider or local runtime;
- instruction / context basis;
- tool permissions;
- external-service dependencies;
- persistent or session state;
- stochastic or configuration settings;
- evidence-capture mechanisms.

These properties do not create a separate AI variant of STATE.

## Repository map

- [`00-foundation/`](00-foundation/) — canonical specification.
- [`01-why-contextual/`](01-why-contextual/) — contextual problem.
- [`02-what-conceptual/`](02-what-conceptual/) — conceptual models.
- [`03-how-logical/`](03-how-logical/) — complete logical Transition control.
- [`04-with-what-physical/`](04-with-what-physical/) — physical realization, Actor patterns, environments and toolchains.
- [`05-tailoring/`](05-tailoring/) — contextual adaptation.
- [`06-assurance/`](06-assurance/) — assurance and trust.
- [`07-reference/`](07-reference/) — compact reference.

See [`CHANGELOG.md`](CHANGELOG.md) for publication history.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.9  
Initial publication: 2026-08-11  
Last modified: 2026-08-13
