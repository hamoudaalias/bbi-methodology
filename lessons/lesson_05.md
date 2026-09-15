---
lesson: 05
title: "Seed pairing must be effective, not assumed"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Rule 5 — Seed pairing must be effective, not assumed

> A `reset()` without an explicit seed produces UNPAIRED episodes — silent
> inter-run variance.

**Generating fact** (Journal d'Audit, 2026-09-02) : two identical runs diverged
(BBI −1093 vs −1138) because `env.reset()` recreated the env with a random seed.
Fix : `reset(seed=...)` everywhere + blocking tests
(`test_env_reset_with_seed_is_deterministic`, `test_paired_rollouts_are_bit_identical`,
`scripts/test_seed_discipline.py` wired into reproduce_phase0.sh).

**Application** : any evaluation script must pass the seed explicitly ; any
control re-run must be **bit-identical** otherwise blocking.
