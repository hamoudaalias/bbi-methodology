---
lesson: 10
title: "A 1-step model cannot predict cumulative interactions"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Rule 10 — A 1-step model cannot predict cumulative interactions

> W's temporal scale must **match the interaction's temporal scale**. An effect
> that only emerges from the **accumulation** of directional biases over H steps
> does not exist at 1-step scale : a 1-step predictor will sum H **zeros** and
> output zero.

**Generating fact** ([[Report Gate 0 CityFlow]]) : on CityFlow, the real H=150
interaction is strong (I_real = +55 accumulated, +79 canonical) and its **sign**
depends on the regime at 100 % of decisions (Design Phase 1 §3) ; but the latent
**1-step** delta ≈ 0 for each step. Closed loop (real anchor) therefore predicts
I_pred = +9.9 (sign ✅) but **amplitude ~13-18 %** and **0 for the NS regime**
under EW-hold (the most salient effect, +104.5). The 1-step latent **crushes
the directional accumulation**.

**Application** : before designing/testing the W architecture for an effect that
accumulates (100-150 steps), choose a model whose **target** (horizon-aware W
predicts the effect accumulated over H) or **structure** (recurrent) carries the
temporal scale of the interaction. A 1-step predictor, even a perfect one,
cannot produce an effect whose amplitude comes from accumulation.
