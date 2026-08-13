# Methodological Source Register

> **Document:** `07-reference/METHODOLOGICAL-SOURCE-REGISTER.md`  
> **Title:** Methodological Source Register  
> **Version:** 0.2  
> **Status:** Working Reference  
> **Created:** 2026-08-11  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


This register records directly relevant methodological source material that informs STATE Engineering principles and rationale.

It is **not a compliance crosswalk**.

External sources may inform STATE requirements, but the external source structure does not become the structure of STATE Engineering.

## Source inclusion rule

A source concept may be absorbed into the universal STATE core only when it is:

1. methodologically relevant;
2. generally applicable across software or systems engineering domains;
3. expressible as an engineering principle, pattern, verification obligation or control property;
4. compatible with STATE's actor-independent state-transition model; and
5. not dependent for its validity on a particular jurisdiction, mission, organization or sector.

Broad compliance aggregation and meta-framework mapping are outside the purpose of this register.

## NIST SP 800-53 Rev. 5 — SA-8 Security and Privacy Engineering Principles

**Authoritative source:**  
https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final

**Current source basis for this STATE revision:** NIST SP 800-53 Rev. 5 material including the current Release 5.2.0 publication set.

**Methodological use:** the 33 SA-8 engineering principles provide directly relevant general systems-security engineering input concerning abstraction, modularity, dependency structure, minimized sharing, least privilege, trust, secure evolvability, continuous protection, metadata, accountability, secure defaults, failure and recovery, human factors, repeatable procedure, procedural rigor, secure modification, documentation and minimization.

**STATE treatment:** all 33 principles are explicitly accounted for in the methodological absorption record in `02-what-conceptual/05-universal-engineering-principles.md`. They are absorbed into twelve STATE-native Universal Engineering Principles and the Secure Modification Foundational Property.

This absorption record demonstrates methodological provenance. It does not assert blanket conformance to every control or contextual requirement in the source publication.

## OWASP Secure by Design

**Authoritative source:**  
https://owasp.org/www-project-secure-by-design-framework/

**Methodological use:** generally applicable secure-design principles and patterns, including security as an architectural property, explicit boundaries, least privilege, secure defaults, resilience, controlled communication, observability and iterative review when designs materially change.

**STATE treatment:** these concepts reinforce Secure Engineering by Construction and inform UEP-01, UEP-03, UEP-04, UEP-06, UEP-07, UEP-09 and UEP-10 where the guidance is generally applicable.

The STATE core does not absorb domain-specific regulatory examples merely because they appear in the source material.

## OWASP Threat Modeling

**Authoritative source:**  
https://owasp.org/www-community/Threat_Modeling

**Methodological use:** threat-oriented analysis as a means of identifying and reasoning about threats and mitigations in the context of something of value.

**STATE treatment:** threat modeling is an available verification and design practice when the risk, architecture or transition warrants it. It is not mandatory for every transition merely by name; Tailoring and Assurance determine the required depth.

## NATO Alliance Digital Strategy

**Authoritative source:**  
https://www.nato.int/en/about-us/official-texts-and-resources/official-texts/2026/01/13/alliance-digital-strategy

**Methodological use:** publicly stated engineering principles relevant to continuous verification, least privilege, secure handling, resilient engineering and digital integration.

**STATE treatment:** only generally applicable engineering concepts are candidates for the universal STATE core. Mission-, alliance-, organizational- or operationally specific requirements remain context-bound and are not universalized by STATE.

## Register discipline

The purpose of this register is to preserve methodological provenance:

- which directly relevant engineering knowledge informed a STATE principle;
- why the principle belongs in a general engineering method;
- where the principle is absorbed into STATE;
- which source-specific contextual material is deliberately not universalized.

A STATE requirement remains a STATE requirement. Source provenance explains its engineering basis without transferring the external source's architecture into the method.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.2  
Initial publication: 2026-08-11  
Last modified: 2026-08-13
