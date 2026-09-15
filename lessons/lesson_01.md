---
lesson: 01
title: "Training loss is not a proxy for latent quality"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Rule 1 — Training loss is not a proxy for latent quality

> A model that fits its training data better does not necessarily learn a
> better causal representation.

**Generating fact** ([[Report Ablation C3]]) : the interventionist had a much
lower training loss (0.232 vs 0.410) but a probe M1 **lower** (0.713 vs 0.776) —
better fit, worse encoding of `h`.

**Application** : any claim of "better representation" must rely on an
**encoding** metric (probe, conditional error), never on loss alone. Never
report loss as evidence of latent quality.
