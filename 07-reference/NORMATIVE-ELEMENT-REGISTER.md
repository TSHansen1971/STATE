# Normative Element Register

> **Document:** `07-reference/NORMATIVE-ELEMENT-REGISTER.md`  
> **Title:** Normative Element Register  
> **Version:** 0.13  
> **Status:** Reference  
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None

This register identifies the stable namespaces currently used by the STATE Engineering method.

It is a registry of existing method elements.

Revision 013A does not create new lifecycle, Authority, Role, Work Product or Conformance namespaces.

## Registered namespaces

| Namespace | Count | Family | Governing document |
|---|---:|---|---|
| `FP` | 12 | Foundational Properties | `02-what-conceptual/02-foundational-properties.md` |
| `UEP` | 12 | Universal Engineering Principles | `02-what-conceptual/05-universal-engineering-principles.md` |
| `AD` | 5 | Authority Domains | `02-what-conceptual/06-role-authority-responsibility-model.md` |
| `LR` | 6 | Logical Roles | `02-what-conceptual/06-role-authority-responsibility-model.md` |
| `WP` | 11 | Work Product classes | `02-what-conceptual/07-work-product-and-evidence-model.md` |
| `EC` | 10 | Evidence Classes | `02-what-conceptual/07-work-product-and-evidence-model.md` |
| `EQ` | 9 | Evidence-Quality Properties | `02-what-conceptual/07-work-product-and-evidence-model.md` |
| `P` | 10 | STATE Cycle phases P0-P9 | `03-how-logical/01-the-state-cycle.md` |
| `G` | 10 | Transition Gates G0-G9 | `03-how-logical/02-transition-gates.md` |
| `F` | 12 | Failure Classes | `03-how-logical/03-failure-repair-and-resumption.md` |
| `TC` | 16 | Transition Contract fields | `03-how-logical/04-transition-contract.md` |
| `CA` | 4 | Contract Amendment classes | `03-how-logical/04-transition-contract.md` |
| `WPK` | 12 | Work Package fields | `03-how-logical/05-work-package-model.md` |
| `CC` | 12 | Claim Classes | `03-how-logical/06-verification-model.md` |
| `VM` | 11 | Verification Method Classes | `03-how-logical/06-verification-model.md` |
| `VR` | 11 | Verification Record fields | `03-how-logical/06-verification-model.md` |
| `VA` | 11 | Verification Adequacy Properties | `03-how-logical/06-verification-model.md` |
| `VI` | 6 | Verification Independence Dimensions | `03-how-logical/06-verification-model.md` |
| `ACS` | 3 | Acceptance Claim Set classes | `03-how-logical/07-acceptance-model.md` |
| `AR` | 14 | Acceptance Record fields | `03-how-logical/07-acceptance-model.md` |
| `AS` | 10 | Acceptance Sufficiency Conditions | `03-how-logical/07-acceptance-model.md` |
| `BE` | 14 | Baseline Establishment Record fields | `03-how-logical/08-baseline-establishment-model.md` |
| `RL` | 14 | Release Record fields | `03-how-logical/09-release-and-provenance-model.md` |
| `PV` | 8 | Provenance Dimensions | `03-how-logical/09-release-and-provenance-model.md` |
| `PR` | 14 | Physical Realization dimensions | `04-with-what-physical/01-physical-realization-model.md` |
| `APR` | 9 | Actor Realization Patterns | `04-with-what-physical/02-actor-realization-patterns.md` |
| `EE` | 16 | Execution Environment fields | `04-with-what-physical/03-execution-environment-and-toolchain-model.md` |
| `TCAP` | 11 | Tool Capability Classes | `04-with-what-physical/03-execution-environment-and-toolchain-model.md` |
| `TI` | 12 | Tailoring Invariants | `05-tailoring/01-tailoring-model.md` |
| `TF` | 12 | Tailoring Factors | `05-tailoring/02-tailoring-decision-model.md` |
| `TLD` | 16 | Tailoring Decision fields | `05-tailoring/02-tailoring-decision-model.md` |
| `RT` | 12 | Re-tailoring triggers | `05-tailoring/02-tailoring-decision-model.md` |
| `TP` | 4 | Scaling Profiles | `05-tailoring/03-scaling-profiles.md` |
| `AO` | 12 | Assurance Objectives | `06-assurance/01-assurance-model.md` |
| `ASP` | 10 | Assurance Sufficiency Properties | `06-assurance/01-assurance-model.md` |
| `ACASE` | 16 | Assurance Case fields | `06-assurance/02-assurance-case-and-confidence.md` |
| `AIP` | 8 | Assurance Independence Patterns | `06-assurance/03-independence-and-assurance-depth.md` |
| `ADD` | 10 | Assurance Depth Dimensions | `06-assurance/03-independence-and-assurance-depth.md` |
| `CS` | 3 | Conformance scopes | `07-reference/CONFORMANCE-MODEL.md` |
| `CON` | 16 | Conformance Requirements | `07-reference/CONFORMANCE-MODEL.md` |
| `CAR` | 16 | Conformance Assessment Record fields | `07-reference/CONFORMANCE-MODEL.md` |

## Current registered population

The registered namespaces above contain **440 named canonical identifiers** across **41 namespaces**.

The number is descriptive of the current method baseline.

It is not a target, maturity measure or complexity goal.

## Namespace rules

A namespace:

- identifies one coherent family of method elements;
- has one governing model;
- shall not be reused for an unrelated family;
- may expand only through a controlled method revision;
- retains published identifiers for historical stability.

## Identity rule

An identifier is a semantic identity, not merely a row number.

For example, `CON-06` remains the Candidate non-authority requirement even if future reference presentation changes.

## Registry and current source

This register supports discovery and consistency checking.

The governing semantic definition remains in the listed current source document and the current integrated method specification.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.13  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
