---
lesson: 41
title: "In visual perception, enriching the encoder does not erase the structural loss in strong dynamics : after two successive failures on distinct provisioned thresholds, definitive closure is the default working hypothesis — the credibility cost of a third failure exceeds the marginal gain of a recalibration"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Lesson 41 — In visual perception, enriching the encoder does not erase the structural loss in strong dynamics : after two successive failures on distinct provisioned thresholds, definitive closure is the default working hypothesis — the credibility cost of a third failure exceeds the marginal gain of a recalibration

(Extension Perception Visuelle v2 — J3, C4 W/C fidelity, 2026-09-10, VERDICT
NEGATIVE, C4 0.8637 < 0.88, cut-off triggered, NO J4, CP decision)

**Lesson (frozen formulation) :** *"In visual perception, enriching the encoder
(restoring ω̂ on three independent chains) improves observability but does not
remove the structural loss in strong dynamics : the quantization residual of the
64×64 codec on the massive seeds subsists. A second failure, with a provisioned
threshold (Lesson 40) still above the true performance on the eval allocation, is
a cumulative signal : after two successive failures, definitive closure becomes
the default working hypothesis — measuring once more costs credibility more than
it delivers information."*

**Contexts :** v2 corrected the root cause identified in v1 (spatial encoder E
under-quantified ω̂ → `missing=['omega']`). The spatio-temporal encoder (z ∈ ℝ¹²,
ω̂_e/ω̂_flow/v_c/κ/ψ, temporal memory) restores the dynamics ; the C4 threshold was
provisioned from 0.9 → **0.88** (CP decision, Lesson 40). Result : **0.8637 <
0.88**, gap −0.0163 (larger than in v1, −0.0042). The sealed reference (EXACT
diligence code, same range) = 0.8702 — this time the **P loop no longer beats the
passive reference** (−0.0065). The profile stays identical to v1 : 7 massive seeds
(m > 3.5) → 0.65–0.86 (mean 0.7367), light seeds → ~1.0 ; 9/20 pass ≥ 0.88.

**Measurements (2000 cycles, 20 seeds × 100, 86028..86047, digest `ff053f23…`
byte-stable 2 runs) :**

1. **The encoder enrichment worked (ω̂ restored) but the fidelity dropped** :
   v2 removed `missing=['omega']` (3 ω̂ chains), yet C4 = 0.8637 < v1 0.8958. The
   channel was not the only limiter : on the massive seeds, the **loss is in the
   angular-velocity differential measured by C** (64×64 re-render), not only in
   the encoding.
2. **The threshold provisioned per Lesson 40 was still too optimistic** : 0.88 > 0.8702
   (sealed ref. same range) — the margin that had to be provisioned is ≈ 0.85–0.86,
   not 0.88. A 2-point gap on the provision, discovered again at J3.
3. **The profile stays identical (structural, not artefact)** : two encoder
   versions, two seed allocations, same massive/light cluster split ⇒ the loss is
   inherent to the perception chain, not repairable by a third encoder without
   rethinking the resolution/tolerance.
4. **The credibility cost of a v3 is asymmetric** : marginal (possible) benefit of
   a third success < cost of a third NEGATIVE. After two failures, definitive
   closure is the default option ; the v3 amendment (re-provision at 0.85–0.86)
   must be motivated by the carrier, not de facto.

**Application :** 1) a provisioned threshold is a **hypothesis**, not a
foundation — provisioning does not guarantee ; plan from J0 the cost of re-measure
on the eval allocation ; 2) two successive failures at distinct sealed thresholds
= cumulative closure signal (no "move the threshold and re-measure" without
explicit carrier deliberation) ; 3) the negative verdict and the range's sealed
reference are part of the deliverable from J3, never after the fact ; 4) only the
carrier opens a v3 — never by recalibration alone.

---
