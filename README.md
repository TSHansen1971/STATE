# STATE Engineering

> **Document:** `README.md`  
> **Title:** STATE Engineering  
> **Version:** 0.5  
> **Status:** Working Draft  
> **Created:** 2026-08-11  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


STATE Engineering is a specification-driven, actor-independent, traceable and evidence-based engineering method for controlling transitions between authoritative system states.

This repository is the canonical public documentation source for the STATE Engineering method. It is structured as navigable Git documentation rather than as a conventional linear manuscript.

## Method architecture

STATE is documented through four abstraction levels:

| Level | Abstraction | Governing question |
|---|---|---|
| **WHY** | Contextual | Why does STATE Engineering exist, and what control problem makes it necessary? |
| **WHAT** | Conceptual | What concepts, properties, roles, authority structures, work products and evidence relationships define STATE? |
| **HOW** | Logical | How is a controlled STATE Transition authorized, bounded, realized, verified, evidenced, accepted and established? |
| **WITH WHAT** | Physical | With what human, synthetic, hybrid, hardware and software capabilities is the logical method realized? |

These four abstraction levels are followed and governed by:

- **Tailoring**
- **Assurance**
- **Reference**

## Canonical STATE Cycle

The logical method is organized as a ten-phase cycle:

```text
P0  Establish Authority and Baseline
 ↓
P1  Specify Intent
 ↓
P2  Define Transition Boundary
 ↓
P3  Inspect Baseline and Establish Context
 ↓
P4  Produce Candidate
 ↓
P5  Execute and Observe
 ↓
P6  Verify Claims
 ↓
P7  Assemble Evidence
 ↓
P8  Decide Acceptance
 ↓
P9  Establish New Baseline
```

Release is a separate optional post-cycle act when deployment or distribution requires its own Release Authority.

Each phase is controlled by a logical Transition Gate. A gate is a decision condition, not a mandatory meeting, committee or document.

Gates may be evaluated by human, automated, synthetic or hybrid means where the required authority and assurance have been established.

## Failure rule

A failed, inconclusive or out-of-bound Transition does not replace the current Authoritative State.

Repair creates a new or revised Candidate State and re-enters the cycle at the earliest phase whose assumptions, authority, specification, boundary or evidence remain invalid.

The previous Authoritative State remains authoritative until P9 completes successfully.

## Repository map

- [`00-foundation/`](00-foundation/) — canonical method specification and architecture.
- [`01-why-contextual/`](01-why-contextual/) — contextual problem and rationale.
- [`02-what-conceptual/`](02-what-conceptual/) — conceptual state, authority, role, work-product and evidence models.
- [`03-how-logical/`](03-how-logical/) — canonical cycle, gates, failure, repair and resumption.
- [`04-with-what-physical/`](04-with-what-physical/) — physical realization.
- [`05-tailoring/`](05-tailoring/) — contextual adaptation.
- [`06-assurance/`](06-assurance/) — assurance and evidence sufficiency.
- [`07-reference/`](07-reference/) — glossary, catalogues and compact normative reference.

See [`CHANGELOG.md`](CHANGELOG.md) for publication history.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.5  
Initial publication: 2026-08-11  
Last modified: 2026-08-13
