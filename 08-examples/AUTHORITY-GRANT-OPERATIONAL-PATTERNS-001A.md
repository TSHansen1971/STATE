# STATE Engineering — Authority Grant Operational Patterns

> **Document:** `08-examples/AUTHORITY-GRANT-OPERATIONAL-PATTERNS-001A.md`
> **Title:** STATE Engineering — Authority Grant Operational Patterns
> **Version:** 001A
> **Status:** Current Documentation
> **Created:** 2026-08-13
> **Last modified:** 2026-08-13
> **Author:** Tor-Ståle Hansen
> **Co-authors:** None

## 1. Nature and authority of this guidance

This document is **non-normative operational guidance**.

It answers a practical question:

> **What does an Authority Grant look like in real work?**

The patterns below apply existing STATE Engineering semantics. They do not create new Authority Domains, logical Roles, Work Product classes, Transition Gates, Conformance Requirements or actor-specific governance exceptions.

Where this guidance and the current normative STATE corpus differ, the normative corpus governs.

## 2. Operational shape of an Authority Grant

STATE treats an Authority Grant as a bounded assignment of legitimate decision or mutation rights.

A practical grant should make the following control information reconstructable to the degree relevant to the Transition:

| Control field | Operational question |
|---|---|
| Authority source | Where does the legitimacy of this grant originate? |
| Authority domain | Which decision rights are being delegated? |
| Actor or Role assignment | Who or what may exercise the grant? |
| Scope | Which system, component, Transition or decision is covered? |
| Permitted actions | What may the Actor decide, approve or change? |
| Constraints | Which invariants or limitations remain binding? |
| Validity | When and under what condition is the grant active? |
| Evidence obligation | What must be recorded when the grant is exercised? |
| Escalation condition | When must the Actor stop and seek additional Authority? |
| Delegation condition | May the Actor delegate any part of the grant onward? |
| Revocation condition | How can the grant be withdrawn or terminated? |

The documentary representation may be lightweight or detailed.

The field set in this section is a **non-normative operationalization for this guidance**. It does not create a new canonical Authority Grant schema or require one physical record format.

The Authority boundary itself must remain understandable where it matters to control.

## 3. Reading the patterns

Each pattern below exposes the minimum WP09 operational fields:

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

The patterns deliberately use different Actor types while preserving the same underlying rule:

> **Capability does not create Authority.**

## 4. Pattern 1 — Human Realization Actor

### Situation

A senior developer is assigned to repair a defect in the invoice-calculation component.

The developer has broad repository access and is technically capable of changing adjacent pricing, customer and deployment code.

### Authority Grant

| Field | Pattern value |
|---|---|
| Role | `LR-02 — Realization Role` |
| Actor | Human developer `H-DEV-01` |
| Capability | Read and modify the full application repository; run tests; create branches; inspect deployment configuration |
| Granted Authority | Modify `services/invoice/` and its directly associated tests to satisfy the approved defect specification |
| Prohibited Authority | Change pricing policy, public API contracts, deployment configuration, Acceptance basis or release state |
| Transition Boundary | Invoice defect Transition `TR-INVOICE-017`; write scope limited to invoice implementation and associated tests |
| Delegation source | Human Transition Authority `TA-INVOICE` under the project's established governance |
| Expiry / termination | Ends when the Transition is accepted, rejected, cancelled or the grant is revoked |
| Evidence obligation | Preserve Candidate identity, source diff, test results and any material deviation |
| Escalation condition | Stop and escalate if repair requires API change, pricing-policy change, dependency change or mutation outside the boundary |

### Example grant statement

```text
grant: AG-INVOICE-017-REALIZE
actor: H-DEV-01
role: LR-02 Realization Role
authority_source: TA-INVOICE
scope: TR-INVOICE-017 / services/invoice/
permitted: bounded implementation and associated test mutation
prohibited: pricing policy, public API, deployment, Acceptance, release
valid_until: transition closure or explicit revocation
evidence: diff + Candidate identity + test results + deviations
escalate_if: required repair exceeds component or approved behavior
delegation: not permitted
```

The developer's broad technical access does not enlarge this grant.

## 5. Pattern 2 — Deterministic Build / Deployment Automation

### Situation

A deterministic pipeline builds an accepted Candidate and deploys it to a controlled staging environment.

The pipeline credentials are technically capable of invoking several deployment actions.

### Authority Grant

| Field | Pattern value |
|---|---|
| Role | Physical automation performing bounded realization / release-execution activity as assigned by the Transition |
| Actor | Deterministic pipeline `AUTO-DEPLOY-STAGE-01` |
| Capability | Build artifacts, sign or package according to configured process, push artifacts and invoke deployment tooling |
| Granted Authority | Build the identified Candidate and deploy only that Candidate to the named staging environment after the configured preconditions are satisfied |
| Prohibited Authority | Select another Candidate, change source, alter Acceptance basis, deploy to production, waive failed Verification or create Release Authority |
| Transition Boundary | Candidate identity plus named staging target and configured deployment window |
| Delegation source | Human-established Transition / Release governance encoded into the pipeline invocation and environment policy |
| Expiry / termination | Single authorized run; terminates on success, failure, cancellation, Candidate mismatch or environment mismatch |
| Evidence obligation | Record Candidate hash, build inputs, artifact identity, execution log, deployment target and result |
| Escalation condition | Stop on identity mismatch, failed prerequisite, unexpected target, unavailable Evidence or any requested action outside staging |

### Operational point

Determinism does not create Authority.

A pipeline that can technically deploy to production is not authorized to do so unless that production action is inside its explicit grant.

## 6. Pattern 3 — LLM Coding Agent

### Situation

An LLM coding agent is assigned a bounded refactor in one parser module.

The agent can inspect much more of the repository and can technically edit any file exposed by its tools.

### Authority Grant

| Field | Pattern value |
|---|---|
| Role | `LR-02 — Realization Role` |
| Actor | LLM coding agent `AI-CODE-01` |
| Capability | Read repository context, reason about code, edit source, invoke existing tests and create Candidate artifacts |
| Granted Authority | Modify `src/parser.py` to perform the specified behavior-preserving refactor |
| Prohibited Authority | Modify tests, dependencies, public API, architecture, Transition Boundary, Acceptance basis or Release state |
| Transition Boundary | One parser-refactor Transition; write scope limited to `src/parser.py` |
| Delegation source | Human Transition Authority through `AG-PARSER-REF-01` |
| Expiry / termination | Ends on Transition closure, explicit revocation or discovery that required work exceeds the grant |
| Evidence obligation | Preserve prompt / instruction where evidentially relevant, Candidate diff, tool execution log, Verification inputs and discovered deviations |
| Escalation condition | Stop if the requested outcome requires mutation outside `src/parser.py`, behavior change, new dependency or architectural decision |

### Operational point

Tool access is Capability.

The grant determines legitimate action.

The agent must record and refuse an attractive out-of-boundary improvement rather than silently implement it.

## 7. Pattern 4 — Autonomous Multi-step Agent

### Situation

An autonomous engineering agent may inspect a repository, plan work, modify bounded files, run checks, revise its Candidate and prepare Evidence without waiting for a human instruction between every step.

### Authority Grant

| Field | Pattern value |
|---|---|
| Role | `LR-02 — Realization Role`, with explicitly assigned evidence-producing activities where applicable |
| Actor | Autonomous multi-step agent `AI-AUTO-02` |
| Capability | Multi-step planning, repository inspection, bounded source mutation, repeated tool use, local test execution and Candidate revision |
| Granted Authority | Independently sequence authorized realization actions inside Work Package `PKG-A`, including repeated repair attempts that remain inside the unchanged Transition Boundary |
| Prohibited Authority | Expand Work Package scope, modify governing specification, grant itself additional Authority, merge to authoritative baseline, make Acceptance decision or release |
| Transition Boundary | `PKG-A` paths, specified invariants, permitted tools and execution environment |
| Delegation source | Human-established Transition Authority assigning the bounded Work Package |
| Expiry / termination | Ends on Work Package completion, explicit cancellation, Authority revocation, boundary uncertainty or specified execution limit |
| Evidence obligation | Preserve plan revisions where material, tool actions, Candidate identities, Verification observations, failures, repair sequence and deviations |
| Escalation condition | Stop when a next useful step requires broader mutation, changed intent, changed architecture, changed Acceptance basis or unavailable required Evidence |

### Operational point

Autonomy changes how often the Actor needs interaction.

It does not silently widen the Actor's Authority.

## 8. Pattern 5 — Mixed Human / AI Realization

### Situation

A human engineer and an AI coding agent work together on the same bounded component.

The human chooses implementation direction and may directly edit the component.

The AI proposes and produces Candidate changes within a narrower sub-boundary.

### Authority Grants

| Field | Human Actor | AI Actor |
|---|---|---|
| Role | `LR-02 — Realization Role`; may additionally hold bounded Architecture Authority if separately granted | `LR-02 — Realization Role` |
| Actor | Human engineer `H-MIX-01` | AI coding agent `AI-MIX-01` |
| Capability | Read / write repository, reason about architecture, run tests, review and revise Candidate | Substantially similar repository read / write and test-tool capability |
| Granted Authority | Modify `component-x/`; choose implementation details that remain inside approved architectural invariants | Modify `component-x/adapters/` according to the human-established implementation direction |
| Prohibited Authority | Change Acceptance basis or Release state unless separately granted | Change architecture, modify outside adapter sub-boundary, change Acceptance basis, approve own Candidate or release |
| Transition Boundary | Full approved `component-x/` Transition | Nested adapter sub-boundary inside the same Transition |
| Delegation source | Human Transition Authority | Human Transition Authority through a narrower Actor Assignment / Authority Grant |
| Expiry / termination | Transition closure or revocation | Transition closure, revocation or loss of the human-established adapter task |
| Evidence obligation | Preserve architectural choices, Candidate diff and Verification basis | Preserve generated Candidate diff, relevant instructions, tool actions and deviations |
| Escalation condition | Escalate changes to intent, cross-component architecture or Acceptance basis | Escalate any need to leave adapter scope or change governing architecture |

### Operational point

Physical collaboration does not merge the grants.

The human and AI may work on the same Candidate while exercising different Authority.

## 9. Pattern 6 — External Supplier or Contractor

### Situation

An external supplier is contracted to implement a bounded subsystem change.

Supplier engineers may be highly capable and may have controlled access to the customer's repository and integration environment.

### Authority Grant

| Field | Pattern value |
|---|---|
| Role | `LR-02 — Realization Role` for the contracted implementation scope |
| Actor | Supplier engineer / supplier team `SUP-REAL-01` |
| Capability | Implement subsystem code, run agreed tests, prepare integration Candidate and inspect necessary interface context |
| Granted Authority | Modify the contracted subsystem and agreed supplier-owned test assets within Transition `TR-SUP-042` |
| Prohibited Authority | Change customer-wide architecture, unrelated components, Acceptance basis, production baseline, Release decision or customer governance |
| Transition Boundary | Contracted subsystem, named interfaces, agreed repositories / paths and stated invariants |
| Delegation source | Customer Transition Authority through the controlled supplier work authorization |
| Expiry / termination | Ends at contract / work-package closure, revocation, supplier off-boarding or Transition closure |
| Evidence obligation | Provide Candidate identity, source / artifact provenance, test results, dependency changes, deviations and required handover Evidence |
| Escalation condition | Stop and escalate interface conflict, required cross-boundary change, unclear requirement, unapproved dependency or inaccessible verification basis |

### Operational point

Commercial responsibility and technical competence do not create customer Acceptance or Release Authority.

Those rights remain where the governing Authority Grants place them.

## 10. Core demonstration — identical Capability, different Authority

Consider two instances of the same engineering agent configuration:

`AI-RED` and `AI-BLUE`.

They have:

- the same model and runtime;
- the same repository credentials;
- the same tool set;
- the same ability to read and edit files;
- the same ability to run tests;
- the same technical ability to create a commit.

Their **Capability is intentionally identical**.

Their Authority Grants are not.

| Field | `AI-RED` | `AI-BLUE` |
|---|---|---|
| Assigned Role | Realization Role | Verification Role |
| Technical Capability | Read, edit, run tests, create commits | Read, edit, run tests, create commits |
| Granted Authority | Modify `component-red/` and create Candidate artifacts | Execute defined Verification and preserve observations |
| Prohibited Authority | Modify outside `component-red/`; Accept; release | Modify Candidate; repair Candidate; Accept; release |
| Transition Boundary | Realization boundary for `component-red/` | Verification boundary for the identified Candidate |
| Required action when defect is found | Repair only if defect is inside the Realization grant | Record FAIL / INCONCLUSIVE and escalate; do not repair |
| Evidence obligation | Transformation Evidence plus Candidate identity | Verification Record plus referenced Evidence |
| Expiry | End of Realization assignment | End of Verification assignment |

Suppose both Actors see the same one-line defect.

Both can technically fix it.

Only `AI-RED` possesses mutation Authority for that component.

The correct STATE behavior is:

```text
AI-RED:
CAN FIX
+ HAS BOUNDED AUTHORITY
→ MAY FIX WITHIN THE GRANT

AI-BLUE:
CAN FIX
+ DOES NOT HAVE MUTATION AUTHORITY
→ SHALL RECORD / ESCALATE, NOT FIX
```

The difference is not intelligence, credentials, tool access or implementation skill.

The difference is Authority.

> **Two Actors may possess identical technical Capability while possessing different Authority.**

## 11. Grant expiry, revocation and stale authority

A grant should not be treated as permanent merely because an Actor remains technically able to perform the action.

Typical termination events include:

- Transition Acceptance;
- Transition rejection or cancellation;
- Work Package completion;
- expiry of a deployment window;
- Actor reassignment;
- explicit revocation;
- baseline or Candidate identity change that invalidates the grant;
- discovery that the grant was based on an invalid Authority source.

After termination, continued access is only technical Capability.

It is not continuing Authority.

## 12. Evidence obligation is part of exercised Authority

An Authority Grant may permit an Actor to perform an action only under an associated Evidence obligation.

Examples include:

- recording Candidate identity before mutation;
- preserving the exact diff;
- recording automation input and artifact identity;
- preserving Verification observations;
- recording material tool actions;
- preserving provenance for supplier artifacts;
- recording a boundary deviation rather than silently expanding scope.

Failure to satisfy the Evidence obligation can make the exercise of an otherwise permitted action unsuitable for progression or Acceptance.

## 13. Escalation is controlled behavior, not failure of autonomy

Escalation is required when the next meaningful action exceeds the current Authority Grant or cannot be classified safely inside it.

A useful operational rule is:

```text
INSIDE GRANT
→ ACT
→ PRESERVE REQUIRED EVIDENCE

OUTSIDE GRANT
→ DO NOT ACT
→ RECORD / ESCALATE

UNCERTAIN
→ DO NOT ASSUME
→ ESCALATE OR OBTAIN AN AMENDED GRANT
```

The Actor is not expected to solve an Authority problem by silently converting it into an implementation decision.

## 14. Compact Authority Grant checklist

Before an Actor exercises material decision or mutation rights, the Transition should be able to answer:

1. What Role is the Actor performing?
2. Who or what is the Actor?
3. What relevant Capability does the Actor possess?
4. What Authority is actually granted?
5. What Authority is explicitly prohibited or retained elsewhere?
6. What is the Transition Boundary?
7. What is the human-established delegation source?
8. When does the grant expire or terminate?
9. What Evidence must accompany exercise of the grant?
10. What condition requires escalation?
11. Is onward delegation allowed?
12. How can the grant be revoked?

If technical access is the only answer to question 4, the Authority Grant is not established merely by that access.

## 15. Operational conclusion

Authority Grants make STATE's actor independence practical.

Human developers, deterministic automation, LLM coding agents, autonomous agents, mixed teams and external suppliers can all participate in the same control model.

The Actor type changes relevant Capability, uncertainty, Evidence and Assurance considerations.

It does not create an independent source of Authority.

The governing relationship remains:

```text
Authority source
→ Authority Grant
→ Actor Assignment
→ bounded exercise
→ Evidence
→ authorized decision
```

and never:

```text
Capability
→ therefore Authority
```

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 001A  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
