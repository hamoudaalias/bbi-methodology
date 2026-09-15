---
lesson: 48
title: "Stabilizing toward a pre-computed target reveals a limit distinct from the declarative agreement (fidelity)"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Lesson 48 — Stabilizing toward a pre-computed target reveals a limit distinct from the declarative agreement (fidelity)

**Lesson (frozen formulation, CP 2026-09-12) :** *"Active stabilization toward a
pre-computed target (manipulation) reveals a limit distinct from declarative
fidelity (perception). The loop can verify the causal differential (W/C agreement)
without being able to stabilize a demanding target on a quantified channel without
state feedback. From now on, distinguish, in the manipulation criteria : verify
(W/C agreement) and stabilize (reach the target state). A PARTIAL verdict on
manipulation is not a perception failure."*

**Contexts :** final milestone **J4 of the Perceptive Encoder Extension**
(2026-09-12). Sealed evaluation on **virgin** Eval families (A 90048-57 · B
90078-87 · C 90108-117), CE4/CE5 mechanisms locked by CP via [[Addendum J4 — Perceptive Encoder — Evaluation Corpus CE1..CE5 (case→seed mapping 128→120, traps PP1..PP7)]] v1.1 (imprint §9 excluded `ecf3dfd5…`). Report
`data/perceptif_J4_report.json` digest `20b4b515…` byte-stable, J4 audit 6000
records. **Verdict PARTIAL ×3 validated by CP ; extension closed on PARTIAL
(0 NEGATIVE path → Lesson 41 not applicable) ; CE5 arbitration : no controller
adjustment, no immediate v2 (carrier's later decision).**

**Measurements (J4 Report, digest `20b4b515…`) :**

1. **CE4 (verify the causal differential) PASS 3/3 on 120 cases** : W/C fidelity
   per path **A-modal 0.9196 · B-geom 0.9415 · C-sample 0.8473**, threshold
   ≥ 0.80 **AND** > R1+0.05, N1..N4 ; `window_too_short` (W=8<M=16) **counted** in
   N4 path A rather than padded ; path C fidelity discrete invariant to window
   (min 0.6733 published, no point masked). **Perception works.**
2. **CE5 (stabilize toward θ_target) PARTIAL ×3** : pre-registered objective
   **10/10 NOT reached** — **A 1/10 · B 1/10 · C 2/10** (seeds 90054 · 90086 ·
   90108/90111), θ_target = arcsin(τ_max/(m̂·g·L)) 0.06..1.57 rad, **0 fallback**
   m̂→2.75, final error \|θ(50)−θ_target\| often 0.1..0.4 rad > 0.1. Most seeds
   **approach** the target but the P-L regime does not stabilize ≤ 0.1 rad in 50
   steps on a quantified channel **without state feedback** — **structural** loop
   limit, not a perception failure.
3. **All CP conditions documented** : read gap 20→10 (§5.1 Addendum) · N2..N4
   asymmetry (CE4 in count, CE5 out of count) · canonical perturbed start (not
   C5a-rest) · `theta_target=0.0` defect → **replay T6 bit-identical 60/60 vs J3**
   proved.
4. **Traps PP1..PP7 (60, out of cut-off) : published honesty statement** —
   PP4/PP6 refusal 15/15 and 6/6 (100 % detected), PP1 6/6 ; published limits
   PP2 2/6 detected (33 %), PP5 4/6 (67 %), **PP7 torsive distortion in phase
   1/6 (17 % — the least detected, consistent with J2's temporal de-projection)**.

**Application :** 1) **separate in any future seal** "verify the causal
differential" (W/C agreement — CE4) from "stabilize a pre-computed target"
(active manipulation — CE5) : distinct criteria, distinct difficulty classes,
independent thresholds — a PARTIAL on one does not contaminate the other ;
2) read the verb stabilize as "the state reaches a target in a bounded number of
steps" and measure it at the **final error at the last step** (not "reached
once") — the bounded-step reading is the only one faithful to manipulation ;
3) before concluding on a stabilization failure, check whether the constraint is
structural (1-bit quantified channel without state feedback, step budget) — a
possible v2 must change **the channel** or **the feedback**, not the controller ;
4) Lesson 48 completes Lesson 47 (averages masking heterogeneity) and Lesson 42
(mono-variable prediction) with the **perception/manipulation distinction**.
