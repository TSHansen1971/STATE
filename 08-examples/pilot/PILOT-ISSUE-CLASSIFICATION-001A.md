# STATE Pilot — Issue Classification

> **Document:** `08-examples/pilot/PILOT-ISSUE-CLASSIFICATION-001A.md`
> **Title:** STATE Pilot — Issue Classification
> **Version:** 001A
> **Status:** Current Documentation
> **Created:** 2026-08-13
> **Last modified:** 2026-08-13
> **Author:** Tor-Ståle Hansen
> **Co-authors:** None

## Purpose

Classify observed problems before proposing a method change.

## Issue classes

### `METHOD-SEMANTIC`

The existing normative model may be incomplete, contradictory or unusable under the observed condition.

### `DOCUMENTATION-AMBIGUITY`

The method may be sound, but the practitioner could not reliably understand the current documentation.

### `TAILORING-ISSUE`

The selected physical control depth or representation was too heavy, too weak or unclear.

### `ACTOR-AUTHORITY-ISSUE`

Role, Actor, Capability, Authority, delegation or boundary semantics were unclear or failed operationally.

### `EVIDENCE-OR-VERIFICATION-ISSUE`

The case exposed inadequate Evidence, Verification method, independence, sufficiency or result handling.

### `IMPLEMENTATION-OR-TOOL-ISSUE`

A problem was caused by the physical realization, toolchain or environment rather than STATE semantics.

### `OPERATOR-BURDEN`

The control activity imposed material burden that should be analyzed for Tailoring or documentation improvement.

### `PROTOCOL-ISSUE`

The validation protocol itself was unable to observe or classify the case reliably.

### `CASE-SPECIFIC`

The observation is material to this case but does not currently support a general STATE claim.

## Classification rule

An issue may have multiple plausible causes.

Record uncertainty rather than forcing one class.

```text
issue_identity:
observation:
primary_class:
alternative_class:
evidence:
impact:
confidence_in_classification:
requires_method_change: YES / NO / INCONCLUSIVE
```

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-SA 4.0  
Version: 001A  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
