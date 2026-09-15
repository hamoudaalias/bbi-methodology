---
lesson: 22
title: "Causal fidelity is measured at the planner's real re-planning cadence (τ), not at τ=1"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Lesson 22 — Causal fidelity is measured at the planner's real re-planning cadence (τ), not at τ=1

> The fidelity of a multi-step plan (predicted cost vs actually executed cost)
> must be measured **at the system's real re-planning cadence** : a horizon-H
> planner that re-plans every τ steps produces a plan that is only actually
> followed over ~τ steps. Measuring it at τ=1 (re-planning every step) makes the
> 12-step plan **semantically empty** — the system never follows it — and the
> fidelity drops artificially (maximal divergence). Fidelity is measured on
> windows where the plan is actually followed (τ ≥ 5) and at the **lookahead**
> ticks (the only moments where a multi-step plan exists).

**Generating fact** (J3 Phase 7, Chantier 3, 2026-09-07) : Mode 3 — Pearson
correlation between the metric cost W planned over H=12 (argmin of the planned
cumulative cost, greedy continuation) and the W cost of the actually executed
path (policy τ), hold-out seed 31500 :

| τ (re-planning cadence) | fid_multipas_W (Pearson, 50-window) | reading |
|---|---|---|
| 1 | 0.42-0.46 | plan never followed → maximal divergence |
| 3 | 0.54 | plan partially followed |
| 5 | 0.76 | ≥ 0.60 |
| 10 (deployed design period) | **0.72 → 0.816** (faithful impl.) | plan actually held |

The **0.77 initially reported at τ=1** was a cadence artefact of the diagnostic
driver (replayed identically : 0.44) — honesty correction ratified by CP. The τ
mechanism is confirmed by the monotone dependence of fidelity.

**Warning signal** : measuring the "fidelity" of a plan at a cadence where the
plan is never executed (τ=1) mixes (1) plan quality and (2) re-planning
frequency. The fidelity drop at τ=1 says nothing about planner quality — it
measures *non-adherence* to the plan. The env-raw Σ(−rew) diagnostic stays
low/negative at all τ (different units, W = cost, not a reward predictor) : it
must not be made a criterion.

**Application** (CP 2026-09-07, τ arbitration Option 1) : for ANY multi-step
planning system, (1) record τ as a pre-registered design constant before
validation ; (2) measure plan↔execution fidelity at lookahead ticks only,
replaying the real execution by snapshot/restore (H0, 0 decision consumed) ;
(3) report fidelity at the deployment τ AND the τ=1 diagnostic as a measure of
re-planning divergence — never as a planner failure. **Corpus brought to 22
lessons.**
