---
lesson: 14
title: "The offline vs online training asymmetry is a feature of the paradigm, not a protocol flaw"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Lesson 14 — The offline vs online training asymmetry is a feature of the paradigm, not a protocol flaw

**Context** (Phase 2, Grid 2×2 bottleneck+spillback, Gate 1, 2026-09-05) :
the PPO baseline (SB3, 204 800 steps of online RL environment on the BAL regime)
dominates BBI (W-HORIZON + P) on **all** configurations — causal NS/EW ×
m∈{1.0,1.5} as well as BAL controls — with gaps of −13 000 to −17 000 of
cumulative reward (paired Wilcoxon AND t-test, α=0.05, Holm on 6, all
significant, disjoint CIs). The falsifying BBI-no-h is even worse than BBI
(+15 000 to +36 000 gain for BBI with h) : causal inference produces a real
advantage, but insufficient against online RL.

**Mechanism** : BBI is offline by design — E/W trained on pre-collected
counterfactual pairs (~500 env.step : 495 collection steps pairs + held states,
train seeds 21000-21002, zero environment access for P at deployment). PPO is
online — trial-and-error learning (204 800 env.step). The training asymmetry
(~400×) is the **value proposition** of the paradigm (sample efficiency), not an
experimental bias. The "equal budget" of design §9 was matched in **evaluation**
(same seeds 1000-1009, same 400 steps/episode) ; it was not matched in
**training** — by construction, offline vs online cannot share the same training
step budget.

**Engraved statement** : any BBI vs online RL comparison must quantify the
training asymmetry (offline environment steps of the collection vs online
learning steps) and discuss it as a potential explanatory variable of the
result — without hiding it, and without presenting it as a protocol flaw. A
verdict where the online side has ~100-400× more training steps proves neither
the inferiority of the causal paradigm nor its equality : it only bounds the
question "does a real causal advantage (here +15k..+36k) suffice to compensate
the massive online-learning advantage ?" — and the answer measured here is no.

**Warning signals** : (1) a BBI vs online RL comparison without a
"env.step budget BBI / env.step budget PPO" line in the results table ;
(2) the words "equal budget" used without specifying training vs evaluation ;
(3) a causal-inferiority verdict drawn from a run where the online side has
~400× more training steps without discussing the asymmetry.

**Contribution** : Lesson 14 added to the methodological corpus (brings the corpus
to 14 lessons). Budget asymmetry quantified (495 vs 204 800, ratio ~400×) and
engraved as a feature of the paradigm — to trace in the article (budget section)
and to discuss in any future BBI vs online RL comparison.
