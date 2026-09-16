---
title: "Lesson 56 — The scalability falsifier is per-NEW-family : point-estimate gain gates (n ≈ 5-7) are not statistics ; n ≥ 12 with a strictly positive 95 % CI lower bound is what elevates a per-family benefit from anecdote to evidence"
type: lesson
project: BBI
tags: [lesson, transfer, scalability, phase-5-agi, j4, evaluation, gain-gate, ci-lower-bound, sample-size, n12, structural-falsifier, anecdotical-evidence, lecon56, en]
date: 2026-09-16
lesson: 56
source: "Methodological Lessons Corpus (BBI).md"
---

# Lesson 56 — The scalability falsifier is per-NEW-family ; a gain gate needs n ≥ 12 and a CI lower bound > 0 to be statistical, not anecdotal

**When :** Transfer-Phase5 extension J4-P5, 2026-09-16 (E-W-C-P-L-A-T,
Phase 5 AGI), sealed spec SHA `4110295b…`. CE1-P5 20/20 determinism,
CE2-P5 0.870 (87/100, ≥ 0.60), **G_pooled = 0.780 ≥ δ = 0.20 on the pooled
conventional-tie subset** (CIBLE 3-8, n = 50), G(C6) = 0.833 ≥ 0 with
95 % CI (0.622, 1.044), G(C7) = 0.667 ≥ 0 with 95 % CI (0.376, 0.957),
G(C8) = 0.917 ≥ 0 with 95 % CI (0.760, 1.073) — all three new families
with **strictly positive CI lower bounds** — CE3-P5 100 % honesty / 0
forcing. Verdict : **POSITIF (×5 → ×8 validated, Phase 6 ×8 → ×16 open).**

**Context / tension :** the Phase-4 J4 (Lesson 55) measured G(C4)/G(C5) on
tie subsets of n = 6/7 — both ≥ 0, but the 95 % CIs were wide, the upper
bound exploded past 1.0, and the conclusion rested on point estimates. The
Phase-5 spec therefore sealed an **alternative non-uniform split** giving
n = 12 ties per NEW family (§2.4/§3.1 : uniform seed % 8 would give only
7-8 ties per family), with the verdict gate being not "G ≥ 0" alone but
**"G ≥ 0 AND 95 % CI lower bound strictly > 0"** per new CIBLE. The
run showed exactly why : the weakest new family, C7, had CE2-P5 = 0.750 on
its tie subset → G(C7) = 0.667 with CI LB = **0.376** — still positive,
but close to 0 ; at P4's n = 6/7 that margin would have been buried in a
wider CI and the verdict would have been a coin flip at the grand-estimate
level. The n ≥ 12 floor turned an anecdotal "looks positive" into a
statistically exploitable bound (the spec's §3.1 sample-size check
predicted LB ∈ [0.505, 0.730] for p ∈ [0.75, 0.90] at CE2-BASE = 0 —
observed 0.622 / 0.376 / 0.760 ; C7's 0.376 lies below the predicted band
because its CE2-BASE = 0.0833 ≠ 0 and p = 0.750 sits at the lower edge of
the prediction's conditions — documented in the J4 report §6, the sealed
criterion "CI LB > 0" still met).

**Lesson :** 1) **a scalability claim is per-NEW-family or it is nothing**
— a pooled gain can be carried by one legacy class ; the falsifier (§3.2)
only bites when each new structural family is measured individually ;
2) **a point-estimate gate "G ≥ 0" on small tie subsets (n ≈ 5-7) is not
a statistical proof** — it is an anecdote that can be swept by noise ; the
sealed mandate is n ≥ 12 per new family **with a strictly positive 95 % CI
lower bound**, so the benefit is "exploitable" not just "observed" ;
3) **the sample size is a spec-time decision** — the non-uniform split was
sealed at J0 precisely because the uniform split was known to undersize
the discriminant class (Phase-4 lesson applied forward) ; never discover
mid-run that a class is too small to infer on ; 4) **the CI LB is the real
verdict number** — report G, CE2-P5, CE2-BASE, n, variance, SE and the
full CI, and gate on LB > 0 ; 5) **a bounded weak family is fine if the
CI LB still excludes 0** — C7 was the weakest new family (CE2-P5 = 0.778,
G = 0.667) ; it was published as such, no threshold moved, no seed excluded,
and the sealed tie subset arithmetic (12 tasks) kept the LB at 0.376 > 0 ;
the honest move is to show the weakest cell raw, not to hide it in a
pooled number ; 6) **a GO written to match the sealed spec is the
zero-arbitration fast path** — J4-P5 had no GO-vs-spec divergence to
arbitrate (unlike J4-P4) because the GO quoted the spec's own reading of
every gate ; this is the Lesson 55 cure applied at the source ; 7) **the
structural generality of a mechanism is proven by applying it
byte-identical to new geometries without modification** — if it were coded
for the original geometries, the per-family decomposition would reveal it
honestly (a mechanism-coded-for-instances cannot survive the
per-NEW-family gate unchanged) — up-scaling is a property of the mechanism,
not of the domain instances (§1 of the Design Doc).

**Application :** 1) at every J0, decide the tie/target split so that each
new discriminant family reaches n ≥ 12 and compute the CI the spec
commits to ; 2) put the CI lower bound, not the point estimate, in the
POSITIF condition of the sealed verdict grid ; 3) publish the weakest
family's raw cell with its CI and its failure breakdown — the scalability
decomposition C3 → C8 is part of the artefact, not optional ; 4) draft the
J4 GO directly from the sealed spec text so no reformulation can create a
divergence to arbitrate ; 5) keep every anti-dilution reading (full
holdout, excl overlaps, actual-predicate tie subset) so nobody can suspect
subset-picking — the tie subset is sealed arithmetic, published alongside
the pooled and full readings.