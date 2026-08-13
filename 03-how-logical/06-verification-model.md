# Verification Model

> **Document:** `03-how-logical/06-verification-model.md`  
> **Title:** Verification Model  
> **Version:** 0.7  
> **Status:** Normative Specification
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


The Verification Model defines how STATE evaluates explicit engineering claims about an identified Candidate State.

STATE uses **verification** as the umbrella term for explicit claim evaluation.

Some claims concern conformance to specification. Others concern fitness for governing intent or intended outcome. The model does not require a separate lifecycle phase merely to distinguish those semantic categories.

## 1. Verification Claim

A **Verification Claim** is a bounded proposition about a specified target under specified conditions.

A useful claim answers:

- what is asserted;
- about which target;
- under which conditions;
- at what scope;
- with what threshold or expected property where applicable.

Example:

```text
Weak:
"The application works."

Bounded:
"Candidate C17 opens the defined reference document set without crash
under environment E4 and preserves the specified document-order invariant."
```

The second claim can be verified.

The first is too ambiguous to support strong Acceptance.

## 2. Claim identity

A Verification Claim shall be distinguishable from other claims to the degree required by the Transition.

A claim may have a stable identifier.

Claim identity supports:

- traceability;
- amendment;
- evidence binding;
- dependency;
- Acceptance Claim Set construction;
- repair and re-verification.

## 3. Canonical Claim Classes

STATE defines twelve canonical Claim Classes.

These are classification aids, not a requirement that every Transition contain twelve claims.

### CC-01 — Identity Claim

Asserts which state, source, artifact, component or release is under consideration.

Examples:

- Candidate identity;
- source revision identity;
- artifact digest identity.

### CC-02 — Transformation Claim

Asserts what changed or did not change between identified states.

Examples:

- only authorized files changed;
- configuration delta matches the Transition Boundary.

### CC-03 — Construction Claim

Asserts a property of building, compiling, assembling, packaging or generating the Candidate.

Examples:

- build succeeds;
- package contains required components.

### CC-04 — Behavioral Claim

Asserts observable functional behavior.

Examples:

- operation returns the specified result;
- user interaction completes without crash.

### CC-05 — Preservation and Invariant Claim

Asserts that a required pre-existing property remains true.

Examples:

- existing supported document types still open;
- unchanged API contract remains valid.

### CC-06 — Integration and Interaction Claim

Asserts behavior that depends on interaction among components, Work Packages or subsystems.

Package-local PASS cannot substitute for an integration claim.

### CC-07 — Security and Boundary Claim

Asserts a security-relevant property.

Examples:

- privilege did not expand;
- trust boundary remains intact;
- unauthorized path remains inaccessible.

### CC-08 — Environment and Compatibility Claim

Asserts behavior or identity relative to a defined environment, dependency state or compatibility condition.

### CC-09 — Performance and Resource Claim

Asserts measurable performance, latency, throughput, memory, capacity or other resource behavior.

### CC-10 — Provenance and Integrity Claim

Asserts origin, transformation lineage, integrity or source-to-artifact relationship.

### CC-11 — Recoverability and Failure-Behavior Claim

Asserts behavior under failure, interruption, restart, rollback or recovery conditions.

### CC-12 — Intent and Outcome Claim

Asserts that the resulting state satisfies the governing intended outcome rather than merely matching an implementation detail.

This class captures validation-type concerns without creating a separate mandatory STATE phase.

## 4. Claim level

Claims may exist at different scopes:

- Work Package;
- component;
- interface;
- integrated Candidate;
- system;
- release.

Claim scope shall be explicit where evidence from a narrower object could otherwise be mistaken for evidence about a broader one.

## 5. Claim dependency

A claim may depend on other claims.

For example:

```text
System Outcome Claim
   ├── Identity Claim
   ├── Behavioral Claim
   ├── Integration Claim
   └── Preservation Claim
```

Supporting claims do not automatically prove the parent claim.

The logical relationship by which they support the parent shall be valid.

## 6. No false aggregation

> **Several narrower PASS results shall not be presented as proof of a broader claim unless the composition relationship itself is justified.**

Examples:

```text
Component A PASS
Component B PASS
≠
Integrated system PASS
```

and:

```text
Build PASS
≠
Behavior PASS
≠
Security PASS
≠
Acceptance
```

## 7. Verification Method Classes

STATE defines eleven Verification Method Classes.

A Transition may use one or several.

### VM-01 — Inspection

Direct examination of state, source, configuration, metadata or artifact.

### VM-02 — Static Analysis

Evaluation without executing the target behavior.

Examples include structural analysis, dependency analysis and source analysis.

### VM-03 — Construction Verification

Build, compile, assemble, package or generation activity used to evaluate a construction claim.

### VM-04 — Test Execution

Execution of defined test cases against the Candidate or relevant component.

### VM-05 — Measurement

Quantitative observation using identified measurement conditions and units.

### VM-06 — Runtime Observation

Direct observation of behavior during actual or representative execution.

### VM-07 — Comparison and Differential Analysis

Comparison of Baseline, Candidate, expected output, alternate implementation or other reference state.

### VM-08 — Simulation or Emulation

Evaluation through a modeled, simulated or emulated environment.

### VM-09 — Analytical Reasoning or Proof

Structured reasoning, formal analysis, calculation or proof used where appropriate.

### VM-10 — Reproduction or Independent Re-execution

Independent repetition of construction, execution or observation to test reproducibility or independence.

### VM-11 — Review and Expert Judgment

Structured human, synthetic or hybrid evaluation where the claim requires interpretation or judgment.

Judgment shall not be disguised as deterministic proof.

## 8. Composite verification

Many important claims require multiple methods.

Example:

```text
Security Boundary Claim
   ├── VM-01 Inspection
   ├── VM-02 Static Analysis
   ├── VM-04 Test Execution
   └── VM-07 Differential Analysis
```

The method combination should be driven by the claim and Assurance need, not by a desire to maximize test count.

## 9. Verification Record structure

WP-06 Verification Record shall be capable of representing:

### VR-01 — Claim Identity

Which claim is being evaluated.

### VR-02 — Target Identity

Which Candidate, component, artifact or state is the verification target.

### VR-03 — Method

Which Verification Method Class or concrete method is used.

### VR-04 — Conditions

Relevant environment, configuration, data, preconditions or execution conditions.

### VR-05 — Observation

What was actually observed.

### VR-06 — Evidence References

Which Evidence Items support or challenge the observation or conclusion.

### VR-07 — Result

PASS, FAIL or INCONCLUSIVE.

### VR-08 — Limitations

What the verification does not establish.

### VR-09 — Verifier

The Verification Role and Actor Assignment responsible for the conclusion.

### VR-10 — Time or Sequence Identity

When or in which Candidate sequence the verification occurred, where relevant.

### VR-11 — Dependency

Other claims or results on which this result depends.

## 10. Result semantics

### PASS

PASS means:

> **The identified evidence is sufficient, under the specified method, target and conditions, to support the identified claim to the required Assurance level.**

PASS does not mean:

- all possible behavior is correct;
- unrelated claims are true;
- Acceptance is granted;
- the Candidate is authoritative.

### FAIL

FAIL means:

> **The available evidence contradicts the claim or demonstrates that the required property is not satisfied under the specified conditions.**

A later authority decision cannot retroactively convert the historical FAIL into PASS.

### INCONCLUSIVE

INCONCLUSIVE means:

> **The available verification basis is insufficient to establish PASS or FAIL to the required Assurance level.**

INCONCLUSIVE is not a weak PASS.

## 11. Status is not result

The following are execution or claim-management states, not verification results:

- NOT EXECUTED;
- NOT YET EVALUATED;
- NOT APPLICABLE;
- BLOCKED.

A required claim cannot be treated as PASS merely because it was not evaluated.

NOT APPLICABLE requires a legitimate scope basis and shall not be used to avoid a failed claim.

## 12. Partial satisfaction

STATE does not use ambiguous “partial PASS” as a canonical result.

Where a claim is only partly satisfied, either:

- the claim should be decomposed into independently meaningful claims; or
- the original claim should be FAIL or INCONCLUSIVE according to the evidence.

This prevents result labels from obscuring what was actually established.

## 13. Verification Adequacy Properties

STATE defines eleven Verification Adequacy Properties.

### VA-01 — Claim Precision

Is the claim bounded enough to be meaningfully evaluated?

### VA-02 — Target Identity

Is the verified object sufficiently identified?

### VA-03 — Method Fitness

Can the selected method actually bear on the claim?

### VA-04 — Condition Representativeness

Are verification conditions sufficiently relevant to the conditions assumed by the claim?

### VA-05 — Coverage

Does the verification address the relevant breadth, cases, boundaries or interaction surfaces?

### VA-06 — Evidence Quality

Are Evidence Items relevant, identifiable, integral and sufficiently traceable?

### VA-07 — Independence

Is verification sufficiently independent from Candidate production for the Assurance objective?

### VA-08 — Reproducibility

Can the relevant observation or result be repeated to the degree required?

### VA-09 — Limitation Visibility

Are material limitations explicit rather than hidden behind PASS?

### VA-10 — Integration Depth

Does the verification occur at the system or integration level where the claim depends on interaction?

### VA-11 — Security-Relevant Depth

Where the claim is security-relevant, does the verification address the affected security property rather than only functional behavior?

## 14. Verification independence

Independence is multidimensional.

STATE defines six useful Independence Dimensions.

### VI-01 — Actor Independence

Different Actor performs Verification from Realization.

### VI-02 — Method Independence

Different analytical or verification method challenges the same claim.

### VI-03 — Tool Independence

Verification does not rely exclusively on the same tool or mechanism that produced the Candidate or original result.

### VI-04 — Environment Independence

Verification is repeated or challenged under a distinct relevant environment where this provides meaningful Assurance.

### VI-05 — Organizational Independence

Verification is performed by an organizationally independent party where consequence requires it.

### VI-06 — Decision Independence

Acceptance Authority is sufficiently independent from production or verification roles for the required Assurance level.

Not every Transition requires every Independence Dimension.

Tailoring and Assurance select the required degree.

## 15. Verification and Work Packages

Work Package-local verification is useful but bounded.

A local PASS establishes only the local claim at the local target and conditions.

If Acceptance depends on interaction among Work Packages, P6 requires integrated verification of the corresponding integrated claim.

## 16. Verification after repair

A repaired Candidate is a new or revised verification target.

Previous PASS results may be reused only where:

- target identity remains applicable;
- the relevant behavior or dependency was unaffected;
- conditions remain applicable;
- the reuse is traceable;
- Assurance does not require re-execution.

The burden is to justify reuse, not to assume it.

## 17. Verification and Contract amendment

If the Transition Contract changes a claim or Acceptance basis after verification:

- the old Verification Record remains historically valid for the old claim;
- the new claim requires evaluation;
- evidence may be reused only where genuinely applicable.

> **Changing the claim does not change what old evidence proved.**

## 18. Canonical Verification rules

> **Verification evaluates explicit claims; it does not certify the Candidate in the abstract.**

> **PASS is bounded by claim, target, method, conditions and limitations.**

> **FAIL remains FAIL in the historical record even when an authorized later control decision changes the Acceptance basis.**

> **INCONCLUSIVE is not PASS.**

> **Several narrower PASS results do not prove a broader claim unless the composition relationship itself is justified.**

> **Package-level verification does not replace integrated verification where the accepted claim depends on interaction.**

> **Changing the claim does not change what old evidence proved.**

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.7  
Initial publication: 2026-08-13  
Last modified: 2026-08-13