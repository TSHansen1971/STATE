# STATE Scaling Profiles

> **Document:** `05-tailoring/03-scaling-profiles.md`  
> **Title:** STATE Scaling Profiles  
> **Version:** 0.10  
> **Status:** Reference
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


STATE Tailoring Profiles are non-mandatory reference patterns.

They illustrate how the same logical method can be realized at different scales.

Profiles are not maturity levels.

A Transition does not become “better” merely by selecting a heavier profile.

## 1. Profile rule

> **Use the lightest realization that remains sufficient for the actual claims, consequence, uncertainty and Assurance need.**

## TP-01 — Compact Controlled Transition

### Typical context

- one Actor or very small team;
- narrow change;
- known Baseline;
- low coupling;
- high reversibility;
- limited external exposure;
- straightforward verification.

### Typical physical realization

One compact record may contain most logical Work Products.

One Actor may perform:

- Specification;
- Realization;
- Verification;
- Evidence Stewardship;
- Baseline Custodianship.

Acceptance Authority may also be combined where legitimate.

Gates may be implicit in one controlled script or work session if their conditions are reconstructable.

### Typical evidence

- Baseline identity;
- diff / transformation identity;
- focused verification result;
- concise Evidence Items;
- Acceptance decision;
- resulting baseline identity.

### Invariants retained

All Tailoring Invariants.

Compact does not mean uncontrolled.

## TP-02 — Standard Controlled Transition

### Typical context

- routine team development;
- moderate change breadth;
- several dependencies;
- established build / verification tooling;
- ordinary product or service impact.

### Typical physical realization

- explicit Transition Contract;
- one or several Work Packages;
- separate Realization and review/Verification activity where useful;
- automated build and test evidence;
- explicit Acceptance Record;
- controlled P9 establishment.

### Typical evidence

- Baseline and Candidate identity;
- transformation record;
- construction evidence;
- behavioral / regression evidence;
- environment identity as relevant;
- decision and provenance.

## TP-03 — Coordinated Multi-Package Transition

### Typical context

- multiple Work Packages;
- distributed team or supplier participation;
- concurrency;
- integration dependencies;
- broader architecture impact;
- several environments or release artifacts.

### Typical physical realization

- explicit Work Package boundaries;
- dependency graph;
- package-local evidence;
- integrated Candidate verification;
- explicit handoff and environment identity;
- stronger provenance;
- clearer Actor / Role / Authority mapping.

### Typical Assurance

- independent review of critical claims;
- explicit integration verification;
- material environment-drift controls;
- evidence attribution across Work Packages.

## TP-04 — Assurance-Intensive Transition

### Typical context

One or more of:

- high consequence of error;
- strong security relevance;
- low reversibility;
- broad exposure;
- substantial uncertainty;
- complex system-level interaction;
- strong provenance need.

### Typical physical realization

May include:

- separate Acceptance Authority;
- independent Verification Actor or organization;
- multiple Verification Methods;
- stronger environment isolation;
- controlled build / artifact pipeline;
- stronger source-to-artifact provenance;
- independent reproduction;
- deeper negative-evidence preservation;
- stronger release controls.

### Important limitation

This profile does not prescribe maximum ceremony.

Every added control shall still have a reason tied to a claim, consequence, uncertainty or Assurance need.

## 2. Profiles are composable

A Transition may use:

- TP-02 overall;
- TP-04 controls for one security-critical claim;
- TP-01 representation for a trivial documentation Work Package.

Tailoring can be claim-sensitive and component-sensitive.

## 3. Profiles do not change semantics

Across all profiles:

```text
Baseline
→ Specification
→ Authority / Boundary
→ Candidate
→ Verification
→ Evidence
→ Acceptance
→ Baseline Establishment
```

remains the same logical control chain.

## 4. Scaling examples

### Example A — one-line documentation correction

Possible realization:

- one Actor;
- one compact record;
- repository commit as Candidate identity;
- rendered / inspected output as Verification;
- ACCEPT and P9 recorded by controlled commit / merge policy.

### Example B — library upgrade

Possible realization:

- explicit dependency and compatibility claims;
- regression verification;
- environment identity;
- security relevance assessment;
- stronger evidence if transitive dependencies change.

### Example C — distributed feature delivery

Possible realization:

- common Transition Contract;
- several Work Packages;
- local package Verification;
- integration claim;
- system-level Acceptance;
- explicit provenance across supplier handoff.

### Example D — high-consequence release

Possible realization:

- independent Verification;
- strong artifact identity;
- release transformation verification;
- explicit Acceptance Authority;
- explicit P9;
- independent Release Authority where needed;
- deeper provenance and retention.

## 5. Anti-pattern: profile by project size alone

Large project does not automatically require TP-04 for every Transition.

Small project does not automatically justify TP-01 for every Transition.

The controlling factors are the actual claims and Tailoring Factors.

## 6. Anti-pattern: inherited bureaucracy

A heavier profile shall not be copied forward solely because it was used historically.

Controls should remain justified.

## 7. Anti-pattern: convenience downgrade

A lighter profile shall not be selected merely because:

- schedule is tight;
- evidence is difficult;
- Verification failed;
- an Actor prefers broader authority;
- tool limitations make proper control inconvenient.

## 8. Canonical Profile rules

> **Profiles are reference patterns, not maturity levels.**

> **Use the lightest realization that remains sufficient for the actual claim and Assurance need.**

> **A profile may be strengthened for one claim without making every Transition activity equally heavy.**

> **Project size alone does not determine Tailoring depth.**

> **No profile changes the logical meaning of Authority, Candidate, Verification, Acceptance or Baseline Establishment.**

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-SA 4.0  
Version: 0.10  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
