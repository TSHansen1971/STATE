# STATE Engineering

> **Document:** `README.md`
> **Title:** STATE Engineering
> **Version:** 0.13
> **Status:** Current Documentation
> **Created:** 2026-08-11
> **Last modified:** 2026-08-13
> **Author:** Tor-Ståle Hansen
> **Co-authors:** None

STATE Engineering is an actor-independent engineering control method for authorized, traceable and Evidence-bound transitions between authoritative system states.

It is built for engineering environments in which realization can be delegated to humans, teams, suppliers, deterministic automation, AI systems, autonomous agents or mixed arrangements without allowing technical Capability to become implicit Authority.

## Start here — twelve questions

### 1. What is STATE Engineering?

STATE controls an engineering Transition from a known Authoritative Baseline through bounded realization, Candidate production, claim-bound Verification, Evidence, authorized Acceptance and explicit Baseline Establishment.

### 2. What problem does it solve?

It addresses the control problem created when implementation Capability can scale or be delegated faster than direct human production and inspection can scale.

The method makes intent, scope, Authority, identity, Verification, Evidence and Acceptance explicit enough for the resulting change to remain governable.

### 3. What is the current release?

The current accepted public release is **`v1.0.0`**.

The active development target is **`v1.1.0`**, but it remains Candidate until explicit owner Acceptance and promotion.

### 4. What specification is current?

Two identities matter:

- accepted release `v1.0.0` is bound to `STATE-ENGINEERING-METHOD-SPECIFICATION-013A`;
- the current integrated **development** specification is [`STATE-ENGINEERING-METHOD-SPECIFICATION-014A`](00-foundation/STATE-ENGINEERING-METHOD-SPECIFICATION-014A.md), which is a Normative Specification in the active v1.1 Candidate corpus.

Development status does not silently change the accepted public release.

### 5. How does v1.0.0 map to corpus 0.13 / 013A?

The authoritative historical mapping is:

```text
v1.0.0
  → corpus 0.13
  → STATE-ENGINEERING-METHOD-SPECIFICATION-013A
```

Release SemVer, corpus identity and stable document identifiers are distinct identities.

See [`VERSION-RELEASE-AND-DOCUMENT-IDENTITY.md`](07-reference/VERSION-RELEASE-AND-DOCUMENT-IDENTITY.md).

### 6. What is normative?

The integrated specification and the current normative control documents it governs define the method.

Start with:

[`00-foundation/STATE-ENGINEERING-METHOD-SPECIFICATION-014A.md`](00-foundation/STATE-ENGINEERING-METHOD-SPECIFICATION-014A.md)

Interpretation and precedence are governed through the Reference layer.

### 7. What is explanatory?

Explanatory documents help a reader understand the normative method without replacing it.

Key explanatory entry points are:

- [`01-why-contextual/02-method-positioning.md`](01-why-contextual/02-method-positioning.md);
- [`STATE-ENGINEERING-WHITEPAPER-001A.md`](STATE-ENGINEERING-WHITEPAPER-001A.md).

Where explanatory text differs from the normative corpus, the normative corpus governs.

### 8. What is an example?

Examples are illustrative and non-normative.

The complete worked P0–P9 Transition is:

[`08-examples/COMPLETE-WORKED-STATE-TRANSITION-001A.md`](08-examples/COMPLETE-WORKED-STATE-TRANSITION-001A.md)

Operational patterns and reusable templates are under [`08-examples/`](08-examples/).

### 9. Where is release Evidence?

Release records and authorized public release Evidence are under:

[`09-releases/`](09-releases/)

The release Evidence material preserves the distinction between original Evidence, published commitment anchors and later explanatory records.

### 10. How is the method licensed?

The current authored documentation remains under **CC BY-NC-ND 4.0**, as stated in each current footer.

A prospective licence transition has been owner-approved for later implementation, but **WP19 has not yet implemented it**. No later licence is represented here as already effective.

### 11. How does a practitioner begin?

For a practical first use:

1. identify the Authoritative Baseline;
2. state the Transition intent and Acceptance basis;
3. establish Authority and Actor Assignment;
4. define the Transition Boundary;
5. produce a Candidate;
6. Verify the actual Required Claims;
7. preserve the relevant Evidence;
8. make the authorized Acceptance decision;
9. establish the new Baseline explicitly.

Reusable starting records are under:

[`08-examples/templates/`](08-examples/templates/)

For empirical evaluation, use [`VALIDATION-PROTOCOL-001A.md`](VALIDATION-PROTOCOL-001A.md) and the [`pilot package`](08-examples/pilot/).

### 12. How are changes to STATE controlled?

STATE itself is developed as a controlled corpus.

Normative changes require explicit owner Authority, bounded work, traceable Evidence and Verification.

Published release tags are immutable.

Candidate material does not become an accepted release merely because it exists on `main`.

## Method architecture

STATE is documented through:

```text
WHY          Contextual
WHAT         Conceptual
HOW          Logical
WITH WHAT    Physical
```

with:

```text
TAILORING
ASSURANCE
REFERENCE
```

as cross-cutting method-control domains.

## Core invariants

- **Capability does not create Authority.**
- Candidate output is not automatically authoritative.
- Discovery does not expand scope.
- Verification outcomes are PASS, FAIL or INCONCLUSIVE.
- Negative Evidence remains visible.
- Repair resumes from the earliest invalidated control condition.
- Actor substitution does not change the logical control semantics.
- Tailoring may compress representation but may not delete required control semantics.

## What STATE is not

STATE is not a project-management method, lifecycle catalogue, software-development methodology, compliance framework, organizational maturity model, AI governance overlay or replacement for domain engineering knowledge.

It is an engineering control method centered on authorized state transition.

## Recommended reading path

A bounded path for a new reader is:

1. [`01-why-contextual/01-the-control-problem.md`](01-why-contextual/01-the-control-problem.md) — why the control problem exists.
2. [`01-why-contextual/02-method-positioning.md`](01-why-contextual/02-method-positioning.md) — what STATE is and is not.
3. [`00-foundation/STATE-ENGINEERING-METHOD-SPECIFICATION-014A.md`](00-foundation/STATE-ENGINEERING-METHOD-SPECIFICATION-014A.md) — current integrated development specification.
4. [`03-how-logical/01-the-state-cycle.md`](03-how-logical/01-the-state-cycle.md) — P0–P9 logical Transition.
5. [`07-reference/ROLE-AUTHORITY-CATALOGUE.md`](07-reference/ROLE-AUTHORITY-CATALOGUE.md) — Role, Actor, Capability and Authority.
6. [`07-reference/WORK-PRODUCT-CATALOGUE.md`](07-reference/WORK-PRODUCT-CATALOGUE.md) — canonical Work Product classes.
7. [`08-examples/COMPLETE-WORKED-STATE-TRANSITION-001A.md`](08-examples/COMPLETE-WORKED-STATE-TRANSITION-001A.md) — complete worked application.
8. [`08-examples/templates/`](08-examples/templates/) — reusable operational starting points.

## Repository map

- [`00-foundation/`](00-foundation/) — integrated specifications and foundation architecture.
- [`01-why-contextual/`](01-why-contextual/) — control problem and method positioning.
- [`02-what-conceptual/`](02-what-conceptual/) — conceptual models and foundational engineering properties.
- [`03-how-logical/`](03-how-logical/) — STATE Cycle, gates, repair, contracts and Acceptance.
- [`04-with-what-physical/`](04-with-what-physical/) — Actor, tool and environment realization.
- [`05-tailoring/`](05-tailoring/) — Tailoring and scaling.
- [`06-assurance/`](06-assurance/) — Evidence, Assurance and independence.
- [`07-reference/`](07-reference/) — normative/reference lookup and methodological provenance.
- [`08-examples/`](08-examples/) — worked examples, patterns, templates and pilot material.
- [`09-releases/`](09-releases/) — release records and authorized public Evidence.
- [`10-development/`](10-development/) — controlled method-development history.

See [`CHANGELOG.md`](CHANGELOG.md) for publication history.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.13  
Initial publication: 2026-08-11  
Last modified: 2026-08-13
