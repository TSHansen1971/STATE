# STATE Engineering Method Specification 008A

> **Document:** `00-foundation/STATE-ENGINEERING-METHOD-SPECIFICATION-008A.md`  
> **Title:** STATE Engineering Method Specification 008A  
> **Version:** 0.8  
> **Status:** Historical Superseded Specification
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


## 1. Purpose

STATE Engineering governs controlled transitions between Authoritative States.

This specification supersedes `STATE-ENGINEERING-METHOD-SPECIFICATION-007A.md` as the current foundational specification and establishes the Baseline Establishment, Release and Provenance Model.

## 2. Canonical definition

> **STATE Engineering is a specification-driven, actor-independent, human-governed, traceable and evidence-based engineering method for controlling transitions between authoritative system states.**

## 3. Current normative model

The method currently defines:

- twelve Foundational Properties;
- twelve Universal Engineering Principles;
- five Authority Domains;
- six canonical logical Roles;
- eleven Work Product classes;
- ten Evidence Classes;
- nine Evidence-Quality Properties;
- ten STATE Cycle phases P0–P9;
- ten Transition Gates G0–G9;
- twelve logical failure classes;
- one governing Transition Contract per Transition;
- bounded Work Package decomposition;
- twelve Claim Classes;
- eleven Verification Method Classes;
- eleven Verification Adequacy Properties;
- six Verification Independence Dimensions;
- four canonical G8 Acceptance outcomes;
- ten Acceptance Sufficiency Conditions;
- fourteen Baseline Establishment Record fields;
- three P9 establishment results;
- fourteen Release Record fields;
- three Release results;
- eight Provenance Dimensions.

## 4. Baseline Establishment definition

Baseline Establishment is the explicit authorized P9 act that assigns authoritative status to the exact accepted Candidate for a defined scope and purpose.

Acceptance and Baseline Establishment are distinct.

## 5. Baseline Establishment Record

WP-09 shall be capable of representing:

1. BE-01 Establishment Identity
2. BE-02 Previous Authoritative State
3. BE-03 Accepted Candidate Identity
4. BE-04 Acceptance Record Identity
5. BE-05 Transition Contract Identity
6. BE-06 Authority Scope
7. BE-07 Resulting Authoritative State Identity
8. BE-08 Effective Condition
9. BE-09 Supersession Relationship
10. BE-10 Known Constraints
11. BE-11 Provenance References
12. BE-12 Baseline Custodian
13. BE-13 Establishment Result
14. BE-14 Failure or Hold Rationale

## 6. P9 outcomes

P9 establishment results are:

- ESTABLISHED;
- HOLD;
- FAILED.

Only ESTABLISHED creates the new Authoritative State.

HOLD or FAILED leaves the previous Authoritative State unchanged.

## 7. Exact-candidate rule

Only the exact Candidate covered by the corresponding ACCEPT decision may be established under that decision.

A Candidate identity mismatch is a G9 failure condition.

## 8. Authoritative State scope

An Authoritative State is authoritative for a defined scope and purpose.

State identity depth is proportional to the claims and future control needs.

## 9. Authoritative State Chain

Authoritative history shall be preserved as a traceable chain of controlled transitions.

Supersession does not erase prior historical authority.

## 10. Rollback rule

Discarding a non-authoritative Candidate is not rollback of authoritative state.

Once a state has become authoritative, return to content equivalent to an earlier state is a new controlled Transition.

> **Rollback of an Authoritative State is forward-moving governance toward a new state, not time travel to an old authority moment.**

A later state may be content-equivalent to an earlier state without being the same historical Authoritative State.

## 11. Concurrent Transition rule

A Candidate based on an earlier Baseline shall not be established without accounting for intervening authoritative change where that change affects the accepted scope.

Affected verification and evidence shall be re-established.

## 12. Release definition

Release is an optional post-cycle authorized act that makes an identified representation of an established Authoritative State available to a defined target, channel, environment or audience.

Release is distinct from Acceptance and Baseline Establishment unless authority and scope explicitly combine them.

## 13. Release Record

WP-10 shall be capable of representing:

1. RL-01 Release Identity
2. RL-02 Authoritative State Identity
3. RL-03 Release Authority
4. RL-04 Release Target
5. RL-05 Released Object Identity
6. RL-06 Release Transformation
7. RL-07 Transformation Environment
8. RL-08 Verification Basis
9. RL-09 Provenance Evidence
10. RL-10 Integrity Evidence
11. RL-11 Effective Release Condition
12. RL-12 Release Result
13. RL-13 Release Constraints
14. RL-14 Supersession Relationship

## 14. Release outcomes

Release results are:

- RELEASED;
- HOLD;
- FAILED.

Release HOLD or FAILED does not retroactively remove Authoritative State status from the underlying baseline.

## 15. Release transformation

Release packaging, build, signing, configuration or deployment is not assumed to be semantically neutral.

Where the transformation can affect the release claim, it requires relevant verification.

## 16. Multiple Releases

One Authoritative State may have multiple distinct Releases.

Each released representation requires identity and provenance sufficient for its own claims.

## 17. Provenance definition

Provenance is the traceable relationship among origin, authorized transformations, identities, Actors, evidence and decisions explaining how a state or artifact came to exist in its asserted form.

## 18. Provenance Dimensions

STATE defines:

1. PV-01 Source Provenance
2. PV-02 Authority Provenance
3. PV-03 Transformation Provenance
4. PV-04 Actor Provenance
5. PV-05 Environment Provenance
6. PV-06 Evidence Provenance
7. PV-07 Decision Provenance
8. PV-08 Distribution Provenance

Not every claim requires every dimension.

## 19. Digest limitation

A cryptographic digest may provide strong identity and integrity evidence.

It does not by itself establish complete provenance.

## 20. Source-to-artifact provenance

Where STATE claims that a released artifact corresponds to an accepted source state, the evidence shall sufficiently connect:

- accepted Candidate / source identity;
- established Authoritative State;
- Release transformation;
- released artifact identity.

## 21. Deployment distinction

A deployed runtime state and an engineering Authoritative State are not automatically the same scope.

Where deployment state is itself authoritative, the Transition Contract and Baseline identity shall establish that explicitly.

## 22. Existing models preserved

The P0–P9 cycle, Transition Contract, Work Package, Verification, Acceptance and WP-01–WP-11 models remain unchanged in their core semantics.

## 23. Canonical Baseline rules

> **Acceptance authorizes progression; Baseline Establishment assigns authoritative status.**

> **Only the exact accepted Candidate may be established under the corresponding Acceptance decision.**

> **P9 HOLD or FAILED leaves the previous Authoritative State unchanged.**

> **Authoritative history is preserved as a chain of state transitions, not overwritten as if earlier states never existed.**

> **Rollback of an Authoritative State is a new controlled Transition, not time travel.**

## 24. Canonical Release and Provenance rules

> **Release is distinct from Acceptance and Baseline Establishment unless authority and scope explicitly combine them.**

> **Release packaging is not assumed to be semantically neutral merely because the source state was accepted.**

> **A released object shall be traceable to the established Authoritative State to the degree required by the release claim.**

> **A digest supports identity and integrity but does not by itself establish full provenance.**

> **One Authoritative State may have multiple distinct Releases.**

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.8  
Initial publication: 2026-08-13  
Last modified: 2026-08-13