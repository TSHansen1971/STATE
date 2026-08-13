# Tailoring Model

> **Document:** `05-tailoring/01-tailoring-model.md`  
> **Title:** Tailoring Model  
> **Version:** 0.10  
> **Status:** Normative Specification
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


Tailoring is the controlled adaptation of STATE Engineering to the consequence, complexity, uncertainty and physical realization of a specific engineering context.

## 1. Tailoring definition

> **Tailoring is the authorized selection of representation, depth, automation, separation and evidence controls within a bounded Tailoring Envelope while preserving the defining semantics of STATE Engineering.**

Tailoring is not permission to remove controls without analysis.

## 2. Tailoring Envelope

The **Tailoring Envelope** is the range of implementation variation allowed while the Foundational Properties and mandatory logical distinctions remain intact.

The envelope separates:

```text
TAILORABLE
physical form
depth
granularity
automation
Actor arrangement
evidence volume
verification method
independence depth
retention depth
release mechanism

from

NON-TAILORABLE
authority semantics
Candidate semantics
claim-bound Verification
Evidence-Based Acceptance
explicit failure
Acceptance / Baseline separation
traceability
secure engineering
authoritative-state integrity
```

## 3. Foundational Properties are non-tailorable

The twelve Foundational Properties are constitutive.

Tailoring may alter how a property is realized.

It may not declare the property unnecessary.

For example:

- Specification may be one paragraph rather than a separate document.
- Authority may be inherited from an established policy rather than manually approved per change.
- Evidence may be three concise records rather than an archive.
- Verification may be automated.
- Baseline Establishment may be performed by a deterministic repository operation.

The underlying semantics remain.

## 4. Tailoring Invariants

STATE defines twelve operational Tailoring Invariants.

### TI-01 — Known Authoritative Starting State

The Transition shall have a sufficiently identified Authoritative State / Baseline.

### TI-02 — Specification before governed mutation

The intended change and Acceptance basis shall be sufficiently established before controlled Candidate production.

### TI-03 — Explicit and bounded Authority

Authority shall be explicit or explicitly inherited and bounded to the relevant scope.

### TI-04 — Role / Actor / Capability / Authority separation

Physical convenience shall not erase the distinction among these concepts.

### TI-05 — Candidate before Authority

Produced state remains non-authoritative until Acceptance and Baseline Establishment complete.

### TI-06 — Bounded Transition

Mutation shall remain within an explicit Transition Boundary or follow explicit escalation.

### TI-07 — Claim-bound Verification

Verification shall identify what claim is being evaluated and against which target.

### TI-08 — Evidence-Based Acceptance

Acceptance shall have an evidentiary basis proportionate to the claim and consequence.

### TI-09 — Acceptance / Baseline Establishment separation

ACCEPT and establishment of authoritative state remain distinct logical acts even if one physical operation implements both.

### TI-10 — Explicit Failure and Uncertainty

FAIL, INCONCLUSIVE, HOLD and other non-success conditions shall not be silently converted into success.

### TI-11 — Traceability and Provenance

Relevant relationships among Baseline, authority, transformation, Verification, Evidence, Acceptance and resulting state shall remain reconstructable.

### TI-12 — Secure Engineering by Construction

Security-relevant properties shall remain part of ordinary engineering control where applicable.

## 5. Semantic Compression

**Semantic Compression** means physically combining several logical control elements while preserving their meaning.

Example:

```text
one compact change record
 ├── baseline
 ├── intent
 ├── boundary
 ├── Actor / authority
 ├── diff identity
 ├── verification
 ├── evidence
 ├── ACCEPT
 └── new baseline identity
```

This may represent many STATE Work Products and gate conditions in one physical object.

Semantic Compression is encouraged where it reduces unnecessary process cost without weakening control.

## 6. Control Deletion

**Control Deletion** occurs when Tailoring removes a required semantic control rather than changing its representation.

Examples include:

- no known Baseline;
- mutation without sufficient specification;
- Actor capability treated as Authority;
- failed verification omitted because it is inconvenient;
- Candidate treated as authoritative because build succeeded;
- ACCEPT treated as equivalent to P9 without establishment identity;
- package-local PASS substituted for integrated claim;
- security-relevant change treated as functionally verified only.

Control Deletion is not conformant Tailoring.

## 7. Logical versus physical phase compression

P0–P9 are logical phase semantics.

A small Transition does not require ten meetings or ten chronological execution blocks.

Example:

```text
one script / one controlled session
can establish:
P0, P1, P2, P3
then execute:
P4, P5, P6, P7
then record:
P8, P9
```

This remains STATE if the gate conditions and logical distinctions are genuinely established.

## 8. Gate automation

Gates may be:

- manually evaluated;
- deterministically automated;
- delegated through policy;
- evaluated by synthetic Actors;
- hybrid.

Automation changes the physical mechanism, not the logical condition.

Where a gate exercises Authority, the authority delegation shall remain valid.

## 9. Work Product compression

WP-01–WP-11 are logical information classes.

Tailoring may:

- combine several into one record;
- distribute one Work Product across several systems;
- use machine-readable representation;
- generate Work Products automatically;
- omit conditional Work Products when the condition does not exist.

Tailoring shall not make required information unreconstructable.

## 10. Role combination

Tailoring may assign several logical Roles to one physical Actor.

The decision shall consider:

- consequence;
- conflict of interest;
- common-cause failure;
- required independence;
- Actor capability;
- evidence quality.

Logical separation remains.

## 11. Verification tailoring

Verification may be tailored in:

- method;
- coverage;
- target breadth;
- environment diversity;
- reproducibility;
- independence;
- security depth;
- performance depth.

Tailoring shall remain driven by claims.

A low-risk change does not require maximum verification.

A high-consequence claim cannot be justified by weak verification merely because deeper verification is inconvenient.

## 12. Evidence tailoring

Evidence depth may be tailored through:

- number of Evidence Items;
- identity strength;
- environment capture;
- preservation duration;
- integrity mechanism;
- reproducibility;
- provenance depth.

Evidence volume is not a proxy for evidence quality.

## 13. Environment tailoring

Environment identity depth depends on the claim.

Examples:

- a Markdown typo correction may require only repository and source identity;
- a compiler-sensitive change may require toolchain identity;
- a performance claim may require hardware and workload conditions;
- a local-model behavior claim may require model/runtime/configuration identity.

## 14. Release tailoring

Release controls are conditional.

A Transition that establishes an internal Authoritative State without external Release does not require WP-10.

A Transition with multiple distributed artifacts may require strong release identity, transformation verification and provenance.

## 15. Tailoring and secure engineering

Tailoring may scale security verification according to relevance and consequence.

It may not declare a security-relevant effect non-security-relevant merely to reduce work.

## 16. Tailoring and no false green

Tailoring decisions shall not be made retrospectively merely to turn an observed failure into success.

A legitimate post-failure change in Acceptance basis is a controlled Contract amendment, not Tailoring of history.

## 17. Tailoring authority

Tailoring itself is an engineering control decision.

The Actor or Role establishing Tailoring shall have authority sufficient to determine the permitted method realization for the scope.

Tailoring Authority may be inherited through organizational or project policy.

## 18. Tailoring evidence

For low-consequence work, the Tailoring rationale may be implicit in an established profile.

For higher-consequence or unusual work, the rationale should be explicit enough to reconstruct why the selected control depth was considered sufficient.

## 19. Re-tailoring

Tailoring shall be reconsidered when the original context materially changes.

Examples:

- scope expands;
- consequence increases;
- new security relevance appears;
- Work Packages become distributed;
- Actor is substituted;
- environment becomes less controlled;
- uncertainty increases;
- Release scope expands;
- verification repeatedly fails.

## 20. Canonical Tailoring rules

> **Tailor physical form and control depth; do not tailor away the control semantics.**

> **Foundational Properties are non-tailorable.**

> **Semantic Compression is permitted; Control Deletion is not.**

> **P0–P9 may be physically compressed, but their required semantics shall remain.**

> **Logical Roles may be physically combined, but their distinctions shall remain.**

> **Verification and evidence depth are proportional to the claim, consequence and uncertainty.**

> **Tailoring shall not be performed retrospectively merely to manufacture a successful result.**

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-SA 4.0  
Version: 0.10  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
