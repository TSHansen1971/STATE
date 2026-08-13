# Tailoring

> **Document:** `05-tailoring/README.md`  
> **Title:** Tailoring  
> **Version:** 0.12  
> **Status:** Working Draft  
> **Created:** 2026-08-11  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


Tailoring defines how STATE Engineering adapts to context without losing its defining control semantics.

Its governing question is:

> **Which implementation details may be scaled, combined, automated or simplified while preserving the properties that make the process a controlled STATE Transition?**

## Contents

1. [`01-tailoring-model.md`](01-tailoring-model.md) — Tailoring Envelope, non-tailorable invariants, Semantic Compression and Control Deletion.
2. [`02-tailoring-decision-model.md`](02-tailoring-decision-model.md) — context factors, Tailoring Decision fields and re-tailoring triggers.
3. [`03-scaling-profiles.md`](03-scaling-profiles.md) — non-mandatory reference profiles.

## Tailoring and Conformance

Tailoring is permitted only inside the Tailoring Envelope.

Conformance therefore does not require identical physical implementations.

It requires preservation of non-tailorable semantics.

A compact Transition may be CONFORMANT.

A highly documented Transition may be NONCONFORMANT.

The decisive question is whether the required STATE controls are genuinely present and reconstructable.

> **Semantic Compression preserves Conformance; Control Deletion breaks it.**

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.12  
Initial publication: 2026-08-11  
Last modified: 2026-08-13
