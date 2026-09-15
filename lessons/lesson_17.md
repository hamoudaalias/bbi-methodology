---
lesson: 17
title: "The response scale (κ, Δconsigne) is not a constrained carrier for the 1-step loss-diff"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Lesson 17 — The response scale (κ, Δconsigne) is not a constrained carrier for the 1-step loss-diff

> Making the h signature **carried by the amplitude of the actuated response**
> (regime-specific κ on a high Δconsigne) makes the window decodable
> (fen+vel MLP 0.60-0.74, frame alone ≈ chance 0.31 — excellent for
> non-leakage) **without** constraining E to code h : the 1-step loss-diff
> minimizes the differential on average over the batch ; the response scale
> (κ ∈ {0.4, 0.6}) can be absorbed by batch accommodation and the action label —
> the regime is **not required** to reduce the loss. M1 remains ~ 0.35 (MLP 0.34).

**Generating fact** (scan Voie A, 2026-09-06) : amplitude-dominated testbed
(N13 : Δconsigne 0.15, κ {0.40, 0.50, 0.60}, common σ 0.02, delay {3, 2, 1},
obs 66D). train_diff converges very well (diff 0.000277, align 0.0026) but
z→h 0.35 — E found a loss solution **without** h.

**Warning signal** : an excellent loss-diff (low diff/align) **does not imply**
that z carries h — loss is not a counterfactual guarantee, Gate 0 M1 remains the
judge.

**Application** : for a testbed to satisfy M1 ≥ 70 %, the regime must be
**critical to the 1-step differential** (a regime error → a prediction error of
the differential). The proposed v4 testbed makes the **action→effect coupling**
(consigne) depend on h (per-regime effect table : polarity/gain/delay) — this is
the condition demonstrated (by the two complementary failures Lesson 16/17) for
an exact diff predictor to be structurally constrained to code h in z.
