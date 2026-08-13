# STATE Engineering v1.0.0-rc.1 — Original Release-Candidate Evidence

> **Document:** `09-releases/v1.0.0-rc.1/README.md`
> **Title:** STATE Engineering v1.0.0-rc.1 — Original Release-Candidate Evidence
> **Version:** 001A
> **Status:** Reference
> **Created:** 2026-08-13
> **Last modified:** 2026-08-13
> **Author:** Tor-Ståle Hansen
> **Co-authors:** None

## 1. Purpose

This directory publishes the original hash-bound evidence for STATE Engineering release candidate `v1.0.0-rc.1`.

The files under `original/` are published byte-for-byte from the original artifacts verified during WP04 preparation.

## 2. Integrity authority

The authoritative release-candidate identity remains the existing annotated Git tag:

`v1.0.0-rc.1`

The tag object is:

`a4c3a8a7d4e0347fdbc0dcdbf91164b59e9d6220`

The tag resolves to commit:

`23068ad4628c10001aa13b9963ed629b39645235`

WP04 does not create, move or rewrite that tag.

## 3. Original evidence mapping

| Tag field | Published payload | SHA-256 |
|---|---|---|
| `Readiness-Evidence-SHA256` | `original/STATE-METHOD-READINESS-016A-evidence-20260813-110614.tar.gz` | `da30e11fc44b7f65c55229c97c9231a62e21749e4944d988a823793a7365b2a2` |
| `Source-Archive-SHA256` | `original/STATE-ENGINEERING-1.0-RC1-source.tar.gz` | `2736ab792236e042823b4f5b708f96f37a06de0c82b10394c1a3135d9d93d3e9` |
| `Source-Manifest-SHA256` | `original/STATE-ENGINEERING-1.0-RC1-MANIFEST.sha256.original` | `5bd4569b137383696c5114a12d49642b9025c94ce6f5320f7bee8bd9327d5d05` |
| `Release-Note-SHA256` | `original/STATE-ENGINEERING-1.0-RC1-RELEASE-NOTE.md.original` | `a797bec7af2c5f3e7b4aaaa522a7b9cc24ad3d4123425029a0810e5646ce9a45` |
| `Release-Record-SHA256` | `original/STATE-ENGINEERING-1.0-RC1-RELEASE-RECORD.md.original` | `dbf9ed56ded7f01d072e91c8b2e54c02d43c4225cf931dab1376fa566ad70bda` |

The Source Manifest has the same SHA-256 commitment as the v1.0.0 Source Manifest. Both original release-context files are retained under their respective published paths.

## 4. Verification

Recompute SHA-256 for a payload and compare it directly with the corresponding commitment in the immutable `v1.0.0-rc.1` tag.

No recreated substitute is represented as original evidence.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-SA 4.0  
Version: 001A  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
