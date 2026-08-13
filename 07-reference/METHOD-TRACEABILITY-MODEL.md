# Method Traceability Model

> **Document:** `07-reference/METHOD-TRACEABILITY-MODEL.md`  
> **Title:** Method Traceability Model  
> **Version:** 0.13  
> **Status:** Normative Specification
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None

STATE makes traceability a property of both engineering Transitions and the method itself.

## 1. Method Traceability definition

> **Method Traceability is the reconstructable internal relationship among Foundational Properties, normative control elements, operational method structures, Assurance and Conformance.**

This is internal method traceability.

It shall not be confused with an external compliance mapping.

## 2. Traceability chain

```text
Foundational Property
        ↓
Conceptual / logical control
        ↓
Operational record or decision structure
        ↓
Evidence and Assurance basis
        ↓
Conformance Requirement
```

The relationship is many-to-many.

## 3. Traceability relationship types

STATE uses the following ordinary-language relationship types:

- **defines** — establishes semantic meaning;
- **implements** — operationalizes a higher-level property;
- **constrains** — limits permitted realization or decision;
- **realizes** — binds a logical element to physical execution;
- **evidences** — provides observable support for a claim or control;
- **assures** — evaluates whether the basis deserves the required trust;
- **assesses** — evaluates an element against Conformance;
- **supersedes** — replaces a prior current semantic baseline while retaining history.

These relationships do not create a new external dependency model.

## 4. Foundational Property traceability

| Foundational Property | Principal STATE controls | Primary Conformance relationship |
|---|---|---|
| `FP-01` Controlled State Transition | P0-P9, G0-G9, Transition Contract, failure / repair model | `CON-05`, `CON-06`, `CON-11`, `CON-12` |
| `FP-02` Known Authoritative State | P0/G0, WP-04, TC-03, BE state identity | `CON-01` |
| `FP-03` Specification before Mutation | P1/G1, WP-01, TC-04 | `CON-02` |
| `FP-04` Explicit and Bounded Authority | AD-01..AD-05, WP-02, TC-05/TC-06 | `CON-03`, `CON-05` |
| `FP-05` Actor Independence | LR roles, Actor Assignment, PR/APR realization | `CON-04` |
| `FP-06` Separation of Role, Actor, Capability and Authority | LR model, Authority Grant, Effective / Authorized Execution Envelopes | `CON-04` |
| `FP-07` Candidate before Authority | P4, P8, P9, Candidate identity, Acceptance, Baseline Establishment | `CON-06`, `CON-11` |
| `FP-08` Traceability by Construction | WP model, Evidence model, PV provenance, Transition Record | `CON-08`, `CON-13` |
| `FP-09` Evidence-Based Acceptance | P6-P8, VR, EC/EQ, AR/AS, Assurance | `CON-07`, `CON-08`, `CON-09`, `CON-10`, `CON-16` |
| `FP-10` Secure Engineering by Construction | Secure Engineering Foundation, UEP set, CC-07, VA-11 | `CON-14` |
| `FP-11` Explicit Failure | F-01..F-12, Verification outcomes, Acceptance outcomes, P9 / Release failure results | `CON-12` |
| `FP-12` Secure Modification | UEP-06, UEP-10, security-relevant Verification and provenance | `CON-14`, `CON-15` |

## 5. Conformance is not the source of the method

Conformance Requirements assess preservation of the method.

They do not create the Foundational Properties they assess.

## 6. Traceability and Tailoring

Tailoring may change physical representation without breaking the traceability chain.

Semantic Compression is valid when the applicable relationships remain reconstructable.

Control Deletion breaks traceability when a required relationship disappears.

## 7. Traceability and Assurance

Assurance evaluates whether the traceability basis deserves trust.

Existence of a link is not sufficient Assurance by itself.

## 8. Traceability and historical evolution

Method evolution is traceable through:

- versioned integrated specifications;
- Git history;
- CHANGELOG entries;
- visible page metadata;
- stable identifiers;
- supersession relationships.

Historical documents are preserved without remaining current normative authority.

## 9. Canonical traceability rules

> **Internal traceability connects method properties to the controls that realize and assess them.**

> **Traceability does not mean every relationship requires a separate document.**

> **A reference link is not sufficient if the linked identity is ambiguous or incorrect.**

> **Conformance assesses method semantics; it does not create them.**

> **Method evolution shall preserve stable identifiers and supersession history.**

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-SA 4.0  
Version: 0.13  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
