# STATE v1.1 WP09 — Authority Grant Operational Patterns Report

> **Document:** `10-development/STATE-V1.1-WP09-AUTHORITY-GRANT-OPERATIONAL-PATTERNS-REPORT-001A.md`
> **Title:** STATE v1.1 WP09 — Authority Grant Operational Patterns Report
> **Version:** 001A
> **Status:** Current Documentation
> **Created:** 2026-08-13
> **Last modified:** 2026-08-13
> **Author:** Tor-Ståle Hansen
> **Co-authors:** None

## 1. Purpose

WP09 answers the practical question:

> **What does an Authority Grant look like in real work?**

The authoritative WP09 start HEAD is:

`94c55400db05dda618e3e6f32ab446456360c19f`

## 2. Guidance artifact

WP09 creates:

`08-examples/AUTHORITY-GRANT-OPERATIONAL-PATTERNS-001A.md`

The artifact is explicitly non-normative operational guidance.

## 3. Required patterns

The guidance contains all six required patterns:

1. human Realization Actor;
2. deterministic build / deployment automation;
3. LLM coding agent;
4. autonomous multi-step agent;
5. mixed human / AI realization;
6. external supplier or contractor.

Each pattern includes:

- Role;
- Actor;
- Capability;
- granted Authority;
- prohibited Authority;
- Transition Boundary;
- delegation source;
- expiry or termination condition;
- Evidence obligation;
- escalation condition.

## 4. Existing Authority Grant semantics and WP09 operationalization

The operational patterns are derived from existing STATE semantics in which:

- WP-02 is the Authority Grant Work Product and establishes bounded decision and mutation authority;
- Authority is established separately from Role, Actor Assignment, Capability and Access;
- delegated Authority remains traceable to a human-established governance source;
- synthetic Actors, automation and agents may exercise delegated Authority where explicitly established;
- technical autonomy does not make an Actor an independent normative source of Authority.

WP09 does not redefine that model.

For practical use, this guidance makes the backlog-required operational details explicit in each pattern: Role, Actor, Capability, granted and prohibited Authority, Transition Boundary, delegation source, expiry or termination, Evidence obligation and escalation condition.

The broader checklist also exposes useful operational details such as scope, constraints, delegation and revocation.

These fields are **non-normative operationalization**, not a new canonical Authority Grant schema.

No new Authority Domain or Work Product class is introduced.

## 5. Core demonstration

The guidance contains two Actors, `AI-RED` and `AI-BLUE`, with deliberately identical technical Capability:

- same model / runtime;
- same repository credentials;
- same tool set;
- same ability to read, edit, test and create commits.

Their Authority differs.

`AI-RED` holds bounded mutation Authority.

`AI-BLUE` holds Verification Authority without Candidate-mutation Authority.

The same defect is therefore repairable by one Actor and recordable / escalatable, but not repairable, by the other.

This demonstrates:

**Capability does not create Authority.**

## 6. Actor independence

The six patterns use the same general Authority Grant semantics for human, automated, synthetic, hybrid and supplier Actors.

No actor-specific Authority exception is created.

## 7. Normative integrity

WP09 changes no normative method document.

It introduces:

- no new Authority Domain;
- no new logical Role;
- no new Work Product class;
- no new Transition Gate;
- no new Conformance Requirement;
- no release promotion.

## 8. WP09 acceptance

**WP09 — Authority Grant operational patterns:** PASS

`RG4 — Demonstrability` remains pending WP10 through WP12.

Next authorized work package:

`WP10 — Stochastic Actor and AI Evidence Patterns`

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-SA 4.0  
Version: 001A  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
