---
lesson: 26
title: "Exploration is only a re-allocation of selection, not a training : it costs nothing and must stay under a double gate"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Lesson 26 — Exploration is only a re-allocation of selection, not a training : it costs nothing and must stay under a double gate

A learning world sometimes needs to act to learn, not only to optimize : when W
is uncertain (high σ², inter-model variance exposed by `action_costs`), favoring
the uncertain action reduces uncertainty. But exploration is a zone of
methodological fragility : if it re-trained anything (E or W), Phase 8
prohibitions would be re-entered ; if it ignored urgency, it would violate
structural safety (Principle 5).

**Generating fact** (Chantier 3 Phase 8, 2026-09-07) : the `CuriousPlanner` creates
NO additional operation — it re-allocates the argmin among already-computed costs
(σ² is already in `action_costs`) : `curious_cost(a) = base_cost(a) −
κ·σ²(a)·safety_ok·energy_ok`. Its falsifiability rests on an **identity** : κ=0 ⇒
decision bit-identical to the frozen planner (T_cur_4).

**The two gates** (they make curiosity safe, not the formula) :
1. **Safety** — `u_ext ≥ threshold` ⇒ curiosity cut (κ_eff=0) : no exploration
   during an urgency (T_cur_2, T_cur_6-c : 0 exploration at high u_ext).
2. **Energy** — E/W budgets exceeded on the current cycle ⇒ curiosity cut :
   exploration is not bought outside budget (T_cur_3).

**Warning signal** : an "exploration" test loop that does not verify that the
explorative decisions have `active=True` (i.e. safety AND energy green) — a
selection hijacking during an urgency would be a silent failure masked by the
formula.

**Application** (Chantier 3, 2026-09-07, 279 PASS / 0 FAIL) : curiosity = bonus
−κ·σ²·gates on the frozen metric ; κ pre-registered (constant) ; `exploration`
audit traced per decision (`n_explorative`). Continuous-loop integration
100 cycles : 0 crash, ≥1 curious diversion, 0 exploration in urgency.
**Corpus brought to 26 lessons.**
