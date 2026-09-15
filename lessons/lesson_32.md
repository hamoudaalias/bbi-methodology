---
lesson: 32
title: "LEARNED causal abstraction transfers better than hand-coded abstraction : classes discovered by clustering on H0 traces capture the transversal structure of domains, not their specificities"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Lesson 32 — LEARNED causal abstraction transfers better than hand-coded abstraction : classes discovered by clustering on H0 traces capture the transversal structure of domains, not their specificities

(Phase 13 — Learned Causal Abstraction ACH-L, post-closure, 2026-09-08, VERDICT SUCCESS, 336 PASS / 0 FAIL)

**Lesson :** *a CLASS abstraction discovered by learning (clustering on the H0
traces of a mastered intersection, frozen spectral projection, zero manual
extractors) transfers MORE causal structure than a hand-coded abstraction
(N1/N2/N3) : the learned class warms E at K_warm=1.0 — i.e. each effect-prediction
adaptation costs 1 pair instead of 16 cold (gain ≥ ×16, cold not reached within
the window). The classes are transversal ("cluster 0" = C and E, D and A
according to the H0 structure), they are universals of causality — not coded
domain specificities.*

Three measured facts underpinning the lesson :

1. **Learning beats the extractors** : the ACH-L representation comes from
   `AbstractionLearner` (spectrenorm + relmag + H0 align, k=3, ARI=1.0 on
   re-freeze, frozen SVD projection and FROZEN codebook SHA-256) — NO N1/N2/N3
   extractor in the loop (T_mapL_1/2, inspection import). The warm head is a
   centroid of the class's `v_c_true` (probe-stabilized pairs), magnitude alone
   adapted on the target by least squares bounded in [1/1.5, 1.5]. On E
   (pre-registered spec SHA `bacacae3…`, 20 seeds), K_warm=1.0 deterministic
   (20×1) vs K_cold=16.0 capped (20×16) → **16.0× gain in ≥ bound** (cold does
   not reach the target within the window ; relative target 0.154 vs ceiling
   0.193).

2. **The learned class REPLICATES and EXCEEDS Level 3** : the C control
   (M/M/1 queues ×2, non-regression) goes from ×6.40 (Phase 12, N3 anti-phase
   head, K_warm=2.5) to **×16.0** (ACH-L class 0, K_warm=1.0, coherence 0.90,
   fidelity gates 1.11/gain 1.21 within bounds). The learned abstraction re-finds
   the symmetry structurally (projection+clustering), not by a symmetry code —
   same class improvement, without design bias.

3. **Honest refusal becomes STRICTER than at Level 3** : B-oscillator and
   RAD-C are refused by the gates (B : fidelity 6.75 ≫ 1.7 ; RAD-C : gain 1.92
   ∉ [0.67,1.5]). Above all, **D (3-queue network) is REFUSED** (coherence 0.52 <
   0.70) while Level 3 transferred it (×2.37) — documented diagnosis : ACH-L
   refuses the transfer the N3 portal accepted. This is the cost of generalization,
   quantified, not hidden : when the learned projection does not confirm the class
   on the target, the honest decision is cold.

**Warning signal :** a gain capped at 16 within the window must NOT be read as
"exactly ×16" : it is a ≥ bound. Reporting "×16" without the bound turns a
cold non-achievement into absolute performance — the same reflex that corrupts
the cut-off. The honest formulation : "K_warm=1.0 deterministic, cold capped at
16, gain in ≥ bound ×16".

**Application :** to transfer causality, LEARN the CLASS (projection + clustering
on H0 traces) rather than coding the abstraction ; the magnitude adapts on the
target, the direction is the class centroid, refusal is decided by the gates
(fidelity ≤ 1.7, gain within bounds) AFTER the projection — never by a hand
re-verified symbolic portal.
