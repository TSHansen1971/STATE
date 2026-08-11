# Role, Actor, Capability and Authority

> **Document:** `02-what-conceptual/03-role-actor-capability-authority.md`  
> **Title:** Role, Actor, Capability and Authority  
> **Version:** 0.1  
> **Status:** Working Draft  
> **Created:** 2026-08-11  
> **Last modified:** 2026-08-11  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None

STATE Engineering is actor-independent but not actor-blind.

The method separates five related concepts.

## Role

A **Role** defines a function that must be performed within the engineering method.

## Responsibility

A **Responsibility** defines what a role is accountable for producing, maintaining, evaluating or controlling.

## Actor

An **Actor** is the actual entity assigned to a role.

An actor may be human, synthetic or hybrid.

## Capability

A **Capability** describes what an actor is technically or operationally able to do.

## Authority

**Authority** describes what decisions, approvals or mutations the actor may legitimately perform within the assigned role.

## Governing separation

```text
ROLE
What function must be performed?

RESPONSIBILITY
What must the role produce or control?

ACTOR
Who or what performs the role?

CAPABILITY
What can that actor actually do?

AUTHORITY
What may that actor decide or change?
```

Capability does not imply authority.

A team with repository-wide technical access may still be authorized to modify only one bounded component.

An autonomous engineering system capable of building, testing, committing and deploying may still be authorized only to produce a candidate state.

## Actor substitution

A role may be reassigned from one actor class to another without redefining the logical role.

For example, an implementation role could be filled by:

- an individual developer;
- an internal engineering team;
- a distributed engineering team;
- an external delivery team;
- a specialist supplier;
- an AI-enabled coding system;
- an autonomous engineering agent;
- a mixed human–synthetic team.

The substitution is valid only when the replacement actor satisfies the capability, authority, traceability and assurance requirements of the role.

Actor substitution shall not silently weaken the control model.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.1  
Initial publication: 2026-08-11  
Last modified: 2026-08-11
