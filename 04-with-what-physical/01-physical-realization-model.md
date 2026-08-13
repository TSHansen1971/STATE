# Physical Realization Model

> **Document:** `04-with-what-physical/01-physical-realization-model.md`  
> **Title:** Physical Realization Model  
> **Version:** 0.9  
> **Status:** Normative Specification
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


The Physical Realization Model defines the binding between actor-independent STATE logic and the concrete resources used to execute it.

## 1. Physical realization definition

> **A Physical Realization is a concrete assignment of actors, execution environments, tools, access and evidence mechanisms to the logical Roles and control obligations of a STATE Transition.**

The physical realization is specific to an implementation context.

The logical STATE method remains independent of it.

## 2. Physical Realization Binding

STATE defines a **Physical Realization Binding** as the reconstructable relationship among:

```text
Logical Role
   │
Actor Assignment
   │
   ├── Actor identity / class
   ├── Capability
   ├── Authority Grant
   ├── Execution Environment
   ├── Tool capability
   ├── Access
   ├── Evidence mechanism
   └── Assurance control
```

A Physical Realization Binding may be represented through existing Actor Assignment, Transition Contract, environment records, configuration or other implementation material.

It is not a new mandatory Work Product.

## 3. Realization dimensions

A Physical Realization shall be capable of representing the following dimensions when relevant.

### PR-01 — Logical Role

Which STATE Role is being realized.

### PR-02 — Actor Identity or Actor Class

Who or what performs the Role.

### PR-03 — Capability Basis

Why the Actor is considered capable of performing the assigned function.

### PR-04 — Authority Basis

Which Authority Grant limits the Actor's legitimate decisions and mutation.

### PR-05 — Execution Environment

The environment in which the Role is performed.

### PR-06 — Tool Capability

The concrete tool or tool class used to perform the activity.

### PR-07 — Access and Credential Basis

What access enables the Actor or tool to reach the relevant system surface.

### PR-08 — Mutation Surface

Which physical system surfaces can actually be changed.

### PR-09 — Evidence-Capture Mechanism

How observations, changes, identity and decisions become Evidence Items.

### PR-10 — Isolation Mechanism

How interference or unintended coupling is reduced where required.

### PR-11 — Communication / Handoff Mechanism

How relevant information crosses Actor, team, supplier or tool boundaries.

### PR-12 — Persistence and State

Which local, remote, persistent or session state can affect execution.

### PR-13 — External Dependency

Which service, network, provider or external system can materially affect the Role.

### PR-14 — Assurance Control

Which additional control is required because of the selected Actor, environment or tool realization.

## 4. Effective Capability Envelope

The **Effective Capability Envelope** is what the physical combination of Actor, tool, environment and access can actually do.

Conceptually:

```text
EffectiveCapabilityEnvelope
=
ActorCapability
∩ ToolCapability
∩ EnvironmentCapability
∩ AvailableAccess
```

The intersection expresses the capabilities actually available in the concrete realization.

## 5. Authorized Execution Envelope

The **Authorized Execution Envelope** is the subset of effective capability that may legitimately be exercised.

Conceptually:

```text
AuthorizedExecutionEnvelope
⊆ EffectiveCapabilityEnvelope
∩ TransitionBoundary
∩ AuthorityGrant
```

This is a control relation, not a requirement for mathematical implementation.

Its purpose is to make one principle explicit:

> **Physical capability never expands logical authority.**

## 6. Access is not authority

Credentials, filesystem permissions, repository rights, shell access, administrator rights, API tokens, cloud roles or tool permissions are physical access mechanisms.

They are not equivalent to STATE Authority.

An Actor can possess access far broader than its authorized Transition.

STATE therefore distinguishes:

```text
can reach
≠
may change
```

## 7. Capability mismatch

A Physical Realization is invalid when an assigned Actor cannot perform the Role to the degree required by the Transition and Assurance objective.

Examples include:

- insufficient technical skill;
- unavailable build environment;
- model incapable of required context depth;
- verification tool unable to observe the target property;
- supplier lacking required system access;
- hardware unable to execute the relevant workload.

Capability mismatch is not repaired by expanding Authority.

## 8. Authority mismatch

An Actor may be fully capable but insufficiently authorized.

Examples:

- developer can deploy but lacks Release Authority;
- supplier can modify adjacent component but Transition Boundary excludes it;
- autonomous agent can commit but has authority only to produce a Candidate;
- verifier can edit source but is assigned read-only verification authority.

Capability does not cure authority mismatch.

## 9. Physical realization and Role combination

One physical Actor may realize multiple logical Roles where Tailoring and Assurance permit it.

The Physical layer records the combination.

It does not collapse the logical distinctions.

Example:

```text
Actor H1
 ├── Specification Role
 ├── Realization Role
 └── Verification Role
```

This may be legitimate for a low-consequence Transition if Assurance remains sufficient.

It does not mean the three Roles became one Role.

## 10. Physical realization and distributed delivery

STATE supports geographically and organizationally distributed delivery.

A Work Package may be assigned to:

- local staff;
- another internal location;
- an inshore team;
- a nearshore team;
- an offshore team;
- a supplier;
- a synthetic Actor;
- a hybrid arrangement.

Location is not Authority.

Contractual relationship is not Authority.

Organizational distance is not automatically independence.

These properties may influence Assurance but do not redefine the Role.

## 11. Physical realization and evidence

The physical implementation must support evidence obligations defined by the logical Transition.

Examples:

- source-control identity;
- terminal or build log;
- test output;
- runtime observation;
- artifact digest;
- environment manifest;
- approval record;
- signed decision;
- automated trace.

The required mechanism depends on the claim.

## 12. Physical realization and secure engineering

Secure Engineering by Construction applies to the Physical layer.

Relevant concerns include:

- least physical access;
- constrained tool permission;
- explicit credentials;
- isolated execution where appropriate;
- controlled external dependencies;
- secure defaults;
- evidence integrity;
- provenance;
- recoverability;
- protection of authoritative baselines.

## 13. Substitution rule

Changing Actor, tool or environment requires reassessment where the substitution can affect:

- capability;
- authority;
- failure mode;
- evidence quality;
- verification independence;
- state identity;
- reproducibility;
- provenance;
- security-relevant properties.

> **Physical substitution does not automatically invalidate the Transition, but neither is it assumed neutral.**

## 14. Canonical Physical Realization rules

> **The logical method defines the control obligation; the Physical layer selects the concrete means.**

> **Physical capability never expands logical authority.**

> **Access is not authority.**

> **Actor, tool and environment substitution shall be assessed for their effect on capability, evidence and Assurance.**

> **A physical Actor may realize multiple logical Roles without collapsing their logical separation.**

> **No specific human sourcing model, AI system, hardware platform or software tool is constitutive of STATE Engineering.**

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-SA 4.0  
Version: 0.9  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
