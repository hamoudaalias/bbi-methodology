---
lesson: 13
title: "A saturated benchmark does not measure decision advantage"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Lesson 13 — A saturated benchmark does not measure decision advantage

**Context** (CityFlow, Gate 1 initial + revised, 2026-09-03) : after a 0/2
failure then a 0/2 failure with state-augmented planner, the reachability battery
revealed that PPO (pure alternation, 400 switchs/episode) matched the fixed
DC(1,1) cycle to within one unit, and that 15 policy families — fixed long/short
cycles, purging machines, LQF, augmented planners, including oracles knowing the
regime — all fell within a ±15 reward range around PPO : nothing beats
alternation.

**Mechanism** : under over-saturation (demand > capacity, ~111 vehicles on
average waiting), the sum of the queues — which IS the reward — is set by
(arrivals − capacity), not by the policy. The policy only controls the
distribution between axes, invisible in the reward. Moreover γ=2.0 exactly
balanced the marginal cost of one more holding step : flat frontier by
construction.

**Engraved statement** : before asking a paradigm to "beat" a baseline, check
that the benchmark is discriminant — i.e. that policies with significantly
different rewards EXIST. A benchmark where the oracle at best reaches equality can
only produce a pre-written verdict. Reward discriminability precedes any paradigm
question.

**Warning signals** : (1) the baseline learns a trivially simple policy
(alternation) ; (2) the rewards of very different policies are almost identical ;
(3) the marginal analysis of one step gives a net delta ≈ 0 ; (4) the reward
decomposition reward = f(queues) shows the queues are fixed.

**Contribution** : Lesson 13 + reachability pre-flight protocol (oracle grid
before gate) added to the corpus. Gate 0 remains acquired (Lesson 10) — the
Gate 1 failure is a measurement-instrument failure, documented as such.
