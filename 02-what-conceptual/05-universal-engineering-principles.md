# Universal Engineering Principles

> **Document:** `02-what-conceptual/05-universal-engineering-principles.md`  
> **Title:** Universal Engineering Principles  
> **Version:** 0.3  
> **Status:** Normative Specification
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None

## UEP-01 — Clear and Controlled Abstraction

> **Systems and transitions should be structured through explicit, comprehensible abstractions, interfaces, layers and dependency relationships.**

Engineering should reduce unnecessary conceptual and structural complexity. A transition should make clear which abstraction boundaries it affects and which it is required to preserve.

## UEP-02 — Minimize Unnecessary Coupling, Sharing and Surface

> **A system and a transition should introduce no more shared mechanism, coupling, exposed surface or security-sensitive element than is necessary for the authorized purpose.**

Minimization reduces the number of interactions that must be trusted, understood, verified and maintained.

## UEP-03 — Least Authority

> **Every role, actor, component and execution context should receive only the authority necessary to perform its assigned function.**

Least Authority includes, but is broader than, runtime privilege. It applies to repository mutation, architecture decisions, transition authorization, deployment, evidence handling and acceptance authority as well as technical access.

Authority should be bounded through an explicit or explicitly inherited Authority Grant. Technical capability, access or organizational seniority does not enlarge that grant.


## UEP-04 — Explicit Mediation and Permission

> **Security-relevant access and privileged action should be governed through explicit, consistently mediated authorization conditions.**

Relevant permission should not depend on accidental reachability, undocumented convention or possession of a broad technical capability.

## UEP-05 — Structured Trust

> **Trust should be explicit, bounded, decomposable and justified at the level where it is required.**

STATE avoids treating an entire actor, team, subsystem or toolchain as uniformly trustworthy merely because one part of it is trusted.

Trust relationships, trusted components and communication paths should be identifiable when they matter to the accepted claim.

## UEP-06 — Secure Evolvability and Continuous Protection

> **A system should be structured so that authorized change can occur without unnecessarily destroying properties and assurances that are intended to survive the change.**

Engineering for a single secure snapshot is insufficient when the system is expected to evolve.

Transition design should identify which protections and invariants must remain effective before, during and after modification.

## UEP-07 — Secure Failure and Recoverability

> **Failure should be anticipated, observable and controlled, with recovery behavior defined where recovery is required.**

This principle applies both to the engineered product and to the engineering process.

A failed STATE transition must not silently replace the previous authoritative baseline.

## UEP-08 — Accountability, Traceability and Provenance

> **Relevant actions, transformations, identities, evidence and decisions should be attributable and reconstructable to the degree required by the accepted claim.**

This principle provides the engineering basis for baseline identity, Transition Records, evidence preservation, artifact identity and source-to-release provenance.

## UEP-09 — Verification by Design

> **Significant engineering claims should have an identified means of verification before acceptance.**

Verification is therefore designed as part of the transition rather than improvised only after implementation is complete.

The verification mechanism may be deterministic, probabilistic, analytical, observational, human, synthetic or hybrid, provided its limitations are explicit and its evidence is relevant to the claim.

## UEP-10 — Security-Relevant Change Requires Security-Relevant Verification

> **When a transition can affect a security-relevant property, verification scope shall include the affected security claim.**

A functional PASS does not automatically establish that privilege, trust, exposure, dependency, provenance or failure properties remained acceptable.

## UEP-11 — Actor-Appropriate Engineering Controls

> **The method shall account for the real operational characteristics and failure modes of the actor assigned to a role.**

Actor independence does not mean actor equivalence.

A local expert team, an inshore or offshore delivery team, deterministic automation and a generative system can perform the same logical role while requiring different controls, supervision, evidence, verification independence or authority boundaries.

Actor assignment shall therefore consider capability, authority, traceability and assurance obligations while preserving the logical definition of the role.


## UEP-12 — Proportional and Explicit Rigor

> **Engineering rigor should be proportionate to the claim, consequence, uncertainty, reversibility and cost of error, and the chosen level of rigor should be explicit.**

STATE does not require maximal process weight for every change.

It requires enough rigor to justify the state transition being accepted.

## Methodological absorption record

The following table records how the 33 engineering principles identified under NIST SP 800-53 SA-8 are absorbed into the STATE-native principle model.

This is a methodological provenance record, not a compliance crosswalk.

| SA-8 principle | STATE absorption |
|---|---|
| (1) Clear Abstractions | UEP-01 |
| (2) Least Common Mechanism | UEP-02 |
| (3) Modularity and Layering | UEP-01 |
| (4) Partially Ordered Dependencies | UEP-01 |
| (5) Efficiently Mediated Access | UEP-04 |
| (6) Minimized Sharing | UEP-02 |
| (7) Reduced Complexity | UEP-01 |
| (8) Secure Evolvability | UEP-06 |
| (9) Trusted Components | UEP-05 |
| (10) Hierarchical Trust | UEP-05 |
| (11) Inverse Modification Threshold | UEP-06, UEP-12 |
| (12) Hierarchical Protection | UEP-05 |
| (13) Minimized Security Elements | UEP-02 |
| (14) Least Privilege | UEP-03 |
| (15) Predicate Permission | UEP-04 |
| (16) Self-reliant Trustworthiness | UEP-05 |
| (17) Secure Distributed Composition | UEP-05 |
| (18) Trusted Communications Channels | UEP-04 |
| (19) Continuous Protection | UEP-06 |
| (20) Secure Metadata Management | UEP-08 |
| (21) Self-analysis | UEP-09 |
| (22) Accountability and Traceability | UEP-08 |
| (23) Secure Defaults | UEP-03, UEP-04 |
| (24) Secure Failure and Recovery | UEP-07 |
| (25) Economic Security | UEP-12 |
| (26) Performance Security | UEP-12 |
| (27) Human Factored Security | UEP-11 |
| (28) Acceptable Security | UEP-12 |
| (29) Repeatable and Documented Procedures | UEP-08 |
| (30) Procedural Rigor | UEP-12 |
| (31) Secure System Modification | FP-12, UEP-06 |
| (32) Sufficient Documentation | UEP-08 |
| (33) Minimization | UEP-02 |

## Broader secure-engineering source influence

OWASP secure-design and threat-oriented engineering material reinforces several STATE principles, particularly:

- security as a design property rather than a late retrofit;
- explicit trust boundaries and system boundaries;
- least privilege and secure defaults;
- architecture-level consideration of resilience and failure;
- threat-oriented analysis where risk warrants it;
- iterative security review when significant design change occurs;
- evidence and verification of implemented security properties.

Public NATO digital-engineering material provides additional methodological support for:

- continuous verification;
- least privilege;
- secure handling;
- resilient engineering;
- lifecycle coherence;
- traceability and integration of requirements and engineering artifacts.

STATE absorbs only generally applicable engineering principles from these sources. Context-bound mission, organization or legal requirements remain outside the universal core unless introduced through Tailoring.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-SA 4.0  
Version: 0.3  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
