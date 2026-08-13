# WITH WHAT — Physical Layer

> **Document:** `04-with-what-physical/README.md`  
> **Title:** WITH WHAT — Physical Layer  
> **Version:** 0.9  
> **Status:** Current Documentation
> **Created:** 2026-08-11  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


The Physical layer defines how the logical STATE method is realized through concrete execution capacity.

Its governing question is:

> **With what actors, hardware, software, environments, toolchains, access mechanisms and evidence mechanisms is a particular STATE implementation performed?**

## Contents

1. [`01-physical-realization-model.md`](01-physical-realization-model.md) — the binding from logical STATE roles and authority to concrete actors, capabilities, environments and tools.
2. [`02-actor-realization-patterns.md`](02-actor-realization-patterns.md) — human, supplier, automated, synthetic and hybrid actor patterns.
3. [`03-execution-environment-and-toolchain-model.md`](03-execution-environment-and-toolchain-model.md) — execution environment identity, tool capability, access, isolation, evidence capture and environment drift.

## Boundary of the Physical layer

The Physical layer may describe:

- individuals and teams;
- sourcing topology;
- suppliers;
- automated systems;
- AI models and agents;
- hardware;
- operating systems and runtimes;
- programming languages;
- editors and development environments;
- repositories;
- build systems;
- verification tools;
- release tools;
- local or remote infrastructure;
- evidence-capture mechanisms.

It does not elevate any of these into a defining property of STATE Engineering.

## Core rule

> **The logical method defines what must be controlled. The Physical layer defines how that control is concretely realized.**

Actor substitution, hardware substitution or tool substitution may change capability, failure modes, evidence and Assurance requirements.

They do not silently change logical Role or Authority.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-SA 4.0  
Version: 0.9  
Initial publication: 2026-08-11  
Last modified: 2026-08-13
