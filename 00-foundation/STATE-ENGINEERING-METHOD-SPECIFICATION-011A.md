# STATE Engineering Method Specification 011A

> **Document:** `00-foundation/STATE-ENGINEERING-METHOD-SPECIFICATION-011A.md`  
> **Title:** STATE Engineering Method Specification 011A  
> **Version:** 0.11  
> **Status:** Historical Superseded Specification
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


## 1. Purpose

STATE Engineering governs controlled transitions between Authoritative States.

This specification supersedes `STATE-ENGINEERING-METHOD-SPECIFICATION-010A.md` as the current foundational specification and establishes the Assurance Model, Assurance Case, independence and Assurance Depth.

## 2. Canonical definition

> **STATE Engineering is a specification-driven, actor-independent, human-governed, traceable and evidence-based engineering method for controlling transitions between authoritative system states.**

## 3. Assurance definition

Assurance is the structured evaluation of whether the control, verification, evidence, independence and uncertainty basis supporting a defined engineering claim or decision is sufficient for the applicable consequence and Assurance Objective.

Assurance does not create Authority.

Assurance does not rewrite Verification Results.

Assurance does not itself decide Acceptance.

## 4. Assurance Objectives

STATE defines twelve Assurance Objectives:

1. AO-01 Authority Validity
2. AO-02 State Identity Integrity
3. AO-03 Specification Adequacy
4. AO-04 Boundary Adequacy
5. AO-05 Physical Realization Fitness
6. AO-06 Verification Adequacy
7. AO-07 Evidence Adequacy
8. AO-08 Independence Adequacy
9. AO-09 Tailoring Adequacy
10. AO-10 Failure and Recovery Adequacy
11. AO-11 Decision Adequacy
12. AO-12 Provenance Adequacy

## 5. Assurance Conclusions

Canonical Assurance Conclusions are exactly:

- SUFFICIENT;
- INSUFFICIENT;
- INCONCLUSIVE.

These are distinct from Verification PASS / FAIL / INCONCLUSIVE and Acceptance ACCEPT / REJECT / REPAIR REQUIRED / INCONCLUSIVE.

## 6. Assurance sufficiency properties

STATE defines:

1. ASP-01 Scope Clarity
2. ASP-02 Identity Coherence
3. ASP-03 Evidence Relevance
4. ASP-04 Evidence Integrity and Provenance
5. ASP-05 Method Adequacy
6. ASP-06 Independence Adequacy
7. ASP-07 Limitation Visibility
8. ASP-08 Residual Uncertainty Visibility
9. ASP-09 Tailoring Validity
10. ASP-10 Decision Coherence

## 7. Assurance Case

An Assurance Case is the reconstructable structured argument connecting an Assurance Objective to the basis for confidence.

It is not a new Work Product class.

Where explicit representation is required, the Assurance Case shall be capable of representing:

1. ACASE-01 Case Identity
2. ACASE-02 Assurance Objective
3. ACASE-03 Scope
4. ACASE-04 Required Assurance Depth
5. ACASE-05 Primary Claim or Decision
6. ACASE-06 Supporting Control Basis
7. ACASE-07 Verification Basis
8. ACASE-08 Evidence Basis
9. ACASE-09 Independence / Challenge
10. ACASE-10 Known Weaknesses
11. ACASE-11 Negative Evidence
12. ACASE-12 Residual Uncertainty
13. ACASE-13 Assumptions
14. ACASE-14 Conclusion
15. ACASE-15 Conclusion Rationale
16. ACASE-16 Assurer Identity

## 8. Confidence

Confidence is claim- and scope-relative.

STATE does not require a universal numerical confidence score.

Confidence is not automatically transitive from component to system.

## 9. Assurance Challenge

Assurance Challenge targets plausible common-cause and decision-relevant failure.

Challenge may use alternate Actors, methods, tools, environments, data, adversarial reasoning or other mechanisms appropriate to the claim.

## 10. Existing Verification Independence Dimensions

The six VI dimensions remain unchanged and are composed by Assurance rather than replaced.

## 11. Assurance Independence Patterns

STATE defines:

1. AIP-01 Independent Actor Challenge
2. AIP-02 Independent Method Challenge
3. AIP-03 Independent Tool Challenge
4. AIP-04 Independent Environment Challenge
5. AIP-05 Independent Data / Oracle Challenge
6. AIP-06 Organizational Challenge
7. AIP-07 Decision Separation
8. AIP-08 Adversarial Challenge

## 12. Assurance Depth

Assurance Depth is proportional and contextual.

STATE does not define a universal maturity level or mandatory numeric Assurance Level.

## 13. Assurance Depth Dimensions

STATE defines:

1. ADD-01 Claim Precision Depth
2. ADD-02 Verification Depth
3. ADD-03 Evidence Depth
4. ADD-04 Independence Depth
5. ADD-05 Environment Control Depth
6. ADD-06 Reproducibility Depth
7. ADD-07 Security Challenge Depth
8. ADD-08 Provenance Depth
9. ADD-09 Failure / Recovery Depth
10. ADD-10 Decision Review Depth

## 14. Selective strengthening

Assurance may be strengthened for individual claims or decisions without applying the same depth to every activity in the Transition.

## 15. Assurance Debt

Assurance Debt is a known unresolved weakness in the trust basis.

It shall remain visible.

It shall not relabel a failed Required Claim as acceptable.

## 16. Negative evidence

Decision-relevant negative evidence shall be considered by Assurance.

Confidence shall not be manufactured by selecting only supporting evidence.

## 17. Assurance and Tailoring

Tailoring selects control depth.

Assurance evaluates whether that selected depth remains sufficient.

Tailoring and Assurance are therefore related but distinct.

## 18. Assurance and ceremony

Document count, test count, reviewer count and approval count are not direct measures of Assurance.

Additional process increases Assurance only where it strengthens the relevant trust basis.

## 19. Existing method preserved

WHY, WHAT, HOW, WITH WHAT and Tailoring remain unchanged in their core semantics.

The P0–P9 Cycle, Work Products, Transition Contract, Work Packages, Verification, Acceptance, Baseline Establishment, Release, Provenance and Physical Realization remain preserved.

## 20. Conformance boundary

This revision does not define STATE Conformance, certification or external assessment.

Conformance is a separate subsequent method concern.

## 21. Canonical Assurance rules

> **Assurance evaluates whether a basis deserves trust; it does not create truth or Authority.**

> **A Verification Result and an Assurance Conclusion are different objects and shall not be substituted for one another.**

> **A SUFFICIENT Assurance Conclusion is bounded by objective, scope, evidence and assumptions.**

> **Assurance shall consider relevant negative evidence and residual uncertainty.**

> **Assurance cannot repair weak evidence by declaration.**

> **Useful independence is independence from the relevant failure source.**

> **Actor count is not a proxy for independence.**

> **Assurance Depth is proportional and claim-relative, not a maturity level.**

> **Independence Theater and evidence volume do not create Assurance.**

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.11  
Initial publication: 2026-08-13  
Last modified: 2026-08-13