---
lesson: 16
title: "Process variance is a carrier of h that the loss-diff erases (common-mode)"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Lesson 16 — Process variance is a carrier of h that the loss-diff erases (common-mode)

> Enriching the h signature with **process noise** (regime-specific σ) does not
> suffice to make h decodable in the latent : the contrastive objective
> (train_diff, alignment encode(a)↔encode(null)) eliminates the **common mode**
> between branches. The variance of h, present in the obs (linear probe obs→h
> 0.82), is **invisible to the loss-diff** (the noise draws of the two branches
> are independent → they cancel in the differential). E, optimizer of the
> loss-diff, has **no reason** to code σ in z → M1 ~ 0.49 (MLP ceiling 0.51),
> while the obs is decodable at 0.82.

**Generating fact** (scan Voie A, 2026-09-06, dev seeds 21400+) : σ-dominated
testbed (N5 : Δconsigne 0.02, κr 0.10, σ {0.12, 0.06, 0.03}, delay {3, 2, 1},
obs 66D window+absolute value of slopes). Obs→h linear 0.818, obs→h MLP 0.792,
but z→h linear 0.487 / MLP 0.511. The raw obs differential (o_next_a −
o_next_null) is itself ≈ chance (0.326) : the common mode carries h.

**Warning signal** : the "frame < window ≥ 60 % ≤ z ≥ 70 %" hierarchy is
satisfied BEFORE passing through E (fen-vel ≤ 0.76) but **breaks inside E**
(z = 0.49). The richness is not in the right object : it must be in the
**training differential**, not in the obs.

**Application** : the Lesson 15 pre-test ("raw windowed obs ≥ 60 %") must be
measured **on the loss-diff object** (the actuated differential), not only on the
passive obs — otherwise one certifies a richness that E cannot consume.
