# Execution Environment and Toolchain Model

> **Document:** `04-with-what-physical/03-execution-environment-and-toolchain-model.md`  
> **Title:** Execution Environment and Toolchain Model  
> **Version:** 0.9  
> **Status:** Normative Specification
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


The Execution Environment and Toolchain Model defines how STATE identifies the concrete technical conditions under which engineering activity occurs.

## 1. Execution Environment definition

> **An Execution Environment is the relevant physical and software context in which a STATE Role, Work Package, verification activity, transformation or release action is performed.**

Environment scope is claim-relative.

A source-editing activity may require one identity depth.

A performance claim may require much deeper hardware and runtime identity.

## 2. Execution Environment fields

STATE defines the following physical environment dimensions.

### EE-01 — Environment Identity

Stable identity or description sufficient to distinguish the relevant environment.

### EE-02 — Hardware Substrate

Relevant processor, memory, storage, accelerator, device or hardware characteristics where they affect the claim.

### EE-03 — Operating System / Runtime

Relevant operating-system, container, virtual-machine, language-runtime or execution-layer identity.

### EE-04 — Workspace Identity

Relevant repository, branch, checkout, worktree, directory or other working-state identity.

### EE-05 — Toolchain Identity

Compilers, interpreters, SDKs, build tools, package managers or other transformation tooling.

### EE-06 — Dependency State

Libraries, packages, frameworks, model weights, external modules or other dependencies relevant to the activity.

### EE-07 — Configuration State

Environment variables, feature flags, build configuration, runtime settings or other relevant configuration.

### EE-08 — Access and Credentials

Credentials, tokens, repository permissions, filesystem access, cloud roles or other physical access mechanisms.

### EE-09 — Network and External Services

Remote services, APIs, model providers, package repositories, databases or network conditions that may affect execution.

### EE-10 — Input and Data State

Relevant data, fixtures, prompts, documents, test corpora or other activity inputs.

### EE-11 — Isolation Boundary

Sandbox, container, workspace, branch, machine, namespace or other mechanism limiting interference.

### EE-12 — Observability and Evidence Capture

Logging, tracing, output capture, audit mechanisms, manifests or other evidence-generating mechanisms.

### EE-13 — Persistence and Mutable State

Caches, generated files, local databases, agent memory, session state or other mutable state that can influence results.

### EE-14 — Temporal / Sequence Context

Relevant date, sequence, version, upstream state or execution order where timing affects identity or behavior.

### EE-15 — Externalized State

State held outside the immediate environment but capable of influencing results, such as remote configuration, service-side policy or hosted model version.

### EE-16 — Recovery / Reset Mechanism

The means by which environment state can be restored, cleaned, rebuilt or re-established when needed for reproducibility or repair.

## 3. Environment identity rule

> **Capture enough environment identity to support the claim; do not collect irrelevant machine trivia merely because it is available.**

Examples:

A pure source-diff claim may not require CPU model.

A performance claim may require CPU, memory, workload and thermal or runtime conditions.

A local-model behavior claim may require model identity, runtime version, context settings and relevant generation parameters.

## 4. Environment drift

**Environment Drift** is a material change in physical or software conditions between:

- Candidate production;
- verification;
- evidence capture;
- Release;
- reproduction.

Drift may invalidate evidence where the claim depends on the changed condition.

Not all drift is material.

## 5. Drift assessment

Environment Drift should be evaluated by asking:

- did the changed property affect the claim;
- did it alter the Candidate;
- did it alter the verification method;
- did it alter the observation conditions;
- did it alter provenance;
- did it alter security or access boundaries.

If yes, affected verification or evidence may require re-establishment.

## 6. Tool capability classes

STATE recognizes the following physical tool capability classes.

These are descriptive, not mandatory products.

### TCAP-01 — Authoring and Modification

Editors, IDEs, generators, refactoring tools or systems used to change source or other state.

### TCAP-02 — Source and State Control

Repositories, version-control tools, object stores or other state-identity mechanisms.

### TCAP-03 — Construction and Transformation

Compilers, build systems, packaging tools, conversion systems or artifact generators.

### TCAP-04 — Dependency and Configuration Management

Package managers, environment managers, configuration systems and dependency resolvers.

### TCAP-05 — Test and Verification Execution

Test runners, harnesses, simulators, emulators or verification automation.

### TCAP-06 — Analysis

Static analyzers, profilers, scanners, diff tools, formal tools or analytical systems.

### TCAP-07 — Runtime and Execution

Application runtimes, local servers, containers, virtual machines, model runtimes or execution hosts.

### TCAP-08 — Artifact and Release

Signing, packaging, registry, deployment, distribution or publication tooling.

### TCAP-09 — Evidence and Observability

Logging, tracing, monitoring, manifest, hashing, signing or evidence collection.

### TCAP-10 — Coordination and Handoff

Issue tracking, documentation, messaging, workflow orchestration or handoff systems.

### TCAP-11 — Synthetic Reasoning / Generation

AI models, code models, reasoning systems or generative systems used in an assigned Role.

A single tool may satisfy several classes.

## 7. Tool identity

Tool identity matters when the tool can materially affect:

- Candidate state;
- verification result;
- evidence;
- artifact generation;
- reproducibility;
- security;
- provenance.

STATE does not require version capture for every incidental utility.

## 8. Tool trust

A tool should not be trusted merely because it is commonly used.

Relevant questions include:

- what claim depends on it;
- what state can it mutate;
- how is its output verified;
- what evidence does it generate;
- can it silently change;
- does it depend on remote state;
- does it share a failure source with the thing it verifies.

## 9. Self-verification risk

A production tool verifying only its own output may provide weak independence.

Examples:

- generator reports its own output valid;
- model critiques its own answer using identical context;
- build system alone asserts package provenance;
- deployment tool alone asserts successful runtime behavior.

Such evidence can be useful.

It may require independent support depending on Assurance.

## 10. Local versus remote execution

STATE is neutral between local and remote execution.

Local execution may provide:

- stronger direct control;
- lower external dependency;
- easier environment identity.

Remote execution may provide:

- scalable infrastructure;
- standardized environments;
- independent service capabilities.

Neither is inherently compliant, secure or trustworthy by location alone.

## 11. Hardware substitution

Hardware changes can be neutral for one claim and material for another.

Examples:

- source formatting may be hardware-neutral;
- performance is not;
- hardware-specific compilation may not be;
- accelerator-dependent model behavior may not be.

Hardware identity is therefore claim-relative.

## 12. Software substitution

Replacing compiler, runtime, library, model, build system or dependency may alter Candidate or verification meaning.

Substitution shall be assessed for:

- output equivalence;
- behavioral change;
- evidence comparability;
- provenance;
- security properties;
- reproduction.

## 13. Synthetic execution environment

When a synthetic Actor is used, the environment may include:

- model identity;
- model/runtime version;
- provider or local host;
- system instructions;
- task context;
- tool definitions and permissions;
- memory / persistence;
- retrieval sources;
- generation configuration;
- external service state.

Only properties relevant to the claim need to be controlled or evidenced.

## 14. Evidence capture by design

The environment should make required evidence observable.

A verification or transformation that cannot produce the evidence required for Acceptance may be physically unsuitable even when it can technically perform the activity.

## 15. Reproducibility

Reproducibility does not universally require byte-for-byte identity.

STATE distinguishes:

- exact reproduction;
- functionally equivalent reproduction;
- statistically consistent reproduction;
- independently corroborated observation.

The required form depends on the claim.

## 16. Canonical Environment and Toolchain rules

> **Environment identity is claim-relative.**

> **Environment Drift invalidates evidence only where the changed condition is material to the claim.**

> **A tool is part of the trusted basis only to the degree that a claim depends on it.**

> **Production tooling does not automatically provide independent verification of its own output.**

> **Local and remote execution are physical realization choices, not different STATE methods.**

> **Hardware, software and model substitution shall be assessed for their effect on Candidate identity, evidence and Assurance.**

> **The physical environment shall support the evidence obligations of the logical Transition.**

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-SA 4.0  
Version: 0.9  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
