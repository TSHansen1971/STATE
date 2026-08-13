# Assurance

> **Document:** `06-assurance/README.md`  
> **Title:** Assurance  
> **Version:** 0.12  
> **Status:** Current Documentation
> **Created:** 2026-08-11  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


Assurance defines how STATE evaluates whether claims, controls, evidence, decisions and resulting state transitions deserve the required degree of trust.

Its governing question is:

> **Is the basis for this claim or decision sufficiently strong for the consequence and uncertainty involved?**

## Contents

1. [`01-assurance-model.md`](01-assurance-model.md) — Assurance Objectives, Conclusions and sufficiency properties.
2. [`02-assurance-case-and-confidence.md`](02-assurance-case-and-confidence.md) — Assurance Case, confidence, challenge and uncertainty.
3. [`03-independence-and-assurance-depth.md`](03-independence-and-assurance-depth.md) — independence and Assurance Depth.

## Assurance and Conformance

Assurance and Conformance answer different questions.

```text
Conformance:
Did the declared scope preserve required STATE semantics?

Assurance:
Does the basis for the claim or decision deserve the required trust?
```

A Transition may be conformant while correctly concluding that Assurance is INSUFFICIENT or INCONCLUSIVE.

That is not a defect in Conformance.

It may demonstrate that the method correctly prevented unjustified authority progression.

A nonconformant process cannot repair its missing STATE semantics merely by producing a strong technical result.

Assurance does not create Conformance by declaration.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.12  
Initial publication: 2026-08-11  
Last modified: 2026-08-13