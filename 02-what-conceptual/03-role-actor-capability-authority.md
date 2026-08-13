# Role, Responsibility, Actor, Capability and Authority

> **Document:** `02-what-conceptual/03-role-actor-capability-authority.md`  
> **Title:** Role, Responsibility, Actor, Capability and Authority  
> **Version:** 0.3  
> **Status:** Normative Specification
> **Created:** 2026-08-11  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


STATE Engineering is actor-independent but not actor-blind.

The method separates five concepts that are frequently conflated in software delivery organizations.

## 1. Role

A **Role** defines a logical function that must be performed within the engineering method.

A role exists independently of the person, team, supplier, automated system or synthetic system assigned to perform it.

## 2. Responsibility

A **Responsibility** defines what a role is accountable for producing, preserving, evaluating, deciding or controlling.

Responsibilities belong to roles before they belong to actors.

## 3. Actor

An **Actor** is the actual entity assigned to a role.

An actor may be:

- an individual human;
- a local human team;
- an inshore, nearshore or offshore team;
- a specialist supplier;
- deterministic automation;
- an AI model;
- an autonomous agent;
- a multi-agent system;
- a hybrid human–synthetic arrangement.

These are realization choices. They do not define different logical methods.

## 4. Capability

A **Capability** describes what an actor is technically, cognitively, organizationally or operationally able to do.

Capability can include:

- knowledge and skill;
- repository access;
- execution access;
- tooling;
- model capability;
- hardware capacity;
- organizational capacity;
- decision-support ability;
- ability to produce evidence.

## 5. Authority

**Authority** describes what an actor is legitimately permitted to decide, approve, delegate or change within the assigned role and scope.

Authority is normative.

Capability is descriptive.

They are not interchangeable.

## 6. Governing separation

```text
ROLE
What function must be performed?

RESPONSIBILITY
What must that function produce, preserve, evaluate or control?

ACTOR
Who or what performs the function?

CAPABILITY
What can that actor actually do?

AUTHORITY
What may that actor legitimately decide, approve or change?
```

## 7. Capability does not create authority

An actor may possess repository-wide technical access while being authorized to modify only one component.

An engineering team may understand a broader architecture while being authorized to implement only a bounded transition.

An automated or synthetic actor may be capable of building, testing, committing and deploying while being authorized only to produce a Candidate State.

Possession of credentials, tools, knowledge or technical reach does not establish legitimate authority.

## 8. Actor substitution

A logical role may be reassigned from one actor class to another without redefining the role itself.

Actor substitution is valid only when the replacement actor satisfies the applicable:

- capability requirements;
- authority grant;
- transition boundary;
- evidence obligations;
- traceability requirements;
- assurance requirements.

> **Actor substitution shall not silently change the control model.**

Replacing a local human developer with an external team or an autonomous engineering agent does not automatically change specification authority, architecture authority, verification requirements or acceptance authority.

## 9. Actor independence is not actor equivalence

STATE does not assume that all actors have identical failure modes.

A senior local team, a newly formed supplier team, deterministic automation and a generative system may all perform the same logical role while requiring different supervision, verification independence, evidence depth or authorization boundaries.

Those differences are handled through actor assignment, Tailoring and Assurance rather than by redefining the logical role.

## 10. Relationship to the canonical role model

This page defines the conceptual separation.

The canonical authority domains, logical roles, delegation rules and role-combination constraints are defined in [`06-role-authority-responsibility-model.md`](06-role-authority-responsibility-model.md).

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.3  
Initial publication: 2026-08-11  
Last modified: 2026-08-13