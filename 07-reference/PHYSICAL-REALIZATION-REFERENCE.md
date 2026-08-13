# Physical Realization Reference

> **Document:** `07-reference/PHYSICAL-REALIZATION-REFERENCE.md`  
> **Title:** Physical Realization Reference  
> **Version:** 0.9  
> **Status:** Reference  
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


This page is the compact reference for the STATE Physical Realization Model.

## Physical Realization dimensions

| ID | Dimension |
|---|---|
| PR-01 | Logical Role |
| PR-02 | Actor Identity or Actor Class |
| PR-03 | Capability Basis |
| PR-04 | Authority Basis |
| PR-05 | Execution Environment |
| PR-06 | Tool Capability |
| PR-07 | Access and Credential Basis |
| PR-08 | Mutation Surface |
| PR-09 | Evidence-Capture Mechanism |
| PR-10 | Isolation Mechanism |
| PR-11 | Communication / Handoff Mechanism |
| PR-12 | Persistence and State |
| PR-13 | External Dependency |
| PR-14 | Assurance Control |

## Actor Realization Patterns

| ID | Pattern |
|---|---|
| APR-01 | Individual Human Actor |
| APR-02 | Co-located Human Team |
| APR-03 | Distributed Human Team |
| APR-04 | Specialist Supplier |
| APR-05 | Deterministic Automation |
| APR-06 | AI Model as Bounded Actor |
| APR-07 | Autonomous or Agentic Actor |
| APR-08 | Multi-Agent System |
| APR-09 | Hybrid Human–Synthetic Arrangement |

## Execution Environment fields

| ID | Field |
|---|---|
| EE-01 | Environment Identity |
| EE-02 | Hardware Substrate |
| EE-03 | Operating System / Runtime |
| EE-04 | Workspace Identity |
| EE-05 | Toolchain Identity |
| EE-06 | Dependency State |
| EE-07 | Configuration State |
| EE-08 | Access and Credentials |
| EE-09 | Network and External Services |
| EE-10 | Input and Data State |
| EE-11 | Isolation Boundary |
| EE-12 | Observability and Evidence Capture |
| EE-13 | Persistence and Mutable State |
| EE-14 | Temporal / Sequence Context |
| EE-15 | Externalized State |
| EE-16 | Recovery / Reset Mechanism |

## Tool Capability Classes

| ID | Class |
|---|---|
| TCAP-01 | Authoring and Modification |
| TCAP-02 | Source and State Control |
| TCAP-03 | Construction and Transformation |
| TCAP-04 | Dependency and Configuration Management |
| TCAP-05 | Test and Verification Execution |
| TCAP-06 | Analysis |
| TCAP-07 | Runtime and Execution |
| TCAP-08 | Artifact and Release |
| TCAP-09 | Evidence and Observability |
| TCAP-10 | Coordination and Handoff |
| TCAP-11 | Synthetic Reasoning / Generation |

## Capability / authority relationship

```text
EffectiveCapabilityEnvelope
=
ActorCapability
∩ ToolCapability
∩ EnvironmentCapability
∩ AvailableAccess
```

and:

```text
AuthorizedExecutionEnvelope
⊆ EffectiveCapabilityEnvelope
∩ TransitionBoundary
∩ AuthorityGrant
```

## Core distinctions

```text
can reach ≠ may change
capability ≠ authority
Actor pattern ≠ logical Role
access credential ≠ Authority Grant
different Actor ≠ automatic independence
AI Actor ≠ separate STATE method
```

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.9  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
