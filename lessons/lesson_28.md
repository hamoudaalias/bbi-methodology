---
lesson: 28
title: "A causal" transfer "is measured by the resolution of its sampling protocol, not by its promises"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Lesson 28 — A causal" transfer "is measured by the resolution of its sampling protocol, not by its promises

(Phase 9 — Chantier 4, 2026-09-08, verdict REFUTED, 299 PASS / 0 FAIL)

**Lesson :** *a" ×10 on the sample "memory-transfer claim is only falsifiable if
the measurement rule resolves below the typical sampling scale of the domain.
Otherwise the floor of the" sustained fidelity "window returns ratios == 1.0
for both arms — and the experiment says nothing.*

Three traps encountered and fixed, each a PROTOCOL artefact and not a model one :

1. **Unbounded drifting latent** : without re-sampling the state at each cycle,
   effects accumulate linearly (z ~ 200 instead of ±1), the fit envelope
   de-conditions and the affine head extrapolates (chain rollbacks). The protocol
   must reinitialize the state distribution as the real world does (regime). That
   was the real"bug"— not the model.

2. **Zero-effect pairs in the fidelity metric** : the rest action has
   `Δtrue ≈ [0] + noise` ; a ratio |Δhyp−Δtrue|/|Δtrue| is ill-posed there and
   artificially sinks the average (0.97 → 0.39). CAUSAL fidelity is defined on
   effect actions ; the rest's non-leakage is judged by the BASE error, not in the
   same window.

3. **Window floor > sampling scale** : with SUSTAIN_WINDOW=100 pairs, two
   disciplines converging in ~20-60 pairs (affine and bias-only, clean data) both
   cross at index 100 — degenerate ratios 1.0, unfalsifiable criterion. Lowering
   the sustain window to 15 (resolution below the scale), arm B crosses at
   12 280 and A at 25 : the experiment becomes able to DISCRIMINATE again, and
   the verdict (REFUTED) becomes a conclusion, not noise.

**Warning signal** : a validation quantity whose floor is coarser than the effect
it claims to measure — any" sustained fidelity over N "with N large compared to
the useful sampling size of the domain.

**Application :** the meta-causal A→B transfer reduces the VARIANCE of the
hypothesis class (Wm≡0, constant), honestly refuses radical structures
(T_meta_4), and re-trains neither E nor W — but the criterion" ≤ 10 % of B's
data cold " is NOT verified on the linear Domain B : the cold affine class reaches
it at the same index. **Corpus brought to 28 lessons.**

---
