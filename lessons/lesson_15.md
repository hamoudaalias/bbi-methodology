---
lesson: 15
title: "A mono-parametric h signature is insufficient for a bottleneck encoder"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Lesson 15 — A mono-parametric h signature is insufficient for a bottleneck encoder

> If the hidden variable h differs between regimes by only one parameter
> (e.g. : a delay), an encoder with a dimensional bottleneck (36→16) and a
> contrastive reconstruction objective cannot separate it linearly at ≥ 70 % in
> the latent. The h signature must be **multidimensional** (e.g. : amplitude +
> delay + target + noise, coupled) to be linearly decodable.

**Generating fact** ([[Report J3 — GATE 0 PROCCH (verdict)]], 2026-09-06) :
Gate 0 PROCCH v2 failed **5/6**, only M1 missing — probe z→h = **47.5 %** < 70 %,
and **z < raw windowed obs (52.9 %)** : the encoder *harms* the encoding of h.
Structural cause : in PROCCH v2, common κ, common target, common noise — **only
the delay L_h ∈ {5,3,1}** distinguishes regimes. Such a thin temporal signature,
seen through the 36→16 bottleneck of a contrastive-reconstruction encoder, is not
linearly separable. In parallel, the **representation/interaction decoupling**
appears (c4 ✅ : cumulative interaction predicted — corr 0.469, amplitude 0.681 —
without c3 passing) : predicting an interaction ≠ inferring h.

**Warning signals** : (1) E decodes h *worse* than the raw windowed obs (z <
raw) ; (2) the regimes differ by only one dynamic parameter (e.g. L_h) ;
(3) single-frame probe ≈ chance but windowed probe < 60 %.

**Application** : any testbed with a hidden variable h must verify that the h
signature is multidimensional BEFORE submitting Gate 0. A linear-decodability
pre-test — **probe on raw windowed obs ≥ 60 %** — must precede Gate 0 (while the
**single-frame** probe must remain ≈ chance ≈ 1/3, non-leakage preserved). The
expected hierarchy : frame ≈ chance < window ≥ 60 % ≤ z (Gate 0 M1) ≥ 70 %.

**Contribution** : Lesson 15 engraved (corpus brought to 15). The Phase 2 M1
addendum was NOT transposed : it required prior proof that E encodes h
(prerequisite absent here — structured CP refusal on 2026-09-06).
