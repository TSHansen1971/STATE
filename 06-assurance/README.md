# Assurance

> **Document:** `06-assurance/README.md`  
> **Title:** Assurance  
> **Version:** 0.10  
> **Status:** Working Draft  
> **Created:** 2026-08-11  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


Assurance addresses whether a STATE Transition and its selected Tailoring deserve the required degree of trust.

## Tailoring assurance

Assurance evaluates whether the chosen Tailoring remains inside the Tailoring Envelope.

Relevant questions include:

- are all Foundational Properties preserved;
- are Tailoring Invariants preserved;
- is physical compression being mistaken for removal of control;
- are combined Roles still logically distinguishable;
- does gate automation preserve gate semantics and Authority;
- is Verification depth sufficient for the Required Claims;
- is evidence depth sufficient for the Acceptance decision;
- is environment identity sufficient for the claim;
- are Actor and tool common-cause failures understood;
- is Release control proportionate to the release claim.

## Over-tailoring assurance

More process is not automatically more Assurance.

Assurance should challenge controls that:

- add ceremony without improving evidence or control;
- duplicate records without increasing traceability;
- delay feedback;
- create stale documentation;
- obscure real decision authority.

## Under-tailoring assurance

Assurance should challenge Tailoring that:

- removes known Baseline identity;
- weakens Authority boundaries;
- turns Candidate into assumed Authority;
- suppresses FAIL or INCONCLUSIVE;
- relies on package-level PASS for system claims;
- removes decision-relevant negative evidence;
- weakens security-relevant verification;
- destroys provenance required by the claim.

## Profile assurance

Reference profiles are starting points.

Assurance considers whether:

- profile assumptions match the actual Transition;
- any deviation is justified;
- re-tailoring triggers have occurred;
- claim-specific strengthening is required.

## Re-tailoring assurance

When context changes materially, the Assurance basis shall consider whether prior Tailoring remains sufficient.

Tailoring is therefore not a one-time administrative label.

It remains a live control decision across the Transition.

Assurance remains proportional to consequence, uncertainty, reversibility, exposure, substitution risk and the cost of being wrong.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.10  
Initial publication: 2026-08-11  
Last modified: 2026-08-13
