# The STATE Cycle

> **Document:** `03-how-logical/01-the-state-cycle.md`  
> **Title:** The STATE Cycle  
> **Version:** 0.1  
> **Status:** Working Draft  
> **Created:** 2026-08-11  
> **Last modified:** 2026-08-11  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None

The canonical STATE cycle is the logical control sequence through which an authoritative system state may become another authoritative system state.

## Phase 0 — Establish Authority

Identify the authoritative system, baseline and governing requirements.

**Output:** Authoritative Baseline.

## Phase 1 — Specify Intent

State what is intended to become true, what constraints apply and what constitutes an acceptable result.

**Output:** Authorized Change Specification.

## Phase 2 — Define the Transition Boundary

Define what the transition may affect and what remains outside authorized scope.

**Output:** Authorized Transition Boundary.

## Phase 3 — Perform Bounded Inspection

Acquire sufficient implementation context to act correctly without replacing implementation with unbounded analysis.

**Output:** Implementation Context.

## Phase 4 — Produce the Candidate

Perform the authorized transformation.

**Output:** Candidate State.

## Phase 5 — Execute and Observe

Build, execute, analyze or otherwise exercise the candidate as required by the claims being evaluated.

**Output:** Execution Evidence.

## Phase 6 — Verify

Evaluate the candidate against specification, invariants, contracts, security-relevant properties and regression requirements.

**Output:** Verification Result.

## Phase 7 — Assemble Evidence

Bind the relevant observations, identities and verification results to the candidate and baseline.

**Output:** Evidence Package or equivalent evidence record.

## Phase 8 — Accept, Reject or Require Repair

An authorized decision process determines whether the candidate may become authoritative.

Valid outcomes include:

- **ACCEPT**
- **REJECT**
- **REPAIR REQUIRED**
- **INCONCLUSIVE**

**Output:** Acceptance Decision.

## Phase 9 — Establish the New Baseline

If accepted, identify the resulting state and establish it as the next authoritative baseline.

**Output:** New Authoritative State.

## Canonical flow

```text
AUTHORITATIVE STATE
        ↓
SPECIFY
        ↓
BOUND
        ↓
INSPECT
        ↓
PRODUCE
        ↓
EXECUTE
        ↓
VERIFY
        ↓
EVIDENCE
        ↓
DECIDE
    ┌───┴──────────────┐
 ACCEPT          REJECT / REPAIR /
    │             INCONCLUSIVE
    ↓
NEW AUTHORITATIVE STATE
```

A failed candidate does not become a baseline by default.

The previous authoritative state remains authoritative until an accepted transition establishes a replacement.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.1  
Initial publication: 2026-08-11  
Last modified: 2026-08-11
