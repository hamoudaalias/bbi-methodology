---
lesson: 25
title: "Counterfactual memory lives OUTSIDE the cycle : a counter hooked to the decision cycle erases its cost"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Lesson 25 — Counterfactual memory lives OUTSIDE the cycle : a counter hooked to the decision cycle erases its cost

The anti-catastrophic-forgetting of a learning world requires replaying the past
(H0 pairs, not transitions) in the guardian's refits. But the past is not a
tick : it has no `begin_cycle`. Two measurable traps : (i) a buffer fed only at
refit time forgets itself — the memory must be **fed at every H0 acquisition**
(each cycle where `v_c_true` is measured) to exist ; (ii) a memory cost counted
**on the decision counter** disappears : `begin_cycle` resets the ops, and the
pairs stored between two cycles fall out of the energetic audit scope.

**Generating fact** (Chantier 2 Phase 8, 2026-09-07) : T_buf_5 showed `total_M=0`
while 74 pairs had been pushed — the common counter was reset by the first
acquisition `begin_cycle`. Decision and memory commits have **incompatible cycles**
(the tick vs the lifetime of the rare regime).

**The right structure** : a dedicated **M line**, counted in its own register
(`EnergyRegulator(extra_layers=("M",), budgets={"M": 50.0})`) that the decision
`begin/end_cycle` never touches ; feeding at acquisition, reading at refit,
commit (`end_cycle`) at end of cycle on this register.

**Anti-forgetting** : eviction from **the most populated regime** (counter > 1),
never from the rare ones : the value of an anti-forgetting memory is precisely to
keep the regimes that risk being crushed by frequency.

**Application** (Chantier 2, 2026-09-07, 270 PASS / 0 FAIL) : buffer fed at every
H0 acquisition, refit on mixed batch (16 recent + 48 memory), regime A
(gain 1.0·u) retested after learning regime B (gain 0.55·u) : fidelity A **0.89**
with memory **vs 0.45 without** (B was crushing A). Cost : dedicated M line,
75 audited ops. **Corpus brought to 25 lessons.**
