# STATE v1.1 WP01 — Metadata Inventory

> **Document:** `STATE-V1.1-WP01-METADATA-INVENTORY-001A.md`
> **Title:** STATE v1.1 WP01 — Metadata Inventory
> **Version:** 001A
> **Status:** Current Documentation
> **Created:** 2026-08-13
> **Last modified:** 2026-08-13
> **Author:** Tor-Ståle Hansen
> **Co-authors:** None

## 1. Scope

This inventory records observable Markdown metadata before WP02 normalization. Missing or inconsistent fields are preserved as findings rather than silently corrected by WP01.

| Path | Header version | Status | Development state | Footer licence | Footer version | WP02 status valid | Header/footer equal |
|---|---|---|---|---|---|---|---|
| 00-foundation/BOOK-ARCHITECTURE-001A.md | 0.1 | Foundation Architecture |  | CC BY-NC-ND 4.0 | 0.1 | NO | YES |
| 00-foundation/README.md | 0.13 | Current Documentation |  | CC BY-NC-ND 4.0 | 0.13 | YES | YES |
| 00-foundation/STATE-ENGINEERING-METHOD-SPECIFICATION-001A.md | 0.1 | Historical Superseded Specification |  | CC BY-NC-ND 4.0 | 0.1 | YES | YES |
| 00-foundation/STATE-ENGINEERING-METHOD-SPECIFICATION-002A.md | 0.2 | Historical Superseded Specification |  | CC BY-NC-ND 4.0 | 0.2 | YES | YES |
| 00-foundation/STATE-ENGINEERING-METHOD-SPECIFICATION-003A.md | 0.3 | Historical Superseded Specification |  | CC BY-NC-ND 4.0 | 0.3 | YES | YES |
| 00-foundation/STATE-ENGINEERING-METHOD-SPECIFICATION-004A.md | 0.4 | Historical Superseded Specification |  | CC BY-NC-ND 4.0 | 0.4 | YES | YES |
| 00-foundation/STATE-ENGINEERING-METHOD-SPECIFICATION-005A.md | 0.5 | Historical Superseded Specification |  | CC BY-NC-ND 4.0 | 0.5 | YES | YES |
| 00-foundation/STATE-ENGINEERING-METHOD-SPECIFICATION-006A.md | 0.6 | Historical Superseded Specification |  | CC BY-NC-ND 4.0 | 0.6 | YES | YES |
| 00-foundation/STATE-ENGINEERING-METHOD-SPECIFICATION-007A.md | 0.7 | Historical Superseded Specification |  | CC BY-NC-ND 4.0 | 0.7 | YES | YES |
| 00-foundation/STATE-ENGINEERING-METHOD-SPECIFICATION-008A.md | 0.8 | Historical Superseded Specification |  | CC BY-NC-ND 4.0 | 0.8 | YES | YES |
| 00-foundation/STATE-ENGINEERING-METHOD-SPECIFICATION-009A.md | 0.9 | Historical Superseded Specification |  | CC BY-NC-ND 4.0 | 0.9 | YES | YES |
| 00-foundation/STATE-ENGINEERING-METHOD-SPECIFICATION-010A.md | 0.10 | Historical Superseded Specification |  | CC BY-NC-ND 4.0 | 0.10 | YES | YES |
| 00-foundation/STATE-ENGINEERING-METHOD-SPECIFICATION-011A.md | 0.11 | Historical Superseded Specification |  | CC BY-NC-ND 4.0 | 0.11 | YES | YES |
| 00-foundation/STATE-ENGINEERING-METHOD-SPECIFICATION-012A.md | 0.12 | Historical Superseded Specification |  | CC BY-NC-ND 4.0 | 0.12 | YES | YES |
| 00-foundation/STATE-ENGINEERING-METHOD-SPECIFICATION-013A.md | 0.13 | Current Foundational Specification |  | CC BY-NC-ND 4.0 | 0.13 | NO | YES |
| 01-why-contextual/01-the-control-problem.md | 0.1 | Current Documentation |  | CC BY-NC-ND 4.0 | 0.1 | YES | YES |
| 01-why-contextual/README.md | 0.1 | Current Documentation |  | CC BY-NC-ND 4.0 | 0.1 | YES | YES |
| 02-what-conceptual/01-the-state-model.md | 0.1 | Current Documentation |  | CC BY-NC-ND 4.0 | 0.1 | YES | YES |
| 02-what-conceptual/02-foundational-properties.md | 0.2 | Normative Specification |  | CC BY-NC-ND 4.0 | 0.2 | YES | YES |
| 02-what-conceptual/03-role-actor-capability-authority.md | 0.3 | Normative Specification |  | CC BY-NC-ND 4.0 | 0.3 | YES | YES |
| 02-what-conceptual/04-secure-engineering-foundation.md | 0.2 | Normative Specification |  | CC BY-NC-ND 4.0 | 0.2 | YES | YES |
| 02-what-conceptual/05-universal-engineering-principles.md | 0.3 | Normative Specification |  | CC BY-NC-ND 4.0 | 0.3 | YES | YES |
| 02-what-conceptual/06-role-authority-responsibility-model.md | 0.3 | Normative Specification |  | CC BY-NC-ND 4.0 | 0.3 | YES | YES |
| 02-what-conceptual/07-work-product-and-evidence-model.md | 0.4 | Normative Specification |  | CC BY-NC-ND 4.0 | 0.4 | YES | YES |
| 02-what-conceptual/README.md | 0.4 | Current Documentation |  | CC BY-NC-ND 4.0 | 0.4 | YES | YES |
| 03-how-logical/01-the-state-cycle.md | 0.8 | Normative Specification |  | CC BY-NC-ND 4.0 | 0.8 | YES | YES |
| 03-how-logical/02-transition-gates.md | 0.5 | Normative Specification |  | CC BY-NC-ND 4.0 | 0.5 | YES | YES |
| 03-how-logical/03-failure-repair-and-resumption.md | 0.5 | Normative Specification |  | CC BY-NC-ND 4.0 | 0.5 | YES | YES |
| 03-how-logical/04-transition-contract.md | 0.6 | Normative Specification |  | CC BY-NC-ND 4.0 | 0.6 | YES | YES |
| 03-how-logical/05-work-package-model.md | 0.6 | Normative Specification |  | CC BY-NC-ND 4.0 | 0.6 | YES | YES |
| 03-how-logical/06-verification-model.md | 0.7 | Normative Specification |  | CC BY-NC-ND 4.0 | 0.7 | YES | YES |
| 03-how-logical/07-acceptance-model.md | 0.7 | Normative Specification |  | CC BY-NC-ND 4.0 | 0.7 | YES | YES |
| 03-how-logical/08-baseline-establishment-model.md | 0.8 | Normative Specification |  | CC BY-NC-ND 4.0 | 0.8 | YES | YES |
| 03-how-logical/09-release-and-provenance-model.md | 0.8 | Normative Specification |  | CC BY-NC-ND 4.0 | 0.8 | YES | YES |
| 03-how-logical/README.md | 0.8 | Current Documentation |  | CC BY-NC-ND 4.0 | 0.8 | YES | YES |
| 04-with-what-physical/01-physical-realization-model.md | 0.9 | Normative Specification |  | CC BY-NC-ND 4.0 | 0.9 | YES | YES |
| 04-with-what-physical/02-actor-realization-patterns.md | 0.9 | Normative Specification |  | CC BY-NC-ND 4.0 | 0.9 | YES | YES |
| 04-with-what-physical/03-execution-environment-and-toolchain-model.md | 0.9 | Normative Specification |  | CC BY-NC-ND 4.0 | 0.9 | YES | YES |
| 04-with-what-physical/README.md | 0.9 | Current Documentation |  | CC BY-NC-ND 4.0 | 0.9 | YES | YES |
| 05-tailoring/01-tailoring-model.md | 0.10 | Normative Specification |  | CC BY-NC-ND 4.0 | 0.10 | YES | YES |
| 05-tailoring/02-tailoring-decision-model.md | 0.10 | Normative Specification |  | CC BY-NC-ND 4.0 | 0.10 | YES | YES |
| 05-tailoring/03-scaling-profiles.md | 0.10 | Reference |  | CC BY-NC-ND 4.0 | 0.10 | YES | YES |
| 05-tailoring/README.md | 0.12 | Current Documentation |  | CC BY-NC-ND 4.0 | 0.12 | YES | YES |
| 06-assurance/01-assurance-model.md | 0.11 | Normative Specification |  | CC BY-NC-ND 4.0 | 0.11 | YES | YES |
| 06-assurance/02-assurance-case-and-confidence.md | 0.11 | Normative Specification |  | CC BY-NC-ND 4.0 | 0.11 | YES | YES |
| 06-assurance/03-independence-and-assurance-depth.md | 0.11 | Normative Specification |  | CC BY-NC-ND 4.0 | 0.11 | YES | YES |
| 06-assurance/README.md | 0.12 | Current Documentation |  | CC BY-NC-ND 4.0 | 0.12 | YES | YES |
| 07-reference/ASSURANCE-REFERENCE.md | 0.11 | Reference |  | CC BY-NC-ND 4.0 | 0.11 | YES | YES |
| 07-reference/BASELINE-RELEASE-PROVENANCE-REFERENCE.md | 0.8 | Reference |  | CC BY-NC-ND 4.0 | 0.8 | YES | YES |
| 07-reference/CONFORMANCE-MODEL.md | 0.12 | Normative Specification |  | CC BY-NC-ND 4.0 | 0.12 | YES | YES |
| 07-reference/CONFORMANCE-REFERENCE.md | 0.12 | Reference |  | CC BY-NC-ND 4.0 | 0.12 | YES | YES |
| 07-reference/DOCUMENT-METADATA-TEMPLATE.md | 0.1 | Reference |  | CC BY-NC-ND 4.0 | 0.1 | YES | YES |
| 07-reference/EVIDENCE-CATALOGUE.md | 0.4 | Reference |  | CC BY-NC-ND 4.0 | 0.4 | YES | YES |
| 07-reference/GLOSSARY.md | 0.13 | Reference |  | CC BY-NC-ND 4.0 | 0.13 | YES | YES |
| 07-reference/METHOD-TRACEABILITY-MODEL.md | 0.13 | Normative Specification |  | CC BY-NC-ND 4.0 | 0.13 | YES | YES |
| 07-reference/METHODOLOGICAL-SOURCE-REGISTER.md | 0.2 | Reference |  | CC BY-NC-ND 4.0 | 0.2 | YES | YES |
| 07-reference/NORMATIVE-ELEMENT-REGISTER.md | 0.13 | Reference |  | CC BY-NC-ND 4.0 | 0.13 | YES | YES |
| 07-reference/NORMATIVE-LANGUAGE.md | 0.13 | Normative Specification |  | CC BY-NC-ND 4.0 | 0.13 | YES | YES |
| 07-reference/PHYSICAL-REALIZATION-REFERENCE.md | 0.9 | Reference |  | CC BY-NC-ND 4.0 | 0.9 | YES | YES |
| 07-reference/README.md | 0.13 | Current Documentation |  | CC BY-NC-ND 4.0 | 0.13 | YES | YES |
| 07-reference/ROLE-AUTHORITY-CATALOGUE.md | 0.13 | Reference |  | CC BY-NC-ND 4.0 | 0.13 | YES | YES |
| 07-reference/STATE-CONFORMANCE-CHECKLIST.md | 0.12 | Reference |  | CC BY-NC-ND 4.0 | 0.12 | YES | YES |
| 07-reference/STATE-CYCLE-REFERENCE.md | 0.5 | Reference |  | CC BY-NC-ND 4.0 | 0.5 | YES | YES |
| 07-reference/TAILORING-REFERENCE.md | 0.10 | Reference |  | CC BY-NC-ND 4.0 | 0.10 | YES | YES |
| 07-reference/TRANSITION-CONTRACT-REFERENCE.md | 0.6 | Reference |  | CC BY-NC-ND 4.0 | 0.6 | YES | YES |
| 07-reference/VERIFICATION-ACCEPTANCE-REFERENCE.md | 0.7 | Reference |  | CC BY-NC-ND 4.0 | 0.7 | YES | YES |
| 07-reference/WORK-PRODUCT-CATALOGUE.md | 0.4 | Reference |  | CC BY-NC-ND 4.0 | 0.4 | YES | YES |
| 08-examples/README.md | 001A | Current Documentation |  | CC BY-NC-ND 4.0 | 001A | YES | YES |
| 09-releases/README.md | 001A | Current Documentation |  | CC BY-NC-ND 4.0 | 001A | YES | YES |
| 10-development/README.md | 1.0.0 | Current Documentation |  | CC BY-NC-ND 4.0 | 1.0.0 | YES | YES |
| 10-development/STATE-EPIC-V1.0.0-001A.md | 1.0.0 | Reference |  | CC BY-NC-ND 4.0 | 1.0.0 | YES | YES |
| 10-development/STATE-EPIC-V1.1.0-001A.md | 001A | Current Documentation | Candidate | CC BY-NC-ND 4.0 | 001A | YES | YES |
| CHANGELOG.md | 0.13 | Active |  | CC BY-NC-ND 4.0 | 0.13 | NO | YES |
| README.md | 0.13 | Current Documentation |  | CC BY-NC-ND 4.0 | 0.13 | YES | YES |

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-SA 4.0  
Version: 001A  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
