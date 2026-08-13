# STATE Engineering

> **Document:** `README.md`  
> **Title:** STATE Engineering  
> **Version:** 0.12  
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
| **WHY** | Contextual | Why does STATE Engineering exist? |
| **WHAT** | Conceptual | What concepts and properties define STATE? |
| **HOW** | Logical | How is a controlled Transition governed? |
| **WITH WHAT** | Physical | With what actors, environments and tools is the method realized? |

These are governed across application by **Tailoring**, **Assurance** and **Reference**.

## STATE Conformance

STATE Conformance answers a narrow question:

> **Does this declared scope preserve the non-tailorable control semantics required by STATE Engineering?**

Conformance does not ask whether the engineering outcome was successful.

A conformant Transition may legitimately end in:

```text
Verification FAIL
Acceptance REJECT
Acceptance REPAIR REQUIRED
Acceptance INCONCLUSIVE
P9 HOLD
P9 FAILED
```

provided those outcomes are handled according to STATE semantics.

Conversely, a technically successful implementation is not STATE-conformant merely because it works.

## Canonical Conformance Status

STATE defines exactly three overall Conformance Status values:

```text
CONFORMANT
NONCONFORMANT
INCONCLUSIVE
```

No partial-conformance status is defined.

A scope is CONFORMANT only when all applicable Conformance Requirements are satisfied.

## Conformance scopes

STATE defines three internal conformance scopes:

- **Transition Conformance** — one actual controlled Transition;
- **Realization Conformance** — one recurring workflow, pipeline or physical realization pattern;
- **Implementation Conformance** — a defined implementation of STATE across a project or engineering system.

A conformant Realization or Implementation demonstrates that the structure can preserve STATE semantics under its declared assumptions.

It does not automatically prove that every individual Transition executed through it was conformant.

## No certification claim

STATE Conformance is an internal method property.

This revision does not establish:

- organizational certification;
- product certification;
- tool certification;
- accredited assessment;
- third-party certification schemes.

## Repository map

- [`00-foundation/`](00-foundation/) — canonical specification.
- [`01-why-contextual/`](01-why-contextual/) — contextual problem.
- [`02-what-conceptual/`](02-what-conceptual/) — conceptual models.
- [`03-how-logical/`](03-how-logical/) — logical method.
- [`04-with-what-physical/`](04-with-what-physical/) — physical realization.
- [`05-tailoring/`](05-tailoring/) — Tailoring.
- [`06-assurance/`](06-assurance/) — Assurance.
- [`07-reference/`](07-reference/) — reference and STATE Conformance material.

See [`CHANGELOG.md`](CHANGELOG.md) for publication history.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.12  
Initial publication: 2026-08-11  
Last modified: 2026-08-13
