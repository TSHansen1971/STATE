# Normative Language and Precedence

> **Document:** `07-reference/NORMATIVE-LANGUAGE.md`  
> **Title:** Normative Language and Precedence  
> **Version:** 0.13  
> **Status:** Normative Working Specification  
> **Created:** 2026-08-13  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None

This document defines how normative statements and document authority are interpreted within STATE Engineering.

## 1. Purpose

STATE uses ordinary engineering language, but certain words carry specific normative force.

The purpose is to prevent ambiguity about mandatory control, prohibition, recommendation, permission, capability, document authority and supersession.

## 2. Mandatory language

### SHALL / MUST

`SHALL` is the preferred forward-looking mandatory term.

Existing current normative text using `MUST` carries the same mandatory force unless the surrounding text clearly uses the word in a non-normative ordinary-language sense.

### SHALL NOT / MUST NOT

These express a mandatory prohibition.

## 3. Recommendation language

### SHOULD

Expresses a recommended engineering practice.

A deviation may be legitimate, but where the recommendation is material to Assurance or Tailoring, the deviation should have a reason.

### SHOULD NOT

Expresses a discouraged practice.

A contrary choice may be legitimate when the engineering basis is explicit.

## 4. Permission language

### MAY

Expresses permission within the stated scope.

`MAY` does not create Authority that does not otherwise exist.

## 5. Capability language

### CAN

Expresses capability or possibility.

`CAN` shall not be interpreted as permission or Authority.

```text
can perform
≠
may perform
≠
is authorized to perform
```

## 6. Definitional language

Statements using `is`, `are`, `means`, `defines` or equivalent language can be normative when they define a canonical STATE concept.

A definition is not weakened merely because it lacks `SHALL`.

## 7. Conditional applicability

Expressions such as:

- where applicable;
- when Release occurs;
- where the claim depends on interaction;
- when required by Tailoring;

make the requirement conditional on a real scope condition.

They do not permit an applicable requirement to be declared irrelevant for convenience.

## 8. Normative Precedence

STATE uses the following interpretation order.

### Level 1 — Current integrated specification

The current `STATE-ENGINEERING-METHOD-SPECIFICATION-*` identified by the Foundation README is the highest integrated normative statement of the method.

### Level 2 — Current normative model documents

A current domain model marked `Normative Working Specification` provides detailed semantics within its scope.

Where the integrated specification deliberately summarizes a model, the domain document supplies detail provided it does not contradict the current integrated specification.

### Level 3 — Normative reference models and catalogues

Reference documents can be normative within their declared subject, particularly catalogues and the Conformance Model.

They do not silently redefine Level 1 or Level 2 semantics.

### Level 4 — Reference summaries, checklists and navigation material

Compact references, checklists and README files support use and navigation.

They summarize; they do not override the governing normative model.

### Level 5 — Historical superseded specifications

Earlier integrated specifications are retained for provenance and method history.

They do not override the current method baseline.

## 9. Apparent conflict

Precedence is not permission to leave contradictions unresolved.

When two current normative texts materially conflict:

1. preserve the existing authoritative method baseline;
2. identify the conflicting statements;
3. apply the higher-precedence interpretation for immediate reading;
4. correct the conflict through a controlled method revision;
5. preserve superseded text as history where applicable.

## 10. Identifier stability

A published identifier shall retain its semantic identity.

STATE identifiers shall not be silently renumbered merely to make a catalogue visually tidy.

If an element is superseded or retired:

- its identifier remains reserved;
- replacement identity is explicit;
- history remains reconstructable.

## 11. Normative naming

Capitalization is used selectively for canonical STATE concepts.

Capitalization supports readability but is not itself the source of normative force.

## 12. Canonical language rules

> **Mandatory language expresses an obligation only within its stated scope.**

> **Permission does not create Authority.**

> **Capability language does not create permission.**

> **Definitions can be normative without a modal verb.**

> **Historical specifications provide provenance, not current precedence.**

> **Published identifiers shall not be silently reused for different semantics.**

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.13  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
