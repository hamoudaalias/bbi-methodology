---
lesson: 47
title: "A PASS verdict on the averages can mask significant heterogeneity between systems"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Lesson 47 — A PASS verdict on the averages can mask significant heterogeneity between systems

**Lesson (frozen formulation, CP 2026-09-11) :** *"A PASS verdict based on the
averages of 50 systems can mask an heterogeneity that makes the performance
fragile. The distribution (quartiles, min, max, rate of systems under the
individual threshold) must be documented. An insufficient margin vs the baselines
(e.g. CS1 vs R1 = 4.7 pts < 10 pts required) means the performance is not fully
attributable to the active primitives. An agent that passes on average but fails
on more than half the systems individually has a"portfolio"type performance —
some systems pull the average, others fail. Causal discovery is possible but not
robust on the whole."*

**Contexts :** J4 v2 of the Causal Discovery Extension (2026-09-11, 50 seeds
89420-89469, B=12). Averages verdict PASS (CS1=0.88, CS2=0.712, CS3=0.886, CS4
50/50, CS5 50/50, CS6 10/10). But diagnostics : 26/50 systems (52 %) under the
individual threshold, CS2 q25=0.60 (the lower quartile is 10 pts under the
threshold), CS1 BBI vs R1 = 4.7 pts (required 10 pts), CS3 BBI (0.886) < R1
(0.891 — the random explores less so has fewer false positives). The PASS verdict
is carried by inter-system variance, not by uniform performance. Lesson 41
(closure after 2 consecutive failures) does NOT apply here (v1 NEGATIVE, v2 PASS =
1 failure + 1 success, not 2 failures).

**Application :** 1) always document the complete distribution
(min/q25/median/q75/max + under-threshold rate), not only the average ;
2) verify the margins vs baselines in **percentage points** (not in fraction) — a
gap of 0.047 = 4.7 pts, not 47 pts ; 3) when CS3 BBI < CS3 R1, active planning (P)
improves recall (CS2) but degrades precision (CS3) — a classic recall/precision
trade-off, not a P failure ; 4) the "portfolio" performance (some systems pull the
average) is a signal that the primitives work on system sub-types, not on all —
document which and why ; 5) Lesson 47 completes Lesson 46 (threshold robustness)
with the **robustness of the performance itself**.
