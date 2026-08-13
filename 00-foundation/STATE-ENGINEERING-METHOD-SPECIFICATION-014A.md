# STATE Engineering Method Specification 014A

> **Document:** `00-foundation/STATE-ENGINEERING-METHOD-SPECIFICATION-014A.md`  
> **Title:** STATE Engineering Method Specification 014A  
> **Version:** 014A  
> **Status:** Normative Specification  
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None

## 1. Purpose

STATE Engineering governs controlled transitions between Authoritative States.

This specification supersedes `STATE-ENGINEERING-METHOD-SPECIFICATION-013A.md` as the current integrated specification in the active STATE development corpus.

Revision 014A consolidates the explicitly authorized post-v1.0 normative change accepted through WP06 while preserving the foundational architecture established by the v1.0.0 corpus.

It does not add:

- a lifecycle phase;
- a Transition Gate;
- an Authority Domain;
- a logical Role;
- a Work Product class;
- a Conformance Requirement;
- an external certification model.

## 2. Canonical definition

> **STATE Engineering is a specification-driven, actor-independent, human-governed, traceable and evidence-based engineering method for controlling transitions between authoritative system states.**

### 2.1 Canonical STATE name decomposition

The canonical decomposition of the name **STATE** is:

- **S — Specification**
- **T — Transition**
- **A — Authority**
- **T — Traceability**
- **E — Evidence**

The decomposition defines the method name and identifies five central control concerns already present in the normative corpus.

It does not establish a strict causal dependency chain among those five terms, does not create five new lifecycle phases, and does not add a new normative identifier family.

The existing method architecture, STATE Cycle, Authority Domains, Roles, Work Products, Evidence model and Conformance model remain unchanged.

This canonicalization is a naming integration authorized by owner decision D4. It does not alter the Section 16 statement that WP06 Sufficiency Governance is the only method-semantic control change consolidated since Specification 013A.


## 3. Normative Precedence

The current integrated specification is the highest integrated normative statement.

Current normative model documents provide detailed semantics within their scope.

Normative reference models and catalogues provide stable lookup and assessment semantics.

Compact references, checklists and README files summarize rather than override.

Historical specifications preserve provenance and do not override the current method.

## 4. Normative language

STATE distinguishes mandatory obligation, mandatory prohibition, recommendation, discouraged practice, permission, capability, definitional semantics and conditional applicability.

Permission and capability do not create Authority.

## 5. Stable identifiers

Published identifiers retain semantic identity.

They shall not be silently renumbered or reused for unrelated semantics.

Superseded identifiers remain historically reserved.

## 6. Normative Element Register

The current method maintains a registry of stable identifier namespaces covering all established model families.

The register is descriptive of the current method structure and does not create a maturity metric.

## 7. Consolidated glossary

The Reference layer maintains one consolidated current glossary.

Earlier incremental definitions are preserved through Git and historical specifications, while the current glossary provides one lookup surface.

The glossary does not override a more specific current normative definition.

## 8. Method Traceability

STATE method traceability connects:

```text
Foundational Property
        ↓
normative control model
        ↓
operational method element
        ↓
evidence / decision structure
        ↓
Assurance
        ↓
Conformance Requirement
```

The mapping is internal to STATE.

It is not an external compliance crosswalk.

## 9. Foundational Property traceability

Each FP-01 through FP-12 has explicit principal relationships to current conceptual or logical controls and to one or more CON requirements.

Conformance Requirements assess method semantics.

They do not create those semantics.

## 10. Role and Authority reference

AD-01 through AD-05 and LR-01 through LR-06 remain independent model families.

No logical Role inherently grants an Authority Domain.

Authority is established separately through an Authority Grant or explicit inherited authority source.

## 11. Existing method preserved

The following remain unchanged in core semantics:

- WHY, WHAT, HOW and WITH WHAT;
- P0-P9 and G0-G9;
- WP-01 through WP-11;
- Transition Contract;
- Work Package model;
- Verification;
- Acceptance;
- Baseline Establishment;
- Release and Provenance;
- Physical Realization;
- Tailoring;
- Assurance;
- Conformance.

## 12. Reference stabilization rules

> **Current normative detail shall have an identifiable governing source.**

> **Historical specifications provide provenance, not current precedence.**

> **Published identifiers shall retain their semantic identity.**

> **The consolidated glossary is a lookup surface, not an override mechanism.**

> **Internal method traceability shall connect Foundational Properties to the controls and Conformance Requirements that realize and assess them.**

> **Roles, Actors, Capability and Authority remain distinct in the Reference layer exactly as in the normative method.**

> **Reference consolidation shall not silently introduce new lifecycle or governance semantics.**


## 13. Authoritative version identity

The identity classes for this Candidate development state are:

| Identity class | Value |
|---|---|
| Current integrated specification in the active development corpus | `STATE-ENGINEERING-METHOD-SPECIFICATION-014A` |
| Stable specification identifier | `014A` |
| Document-local Version metadata | `014A` |
| Active development target | `v1.1.0` |
| Development state | Candidate |
| Current accepted public release | `v1.0.0` |
| Integrated specification bound to accepted `v1.0.0` | `STATE-ENGINEERING-METHOD-SPECIFICATION-013A` |

Specification 014A does not itself establish or promote release `v1.1.0`.

Release identity remains subject to explicit authorized release action.

## 14. Predecessor and supersession relation

The direct predecessor of 014A is:

`STATE-ENGINEERING-METHOD-SPECIFICATION-013A`

014A supersedes 013A as the current integrated specification in the active development corpus.

This supersession does not rewrite the accepted `v1.0.0` release. The immutable `v1.0.0` release remains bound to its released commit and to Specification 013A.

013A therefore remains the historical integrated specification of `v1.0.0` while 014A becomes the current integrated Candidate specification for continuing v1.1 development.

## 15. Revision rules

Integrated specification revision shall preserve the following rules:

1. a new current integrated specification receives a new unused stable specification identifier;
2. a superseded specification identifier remains historically reserved;
3. release version, stable specification identifier and document-local Version metadata remain distinct identity classes;
4. a Candidate specification does not become an accepted release through technical existence or repository publication alone;
5. accepted normative change shall be traceable to authorized method-development work;
6. a consolidation revision shall not silently introduce semantics outside its authorized change set;
7. historical release tags shall not be moved to follow a later specification.

## 16. Accepted normative change since Specification 013A

The only method-semantic change consolidated by Revision 014A is the WP06 Sufficiency Governance rule.

The rule establishes that:

1. every sufficiency threshold belongs to the Acceptance basis or gate condition in which it is used;
2. establishment or change of the threshold requires the Authority already responsible for the governing basis or condition;
3. a threshold shall be knowable to the degree required before it is relied upon to justify PASS;
4. weakening an established threshold changes the governing Acceptance basis or gate condition and therefore requires explicit authorized change;
5. weak, incomplete or inconvenient Evidence does not authorize a Realization Actor or evaluating mechanism to redefine what counts as sufficient;
6. where the applicable threshold cannot be established or evaluated under existing Authority, PASS shall not be manufactured.

Sufficiency is therefore governed through existing STATE Acceptance, Gate, Contract-amendment and Authority semantics.

No separate Sufficiency Authority exists.

## 17. Explicit not-added confirmation

Revision 014A does not introduce:

- a new lifecycle phase;
- a new STATE Cycle phase;
- a new Transition Gate;
- a new Foundational Property;
- a new Authority Domain;
- a new logical Role;
- a new Work Product class;
- a new Conformance Requirement;
- a new actor class with exceptional Authority semantics;
- a new release state;
- a new public corpus-version sequence.

## 18. Unchanged architectural invariants

The following architectural invariants remain unchanged:

1. **Capability does not create Authority.**
2. **Candidate-before-Authority.**
3. **Discovery does not expand scope.**
4. **Verification outcomes remain PASS, FAIL or INCONCLUSIVE; FAIL or INCONCLUSIVE shall not be silently converted to PASS.**
5. **Repair resumes from the earliest invalidated phase.**
6. **Control semantics remain actor-independent when Actor substitution preserves required capability and valid Authority.**

The four abstraction levels WHY / WHAT / HOW / WITH WHAT and the cross-cutting Tailoring, Assurance and Reference domains remain unchanged.
---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-SA 4.0  
Version: 014A  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
