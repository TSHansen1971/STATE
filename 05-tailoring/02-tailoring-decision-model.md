# Tailoring Decision Model

> **Document:** `05-tailoring/02-tailoring-decision-model.md`  
> **Title:** Tailoring Decision Model  
> **Version:** 0.10  
> **Status:** Normative Specification
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


The Tailoring Decision Model defines the context factors used to choose a proportionate STATE realization and the minimum information needed to make that choice reconstructable where required.

## 1. Tailoring is a decision, not a preset

STATE does not require a universal numeric risk score.

Tailoring is an engineering judgment informed by relevant context factors.

Profiles may accelerate common decisions, but the chosen realization shall remain appropriate to the actual Transition.

## 2. Tailoring Factors

STATE defines twelve Tailoring Factors.

### TF-01 — Consequence of Error

What happens if the Transition is wrong?

Consider:

- safety;
- security;
- availability;
- financial or mission consequence;
- irreversible loss;
- downstream propagation.

### TF-02 — Change Breadth

How much of the system or architecture can the Transition affect?

### TF-03 — Complexity and Coupling

How many dependencies, interfaces, hidden interactions or emergent effects exist?

### TF-04 — Uncertainty and Novelty

How much is unknown, new, poorly observed or difficult to predict?

### TF-05 — Reversibility

How easily can an undesirable Candidate or Release be corrected without compounding harm?

### TF-06 — Exposure

How broadly can the resulting state affect users, systems, environments or external parties?

### TF-07 — Security Relevance

Can the Transition affect privilege, trust, exposure, provenance, access, confidentiality, integrity, availability or failure behavior?

### TF-08 — Actor and Organizational Distribution

How many Actors, teams, suppliers or organizational boundaries participate?

Distribution does not itself mean high risk, but it changes handoff and common-state control.

### TF-09 — Automation and Autonomy

How much independent action can tools, automation or synthetic Actors perform before human intervention?

### TF-10 — Environment Variability

How much can hardware, runtime, dependency, external service or configuration variation affect the result?

### TF-11 — Evidence and Provenance Need

How important is later reconstruction, independent corroboration, reproducibility or source-to-artifact linkage?

### TF-12 — External Dependency

How much does the Transition depend on systems, providers, infrastructure or state outside direct control?

## 3. Tailoring Decision fields

Where an explicit Tailoring Decision is required, it shall be capable of representing:

### TLD-01 — Decision Identity

Identity of the Tailoring decision or profile application.

### TLD-02 — Transition Scope

Which Transition, project or class of Transitions the Tailoring applies to.

### TLD-03 — Governing Profile

Reference profile or local profile used as the starting point, if any.

### TLD-04 — Context Factors

Material Tailoring Factors supporting the decision.

### TLD-05 — Role Arrangement

Physical combination or separation of logical Roles.

### TLD-06 — Gate Realization

Manual, automated, delegated or hybrid gate mechanisms.

### TLD-07 — Work Product Representation

How logical Work Products are physically represented or compressed.

### TLD-08 — Verification Depth

Selected methods, coverage and claim depth.

### TLD-09 — Independence Depth

Required Actor, method, tool, environment, organizational or decision independence.

### TLD-10 — Evidence Depth

Identity, integrity, provenance, preservation and reproduction expectations.

### TLD-11 — Environment Control

Required environment identity, isolation, reset and drift controls.

### TLD-12 — Work Package / Coordination Model

Package decomposition, concurrency, handoff or integration control where relevant.

### TLD-13 — Release Control

Release identity, transformation verification and provenance depth where applicable.

### TLD-14 — Escalation / Re-tailoring Triggers

Conditions requiring Tailoring reconsideration.

### TLD-15 — Tailoring Authority

Who or what is authorized to establish the Tailoring decision.

### TLD-16 — Decision Rationale

Why the selected realization is considered sufficient.

## 4. Tailoring Decision is not a new Work Product class

The Tailoring Decision may be represented within:

- the Transition Contract;
- WP-05 Transition Record;
- project policy;
- a reusable profile;
- an Assurance record;
- another controlled representation.

STATE does not add WP-12.

## 5. Inherited Tailoring

A project or organization may establish a reusable Tailoring profile.

A Transition may inherit that profile when:

- scope is within the profile's validity;
- Tailoring Factors remain within intended assumptions;
- no trigger requires deviation or re-tailoring.

Inherited Tailoring reduces repeated ceremony.

It does not remove responsibility to detect context change.

## 6. Tailoring deviation

A Transition may deviate from a profile when the deviation is:

- explicit where material;
- authorized;
- justified by actual context;
- compatible with Tailoring Invariants.

A profile is a default, not an excuse to apply irrelevant controls.

## 7. Upward and downward tailoring

Tailoring may increase or reduce control depth.

**Upward tailoring** may add:

- independent verification;
- stronger evidence identity;
- stronger environment control;
- more Work Package isolation;
- deeper security verification;
- stronger release provenance.

**Downward tailoring** may reduce:

- separate documents;
- Actor separation;
- evidence volume;
- verification breadth;
- environment capture;
- release ceremony.

Downward tailoring remains inside the Tailoring Envelope.

## 8. Re-tailoring triggers

STATE defines twelve common re-tailoring triggers.

### RT-01 — Scope Expansion

Transition Boundary or Work Package breadth materially expands.

### RT-02 — Consequence Increase

Potential cost of error becomes materially greater.

### RT-03 — Security-Relevant Discovery

A previously unrecognized security property becomes affected.

### RT-04 — Architecture Impact

The Transition crosses or changes an architectural boundary.

### RT-05 — Actor Substitution

A materially different Actor or supplier takes over a Role.

### RT-06 — Automation / Autonomy Increase

Execution becomes more autonomous or gains broader tool capability.

### RT-07 — Environment Change

Relevant runtime, hardware, dependency, provider or external service changes.

### RT-08 — Repeated Verification Failure

Failure pattern suggests the original control depth or understanding is insufficient.

### RT-09 — Evidence Weakness

Required claims cannot be supported with the selected evidence mechanism.

### RT-10 — Distribution Increase

More teams, organizations, locations or handoffs become involved.

### RT-11 — Release Expansion

Release target, audience, artifact set or deployment surface expands materially.

### RT-12 — Residual Uncertainty Increase

New uncertainty makes the existing Assurance basis inadequate.

## 9. Tailoring proportionality

The target is not minimum process.

The target is **sufficient control at justified cost**.

Over-tailoring can:

- delay feedback;
- hide important information in ceremony;
- create stale documents;
- encourage checkbox behavior.

Under-tailoring can:

- erase authority boundaries;
- weaken Verification;
- destroy provenance;
- permit false green;
- make failure unreconstructable.

## 10. Canonical Tailoring Decision rules

> **Tailoring shall be driven by engineering context rather than document count or organizational habit.**

> **A reusable profile may be inherited only while its assumptions remain valid.**

> **Tailoring may increase or decrease control depth, but shall remain inside the Tailoring Envelope.**

> **Material context change triggers re-tailoring.**

> **Tailoring Decision information may be embedded in existing STATE records; it does not create a new mandatory Work Product.**

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.10  
Initial publication: 2026-08-13  
Last modified: 2026-08-13