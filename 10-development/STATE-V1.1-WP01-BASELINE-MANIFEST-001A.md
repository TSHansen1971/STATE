# STATE v1.1 WP01 — Authoritative Baseline Manifest

> **Document:** `STATE-V1.1-WP01-BASELINE-MANIFEST-001A.md`
> **Title:** STATE v1.1 WP01 — Authoritative Baseline Manifest
> **Version:** 001A
> **Status:** Current Documentation
> **Created:** 2026-08-13
> **Last modified:** 2026-08-13
> **Author:** Tor-Ståle Hansen
> **Co-authors:** None

## 1. Purpose

This document records the authoritative post-v1.0 starting state for STATE Engineering v1.1.0 after the controlled pre-WP01 planning-baseline correction.

WP01 captures identity and evidence. It does not normalize, repair or otherwise mutate the normative method corpus.

## 2. Repository identity

- Repository: `/Users/tostha/prosjekter/state`
- Branch: `main`
- Authoritative pre-WP01 HEAD: `e7a5b6edfd94040dda9dbddabdad4a570c89494f`
- Parent: `fa3d2af425e838ebcc06272cd0930362116ed0c9`
- Commit subject: `docs: correct STATE v1.1 planning baseline`
- Origin: `git@github.com:TSHansen1971/STATE.git`
- Remote `main` at capture: `e7a5b6edfd94040dda9dbddabdad4a570c89494f`
- Working tree at capture: clean

## 3. Corrected repository namespace

The captured baseline contains the durable top-level namespaces:

- `08-examples/`;
- `09-releases/`;
- `10-development/`.

The former misspelled development namespace is not tracked in this baseline.

## 4. Published release identity

- `v1.0.0` annotated tag object: `c56b5d3befd7e57d054abe9a770ecfeb064c3627`
- `v1.0.0` peeled commit: `23068ad4628c10001aa13b9963ed629b39645235`
- `v1.0.0-rc.1` annotated tag object: `a4c3a8a7d4e0347fdbc0dcdbf91164b59e9d6220`
- `v1.0.0-rc.1` peeled commit: `23068ad4628c10001aa13b9963ed629b39645235`

Local and remote tag identities were equal at capture time.

## 5. Baseline specification

- Path: `00-foundation/STATE-ENGINEERING-METHOD-SPECIFICATION-013A.md`
- SHA-256: `5d6a56185fab283be5de38ef57cf8c8e23a613ff34ff31d546aeff05e139ac71`
- Historical relation carried into v1.1 reconciliation: `v1.0.0 → corpus 0.13 → Specification 013A`

## 6. Owner decisions at baseline

- D1 — Public version policy: ACCEPTED; implementation belongs to WP03.
- D2 — Next specification identifier: PENDING EVIDENCE.
- D3 — Documentation licence: ACCEPTED; implementation belongs to WP19.
- D4 — Canonical STATE decomposition: ACCEPTED; controlled integration belongs to WP20.
- D5 — v1.0.0 release-evidence publication: PENDING WP01 EVIDENCE.

## 7. WP01 acceptance

The authoritative post-v1.0 starting state is reconstructable from repository identity, Git lineage, release tags, specification identity, file hashes, metadata inventory and evidence-location observations.

**WP01:** PASS  
**RG1 — Baseline Integrity:** PASS

This result does not convert any discrepancy discovered by WP01 into PASS for a later work package.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 001A  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
