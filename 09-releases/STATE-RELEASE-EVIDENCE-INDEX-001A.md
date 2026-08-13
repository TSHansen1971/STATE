# STATE Engineering — Public Release Evidence Index

> **Document:** `09-releases/STATE-RELEASE-EVIDENCE-INDEX-001A.md`
> **Title:** STATE Engineering — Public Release Evidence Index
> **Version:** 001A
> **Status:** Reference
> **Created:** 2026-08-13
> **Last modified:** 2026-08-14
> **Author:** Tor-Ståle Hansen
> **Co-authors:** None

## 1. Purpose

This index provides the public verification entry point for original STATE Engineering release evidence published under owner decision D5 Path A.

## 2. Published evidence sets

| Release identity | Evidence directory | Tag state |
|---|---|---|
| `v1.1.0` | `09-releases/v1.1.0/` | Owner-promoted immutable annotated tag |
| `v1.1.0-rc.1` | `09-releases/v1.1.0-rc.1/` | Accepted immutable Release Candidate tag |
| `v1.0.0` | `09-releases/v1.0.0/` | Existing immutable annotated tag |
| `v1.0.0-rc.1` | `09-releases/v1.0.0-rc.1/` | Existing immutable annotated tag |

## 2.1 v1.1.0 promotion Evidence

The v1.1.0 release uses a forward promotion-evidence model.

The public stable-release directory contains:

- the exact owner Acceptance statement and its SHA-256;
- the promotion record;
- release manifest;
- release note;
- release Evidence package.

The stable annotated tag binds these release artifacts and the accepted Candidate evidence.

Owner Acceptance statement SHA-256:

`9b67c0899d810767f3abf999c6d6feb531f0c7d72a894a036666222f8d836b42`

## 3. Verification model

The public verification model is:

1. inspect the existing annotated Git tag;
2. obtain the hash commitment for the relevant artifact class;
3. recompute SHA-256 over the published payload under the matching release directory;
4. require exact equality;
5. treat any inequality as verification failure.

The publication wrapper documents are not substitutes for the evidence. The hash-bound payload bytes are the evidence.

## 4. Historical integrity

The evidence was not regenerated for WP04.

The ten unique hash-bound original artifact identities were located locally, reverified against the existing tag commitments and then copied byte-for-byte into the public release namespace.

Eleven tag-field commitments are represented because the Source Manifest SHA-256 is shared by both release contexts.

## 5. Original text-payload convention

Original text evidence that historically used `.md` or `.sha256` filenames is published with an additional `.original` suffix.

This suffix exists only to distinguish immutable evidence payloads from editable repository documentation. Verification is over file bytes, and those bytes are unchanged from the originals bound by the release tags.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-SA 4.0  
Version: 001A  
Initial publication: 2026-08-13  
Last modified: 2026-08-14
