---
lesson: 49
title: "A rich channel and state feedback solve perception, not stabilization : manipulation requires a damping controller"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Lesson 49 — A rich channel and state feedback solve perception, not stabilization : manipulation requires a damping controller

**Lesson (frozen formulation, CP 2026-09-13) :** *"The rich channel [θ̃, ω̃]
float64 and the closed-loop feedback solve perception (CE4 PASS), but do NOT
suffice for stabilization (CE5 PARTIAL). Active manipulation requires more than a
rich channel and state feedback : it requires a controller able to damp the
dynamics, not only to verify it. The stabilization failure on a rich channel is a
controller limit, not a channel limit. From now on distinguish : perceive (channel
+ encoder), verify (W/C agreement), stabilize (controller + damping)."*

**Contexts :** final milestone **J4 of the Perceptive Encoder v2 Extension**
(2026-09-13). v2 relaunch decided on Lesson 48 (v1 closed on PARTIAL, spec
`5165e9df…`), Design Doc [[Design Doc Perceptive Encoder v2 J0 — Rich channel and state feedback for active manipulation (Lesson 48)]] sealed (spec §9 excluded
`52ec1014…`, diligence D1-D5 PASS digest `49309e2b…`), CE4/CE5 mechanisms locked
by CP via [[Addendum J4 — Perceptive Encoder — Evaluation Corpus CE1..CE5 (W gate CP Option 3, R1 mirror, traps PP1..PP7)]] (gate W N1..N4, N4 `missing[]`
in the count, R1 mirror on 92030..92059). Report `data/perceptif_v2_J4_report.json`
digest **`ddf23cea…`** byte-stable, audit 3000 records.

**Measurements (J4 v2 Report) :**

1. **CE4 (verify the causal differential) PASS 3/3 — SATURATED** : W/C fidelity
   per path **A-modal 1.0000 · B-geom 0.9994 · C-sample 1.0000** (≥ 0.80 AND >
   R1 mirror + 0.05 ; R1 mirror +0.0053/−0.0803/−0.0205, rel. thresholds
   +0.0553/−0.0303/+0.0295), N1..N4, N4 `missing[]` honest in the count
   (`window_too_short` path A, `circle` path B, `extrema`/`omega` path C). **v1
   (0.9196/0.9415/0.8473) is surpassed — with a rich channel and closed-loop
   feedback, perception saturates at 1.0.** *Perception is solved.*
2. **CE5 (stabilize toward θ_target) PARTIAL ×3 — 10/10 NOT reached** : **A 2/10 ·
   B 5/10 · C 2/10** (seeds 92060/92064 · 92072/92075/92076/92077/92079 ·
   92081/92084), **9/30 vs 4/30 in v1** (gain), θ_target = min(π/2,
   asin(τ_max/(m̂·g·L))) from **perceptive m̂** (never m_true), final error
   \|θ(50)−θ_target\| < 0.1 rad, **0 fallback** m̂→2.75, **0 π/2 diag** (no m̂ ≤
   0.51 — reachable range). The seeds approach (0.01..0.28 rad) but the P-L regime
   does not **lock** ≤ 0.1 rad in 50 steps (transient stabilization 1..18 cycles).
3. **Controlled v1 → v2 proof** : only the pair **(channel, state feedback)**
   changed (CP decision 2026-09-12, never the controller — 0 loop modification).
   The perception degradation **disappeared** (CE4 1.0) but stabilization **does not
   follow** — the "channel was the bottleneck" hypothesis is **falsified** : the
   bottleneck is the controller (damping), not the channel.
4. **Traps PP1..PP7 (60, out of cut-off) : published honesty statement** —
   PP1/PP4/PP6 refusal 6/6, 15/15, 6/6 (100 %) ; PP3 11/15 (73 %) ; PP5 2/6 (33 %) ;
   **PP2 strong noise 0/6 detected (filtering limit : maximal noise
   indistinguishable from the sealed ε_v2 noise)** ; **PP7 6/6 failures published**
   (pathological π/2 target injected → the system publishes the non-stabilization,
   0 crash, 0 fabrication).
5. **Programme closure activated (§7 v2, Lesson 41 by programme)** : CE5 PARTIAL
   on the 3 paths → Perceptive Encoder **v2 programme closed** ; verdict validated
   by CP 2026-09-13.

**Application :** 1) **in any manipulation seal, the chain has three tiers and is
evaluated per tier** : perceive (channel + encoder — CE4), verify (W/C
agreement), stabilize (controller + damping — CE5) ; a PARTIAL at the last tier
never contaminates the first two, and **saturating CE4 predicts nothing about
CE5** ; 2) **falsify by controlled contrast** : when a limit is suspected to live
in the channel, enrich ONLY the channel and the feedback (never the controller) —
a CE4 that saturates with an unchanged CE5 locates the bottleneck with certainty ;
3) **any exit door after "rich channel" goes through the controller** : explicit
damping, systematic ω̂_LONG, maintain-vs-approach planning — with a new J0 and a
D1-D5 diligence, never a post-measurement threshold tuning ; 4) Lesson 49
completes Lesson 48 (verify ≠ stabilize) with the **bottleneck localization :
perception vs controller** and the order of attempts (channel first, controller
next).
