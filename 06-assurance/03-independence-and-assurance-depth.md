# Independence and Assurance Depth

> **Document:** `06-assurance/03-independence-and-assurance-depth.md`  
> **Title:** Independence and Assurance Depth  
> **Version:** 0.11  
> **Status:** Normative Specification
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


Independence is one method for improving Assurance by reducing the chance that the same failure source controls production, Verification, evidence and decision.

It is not an end in itself.

## 1. Independence principle

> **Useful independence is independence from a relevant failure source, not merely separation by Actor count or organizational label.**

## 2. Existing Verification Independence Dimensions

The Verification Model already defines:

- VI-01 Actor Independence;
- VI-02 Method Independence;
- VI-03 Tool Independence;
- VI-04 Environment Independence;
- VI-05 Organizational Independence;
- VI-06 Decision Independence.

The Assurance layer composes these dimensions rather than replacing them.

## 3. Assurance Independence Patterns

STATE defines eight Assurance Independence Patterns.

### AIP-01 — Independent Actor Challenge

A different Actor challenges the claim, evidence or decision basis.

Useful when individual judgment or implementation assumptions are material.

### AIP-02 — Independent Method Challenge

A different Verification or analytical method evaluates the same or related claim.

Useful where one method has known blind spots.

### AIP-03 — Independent Tool Challenge

A materially different tool checks the output or conclusion.

Useful where producer and verifier otherwise share one implementation failure source.

### AIP-04 — Independent Environment Challenge

Verification is repeated or challenged in a distinct relevant environment.

Useful for environment-sensitive claims.

### AIP-05 — Independent Data / Oracle Challenge

The conclusion is challenged using a different reference dataset, oracle, test source or expected-output basis.

Useful where the original oracle may be wrong.

### AIP-06 — Organizational Challenge

A separate organizational unit, supplier or independent party challenges the basis.

Useful where incentive, hierarchy or organizational common cause is material.

### AIP-07 — Decision Separation

Acceptance or Release decision is exercised independently from Candidate production where consequence justifies it.

### AIP-08 — Adversarial Challenge

An Actor or method deliberately searches for counterexamples, boundary failures, misuse paths or unsupported assumptions.

Useful especially for security, failure behavior and high-uncertainty claims.

## 4. False independence

Apparent independence may be weak where challengers share:

- the same underlying model;
- the same prompt or context;
- the same source data;
- the same test oracle;
- the same tool;
- the same environment;
- the same organizational incentive;
- the same hidden assumption.

Example:

```text
Agent A reviews Agent B
but both use:
same model
same context
same tools
same oracle

Actor labels differ
common-cause basis may not
```

## 5. Independence depth

STATE does not prescribe universal separation.

The selected independence depth should correspond to:

- consequence of error;
- uncertainty;
- security relevance;
- reversibility;
- common-cause risk;
- autonomy;
- organizational distribution;
- provenance need.

## 6. Assurance Depth

**Assurance Depth** is the selected strength of evaluation, challenge, evidence and independence required to justify confidence for an Assurance Objective.

It is continuous and contextual.

STATE does not define mandatory maturity levels or a universal numeric Assurance Level.

## 7. Assurance Depth dimensions

STATE defines ten Assurance Depth Dimensions.

### ADD-01 — Claim Precision Depth

How precisely claims and decision scope must be specified.

### ADD-02 — Verification Depth

How broad, diverse and rigorous Verification must be.

### ADD-03 — Evidence Depth

How strong identity, integrity, provenance and preservation must be.

### ADD-04 — Independence Depth

How many and which common-cause dimensions require separation or alternate challenge.

### ADD-05 — Environment Control Depth

How tightly hardware, software, dependencies, external services and mutable state must be controlled.

### ADD-06 — Reproducibility Depth

How strongly results must be repeatable or independently corroborated.

### ADD-07 — Security Challenge Depth

How deeply security boundaries, misuse, privilege and failure behavior must be challenged.

### ADD-08 — Provenance Depth

How completely source, transformation, Actor, environment, evidence and decision lineage must be reconstructed.

### ADD-09 — Failure / Recovery Depth

How much failure injection, recovery, rollback or interruption behavior must be demonstrated.

### ADD-10 — Decision Review Depth

How much independent or multi-step scrutiny is required before Acceptance, Baseline Establishment or Release.

## 8. Proportional strengthening

Assurance may be strengthened selectively.

Example:

```text
ordinary functional claims
    → moderate Verification

security-boundary claim
    → stronger independent challenge

release-provenance claim
    → stronger artifact identity and provenance
```

The whole Transition need not become equally heavy.

## 9. Assurance Debt

**Assurance Debt** is a known unresolved weakness in the trust basis that remains visible for future action.

Examples:

- environment cannot yet be reproduced;
- one supporting claim relies on a single tool;
- supplier provenance is incomplete;
- one non-required claim remains INCONCLUSIVE.

Assurance Debt is not permission to accept a failed Required Claim.

Where the weakness blocks a Required Claim or required Assurance Sufficiency Property, the correct conclusion remains INSUFFICIENT or INCONCLUSIVE.

## 10. Assurance Debt handling

Where Assurance Debt is permitted by the governing Acceptance basis, it should identify:

- weakness;
- scope;
- consequence;
- rationale for deferral;
- responsible authority;
- trigger or intended resolution.

The weakness remains visible.

## 11. No independence theater

Adding reviewers, committees, agents or approvals without materially challenging the relevant failure source is **Independence Theater**.

It increases process cost without necessarily increasing Assurance.

## 12. No assurance by volume

Large evidence sets, many tests or many reviewers are not independently meaningful metrics of Assurance.

Quality depends on relevance to the claim and failure model.

## 13. Canonical Independence and Depth rules

> **Useful independence is independence from the relevant failure source.**

> **Actor count is not a proxy for independence.**

> **Assurance Depth is proportional and claim-relative, not a maturity level.**

> **Selective strengthening is permitted and encouraged where only some claims require deeper Assurance.**

> **Assurance Debt shall remain visible and shall not relabel a failed Required Claim as acceptable.**

> **Independence Theater and evidence volume do not create Assurance.**

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.11  
Initial publication: 2026-08-13  
Last modified: 2026-08-13