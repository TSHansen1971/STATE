# STATE Pilot — Feedback-to-Backlog Procedure

> **Document:** `08-examples/pilot/FEEDBACK-TO-BACKLOG-PROCEDURE-001A.md`
> **Title:** STATE Pilot — Feedback-to-Backlog Procedure
> **Version:** 001A
> **Status:** Current Documentation
> **Created:** 2026-08-13
> **Last modified:** 2026-08-13
> **Author:** Tor-Ståle Hansen
> **Co-authors:** None

## Purpose

Convert pilot observations into controlled development Candidates without allowing empirical feedback to mutate the method automatically.

## Procedure

### 1. Preserve the observation

Record the raw observation and Evidence before interpretation.

### 2. Classify the issue

Use `PILOT-ISSUE-CLASSIFICATION-001A.md`.

### 3. Bound the claim

State exactly what the case supports and what it does not support.

### 4. Determine disposition

One of:

- no method action;
- documentation clarification Candidate;
- Tailoring guidance Candidate;
- validation-protocol improvement Candidate;
- operational example/template Candidate;
- normative method-change Candidate;
- additional evidence required;
- INCONCLUSIVE / hold.

### 5. Create a backlog Candidate

```text
candidate_backlog_item:
source_pilot:
source_issue:
claim:
evidence_reference:
proposed_scope:
normative_change_possible: YES / NO
owner_authority_required:
dependencies:
```

### 6. Preserve Authority

A pilot finding does not authorize a normative method change.

Normative change requires a separately authorized method-development Transition.

### 7. Trace resolution

If accepted for future work, preserve traceability:

```text
PILOT OBSERVATION
→ ISSUE
→ BACKLOG CANDIDATE
→ AUTHORIZED WORK PACKAGE
→ CANDIDATE CHANGE
→ VERIFICATION
→ OWNER ACCEPTANCE
```

No result is silently upgraded because it is inconvenient to the release plan.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-SA 4.0  
Version: 001A  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
