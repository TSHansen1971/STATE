# STATE Engineering — Validation Protocol

> **Document:** `VALIDATION-PROTOCOL-001A.md`
> **Title:** STATE Engineering — Validation Protocol
> **Version:** 001A
> **Status:** Current Documentation
> **Created:** 2026-08-13
> **Last modified:** 2026-08-13
> **Author:** Tor-Ståle Hansen
> **Co-authors:** None

## 1. Purpose

This protocol defines a repeatable way to evaluate STATE Engineering in real engineering Transitions without confusing an experience report with normative truth.

It is an empirical validation protocol.

It is not a new Conformance Requirement and does not modify the normative method.

## 2. Validation principle

Evidence shall be interpreted only at the level actually supported by the case.

A successful case does not prove universal validity.

A failed case does not automatically invalidate the architecture.

A validation case may instead reveal:

- a supported control claim;
- a partially supported claim;
- a not-supported claim;
- an inconclusive basis;
- a newly observed issue;
- a case-specific limitation;
- a protocol defect;
- an implementation or documentation ambiguity.

## 3. Result vocabulary

Each evaluated dimension shall use one of:

- `supported`;
- `partially supported`;
- `not supported`;
- `inconclusive`;
- `newly observed issue`.

The result shall be accompanied by Evidence and limitations.

No numerical score silently overrides this vocabulary.

## 4. Case identity

Every validation case shall record:

```text
validation_case_identity:
date:
practitioner_or_team:
domain:
transition_class:
baseline_identity:
candidate_identity_or_identities:
state_specification_version:
tailoring_profile_or_decision:
actor_arrangement:
authority_arrangement:
execution_environment:
case_start:
case_end:
```

Personal or sensitive information should be minimized to what the validation claim actually requires.

## 5. Pre-case claims

Before execution, state which STATE claims the case is capable of testing.

Example:

```text
claim V-01:
  STATE makes the active Transition Boundary understandable to the practitioner.

claim V-02:
  STATE makes Capability / Authority separation operationally usable.

claim V-03:
  earliest-invalidated-phase repair avoids unnecessary restart while preserving control.
```

A case shall not be described as validating claims that were not meaningfully observable.

## 6. Evaluation dimensions

### 6.1 Transition completeness

Can the case reconstruct the required P0–P9 control progression at the Tailored physical depth?

Record missing, compressed and repeated elements.

### 6.2 Boundary control

Was the active Transition Boundary understandable?

Were out-of-boundary discoveries classified, refused or escalated correctly?

### 6.3 Authority clarity

Could practitioners distinguish technical Capability, access, Role and legitimate Authority?

Were decision rights ambiguous at any point?

### 6.4 Actor substitution

Where an Actor was substituted or could reasonably have been substituted, did the logical control semantics remain stable?

Record Capability, Authority and Evidence differences introduced by substitution.

### 6.5 Evidence sufficiency

Was the Evidence available adequate for the authorized Acceptance basis?

Record missing Evidence, excessive Evidence and any sufficiency ambiguity.

### 6.6 Verification effectiveness

Did Verification detect incorrect, incomplete or unsupported claims?

Did PASS remain bounded to the actual claim and method?

Were FAIL and INCONCLUSIVE visible?

### 6.7 Repair-loop effectiveness

When failure occurred, did repair resume from the earliest invalidated control condition?

Record whether the repair loop preserved valid upstream work and repeated invalidated downstream controls.

### 6.8 Traceability

Could a reviewer reconstruct the relation among Baseline, Specification, Authority, Actor Assignment, Candidate, Verification, Evidence, Acceptance and new Baseline?

### 6.9 Tailoring effectiveness

Did Tailoring reduce unnecessary representation without Control Deletion?

Record where Tailoring was too heavy, too light or ambiguous.

### 6.10 Operator burden

Record practitioner burden attributable to STATE control activity.

Distinguish method-control burden from ordinary engineering work.

Use both qualitative observations and elapsed effort where measurable.

### 6.11 Elapsed control effort

Record time spent specifically on:

- Authority / scope establishment;
- records and traceability;
- Verification planning;
- Evidence assembly;
- Acceptance preparation;
- repair / resumption control.

Do not treat elapsed time alone as method quality.

### 6.12 Defects prevented or detected

Record defects, boundary violations, unsupported assumptions or provenance gaps prevented or detected by STATE controls where there is a defensible causal observation.

Avoid claiming prevention where only detection is observed.

### 6.13 Unauthorized-action detection

Record any action attempted, proposed or performed outside Authority.

Classify whether STATE controls prevented, detected late or failed to detect the action.

### 6.14 Practitioner ambiguity

Record terms, boundaries, Roles, Work Products, gates or decisions that practitioners found unclear.

Ambiguity is Evidence for documentation or method-development backlog, not something to hide from the case report.

## 7. Evidence-capture rule

For every dimension, preserve:

```text
dimension:
observation:
evidence_reference:
result:
limitations:
alternative_explanation:
new_issue_reference:
```

Negative Evidence is retained.

The validation report shall not be edited into a success narrative by deleting inconvenient observations.

## 8. Independence and observer effects

Where feasible, record whether the evaluator:

- performed the Transition;
- designed the Tailoring;
- held Authority;
- performed Verification;
- reviewed the Evidence after completion.

The protocol does not require full organizational independence for every pilot.

It requires that dependence and possible observer effects remain visible.

## 9. Quantitative measurements

Quantitative data may include:

- elapsed control effort;
- number of repair loops;
- number of out-of-boundary discoveries;
- number of unauthorized actions proposed or attempted;
- number of defects detected;
- number of INCONCLUSIVE claims;
- Evidence item count;
- practitioner-reported ambiguity count.

These values are descriptive unless a separately defined study design supports stronger inference.

## 10. Post-case analysis

The case report shall distinguish:

1. evidence about the engineering Transition itself;
2. evidence about STATE's usability;
3. evidence about STATE's control effectiveness;
4. evidence about the chosen Tailoring;
5. evidence about documentation quality;
6. evidence that is too weak for a conclusion.

## 11. Case conclusion

A validation case conclusion shall include:

```text
claims_evaluated:
claims_not_observable:
supported:
partially_supported:
not_supported:
inconclusive:
newly_observed_issues:
case_specific_limitations:
method_backlog_candidates:
protocol_improvement_candidates:
```

## 12. No universalization from one case

One case can demonstrate that a STATE control was usable under that case's conditions.

It cannot by itself establish universal method validity, organization-scale scalability or sector-wide effectiveness.

Broader claims require broader and appropriately independent Evidence.

## 13. Feedback control

New issues are fed into method development as Candidates for investigation.

A validation finding does not mutate the normative method automatically.

Normative change still requires legitimate owner Authority, bounded method-development work, Verification and Acceptance.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 001A  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
