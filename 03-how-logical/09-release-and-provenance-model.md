# Release and Provenance Model

> **Document:** `03-how-logical/09-release-and-provenance-model.md`  
> **Title:** Release and Provenance Model  
> **Version:** 0.8  
> **Status:** Normative Working Specification  
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


The Release and Provenance Model defines how an accepted and established Authoritative State may be distributed, deployed, published or otherwise released while preserving its relationship to the state that was actually accepted.

Release is an optional post-cycle act.

## 1. Release definition

> **Release is an authorized act that makes an identified representation of an established Authoritative State available to a defined target, channel, environment or audience.**

Release may involve:

- packaging;
- signing;
- copying;
- publishing;
- deployment;
- installation;
- distribution;
- activation.

Not all projects use all forms.

## 2. Release is not Acceptance

A Candidate can be accepted and established without being released.

A Release Actor cannot create Acceptance merely by distributing an artifact.

Release Authority and Acceptance Authority are distinct authority domains unless explicitly combined.

## 3. Release transformation

Release may be a pure distribution act or may include transformation.

Examples of transformation include:

- compilation;
- packaging;
- compression;
- signing;
- installer construction;
- containerization;
- environment-specific configuration.

Where a release transformation can affect the released claim, it requires relevant verification and provenance.

> **Release packaging is not assumed to be semantically neutral merely because the source state was accepted.**

## 4. Release Record

WP-10 shall be capable of representing the following fields where Release is distinct.

### RL-01 — Release Identity

Stable identity of the Release act or release instance.

### RL-02 — Authoritative State Identity

Reference to the established state from which Release derives.

### RL-03 — Release Authority

Authority Grant and Actor exercising Release Authority.

### RL-04 — Release Target

Channel, environment, audience, endpoint or distribution target.

### RL-05 — Released Object Identity

Identity of the exact artifact, package, deployment or representation released.

### RL-06 — Release Transformation

Description or identity of packaging, build, signing, configuration or other transformation between Authoritative State and released object.

### RL-07 — Transformation Environment

Relevant environment identity where transformation can affect provenance or reproducibility.

### RL-08 — Verification Basis

Verification relevant to the released representation.

### RL-09 — Provenance Evidence

Evidence linking the released object to the Authoritative State and transformation chain.

### RL-10 — Integrity Evidence

Digest, signature, manifest or other integrity mechanism where required by the release claim.

### RL-11 — Effective Release Condition

Time, sequence, publication event or activation condition.

### RL-12 — Release Result

RELEASED, HOLD or FAILED.

### RL-13 — Release Constraints

Known channel, environment, compatibility or operational constraints.

### RL-14 — Supersession Relationship

Previous Release or released representation superseded by this Release, where applicable.

## 5. Release result semantics

### RELEASED

The identified object has been released under valid Release Authority.

### HOLD

Release is authorized or prepared but an unresolved condition prevents completion.

### FAILED

The release act did not complete as intended.

HOLD and FAILED do not retroactively remove Authoritative State status from the underlying baseline.

## 6. One state, multiple releases

One Authoritative State may legitimately produce multiple Releases.

Examples:

```text
A20
 ├── Release R20-mac
 ├── Release R20-linux
 └── Release R20-offline
```

These Releases may share source authority while differing in:

- packaging;
- platform;
- configuration;
- target;
- artifact identity.

Each released representation requires provenance sufficient for its own claims.

## 7. Multiple states, same version label

Human-readable version labels are not guaranteed unique state identities.

If two different Authoritative States are released under the same marketing or display label, STATE provenance shall still distinguish them.

A display label is not sufficient evidence of state identity unless the governing context explicitly makes it so.

## 8. Release provenance chain

A release claim should be reconstructable through the relevant chain:

```text
Authoritative State
      │
      ▼
Release Transformation
      │
      ▼
Released Object
      │
      ▼
Release Verification
      │
      ▼
Integrity / Provenance Evidence
      │
      ▼
Release Decision
      │
      ▼
Target / Channel
```

Where the Release transformation is deterministic and fully controlled, the chain may be compact.

Where it is complex, stronger evidence may be required.

## 9. Provenance definition

> **Provenance is the traceable relationship among the origin, authorized transformations, identities, evidence and decisions that explain how a state or artifact came to exist in its asserted form.**

Provenance is broader than a hash.

A cryptographic digest can support identity and integrity.

It does not by itself explain:

- who authorized the transformation;
- which source state was used;
- which environment produced the artifact;
- which verification applied;
- which decision released it.

## 10. Provenance dimensions

STATE defines eight useful provenance dimensions.

### PV-01 — Source Provenance

Which source or Baseline state the object derives from.

### PV-02 — Authority Provenance

Which Authority Grants governed the relevant transitions or release.

### PV-03 — Transformation Provenance

Which transformations produced the resulting state or artifact.

### PV-04 — Actor Provenance

Which Actors performed relevant Roles.

### PV-05 — Environment Provenance

Which relevant execution, build or transformation environment applied.

### PV-06 — Evidence Provenance

How decision-relevant Evidence Items were produced and associated.

### PV-07 — Decision Provenance

Which Acceptance, Baseline Establishment and Release decisions applied.

### PV-08 — Distribution Provenance

Where and how the released representation was distributed or activated.

Not every claim requires every dimension.

## 11. Source-to-artifact provenance

Where STATE claims that a released artifact corresponds to an accepted source state, the provenance basis shall be sufficient to link:

```text
accepted source identity
      ↓
established Authoritative State
      ↓
release transformation
      ↓
released artifact identity
```

A successful source build performed earlier does not prove that a later distributed artifact is the same artifact.

## 12. Artifact identity

Artifact identity may use:

- cryptographic digest;
- signed manifest;
- package identity;
- immutable repository identity;
- trusted storage identity;
- another mechanism appropriate to the claim.

No specific mechanism is mandatory.

## 13. Release verification

Release verification may evaluate:

- artifact identity;
- packaging completeness;
- signature or integrity;
- installability;
- deployment behavior;
- target compatibility;
- source-to-artifact relationship;
- release-channel correctness.

Release verification is claim-driven.

## 14. Re-release

Releasing the same Authoritative State again creates a new Release identity where the act, target or artifact identity matters.

A re-release may reuse earlier verification only where:

- released object identity is unchanged or equivalence is justified;
- relevant transformation is unchanged;
- target assumptions remain valid;
- Assurance permits reuse.

## 15. Release correction

A bad or misdirected Release does not justify silently editing the Release Record.

Corrective action may include:

- withdrawal;
- replacement;
- new Release;
- new Transition if the underlying Authoritative State must change.

The original release event remains part of provenance where material.

## 16. Deployment versus authoritative state

A deployed runtime state and an engineering Authoritative State are not automatically identical concepts.

A project may choose to make deployment state part of the authoritative scope.

If so, the Transition Contract and Baseline identity shall say so.

Otherwise, release/deployment is a related post-cycle act whose identity is linked to the engineering baseline.

## 17. Rollback after release

Operational rollback of a released deployment may be:

- a release-level action using an already authoritative earlier representation; or
- a new controlled Transition if the authoritative engineering state itself must change.

The distinction depends on which state is authoritative for the governing scope.

STATE therefore asks:

> **What state is actually being changed, and under which authority?**

rather than assuming every “rollback” is the same operation.

## 18. Provenance preservation

Provenance depth is proportional to:

- claim strength;
- consequence of substitution;
- reproducibility need;
- distribution risk;
- auditability need;
- assurance objective.

STATE does not require indefinite preservation of every intermediate object.

It requires enough preservation to support the relevant future claim.

## 19. Canonical Release rules

> **Release is distinct from Acceptance and Baseline Establishment unless authority and scope explicitly combine them.**

> **Release packaging is not assumed to be semantically neutral merely because the source state was accepted.**

> **A released object shall be traceable to the established Authoritative State to the degree required by the release claim.**

> **A digest supports identity and integrity but does not by itself establish full provenance.**

> **Release HOLD or FAILED does not retroactively remove authoritative status from the established baseline.**

> **One Authoritative State may have multiple distinct Releases.**

> **A display version label is not sufficient state identity when stronger identity is required.**

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.8  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
