---
lesson: 18
title: "The 1-step tell in the obs frees E : the latent is never forced to factorize h"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Lesson 18 — The 1-step tell in the obs frees E : the latent is never forced to factorize h

> Whatever the parameters of the reactor family, if the trace of h is **readable
> in the obs** (window, velocity, differential), E solves the loss-diff by
> **using the tell directly** (continuous obs features) and **never groups z by
> regime** : M1 (probe z→h) stays 0.34-0.51 for obs→h decodabilities of 0.43-0.82.
> The constraint "make the differential depend on h" is NOT enough — the
> necessary constraint is "make the prediction impossible without h **beyond
> what the obs reveals**".

**Generating fact** (scan Voie A + v4 demonstration, 2026-09-06) : four tested
families — nothing (v2), variance σ (N5 : A2 0.82 / M1 0.49), amplitude κ
(N13 : A2 0.63 / M1 0.35), action→effect table per regime (v4 : A2 0.70 /
M1 0.36, with doubled J2 diff loss proving the mechanism's engagement) —
**the pattern is invariant** : high A2, low M1, z < obs. E chooses the loss
solution that exploits the continuous cues instead of factorizing h
categorically.

**Warning signal** : high A2 (obs→h) ⚠ is NOT a predictor of M1 ; only the
**direct proof** (trained E, probe z→h) counts. An E feasibility pre-test must be
the first step of a J1, before Gate -1.

**Application** : the testbed must **not** leave the h tell in the
1-step/short-window obs ; h must drive a **hidden subsystem** (s_h) whose output
passes through a non-linear/noisy function that the obs alone cannot invert →
predicting o_{t+1} without s_h is structurally wrong → E is constrained to keep
s_h in z → M1 becomes passable (measured, never guaranteed). This is the v5
testbed ("hidden subsystem") submitted in the Design Doc Phase 3 bis.

**ⓘ VALIDATED BY SPIKE (same day, `diag_v5_hidden.py`, dev seeds) :** the
v5 construction passes end-to-end with unchanged E — hidden subsystem s
(AR(1), marginal σ=1 identical ∀h), probes w = s²−1, regime = pairs of slopes
(ρ₁,ρ₂) permuted over 2 sensors, common T/P room. Frame non-leakage 0.32 ≤
0.42, window+velocity richness 0.86/0.83, **M1 z→h 0.78-0.84 (lin) / 0.82-0.84
(MLP) on 3 E configs** — the first construction in the whole falsification to
satisfy non-leakage + richness + M1 ≥ 0.70 simultaneously. The sufficient
condition is not "make the diff h-dependent" but "make the next-step
prediction impossible without H state".

**ⓘ GENERALIZATION — Transposing a spike into a physical arena can degrade M1 :
the arena's alternative cues free E from h factorization** (J2v5, 2026-09-07) :
W-HORIZON on the v5 testbed transposed into the PROCCH arena (obs 66-d, no h
tell in the frame, common T/P room, H0, sealed seeds 21750-21999, holdout
21950-21999). W_corr holdout=0.440 (> 0.2) and amp_ratio=0.425 (≥ 0.25) pass,
but **M1 z→h holdout = 0.387 lin / 0.414 MLP** (< 0.70), G_corr 0.026
(quasi-random). The convergence table (n_ep ∈ {50,125,200}, epochs ∈ {5,10,20})
shows a **structural plateau** : M1 min(lin,mlp) stays 0.36-0.42 and rises neither
with B nor with epochs, while W_corr (0.249→0.359) and amp_ratio (0.373→0.492)
grow monotonically with B. This is not a budget problem : the encoder does not
extract h from the available signal because the common physical dynamics provide
sufficient alternative continuous cues to predict the 1-step differential
**without encoding h**. The factorization guarantee is not transferable from a
synthetic spike to an arena ; a spike passing M1 ≥ 0.70 is NOT a guarantee that
the transposition will pass (spike v5 passed M1 0.78-0.84, the arena drops it to
0.39-0.41).
