---
lesson: 44
title: "An oracle ceiling close to the threshold is a signal of insufficient budget calibration"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Lesson 44 — An oracle ceiling close to the threshold is a signal of insufficient budget calibration

**Lesson (frozen formulation, CP 2026-09-11) :** *"When the oracle barely caps
above the threshold (margin < 0.05), the test measures the budget constraint, not
the agent's capacity. The budget must be calibrated so that the oracle exceeds
the threshold by at least 0.10. Moreover, the self-retention edges (i,i) must be
explicitly excluded from CS3 scoring or filtered by the agent."*

**Contexts :** Milestone J4 Causal Discovery — sealed evaluation 50 new systems
(seeds 89200-89249), CS1-CS6, B_max=10, amendment A'1, cut-off frozen since J0'.
Verdict **NEGATIVE** published (CS2=0.664 < 0.70 ; 24/50 systems < 0.70), report
digest `79c04ef6…` byte-stable. **CP arbitration 2026-09-11 :** NEGATIVE
confirmed, methodological cause (oracle ceiling 0.729 at B=10, margin 0.029).
Option B recommended (v2 with B_max=15 re-sealed, self-retention (i,i) fix).
Extension not definitively closed — 1st failure, Lesson 41 (2 consecutive
failures = closure) does not apply.

**Measurements (J4 Report, digest `79c04ef6…`) :**

1. **CS2 (recall) fails massively despite excellent precision** : mean CS2 0.664
   (min 0.125 · median 0.714 · max 1.000), 26/50 ≥ 0.70, 24/50 in failure (mean
   0.501), spread over the whole range — dense, not an outlier tail. Mean CS3
   0.938 — precision does not suffer → the deficit is **coverage**, not noise.
2. **The ceiling is first the budget, not the agent** : the R2 oracle itself caps
   at CS2=0.729 with B=10 (barely +2.9 pts above the threshold). BBI=0.664. No
   strategy, including the oracle, crosses the threshold with a comfortable
   margin → the scope is a consequence of the protocol (B_max + internal re-sims
   at F=25 steps), not of a planning defect.
3. **The self-retention edges (i,i) are clean FPs invisible to
   verify_attribution** : on the 6 systems CS3<0.80
   (89202/89208/89212/89216/89229/89247), confirmed (0,0)/(1,1) edges match no
   friction → count in CS3 (min 0.60) but do not appear in
   `false_positive_pairs` (a≠b filter). Alongside the known transitive FPs
   ((0,2)/(2,0), (1,2)/(2,1)) — the Lesson 43 ceiling.
4. **Honesty and sobriety hold perfectly** : CS5 50/50 (0 fabrication,
   indeterminate declared), CS4 50/50 (mean 9.8/10), CS6 10/10 (determinism),
   CS1 0.960 (≥0.80), baselines beaten (BBI CS1 +46.7 pts vs R0, +20.7 pts vs R1 ;
   close to oracle R2 0.973).

**Application :** 1) a sealed evaluation must **pre-register the cut-off and
publish the NEGATIVE without moving any threshold** — the discipline holds as much
for NEGATIVE as for PASS ; 2) diagnose recall and precision separately : coverage
(CS2) is the budget/scope effect, precision (CS3) is local (self-retention +
transitive) ; 3) before concluding on a NEGATIVE, verify the share of
methodological ceiling (oracle under B_max) — here the oracle at 0.729 <
threshold 0.70 + comfortable margin, so the test poorly distinguished coverage
from ceiling → a future seal must allocate free post-B validation edges (2nd
re-confirmation pass) or increase B_max to make the test discriminant ;
4) Lesson 44 completes Lesson 43 (dense direct/transitive ceiling) with the
budget-scope ceiling and self-retention precision ; 5) fixing the (i,i) edge
collection at the attribution step (distinguishing real friction from the
gyroscopic echo) would lift CS3 without touching the thresholds.
