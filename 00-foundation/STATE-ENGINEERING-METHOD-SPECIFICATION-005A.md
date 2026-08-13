# STATE Engineering Method Specification 005A

> **Document:** `00-foundation/STATE-ENGINEERING-METHOD-SPECIFICATION-005A.md`  
> **Title:** STATE Engineering Method Specification 005A  
> **Version:** 0.5  
> **Status:** Current Foundational Specification  
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


## 1. Purpose

STATE Engineering governs controlled transitions between Authoritative States.

This specification supersedes `STATE-ENGINEERING-METHOD-SPECIFICATION-004A.md` as the current foundational specification and establishes the canonical logical STATE Cycle.

## 2. Canonical definition

> **STATE Engineering is a specification-driven, actor-independent, human-governed, traceable and evidence-based engineering method for controlling transitions between authoritative system states.**

## 3. Core architecture

STATE comprises:

- WHY — Contextual;
- WHAT — Conceptual;
- HOW — Logical;
- WITH WHAT — Physical;

governed across implementation by Tailoring, Assurance and Reference.

## 4. Foundational model

The current method foundation includes:

- twelve Foundational Properties;
- twelve Universal Engineering Principles;
- five Authority Domains;
- six canonical logical Roles;
- eleven canonical Work Product classes;
- ten Evidence Classes;
- nine Evidence-Quality Properties;
- the ten-phase P0–P9 STATE Cycle;
- ten logical Transition Gates G0–G9.

## 5. Canonical STATE Cycle

### P0 — Establish Authority and Baseline

Establish the authoritative starting state and legitimate authority basis.

Output: authorized starting condition.

Gate: G0 Authority & Baseline Gate.

### P1 — Specify Intent

Translate governing intent into operational Transition specification.

Output: WP-01 Transition Intent and Specification.

Gate: G1 Specification Gate.

### P2 — Define Transition Boundary

Establish what may change, what shall not change and when escalation is required.

Output: Authorized Transition Boundary.

Gate: G2 Boundary Gate.

### P3 — Inspect Baseline and Establish Context

Acquire sufficient implementation context through bounded inspection.

Output: sufficient implementation context.

Gate: G3 Readiness Gate.

Canonical rule:

> **Inspect enough to act; do not inspect instead of acting.**

### P4 — Produce Candidate

Perform authorized mutation and establish identifiable Candidate State.

Output: Candidate State plus transformation evidence.

Gate: G4 Candidate Identity Gate.

### P5 — Execute and Observe

Exercise or analyze the Candidate under relevant conditions and capture observations.

Output: execution and observation Evidence Items.

Gate: G5 Observation Gate.

### P6 — Verify Claims

Evaluate required claims and record method, observation, evidence, conclusion and limitation.

Output: Verification Records.

Gate: G6 Verification Gate.

### P7 — Assemble Evidence

Bind evidence to Baseline, Candidate, claims and decision context.

Output: decision-ready Evidence Set.

Gate: G7 Evidence Gate.

### P8 — Decide Acceptance

Acceptance Authority decides:

- ACCEPT;
- REJECT;
- REPAIR REQUIRED;
- INCONCLUSIVE.

Output: WP-08 Acceptance Record.

Gate: G8 Acceptance Gate.

Only ACCEPT permits progression to P9.

### P9 — Establish New Baseline

Explicitly establish the accepted Candidate as the next Authoritative State.

Output: WP-09 Baseline Establishment Record and new Authoritative State.

Gate: G9 Baseline Establishment Gate.

## 6. Transition Gate semantics

A Transition Gate is a logical decision condition.

It is not inherently a meeting, manual approval, separate document or human click.

A gate may be automated where:

- evaluation conditions are specified;
- evaluator capability is sufficient;
- authority is valid and delegated where required;
- evidence is retained;
- escalation behavior exists for ambiguity or failure.

## 7. Gate meanings

- G0 — authority and Baseline are sufficient.
- G1 — specification is sufficient.
- G2 — Transition Boundary is sufficient.
- G3 — implementation context is sufficient.
- G4 — Candidate identity and transformation are sufficient.
- G5 — observation basis is sufficient.
- G6 — required verification outcomes are explicit.
- G7 — evidentiary basis is decision-ready.
- G8 — authorized Acceptance decision is made.
- G9 — accepted state is explicitly established as authoritative.

## 8. Process-gate versus claim outcome

Passing G6 does not mean every claim passed.

G6 can be satisfied when required claims have explicit PASS, FAIL or INCONCLUSIVE outcomes.

Gate success means the verification process is sufficiently complete for the next decision.

Claim success is a property of the individual claim.

## 9. Failure

FAIL and INCONCLUSIVE are first-class engineering outcomes.

A failed Candidate does not replace the Authoritative State.

A failed gate does not grant permission to bypass the gate merely because later technical actions remain possible.

## 10. Repair

Repair creates a new or revised Candidate State.

Verification evidence from a previous Candidate may be reused only when it remains valid for the new Candidate, claim and conditions.

Candidate identity shall be sufficient to prevent silent evidence substitution.

## 11. Earliest-invalidated-phase rule

After failure, discovery or interruption:

> **Resume at the earliest phase whose required control condition is no longer valid.**

Examples:

- implementation defect → normally P4;
- verification-method defect → P5 or P6;
- evidence mismatch → P6 or P7;
- scope expansion → P2;
- intent change → P1;
- Baseline or authority change → P0.

## 12. Boundary breach

Discovery that an action lies outside the Transition Boundary does not create authority.

The actor shall preserve state, record the condition where material, escalate and re-establish the appropriate gate before proceeding.

## 13. Safe resumption

A Transition may resume after interruption when its preceding gate conditions can be reconstructed as still valid.

A Resume Point is therefore a verified control position, not merely the point at which work stopped.

## 14. Acceptance and baseline establishment

Acceptance and baseline establishment are distinct logical acts.

Before G9 passes, the previous Authoritative State remains authoritative.

This remains true even if G8 produced ACCEPT.

## 15. Release

Release is an optional post-cycle act when distribution, deployment or publication requires separate Release Authority.

Release failure does not automatically erase Acceptance or baseline establishment.

## 16. Phase overlap

Phases define logical dependency, not mandatory serial wall-clock execution.

Evidence capture may begin before P7.

Verification preparation may begin before P6.

Activities may overlap where authority, dependency, traceability and Assurance remain valid.

## 17. No false green

STATE prohibits uncontrolled conversion of failure into success, including:

- weakening verification only to obtain PASS;
- silently reducing claim scope after failure;
- discarding relevant negative evidence;
- replacing a Candidate without updating identity;
- expanding scope because technical access exists;
- treating Acceptance as baseline establishment.

## 18. Canonical cycle rule

> **Production changes state. Verification evaluates claims about state. Evidence supports or challenges those claims. Acceptance authorizes state. Baseline establishment makes accepted state authoritative.**

## 19. Canonical authority rule

> **Technical ability to continue does not establish authority or justify gate progression.**

## 20. Canonical state rule

> **A Candidate State shall not become authoritative by implementation success, verification success, evidence accumulation or Acceptance alone. It becomes authoritative only after explicit baseline establishment at P9.**

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.5  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
