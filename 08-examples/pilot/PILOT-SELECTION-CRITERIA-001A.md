# STATE Pilot — Selection Criteria

> **Document:** `08-examples/pilot/PILOT-SELECTION-CRITERIA-001A.md`
> **Title:** STATE Pilot — Selection Criteria
> **Version:** 001A
> **Status:** Current Documentation
> **Created:** 2026-08-13
> **Last modified:** 2026-08-13
> **Author:** Tor-Ståle Hansen
> **Co-authors:** None

## Selection objective

Choose a case large enough to exercise meaningful STATE controls and small enough to observe end-to-end.

## Required characteristics

A preferred pilot has:

- an identifiable pre-Transition Baseline;
- a bounded desired change;
- identifiable Authority;
- observable Actor Assignment;
- a definable Transition Boundary;
- concrete Candidate output;
- claim-bound Verification;
- preservable Evidence;
- an explicit Acceptance decision;
- observable P9 Baseline Establishment or explicit non-establishment;
- practical access to the practitioner or team for post-case assessment.

## Prefer

Prefer cases with one or more of:

- delegated realization;
- human/AI or automation involvement;
- meaningful boundary choices;
- realistic possibility of failure/repair;
- provenance requirements;
- non-trivial Verification.

## Avoid for the first pilot

Avoid cases whose primary difficulty is:

- organization-wide transformation;
- very long elapsed duration;
- inaccessible Evidence;
- confidential context that makes independent inspection impossible;
- a Transition Boundary too broad to reconstruct;
- an outcome that cannot be evaluated within the pilot window.

## Candidate pilot classes

- bounded software change;
- documentation-controlled engineering change;
- AI-assisted refactoring;
- configuration change;
- controlled automation deployment.

## Selection record

```text
pilot_candidate:
transition_class:
why_bounded:
observable_baseline:
observable_candidate:
authority_access:
evidence_access:
expected_duration:
material_risks:
reason_selected_or_rejected:
```

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-SA 4.0  
Version: 001A  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
