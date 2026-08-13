# STATE Engineering — Releases

> **Document:** `09-releases/README.md`
> **Title:** STATE Engineering — Releases
> **Version:** 001A
> **Status:** Current Documentation
> **Created:** 2026-08-13
> **Last modified:** 2026-08-14
> **Author:** Tor-Ståle Hansen
> **Co-authors:** None

## Purpose

This directory is the stable repository namespace for STATE Engineering release records and authorized public release evidence.

Owner decision D5 is resolved as **Path A — publish original hash-bound release evidence**.

The original evidence for `v1.0.0` and `v1.0.0-rc.1` is now published under release-specific directories and is verifiable directly against the existing immutable annotated Git tags.

## Public evidence entry point

See:

`STATE-RELEASE-EVIDENCE-INDEX-001A.md`

## Evidence-payload rule

Files under a release-specific `original/` directory are immutable evidence payloads, not editable current method documents.

They shall not be modified to satisfy later documentation formatting or metadata rules. Where an original text artifact would otherwise be mistaken for current Markdown documentation, the repository appends `.original` to the filename while preserving the exact original bytes.

No recreated or modified substitute shall be represented as original release evidence.

## Namespace boundary

The repository reserves:

- `08-examples/` for illustrative examples;
- `09-releases/` for release records and authorized public release evidence;
- `10-development/` for method-development history, epics and controlled planning material.

Published Git release tags remain immutable and are not controlled through directory changes.


## v1.1.0 — Accepted stable release

Owner-controlled WP23 promotes the accepted Candidate to stable release `v1.1.0`.

Stable release documentation and public promotion Evidence are under:

`09-releases/v1.1.0/`

The accepted Candidate remains independently identified by:

- tag: `v1.1.0-rc.1`;
- Candidate commit: `73c3fb4a9fcf7caa4f89acc840d7c856e4b63f2b`;
- RC annotated tag object: `0724b5e34e03064cb24500f7836aefb02789d257`.

The stable `v1.1.0` annotated tag is the authoritative stable release identity.

## v1.1.0-rc.1 Candidate preparation

WP22 prepares a Candidate release state for owner Acceptance.

The proposed tag name is:

`v1.1.0-rc.1`

The tag is **not published by WP22**.

Candidate preparation material is under:

`09-releases/v1.1.0-rc.1/`

The immutable Candidate identity is the WP22 commit established after all Release Integrity controls pass.


---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-SA 4.0  
Version: 001A  
Initial publication: 2026-08-13  
Last modified: 2026-08-14
