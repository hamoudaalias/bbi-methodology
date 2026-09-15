---
lesson: 04
title: "Any incomplete action coverage produces out-of-distribution predictions"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Rule 4 — Any incomplete action coverage produces out-of-distribution predictions

> If W has not seen all actions at training, the planner compares OOD
> predictions — non-interpretable results.

**Generating fact** ([[Report Phase 0bis]] §3) : the first 0bis run trained W on
"Maintain"-only rollouts → "harmful memory" (p<0.006) — artefactual false
negative. Fix : uniform policy + **blocking** action-coverage tests
(`seq_uniform_policy_covers_all_actions`).

**Application** : any W training dataset must cover the action space — verified
by a blocking test before any benchmark.
