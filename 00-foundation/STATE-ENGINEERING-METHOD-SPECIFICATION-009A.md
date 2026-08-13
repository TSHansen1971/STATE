# STATE Engineering Method Specification 009A

> **Document:** `00-foundation/STATE-ENGINEERING-METHOD-SPECIFICATION-009A.md`  
> **Title:** STATE Engineering Method Specification 009A  
> **Version:** 0.9  
> **Status:** Current Foundational Specification  
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


## 1. Purpose

STATE Engineering governs controlled transitions between Authoritative States.

This specification supersedes `STATE-ENGINEERING-METHOD-SPECIFICATION-008A.md` as the current foundational specification and establishes the Physical Realization, Actor and Execution Environment Model.

## 2. Canonical definition

> **STATE Engineering is a specification-driven, actor-independent, human-governed, traceable and evidence-based engineering method for controlling transitions between authoritative system states.**

## 3. Abstraction boundary

WHY defines context.

WHAT defines the conceptual method.

HOW defines logical operation.

WITH WHAT defines concrete realization through Actors, hardware, software, environments, tools and access mechanisms.

No physical realization is constitutive of STATE Engineering.

## 4. Physical Realization Binding

A Physical Realization Binding maps logical control to concrete execution through:

1. PR-01 Logical Role
2. PR-02 Actor Identity or Actor Class
3. PR-03 Capability Basis
4. PR-04 Authority Basis
5. PR-05 Execution Environment
6. PR-06 Tool Capability
7. PR-07 Access and Credential Basis
8. PR-08 Mutation Surface
9. PR-09 Evidence-Capture Mechanism
10. PR-10 Isolation Mechanism
11. PR-11 Communication / Handoff Mechanism
12. PR-12 Persistence and State
13. PR-13 External Dependency
14. PR-14 Assurance Control

The binding is a logical relationship and does not require a new Work Product class.

## 5. Effective Capability Envelope

The Effective Capability Envelope describes what the concrete Actor, tool, environment and access combination can actually do.

Conceptually:

```text
EffectiveCapabilityEnvelope
=
ActorCapability
∩ ToolCapability
∩ EnvironmentCapability
∩ AvailableAccess
```

## 6. Authorized Execution Envelope

The Authorized Execution Envelope is the subset of physical capability permitted for the Transition.

Conceptually:

```text
AuthorizedExecutionEnvelope
⊆ EffectiveCapabilityEnvelope
∩ TransitionBoundary
∩ AuthorityGrant
```

Physical capability never expands logical authority.

## 7. Access rule

Access is not Authority.

Credentials, administrative rights, repository permissions, filesystem access, API tokens or tool permissions do not by themselves create a legitimate right to mutate or decide.

## 8. Actor Realization Patterns

STATE recognizes common non-exclusive patterns:

1. APR-01 Individual Human Actor
2. APR-02 Co-located Human Team
3. APR-03 Distributed Human Team
4. APR-04 Specialist Supplier
5. APR-05 Deterministic Automation
6. APR-06 AI Model as Bounded Actor
7. APR-07 Autonomous or Agentic Actor
8. APR-08 Multi-Agent System
9. APR-09 Hybrid Human–Synthetic Arrangement

These patterns do not define separate methods.

## 9. AI and synthetic actors

AI is a Physical realization option.

Where relevant, synthetic Actor identity may include model, runtime/provider, context/instruction basis, tool permissions, persistence, external dependencies and configuration.

Apparent competence does not create Authority.

Autonomy is capability, not authority.

## 10. Distributed and supplier actors

Local, inshore, nearshore, offshore and supplier execution are physical delivery arrangements.

Geography, employment status and supplier status do not themselves define Authority or Assurance.

## 11. Actor substitution

Actor substitution shall be assessed where it can affect:

- capability;
- Authority;
- access;
- environment;
- tools;
- evidence;
- independence;
- provenance.

Logical Role remains stable.

## 12. Execution Environment

STATE defines sixteen environment fields:

1. EE-01 Environment Identity
2. EE-02 Hardware Substrate
3. EE-03 Operating System / Runtime
4. EE-04 Workspace Identity
5. EE-05 Toolchain Identity
6. EE-06 Dependency State
7. EE-07 Configuration State
8. EE-08 Access and Credentials
9. EE-09 Network and External Services
10. EE-10 Input and Data State
11. EE-11 Isolation Boundary
12. EE-12 Observability and Evidence Capture
13. EE-13 Persistence and Mutable State
14. EE-14 Temporal / Sequence Context
15. EE-15 Externalized State
16. EE-16 Recovery / Reset Mechanism

## 13. Environment identity

Environment identity is claim-relative.

STATE requires enough environment identity to support the claim, not exhaustive collection of irrelevant machine detail.

## 14. Environment Drift

Environment Drift is material only where changed conditions affect the claim, Candidate, verification, evidence, provenance or security boundary.

Material drift requires re-evaluation of affected evidence.

## 15. Tool Capability Classes

STATE recognizes eleven descriptive capability classes:

1. TCAP-01 Authoring and Modification
2. TCAP-02 Source and State Control
3. TCAP-03 Construction and Transformation
4. TCAP-04 Dependency and Configuration Management
5. TCAP-05 Test and Verification Execution
6. TCAP-06 Analysis
7. TCAP-07 Runtime and Execution
8. TCAP-08 Artifact and Release
9. TCAP-09 Evidence and Observability
10. TCAP-10 Coordination and Handoff
11. TCAP-11 Synthetic Reasoning / Generation

No specific product is mandatory.

## 16. Tool trust

A tool belongs to the trusted basis only to the degree that a claim depends on it.

A production tool verifying only its own output may require independent corroboration.

## 17. Local and remote execution

STATE is neutral between local and remote execution.

Location alone does not establish trust, security, compliance or independence.

## 18. Hardware and software substitution

Hardware, runtime, dependency, compiler, model or other tool substitution shall be assessed where it can affect Candidate identity, evidence comparability, verification meaning, provenance or Assurance.

## 19. Evidence by physical design

A selected Physical Realization shall support the evidence obligations of the logical Transition.

Technical ability to perform an activity is insufficient if required evidence cannot be produced or preserved.

## 20. Existing logical models preserved

The P0–P9 Cycle, Transition Contract, Work Package, Verification, Acceptance, Baseline Establishment, Release, Provenance and WP-01–WP-11 semantics remain logically unchanged.

## 21. Canonical Physical rules

> **The logical method defines the control obligation; the Physical layer selects the concrete means.**

> **Physical capability never expands logical authority.**

> **Access is not authority.**

> **Actor independence does not mean actor equivalence.**

> **Autonomy is capability, not authority.**

> **Environment identity is claim-relative.**

> **Actor, hardware, software, model, tool and environment substitution shall be assessed for their effect on Candidate identity, evidence and Assurance.**

> **No specific human sourcing model, AI system, hardware platform or software tool is constitutive of STATE Engineering.**

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.9  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
