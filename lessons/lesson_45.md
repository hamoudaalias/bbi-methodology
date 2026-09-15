---
lesson: 45
title: "A strict dose-response criterion can make a test unsolvable on non-linear mechanisms, even for the oracle"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Lesson 45 — A strict dose-response criterion can make a test unsolvable on non-linear mechanisms, even for the oracle

**Lesson (frozen formulation, CP 2026-09-11) :** *"A strict dose-response
criterion can make a test unsolvable on complex non-linear mechanisms, even for
the oracle. The pre-sealing diligence must verify the solvability of the test by
sub-family, not only on average. An unsolvable-by-design test is not an agent
failure ; it is a protocol calibration error."*

**Contexts :** Causal Discovery pre-sealing diligence v2 (amendment A'2,
2026-09-11). Oracle mapping 120 seeds × 5 budgets (SHA `6bf67951…`,
600 R2_oracle calls). Structural facts :

- **F1 — 3rd-step artefact :** the sealed dose-response criterion
  `monotone = all(effects[k] >= effects[k-1]*0.7)` (testbed l.492) **de-confirms**
  an edge when the 3rd step (a, 2a, 4a) breaks the monotony. At B=15 (3 steps)
  the oracle ceiling **decreases** vs B=12 (2 steps) : B=10 → 0/12 families
  ≥ 0.80, **B=12 → 6/12**, B=15 → 4/12 (89340/89350 drop), B=18/20 → 2/12. The
  oracle ceiling **is not monotone in budget**.
- **F2 — J4 family risk :** the eval family (89420-89469) initially off-map ;
  oracle-only probed at B=12 : 5/5 sub-families ≥ 0.80 (means 0.819-0.881, total
  0.855) → solvable, kept.

**Application :** 1) **any pre-sealing diligence must map the oracle ceiling PER
SUB-FAMILY, over the WHOLE candidate budget range**, before freezing B_max and the
seeds — the oracle ceiling can drop when the budget rises (criterion artefact,
not physics) ; 2) the optimal budget is not "the largest possible" but "the one
where the ceiling is maximal and ≥ threshold + margin" ; 3) the final verdict
(J4) must rest on a family **proved solvable** by the oracle ; 4) Lesson 45
completes Lesson 44 (budget calibration at the threshold margin) with the
**non-monotonicity** of the ceiling.
