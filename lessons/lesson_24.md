---
lesson: 24
title: "Online learning of a World Model has a golden rule : majority persistence + a living counterfactual reference (H0), not spikes nor a score"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Lesson 24 — Online learning of a World Model has a golden rule : majority persistence + a living counterfactual reference (H0), not spikes nor a score

A causal model learning online by receiving the world as it drifts learns in fact
**nothing safe** : the only measure that separates a true dynamics change from a
whim of the wind is the **counterfactual** error — the gap between the
hypothetical Δ predicted `W(z,a) − W(z,a_null)` and the true Δ measured on the H0
branch `z_true − z_null`. Layer C (already judging False Urgencies and
Auto-Illusions) then becomes the **guardian** that authorizes or forbids the update
of W's weights.

**Generating fact** (Chantier 1 Phase 8, 2026-09-07) : the Rust core only exposes
**E+W** trainings (no W-only) — counterfactual or not, `train_*` moves the
encoder. Two ways collapse : (a) calling `train_*` on a drift buffer ⇒ the encoder
migrates and breaks the latent semantics for C and P (catastrophic forgetting,
Lessons 6/22) ; (b) fitting on the **reward** ⇒ the model learns to anticipate
scores, not effects. The safe path is an **additive residual Python head**
`W'(z,a) = W_rust(z,a) + G(z,a)` in the frozen latent space : the update never
touches E (proved by `encode` bit-identity), and the ridge least-squares target
is the causal effect H0.

Three guardrails make the update **safe**, not just possible :
1. **Majority persistence** — never an isolated spike : the trigger is validated
   only by the majority of the last k ticks (Lesson 6). Noise is a knight, not an
   emergency.
2. **Layer C gate** — a persistent error on a background of False Urgency
   (high u_ext, effect ≈ 0) stays **blocked** : one does not learn on a phantom
   alert.
3. **Anti-regression rollback** — refit on a window of contradictory pairs
   (regime collision : 60 pairs of one regime, 8 of another) that would degrade
   the average LIVE error beyond tolerance ⇒ **bit-identical restoration** of the
   previous head. The guardian never self-destructs ; it waits for a cleaner
   reference frame.

**Warning signal** : a "the fit corrected" test satisfying `assert w_call ≈
z_true` with pairs whose `z_true` and `z_null` receive the SAME offset — the
relative error is zero because Δ stayed 0, not because the model was learning.
The drift must be carried by the **EFFECT DIFFERENCE** (true Δ ≠ base Δ)
otherwise the test measures wind (cf. T_guard_4 vs T_guard_2).

**Application** (Chantier 1, 2026-09-07, 260 PASS / 0 FAIL) : for each online
micro-update of W, (1) the trigger requires the counterfactual error above the
threshold AND the persistence majority — never a spike ; (2) the gate remains
submitted to Layer C (False Urgency ⇒ blocking) ; (3) the refit is validated by
anti-regression rollback (bit-identical restoration of the previous head). E is
never touched (`encode` bit-identical before/after). **Corpus brought to 24
lessons.**
