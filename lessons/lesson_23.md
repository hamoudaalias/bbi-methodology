---
lesson: 23
title: "A "toy" real-time loop can die before one measures it live : a bench clock is needed"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Lesson 23 — A "toy" real-time loop can die before one measures it live : a bench clock is needed

A non-throttled control loop on a synthetic environment runs thousands of cycles
in < 1 s. Any "live API" protocol (POST /consigne then check the effect on a
LATER cycle, tail-follow /stream, refreshing dashboard) then executes **after the
death of the loop** : measuring the effect of a consigne on an already-finished
environment is a false measurement (u_ext not findable), and an SSE tail-follow
stream opened after the end produces **no event** — and can block forever.

**Generating fact** (J4 Phase 7, Chantier 4, 2026-09-07) : the first run of the
integration driver showed `cycle=120` from the first `/status` (the loop had
already finished) ; the POST `/consigne` did not produce u_ext=0.9 ; the
`/stream` after loop end blocked indefinitely. The loop churned cycles in a
fraction of a second.

**The right clock** : slow down **the cadence**, never the steps. `loop.run(k)` =
k bit-identical steps. The J4 driver cuts the horizon into **chunks** of 20 steps
with a 0.4 s pause between chunks : the system executes exactly the same work
(amortized budget and metrics unchanged), but the loop stays "alive" ~12 s,
leaving a real window for HTTP pokes, post-POST consigne and SSE tail. This is a
bench clock, not a system modification.

**Warning signal** : an integration criterion (here `ok_api`) failing not on
semantics but on the **temporal window** of the test — and a network hang that
redistributes the failure toward the timeout rather than toward the criterion
concerned. Bench sync (wait-turn, SSE consumer thread with join timeout) must be
separated from the assertion : a channel that produces nothing is a bench event,
to be logged, not a blockage.

**Application** (CP 2026-09-07) : for any "live" protocol on a fast system,
(1) throttle the cadence by chunks (+ pause), never the steps ; (2) exercise
consigne/SSE during a known-alive state (loop at ≥ 5 cycles, remaining chunks > 0) ;
(3) verify `u_ext` on a strictly post-POST cycle ; (4) consume SSE in a separate
thread with join(timeout) and mark "0 event" as bench data. **Corpus brought to
23 lessons.**
