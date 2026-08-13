# STATE Engineering — Tailoring Profiles by Control Intensity

> **Document:** `08-examples/TAILORING-PROFILES-BY-CONTROL-INTENSITY-001A.md`
> **Title:** STATE Engineering — Tailoring Profiles by Control Intensity
> **Version:** 001A
> **Status:** Current Documentation
> **Created:** 2026-08-13
> **Last modified:** 2026-08-13
> **Author:** Tor-Ståle Hansen
> **Co-authors:** None

## 1. Nature

These profiles are **illustrative and non-normative**.

They demonstrate how STATE can scale down and up without deleting its defining control semantics.

They do not create maturity levels or new Tailoring Invariants.

> **Tailoring may compress representation. Tailoring may not delete required control semantics.**

## 2. The invariant question

Across every profile, a third party must still be able to reconstruct the degree required by the Transition:

- Authority;
- Traceability;
- Evidence;
- Verification;
- Acceptance;
- recovery semantics.

All twelve existing Tailoring Invariants `TI-01` through `TI-12` remain applicable.

## 3. Profile A — Low-complexity bounded change

### Context

A one-line documentation correction is made in a known repository.

The change is narrow, reversible, low-coupling and straightforward to inspect.

### Tailoring approach

Use Semantic Compression.

One compact physical Transition Record can carry the logical information that would otherwise be represented across several Work Products.

### Compact Transition Record

```text
transition: TR-DOC-001
baseline: commit abc123
intent/specification:
  correct one factual spelling error in docs/page.md
acceptance_basis:
  rendered text contains the intended correction
  no other content changes
authority:
  maintainer policy authorizes this bounded documentation mutation
actor:
  H-DOC-01
boundary:
  docs/page.md only
candidate:
  commit candidate def456
verification:
  diff scope: PASS
  rendered text: PASS
evidence:
  baseline id
  one-file diff
  rendered inspection
acceptance:
  ACCEPT
baseline_establishment:
  accepted commit becomes current repository baseline
deviation:
  none
```

### Logical mapping

The single record physically combines information from `WP-01`, `WP-02`, `WP-03`, `WP-04`, `WP-05`, `WP-06`, `WP-07`, `WP-08` and `WP-09`.

No logical Work Product class is deleted.

`WP-10` is not applicable because no distinct Release occurs.

`WP-11` is conditional and not needed because no material deviation or Authority uncertainty occurs.

### Recovery semantics

If rendered Verification fails, the FAIL is preserved. The repair resumes from the earliest invalidated control condition rather than silently changing the Acceptance basis.

### Profile A conclusion

Administrative representation is compressed heavily.

Authority, Traceability, Evidence, Verification, Acceptance and recovery semantics remain reconstructable.

## 4. Profile B — Controlled engineering change

### Context

A routine application change touches several implementation files and established tests.

Consequence and coupling are moderate.

### Tailoring approach

Use ordinary STATE Work Product separation similar to the existing standard controlled profile.

### Physical records

```text
Transition Charter / Contract
Authority Grant
Actor Assignment
Baseline Record
Transition Record
Verification Record
Evidence Set
Acceptance Record
Baseline Establishment Record
Deviation / Repair record when required
Release Record only when a distinct Release occurs
```

### Actor arrangement

- human Transition Authority;
- human or synthetic Realization Actor;
- separate review/Verification activity where useful;
- Evidence Stewardship may be automated;
- human or legitimately delegated Acceptance Authority;
- Baseline Custodian establishes P9.

### Evidence depth

Typical Evidence includes:

- Baseline and Candidate identity;
- transformation diff;
- build/construction Evidence;
- behavioral/regression Evidence;
- environment identity where relevant;
- negative Evidence;
- decision/provenance records.

### Failure and repair

A Required Claim that FAILs remains FAIL.

The Transition records `REPAIR REQUIRED`, identifies the earliest invalidated phase and repeats the required downstream controls for the repaired Candidate.

### Profile B conclusion

Representation is moderately separated because the engineering context benefits from explicit handoffs and claim-bound Verification.

No additional STATE semantics are created.

## 5. Profile C — High-consequence / high-complexity Transition

### Context

One or more conditions apply:

- high consequence of error;
- strong security relevance;
- low reversibility;
- broad exposure;
- complex system interaction;
- multiple Work Packages or suppliers;
- substantial uncertainty;
- strong provenance need.

### Tailoring approach

Increase control depth where tied to claims, consequence, uncertainty or Assurance need.

Do not increase ceremony merely for appearance.

### Authority separation

Use explicit, separately identifiable:

- Intent Authority;
- Architecture Authority where relevant;
- Transition Authority;
- Realization Role / Actors;
- independent or failure-source-separated Verification;
- Evidence Stewardship;
- Acceptance Authority;
- Baseline Custodianship.

Capability overlap does not merge these Authority rights.

### Evidence and provenance

Evidence may include:

- stronger Baseline and Candidate identity;
- Work-Package-local and integrated Evidence;
- environment and toolchain identity;
- source-to-artifact provenance;
- supplier handoff provenance;
- negative Evidence;
- independent reproduction where justified;
- security-specific Verification where relevant;
- retained residual uncertainty;
- explicit release provenance if Release occurs.

### Independent Verification

Critical claims may use different Actors, tools, methods, environments or organizations where those separations reduce material common-cause failure.

A second Actor is not automatically independent.

### Acceptance

Acceptance Authority receives a decision-ready Evidence Set containing both positive and negative Evidence.

Assurance does not rewrite Verification.

Acceptance does not establish the new Authoritative State by itself; P9 remains distinct.

### Recovery

Failure is preserved and repair resumes from the earliest invalidated control condition.

If scope, consequence, security relevance, Actor arrangement, environment or uncertainty materially changes, re-Tailoring is required.

### Profile C conclusion

Control depth is stronger, but no heavier profile is “more STATE” than a lighter conformant realization.

## 6. Cross-profile comparison

| Control concern | Profile A | Profile B | Profile C |
|---|---|---|---|
| Physical representation | one compact record | separated ordinary records | separated and deeper evidence/provenance |
| Authority | compact but explicit/inherited | explicit grant and assignment | strongly separated authority domains |
| Traceability | compact chain | ordinary record links | Work Package + integrated provenance |
| Verification | focused deterministic inspection | normal build/test/review | multiple/independent methods where justified |
| Evidence | minimal claim-sufficient | ordinary engineering Evidence | deeper provenance, environment, negative Evidence |
| Acceptance | concise explicit decision | explicit Acceptance Record | separate Acceptance Authority and stronger basis |
| Recovery | same earliest-invalidated-phase rule | explicit repair record when needed | explicit repair + re-Tailoring triggers |
| Tailoring Invariants | all retained | all retained | all retained |

## 7. Control-compression test

A compressed realization is acceptable only while the required semantics remain reconstructable.

Compression becomes Control Deletion when it removes, for example:

- the known Baseline;
- sufficient Specification;
- bounded Authority;
- Candidate identity;
- claim-bound Verification;
- decision-relevant Evidence;
- explicit failure/uncertainty;
- Acceptance;
- P9 Baseline Establishment;
- material provenance;
- secure-engineering treatment where applicable.

## 8. Operational conclusion

The lightest realization can be the correct STATE realization.

The heaviest realization can still be wrong if it deletes or confuses control semantics.

> **Semantic Compression preserves control; Control Deletion does not.**

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-SA 4.0  
Version: 001A  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
