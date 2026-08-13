# STATE Engineering

> **Document:** `README.md`  
> **Title:** STATE Engineering  
> **Version:** 0.7  
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
| **HOW** | Logical | How is a controlled Transition contracted, executed, verified, accepted and established? |
| **WITH WHAT** | Physical | With what human, synthetic, hybrid, hardware and software capabilities is the logical method realized? |

The method is governed across implementation by Tailoring, Assurance and Reference.

## Canonical STATE Cycle

```text
P0  Establish Authority and Baseline
P1  Specify Intent
P2  Define Transition Boundary
P3  Inspect Baseline and Establish Context
P4  Produce Candidate
P5  Execute and Observe
P6  Verify Claims
P7  Assemble Evidence
P8  Decide Acceptance
P9  Establish New Baseline
```

## Verification model

STATE treats verification as explicit claim evaluation.

The basic relationship is:

```text
CLAIM
  ↓
TARGET
  ↓
METHOD
  ↓
CONDITIONS
  ↓
OBSERVATION
  ↓
EVIDENCE
  ↓
RESULT
  ↓
LIMITATIONS
```

A PASS applies only to the identified claim, target and conditions.

A PASS is not a general certificate that the Candidate is correct.

FAIL remains FAIL even if Acceptance Authority later authorizes a changed Acceptance basis. Old evidence does not change meaning retroactively.

STATE defines twelve Claim Classes, eleven Verification Method Classes and eleven Verification Adequacy Properties.

## Acceptance model

Acceptance is an authorized decision over an identified Candidate and an explicit Acceptance Claim Set.

The valid G8 outcomes remain:

- **ACCEPT**
- **REJECT**
- **REPAIR REQUIRED**
- **INCONCLUSIVE**

STATE does not define a fifth “conditional acceptance” outcome.

If a condition must be satisfied before the Candidate can legitimately become authoritative, that condition is part of the Acceptance basis and must be resolved before ACCEPT.

Acceptance is bounded:

> **Acceptance establishes only the claims and scope actually covered by the Acceptance basis. It is not a universal assertion about the Candidate.**

P9 remains separate. ACCEPT does not itself create a new Authoritative State.

## Repository map

- [`00-foundation/`](00-foundation/) — canonical method specification and architecture.
- [`01-why-contextual/`](01-why-contextual/) — contextual problem and rationale.
- [`02-what-conceptual/`](02-what-conceptual/) — conceptual models.
- [`03-how-logical/`](03-how-logical/) — cycle, gates, failure handling, Transition Contract, Work Packages, verification and Acceptance.
- [`04-with-what-physical/`](04-with-what-physical/) — physical realization.
- [`05-tailoring/`](05-tailoring/) — contextual adaptation.
- [`06-assurance/`](06-assurance/) — assurance, independence and evidence sufficiency.
- [`07-reference/`](07-reference/) — glossary, catalogues and compact reference.

See [`CHANGELOG.md`](CHANGELOG.md) for publication history.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.7  
Initial publication: 2026-08-11  
Last modified: 2026-08-13
