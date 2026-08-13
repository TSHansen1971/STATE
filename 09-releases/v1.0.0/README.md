# STATE Engineering v1.0.0 — Original Release Evidence

> **Document:** `09-releases/v1.0.0/README.md`
> **Title:** STATE Engineering v1.0.0 — Original Release Evidence
> **Version:** 001A
> **Status:** Reference
> **Created:** 2026-08-13
> **Last modified:** 2026-08-13
> **Author:** Tor-Ståle Hansen
> **Co-authors:** None

## 1. Purpose

This directory publishes the original hash-bound evidence for the accepted STATE Engineering `v1.0.0` release.

Owner decision D5 selected **Path A — publish original hash-bound evidence**.

The files under `original/` are evidence payloads. They are published byte-for-byte from the original artifacts located and verified during WP04 preparation.

## 2. Integrity authority

The authoritative release identity remains the existing annotated Git tag:

`v1.0.0`

The tag object is:

`c56b5d3befd7e57d054abe9a770ecfeb064c3627`

The tag resolves to commit:

`23068ad4628c10001aa13b9963ed629b39645235`

WP04 does not create, move or rewrite that tag.

## 3. Original evidence mapping

| Tag field | Published payload | SHA-256 |
|---|---|---|
| `RC1-Review-Evidence-SHA256` | `original/STATE-METHOD-RC-REVIEW-018A-evidence-20260813-112140.tar.gz` | `c3d7be932c2bf17209b315c550727e48e5d0af8607301ce220942b88ae8a6c52` |
| `Source-Archive-SHA256` | `original/STATE-ENGINEERING-1.0.0-source.tar.gz` | `20e8f04e91cd2810061479f9333be05ce50a48a7135df80cf651998dbcf5c3a4` |
| `Source-Manifest-SHA256` | `original/STATE-ENGINEERING-1.0.0-MANIFEST.sha256.original` | `5bd4569b137383696c5114a12d49642b9025c94ce6f5320f7bee8bd9327d5d05` |
| `Promotion-Record-SHA256` | `original/STATE-ENGINEERING-1.0.0-PROMOTION-RECORD.md.original` | `9305c81ce42a99abfbba46a519c078a907e9843bc4c03eefd9b958db27cddb88` |
| `Release-Note-SHA256` | `original/STATE-ENGINEERING-1.0.0-RELEASE-NOTE.md.original` | `0ccc5b492ccb7b8107f804b08d6fb48ed4cb4b77baa0400ce78608d55e6978e3` |
| `Release-Record-SHA256` | `original/STATE-ENGINEERING-1.0.0-RELEASE-RECORD.md.original` | `3f8355b5401315b84396f2accb72f6f9cdfb3c6b2b2233ffb70c3a95432b5312` |

The `.original` suffix is a repository wrapper convention only. It prevents immutable historical text payloads from being confused with editable current STATE Markdown documentation. The suffix does not modify the payload bytes.

## 4. Verification

A third party can verify any payload by recomputing SHA-256 and comparing it directly with the corresponding hash commitment in the immutable `v1.0.0` tag.

The evidentiary chain is:

`annotated release tag → declared SHA-256 → published original payload → recomputed SHA-256`

## 5. Publication-safety decision

A bounded pre-publication inspection found:

- zero blocking secret or credential findings;
- zero oversized or uninspected binary/text units within the evidence set;
- review-level occurrences of an original local user path and author e-mail address in two evidence archives.

The owner explicitly authorized unchanged publication of those original artifacts. They were not redacted because any byte change would invalidate the tag-bound SHA-256 identity.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 001A  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
