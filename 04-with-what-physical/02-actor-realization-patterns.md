# Actor Realization Patterns

> **Document:** `04-with-what-physical/02-actor-realization-patterns.md`  
> **Title:** Actor Realization Patterns  
> **Version:** 0.9  
> **Status:** Normative Working Specification  
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


STATE is actor-independent at the logical level and actor-specific at the Physical level.

This page defines common realization patterns without making them exhaustive or mandatory.

## 1. Pattern rule

> **Actor patterns describe how a logical Role may be physically realized. They do not define different versions of the STATE method.**

## APR-01 — Individual Human Actor

One human performs one or more logical Roles.

Typical physical considerations include:

- knowledge and skill;
- access;
- availability;
- local environment;
- evidence capture;
- role combination;
- decision independence.

A single-person project can use STATE.

Logical separation is preserved even when physical separation is impossible or unnecessary.

## APR-02 — Co-located Human Team

A local team distributes Roles and Work Packages among several people working in a common organizational or physical environment.

Physical considerations include:

- handoff;
- shared workspace;
- source coordination;
- review independence;
- shared credentials or access;
- integrated Candidate construction.

## APR-03 — Distributed Human Team

A team operates across locations, time zones or organizational units.

This pattern includes inshore, nearshore and offshore arrangements.

Physical considerations include:

- communication latency;
- handoff quality;
- shared state identity;
- environment differences;
- access boundaries;
- Work Package dependency;
- evidence preservation across boundaries.

Geographic distance does not itself imply poor or strong Assurance.

## APR-04 — Specialist Supplier

A supplier or external organization performs one or more Roles or Work Packages.

Physical considerations include:

- authority source;
- contractual versus engineering authority;
- access;
- interface boundary;
- deliverable identity;
- provenance;
- evidence handoff;
- Acceptance independence.

A commercial agreement can define obligations.

It does not by itself establish STATE Acceptance Authority.

## APR-05 — Deterministic Automation

A script, build system, pipeline, policy engine or other deterministic mechanism performs a bounded function.

Typical uses include:

- build;
- transformation;
- checking;
- test execution;
- artifact packaging;
- evidence collection;
- gate evaluation.

Automation is powerful where conditions are explicit and repeatable.

Its capability and authority remain bounded.

## APR-06 — AI Model as Bounded Actor

A language model or other generative model performs a Role or part of a Role under explicit Actor Assignment.

Possible functions include:

- specification drafting;
- code generation;
- analysis;
- test generation;
- review;
- evidence summarization.

Relevant physical characteristics may include:

- model identity;
- runtime or provider;
- context and instruction basis;
- tool access;
- external-service dependence;
- stochastic configuration;
- state or memory;
- evidence capture.

An AI model does not gain Authority from apparent competence.

## APR-07 — Autonomous or Agentic Actor

An agentic system can plan and execute multiple actions through tools under a bounded objective.

Relevant controls may include:

- explicit Transition Boundary;
- command / tool authorization;
- execution sandboxing;
- mutation limits;
- gate authority;
- stop and escalation conditions;
- durable action trace;
- independent verification.

Autonomy is a capability characteristic.

It is not an Authority Domain.

## APR-08 — Multi-Agent System

Several synthetic Actors divide Roles, Work Packages, review or verification among themselves.

Physical considerations include:

- shared versus separate context;
- coordination;
- common failure sources;
- tool overlap;
- model commonality;
- evidence attribution;
- false independence.

Two agents using the same underlying model, prompt basis and evidence may not provide meaningful independent verification merely because they have different labels.

## APR-09 — Hybrid Human–Synthetic Arrangement

Humans and synthetic Actors share execution and control.

Examples include:

```text
Human Intent Authority
       ↓
Synthetic Specification / Realization
       ↓
Deterministic Verification
       ↓
Human Acceptance Authority
```

or:

```text
Human Specification
       ↓
AI Realization
       ↓
AI + Human Verification
       ↓
Human Baseline Establishment
```

STATE does not prescribe one hybrid arrangement.

The required control depends on consequence, uncertainty and Assurance.

## 2. Actor substitution

Actor substitution means one Actor replaces another in the same logical Role or Work Package.

Substitution requires reassessment where relevant of:

- capability;
- Authority Grant;
- physical access;
- environment;
- tools;
- independence;
- evidence mechanism;
- handoff state;
- provenance.

The logical Role remains stable.

## 3. Capability profile

A Physical Actor may have a capability profile including:

- domain knowledge;
- engineering skill;
- system knowledge;
- reasoning capacity;
- execution throughput;
- tool competence;
- context capacity;
- availability;
- reproducibility;
- ability to preserve evidence.

STATE does not define a universal scoring system.

Tailoring may introduce one where useful.

## 4. Human-specific failure modes

Human Actors may exhibit:

- misunderstanding;
- memory failure;
- fatigue;
- inconsistent execution;
- undocumented tacit knowledge;
- authority assumption;
- handoff loss.

These are engineering considerations.

They are not reasons to treat humans as outside the control model.

## 5. Synthetic-specific failure modes

Synthetic Actors may exhibit:

- hallucinated state;
- context loss;
- stochastic inconsistency;
- tool misuse;
- prompt or instruction conflict;
- false confidence;
- hidden provider/runtime change;
- weak long-horizon state continuity.

These are physical Actor characteristics.

They do not redefine the logical method.

## 6. Supplier and distributed-team failure modes

Distributed delivery may introduce:

- delayed feedback;
- environment mismatch;
- incomplete context;
- contract/interface ambiguity;
- identity mismatch;
- evidence handoff gaps;
- local optimization against system-level claims.

These are handled through the same Transition Contract, Work Package, evidence and Assurance structures.

## 7. False independence

Different Actors do not necessarily provide independent verification.

Potential common-cause dependence includes:

- same human author reviewing own work;
- same model family;
- same tool;
- same test oracle;
- same environment;
- same upstream data;
- same hidden assumption.

Independence is assessed through the Verification Independence Dimensions, not through Actor count alone.

## 8. Canonical Actor Pattern rules

> **Actor independence does not mean actor equivalence.**

> **Geography, employment status, supplier status or synthetic nature does not by itself define Authority.**

> **Autonomy is capability, not authority.**

> **Multiple Actors do not create meaningful independence when they share the same relevant failure source.**

> **AI is a Physical realization option, not a constitutive element of STATE Engineering.**

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.9  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
