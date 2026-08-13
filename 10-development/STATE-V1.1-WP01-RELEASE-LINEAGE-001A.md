# STATE v1.1 WP01 — Release Lineage Report

> **Document:** `STATE-V1.1-WP01-RELEASE-LINEAGE-001A.md`
> **Title:** STATE v1.1 WP01 — Release Lineage Report
> **Version:** 001A
> **Status:** Current Documentation
> **Created:** 2026-08-13
> **Last modified:** 2026-08-13
> **Author:** Tor-Ståle Hansen
> **Co-authors:** None

## 1. Purpose

This report separates Git release identity, corpus-version identity, stable specification identity and post-release development identity.

## 2. Published v1.0.0 identity

| Item | Identity |
|---|---|
| Release tag | `v1.0.0` |
| Annotated tag object | `c56b5d3befd7e57d054abe9a770ecfeb064c3627` |
| Peeled commit | `23068ad4628c10001aa13b9963ed629b39645235` |
| Release-candidate tag | `v1.0.0-rc.1` |
| RC annotated tag object | `a4c3a8a7d4e0347fdbc0dcdbf91164b59e9d6220` |
| RC peeled commit | `23068ad4628c10001aa13b9963ed629b39645235` |

## 3. Post-release development lineage

| Item | Identity |
|---|---|
| Pre-correction v1.1 planning HEAD | `fa3d2af425e838ebcc06272cd0930362116ed0c9` |
| Corrected planning baseline / WP01 start HEAD | `e7a5b6edfd94040dda9dbddabdad4a570c89494f` |
| Branch | `main` |
| Remote main at WP01 capture | `e7a5b6edfd94040dda9dbddabdad4a570c89494f` |

## 4. Historical release/corpus/specification relation

The v1.1 planning baseline records:

`v1.0.0 → corpus 0.13 → Specification 013A`

D1 has authorized SemVer as the forward public corpus/release version beginning with v1.1.0. WP03, not WP01, is responsible for implementing that reconciliation in the corpus.

## 5. Identity invariant

Release version, corpus version history and stable document identifier are distinct identities. Their relation may be documented, but they shall not be conflated.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 001A  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
