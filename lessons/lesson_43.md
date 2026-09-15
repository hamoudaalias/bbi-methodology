---
lesson: 43
title: "Causal discovery by intervention has a ceiling when the system is densely coupled : the intervention on one body propagates to all bodies via a global field, the dose-response measures the total effect (not the direct effect), and the direct link is indistinguishable from the transitive link by simple intervention"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Lesson 43 — Causal discovery by intervention has a ceiling when the system is densely coupled : the intervention on one body propagates to all bodies via a global field, the dose-response measures the total effect (not the direct effect), and the direct link is indistinguishable from the transitive link by simple intervention
**Lesson (frozen formulation) :** *"When the coupling is dense — a global field
(well field) connects all bodies — the intervention on one body produces a
measurable response in all bodies. The dose-response then measures the total
effect, not the direct effect. The direct causal link (1→2) and the transitive
link (1→0→2) are indistinguishable by simple intervention. To distinguish them,
targeted multi-body interventions (intervening on A while keeping B fixed) or
fine temporal observations (propagation delay) are needed."*

**Contexts :** Milestone J2 Causal Discovery (Causal Touch + C attribution,
5 pilots 89110-89114, budget B_max=10, amendment A'1 CS1 = bodies alone). Verdict
PASS (recall 0.722 ≥ 0.70, confirmed absents 0.167 ≤ 0.25, derivative traps 5/5,
sobriety 5/5, T_dec_gate 4/5 ≥ 70 %). But 2 declared false positives : (89110,
(1,2)) and (89111, (1,0)), both due to transitive coupling via the well field
(chains 1→0→2 and 1→2→0).

**Measurements (J2 Report, digest `c0ccae9b…`) :**

1. **The 2 FPs are structural, not agent errors** : in a 3-body + well system,
   the kick on one body produces a measurable response in **all** bodies (common
   coupling). The dose-response does not distinguish 1→2 direct from 1→0→2
   transitive.
2. **Test of the specificity guards** : imposing that the target beats the 3rd
   body reduces the FPs but collapses true recall (13/18, 5 misses) — raw
   specificity breaks the legitimate signal on densely coupled systems.
3. **The ceiling is a limit of the intervention method, not of the testbed alone** :
   the oracle itself (R2, B=10) caps at recall 0.74. The direct and transitive
   links are jointly non-identifiable from outside with simple interventions only.
4. **CS5 (honesty) becomes the guardrail** : the 2 FPs are declared in L_trace
   (non-discoveries vs false attributions). Epistemic honesty ≠ zero error ; it
   is zero masked error.

**Application :** 1) a causal-discovery-by-intervention protocol must anticipate
the "global field" ceiling : when the coupling is dense, plan multi-body
interventions (keeping B fixed while kicking A) or finite-delay temporal
observations to lift the direct/transitive indistinguishability ; 2) if the
method cannot lift the indistinguishability, the methodological bias must be
provisioned in the thresholds (recall capped by the oracle, not by the agent)
AND declared in L_trace — never masked ; 3) Lesson 43 completes Lesson 34
(causality requires intervention) by bounding what simple intervention can
identify ; Lesson 44 (J4) draws the consequence on budget and scope.

**Corpus brought to 43 lessons.**
