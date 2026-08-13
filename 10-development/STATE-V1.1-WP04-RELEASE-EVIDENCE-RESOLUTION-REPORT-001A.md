# STATE v1.1 WP04 — v1.0.0 Release Evidence Resolution Report

> **Document:** `10-development/STATE-V1.1-WP04-RELEASE-EVIDENCE-RESOLUTION-REPORT-001A.md`
> **Title:** STATE v1.1 WP04 — v1.0.0 Release Evidence Resolution Report
> **Version:** 001A
> **Status:** Current Documentation
> **Created:** 2026-08-13
> **Last modified:** 2026-08-13
> **Author:** Tor-Ståle Hansen
> **Co-authors:** None

## 1. Purpose

WP04 resolves owner decision D5 by implementing **Path A — publish original hash-bound release evidence**.

The authoritative WP04 start HEAD is:

`9b888c01f772da5295aa1b62e1cf23b211e82128`

## 2. Decision basis

Before publication:

- all eleven tag-field commitments were captured from `v1.0.0` and `v1.0.0-rc.1`;
- those commitments resolve to ten unique SHA-256 artifact identities;
- all ten unique original artifacts were located as exact local hash matches;
- all ten were reverified immediately before publication;
- publication-safety inspection found zero blocking secret or credential findings;
- review-level local user-path and author e-mail occurrences were explicitly accepted by the owner for unchanged publication.

## 3. Publication rule

Every evidence payload published by WP04 is byte-identical to the corresponding original.

Where original text evidence used a `.md` or `.sha256` filename, the public repository appends `.original` to distinguish immutable evidence payloads from editable current documentation.

The filename wrapper does not change file bytes or SHA-256.

## 4. Public evidence locations

- `09-releases/v1.0.0/`
- `09-releases/v1.0.0-rc.1/`
- `09-releases/STATE-RELEASE-EVIDENCE-INDEX-001A.md`

## 5. Integrity model

A public claim that an artifact is original release evidence is supported only when:

`existing immutable tag commitment == recomputed SHA-256 of published payload`

WP04 does not rely on a recreated narrative artifact as proof of the historical release event.

## 6. Protected state

WP04 does not:

- modify `v1.0.0` or `v1.0.0-rc.1`;
- create or promote `v1.1.0`;
- alter Specification 001A–013A;
- change STATE method semantics;
- perform the future licence transition;
- resolve WP05 traceability.

## 7. Acceptance

PASS requires:

- every tag commitment represented by an original published payload;
- exact SHA-256 equality for every published payload;
- byte identity between source original and public copy;
- explicit wrapper documentation;
- D5 recorded as Path A;
- release-tag immutability;
- clean post-commit repository state.

**WP04 — v1.0.0 release-evidence resolution:** PASS

`RG2 — Corpus Integrity` remains pending WP05.

Next authorized work package:

`WP05 — Traceability closure and matrix generation`

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 001A  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
