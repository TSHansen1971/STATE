# STATE Operational Template — Repair / Resumption Record

> **Document:** `08-examples/templates/REPAIR-RESUMPTION-RECORD-TEMPLATE-001A.md`
> **Title:** STATE Operational Template — Repair / Resumption Record
> **Version:** 001A
> **Status:** Current Documentation
> **Created:** 2026-08-13
> **Last modified:** 2026-08-13
> **Author:** Tor-Ståle Hansen
> **Co-authors:** None

## Nature

This is a **non-normative operational template**.

It is a reusable physical representation of existing STATE semantics.

**Canonical mapping:** WP-05 Transition Record plus WP-11 where the failure/deviation is material

The template name does not create a new Work Product class.

## Template

```text
repair_record_identity:
transition_identity:
failed_candidate:
failed_claim_or_condition:
failure_result:
negative_evidence_reference:
diagnosis:
still_valid_phases_or_controls:
invalidated_phases_or_controls:
earliest_invalidated_phase:
authorized_repair_scope:
acceptance_basis_changed: YES / NO
boundary_changed: YES / NO
new_candidate_identity:
repeated_verification_required:
resolution:
```

Repair resumes from the earliest invalidated control condition.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-SA 4.0  
Version: 001A  
Initial publication: 2026-08-13  
Last modified: 2026-08-13
