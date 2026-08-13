# STATE v1.1 WP03 — Version and Release Identity Reconciliation Report

> **Document:** `10-development/STATE-V1.1-WP03-VERSION-RELEASE-IDENTITY-REPORT-001A.md`
> **Title:** STATE v1.1 WP03 — Version and Release Identity Reconciliation Report
> **Version:** 001A
> **Status:** Current Documentation
> **Created:** 2026-08-13
> **Last modified:** 2026-08-13
> **Author:** Tor-Ståle Hansen
> **Co-authors:** None

## 1. Purpose

WP03 implements owner decision D1 against authoritative start HEAD `f9bc550c79d97ae79cb4c91bb7ecc87d7abe7fb5`.

The work reconciles release identity, historical corpus identity, stable document identifiers, document-local Version metadata and Candidate development state without promoting v1.1.0 or changing STATE method semantics.

## 2. Verified historical mapping

The v1.0.0 annotated release resolves to:

- release: `v1.0.0`;
- commit: `23068ad4628c10001aa13b9963ed629b39645235`;
- historical released corpus: `0.13`;
- integrated specification: `STATE-ENGINEERING-METHOD-SPECIFICATION-013A`.

Canonical mapping:

`v1.0.0 → corpus 0.13 → Specification 013A`

## 3. Historical 0.14 clarification

The existing CHANGELOG contains a historical `0.14` Release Readiness stabilization entry.

WP03 preserves that entry but clarifies its identity: it is a stabilization milestone and does not supersede the authoritative v1.0.0 released-corpus mapping to `0.13`.

No historical record was deleted or rewritten.

## 4. Forward D1 policy

WP03 implements D1 as follows:

1. the historical `0.x` corpus-version sequence is closed;
2. no new public corpus identity shall be allocated from that sequence;
3. beginning with an accepted `v1.1.0` release, public corpus version equals release SemVer;
4. stable document identifiers remain independent of release SemVer;
5. per-document Version metadata remains document-local;
6. Candidate development state does not create an accepted release;
7. release promotion remains an explicit owner-controlled action.

## 5. Files changed

WP03 changes only:

- `README.md`;
- `CHANGELOG.md`;
- `07-reference/DOCUMENT-METADATA-TEMPLATE.md`;
- new `07-reference/VERSION-RELEASE-AND-DOCUMENT-IDENTITY.md`;
- this WP03 report.

## 6. Protected identities

WP03 does not:

- modify Specification 001A–013A;
- create or move `v1.0.0`, `v1.0.0-rc.1`, `v1.1.0` or `v1.1.0-rc.1` tags;
- publish a v1.1.0 release;
- change the current CC BY-NC-ND 4.0 licence treatment;
- resolve D2, D3, D4 or D5 beyond their already authorized planning states.

## 7. Acceptance

PASS requires:

- the historical mapping to be explicit from the repository;
- the 0.14 ambiguity to be explicitly bounded;
- no new public 0.x corpus-version allocation;
- prospective SemVer alignment to be documented;
- stable document identifiers to remain separate;
- Candidate v1.1.0 not to be represented as accepted;
- Specification 001A–013A byte identity;
- release-tag immutability;
- repository metadata consistency.

**WP03 — Version and release identity reconciliation:** PASS

`RG2 — Corpus Integrity` remains pending WP04 and WP05.

Next authorized work package after owner resolution of D5:

`WP04 — v1.0.0 release-evidence resolution`

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-SA 4.0  
Version: 001A  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
