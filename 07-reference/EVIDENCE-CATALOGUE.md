# STATE Evidence Catalogue

> **Document:** `07-reference/EVIDENCE-CATALOGUE.md`  
> **Title:** STATE Evidence Catalogue  
> **Version:** 0.4  
> **Status:** Reference  
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


This catalogue provides the compact reference view of STATE Evidence Classes and Evidence-Quality Properties.

## Evidence classes

| ID | Evidence class | Primary question |
|---|---|---|
| EC-01 | Identity Evidence | Which state, source, file or artifact is this? |
| EC-02 | Authority Evidence | Who or what was authorized to act or decide? |
| EC-03 | Transformation Evidence | What changed? |
| EC-04 | Construction and Build Evidence | Was the system or artifact successfully constructed? |
| EC-05 | Behavioral Evidence | How did the candidate actually behave? |
| EC-06 | Regression and Preservation Evidence | Which required existing properties remained true? |
| EC-07 | Security and Boundary Evidence | Which security-relevant boundaries or properties were preserved or changed? |
| EC-08 | Environment Evidence | Under what relevant conditions was the work performed or verified? |
| EC-09 | Provenance and Integrity Evidence | Where did the state or artifact come from and can substitution be excluded to the required degree? |
| EC-10 | Decision Evidence | What decision was made, by what authority and on what basis? |

## Evidence-quality properties

| ID | Property | Core question |
|---|---|---|
| EQ-01 | Relevance | Does this evidence actually bear on the claim? |
| EQ-02 | Identity | Is the evidence itself sufficiently identifiable? |
| EQ-03 | Integrity | Can silent or unintended alteration be excluded to the required degree? |
| EQ-04 | Provenance | Is the evidence origin and transformation history sufficiently known? |
| EQ-05 | Sufficiency | Is there enough evidence for the strength of the claim? |
| EQ-06 | Reproducibility | Can the observation or verification be repeated as required? |
| EQ-07 | Independence | Is the evidence sufficiently independent of production for the Assurance objective? |
| EQ-08 | Timeliness | Does the evidence correspond to the state and decision being evaluated? |
| EQ-09 | Preservation | Will the evidence remain available and interpretable for the required period? |

## Claim–evidence rule

Evidence should be referenced from a Verification Record or decision context through the claim it supports or challenges.

A directory full of logs is not automatically a strong Evidence Set.

The evidentiary question is:

> **Which claim does this item bear on, and why is it sufficient or insufficient for that claim?**

## Security-relevant evidence

Security-relevant verification may require one or more evidence classes, depending on the claim.

Examples include:

- privilege or permission comparison;
- trust-boundary analysis;
- security-test result;
- attack-surface comparison;
- dependency change evidence;
- failure-mode observation;
- provenance validation;
- release-identity verification.

No single evidence class is universally mandatory for every transition.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.4  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
