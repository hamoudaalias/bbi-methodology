---
lesson: 38
title: "When velocity is not observable, one does not invent it : one reconstructs it causally from position (midpoint estimator), and the sliding controller based on this inferred velocity keeps fidelity ≥ 0.9 and robust manipulation — statistically, the agent "sees" almost as well as with ω truth"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Lesson 38 — When velocity is not observable, one does not invent it : one reconstructs it causally from position (midpoint estimator), and the sliding controller based on this inferred velocity keeps fidelity ≥ 0.9 and robust manipulation — statistically, the agent "sees" almost as well as with ω truth

(GENESIS Phase Delta — Partial observation θ only, hidden mass, 2026-09-09,
VERDICT POSITIVE, 448 PASS / 5 FAIL assumed — Lesson engraved by the carrier
at Delta close, discovery of the phase)

**Lesson (frozen formulation) :** *"When a degree of freedom of the system is
hidden (never read), one does not inject noise : one reconstructs it with a closed
causal estimator from the observable variable — in the midpoint, ω̂(t_k) =
(θ_k − θ_{k−1})/dt on the integration mesh — and this reconstructed velocity
feeds all layers (Causal Touch, loop, manipulation) with the same exactness as
the truth : mass error ≤ 1 %, fidelity W/C ≥ 0.9, robust manipulation ±20 %.
The agent also keeps its perceptual purity — E/W/P never read the hidden state."*

**Contexts :** in Alpha/Beta/Gamma the states (θ, ω) were observed ; Delta
removes **ω from the observation space** : the agent reads ONLY θ, the mass `m`
is hidden (b=0.5 known). Question : can one control and infer without ever
touching the velocity? Answer built : yes — by RK4 construction, the sequence of
observed θ is a **bijection** toward ω on the same mesh, and the
`omega_hat_delta` estimator (sealed Δ §3, midpoint) reconstructs it causally
(causal version == full version, tested T_delta_0b).

**Measurements (448 PASS / 5 FAIL assumed, J0 diligence reproduced) :**

1. **Mass inference at ω̂ == inference at ω (worst 1 %, threshold 15 %) :**
   causal Touch Δ (kick ±2.5, coast 500, `m_est = b·Σω̂²dt/(f0−f1)`,
   quadrature aligned by midpoints) — error 0.999 % / 0.521 % / 0.449 %
   (m=1/2.5/4), pair agreement 0.0000 % ; the pair bias is identical to the
   diligence measured BEFORE sealing (reproduction, no recalibration). The
   quadrature must cut each average at the **midpoint** of its interval — a
   half-step offset costs percentages.
2. **A "ω-blind" E-W-C-P-L loop keeps the fidelity** : E reads θ ALONE, W
   predicts from the belief (θ, ω̂) over 2 RK4 steps (surface
   σ=(θ′−θ_c)+0.18·ω̂′), C measures the truth by H0 (the ONLY function
   authorized to read ω), P deterministic argmin. Fidelity ≥ 0.9 per seed (floor
   0.9815 = diligence, min 0.9817), 0 crash/0 NaN, Στ² exactly recomposed. Static
   proof (ast) that E/W/P contain **no** read of the hidden state : perceptual
   purity is not an intention, it is a verifiable assertion of the code.
3. **The adaptive target holds even under ±20 % doubt on the belief** : each seed
   manipulates ITS target `θ_target = arcsin(τ_max/(m_agent·g·L))`
   (tenable : τ_hold == τ_max), band entry reported (up to 52 steps, non-blocking —
   the task is earned more for small masses where the target is set high),
   TERMINAL criterion ≤ 0.10, worst **0.024 rad** 20/20 and **identical under
   m_agent × ±20 %** (60/60). A belief error well above the inferred (±20 % ≫ 1 %)
   does not degrade regulation thanks to the sliding surface (LESSON 36).

**Application :** 1) when a state is not observable, prefer a **closed causal
reconstruction on the integration mesh** (bijection by construction) over any
noisy statistical estimate — the midpoint is the practical key ; 2) guarantee
perceptual purity by a **static assertion** (ast), not by the code's good will ;
3) fidelity and robust manipulation validate the self-taught observer : the
knowledge of a hidden state is not necessary for control if its causal
reconstruction is exact to the step ; 4) a "tenable" target computed by static
equation (max-torque equality) gives an explicit margin and makes the ±20 %
robustness verifiable in both directions. **Corpus brought to 38 lessons.**
