---
lesson: 19
title: "The seed-dependent stability of the hidden subsystem is a property of the construction, not of the spike"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Lesson 19 — The seed-dependent stability of the hidden subsystem is a property of the construction, not of the spike

> A hidden-subsystem construction validated on ≤ 4 seed families (spike dev,
> sealed arena) can **leak on a 5th adjacent family** with no code change.
> Non-leakage is not a property of the spike nor of the configuration : it is a
> **seed-dependent** property of the construction. The direct proof must be
> carried on **≥ 5 disjoint seed families** BEFORE Gate 0, and an NF stability
> pre-test on 10 dev seeds is mandatory before any gate.

**Generating fact** (J3v5-FIX, 2026-09-07) : Gate 0 v5 (seeds 22100-22109) on a
new family → **failure 4/6** with **A2 obs66 = 0.932** (massive leakage) while
the previous families were non-leaking : spike dev seeds (frame cross 0.37),
sealed family 21750+ (NF frame ≤ 0.42 via preflight J1v5). The diagnosis on dev
seeds 21400+ confirms the discontinuity : intra-episode leakage on the 66D obs
(obs66 0.946, win36 0.886, slope30 0.874, tp 0.851, w 0.808 — 10/10 seeds > 0.60),
jumping from one family to another while the frame alone stays ≈ chance
everywhere (cross 0.373). The construction is identical — only the seed
trajectory changes. The instability comes from the readability of the AR(1) ACF
of s in the multi-frame window, whose saliency varies with the seed.

**Warning signal** : a testbed validated on its dev seeds has NO non-leakage
proof for the Gate families. The discontinuity can appear at the gate with no
prefiguration on the known families.

**Application** (CP 2026-09-07) : verify NF ≤ threshold on **≥ 5 disjoint seed
families BEFORE Gate 0** ; mandatory NF pre-test on 10 dev seeds ; if NF > 0.42
on > 1/10 seeds → **harden the construction** (non-linearity g, noise ε, slope-gap
reduction ρ) before triggering any gate.
