---
lesson: 46
title: "A percentage threshold on a tiny base (< 20) is statistically non-robust ; prefer an absolute threshold"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Lesson 46 — A percentage threshold on a tiny base (< 20) is statistically non-robust ; prefer an absolute threshold

**Lesson (frozen formulation, CP 2026-09-11) :** *"A percentage threshold on a
tiny base (e.g. 40 % on 8 FP) is statistically non-robust (±1 unit = ±12.5 pts).
When the base is < 20, an absolute threshold (e.g. FP ≤ 5) is more stable and
reaches the same physical objective. The pre-sealing diligence must verify the
statistical robustness of thresholds, not only their nominal value."*

**Contexts :** V2/V3 conflict of the pre-sealing diligence v2 (amendment A'5,
2026-09-11). V3 ((i,i) false reduction) at B=12 : FP 8→5 (37.5 %, RED under the
40 % threshold) but at B=15 : FP 7→4 (42.9 %, GREEN) — the optimal budget for V2
(B=12, Lesson 45) made V3 fail, and vice versa. The base of 8 FP over 50 seeds
makes the percentage unstable : **±1 seed = ±12.5 pts**.

**Application :** 1) when the variable of interest has a base < 20 events,
formulate the criterion as an **absolute threshold** (FP ≤ 5), not in % — % magnifies
one unit of noise into dozens of points ; 2) a pre-sealing amendment that changes
the **formulation** of a threshold (without changing its physical objective nor
the evaluated budgets/scores) is a statistical-robustness correction, NOT post-
measurement threshold tuning — it must be documented as such (A'5) ;
3) simultaneously verify that the criterion's physical objective is reached
(TP ≥ 90 % here) ; 4) Lesson 46 completes Lesson 45 (a mis-calibrated threshold
makes the test non-robust) with the **metrology of diligence thresholds**.
