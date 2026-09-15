---
lesson: 27
title: "In a living system, every regulator must be indexed on the clock of the phenomenon it monitors, not on its own"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Lesson 27 — In a living system, every regulator must be indexed on the clock of the phenomenon it monitors, not on its own

An agent in continuous learning is a system that LASTS. The integrator's classic
mistake is to index each mechanism on the clock of its own functioning (fit
epochs, accounting cumuls) instead of the clock of the external phenomenon it
must follow (world cycles, time since a visit). At 50 000 cycles these
desynchronizations become silent failures : the system does not "notice"itself
failing.

**Generating fact** (Chantier 4 Phase 8, 2026-09-07) : the lifelong integration
failed **3 times** before passing, and each failure was a time-scale bug, not a
computation bug :

1. **auto-fit never armed** — the gating counted fit *epochs*
   (`(epoch+1) % period`) : in a loop where one never fits in nominal (epoch=0),
   auto-fit was structurally impossible. The right reference is the **world
   cycle** since the last fit (`_last_fit_cycle`).
2. **O(n²) energy** — the" memory "regulator **accumulated** its cumulative cost
   and re-summed it at each flush : at the 50 000th read the M line cost ~50 000
   ops. A *stratum* mode (flush of the increment, layer reset) brings the read
   back to O(1) — 16.71% of the decision, within budget.
3. **Inverted staleness** — `σ² ∝ e^(−gap)` is **maximal just after a visit** :
   the explorer stayed locked on the already-certain action and never re-tested
   the forgotten world (0 diversions over 50k = undetectable drift). Correct
   staleness **grows** with time since the last visit (`1 − e^(−gap/τ)`) : it is
   time that makes one uncertain, not freshness.

(A 4th failure was operational : memory eviction O(capacity) by numpy scan at
each push, and an unbounded latent that de-conditioned the ridge → chain
rollbacks. Eviction became O(1) amortized via per-regime FIFO buckets ; the latent
is bounded like the output of encoder E.)

**Warning signal** : a control quantity (energy, staleness, cadence) that is a
function of the PROCESS LIFETIME and not of the world time — any cumulative
counter read repeatedly is one.

**Application** (Chantier 4, 2026-09-07, 287 PASS / 0 FAIL) : run 50 000 cycles,
drift of regime A (0.60→0.25) injected into the ENV at cycle 10000, zero human
intervention. Detection at cycle **10011** (±11), purge of **391** A pairs,
2 cadenced refits, fidelities B/C/A_new ≈ 1.000, energy 16.71% < 20%.
**Corpus brought to 27 lessons.**

---
