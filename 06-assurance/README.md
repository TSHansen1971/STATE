# Assurance

> **Document:** `06-assurance/README.md`  
> **Title:** Assurance  
> **Version:** 0.3  
> **Status:** Working Draft  
> **Created:** 2026-08-11  
> **Last modified:** 2026-08-13  
> **Author:** Tor-Ståle Hansen  
> **Co-authors:** None


Assurance addresses whether a STATE transition, its evidence, its role arrangement and its resulting claims deserve trust.

Assurance is not identical to testing.

Testing may produce evidence. Verification evaluates specified claims. Acceptance authorizes state. Assurance evaluates the sufficiency, independence and trustworthiness of that overall basis.

STATE distinguishes at least three assurance perspectives:

## Process assurance

Was the required STATE process followed with appropriate rigor?

This includes whether role and authority assignments were sufficiently explicit for the transition.

## Transition assurance

Is the evidence sufficient to support the claims made about this specific transition?

This includes whether production, verification, evidence stewardship and acceptance were separated to a degree appropriate to the consequence and uncertainty involved.

## Resulting-state assurance

Is there sufficient basis to trust the relevant properties claimed for the accepted state?

## Role-separation assurance

Logical role separation is always required.

Physical separation between actors is required only when the assurance objective cannot be achieved through combined assignment.

Relevant questions include:

- Did the Realization Role effectively certify its own output without independent evidence?
- Did an actor exercise authority outside its explicit or inherited grant?
- Was Acceptance Authority independent enough for the consequence of the decision?
- Can the authority chain be traced to a legitimate human-established governance source?
- Did role combination create a conflict that weakened verification or acceptance?
- Were actor-specific failure modes addressed through appropriate controls?

Assurance requirements are proportionate to consequence, uncertainty, reversibility, exposure and the cost of being wrong.

Where independence matters, producer and verifier need not necessarily be different organizations or technologies, but production and verification shall remain logically separable and the chosen degree of independence shall be explicit.

---

© Tor-Ståle Hansen, https://x.com/TSHansen1971

CC BY-NC-ND 4.0  
Version: 0.3  
Initial publication: 2026-08-11  
Last modified: 2026-08-13
