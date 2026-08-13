# Role and Authority Catalogue

> **Document:** `07-reference/ROLE-AUTHORITY-CATALOGUE.md`  
> **Title:** Role and Authority Catalogue  
> **Version:** 0.13  
> **Status:** Reference  
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None

This catalogue provides a compact reference for the canonical logical Roles and Authority Domains defined by STATE.

It does not create new Roles or Authority Domains.

## Authority Domains

| ID | Domain | Core decision right |
|---|---|---|
| `AD-01` | Intent Authority | Establish or approve intended outcomes, priorities and intent-level trade-offs. |
| `AD-02` | Architecture Authority | Establish or approve structural rules, architectural boundaries and architectural invariants. |
| `AD-03` | Transition Authority | Establish or approve what may change within a particular Transition. |
| `AD-04` | Acceptance Authority | Decide whether an identified Candidate receives ACCEPT, REJECT, REPAIR REQUIRED or INCONCLUSIVE. |
| `AD-05` | Release Authority | Authorize distribution, deployment, publication or other Release of an established state or representation. |

## Logical Roles

| ID | Role | Core responsibility |
|---|---|---|
| `LR-01` | Specification Role | Transform approved intent and constraints into a sufficiently operational specification. |
| `LR-02` | Realization Role | Produce Candidate State within the authorized Transition Boundary. |
| `LR-03` | Verification Role | Evaluate explicit claims using appropriate Verification Methods. |
| `LR-04` | Evidence Stewardship Role | Preserve evidence identity, linkage, provenance and availability. |
| `LR-05` | Baseline Custodianship Role | Preserve authoritative-state identity and continuity. |
| `LR-06` | Assurance Role | Evaluate adequacy of control, verification, evidence, independence and confidence basis. |

## No inherent Role Authority

A logical Role does **not** automatically carry an Authority Domain.

```text
Role
  ≠
Authority

Actor Assignment
  ≠
Authority Grant

Capability
  ≠
Authority

Access
  ≠
Authority
```

Authority is established separately and then bound through an Authority Grant or explicit inherited authority source.

## Role combination

One physical Actor may realize several logical Roles where Tailoring and Assurance permit it.

The Role identities remain separate.

## Authority combination

One Actor may hold several Authority Domains.

Combination shall remain explicit and shall not defeat required Assurance.

In particular:

- Acceptance Authority is not implied by Realization capability;
- Release Authority is not implied by Acceptance Authority;
- Architecture Authority is not implied by repository access;
- Transition Authority is not implied by the ability to mutate the system.

## Delegation

Delegated authority remains traceable to a human-established governance source.

Synthetic Actors, automation and agents may exercise delegated authority where explicitly established.

Their technical autonomy does not make them independent normative sources of Authority.

## Canonical Role / Authority rules

> **Responsibilities belong to Roles before they belong to Actors.**

> **Roles do not create Authority.**

> **Capability does not create Authority.**

> **Access does not create Authority.**

> **Actor substitution shall not silently change Role or Authority semantics.**

> **Physical Role combination may be tailored; logical Role separation remains explicit.**

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-SA 4.0  
Version: 0.13  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
