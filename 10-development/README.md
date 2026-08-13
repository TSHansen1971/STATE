# STATE Engineering — Method Development

> **Document:** `10-development/README.md`  
> **Title:** STATE Engineering — Method Development  
> **Version:** 1.1.0  
> **Status:** Current Documentation  
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-14
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


This directory preserves the controlled development history and forward development backlog of the STATE Engineering method.

It is distinct from the normative method corpus.

Documents in this directory describe how the method itself was developed, stabilized, released and subsequently evolved. They do not become normative merely by being present here. Normative authority remains with the current STATE Engineering Method Specification and the normative precedence rules of the corpus.

## Development-lineage rule

A completed release epic may be documented retrospectively when the development history can be reconstructed from repository commits, specifications, verification records and release evidence.

A retrospective development record shall:

- identify itself explicitly as retrospective;
- distinguish historical fact from later interpretation;
- preserve the identifiers and sequence actually used;
- avoid pretending that a planning artifact existed before it was created;
- preserve immutable published release identities;
- avoid rewriting historical failures, repairs or decision boundaries.

A future epic is a Candidate planning and control artifact until explicitly accepted.

## Epic index

### STATE Engineering v1.0.0

[`STATE-EPIC-V1.0.0-001A.md`](STATE-EPIC-V1.0.0-001A.md)

Retrospective reconstruction of the development sequence that established the initial public method, matured the normative model through Specification 013A, stabilized the corpus, passed release-readiness review, established `v1.0.0-rc.1`, and promoted the unchanged method corpus to `v1.0.0`.

### STATE Engineering v1.1.0

[`STATE-EPIC-V1.1.0-001A.md`](STATE-EPIC-V1.1.0-001A.md)

Completed post-v1.0 consolidation, demonstration and operationalization epic. It began from the immutable `v1.0.0` release baseline, passed WP01–WP23 and RG1–RG6, and was owner-promoted to the stable `v1.1.0` release.

[`STATE-V1.1.0-METHOD-DEVELOPMENT-CONFORMANCE-MANIFEST-001A.md`](STATE-V1.1.0-METHOD-DEVELOPMENT-CONFORMANCE-MANIFEST-001A.md)

Retrospective self-application manifest reconstructing the v1.1.0 development and release as an evidence-bound application of STATE Engineering to the engineering of STATE Engineering itself. Its overall assessment is `SUPPORTED`; it is a development-history case and does not become normative merely by being published here.

## Historical continuity

The development lineage represented here is:

```text
Initial public foundation
        ↓
Specifications 001A–013A
        ↓
Whole-method readiness audit
        ↓
Release stabilization
        ↓
Post-stabilization readiness audit
        ↓
v1.0.0-rc.1
        ↓
RC integrity and acceptance review
        ↓
v1.0.0
        ↓
Post-v1.0 development backlog
        ↓
Candidate v1.1.0
        ↓
WP21 / RG6 release integrity
        ↓
Owner Acceptance / WP23
        ↓
v1.1.0
```

The published `v1.0.0` and `v1.0.0-rc.1` Git tags remain immutable historical release identifiers.

## Repository directory namespace

The post-v1.0 development baseline reserves the following durable top-level namespaces:

- `08-examples/` — illustrative, non-normative examples;
- `09-releases/` — release records and authorized public release evidence;
- `10-development/` — method-development history, epics and controlled planning material.

The former published development path contained a spelling error. The path is corrected prospectively through Git history rather than hidden through history rewriting.

After this correction, these top-level numbers and purposes shall not be casually renumbered or repurposed. Any later structural change requires an explicit authorized repository transition.


---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-SA 4.0  
Version: 1.1.0  
Initial publication: 2026-08-13  
Last modified: 2026-08-14
