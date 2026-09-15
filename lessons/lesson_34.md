---
lesson: 34
title: "The causal floor : causality requires at least one intervention ; no passive observation reveals magnitude, the effect is state-dependent and does not calibrate outside its state"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Lesson 34 — The causal floor : causality requires at least one intervention ; no passive observation reveals magnitude, the effect is state-dependent and does not calibrate outside its state

(Phase 15 — Dimensional Programme / Scale Probe, 2026-09-08, VERDICT NEGATIVE, 364 PASS / 5 FAIL assumed — formulation FROZEN by Chef CP)

**Lesson (Chef's frozen formulation) :** *"The causal floor : causality requires
at least one intervention. No system can infer the causal structure of a domain
from passive observation alone, because the causal effect is state-dependent and
is only revealed by intervention."*

**Generating fact** (Phases 14-15, 2026-09-08) : Phase 14 fails by magnitude
blindness ; Phase 15 (Scale Probe) corrects the magnitude in z0 — a single H0
pair measured by direct intervention on the domain — but the effect varies
between states : **the calibration does not transfer** (E 18/20 fall back into
cold at 16 pairs, F 16/20). Causal few-shot transfer (Phase 13, Kw=1.0, ×16 gain)
is **close to the theoretical minimum** : 1 H0 pair = floor (first intervention) ;
zero-shot is **fundamentally out of reach** — not a BBI limitation, a property of
causal inference.

Four measured facts underpinning the lesson (sealed J0 v1.2, frozen seeds,
`data/phase15_scale_transfer_results.json`) :

1. **The Probe corrects the magnitude locally (z0), and the guard's silence IS
   the proof.** On F, the probe (1 H0 pair : a_probe vs a_null on z0,
   scale_gain = ‖Δz_probe‖/‖a_probe‖) produces scale gains ×1.3 to ×11.7
   (mean ≈ ×4.5) ; the calibrated head g=g_cal leaves 4 seeds in `pure bet`
   without triggering. Live ablation (T_scale_5) : replaying these 4 seeds in
   g=1.0 (**without probe**) makes the magnitude guard trigger on 4/4. The
   "silence" was the calibration, not permissiveness — the Direction is now
   learned by intervention, not only alignment.
2. **The magnitude guard replaces the alignment guard — and proves the
   alignment guard was blind.** Bounds ‖Δ̂(z)‖ ∈ [1/3, 3]×‖v_c_true‖
   (T_mag_1/2/3) : effect ×5 too big OR too small → trigger, ×2 → silence at the
   exact threshold. Replayed on Phase 14 (T_mag_4), it would have caught the ≈×5
   magnitude that alignment alone had missed. False zero-shots go from **24 (P14)
   to 3 (P15)** — including **0 on RAD-C**, and the 3 remaining (all on B) are
   **documented floors** (Option B, Chef J2 decision : 70201 `structural_blind`,
   70203/70206 `sporadic_absorbed` — effect not representable by 1 H0 pair, not a
   guard failure).
3. **The causal effect is state-dependent : calibrating in z0 does not transfer
   outside z0.** F : 4 pure / 16 cold — the 2 cold heads capable of the target
   cap at fid 0.0616 < target 0.052 (T_scale_4 : fid_part ✓ but mean K_F=5.25 >
   3.0 ✘, cut-off > 5.0 triggered) ; E : 2 pure / 18 cold — mean K_E = 15.3 >
   11.2 (C4 non-regression ✘) ; B : 3 pure / 1 warm / 16 cold ; RAD-C : 0 pure /
   5 warm / 15 cold. The gain measured in one state only holds for that state —
   the z0 intervention reveals the domain's magnitude in z0, not its magnitude
   map.
4. **1 H0 pair = floor (first intervention), below it : causal inference does not
   start.** The observable Phase 13 → 14 → 15 difference is clean : few-shot ×16
   (Kw=1.0 ≥ 1 counterfactual H0 pair) → zero-shot 0 pair : refuted twice
   (Phase 14 : frozen hypothesis; Phase 15 : local calibration then
   state-dependence) — by TWO measured DISTINCT mechanisms, which is not a
   methodological coincidence but the bound of causality. E 18/20 and F 16/20
   fall back into cold at 16 pairs : the z0 calibration does not "transfer" into
   cold any more than it replaces cold.

**Warning signal :** a pre-registered failure that is measured and published does
NOT sanction — it protects. The FAIL T_scale_4 (mean_K_F 5.25 > 3.0 from the
sealed JSON) and T_scale_6 (3 B false ≠ 0) PROVE the protocol is falsifiable :
they fail because the measurement really showed 5.25 > 3.0 and 3 false. Weakening
an honesty test to "pass" would destroy exactly what ×1 → ×2 → ×3.95 → ×6.40 →
×16 has built : the proof. Causality is not bought on credit : a system that has
NEVER intervened cannot have a magnitude — the Probe is the minimum intervention,
the floor is 1 H0 pair.

**Application :** DO NOT attempt a "smarter" causal zero-shot : the bound is
the property, not the protocol. Few-shot with **≥ 1 counterfactual H0 pair per
state** (or per group of similar states — clustering of the z space, not of the
domains) is the next licit tier ; calibrate a Probe on SEVERAL states and verify
the stationarity of the scale_gain before any transfer ; treat any single-state
calibration as local, never global. **Corpus brought to 34 lessons.**

---
