---
lesson: 21
title: "Equality of the observation function is not enough for non-leakage : equality of the STATE MARGINALS is required. And homogeneity of the causal coupling is a prerequisite of M1"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Lesson 21 — Equality of the observation function is not enough for non-leakage : equality of the STATE MARGINALS is required. And homogeneity of the causal coupling is a prerequisite of M1

> Equality of the **observation function** o_t = f(x_t) ∀h does NOT guarantee
> non-leakage : what matters is equality of the **state marginals** x_t (and
> therefore of o_t). If the transition dynamics makes one regime diverge and
> another converge, the marginal of x_t depends on h and the single-frame probe
> alone bills the leakage — regardless of the shape of o. And for E to learn the
> causal coupling, the effect |φ_h(x)| must be lower-bounded (homogeneous, ≠ 0)
> uniformly in x and h.

**Generating fact** (J1 Phase 4, 2026-09-07) : "non-linear regime-dependent
transition" construction (CP order §3.2), o_t = x_t + ε identical ∀h,
transition x_{t+1} = x_t + a·φ_h(x_t) with φ_A = (sin x₁, cos x₂), φ_B =
(cos x₁, sin x₂), φ_C = (tanh x₁, tanh x₂). Despite the identical obs function,
the DISTRIBUTION of x_t differs by regime (tanh does not saturate → C diverges,
|o| p95 = 36 vs 5.6 for A/B ; sin/cos have fixed points → effect ≈ noise) →
**NF frame alone = 0.458 > 0.42** AND non-homogeneous coupling → **M1 = 0.578**.
Two violations : (1) x marginals not equal ∀h, (2) effect |φ_h| not
lower-bounded (0.08 at fixed points vs 0.68 elsewhere).

**Confirmation** (J1 Phase 4 CORRECTION, rotation fields, CP §3.1 — ONE
allowed iteration, the last) : φ_h = R(θ_h)·r(x), r = tanh(‖x‖)·x/‖x‖,
θ = {0°, 120°, 240°}. The effect becomes homogeneous (p50 ≈ 0.20 ∀h, bounded,
non-zero) BUT the marginal still leaks : θ=0° pushes radially → A diverges
(p95=25.4), θ=±120° (cos = −0.5) → B/C collapse toward 0 (p95≈1.3). Rotating the
EFFECT does not make the transition measure-preserving. **NF = 0.474 > 0.42**,
M1 capped (0.496 lin / 0.696 MLP). Lesson 21 confirmed by two independent
constructions.

**Warning signal** : a construction that verifies "same obs function" without
verifying "same state marginals in the dynamics" is doomed to leak — and a
coupling whose amplitude can vanish (fixed points, saturation) never feeds M1.

**Application** (CP 2026-09-07, ABSOLUTE CUT-OFF Phase 4) : any hidden-variable
testbed construction must verify BEFORE any spike, as non-negotiable structural
pre-conditions :
1. **Marginal equality** : distribution of x_t (therefore of o_t) identical ∀h on
   the blind policy — by dynamic construction, not only by the shape of o ;
2. **Coupling homogeneity** : inf ‖φ_h(x)‖ > 0 on the generic support
   (no reachable fixed points, no directional saturation).
Without these two invariants, spike and gates cannot distinguish non-leakage from
the absence of signal. Phase 4 definitively closed on an honest negative verdict :
even with the two vehicles separated (obs = state + noise, coupling =
transition), the testbed does not reach NF/M1 co-satisfaction. The construction
of a non-toy discriminant benchmark for the prediction→behavior conversion
remains open. **Corpus brought to 21 lessons.**
