# Ted is from Accounting, Martha is from Payroll
## What Modern Human Security Tells Us About How to Secure AI Without Mathematical Guarantees

*James Myint (Jay) — initial deposit, April 2026*
*Licensed under CC BY-SA 4.0*

---

## Overview

AI safety research is largely organized around the pursuit of mathematical guarantees — formal verification, alignment proofs, interpretability methods that promise ground truth about model internals. There is a problem: those guarantees are not available. This is not an engineering gap to be closed by further research. It is a structural impossibility established by results in computational complexity theory and thermodynamics. (See companion work: *Cascading Impossibility of Verification*.)

This paper does not propose we give up on AI safety. It proposes we look at what we already know how to do.

**Ted from Accounting cannot approve his own expenses. Martha from Payroll cannot cut a check without a purchase order. Neither of them has been formally verified as trustworthy. We run civilization on this anyway.**

Human institutional security has solved — imperfectly but durably — the problem of securing systems composed of agents whose internal states are unverifiable and whose alignment cannot be mathematically guaranteed. The tools are mature, battle-tested, and almost entirely absent from mainstream AI safety discourse.

---

## The Problem With Mathematical Guarantees

Formal verification of software behavior is bounded by Rice's theorem: no algorithm can decide non-trivial semantic properties of arbitrary programs. AI systems are not exempt. Interpretability research can characterize behavior in observed contexts but cannot guarantee behavior in unobserved ones. Mathematical alignment proofs require formalizing human values completely enough to verify against — a problem that has not been solved and may not be solvable.

This is not a critique of the researchers pursuing these goals. It is a structural observation: the guarantee being sought may not exist in the form being sought. Waiting for it is not a safety strategy.

Meanwhile, institutions have been doing something else.

---

## What Ted and Martha Know

Ted is from Accounting. He has a salary, a mortgage, a reputation, a manager, and access to the general ledger. He is not mathematically verified as honest. He is secured through institutional mechanisms that don't require his internal states to be legible:

**Separation of duties.** Ted cannot approve his own expenses. The person who requests a payment is not the person who authorizes it is not the person who executes it. No single actor has full authority over a transaction. Collusion is possible but costly and requires coordination across multiple parties with independent incentive structures.

**Audit trails.** Not full verification — nobody reads every line of the ledger every day. But sufficient coverage that malfeasance is detectable after the fact, and detection probability is high enough to deter most bad actors most of the time.

**Need-to-know compartmentalization.** Ted doesn't have access to payroll. Martha doesn't have access to vendor contracts. Blast radius is bounded by limiting the scope of any single actor's authority. Compromise of Ted does not compromise Martha.

**Escalation paths and circuit breakers.** Transactions above a threshold require additional authorization. Anomalies trigger review. No single actor can move arbitrarily large resources without additional friction.

**Social accountability and reputational stakes.** Ted's professional identity is attached to his behavior. Firing and prosecution exist. Reference checks happen. The consequences of defection are real and persistent.

**Redundant human review.** For high-stakes decisions, multiple independent humans are involved. Not because any one of them is verified trustworthy, but because the probability of coordinated failure across independent reviewers is lower than the probability of individual failure.

None of this is mathematically guaranteed. All of it is robust enough to run global financial systems, nuclear arsenals, hospitals, and democratic governments on.

---

## The Proposal

AI governance should be designed to look like a well-run organization with good HR policy, not a formal verification system.

Concretely:

**Role-based access control.** AI systems should have roles with bounded authorities. A model that can read should not automatically write. A model that can write should not automatically execute. A model that can execute in sandboxed environments should not automatically reach production systems. These are org-chart decisions, not research problems.

**Separation of duties for AI actions.** High-stakes AI outputs should require authorization from actors with independent incentive structures — including humans — before execution. The AI equivalent of "Ted cannot approve his own expenses."

**Audit trails designed for deterrence, not omniscience.** We do not need to verify every inference. We need sufficient logging that anomalous behavior is detectable and that detection probability is known to any adversarial actor, whether that actor is an external attacker or the model itself.

**Compartmentalization by blast radius.** AI systems should be granted access to only the resources required for their current task. Compromise or misalignment of a specialized system should not cascade to unrelated systems. This is need-to-know applied to AI.

**Escalation thresholds.** Actions above a defined impact threshold should trigger human review. The threshold should be conservative and the review should be substantive, not rubber-stamping.

**Reputational and accountability infrastructure for AI developers and deployers.** Mathematical guarantees are unavailable. Liability, professional accountability, and regulatory enforcement are not. Attaching real consequences to AI failures shifts incentive structures in the way that makes institutional security work for Ted and Martha.

---

## Why This Is Underrated

The AI safety field is young and was founded largely by people with backgrounds in mathematics, computer science, and philosophy. The instinct toward formal guarantees is understandable and not wrong — formal methods are valuable where they apply.

But the field has underweighted the accumulated knowledge of security practitioners, organizational psychologists, compliance professionals, auditors, and institutional designers who have spent decades building systems that are secure enough without being formally verifiable. This knowledge exists. It is transferable. It does not require solving alignment first.

Ted from Accounting is not a solved problem. Organizations get defrauded. Institutions fail. But the failure rate is low enough and the recovery mechanisms are robust enough that civilization continues to function. That is the bar AI governance needs to clear — not mathematical perfection, but durable-enough robustness at civilizational scale.

We already know how to do this. We should start doing it.

---

## Relationship to CIV

This paper is a companion to the Cascading Impossibility of Verification (CIV) framework, which establishes the formal impossibility of mathematical AI safety guarantees via Rice's theorem, Landauer's principle, and thermodynamic accounting. CIV establishes why the guarantees aren't coming. Ted is from Accounting proposes what to do instead.

They are intended to be read together.

---

## Status

- [x] Core argument established
- [x] Prior art deposit (this document)
- [ ] Full paper with institutional security literature review
- [ ] Case studies: separation of duties in existing AI deployments
- [ ] Policy recommendations section
- [ ] Integration with CIV framework paper

---

## License

Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)

You are free to share and adapt this material for any purpose, provided you give appropriate credit and distribute any derivative works under the same license.

---

*This document constitutes a public prior art deposit. Timestamp established by repository commit history.*
