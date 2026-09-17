---
title: "Lesson 59 — A recursive lift is only as good as its discriminant class : per-role constructibility at J1, construction repairs before the holdout (not threshold moves), and metric conventions published with provenance"
type: lesson
project: BBI
tags: [lesson, order-2, phase-8-agi, e-w-c-p-l-a-t-i-k-a2, recursive-abstraction, discriminant-class, per-role-constructibility, baseline-design, impossibility-proof, construction-fix, addendum, re-seal, threshold-discipline, coherence-convention, ablation, holdout-integrity, lecon59, en]
date: 2026-09-17
lesson: 59
source: "Methodological Lessons Corpus (BBI).md"
---

# Lesson 59 — A recursive lift is only as good as its discriminant class

**When :** Order-2 abstraction J0→J4-O2, 2026-09-17 (E-W-C-P-L-A-T-I-K·A²,
Phase 8 AGI), sealed spec `62a79a25…` (re-sealed via
[[Addendum_Order2_Hierarchical_Baseline]] `84bebb93…`). J1-O2 shipped the
multi-view testbed + A² (R6-R10, T1-T5 5/5) ; J2-O2 the read-only seam with
provenance gates (S1-S6) ; J3-O2 the causality assertions on **DEV**
(C/D/E : consensus vs single 63/63, consensus vs pooled 63/63, L=1 ablation
`≡` BASE-single with gain 0.841). J4-O2 on the virgin holdout
**91300-91399** : CE1 20/20, **CE2-order2 = 0.850** (order-1 single 0.310 /
pooled 0.020), **G_order2 = 0.841** CI95 `(0.751, 0.932)` n = 63,
**G(L=3) = 0.818** (LB 0.687) / **G(L=5) = 0.867** (LB 0.745),
**G(meta-pivot) = G(meta-reference) = G(meta-hierarchical) = 1.000**
(zero-variance), **CE3 3/3/0 forcing**, **CE4** base-case 100/100 +
coherence 0.950. Verdict **POSITIF** — the `A²` layer of
`E-W-C-P-L-A-T-I-K·A²` validated ; recursion trajectory CLOSE.

**Context / tension :** For a sealed-rules lift there is no discovered
object to lock (Lesson 57 has no object here), so the whole claim reduces to
two falsifiers : the **base-case identity** (`A²(L=1) ≡ A(1)`) and the
**gain over BOTH order-1 baselines on a class where they fail by
construction**, plus the **consensus-removal ablation**. The tension is that
this class — the discriminant class — is not a formality : it must be
*constructible per meta-role*. Under the literal "frozen rule family on the
pooled observables", the relational role's natural pooled lift (containment
frequency) makes a hierarchical discriminant **algebraically impossible**
(both-miss needs `freq(decoy) > freq(latent)` ⟺ `y > x` ; plurality-equals-
latent needs `x > y` ; contradiction). Published as-is, the phase would have
returned `G(meta-hierarchical) = 0` — a **false negative about the
mechanism** produced by a baseline choice. The honest sequence was : prove
the impossibility at J1 (before J4), have the CP arbitrate the baseline
(Option (a) : the score-based min bbox area — the order-1 lift of R3's
enclosure ratio), **re-seal** the spec without touching δ, windows, family
or the verdict grid, and re-verify per-role constructibility (T5 21/21/21 →
J3 per-role gain 0.333 → J4 role G = 1.000). Secondary tension : the Design
Doc §9 placed a determinism window on the **holdout** in J3 while requiring
the holdout untouched — caught **before opening**, corrected by the CP to
DEV ; the holdout stayed sealed. Third, quieter : CE4-O2(b) *"the plurality
object agrees"* does not define what happens when a half-fold abstains
(tie) — the convention (abstention never contradicts) was fixed in code at
J1-O2 (`6f8a064`), **pre-holdout**, with the strict variant (0.430)
published next to the primary (0.950).

**Lesson :** 1) **a recursive-lift claim lives or dies on its discriminant
class** — make each mapped role able to *carry* the class (n ≥ 12, CI95
LB > 0) a hard pre-holdout deliverable (J1 self-test), never a J4 surprise ;
2) **an order-1 baseline is a design choice with mathematical
consequences** — when the baseline family is relational, test
constructibility analytically (a two-clause contradiction is cheap) and
treat an impossibility of the class as a **construction deficiency**, never
as a result about the mechanism ; 3) **repairing a construction bug before
the holdout is not a threshold move** — the prohibition protects *measured*
numbers ; a pre-measurement baseline definition, documented by an Addendum
with the impossibility proof and a re-sealed spec SHA, keeps the claim
testable (state explicitly what did NOT change : δ, windows, grid, family) ;
4) **publish the falsifiers separately from the verdict** — base-case
identity + C/D/E causality + the ablation give the verdict its meaning
(recursion, not re-parameterisation) and are cheap to assert ; 5) **publish
under-specified metric conventions with their provenance** — name the
convention's pre-holdout commit and show the alternatives (strict/parity),
so an ambiguity never first surfaces in the final report ; 6) **a
zero-variance CI is a legitimate outcome by construction** (1.000 vs 0.000
on every role-specific discriminant task) — publish the degeneracy
explicitly rather than dressing it up ; 7) **re-read protocol arithmetic
against the integrity rules before opening** — a determinism window
borrowed from the holdout in a causal step is an integrity bug even when
the prose *seems* coherent.

**Application :** 1) at J0/J1 of any recursive/lift phase, seal the per-role
and per-view-count discriminant decomposition with the n ≥ 12 floor and
verify it in a T-test before any holdout access ; 2) include the
impossibility analysis of the baseline family in the J1 diligence
(frequency vs score for relational rules) ; 3) if the repair changes the
mechanism's definition, write the Addendum + re-seal and list the
invariants that did NOT change ; 4) run the J4 instrument first on DEV
(J3 : determinism, causal assertions, ablation) so the holdout opening
executes a validated instrument ; 5) ship every metric-convention variant
(primary, strict, alternate split) and its commit provenance in the report
and the result JSON ; 6) check protocol windows against the holdout rules
at J0-review time, not at execution time.
