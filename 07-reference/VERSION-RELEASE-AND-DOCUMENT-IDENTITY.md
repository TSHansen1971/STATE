# STATE Engineering — Version, Release and Document Identity

> **Document:** `07-reference/VERSION-RELEASE-AND-DOCUMENT-IDENTITY.md`
> **Title:** STATE Engineering — Version, Release and Document Identity
> **Version:** 001A
> **Status:** Reference
> **Created:** 2026-08-13
> **Last modified:** 2026-08-13
> **Author:** Tor-Ståle Hansen
> **Co-authors:** None

## 1. Purpose

This reference defines how STATE Engineering distinguishes release identity, public corpus identity, stable document identity, document-local version metadata and development state.

The purpose is identity clarity. This reference does not create or change STATE method semantics.

## 2. Identity classes

### 2.1 Release identity

An accepted public STATE release is identified by an authorized immutable Git release tag of the form:

`vMAJOR.MINOR.PATCH`

A target release name in planning material is not an accepted release identity.

### 2.2 Public corpus identity

For accepted STATE releases beginning with `v1.1.0`, the public corpus version is the same SemVer value as the release version, without creating a separate public corpus-version sequence.

Therefore, after the forward policy takes effect:

`release vX.Y.Z ↔ public corpus X.Y.Z`

Candidate development toward a target release does not itself create that public corpus identity.

### 2.3 Stable document identifier

A stable document identifier identifies a document or specification revision independently of release SemVer.

Example:

`STATE-ENGINEERING-METHOD-SPECIFICATION-013A`

The `013A` identifier is not a SemVer release number and shall not be inferred from, renumbered to match or conflated with a release version.

The next current integrated development specification is `014A`; that identifier is likewise a stable document identity, not release `v1.1.0`.

### 2.4 Document Version metadata

The visible per-document `Version` field is document-local revision metadata unless a document explicitly defines a different meaning.

It shall match the visible footer `Version` value in the same document.

A document-local Version value shall not, by itself, be used to infer the accepted repository release or public corpus identity.

### 2.5 Development state

A value such as `Candidate` records development or transition state.

It is not:

- an accepted release;
- a public corpus version;
- a document Status;
- a grant of Authority to promote a release.

## 3. Historical v1.0.0 mapping

The authoritative historical mapping is:

`v1.0.0 → corpus 0.13 → STATE-ENGINEERING-METHOD-SPECIFICATION-013A`

The historical `0.x` sequence is preserved as provenance.

The `0.14` Release Readiness entry in the historical CHANGELOG records a stabilization milestone. It does not supersede the authoritative released-corpus mapping above.

## 4. Forward version policy

The owner accepted the following forward policy for STATE v1.1 development:

1. the historical public/internal `0.x` corpus-version sequence is closed;
2. no new public corpus identity shall be allocated from that `0.x` sequence;
3. beginning with the accepted `v1.1.0` release, public corpus version and release SemVer are one identity;
4. stable document identifiers remain independent of release SemVer;
5. document-local Version metadata remains separate from release identity;
6. historical identities are preserved rather than rewritten;
7. a Candidate target release does not become accepted merely because development artifacts refer to it;
8. publication or movement of a release tag requires explicit authorized release action.

## 5. Current identity state during v1.1 development

At the current post-WP07 Candidate development state:

| Identity | Value |
|---|---|
| Current accepted release | `v1.0.0` |
| Authoritative v1.0.0 commit | `23068ad4628c10001aa13b9963ed629b39645235` |
| Historical released corpus identity | `0.13` |
| Released integrated specification | `STATE-ENGINEERING-METHOD-SPECIFICATION-013A` |
| Current integrated development specification | `STATE-ENGINEERING-METHOD-SPECIFICATION-014A` |
| Current development specification identifier | `014A` |
| Active development target | `v1.1.0` |
| Development target state | Candidate |
| Accepted `v1.1.0` release | Not yet established |

## 6. Interpretation rule

When identities appear together, they shall be named by class.

For example:

- **release:** `v1.0.0`;
- **historical corpus:** `0.13`;
- **specification identifier:** `013A`;
- **document Version:** the local visible Version value of the document;
- **development state:** Candidate, where applicable.

A bare number shall not be relied upon where its identity class is material to an engineering or release decision.

## 7. Historical preservation

WP03 does not rename historical specifications, alter published release tags or rewrite the historical `0.x` records.

The reconciliation is prospective: it removes ambiguity from interpretation and defines the version policy for future accepted releases.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 001A  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
