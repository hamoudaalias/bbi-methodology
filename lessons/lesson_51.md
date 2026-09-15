---
lesson: 51
title: "Explicit damping in the band moves the stabilization limit, does not remove it (PARTIAL at the published floor)"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Lesson 51 — Explicit damping in the band moves the stabilization limit, does not remove it (PARTIAL at the published floor)

**Lesson (frozen formulation, CP 2026-09-14) :** *"On a hidden-mass testbed with
capped torque (τ_max = 5.0), adding explicit damping to layer P — ω̂_LONG (sliding
window W_CAP=32) + a MAINTAIN-vs-APPROACH phase separated by a threshold γ in the
band — moves the stabilization limit without removing it : 10/30 (n_judges 30,
0 π/2 diag) vs reproduction floor 9/30 (CE5 v2 baseline on block 92xxx), i.e. +1,
far below the POS ≥ 25/30 threshold. The PARTIAL verdict is published as-is,
cut-offs invariant."*

**Contexts :** workstream **Damped Stabilizing Controller (Lesson 49)** — Design
Doc [[Design Doc Damped Stabilizing Controller J0 — Explicit damping in Layer P
(Lesson 49)]] sealed J0' (spec `cc0e662b…`, diligence D1-D5 PASS), suites J1 → J4 :
**J1** ω̂_LONG + wired policy (10 bit-identical dev, sha suite `3747978d…`),
**J2** v2 baseline non-regression replayed ×2 in independent processes == digest
**`ddf23cea…`** bit-identical (pristine loop `2c1b074d…`), **J3** JSONL audit 20
dev (fixed keys, 0 NaN, ×2 bit-identical, digest **`3e17453d…`**) + eval-virginity
scan, **J4** virgin eval 93_000-93_029 (report digest **`809838ec…`**, audit
`843252e0…`, commit `d445927`) — see [[Damped Stabilizing Controller J4 Report —
PARTIAL verdict (10 out of 30) over virgin eval 93000-93029]].

**Measurements (J4 Report — verdict PARTIAL) :**

1. **10/30 ≤ PARTIAL threshold (10-24), POS (≥ 25) not reached** : n_judges 30,
   n_diag_π/2 = 0, 0 m̂ fallback, 0 NaN, ×2 bit-identical determinism per seed
   (integrated auto-replay).
2. **BIMODAL failure structure (not a single bottleneck)** : the 20 failures span
   the whole m̂ axis 0.52-4.72 — 11/12 failures in **light regime** (m̂ ≤ ~1.9 :
   light arms over-correct, residual oscillation, error 0.16-0.58 rad) AND 9/18
   failures in **heavy/very heavy regime** (m̂ ≥ 2.33, including the two most
   massive 4.57 and 4.72 : the τ_max=5.0 torque saturates and the target is
   under-reached, error 0.10-0.26 rad) ; the 10 successes concentrate in
   **intermediate inertia** (8/10 in [2.3, 4.4], median ~3.5, error 0.004-0.061
   rad). The damping helps precisely where the CE5 v2 cases already succeeded :
   extending τ_max alone only touches the heavy tail, not the dominant light
   regime.
3. **ω̂_LONG never imputes** : window < W_CAP → None (never an average over an
   incomplete window) ; 0 cycle where θ_target exceeds τ_hold ; traps PP1..PP7
   30/30 with 0 NaN, bounded torque, and the pathological failure PP7 (m̂=0.5 →
   θ_target=π/2) **published** (echec_honnete).
4. **Controlled v2 → controller contrast** : the rich v2 channel had solved
   perception (CE4 saturated 1.0) but not stabilization (CE5 9/30) ; injecting the
   damping adds +1 — but the target falsification (≥ 25/30) fails on the **two
   extreme regimes**, not on information : neither channel nor damping covers the
   full testbed. **Post-closure erratum** : the first reading "failures = high
   masses + torque margin" was wrong (9/20 failures have m̂ ≥ 2.33) ; measurement
   and digests unchanged, only the interpretation was corrected.

**Application :** 1) **a stabilizing policy is not judged only by its finesse in
the band, but by its reach over the WHOLE inertial axis** — pre-declare the two
regimes (light-arm over-correction, heavy-arm torque saturation) and cover them
separately (a single design variable — τ_max or γ — cannot target 25/30) ;
2) **a PARTIAL at the floor is an honest reproduction, not a result** — publish
the raw score, the baseline link, and the complete m̂ mapping of failures (not a
sorted tail) ; 3) **any relaunch goes through a J0 + D1-D5 diligence, never a
post-measurement γ/τ tuning** (Lesson 30) ; 4) Lesson 51 completes Lessons 49-50
with **the scope of the stabilization problem : the damping moves the reference
within an inertia window, it does not remove the two extreme limits**.
