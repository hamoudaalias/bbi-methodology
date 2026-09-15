---
lesson: 20
title: "The structural NF/M1 trade-off : a hidden variable that is at once non-leaking AND inferable in the latent is a rare property of the testbed construction"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Lesson 20 — The structural NF/M1 trade-off : a hidden variable that is at once non-leaking AND inferable in the latent is a rare property of the testbed construction

> There is a **structural trade-off** between the non-leakage of h (c2/A2 ≤
> threshold) and its encoding in the latent (c3/M1 ≥ 0.70). Reducing the temporal
> distinguishability of h in the obs (for non-leakage) crushes the causal
> coupling of h to the next step (necessary for M1) : no point of the bounded
> correction space satisfies c2 AND c3 simultaneously. This is not an architecture
> failure — it is a limit of the testbed construction for the causal paradigm.

**Generating fact** (J3v5-FIX, 2026-09-07) : bounded correction space exhausted
on dev seeds (pre-registered before testing, per the CP protocol) : ρ tightening
{0.15,0.80,0.97} → {0.40,0.65,0.90} then {0.50,0.60,0.75}, noise σ 0.02→0.05,
non-linearity g = tanh(3·s), observation noise ε = 0.05 on the probes w :

| Config | NF obs66 cross | M1 z→h cross | Verdict |
|---|---|---|---|
| BASE (ρ 0.15/.80/.97, σ.02) | 0.806 | 0.41 (J2v5) | leak |
| TIGHT (0.40/.65/.90, σ.02) | 0.624 | 0.52-0.54 | leak + M1 < 0.70 |
| TIGHT + σ 0.05 | 0.624 | 0.51-0.52 | leak + M1 < 0.70 |
| VTIGHT (0.50/.60/.75, σ.05) | **0.427** | 0.39-0.49 | M1 fails |
| VTIGHT + tanh(3·s) | ~0.42 | 0.41 | M1 fails |
| VTIGHT + obs noise ε 0.05 | 0.659 | — | leak AGGRAVATED |

The tightening lowers NF but M1 stays < 0.70 ; the observation noise turns
leakage back on (the T/P probes become the dominant channel). Symmetric
trajectory of the trade-off : reading h in the obs frees M1 (trivial) without
decorrelating the obs ; hiding h in the obs prevents M1 (E no longer extracts h)
while reducing the richness. The T/P arena provides alternative continuous cues
that the ρ tightening does not eliminate.

**Warning signal** : a config passing c2 and c3 on dev seeds is NOT a proof of
co-satisfaction on the Gate families — and if the trade-off is structural,
**no tuning** combines the two.

**Application** (CP 2026-09-07, absolute cut-off) : any hidden-variable testbed
must verify the **co-satisfaction of c2 AND c3 on ≥ 5 seed families BEFORE Gate
0**. If the tension is structural (the two criteria antonymic over the whole
bounded correction space), the testbed cannot simultaneously test h inference
and its causal exploitation. Phase 3 closed on an honest negative verdict : the
construction of hidden-variable testbeds for this paradigm is an **open problem**,
a methodological contribution in itself (Lessons 15-20).

---
