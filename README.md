# STATE Engineering

> **Document:** `README.md`  
> **Title:** STATE Engineering  
> **Version:** 0.11  
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
| **WHAT** | Conceptual | What concepts and properties define STATE? |
| **HOW** | Logical | How is a controlled Transition governed? |
| **WITH WHAT** | Physical | With what actors, environments and tools is the logical method realized? |

These are governed across application by **Tailoring**, **Assurance** and **Reference**.

## Assurance

Assurance asks whether the control basis for a claim, decision or state transition deserves the required degree of trust.

STATE Assurance does not create truth, Authority or correctness.

It evaluates the strength of the basis on which those things are being asserted.

The canonical Assurance relationship is:

```text
ASSURANCE OBJECTIVE
        ↓
CLAIMS / DECISIONS IN SCOPE
        ↓
CONTROL BASIS
        ↓
VERIFICATION + EVIDENCE
        ↓
INDEPENDENT CHALLENGE WHERE REQUIRED
        ↓
WEAKNESSES + RESIDUAL UNCERTAINTY
        ↓
ASSURANCE CONCLUSION
```

## Assurance conclusion

STATE defines three canonical Assurance Conclusions:

```text
SUFFICIENT
INSUFFICIENT
INCONCLUSIVE
```

These are not Verification Results and are not Acceptance decisions.

```text
Verification PASS ≠ Assurance SUFFICIENT
Assurance SUFFICIENT ≠ ACCEPT
ACCEPT ≠ ESTABLISHED
```

## Assurance Case

An **Assurance Case** is the reconstructable structured reasoning that connects an Assurance Objective to the claims, evidence, challenge, weaknesses, uncertainty and conclusion that support it.

An Assurance Case may be one sentence for a compact low-consequence Transition or a substantial structured body of evidence for a high-consequence Transition.

It is a logical composition, not a new mandatory Work Product class.

## Independence

Independence is a means of challenging common-cause error.

More independence is not automatically more Assurance.

Useful independence is independence from the failure source relevant to the claim.

Two reviewers, agents or tools that share the same assumptions, model, oracle, environment or data may provide less independent challenge than their count suggests.

## Assurance depth

Assurance depth is selected through Tailoring.

It increases where consequence, uncertainty, security relevance, irreversibility, distribution, autonomy, provenance need or external dependency require a stronger trust basis.

The goal is not maximal process.

The goal is a sufficient trust basis for the claim and decision.

## Repository map

- [`00-foundation/`](00-foundation/) — canonical specification.
- [`01-why-contextual/`](01-why-contextual/) — contextual problem.
- [`02-what-conceptual/`](02-what-conceptual/) — conceptual models.
- [`03-how-logical/`](03-how-logical/) — logical method.
- [`04-with-what-physical/`](04-with-what-physical/) — physical realization.
- [`05-tailoring/`](05-tailoring/) — Tailoring.
- [`06-assurance/`](06-assurance/) — Assurance Model, Assurance Case, confidence and independence.
- [`07-reference/`](07-reference/) — compact reference.

See [`CHANGELOG.md`](CHANGELOG.md) for publication history.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.11  
Initial publication: 2026-08-11  
Last modified: 2026-08-13
