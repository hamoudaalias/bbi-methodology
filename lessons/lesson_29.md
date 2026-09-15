---
lesson: 29
title: "Comparing causal structures requires a physical detector, not a sampling heuristic"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Lesson 29 — Comparing causal structures requires a physical detector, not a sampling heuristic

(Phase 10 — Chantiers 1-3 + J4, 2026-09-07, verdict VALIDATED, 308 PASS / 0 FAIL)

**Lesson :** *the abstraction of a domain is only reliable if each invariant is
derived from a PHYSICAL signature of the system (jacobian, coupled branches,
persistence), not from a sampling-shape heuristic (alternation, means) —
otherwise the detected structure depends on the sampling cadence, and two
identical domains can be declared dissimilar.*

Three examples measured in this phase, all corrected toward the physical
signature :

1. **The invisible oscillator at φ=0.46 rad/step** : the initial detector
   ("alternation of increments > 0.30") is blind to B's regime — sampling
   frequency fine compared to the period (≈13.6 steps), the consecutive
   increments keep the same sign between half-periods (alternation ≈ 0.15 < bar).
   The honest signature : the **complex mode of the free jacobian** (LS fit
   `z_{t+1} = M·z_t`, conjugate eigenvalues) — exact at any cadence under Nyquist,
   and null for A's persistent latent (M = identity).

2. **The radical effect masked by the H0 oracle** : measuring effects via
   `make_h0` (oracle of domain B) would have given the Radical the same sheet as
   B — the oracle is the pure truth of the DOMAIN, not what a coupled agent
   observes. The honest measurement : **coupled branches** (snapshot → step(a) →
   encode ; restore → step(0) → encode) with SIGNED vector constancy
   `||mean Δ||/mean||Δ||` — which accounts for direction reversal
   (0.07 for the Radical, 1.0 for B).

3. **Similarity dominated by shared topology** : an unweighted cosine puts
   A↔RAD at 0.52 (above the 0.50 refusal bar) because the SHARED invariants
   (state, accumulator, cause_effect, rest) dominate the dot product. The honest
   separation comes from the **fidelity topology** (effect_constant vs
   state_dependent, learnable vs flat) : it is the part of the structure that
   decides whether A's hypothesis class is LEGAL on B — therefore it must dominate
   the similarity (weight 8 vs 1 for dynamics). Measured result : sim(A,B)=0.995,
   sim(A,RAD)=0.379.

**Warning signal :** an invariant detector whose verdict depends on the
period/sampling-step ratio, or an abstract similarity dominated by invariants
that do not DISTINGUISH the domains.

**Application :** on this abstraction, the transfer decision is honest with three
outcomes (transfer/refusal/uncertain), the Radical is refused TWICE (similarity
0.38 < 0.50 AND explicit constant-vs-state-dependent contradiction), and the
sampling gain measured by minimal-K protocol is **K_warm/K_cold = 0.48**
(1.75 vs 3.62 pairs, 40 seeds) — half, not the literal factor 10 : the falsifiable
quantity is the RATIO, not the percentage of a window floor. **Corpus brought to
29 lessons.**

---
