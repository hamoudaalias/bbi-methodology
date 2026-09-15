---
lesson: 36
title: "Inference precision transfers integrally in closed loop : an exact belief makes the world transparent (fidelity 1.000), and the right measure of an already-satisfied task is its real cost, not a flattering simulation"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Lesson 36 — Inference precision transfers integrally in closed loop : an exact belief makes the world transparent (fidelity 1.000), and the right measure of an already-satisfied task is its real cost, not a flattering simulation

(GENESIS Phase Beta — 2-Segment Arm with Hidden Terminal Mass, 2026-09-09,
VERDICT POSITIVE, 402 PASS / 5 FAIL assumed — Lesson engraved at J0 seal §9,
confirmed by the Chef at Beta close)

**Lesson (Chef's frozen formulation) :** *"When W and C measure the same causal
quantity, an exact belief makes the world transparent (fidelity 1.000). And the
right measure of an already-satisfied task is its real cost (n_steps = 0), not a
flattering simulation."*

**Generating fact** (J0-J4, 2026-09-08→09) : the planar 2-segment arm with
hidden terminal mass (m2 ∈ [0.5,5.0], the only hidden parameter) is a new tier :
4-dim state space, coupled inertias, unlike the 1-DOF pendulum of Alpha. Three
observations :

1. **A single H0 pair still suffices in multi-DOF** : from rest, the
   counterfactual probe a=7=(+2.5,0) vs null a=4=0 reveals m2 through the **W grid**
   {0.50..5.00, step 0.01} — error **0.00 %** (mean=max) on 30/30. Lesson 34
   alive : causality is an intervention, not an observation, and its state
   dimension hardly matters when the intervention is clean.
2. **The Causal-Touch belief (0.00 %) makes the W/C loop transparent** : 2000
   cycles (20 seeds × 100), **0 crash, 0 NaN, fidelity W/C = 1.000 (min=max)** —
   prediction and measurement are identical. Perfect inference eliminates the
   belief/world gap : the planner sees the true dynamics at 2 steps.
3. **The already-satisfied task is measured by its real cost, not by a fake
   progress** : the rest start (defensive convention §4.1) is **already in the
   band** ‖rest−q_target‖ = 0.1131 < 0.15 — exactly the "worst 0.1131" predicted
   by the J0 diligence. C5 passes in **0 steps** : reached_steps=0, 0 torque
   injected (NULL optimal at equilibrium). T_beta_6c traces the raw measure
   (error == ‖rest−target‖), without inflating the task or inventing steps.

**Recorded limit (strategic vigilance point, Chef decision) :** the **2-step**
predictive planner does not recover **out-of-band** states for heavy masses
(perturbed start q=[0.25,−0.25] → 4/20, min 0.1413, the heavy ones oscillate,
final error up to ~3 rad) — measured as a **non-cut-off** extra, published in the
report §4. It is a real architectural limit (planning horizon) to address for
complex manipulation tasks, not a phase failure.

**Application :** 1) an exact inferential belief (Causal-Touch W grid or
equation) must feed the W planner as-is — W/C fidelity is then a **measure of
the inference quality**, not a tax of the loop (T_beta_5 audits E/W/C/P/L per
cycle) ; 2) an objective already satisfied by the start state (band, defensive
convention) is declared **reached in 0 steps, cost 0**, traced honestly, and the
physical point (no torque at equilibrium) is documented — never rebuilt into a
fictional demonstration ; 3) distinguish in the report **sealed conformity**
(what the contract requires) and **measured limit** (what the method does not yet
cover) — both published side by side, only the first decides the verdict.
**Corpus brought to 36 lessons.**
