# STATE Engineering

> **Document:** `README.md`  
> **Title:** STATE Engineering  
> **Version:** 0.8  
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
| **HOW** | Logical | How is a controlled Transition contracted, executed, verified, accepted, established and, where applicable, released? |
| **WITH WHAT** | Physical | With what human, synthetic, hybrid, hardware and software capabilities is the logical method realized? |

The method is governed across implementation by Tailoring, Assurance and Reference.

## P9 — Baseline establishment

Acceptance at P8 authorizes progression.

It does not itself change which state is authoritative.

P9 completes the authority transition:

```text
Previous Authoritative State
          │
          ▼
      Transition
          │
          ▼
   Candidate State
          │
       G8 ACCEPT
          │
          ▼
  Accepted Candidate
          │
          ▼
   P9 / G9 Baseline
     Establishment
          │
          ▼
 New Authoritative State
```

Baseline establishment preserves an explicit continuity relationship between the prior Authoritative State, the accepted Candidate and the new Authoritative State.

## Authoritative State Chain

STATE treats authoritative history as a chain of controlled state transitions rather than as overwritten history.

A previous baseline may become superseded for the active purpose, but it does not cease to have existed.

A later return to an earlier state is therefore a **new controlled Transition** from the current Authoritative State toward a Candidate equivalent to or derived from the earlier state.

Rollback is not time travel.

## Release

Release remains an optional post-cycle act.

An accepted and established state may be:

- unreleased;
- released once;
- released through several channels or artifact variants;
- superseded before release.

Release Authority is distinct from Acceptance Authority unless explicitly combined.

A released artifact shall be traceable to the accepted and established state to the degree required by the release claim.

## Provenance

STATE provenance connects the relevant authority and transformation chain:

```text
Intent
  ↓
Baseline
  ↓
Transition Contract
  ↓
Work Packages / Transformation
  ↓
Candidate
  ↓
Verification
  ↓
Evidence
  ↓
Acceptance
  ↓
Baseline Establishment
  ↓
Authoritative State
  ↓
Release, when applicable
```

Provenance is claim-relative. The required identity depth depends on what is being asserted.

## Repository map

- [`00-foundation/`](00-foundation/) — canonical method specification and architecture.
- [`01-why-contextual/`](01-why-contextual/) — contextual problem and rationale.
- [`02-what-conceptual/`](02-what-conceptual/) — conceptual models.
- [`03-how-logical/`](03-how-logical/) — complete logical Transition control including P9 and release/provenance.
- [`04-with-what-physical/`](04-with-what-physical/) — physical realization.
- [`05-tailoring/`](05-tailoring/) — contextual adaptation.
- [`06-assurance/`](06-assurance/) — assurance and evidence sufficiency.
- [`07-reference/`](07-reference/) — glossary, catalogues and compact reference.

See [`CHANGELOG.md`](CHANGELOG.md) for publication history.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.8  
Initial publication: 2026-08-11  
Last modified: 2026-08-13
