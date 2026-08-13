# Assurance

> **Document:** `06-assurance/README.md`  
> **Title:** Assurance  
> **Version:** 0.9  
> **Status:** Working Draft  
> **Created:** 2026-08-11  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


Assurance addresses whether a STATE Transition and its Physical Realization deserve the required degree of trust.

## Physical realization assurance

Assurance considers whether the assigned physical realization is fit for the logical obligation.

Relevant questions include:

- does the Actor have sufficient capability;
- does the Actor have only appropriate authority;
- is physical access broader than authority and, if so, is that controlled;
- is the Execution Environment sufficiently identified;
- can required evidence actually be captured;
- do selected tools introduce common-cause failure;
- does Actor or tool substitution affect prior verification;
- are external services part of the trusted basis;
- is isolation sufficient for concurrent or high-consequence work.

## Actor assurance

Actor independence does not mean Actor equivalence.

Assurance considers Actor-specific failure modes for:

- humans;
- teams;
- suppliers;
- deterministic automation;
- synthetic Actors;
- autonomous agents;
- multi-agent systems;
- hybrid arrangements.

The Actor class does not determine Assurance by itself.

The relevant capability, failure sources, authority and evidence do.

## False independence

Different Actors may still share:

- the same model;
- the same tool;
- the same environment;
- the same test oracle;
- the same source assumption;
- the same provider;
- the same data.

Actor count alone is not evidence of independence.

## Environment assurance

Environment Assurance considers:

- identity depth;
- material drift;
- dependency state;
- access;
- mutable and persistent state;
- remote dependencies;
- evidence capture;
- recovery and reset capability.

## Tool assurance

A tool may be:

- producer;
- verifier;
- evidence source;
- release transformer;
- authority mechanism.

Its role in the trusted basis should be explicit where material.

A tool verifying only its own output may require independent corroboration.

## Substitution assurance

Changing Actor, hardware, software, model, tool or environment requires reassessment where the change can affect:

- Candidate identity;
- verification meaning;
- evidence comparability;
- independence;
- provenance;
- security;
- reproducibility.

Assurance remains proportional to consequence, uncertainty, reversibility, exposure, substitution risk and the cost of being wrong.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.9  
Initial publication: 2026-08-11  
Last modified: 2026-08-13
