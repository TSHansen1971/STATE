# STATE Engineering Method Specification 007A

> **Document:** `00-foundation/STATE-ENGINEERING-METHOD-SPECIFICATION-007A.md`  
> **Title:** STATE Engineering Method Specification 007A  
> **Version:** 0.7  
> **Status:** Historical Superseded Specification
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


## 1. Purpose

STATE Engineering governs controlled transitions between Authoritative States.

This specification supersedes `STATE-ENGINEERING-METHOD-SPECIFICATION-006A.md` as the current foundational specification and establishes the Verification and Acceptance Model.

## 2. Canonical definition

> **STATE Engineering is a specification-driven, actor-independent, human-governed, traceable and evidence-based engineering method for controlling transitions between authoritative system states.**

## 3. Current normative model

The method currently defines:

- twelve Foundational Properties;
- twelve Universal Engineering Principles;
- five Authority Domains;
- six canonical logical Roles;
- eleven Work Product classes;
- ten Evidence Classes;
- nine Evidence-Quality Properties;
- ten STATE Cycle phases P0–P9;
- ten Transition Gates G0–G9;
- twelve logical failure classes;
- one governing Transition Contract per Transition;
- bounded Work Package decomposition;
- twelve canonical Claim Classes;
- eleven Verification Method Classes;
- eleven Verification Adequacy Properties;
- six Verification Independence Dimensions;
- four canonical G8 Acceptance outcomes;
- ten Acceptance Sufficiency Conditions.

## 4. Verification definition

Verification is the evaluation of an explicit claim about an identified target using an identified method, conditions, observations and evidence.

Verification does not certify a Candidate in the abstract.

## 5. Claim Classes

STATE defines:

1. CC-01 Identity Claim
2. CC-02 Transformation Claim
3. CC-03 Construction Claim
4. CC-04 Behavioral Claim
5. CC-05 Preservation and Invariant Claim
6. CC-06 Integration and Interaction Claim
7. CC-07 Security and Boundary Claim
8. CC-08 Environment and Compatibility Claim
9. CC-09 Performance and Resource Claim
10. CC-10 Provenance and Integrity Claim
11. CC-11 Recoverability and Failure-Behavior Claim
12. CC-12 Intent and Outcome Claim

Not every Transition requires every class.

## 6. Claim scope and composition

A claim shall be bounded to its relevant target and scope.

Several narrower PASS results shall not be presented as proof of a broader claim unless the composition relationship itself is justified.

Package-level PASS does not imply integrated Candidate PASS.

## 7. Verification Method Classes

STATE defines:

1. VM-01 Inspection
2. VM-02 Static Analysis
3. VM-03 Construction Verification
4. VM-04 Test Execution
5. VM-05 Measurement
6. VM-06 Runtime Observation
7. VM-07 Comparison and Differential Analysis
8. VM-08 Simulation or Emulation
9. VM-09 Analytical Reasoning or Proof
10. VM-10 Reproduction or Independent Re-execution
11. VM-11 Review and Expert Judgment

Method selection shall be driven by the claim and Assurance need.

## 8. Verification Record

WP-06 shall be capable of representing:

1. VR-01 Claim Identity
2. VR-02 Target Identity
3. VR-03 Method
4. VR-04 Conditions
5. VR-05 Observation
6. VR-06 Evidence References
7. VR-07 Result
8. VR-08 Limitations
9. VR-09 Verifier
10. VR-10 Time or Sequence Identity
11. VR-11 Dependency

## 9. Verification Results

Canonical Verification Results are:

- PASS;
- FAIL;
- INCONCLUSIVE.

NOT EXECUTED, NOT YET EVALUATED, NOT APPLICABLE and BLOCKED are not PASS/FAIL results.

STATE does not use ambiguous partial PASS as a canonical outcome.

## 10. PASS semantics

PASS means that the identified evidence sufficiently supports the identified claim for the identified target and conditions to the required Assurance level.

PASS is bounded.

It does not imply Acceptance.

## 11. FAIL semantics

FAIL means that evidence contradicts the claim or demonstrates that the required property is not satisfied under the specified conditions.

FAIL remains part of historical provenance even if later authority changes the Acceptance basis.

## 12. INCONCLUSIVE semantics

INCONCLUSIVE means the verification basis is insufficient to establish PASS or FAIL to the required Assurance level.

INCONCLUSIVE is not PASS.

## 13. Verification Adequacy

STATE defines:

1. VA-01 Claim Precision
2. VA-02 Target Identity
3. VA-03 Method Fitness
4. VA-04 Condition Representativeness
5. VA-05 Coverage
6. VA-06 Evidence Quality
7. VA-07 Independence
8. VA-08 Reproducibility
9. VA-09 Limitation Visibility
10. VA-10 Integration Depth
11. VA-11 Security-Relevant Depth

## 14. Verification Independence

STATE recognizes:

- VI-01 Actor Independence;
- VI-02 Method Independence;
- VI-03 Tool Independence;
- VI-04 Environment Independence;
- VI-05 Organizational Independence;
- VI-06 Decision Independence.

The required dimensions and depth are selected through Tailoring and Assurance.

## 15. Acceptance definition

Acceptance is the authorized P8 decision about whether an identified Candidate, under an explicit Acceptance Claim Set, scope, evidence basis and residual uncertainty, may progress to P9.

Acceptance is not verification.

## 16. Acceptance Claim Set

Claims may be:

- ACS-01 Required Claim;
- ACS-02 Supporting Claim;
- ACS-03 Informational Claim.

Changing a Required Claim after failure is a Contract amendment and authority event.

It is not a result relabeling operation.

## 17. Acceptance Record

WP-08 shall be capable of representing:

1. AR-01 Candidate Identity
2. AR-02 Transition Contract Identity
3. AR-03 Acceptance Scope
4. AR-04 Acceptance Claim Set
5. AR-05 Verification Basis
6. AR-06 Evidence Basis
7. AR-07 Deviations
8. AR-08 Residual Uncertainty
9. AR-09 Assurance Basis
10. AR-10 Acceptance Authority
11. AR-11 Decision
12. AR-12 Decision Rationale
13. AR-13 Effective Constraints
14. AR-14 Decision Identity

## 18. G8 outcomes

STATE preserves exactly four canonical G8 outcomes:

- ACCEPT;
- REJECT;
- REPAIR REQUIRED;
- INCONCLUSIVE.

STATE does not define a fifth conditional-acceptance outcome.

## 19. ACCEPT semantics

ACCEPT means that Acceptance Authority has determined that:

- the Candidate is sufficiently identified;
- the current Transition Contract is identified;
- Required Claims are sufficiently resolved;
- evidence is sufficient;
- material deviations are resolved;
- residual uncertainty is visible and acceptable within authority;
- Assurance conditions are satisfied;
- the Candidate may progress to P9.

ACCEPT does not itself establish the new Authoritative State.

## 20. Required Claim rule

A Required Claim that remains FAIL or INCONCLUSIVE prevents ACCEPT under the unchanged Acceptance basis.

If a Required Claim is legitimately changed or removed, the change shall be:

- authorized;
- explicit;
- traceable;
- reflected in the Transition Contract;
- followed by verification appropriate to the new claim.

Historical evidence is not rewritten.

## 21. Accepted deviations

An accepted deviation is not a retroactive PASS.

The deviation, applicable authority, Contract amendment and resulting claim basis shall remain traceable.

## 22. Acceptance Sufficiency Conditions

STATE defines:

1. AS-01 Candidate Identity
2. AS-02 Contract Identity
3. AS-03 Required Claim Resolution
4. AS-04 Evidence Sufficiency
5. AS-05 Deviation Resolution
6. AS-06 Residual Uncertainty Visibility
7. AS-07 Authority Validity
8. AS-08 Assurance Sufficiency
9. AS-09 State Coherence
10. AS-10 Baseline Establishment Readiness

## 23. Acceptance scope

Acceptance is claim-bound, Candidate-bound and scope-bound.

ACCEPT does not assert universal correctness.

## 24. Acceptance Authority

Acceptance Authority decides.

It does not rewrite Verification Results.

Capability does not create Acceptance Authority.

Delegated Acceptance remains traceable to a human-established governance source.

## 25. Work Package relationship

Work Package completion and local PASS do not imply Acceptance.

Integrated and system-level Required Claims remain subject to P6 verification and P8 Acceptance.

## 26. Acceptance and baseline establishment

ACCEPT permits progression to P9.

Only successful P9 / G9 establishes the new Authoritative State.

## 27. Canonical Verification rules

> **Verification evaluates explicit claims; it does not certify the Candidate in the abstract.**

> **PASS is bounded by claim, target, method, conditions and limitations.**

> **FAIL remains FAIL in the historical record even when a later authorized control decision changes the Acceptance basis.**

> **INCONCLUSIVE is not PASS.**

> **Several narrower PASS results do not prove a broader claim unless the composition relationship itself is justified.**

## 28. Canonical Acceptance rules

> **Acceptance is claim-bound, scope-bound and Candidate-bound.**

> **Acceptance Authority decides; it does not rewrite Verification Results.**

> **A Required Claim that remains FAIL or INCONCLUSIVE prevents ACCEPT under the unchanged Acceptance basis.**

> **An accepted deviation is not a retroactive PASS.**

> **STATE does not use a fifth conditional-acceptance outcome to hide unmet Acceptance conditions.**

> **ACCEPT permits progression to P9; it does not itself create the new Authoritative State.**

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.7  
Initial publication: 2026-08-13  
Last modified: 2026-08-13