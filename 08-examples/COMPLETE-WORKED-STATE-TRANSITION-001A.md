# STATE Engineering — Complete Worked STATE Transition

> **Document:** `08-examples/COMPLETE-WORKED-STATE-TRANSITION-001A.md`
> **Title:** STATE Engineering — Complete Worked STATE Transition
> **Version:** 001A
> **Status:** Current Documentation
> **Created:** 2026-08-13
> **Last modified:** 2026-08-13
> **Author:** Tor-Ståle Hansen
> **Co-authors:** None

## 1. Nature and authority of this example

This document is **illustrative and non-normative**.

It demonstrates one concrete application of existing STATE Engineering semantics. It does not create a new Phase, Transition Gate, Authority Domain, logical Role, Work Product class, Evidence class, Conformance Requirement or actor-specific governance rule.

Where this example and the current normative STATE corpus differ, the normative corpus governs.

The case is deliberately small enough that every transition decision can be inspected end-to-end.

The worked case is self-contained: the baseline, specification, Authority assignments, Candidates, observations, Verification results, Evidence, repair decision, Acceptance decision and Baseline Establishment needed to understand the Transition are included here.

## 2. Case summary

A small Python package contains a manifest parser used to read SHA-256 manifest lines.

The authorized engineering intent is:

> Refactor duplicate SHA-256 validation logic into one private helper without changing public API, accepted input behavior, rejected input behavior, dependencies or path-handling semantics.

The Realization Actor is an LLM coding agent.

The example begins with Authoritative State `B0`, produces failed Candidate `C1`, records a required Verification FAIL, preserves the negative Evidence, repairs from the earliest invalidated phase, produces Candidate `C2`, verifies it successfully, obtains human Acceptance, and explicitly establishes `C2` as new Authoritative State `B1`.

During inspection the LLM discovers a plausible path-traversal hardening improvement. It has the technical capability to implement it. It does not have Authority to change path-handling behavior. The improvement is therefore recorded and refused within this Transition.

## 3. Repository fragment used by the example

The illustrative repository is:

```text
manifest-example/
├── pyproject.toml
├── src/
│   └── manifest.py
└── tests/
    └── test_manifest.py
```

### 3.1 Authoritative baseline `B0`

`src/manifest.py`:

```python
import re

HASH_RE = re.compile(r"^[0-9a-f]{64}$")


def parse_manifest_line(line: str) -> tuple[str, str]:
    digest, separator, path = line.partition("  ")
    if not separator:
        raise ValueError("invalid manifest line")
    if not HASH_RE.fullmatch(digest):
        raise ValueError("invalid digest")
    return digest, path


def validate_digest(value: str) -> bool:
    return bool(HASH_RE.fullmatch(value))
```

`tests/test_manifest.py` contains the baseline behavioral assertions:

```python
import pytest

from manifest import parse_manifest_line, validate_digest


LOWER = "a" * 64
UPPER = "A" * 64


def test_lowercase_digest_is_valid():
    assert validate_digest(LOWER) is True


def test_uppercase_digest_is_rejected():
    assert validate_digest(UPPER) is False


def test_parse_returns_path_verbatim():
    assert parse_manifest_line(f"{LOWER}  ../archive.bin") == (
        LOWER,
        "../archive.bin",
    )


def test_missing_separator_is_rejected():
    with pytest.raises(ValueError, match="invalid manifest line"):
        parse_manifest_line(LOWER)


def test_uppercase_manifest_digest_is_rejected():
    with pytest.raises(ValueError, match="invalid digest"):
        parse_manifest_line(f"{UPPER}  archive.bin")
```

The unusual `../archive.bin` behavior is intentional **for this baseline**. The worked Transition is not authorized to decide whether that historical behavior is good engineering. It is authorized only to preserve it while refactoring digest validation.

## 4. Transition identifiers

| Item | Identifier |
|---|---|
| Transition | `TR-MANIFEST-REF-001` |
| Authoritative Baseline | `B0` |
| First Candidate | `C1` |
| Repaired Candidate | `C2` |
| Resulting Authoritative State | `B1` |
| Boundary-deviation record | `DEV-01` |
| First Verification Record | `VR-C1` |
| Second Verification Record | `VR-C2` |
| Evidence Set for first candidate | `ES-C1` |
| Evidence Set for repaired candidate | `ES-C2` |
| Acceptance Record | `AR-C2` |
| Baseline Establishment Record | `BER-B1` |

These are example-local record identities, not new STATE method identifiers.

## 5. Role / Actor / Capability / Authority assignment

| Logical Role / Authority | Physical Actor | Relevant capability | Granted Authority | Explicitly not granted |
|---|---|---|---|---|
| Intent Authority (`AD-01`) | Human `H1`, product owner | Define desired outcome and acceptance intent | Authorize behavior-preserving refactor objective | Source mutation |
| Architecture Authority (`AD-02`) | Human `H2`, software maintainer | Evaluate module boundaries and API consequences | Preserve public API and architecture constraints | Acceptance of resulting Candidate |
| Transition Authority (`AD-03`) | Human `H2`, software maintainer | Define mutation boundary and escalation conditions | Authorize mutation of `src/manifest.py` only | Change tests, dependencies or path semantics |
| Acceptance Authority (`AD-04`) | Human `H1`, product owner | Decide whether evidence satisfies acceptance basis | ACCEPT / REJECT / REPAIR REQUIRED / INCONCLUSIVE for this Transition | Modify Candidate |
| Specification Role (`LR-01`) | Human `H2` | Convert intent into bounded engineering specification | Produce WP-01 | Acceptance Authority |
| Realization Role (`LR-02`) | LLM coding agent `AI-1` | Read repository, edit Python, run tests, reason about code | Modify `src/manifest.py` inside WP-02 grant | Modify tests, dependencies, public API, path behavior, Authority Grants |
| Verification Role (`LR-03`) | Deterministic `pytest` harness `V1`, interpreted by human `H2` | Execute specified behavioral checks | Produce observations and PASS / FAIL outcomes | Candidate mutation or Acceptance |
| Evidence Stewardship Role (`LR-04`) | Automation `E1` | Preserve diff, test logs, identities and records | Assemble claim-bound Evidence Set | Redefine claims or Acceptance basis |
| Baseline Custodianship Role (`LR-05`) | Human `H2` | Maintain repository baseline identity | Record `B0` and, after Acceptance, establish `B1` | Accept Candidate |
| Assurance Role (`LR-06`) | Human `H2` | Review separation, sufficiency and negative Evidence | Challenge unsupported progression | Rewrite Verification result |

The LLM's ability to edit any file available to its tool environment is **Capability**.

Its Authority is narrower.

> **Capability does not create Authority.**

## 6. Concrete logical Work Products

The example physically consolidates some logical Work Products into this one document, which remains consistent with STATE's logical Work Product model.

### WP-01 — Transition Intent and Specification

**Transition:** `TR-MANIFEST-REF-001`

**Intended outcome:** extract duplicate SHA-256 format checking into one private helper.

**Required invariants:**

1. `parse_manifest_line()` signature remains unchanged.
2. `validate_digest()` signature remains unchanged.
3. Lowercase 64-character hexadecimal digest remains accepted.
4. Uppercase digest remains rejected.
5. Missing double-space separator remains rejected.
6. Path text after the separator remains returned verbatim.
7. No dependency changes.
8. No public symbol is added or removed.

**Non-goals:**

- security hardening of path behavior;
- acceptance of uppercase digests;
- parser redesign;
- dependency replacement;
- test redesign;
- release or deployment.

**Acceptance basis:** required Claims `CL-01` through `CL-07` below shall all be PASS for the accepted Candidate; Evidence shall be bound to the correct Candidate; no unresolved in-boundary deviation may remain.

### WP-02 — Authority Grant

**Grant:** `AG-TR-MANIFEST-REF-001`

**Source:** Human Transition Authority `H2`.

**Actor:** `AI-1`.

**Permitted mutation:** `src/manifest.py`.

**Permitted read scope:** repository files required to understand and verify this bounded refactor.

**Permitted execution:** run existing manifest tests and read their output.

**Constraints:**

- preserve behavior;
- preserve public API;
- do not modify tests;
- do not modify `pyproject.toml`;
- do not add dependencies;
- do not change path-handling semantics;
- stop and escalate if the desired change requires an action outside this boundary.

**Validity:** this Transition only, ending at Acceptance, rejection, cancellation or explicit revocation.

### WP-03 — Actor Assignment

`AI-1` is assigned `LR-02 Realization Role` for `TR-MANIFEST-REF-001`.

Required capability is Python refactoring within one module plus ability to execute existing tests.

Granted Authority is exactly `AG-TR-MANIFEST-REF-001`.

No Architecture, Transition or Acceptance Authority is delegated to `AI-1`.

### WP-04 — Baseline Record

**Baseline:** `B0`.

**Tracked illustrative files:**

- `src/manifest.py` as shown in Section 3.1;
- `tests/test_manifest.py` as shown in Section 3.1;
- `pyproject.toml` unchanged throughout the Transition.

**Authoritative-state rule:** `B0` remains authoritative until G9 completes for an accepted Candidate.

### WP-05 — Transition Record

The central Transition Record is:

```text
TR-MANIFEST-REF-001
baseline: B0
specification: WP-01
authority: AG-TR-MANIFEST-REF-001
realization actor: AI-1
candidate 1: C1
verification 1: VR-C1
evidence 1: ES-C1
acceptance decision after C1: REPAIR REQUIRED
resume point: P4
candidate 2: C2
verification 2: VR-C2
evidence 2: ES-C2
acceptance decision after C2: ACCEPT
baseline establishment: BER-B1
resulting authoritative state: B1
```

### WP-06 — Verification Record

The Verification Role evaluates:

| Claim | Required result |
|---|---|
| `CL-01` | Public function signatures unchanged |
| `CL-02` | Lowercase digest remains accepted |
| `CL-03` | Uppercase digest remains rejected |
| `CL-04` | Missing separator remains rejected |
| `CL-05` | Path text remains returned verbatim |
| `CL-06` | Only `src/manifest.py` is mutated by Realization |
| `CL-07` | Dependencies unchanged |

Two concrete Verification Records, `VR-C1` and `VR-C2`, are shown later.

### WP-07 — Evidence Set

Each candidate has its own Evidence Set.

`ES-C1` contains:

- Candidate identity `C1`;
- source diff `B0 → C1`;
- test execution log for `C1`;
- claim-to-result table `VR-C1`;
- negative Evidence for `CL-03`;
- `DEV-01` boundary discovery.

`ES-C2` contains:

- Candidate identity `C2`;
- repair diff `C1 → C2`;
- cumulative diff `B0 → C2`;
- second test execution log;
- claim-to-result table `VR-C2`;
- preserved reference to the earlier `C1` failure;
- `DEV-01` showing that the out-of-bound improvement remained unimplemented.

### WP-08 — Acceptance Record

`AR-C2` records:

- Candidate: `C2`;
- Acceptance basis: all required `CL-01` through `CL-07` PASS;
- Evidence Set: `ES-C2`;
- unresolved in-boundary deviation: none;
- known out-of-bound discovery: `DEV-01`, not part of accepted Candidate;
- decision: `ACCEPT`;
- Acceptance Authority: human `H1`.

### WP-09 — Baseline Establishment Record

`BER-B1` records:

- prior Authoritative State: `B0`;
- accepted Candidate: `C2`;
- Acceptance Record: `AR-C2`;
- new Authoritative State: `B1`;
- establishment performed by Baseline Custodian `H2` after G8 ACCEPT;
- `B0` ceases to be current only after G9 passes.

### WP-10 — Release Record

**Not applicable.**

This Transition establishes a new authoritative development baseline only. It does not authorize deployment, distribution or release.

### WP-11 — Deviation and Escalation Record

`DEV-01`:

```text
discovered_at: P3
discovered_by: AI-1
condition: parse_manifest_line returns path text such as "../archive.bin" verbatim
possible_improvement: reject absolute paths and parent-directory traversal
technical_capability: AI-1 is capable of implementing the hardening
current_authority: behavior-preserving refactor only
boundary_classification: OUTSIDE TRANSITION BOUNDARY
action: DO NOT IMPLEMENT
escalation: record for separate Intent / Architecture / Transition decision
effect_on_current_transition: none, because current acceptance basis requires preservation of existing path behavior
```

`DEV-01` is not a silent security waiver. It is an explicit statement that the discovered issue requires a different authorized Transition if the owner chooses to change that behavior.

## 7. P0 — Establish Authority and Baseline

### Inputs

- refactoring need from `H1`;
- current repository state `B0`;
- authority source from humans `H1` and `H2`.

### Activities

`H2` confirms `B0` as the current Authoritative State.

`H1` establishes the intended outcome: behavior-preserving refactor only.

`H2` issues `AG-TR-MANIFEST-REF-001` and assigns `AI-1` to the Realization Role.

### Concrete output

WP-02, WP-03, WP-04 and initial WP-05 are established exactly as recorded in Section 6.

### G0 — Authority & Baseline Gate

**Outcome: PASS**

Basis:

- Baseline identity is explicit: `B0`;
- Authority source is explicit;
- Realization Authority is bounded;
- Acceptance Authority remains human and separate from Realization.

`AI-1` may proceed to specification work but cannot decide its own Acceptance.

## 8. P1 — Specify Intent

`H2` converts the human intent into WP-01.

The crucial phrase is **behavior-preserving**.

The Acceptance basis is not “tests look reasonable” and is not “the LLM believes the refactor is equivalent”.

The Acceptance basis is the explicit set `CL-01` through `CL-07`.

### G1 — Specification Gate

**Outcome: PASS**

The intended change, invariants, non-goals and Acceptance basis are explicit enough to distinguish allowed refactoring from behavior change.

## 9. P2 — Define Transition Boundary

The authorized mutation boundary is:

```text
MAY WRITE:
  src/manifest.py

MAY READ:
  repository implementation and verification context needed for this Transition

MAY EXECUTE:
  existing manifest verification tests

SHALL NOT WRITE:
  tests/test_manifest.py
  pyproject.toml
  any other repository file

SHALL NOT CHANGE:
  public API
  accepted/rejected digest behavior
  path-handling behavior
  dependency set

ESCALATE IF:
  a useful change requires any forbidden mutation or behavior change
```

### G2 — Boundary Gate

**Outcome: PASS**

A proposed action can be classified as inside, outside or uncertain relative to the grant.

## 10. P3 — Inspect Baseline and Establish Context

`AI-1` reads `src/manifest.py` and the existing tests.

It confirms duplicate SHA-256 validation in:

- `parse_manifest_line()`;
- `validate_digest()`.

It also notices that the parser returns `../archive.bin` unchanged.

### Boundary discovery

`AI-1` reasons that rejecting parent-directory traversal could improve security.

It has enough Python capability and repository access to implement that improvement immediately.

It does **not** do so.

Instead, it creates `DEV-01` and reports:

> The path-hardening change is technically feasible but outside the authorized behavior-preserving Transition Boundary. I will not implement it in this Transition.

This is the required boundary refusal.

The discovery does not expand the Transition.

### G3 — Readiness Gate

**Outcome: PASS**

Enough reliable context exists to perform the bounded refactor. The path discovery does not invalidate the current specification because preservation of current path behavior is an explicit invariant.

## 11. P4 — Produce Candidate `C1`

`AI-1` performs the authorized refactor.

Candidate `C1` is:

```python
import re

HASH_RE = re.compile(r"^[0-9a-f]{64}$")


def _is_sha256(value: str) -> bool:
    return bool(HASH_RE.fullmatch(value.lower()))


def parse_manifest_line(line: str) -> tuple[str, str]:
    digest, separator, path = line.partition("  ")
    if not separator:
        raise ValueError("invalid manifest line")
    if not _is_sha256(digest):
        raise ValueError("invalid digest")
    return digest, path


def validate_digest(value: str) -> bool:
    return _is_sha256(value)
```

The refactor is structurally attractive but semantically wrong.

The call to `.lower()` silently broadens accepted behavior.

`AI-1` does not possess Authority to decide that this widening is desirable.

### G4 — Candidate Identity Gate

**Outcome: PASS**

`C1` is identifiable and reconstructable from `B0`.

Passing G4 does not mean `C1` is correct or acceptable.

## 12. P5 — Execute and Observe Candidate `C1`

The Verification Actor executes the existing tests.

Observed output:

```text
tests/test_manifest.py::test_lowercase_digest_is_valid PASSED
tests/test_manifest.py::test_uppercase_digest_is_rejected FAILED
tests/test_manifest.py::test_parse_returns_path_verbatim PASSED
tests/test_manifest.py::test_missing_separator_is_rejected PASSED
tests/test_manifest.py::test_uppercase_manifest_digest_is_rejected FAILED

2 failed, 3 passed
```

No test is weakened, deleted or rewritten.

### G5 — Observation Gate

**Outcome: PASS**

Execution occurred under the required conditions and the observations, including failures, are preserved.

## 13. P6 — Verify Claims for Candidate `C1`

`VR-C1` is:

| Claim | Method | Observation | Result | Limitation |
|---|---|---|---|---|
| `CL-01` signatures unchanged | source comparison | signatures unchanged | PASS | example checks named public functions only |
| `CL-02` lowercase accepted | existing test | passed | PASS | scoped to 64 lowercase `a` fixture |
| `CL-03` uppercase rejected | existing tests | uppercase accepted by `C1` | **FAIL** | none material |
| `CL-04` missing separator rejected | existing test | passed | PASS | specified malformed case |
| `CL-05` path returned verbatim | existing test | `../archive.bin` unchanged | PASS | this is preservation, not endorsement |
| `CL-06` mutation scope | diff inspection | only `src/manifest.py` changed | PASS | verification artifacts external |
| `CL-07` dependencies unchanged | `pyproject.toml` identity check | unchanged | PASS | none material |

### Required G6 Verification FAIL demonstration

**G6 Verification FAIL: `CL-03 = FAIL` for Candidate `C1`.**

The phrase above describes the required claim-level Verification outcome produced at P6/G6.

The logical **G6 process gate** nevertheless has outcome **PASS**, because all required claims have explicit outcomes, methods, Evidence references and visible limitations.

This distinction is intentional:

> G6 process completeness does not convert a failing engineering claim into PASS.

The negative result remains `FAIL`.

No false green occurs.

## 14. P7 — Assemble Evidence for Candidate `C1`

`E1` assembles `ES-C1`.

The failed test output is preserved.

The Evidence Set does not delete `CL-03` and does not redefine the Acceptance basis.

`DEV-01` is also preserved so the later decision can see that an out-of-bound improvement was discovered and intentionally not implemented.

### G7 — Evidence Gate

**Outcome: PASS**

The Evidence is decision-ready even though it supports a negative decision for the current Candidate.

Negative Evidence is still Evidence.

## 15. P8 — Decide Acceptance for Candidate `C1`

Human Acceptance Authority `H1` reviews:

- `VR-C1`;
- `ES-C1`;
- the unchanged Acceptance basis;
- `DEV-01`.

Because required Claim `CL-03` is FAIL, the unchanged Acceptance basis cannot support ACCEPT.

`H1` records:

```text
candidate: C1
decision: REPAIR REQUIRED
reason: required claim CL-03 is FAIL
acceptance_basis_change: NONE
verification_rewrite: NONE
boundary_change: NONE
```

### G8 — Acceptance Gate

**Outcome: REPAIR REQUIRED**

Acceptance Authority does not weaken the requirement that uppercase digests remain rejected.

## 16. Repair analysis and earliest-invalidated-phase resumption

The failure is diagnosed.

What remains valid:

- P0 Authority and Baseline;
- P1 intent and Acceptance basis;
- P2 Transition Boundary;
- P3 implementation context.

What is invalid:

- the P4 Candidate implementation.

The earliest invalidated control condition is therefore **P4 — Produce Candidate**.

The Transition does not restart at P0 because Authority did not change.

It does not restart at P1 because intent did not change.

It does not restart at P2 because the boundary did not change.

It does not resume merely at P8 because the Candidate itself must be repaired.

> **Resume Point: P4.**

## 17. Repair at P4 — Produce Candidate `C2`

`AI-1` removes the unauthorized behavior widening while preserving the private helper refactor.

Candidate `C2` is:

```python
import re

HASH_RE = re.compile(r"^[0-9a-f]{64}$")


def _is_sha256(value: str) -> bool:
    return bool(HASH_RE.fullmatch(value))


def parse_manifest_line(line: str) -> tuple[str, str]:
    digest, separator, path = line.partition("  ")
    if not separator:
        raise ValueError("invalid manifest line")
    if not _is_sha256(digest):
        raise ValueError("invalid digest")
    return digest, path


def validate_digest(value: str) -> bool:
    return _is_sha256(value)
```

`DEV-01` remains unresolved by design and remains outside the Candidate change.

### G4 — Candidate Identity Gate, second pass

**Outcome: PASS**

`C2` is a new Candidate identity and is distinguishable from failed Candidate `C1`.

Evidence from `C1` is not silently relabeled as evidence for `C2`.

## 18. P5 — Execute and Observe Candidate `C2`

Second execution:

```text
tests/test_manifest.py::test_lowercase_digest_is_valid PASSED
tests/test_manifest.py::test_uppercase_digest_is_rejected PASSED
tests/test_manifest.py::test_parse_returns_path_verbatim PASSED
tests/test_manifest.py::test_missing_separator_is_rejected PASSED
tests/test_manifest.py::test_uppercase_manifest_digest_is_rejected PASSED

5 passed
```

### G5 — Observation Gate, second pass

**Outcome: PASS**

Observations are bound to `C2`.

## 19. P6 — Verify Claims for Candidate `C2`

`VR-C2`:

| Claim | Result | Evidence |
|---|---|---|
| `CL-01` public signatures unchanged | PASS | `B0 → C2` source comparison |
| `CL-02` lowercase digest accepted | PASS | second test log |
| `CL-03` uppercase digest rejected | PASS | second test log |
| `CL-04` missing separator rejected | PASS | second test log |
| `CL-05` path returned verbatim | PASS | second test log |
| `CL-06` only authorized source mutated | PASS | cumulative diff |
| `CL-07` dependencies unchanged | PASS | `pyproject.toml` identity |

### G6 — Verification Gate, second pass

**Outcome: PASS**

All required claims have explicit PASS outcomes and visible verification basis.

The earlier `C1` FAIL remains preserved in transition history.

## 20. P7 — Assemble Evidence for Candidate `C2`

`ES-C2` binds:

1. Baseline `B0`;
2. Candidate `C2`;
3. cumulative source diff;
4. second execution log;
5. `VR-C2`;
6. preserved `VR-C1` failure history;
7. `DEV-01`;
8. actor and Authority records.

The Evidence Set makes clear that the path-hardening improvement was not included in `C2`.

### G7 — Evidence Gate, second pass

**Outcome: PASS**

Evidence is sufficient for the requested bounded Acceptance decision.

## 21. P8 — Decide Acceptance for Candidate `C2`

Human Acceptance Authority `H1` reviews the unchanged Acceptance basis.

All required claims are PASS.

The only open discovery, `DEV-01`, is explicitly outside the current Transition and did not change the accepted claims.

`AR-C2`:

```text
candidate: C2
acceptance_basis: CL-01 through CL-07
verification_record: VR-C2
evidence_set: ES-C2
known_out_of_boundary_discovery: DEV-01
decision: ACCEPT
acceptance_authority: H1
authority_basis_changed: NO
```

### G8 — Acceptance Gate, second pass

**Outcome: ACCEPT**

The decision is human-authorized.

The LLM does not accept its own work.

`C2` is now accepted but is still not the Authoritative State.

## 22. P9 — Establish New Baseline

Baseline Custodian `H2` verifies that the accepted Candidate identity in `AR-C2` is exactly `C2`.

`BER-B1` is completed:

```text
prior_authoritative_state: B0
accepted_transition: TR-MANIFEST-REF-001
accepted_candidate: C2
acceptance_record: AR-C2
new_authoritative_state: B1
established_by: H2
```

### G9 — Baseline Establishment Gate

**Outcome: PASS**

Only now does `B1` become the new Authoritative State.

`B0` remained authoritative during:

- production of `C1`;
- failure of `C1`;
- repair;
- production and successful verification of `C2`;
- Acceptance of `C2`.

This preserves Candidate-before-Authority.

## 23. Complete P0–P9 / G0–G9 trace

| Phase | Gate | Result | Principal concrete output |
|---|---|---|---|
| P0 Establish Authority and Baseline | G0 | PASS | `AG-TR-MANIFEST-REF-001`, `B0`, actor assignments |
| P1 Specify Intent | G1 | PASS | WP-01 with `CL-01`–`CL-07` |
| P2 Define Transition Boundary | G2 | PASS | write/read/execute boundary |
| P3 Inspect Baseline and Establish Context | G3 | PASS | implementation context + `DEV-01` refusal |
| P4 Produce Candidate | G4 | PASS | `C1` |
| P5 Execute and Observe | G5 | PASS | first test log |
| P6 Verify Claims | G6 | process PASS; **claim FAIL** | `VR-C1`, `CL-03 = FAIL` |
| P7 Assemble Evidence | G7 | PASS | `ES-C1`, negative Evidence preserved |
| P8 Decide Acceptance | G8 | REPAIR REQUIRED | repair decision |
| P4 repair resume | G4 | PASS | `C2` |
| P5 second execution | G5 | PASS | second test log |
| P6 second Verification | G6 | PASS | `VR-C2`, all required claims PASS |
| P7 second Evidence assembly | G7 | PASS | `ES-C2` |
| P8 second Acceptance | G8 | ACCEPT | `AR-C2` |
| P9 Establish New Baseline | G9 | PASS | `BER-B1`, new Authoritative State `B1` |

## 24. Boundary refusal — why capability did not create Authority

The most tempting extra change in the case is path hardening.

The LLM had:

- the implementation skill;
- repository read access;
- source write capability;
- enough context to design the change.

It did **not** have:

- Intent Authority to redefine desired behavior;
- Architecture Authority to redefine path semantics;
- Transition Authority to expand the mutation boundary;
- Acceptance Authority to decide that a broader change was acceptable.

Therefore the correct STATE action was:

```text
DISCOVER
→ CLASSIFY OUTSIDE BOUNDARY
→ RECORD
→ REFUSE IMPLEMENTATION
→ ESCALATE FOR A SEPARATE AUTHORIZED DECISION
```

Not:

```text
DISCOVER
→ "GOOD IDEA"
→ IMPLEMENT BECAUSE THE TOOL CAN
```

This is the operational meaning of:

> **Capability does not create Authority.**

## 25. Failure semantics — why the first Candidate was useful

`C1` was not hidden, relabeled or silently replaced.

Its failure established useful information:

- the extracted helper was not behavior-preserving;
- `.lower()` was the invalidating implementation choice;
- the specification itself did not need to change;
- the boundary did not need to change;
- Authority did not need to change;
- repair could therefore resume at P4.

The Verification FAIL narrowed the repair.

It did not justify weaker Verification.

## 26. Why Acceptance did not establish the baseline

After G8 ACCEPT for `C2`, the Transition still had one logical act remaining.

P9 established the accepted Candidate as `B1`.

This preserves the distinction:

```text
Production ≠ Verification
Verification ≠ Evidence
Evidence ≠ Acceptance
Acceptance ≠ Baseline Establishment
```

Even a fully capable automated pipeline may combine physical execution of these activities, but the logical distinctions remain reconstructable.

## 27. Example outcome

The worked example demonstrates:

- all P0 through P9 phases;
- every G0 through G9 gate;
- explicit human and synthetic Actors;
- Role / Actor / Capability / Authority separation;
- concrete WP-01 through WP-09 and WP-11 content;
- explicit WP-10 non-applicability;
- a bounded Transition;
- an explicit Acceptance basis;
- claim-bound Evidence;
- a first Verification FAIL at G6;
- preservation of negative Evidence;
- REPAIR REQUIRED;
- earliest-invalidated-phase resumption at P4;
- a second Verification pass;
- human-authorized ACCEPT;
- explicit P9 baseline establishment;
- an AI-discovered out-of-boundary improvement;
- explicit refusal to implement that improvement;
- proof by action that technical capability did not create Authority.

The final state is:

```text
B0 — old Authoritative State
C1 — failed Candidate, never authoritative
C2 — repaired and accepted Candidate
B1 — new Authoritative State only after P9/G9
DEV-01 — separately recorded out-of-boundary hardening opportunity
```

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-SA 4.0  
Version: 001A  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
