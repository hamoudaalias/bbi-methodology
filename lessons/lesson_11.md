---
lesson: 11
title: "The closed loop is necessary but NOT sufficient"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Rule 11 — The closed loop is necessary but NOT sufficient

> Anchoring to the real obs at each step corrects the open-loop collapse (the
> self-propagation of W errors over H iterations), but **does not create signal
> the model has not learned**. A sum of 150 zeros = zero, anchored or not.

**Generating fact** ([[Report Gate 0 CityFlow]] §6) : open-loop at H=150
collapses into a fixed point ; the **closed loop** (real anchor) corrects it, but
the **amplitude remains 18 %** — the model does not predict the effect, so the
anchoring does not invent it. Closed-loop evaluation is an **evaluation method
more faithful** to production (the planner sees the real state at each step),
but it is a **prerequisite, not a remedy** : it adds no learned information.

**Application** : always evaluate a long-horizon model in **closed loop**
(anchored) so as not to confuse method collapse with model limit ; but do not
conclude on a correction if the anchoring only brings back the sign. A correct
sign with compressed amplitude under closed loop is an **architectural failure**,
not a partial success.
