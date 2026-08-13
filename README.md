# STATE Engineering

> **Document:** `README.md`  
> **Title:** STATE Engineering  
> **Version:** 0.13  
> **Status:** Current Documentation
> **Created:** 2026-08-11  
> **Last modified:** 2026-08-13
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None

STATE Engineering is a specification-driven, actor-independent, traceable and evidence-based engineering method for controlling transitions between authoritative system states.

This repository is the canonical public documentation source for the STATE Engineering method.

## Current method baseline

The current integrated normative specification is:

[`00-foundation/STATE-ENGINEERING-METHOD-SPECIFICATION-014A.md`](00-foundation/STATE-ENGINEERING-METHOD-SPECIFICATION-014A.md)

Revision 014A is the current integrated Candidate specification for v1.1 development. It consolidates the bounded WP06 Sufficiency Governance change without adding a lifecycle phase, STATE Cycle phase, Transition Gate, Foundational Property, Authority Domain, logical Role, Work Product class or Conformance Requirement.

## Release and corpus identity

The current **accepted public release** is `v1.0.0`.

Its authoritative historical identity mapping is:

`v1.0.0 → corpus 0.13 → STATE-ENGINEERING-METHOD-SPECIFICATION-013A`

The active development target is `v1.1.0`, but it remains Candidate and is **not** the current accepted release.

The current integrated specification in that active Candidate development corpus is `STATE-ENGINEERING-METHOD-SPECIFICATION-014A`.

The historical `0.x` corpus-version sequence is closed. Beginning with an accepted `v1.1.0` release, STATE uses release SemVer as the single public corpus version. Stable document identifiers such as `013A` remain independent of release SemVer.

Per-document `Version` metadata is document-local revision metadata and shall not be used by itself to infer release identity.

See [`07-reference/VERSION-RELEASE-AND-DOCUMENT-IDENTITY.md`](07-reference/VERSION-RELEASE-AND-DOCUMENT-IDENTITY.md) for the identity rules.

## Method architecture

STATE is documented through:

```text
WHY          Contextual
WHAT         Conceptual
HOW          Logical
WITH WHAT    Physical
```

with the cross-cutting domains:

```text
TAILORING
ASSURANCE
REFERENCE
```

## Normative reference

The Reference layer now provides:

- consolidated terminology;
- normative-language rules;
- a registry of identifier namespaces;
- internal method traceability;
- Role / Authority catalogue;
- cycle, Work Product, Evidence, Verification, Acceptance, Physical Realization, Tailoring, Assurance and Conformance references.

## Internal traceability

STATE's own method structure is traceable as:

```text
Foundational Property
        ↓
Normative control model
        ↓
Operational method element
        ↓
Evidence / decision structure
        ↓
Assurance
        ↓
Conformance Requirement
```

This is internal method traceability.

It is not an external compliance mapping.

## Repository map

- [`00-foundation/`](00-foundation/) — current and historical integrated method specifications.
- [`01-why-contextual/`](01-why-contextual/) — contextual problem.
- [`02-what-conceptual/`](02-what-conceptual/) — conceptual models.
- [`03-how-logical/`](03-how-logical/) — logical method.
- [`04-with-what-physical/`](04-with-what-physical/) — physical realization.
- [`05-tailoring/`](05-tailoring/) — Tailoring.
- [`06-assurance/`](06-assurance/) — Assurance.
- [`07-reference/`](07-reference/) — normative reference, consolidated glossary, traceability and Conformance.

See [`CHANGELOG.md`](CHANGELOG.md) for publication history.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.13  
Initial publication: 2026-08-11  
Last modified: 2026-08-13
