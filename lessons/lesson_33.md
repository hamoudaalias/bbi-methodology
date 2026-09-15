---
lesson: 33
title: "An Auto-Illusion guard must check alignment AND magnitude : a directionally correct but wrongly-amplitude hypothesis is an Auto-Illusion that alignment alone does not detect. Moreover, a few-shot fallback on ≤ 5 pairs does not suffice to stabilize causal directions in a zero-shot context."
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Lesson 33 — An Auto-Illusion guard must check alignment AND magnitude : a directionally correct but wrongly-amplitude hypothesis is an Auto-Illusion that alignment alone does not detect. Moreover, a few-shot fallback on ≤ 5 pairs does not suffice to stabilize causal directions in a zero-shot context.

(Phase 14 — ZSCG Zero-Shot Causal Guarded, 2026-09-08, VERDICT NEGATIVE, 345 PASS / 2 FAIL assumed — formulation FROZEN by Chef CP)

**Lesson (Chef's frozen formulation) :** *an Auto-Illusion guard must check
alignment AND magnitude : a directionally correct but wrongly-amplitude
hypothesis is an Auto-Illusion that alignment alone does not detect. Moreover, a
few-shot fallback on ≤ 5 pairs does not suffice to stabilize causal directions
in a zero-shot context.*

**Generating fact** (Phase 14, J3) : on RAD-C and B, the real effect is aligned
with the hypothesis (align 0.66–0.79) but ~5× larger →
`is_auto_illusion` (alignment only) never triggers → **24 false zero-shots**. The
warm fallback (`ClassWarmHead.from_class` on ≤5 pairs) produces no stable
direction → systematic cold-start escalation (K_total=16).

Three measured facts underpinning the lesson (sealed J0 v1.1, frozen seeds,
`data/phase14_zero_shot_results.json`) :

1. **Alignment is not enough — magnitude decides.** On RAD-C and B, the real
   effect is positively aligned with the class 0 hypothesis (align 0.66–0.79 on
   the 5 cycles of a typical seed) but **‖v_c_true‖ ≈ 1.3–2.7 vs ‖Δ̂‖ ≈ 0.39** —
   the hypothesis is right in direction, wrong in amplitude (~×5).
   `is_auto_illusion` (Pearson only) never triggers → `pure bet` maintained →
   **18/20 false on RAD-C, 6/20 on B**. A directionally correct but
   wrongly-amplitude hypothesis IS an Auto-Illusion : guarding oneself is
   GIVING ONESELF A MAGNITUDE TO HOLD.

2. **The frozen bet g=1.0 is structurally too poor for the target.** On E, the ZS
   head caps the final fidelity at 0.07–0.09 (target 0.173, reference ceiling
   0.216 consistent with Phase 13) — **no seed** reaches it, including the 6
   where the guard does not blame it. The codebook class does not carry the E
   effect, and the ≤5-pair fallback does not suffice for ACH-L few-shot
   (`warm_garde=0` on E and RAD-C) → any escalation degenerates into cold
   (K_total=16, target not reached).

3. **The vocabulary over-considers virtual criticism, not measurement.**
   Three alerts proved to be noise : T_zs_4b does not trigger, the J1 (coherence)
   guard even less, and the only breakdown = dominated coupling (≤5 % of seeds —
   the breakdown guards E exclusively, neutral for B/RAD-C ; E authority 3.48 →
   yes but it is FOR E). A regulation loop that only displays signals without
   annotating their trigger reasons throws the bolt, not the risk.

**Warning signal :** a pre-registered failure that is measured and published does
NOT sanction — it protects. The 2 FAIL (T_zs_4, the test that reads the JSON and
requires 0 false + 100 % detection) PROVE the protocol is falsifiable : they fail
because the measurement really showed 24 false and 5–55 % detection. Weakening an
honesty test to "pass" would destroy exactly what falsification protects.

**Application :** before attempting causal zero-shot again (carrier decision
required, not automatic), guard on **magnitude** (bounds of Δ̂ vs the audit's
‖v_c_true‖) and not on alignment alone ; DO NOT freeze the hypothesis at g=1.0
from a codebook learned on other domains ; give the fallback more decision pairs
than a ClassMapper ≤5 supports ; weight the false by the head's effect, never by
the sample. **Corpus brought to 33 lessons.**
