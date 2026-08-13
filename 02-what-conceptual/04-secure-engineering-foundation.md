# Secure Engineering Foundation

> **Document:** `02-what-conceptual/04-secure-engineering-foundation.md`  
> **Title:** Secure Engineering Foundation  
> **Version:** 0.2  
> **Status:** Foundational Working Specification  
> **Created:** 2026-08-11  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


STATE Engineering treats secure engineering as a foundational property of controlled change.

Security is not introduced as a separate lifecycle after functional implementation and is not confined to a specialist security role.

## 1. Core rule

> **Security-relevant engineering principles are intrinsic to the STATE method and are applied throughout specification, transition design, realization, verification, modification and acceptance.**

This property is referred to as **Secure Engineering by Construction**.

## 2. Methodological scope

The universal STATE core incorporates generally applicable, domain-neutral secure software and systems engineering principles and patterns.

The secure-engineering foundation is concerned with engineering behavior such as:

- clear abstractions, interfaces and boundaries;
- modularity and controlled dependencies;
- reduced unnecessary complexity;
- minimized unnecessary coupling and sharing;
- least authority and least privilege;
- explicit mediation of privileged actions;
- structured trust and controlled trust relationships;
- secure defaults;
- secure evolvability;
- continuous protection of required properties;
- secure failure and recovery;
- accountability, traceability and provenance;
- repeatable and sufficiently documented engineering procedures;
- secure modification;
- verification designed to match security-relevant claims;
- minimization;
- rigor proportionate to consequence and uncertainty.

These concepts are expressed through STATE-native Foundational Properties and Universal Engineering Principles.

## 3. Cross-layer application

Secure Engineering by Construction applies across all four abstraction levels.

### WHY — Contextual

The engineering context must recognize that uncontrolled change can degrade system trust, security and assurance even when functional behavior appears successful.

### WHAT — Conceptual

Security-relevant concepts such as authority boundary, trust relationship, privilege, dependency, invariant, provenance, failure state and recovery state are treated as first-class engineering concepts when relevant.

### HOW — Logical

The transition logic must include security-relevant specification, boundaries, invariants, verification and evidence whenever the transition can affect such properties.

### WITH WHAT — Physical

Concrete realization may use human controls, technical controls, automated verification, isolation, signing, hashing, access control, analysis tooling, reproducible execution or other mechanisms appropriate to the logical requirement.

No specific product or tool is constitutive of STATE.

## 4. Security-relevant transition rule

A transition is security-relevant when it can materially change a security-relevant property, including for example:

- authority or privilege;
- trust boundary or trust relationship;
- component or service exposure;
- dependency structure;
- execution environment;
- authentication or authorization behavior;
- protected communication;
- failure or recovery behavior;
- logging, auditability or evidence quality;
- source-to-artifact provenance;
- release or distribution integrity.

A security-relevant transition requires security-relevant verification proportionate to the affected claim.

## 5. Domain boundary

The universal STATE method defines secure-engineering methodology and generally applicable engineering patterns.

It does not make jurisdiction-, mission-, organization-, sector- or contract-specific obligations universal merely because such obligations may apply to a particular system.

Context-specific obligations are introduced through **Tailoring** when required.

This preserves a universal method core while allowing concrete implementations to satisfy additional external obligations.

## 6. Source discipline

STATE develops its own coherent normative principles rather than organizing itself as an external compliance crosswalk.

Directly relevant authoritative engineering sources may inform the rationale for a STATE requirement. The methodological source register records that provenance.

The external source therefore informs **why** a STATE engineering rule exists. It does not become the architecture of the STATE method.

## 7. Relationship to Assurance

Secure engineering and assurance are related but distinct.

Secure Engineering by Construction governs how security-relevant properties are considered throughout engineering.

Assurance evaluates whether the claims made about those properties are sufficiently supported by trustworthy evidence.

A secure design assertion without adequate evidence remains an unsupported assertion.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.2  
Initial publication: 2026-08-11  
Last modified: 2026-08-13
