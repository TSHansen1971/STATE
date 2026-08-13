# STATE Engineering Glossary

> **Document:** `07-reference/GLOSSARY.md`  
> **Title:** STATE Engineering Glossary  
> **Version:** 0.9  
> **Status:** Working Draft  
> **Created:** 2026-08-11  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


This glossary establishes the current working vocabulary of STATE Engineering.

## Access

A physical mechanism allowing an Actor or tool to reach, observe or mutate a system surface. Access does not itself establish Authority.

## Actor

The human, synthetic or hybrid entity assigned to perform a logical STATE Role.

## Actor Independence

The property by which logical Roles and responsibilities remain defined independently of Actor type.

## Actor Realization Pattern

A common physical form through which a logical STATE Role may be performed, such as an individual human, distributed team, supplier, deterministic automation, synthetic Actor or hybrid arrangement.

## Authorized Execution Envelope

The subset of effective physical capability that may legitimately be exercised under the applicable Authority Grant and Transition Boundary.

## Authority

The legitimate permission to decide, approve, delegate or mutate within a defined scope.

## Capability

What an Actor, tool or environment is actually able to do.

## Effective Capability Envelope

The capabilities actually available through the intersection of Actor capability, tool capability, environment capability and available access.

## Environment Drift

A material change in hardware, software, configuration, dependency, external service, data or other Execution Environment condition between relevant engineering activities.

## Execution Environment

The relevant physical and software context in which a STATE Role, Work Package, verification activity, transformation or Release action is performed.

## Externalized State

Material state outside the immediate local environment that can affect execution, such as remote configuration, service-side policy or hosted model version.

## False Independence

The appearance of independent verification where Actors or methods still share a material common failure source.

## Hybrid Actor Arrangement

A physical realization in which human and synthetic Actors jointly perform STATE Roles or Work Packages.

## Isolation Mechanism

A physical or logical mechanism reducing unintended interference among Work Packages, Actors, environments or mutable state.

## Mutation Surface

The physical system surface that an Actor or tool can actually change.

## Physical Realization

The concrete assignment of Actors, execution environments, tools, access and evidence mechanisms to the logical Roles and control obligations of a STATE Transition.

## Physical Realization Binding

The reconstructable relationship among logical Role, Actor Assignment, capability, Authority, Execution Environment, tool capability, access, evidence mechanism and Assurance control.

## Synthetic Actor

A non-human computational Actor, such as an AI model, agent or multi-agent system, assigned to perform one or more logical STATE functions.

## Tool Capability

The concrete transformation, verification, execution, analysis, release, evidence or coordination capability provided by a physical tool.

## Toolchain

The set of physical software tools and dependencies used to author, transform, construct, verify, execute, package or release state.

## Work Package

A bounded execution/control unit subordinate to one governing Transition Contract.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.9  
Initial publication: 2026-08-11  
Last modified: 2026-08-13
