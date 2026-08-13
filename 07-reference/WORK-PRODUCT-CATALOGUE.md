# STATE Work Product Catalogue

> **Document:** `07-reference/WORK-PRODUCT-CATALOGUE.md`  
> **Title:** STATE Work Product Catalogue  
> **Version:** 0.4  
> **Status:** Reference  
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


This catalogue is the compact reference view of canonical STATE Work Product classes.

It does not require one physical file per Work Product.

| ID | Work Product | Core purpose | Conditional? |
|---|---|---|---|
| WP-01 | Transition Intent and Specification | Define intended change, constraints, invariants and acceptance basis | No |
| WP-02 | Authority Grant | Establish bounded decision and mutation authority | No, but may be inherited/referenced |
| WP-03 | Actor Assignment | Bind actual actors to logical roles and authority | No |
| WP-04 | Baseline Record | Identify the Authoritative State used as transition input | No |
| WP-05 | Transition Record | Connect baseline, authorization, mutation, verification, evidence and decision | No |
| WP-06 | Verification Record | Record claim, method, observation, evidence, result and limitations | No |
| WP-07 | Evidence Set | Bind relevant Evidence Items to transition claims | No |
| WP-08 | Acceptance Record | Record ACCEPT / REJECT / REPAIR REQUIRED / INCONCLUSIVE decision | No |
| WP-09 | Baseline Establishment Record | Establish an accepted state as the next Authoritative State | Required only for ACCEPT |
| WP-10 | Release Record | Authorize and identify release when release is distinct from acceptance | Yes |
| WP-11 | Deviation and Escalation Record | Preserve material deviation, escalation or authority uncertainty | Yes |

## Representation rule

Several logical Work Products may share one physical representation when the required information remains distinguishable and traceable.

Conversely, one logical Work Product may be physically distributed across multiple controlled records when necessary.

## Minimum relationship

```text
WP-01 Specification
      │
WP-02 Authority ── WP-03 Actor Assignment
      │
WP-04 Baseline
      │
      ▼
WP-05 Transition Record
      │
      ├── WP-06 Verification
      │        │
      │        └── WP-07 Evidence Set
      │
      └── WP-08 Acceptance
                 │
          ┌──────┴──────┐
        ACCEPT        OTHER
          │
          ▼
WP-09 Baseline Establishment
          │
          └── WP-10 Release, when applicable
```

WP-11 may be attached at any point where material deviation, escalation or unresolved authority requires preservation.

## Tailoring rule

Tailoring may change:

- physical format;
- degree of separation;
- metadata depth;
- identity mechanism;
- evidence-retention depth;
- automation level.

Tailoring shall not remove the logical information required to justify the claims and authority of the Transition.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.4  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
