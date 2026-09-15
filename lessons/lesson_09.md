---
lesson: 09
title: "A rare signal does not exist for an unweighted MSE"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Rule 9 — A rare signal does not exist for an unweighted MSE

> If a causal mechanism depends on a specific interaction (Action A × Hidden
> State B) that occurs in only a minority of transitions, a World Model trained
> with a standard MSE will ignore this interaction in favor of average dynamics.
> Signal amplification or targeted over-exposure (without filtering failures) is
> a structural prerequisite before any planning test.

**Generating fact** ([[Report C3.1]]) : Condition C failed at 12 % of E1
events (predicted −0.04 vs actual −2.63).

**Measured generalization (Gate 0)** : even with amplified signal (E1-strong :
actual doubled to −4.36) and over-exposed events (27.2 %), a 1-step MLP still
predicts the **opposite direction** of the interaction (+0.13) — **this is a
representation limit, not a sampling one**. Before blaming the data, test the
model on the interaction ; before concluding on the model, amplify the data. If
both fail : the prediction architecture itself is at fault (lead : **differential**
prediction W(z,a)−W(z,a_null) instead of transition MSE).

**Application** : any planning test on an interactional mechanism must be
preceded by a **coherence gate** (does the model predict the interaction ?)
BEFORE any benchmark on the validation seeds — and respect the cut-off if it
fails.
