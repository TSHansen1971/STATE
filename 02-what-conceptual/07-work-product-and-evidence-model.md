# Work Product and Evidence Model

> **Document:** `02-what-conceptual/07-work-product-and-evidence-model.md`  
> **Title:** Work Product and Evidence Model  
> **Version:** 0.4  
> **Status:** Normative Specification
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


The Work Product and Evidence Model defines the information objects required to control, reconstruct and justify a STATE Transition.

It is deliberately logical rather than document-centric.

## 1. Work Product

A **Work Product** is an identifiable information object produced, maintained or consumed by one or more STATE roles for the purpose of controlling, performing, verifying, evidencing or authorizing a Transition.

A Work Product may be:

- persistent or transient;
- human-readable or machine-readable;
- stored as a file, repository object, issue, database record, automated log or other representation;
- represented independently or combined physically with other Work Products.

The logical identity of the Work Product is more important than its storage format.

## 2. Logical work product is not physical document

STATE explicitly rejects the assumption that every logical Work Product requires a separate document.

For example, a low-risk Transition could represent:

- Transition Intent and Specification;
- Authority Grant;
- Actor Assignment;
- Verification Result;
- Acceptance Record;

inside one structured issue or change record.

A higher-assurance Transition may require these as separately controlled records.

The Tailoring question is:

> **Can the required information, authority, evidence and traceability be distinguished and reconstructed with the required assurance?**

If yes, physical consolidation is allowed.

## 3. Canonical Work Product classes

STATE defines eleven canonical Work Product classes.

### WP-01 — Transition Intent and Specification

**Purpose:** define what the Transition is intended to achieve and the basis on which its result will be judged.

Typical content includes:

- intended outcome;
- relevant constraints;
- relevant invariants;
- non-goals;
- acceptance basis;
- unresolved assumptions;
- references to governing intent or architecture where needed.

Primary relationship: Specification Role.

### WP-02 — Authority Grant

**Purpose:** record or reference the authority under which a role or actor may decide, approve, delegate or mutate within the Transition.

Typical content includes:

- authority source;
- authority domain;
- scope;
- permitted actions;
- constraints;
- validity;
- escalation conditions;
- delegation conditions;
- revocation conditions.

Primary relationship: applicable Authority Domain.

### WP-03 — Actor Assignment

**Purpose:** bind actual human, synthetic or hybrid actors to logical STATE roles and relevant Authority Grants.

Typical content includes:

- actor identity or actor class;
- assigned role or roles;
- required capability;
- granted authority;
- applicable scope;
- evidence obligations;
- independence requirements.

### WP-04 — Baseline Record

**Purpose:** identify the Authoritative State selected as input to the Transition.

Typical content may include:

- source revision;
- configuration identity;
- dependency identity;
- environment identity;
- relevant artifact identity;
- date or sequence identity;
- references to previous acceptance.

The required depth depends on the claim being accepted.

Primary relationship: Baseline Custodianship Role.

### WP-05 — Transition Record

**Purpose:** provide the central traceability object connecting the authorized input state to the resulting candidate and decision.

The Transition Record should be capable of referencing:

- Transition ID;
- Baseline Record;
- Transition Intent and Specification;
- Authority Grants;
- Actor Assignments;
- relevant invariants;
- actual mutation;
- verification;
- evidence;
- deviations;
- Acceptance Record;
- resulting state identity.

The Transition Record may itself contain some of these logical Work Products or reference them externally.

### WP-06 — Verification Record

**Purpose:** record what was verified, how it was verified and what result was obtained.

Typical content includes:

- claim or requirement under verification;
- verification method;
- verification conditions;
- observed result;
- PASS, FAIL or INCONCLUSIVE conclusion where applicable;
- verifier identity or role;
- limitations;
- references to Evidence Items.

Primary relationship: Verification Role.

### WP-07 — Evidence Set

**Purpose:** bind the Evidence Items relevant to one or more engineering claims.

An Evidence Set may be represented as:

- a manifest;
- a directory or archive;
- references to immutable records;
- a structured database object;
- a signed collection;
- another controlled representation.

The Evidence Set should allow relevant evidence to be associated with the correct baseline, candidate, verification and decision.

Primary relationship: Evidence Stewardship Role.

### WP-08 — Acceptance Record

**Purpose:** record the authorized decision about the Candidate State.

Valid decisions include:

- ACCEPT;
- REJECT;
- REPAIR REQUIRED;
- INCONCLUSIVE.

Typical content includes:

- Candidate State identity;
- acceptance claims;
- verification basis;
- evidence references;
- known deviations;
- decision;
- Acceptance Authority;
- decision date or sequence.

### WP-09 — Baseline Establishment Record

**Purpose:** establish the identity of a newly accepted state as the next Authoritative State.

It links:

- prior baseline;
- accepted Transition;
- Acceptance Record;
- resulting state identity;
- effective authority status.

This Work Product prevents the logical leap from “accepted candidate” to “assumed baseline.”

### WP-10 — Release Record

**Purpose:** record release or deployment authorization when release is a distinct governance act.

Typical content includes:

- accepted state identity;
- released artifact identity;
- release target or channel;
- Release Authority;
- provenance reference;
- release decision.

This Work Product is conditional.

### WP-11 — Deviation and Escalation Record

**Purpose:** preserve material departures, discovered boundary conditions, unresolved authority questions or accepted deviations that influence the Transition decision.

This Work Product is created only when such a condition exists.

It may record:

- deviation from specification;
- requested scope expansion;
- authority uncertainty;
- verification limitation;
- accepted exception;
- unresolved risk;
- escalation and decision.

## 4. Required information, optional physical separation

STATE distinguishes between:

- **logical requirement** — the information must exist when applicable;
- **physical representation** — where and how that information is stored.

A Work Product class may therefore be mandatory for a Transition while its separate file representation remains optional.

Example:

```text
One structured Transition record
    │
    ├── WP-01 Specification section
    ├── WP-02 Authority section
    ├── WP-03 Actor assignment section
    ├── WP-06 Verification section
    ├── WP-08 Acceptance section
    └── references WP-07 Evidence Set
```

This remains valid STATE if the logical distinctions and required traceability are preserved.

## 5. Evidence Item

An **Evidence Item** is an identifiable observation, artifact, record or measurement used to support or challenge an engineering claim.

Examples include:

- a commit identity;
- a diff;
- a build log;
- a test result;
- a runtime observation;
- a permission comparison;
- an artifact hash;
- an environment manifest;
- a signature;
- a release digest.

Evidence Items become useful only in relation to claims.

## 6. Claim–Evidence Binding

STATE uses a claim-bound evidence model.

> **Evidence is not sufficient merely because it exists. It must be relevant to the claim being accepted.**

A Verification Record should therefore be capable of expressing:

```text
CLAIM
What is asserted?

METHOD
How was the claim evaluated?

OBSERVATION
What was observed?

EVIDENCE
Which identifiable Evidence Items support or challenge the observation?

CONCLUSION
PASS / FAIL / INCONCLUSIVE or another explicitly defined result

LIMITATION
What remains unproven or uncertain?
```

## 7. Evidence classes

STATE defines ten canonical evidence classes.

### EC-01 — Identity Evidence

Supports claims about which state, source, file, artifact or release is being discussed.

Examples:

- commit identifiers;
- cryptographic digests;
- manifests;
- immutable object identities.

### EC-02 — Authority Evidence

Supports claims about who or what was authorized to decide or act.

Examples:

- Authority Grant;
- approval record;
- policy decision;
- delegated authorization record.

### EC-03 — Transformation Evidence

Supports claims about what changed between states.

Examples:

- diff;
- patch;
- migration record;
- changed-file manifest;
- configuration delta.

### EC-04 — Construction and Build Evidence

Supports claims about successful or failed construction, compilation, packaging or assembly.

Examples:

- build log;
- compiler output;
- package manifest;
- signing output.

### EC-05 — Behavioral Evidence

Supports claims about observed system behavior.

Examples:

- runtime observations;
- functional tests;
- integration tests;
- measured outputs.

### EC-06 — Regression and Preservation Evidence

Supports claims that required pre-existing properties remained true.

Examples:

- regression tests;
- invariant checks;
- compatibility checks;
- before/after behavioral comparison.

### EC-07 — Security and Boundary Evidence

Supports claims about security-relevant properties or boundaries.

Examples:

- privilege comparison;
- access-control verification;
- trust-boundary analysis;
- security test result;
- attack-surface comparison;
- failure-mode observation.

### EC-08 — Environment Evidence

Supports claims about the conditions under which construction or verification occurred.

Examples:

- operating-system identity;
- toolchain version;
- dependency state;
- hardware or runtime characteristics;
- environment configuration.

### EC-09 — Provenance and Integrity Evidence

Supports claims that an artifact or state originates from the asserted source and has not been silently substituted.

Examples:

- hash chains;
- source-to-artifact manifests;
- signatures;
- reproducible build records;
- artifact lineage.

### EC-10 — Decision Evidence

Supports reconstruction of the engineering decision itself.

Examples:

- Acceptance Record;
- rejection rationale;
- repair decision;
- escalation decision;
- Release Record.

## 8. Evidence-quality properties

Evidence should be evaluated through the following properties to the degree relevant to the claim.

### EQ-01 — Relevance

Does the Evidence Item actually bear on the claim?

### EQ-02 — Identity

Can the Evidence Item itself be identified unambiguously enough for the claim?

### EQ-03 — Integrity

Is there sufficient basis to trust that the Evidence Item was not unintentionally or silently altered?

### EQ-04 — Provenance

Can the origin and transformation history of the Evidence Item be established to the required degree?

### EQ-05 — Sufficiency

Does the Evidence Set provide enough basis for the strength of the claim?

### EQ-06 — Reproducibility

Can the observation or verification be repeated to the degree required?

Reproducibility does not always mean byte-identical results.

### EQ-07 — Independence

Is the evidence or verification sufficiently independent from the production mechanism for the required Assurance level?

### EQ-08 — Timeliness

Does the evidence correspond to the state, candidate, environment and decision actually being evaluated?

### EQ-09 — Preservation

Can the Evidence Item remain available and interpretable for as long as the relevant claim requires?

## 9. Evidence sufficiency

Evidence sufficiency is not measured by file count.

A large Evidence Set may still be weak if it does not support the relevant claim.

A small Evidence Set may be sufficient for a narrow low-consequence claim.

The governing principle remains:

> **The strength of evidence should be proportionate to the strength of the claim, the consequence of error and the uncertainty that remains.**

## 10. Negative evidence

Evidence may challenge a claim.

FAIL and INCONCLUSIVE evidence are first-class engineering results.

Evidence shall not be discarded merely because it does not support acceptance when it remains relevant to diagnosis, assurance, decision provenance or later repair.

## 11. Evidence and actor independence

The evidence obligation belongs to the logical Transition and role model, not to a particular actor class.

A human team, offshore supplier, deterministic automation or synthetic actor may all be required to produce the same logical evidence classes.

The physical mechanism may differ.

## 12. Evidence and secure engineering

Security-relevant claims require security-relevant Evidence Items.

A functional PASS cannot be treated as evidence that unrelated privilege, trust, exposure, provenance or failure properties remain acceptable.

## 13. Evidence and privacy or domain rules

The universal STATE Evidence Model describes engineering evidence.

It does not define jurisdiction-, sector-, mission- or organization-specific retention, privacy, classification or disclosure rules.

Those constraints are introduced through Tailoring where applicable.

## 14. Work Product lifecycle

A logical Work Product may evolve through the Transition.

Examples:

- Specification may be clarified under authorized change;
- Actor Assignment may change;
- Verification Record may acquire additional observations;
- Evidence Set may expand;
- Acceptance Record is created only when a decision is made;
- Baseline Establishment Record exists only after acceptance establishes a new authoritative state.

Version and identity controls should reflect the consequence of silently confusing one revision with another.

## 15. Work Product ownership

No Work Product is authoritative merely because one role created it.

Its authority depends on its function.

Examples:

- the Realization Role may produce transformation evidence but does not thereby create Acceptance Authority;
- the Verification Role may produce a PASS result but does not thereby establish the baseline;
- the Baseline Custodianship Role may record a new baseline but only after valid Acceptance;
- the Evidence Stewardship Role preserves evidence without deciding what the evidence proves.

## 16. Minimal Transition information set

A minimal STATE Transition shall be capable of answering:

1. What was the authoritative input state?
2. What was intended to change?
3. What was authorized to change?
4. Which actors performed which logical roles?
5. What actually changed?
6. What claims were verified?
7. What evidence supports or challenges those claims?
8. What was the decision?
9. What state, if any, became the new authoritative baseline?

These answers may reside in several Work Products or one consolidated physical record.

## 17. Canonical rules

> **Logical Work Products define information obligations, not mandatory file counts.**

> **Evidence shall be bound to claims, states and decisions rather than accumulated without purpose.**

> **A verification result shall identify what was verified and the evidence on which the result depends.**

> **Evidence sufficiency is proportional to claim strength, consequence and residual uncertainty.**

> **An accepted candidate does not become a baseline until baseline establishment is explicit.**

> **A released artifact shall be traceable to the accepted state when release integrity is part of the claim.**

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.4  
Initial publication: 2026-08-13  
Last modified: 2026-08-13