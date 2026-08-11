# Foundational Properties

> **Document:** `02-what-conceptual/02-foundational-properties.md`  
> **Title:** Foundational Properties  
> **Version:** 0.1  
> **Status:** Working Draft  
> **Created:** 2026-08-11  
> **Last modified:** 2026-08-11  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None

The following properties define the initial foundational character of STATE Engineering.

## FP-01 — Controlled State Transition

Software engineering is governed as controlled transition between sufficiently identified system states.

## FP-02 — Known Authoritative State

Every controlled transition begins from a sufficiently identified authoritative state.

## FP-03 — Specification before Mutation

The intended change, relevant constraints and acceptance basis are established before a resulting mutation is accepted as authoritative.

## FP-04 — Explicit and Bounded Authority

Every transition operates within established authority and boundaries.

## FP-05 — Actor Independence

Roles and responsibilities are defined independently of whether the performing actor is human, synthetic or hybrid.

## FP-06 — Separation of Role, Actor, Capability and Authority

The function to be performed, the entity performing it, what that entity can technically do and what it is authorized to decide are separate concepts.

## FP-07 — Candidate before Authority

A produced state remains a candidate until an authorized acceptance process establishes it as authoritative.

## FP-08 — Traceability by Construction

The relevant chain from intent to resulting state shall be reconstructable.

## FP-09 — Evidence-Based Acceptance

Acceptance shall be supported by evidence appropriate to the claim being accepted.

## FP-10 — Secure Engineering by Construction

Generally applicable secure engineering principles are intrinsic to the method rather than appended as a separate lifecycle.

## FP-11 — Explicit Failure

FAIL and INCONCLUSIVE are valid outcomes and shall not be silently transformed into PASS.

## FP-12 — Secure Modification

Modification shall preserve the degree of rigor required for the properties and assurances intended to survive the change.

These properties are intended to remain stable while the detailed practices used to realize them may be tailored.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.1  
Initial publication: 2026-08-11  
Last modified: 2026-08-11
