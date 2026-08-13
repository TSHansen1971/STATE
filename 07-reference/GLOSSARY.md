# STATE Engineering Glossary

> **Document:** `07-reference/GLOSSARY.md`  
> **Title:** STATE Engineering Glossary  
> **Version:** 0.13  
> **Status:** Reference  
> **Created:** 2026-08-11  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None

This glossary consolidates the current working vocabulary of STATE Engineering.

Definitions are governed by the current method specification and the normative model document in which a concept is defined. This glossary is a consolidated lookup surface; it does not override a more specific current normative definition.

## Acceptance

The authorized P8 decision about whether an identified Candidate State may progress toward authoritative status.

## Acceptance Authority

The authority to decide ACCEPT, REJECT, REPAIR REQUIRED or INCONCLUSIVE for a defined Candidate and scope.

## Acceptance Basis

The governing claims, conditions, evidence expectations, deviations, uncertainty tolerance and authority basis against which a Candidate is decided.

## Acceptance Claim Set

The set of Required, Supporting and Informational Claims governing an Acceptance decision.

## Acceptance Gate

G8 of the STATE Cycle, at which Acceptance Authority records ACCEPT, REJECT, REPAIR REQUIRED or INCONCLUSIVE.

## Acceptance Record

WP-08, recording Candidate identity, Contract identity, Acceptance scope, claims, evidence, deviations, residual uncertainty, authority, decision and rationale.

## Acceptance Scope

The explicit system, component, artifact, environment, purpose or state scope covered by an Acceptance decision.

## Acceptance Sufficiency Condition

A logical condition used to determine whether the basis for ACCEPT is sufficient.

## Accepted Candidate

A Candidate State for which G8 has produced ACCEPT but which has not necessarily completed P9 Baseline Establishment.

## Access

A physical mechanism allowing an Actor or tool to reach, observe or mutate a system surface. Access does not itself establish Authority.

## Actor

The human, synthetic or hybrid entity assigned to perform a logical STATE Role.

## Actor Assignment

The binding of an actual Actor to logical Roles and applicable Authority Grants.

## Actor Independence

The property by which logical Roles and responsibilities remain defined independently of Actor type.

## Actor Realization Pattern

A common physical form through which a logical STATE Role may be performed, such as an individual human, distributed team, supplier, deterministic automation, synthetic Actor or hybrid arrangement.

## Amendment History

The traceable record of material authorized changes to a Transition Contract.

## Architecture Authority

The authority to establish or approve structural rules, architectural boundaries and architectural invariants within a defined scope.

## Assurance

The structured evaluation of whether the control, verification, evidence, independence and uncertainty basis supporting a defined engineering claim or decision is sufficient for the applicable consequence and Assurance Objective.

## Assurance Basis

The claims, controls, Verification Records, Evidence, Authority, Tailoring, environment, challenge and provenance used to support an Assurance Conclusion.

## Assurance Case

The reconstructable structured argument connecting an Assurance Objective and scope to the claims, control basis, evidence, challenge, weaknesses, residual uncertainty and conclusion used to justify confidence.

## Assurance Challenge

A deliberate attempt to identify why an engineering claim, evidence basis or confidence argument may be wrong.

## Assurance Conclusion

SUFFICIENT, INSUFFICIENT or INCONCLUSIVE for a defined Assurance Objective and scope.

## Assurance Debt

A known unresolved weakness in the trust basis that remains explicit for future action and does not relabel a failed Required Claim.

## Assurance Deficiency

A weakness that reduces justified confidence in an Assurance Basis.

## Assurance Depth

The selected strength of evaluation, challenge, evidence and independence required to justify confidence for an Assurance Objective.

## Assurance Objective

A defined trust question whose adequacy is being evaluated by Assurance.

## Assurance Role

The logical role responsible for evaluating the adequacy of control, verification, evidence sufficiency and independence for the applicable assurance objective.

## Authoritative State

A sufficiently identified system state accepted and explicitly established as authoritative for a defined scope and purpose.

## Authoritative State Chain

The traceable sequence of Authoritative States and the controlled Transitions by which authority moved from one state to the next.

## Authority

The legitimate permission to decide, approve, delegate or mutate within a defined scope.

## Authority Boundary

The explicit limit of what a Role or Actor may decide, approve or change within a defined context.

## Authority Domain

A category of legitimate engineering decision right defined by STATE.

## Authority Grant

The bounded authority object governing legitimate engineering action or decision.

## Authorized Execution Envelope

The subset of effective physical capability that may legitimately be exercised under the applicable Authority Grant and Transition Boundary.

## Baseline

The specific Authoritative State selected as input to a Transition.

## Baseline Custodianship Role

The logical role responsible for preserving authoritative-state identity and continuity and for preventing an unaccepted candidate from silently becoming the baseline.

## Baseline Establishment

The explicit P9 act that assigns authoritative status to the exact accepted Candidate for a defined scope and purpose.

## Baseline Establishment Gate

G9 of the STATE Cycle, which verifies that the accepted state has been explicitly established as authoritative.

## Baseline Establishment Record

WP-09, preserving previous state, accepted Candidate, Acceptance, Contract, authority scope, resulting state identity and establishment result.

## Baseline Record

The Work Product identifying the Authoritative State selected as input to a Transition.

## Baseline Scope

The defined system, source, artifact, configuration, deployment or other state domain for which an Authoritative State has authority.

## Boundary Breach

A discovered condition in which a required or attempted action lies outside the authorized Transition Boundary.

## Candidate Revision

A materially distinct Candidate State produced during repair or further realization and requiring identity sufficient to prevent evidence confusion with another candidate.

## Candidate State

A produced system state that has not yet completed Baseline Establishment.

## Capability

What an Actor, tool or environment is actually able to do.

## Claim Dependency

A relationship in which evaluation or truth of one Verification Claim depends on one or more other claims.

## Claim Scope

The Work Package, component, interface, integrated Candidate, system or release level to which a Verification Claim applies.

## Claim–Evidence Binding

The explicit relationship between an engineering claim and the Evidence Items used to support or challenge it.

## Conditional Acceptance

Not a canonical STATE outcome. If a condition is required before authoritative status, it remains part of the Acceptance basis and must be resolved before ACCEPT.

## Confidence

Justified belief in the adequacy of an Assurance Basis for a defined objective and scope.

## Conformance Assessment

The structured evaluation of a declared scope against the applicable internal STATE Conformance Requirements.

## Conformance Assessment Record

The logical record of assessment scope, requirement dispositions, evidence, nonconformities, inconclusive items, overall status and reassessment conditions.

## Conformance Claim

An assertion that a defined Transition, Realization or Implementation satisfies the applicable internal STATE Conformance Requirements.

## Conformance Requirement

One of the sixteen non-tailorable internal requirements used to determine whether a declared scope preserves STATE control semantics.

## Conformance Scope

The explicit boundary of a Conformance assessment: Transition, Realization or Implementation.

## Conformance Status

CONFORMANT, NONCONFORMANT or INCONCLUSIVE for a declared internal STATE Conformance scope.

## Contract Amendment

An explicit authorized change to one or more governing elements of a Transition Contract.

## Control Deletion

Removal of a required STATE control semantic under the guise of simplification. Control Deletion is not conformant Tailoring.

## Criterion Disposition

SATISFIED, NOT SATISFIED, INCONCLUSIVE or NOT APPLICABLE for an individual Conformance Requirement.

## Deviation and Escalation Record

The conditional Work Product preserving material deviation, authority uncertainty, requested scope expansion, verification limitation or related escalation.

## Downward Tailoring

Reduction in physical representation or control depth while remaining inside the Tailoring Envelope.

## Effective Capability Envelope

The capabilities actually available through the intersection of Actor capability, tool capability, environment capability and available access.

## Effective Condition

The time, sequence, event or other condition at which a Baseline Establishment or Release becomes effective.

## Environment Drift

A material change in hardware, software, configuration, dependency, external service, data or other Execution Environment condition between relevant engineering activities.

## Establishment Result

ESTABLISHED, HOLD or FAILED at P9.

## Evidence

Observable information used to support or challenge an engineering claim.

## Evidence Class

A canonical category describing the kind of engineering claim an Evidence Item can support.

## Evidence Gate

G7 of the STATE Cycle, which determines whether the evidentiary basis is decision-ready for the requested Acceptance decision.

## Evidence Item

An identifiable observation, artifact, record or measurement used to support or challenge a claim.

## Evidence Set

WP-07, binding relevant Evidence Items to one or more engineering claims.

## Evidence Stewardship Role

The logical role responsible for preserving evidence identity, linkage, provenance and availability.

## Evidence Sufficiency

The degree to which the available Evidence Set provides enough basis for the strength and consequence of a claim.

## Evidence-Based Acceptance

The STATE property requiring Acceptance to be supported by evidence appropriate to the claim being accepted.

## Evidence-Quality Property

A property used to evaluate whether evidence is fit for its intended claim, including relevance, identity, integrity, provenance, sufficiency, reproducibility, independence, timeliness and preservation.

## Execution Environment

The relevant physical and software context in which a STATE Role, Work Package, verification activity, transformation or Release action is performed.

## Externalized State

Material state outside the immediate local environment that can affect execution, such as remote configuration, service-side policy or hosted model version.

## FAIL

A Verification Result indicating that evidence contradicts the claim or demonstrates that the required property is not satisfied under the specified conditions.

## False Independence

The appearance of independent verification where Actors or methods still share a material common failure source.

## Foundational Property

A constitutive property that must remain present for an engineering process to retain the defining character of STATE Engineering.

## Gate

A logical decision condition establishing whether the control conditions required for progression are sufficiently satisfied.

## Hybrid Actor Arrangement

A physical realization in which human and synthetic Actors jointly perform STATE Roles or Work Packages.

## Implementation Conformance

Conformance of a defined engineering-system or project implementation of STATE under declared assumptions and Tailoring.

## Inconclusive

A valid engineering outcome indicating that available verification or evidence is insufficient to establish the required conclusion.

## INCONCLUSIVE

A Verification or Acceptance outcome indicating that available basis is insufficient to establish the required conclusion.

## Independence Theater

Additional Actor, approval, reviewer or process separation that does not materially challenge the relevant common-cause failure source.

## Inherited Tailoring

Application of an established Tailoring profile or policy to a Transition whose context remains within the profile's assumptions.

## Integrated Candidate

A Candidate State resulting from integration of one or more Work Package outputs.

## Integration

The engineering transformation that combines Work Package outputs into a Candidate State or a broader Candidate revision.

## Intent and Outcome Claim

CC-12, asserting that the Candidate satisfies the governing intended outcome or purpose.

## Intent Authority

The authority to establish or approve intended outcomes, priorities and intent-level trade-offs within a defined scope.

## Invariant

A relevant property required to remain true through a Transition.

## Isolation Mechanism

A physical or logical mechanism reducing unintended interference among Work Packages, Actors, environments or mutable state.

## Least Authority

The principle that a Role, Actor, component or execution context should receive only the authority necessary to perform its assigned function.

## Logical Role Separation

The requirement that distinct STATE functions remain conceptually separate even when one physical Actor performs multiple roles.

## Method Fitness

The degree to which a Verification Method can legitimately bear on the claim being evaluated.

## Method Traceability

The reconstructable internal relationship among Foundational Properties, normative control elements, evidence obligations, Assurance and Conformance requirements.

## Methodological Provenance

The traceable relationship between a STATE principle or rule and the directly relevant engineering knowledge that informed its rationale.

## Mutation Envelope

The bounded subset of a Transition Boundary within which a Work Package is authorized to mutate state.

## Mutation Surface

The physical system surface that an Actor or tool can actually change.

## Nonconformity

An applicable Conformance Requirement assessed as NOT SATISFIED.

## Normative Element

A named STATE method object, rule, property, role, control, field, class, condition or assessment element whose semantics are governed by the current method.

## Normative Namespace

A stable identifier prefix used to distinguish a family of STATE Normative Elements, such as FP, WP, TC, CON or AO.

## Normative Precedence

The rule determining which current STATE document controls when two method texts appear to express conflicting semantics.

## Normative Requirement

A mandatory STATE obligation expressed through mandatory language or a constitutive named requirement within its declared scope.

## Package Completion

The condition in which a Work Package has satisfied its bounded objective and evidence obligations. Package Completion is not Transition Acceptance.

## PASS

A Verification Result indicating that identified evidence sufficiently supports an identified claim for an identified target and conditions at the required Assurance level.

## Phase

A canonical logical segment of the STATE Cycle defined by purpose, required control conditions and output.

## Physical Realization

The concrete assignment of Actors, execution environments, tools, access and evidence mechanisms to the logical Roles and control obligations of a STATE Transition.

## Physical Realization Binding

The reconstructable relationship among logical Role, Actor Assignment, capability, Authority, Execution Environment, tool capability, access, evidence mechanism and Assurance control.

## Provenance

The traceable relationship among origin, authorized transformations, identities, Actors, evidence and decisions explaining how a state or artifact came to exist in its asserted form.

## Provenance Dimension

A category of provenance information: source, authority, transformation, Actor, environment, evidence, decision or distribution provenance.

## Re-tailoring

Reassessment of the selected Tailoring when material context change invalidates or weakens the original Tailoring basis.

## Realization Conformance

Conformance of a recurring workflow, pipeline, toolchain or physical realization pattern intended to support STATE semantics.

## Realization Role

The logical Role responsible for producing the Candidate State within the authorized Transition Boundary.

## Reference Authority

The degree to which a STATE document is authoritative for interpretation, ranging from the current integrated specification through normative model documents to summaries, checklists and historical material.

## Release

An authorized post-cycle act that makes an identified representation of an established Authoritative State available to a defined target, channel, environment or audience.

## Release Authority

The authority to distribute, deploy, publish or otherwise release an established state or representation.

## Release Record

WP-10, recording Release identity, source Authoritative State, authority, target, released object, transformation, verification, provenance, integrity and result.

## Release Result

RELEASED, HOLD or FAILED.

## Release Transformation

A build, packaging, signing, configuration, deployment or other transformation performed between an established Authoritative State and a released representation.

## Released Object

The exact artifact, package, deployment, publication or other representation made available by a Release.

## Repair

An authorized mutation intended to correct a failed or unacceptable Candidate State without silently changing the governing intent or authority.

## Required Claim

ACS-01, a claim that must be sufficiently satisfied for ACCEPT under the current Acceptance basis.

## Residual Uncertainty

Material uncertainty remaining after practical Verification and Assurance activity.

## Responsibility

What a Role is accountable for producing, preserving, evaluating, deciding or controlling.

## Resume Point

A reconstructed cycle position whose preceding gate conditions remain valid and from which a Transition can safely continue.

## Role

A defined logical function within the engineering method, independent of the Actor assigned to perform it.

## Rollback

A colloquial term for reversal or restoration. When the Authoritative State itself has already changed, STATE treats rollback as a new controlled Transition toward a new Authoritative State, even when the resulting content is equivalent to an earlier state.

## Scaling Profile

A non-mandatory reference pattern illustrating a coherent physical realization of STATE at a particular control depth or execution context.

## Secure Engineering by Construction

The foundational property by which generally applicable secure-engineering principles are intrinsic to the ordinary STATE method rather than appended as a separate late lifecycle.

## Security Invariant

A security-relevant property that is required to remain true through a Transition.

## Semantic Compression

Physical combination of multiple logical STATE control objects or stages into a smaller number of physical records, operations or mechanisms while preserving their logical distinctions.

## Source-to-Artifact Provenance

The evidentiary relationship connecting an accepted source state through establishment and release transformation to a specific released artifact.

## Specification

An operational expression of intended change, constraints, relevant invariants and Acceptance basis.

## Specification Role

The logical role responsible for transforming approved intent and constraints into a sufficiently operational specification for a Transition.

## STATE Cycle

The canonical P0–P9 logical process that carries a Transition from authorized Baseline through Candidate production, verification, evidence, Acceptance and explicit baseline establishment.

## Structured Trust

The principle that trust should be explicit, bounded, decomposable and justified at the level where it is required.

## Superseded Authoritative State

A previously authoritative state replaced for the same defined scope by a later established Authoritative State while remaining part of historical provenance.

## Supporting Claim

ACS-02, a claim that supports the decision context but is not independently mandatory for ACCEPT.

## Synthetic Actor

A non-human computational Actor, such as an AI model, agent or multi-agent system, assigned to perform one or more logical STATE functions.

## Tailoring

The authorized selection of representation, depth, automation, separation and evidence controls within the Tailoring Envelope while preserving the defining semantics of STATE Engineering.

## Tailoring Adequacy

Confidence that the selected Tailoring remains within the Tailoring Envelope and preserves required STATE semantics.

## Tailoring Authority

The authority to establish or approve a Tailoring decision for a defined scope.

## Tailoring Decision

The controlled decision defining how STATE will be physically and procedurally realized for a Transition or class of Transitions.

## Tailoring Envelope

The permitted range of physical and procedural variation within which Foundational Properties and required control semantics remain intact.

## Tailoring Factor

A context property used to determine appropriate control depth, such as consequence, complexity, uncertainty, reversibility, security relevance or distribution.

## Tailoring Invariant

A non-tailorable operational semantic that shall remain true across all conformant STATE realizations.

## Tool Capability

The concrete transformation, verification, execution, analysis, release, evidence or coordination capability provided by a physical tool.

## Toolchain

The set of physical software tools and dependencies used to author, transform, construct, verify, execute, package or release state.

## Traceability

The ability to reconstruct relevant relationships among intent, Baseline, authorization, transformation, verification, evidence, decision and resulting state.

## Transition

A controlled transformation from one Authoritative State toward a Candidate State and, if accepted and established, a new Authoritative State.

## Transition Authority

The authority to define or approve what is allowed to change within a specific Transition.

## Transition Boundary

The explicit scope within which a Transition is authorized to operate.

## Transition Conformance

Conformance of one actual controlled STATE Transition.

## Transition Contract

The reconstructable governing logical composition of baseline, intent, authority, scope, roles, dependencies, verification, evidence and Acceptance basis for one Transition.

## Transition Contract Amendment

A material authorized change to the governing Transition Contract that remains traceable and triggers re-evaluation of affected gate conditions.

## Transition Gate

A gate controlling logical progression between STATE Cycle phases.

## Transition Intent and Specification

The Work Product defining intended outcome, constraints, invariants, non-goals and Acceptance basis for a Transition.

## Transition Record

The central Work Product connecting baseline, specification, authority, Actor Assignments, mutation, verification, evidence, decision and resulting state.

## Universal Engineering Principle

A STATE-native principle expressing generally applicable engineering behavior used across abstraction levels to preserve the Foundational Properties.

## Upward Tailoring

Increase in control depth, independence, evidence, isolation or verification because context requires stronger Assurance.

## Verification

The evaluation of an explicit claim about an identified target using an identified method, conditions, observations and evidence.

## Verification Adequacy

The degree to which claim precision, target identity, method fitness, conditions, coverage, evidence, independence and limitations provide a sufficient verification basis.

## Verification Claim

A bounded proposition about an identified target under identified conditions.

## Verification Gate

G6 of the STATE Cycle, which requires required claims to have explicit outcomes and visible limitations.

## Verification Independence

The degree to which verification challenges production or prior conclusions through distinct actors, methods, tools, environments, organizations or decisions.

## Verification Method

The concrete means used to evaluate a Verification Claim.

## Verification Record

WP-06, recording claim identity, target, method, conditions, observation, evidence, result, limitations, verifier and dependencies.

## Verification Result

PASS, FAIL or INCONCLUSIVE for a bounded Verification Claim.

## Verification Role

The logical role responsible for evaluating claims about the Candidate State using verification methods appropriate to those claims.

## Work Package

A bounded execution/control unit subordinate to one governing Transition Contract.

## Work Package Dependency

A state, information, execution, integration, environment or authority condition on which Work Package validity or progression depends.

## Work Package State

The logical execution status of a Work Package: PLANNED, READY, ACTIVE, BLOCKED, COMPLETED, FAILED, CANCELLED or SUPERSEDED.

## Work Product

An identifiable information object produced, maintained or consumed by STATE Roles to control, perform, verify, evidence or authorize a Transition.


## STATE name decomposition

The canonical decomposition of the method name:

- **S — Specification**
- **T — Transition**
- **A — Authority**
- **T — Traceability**
- **E — Evidence**

The decomposition names five central STATE control concerns.

It is not a strict causal dependency chain and does not create a separate lifecycle, phase sequence, Authority Domain, Role, Work Product class, Evidence class or Conformance Requirement.


---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-SA 4.0  
Version: 0.13  
Initial publication: 2026-08-11  
Last modified: 2026-08-13
