---
lesson: 42
title: "A prediction function P depending on a single variable available at the first horizon produces identical predictions at all horizons : the test then measures the construction of the causal chain, not the refinement of progressive anticipation"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Lesson 42 — A prediction function P depending on a single variable available at the first horizon produces identical predictions at all horizons : the test then measures the construction of the causal chain, not the refinement of progressive anticipation

(Extension Trading — J4, Brier and financial causal chains SPY+FRED, 2026-09-10, VERDICT PASS, documented design limitation)

**Lesson (frozen formulation) :** *"When the decision function P only integrates
a variable available from the first horizon (e.g. σ_ratio_j in trading, σ_ratio
computed on the day j's complete data), the predictions are identical at all
horizons H-5/H-3/H-1/H-0. The multi-horizon protocol no longer tests progressive
anticipation — it tests the ability to build causal chains that enrich with
information. If the design aims to validate progressive anticipation, P must
integrate horizon-dependent information (data that only exists at the late
horizons), and the seal must guarantee that this information is not revealed
prematurely. Otherwise the" anticipation "axis measures a design limitation,
not a system strength."*

**Contexts :** the Trading Extension (SPY + FRED, σ_ratio = σ_5d/σ_20d, threshold
1.5, 4 horizons H-5/H-3/H-1/H-0) delivered a PASS verdict (agent Brier 0.0331 <
R2 GARCH 0.0949 < R1 0.1274 < R0 0.3438 ; causal quality 3.0/3 ; robustness 8.3 %
≤ 10 % ; honesty P7 6/6 ; fidelity W/C 1.0). But the predictions are identical at
the 4 horizons : p_high = 0.784179 (case N1-87020) on H-5, H-3, H-1, H-0. The
causal chain enriches (empty at H-5, 2 links at H-3/H-1/H-0), the missing change,
but the P decision does not. Cause : P is a function of σ_ratio_j alone, available
from H-5 (the day j's data is complete at all horizons). Sealed conformity :
§7 Design Doc Trading J0 "P plans anticipation : deterministic prediction from
(σ_ratio of W, C chain)".

**Measurements (J4 Report, digest `4861d94…`) :**

1. **Identity of predictions** : 128 cases × 4 horizons = 512 records, p_high
   identical over the 4 horizons for each case (stabilite_horizons = true,
   median advance 120 h = design artefact). The causal chain differs per horizon
   (chain↔horizon tightness verified : chains only mention revealed variables).
2. **Axis C (anticipation) : technically PASS (120 h ≥ 24 h), semantically null** :
   the median advance is an artefact (identical predictions), not real
   anticipation. Axis C is an objective technically reached but its meaning is
   null in this seal.
3. **What the PASS proves** : the BBI primitives (H0, Causal Touch, Causal
   Module, E-W-C-P-L loop, epistemic honesty) hold on real financial data. The
   system builds causal chains, counterfactuals (agreement 0.0), is robust to
   traps (degradation 8.3 % ≤ 10 %, false P3 = 0) and honest (P7 6/6).
4. **What the PASS does NOT prove** : the progressive refinement of anticipation.
   To test that, a Trading v2 with a horizon-dependent P function (integrating
   information that only exists at the late horizons) would be needed.
5. **Limitation consistent with the seal** : the P function should have
   integrated the information specific to each horizon, not only σ_ratio. In
   EU261, the prediction evolved because W integrated horizon-dependent
   information. In Trading, W = σ_ratio, available from H-5.

**Application :** 1) a multi-horizon protocol must verify that the decision
function depends on information that really differs from one horizon to the
next — otherwise the test measures chain construction, not anticipation ; 2) if
the design targets progressive anticipation, P must integrate variables that only
exist at the late horizons (e.g. intraday data at H-1, complete state at H-0),
and the seal must guarantee that this information is not revealed prematurely
(horizon tightness) ; 3) the limitation must be documented in the J4 Report, the
Design Doc, the Audit Journal, the NeurIPS Addendum — never hidden ; 4) Lesson 42
completes Lesson 41 (two successive failures = closure signal) and Lesson 40
(irreducible perceptual loss) — three lessons on building valid tests : do not
measure what the design cannot measure.

**Corpus brought to 42 lessons.**
