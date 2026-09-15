---
lesson: 50
title: "Symbolic spatial causal intervention has a ceiling on tasks requiring cross-example bootstrapping"
type: lesson
project: BBI
tags: [methodology, lesson]
---

## Lesson 50 — Symbolic spatial causal intervention has a ceiling on tasks requiring cross-example bootstrapping

**Lesson (frozen formulation, CP 2026-09-14) :** *"Symbolic spatial causal
intervention (Causal Touch on grids, E-W-C-P-L loop without DL/LLM) caps on tasks
requiring a semantic object role (pivot/reference), hierarchical objects
(perforation, inner frame) or cross-example bootstrapping (rule inference over
several pairs). Beyond this ceiling, enriching the hypothesis library or the
transformations does not pass the test : the bottleneck is the semantic role and
multi-example generalization, not the expressivity of the primitives. The failure
statement is published."*

**Contexts :** milestone **D4' of ARC-AGI-2** (2026-09-14), competitions
programme. Design Doc [[Design Doc ARC-AGI-2 J0]] sealed J0' (spec `2eab957b…`,
diligence D1-D5 PASS), seed `95000`, train sub-sample 40 tasks, budget 30 s/puzzle
(ARC-AGI-2 runner), pre-defined §8.2 threshold **≥ 20 %**. Runner
`diligence_d4_prime.py` out-of-module (inherited `d4_oracle` reused) — the BBI
school publishes the verdict, the library is documented section 8.1/8.3. Report
`competitions/arc/diligence_d4_prime_report.json` digest **`ecf98478…`**.

**Measurements (D4' Report — verdict NEGATIVE) :**

1. **Full BBI ceiling = 7.5 % (3/40), required ≥ 20 % → MET=False** : E (encoder:
   connected components, symmetries, periods) + W (semantic PER-OBJECT
   hypotheses : `mapColor`, `delColors`, `recolBySizeRank`, `fillEncl`, `symGrille`)
   + d4 geometric inheritance. Real W gain over D4 (bounded library depth≤2,
   5.0 %) : **+1/40** (`b230c067` → `obj:recolBySizeRankMatch`).
2. **3 resolutions / 37 out of scope** : `3c9b0459`→r180, `9172f3a0`→scale3
   (geometric, already in D4) + `b230c067` (per-object, new). The remaining 37
   require **semantic role** (pivot/reference object), **hierarchical objects**
   (perforation/inner frame), **cross-example bootstrapping** (rule not closed on
   one grid but inferred from TWO pairs).
3. **Controlled v1→v2 contrast (D4→D4')** : only the hypothesis layer changed
   (D4: whole-grid transformations → D4': per-object reasoning). The 5.0 %→7.5 %
   move with +1 new resolution **falsifies** the "the short-ops library was the
   bottleneck" hypothesis : the bottleneck is the **semantic role + multi-example
   generalization**, not the expressivity of the primitives.
4. **Honesty : no threshold moved** — CE2/E3 §6 frozen from J0, no scope waiver
   (10×10 refused, Lesson 30), no massive feature-engineering (Lesson 45).
   Option B decided by CP 2026-09-14 : **NEGATIVE closure of the ARC-AGI-2
   programme**, 10 h/week budget reallocated (ICLR 2027 5 h · Predictive AI Eval
   3 h · Metaculus 2 h).

**Application :** 1) **publish the NEGATIVEs as proof of rigor** : a documented
negative result with root-cause analysis (here : semantic role + cross-example
bootstrapping out of scope) becomes a scientific asset — integrated into the ICLR
2027 paper ; 2) **distinguish the transformation bottleneck from the role
bottleneck** : when per-object hypotheses do not generalize, enriching expressivity
is not enough — a **role** identification (pivot/reference) and **multi-pair
bootstrapping are needed — out of scope without DL/LLM** ; 3) **any exit door
after a NEGATIVE goes through an arbitration and never through threshold tuning**
(Lesson 30), even at the cost of closing the programme ; 4) Lesson 50 completes
Lessons 40-41/48-49 with the **ceiling of symbolic spatial causal intervention**
and the closure discipline on a structural-failure statement.
