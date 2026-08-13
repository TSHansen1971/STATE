# Methodological Source Register

> **Document:** `07-reference/METHODOLOGICAL-SOURCE-REGISTER.md`
> **Title:** Methodological Source Register
> **Version:** 0.2
> **Status:** Reference
> **Created:** 2026-08-11
> **Last modified:** 2026-08-13
> **Author:** Tor-Ståle Hansen
> **Co-authors:** None

This register records directly relevant methodological source material that genuinely informs STATE Engineering principles and rationale.

It is not a compliance crosswalk.

External sources may inform STATE requirements, but the source architecture does not become the architecture of STATE Engineering.

## 1. Source inclusion rule

A source belongs in this register only when its actual methodological influence can be stated explicitly.

For each registered source the register records:

1. **methodological concept supported**;
2. **classification** — `Normative influence`, `Engineering principle`, `Historical context` or `Explanatory background`;
3. **STATE concept affected**;
4. **not inherited by STATE**;
5. **provenance status**.

A source concept may be absorbed into the universal STATE core only when it is:

- methodologically relevant;
- generally applicable across software or systems engineering domains;
- expressible as an engineering principle, pattern, Verification obligation or control property;
- compatible with STATE's actor-independent state-transition model;
- not dependent for its validity on a particular jurisdiction, mission, organization or sector.

Broad compliance aggregation and external meta-framework mapping are outside the purpose of this register.

## 2. NIST SP 800-53 Rev. 5 — SA-8 Security and Privacy Engineering Principles

**Authoritative source:**  
https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final

**Methodological concept supported:** general systems-security engineering principles concerning abstraction, modularity, dependency structure, minimized sharing, least privilege, trust, secure evolvability, continuous protection, metadata, accountability, secure defaults, failure and recovery, human factors, repeatable procedure, procedural rigor, secure modification, documentation and minimization.

**Classification:** `Engineering principle`

**STATE concept affected:** Secure Engineering by Construction; the Universal Engineering Principles; the Secure Modification Foundational Property; claim-appropriate Logical, Physical and Assurance controls.

**What STATE does not inherit:** the external source's control architecture, control numbering as STATE identifiers, blanket conformance claims, organization-specific implementation assumptions or contextual obligations that are not generally applicable engineering principles.

**Provenance status:** authoritative public NIST source recorded. The methodological absorption is explicitly traceable in `02-what-conceptual/05-universal-engineering-principles.md`, where the 33 SA-8 principles are accounted for through STATE-native engineering principles.

## 3. OWASP Secure by Design

**Authoritative source:**  
https://owasp.org/www-project-secure-by-design-framework/

**Methodological concept supported:** secure design as an architectural and engineering property, including explicit boundaries, least privilege, secure defaults, resilience, controlled communication, observability and iterative review when designs materially change.

**Classification:** `Engineering principle`

**STATE concept affected:** Secure Engineering by Construction and the STATE Universal Engineering Principles concerned with explicit boundaries, security architecture, least privilege, resilience, observability and controlled change.

**What STATE does not inherit:** an external organizing structure, mandatory use of source-specific lifecycle terminology, domain-specific examples, organizational prescriptions or a blanket claim of conformance to all source material.

**Provenance status:** authoritative public OWASP project source recorded; STATE use is bounded to generally applicable secure-design principles.

## 4. OWASP Threat Modeling

**Authoritative source:**  
https://owasp.org/www-community/Threat_Modeling

**Methodological concept supported:** threat-oriented reasoning used to identify threats, assets, attack paths and mitigations when such analysis is material to a Transition or engineering claim.

**Classification:** `Engineering principle`

**STATE concept affected:** available design and Verification practices under the Conceptual, Logical, Tailoring and Assurance layers.

**What STATE does not inherit:** a requirement that every STATE Transition perform threat modeling merely by name, a source-specific process as the STATE lifecycle, or a universal mandatory depth independent of context.

**Provenance status:** authoritative public OWASP community guidance recorded. Its use in STATE remains conditional on Transition context, risk, architecture, Tailoring and Assurance need.

## 5. NATO Alliance Digital Strategy

**Authoritative source:**  
https://www.nato.int/en/about-us/official-texts-and-resources/official-texts/2026/01/13/alliance-digital-strategy

**Methodological concept supported:** publicly stated engineering principles relevant to continuous Verification, least privilege, secure handling, resilient engineering and digital integration.

**Classification:** `Engineering principle`

**STATE concept affected:** general secure-engineering rationale and cross-cutting principles where those concepts are domain-neutral and technically applicable.

**What STATE does not inherit:** mission-specific, alliance-specific, organizational, operational, command, policy or context-bound requirements; the external document's institutional structure; or any assumption that those requirements are universal STATE method requirements.

**Provenance status:** authoritative public official-text source recorded. STATE use is deliberately restricted to generally applicable engineering content.

## 6. Legal and regulatory exclusion rule

Legal or regulatory obligations are not methodological sources merely because STATE may be used in contexts where such obligations apply.

Domain-specific legal or regulatory requirements belong to scoped demand-side context, Specification, constraints or Tailoring unless expressly incorporated into the method through a separately authorized decision.

This prevents contextual obligations from being mistaken for universal STATE architecture.

## 7. Register discipline

For a source to remain in this register, the method shall be able to answer:

```text
WHAT DID THIS SOURCE ACTUALLY INFORM?
WHAT KIND OF INFLUENCE IS IT?
WHERE IS THAT INFLUENCE VISIBLE IN STATE?
WHAT DID STATE DELIBERATELY NOT INHERIT?
CAN THE SOURCE PROVENANCE BE IDENTIFIED?
```

A STATE requirement remains a STATE requirement.

Source provenance explains its engineering basis without transferring the external source's architecture into STATE.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.2  
Initial publication: 2026-08-11  
Last modified: 2026-08-13
