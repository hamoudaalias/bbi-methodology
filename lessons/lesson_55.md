---
title: "Lesson 55 — The sealed spec is the only source of truth : a GO that reformulates a sealed protocol cannot override it, and a runtime-coupling gain gate is measured where the ablation fails by construction"
type: lesson
project: BBI
tags: [lesson, transfer, scalability, phase-4-agi, j4, governance, sealed-spec, arbitration, gain-gate, dilution, spec-prime, lecon55, en]
date: 2026-09-16
lesson: 55
source: "Methodological Lessons Corpus (BBI).md"
---

# Lesson 55 — The sealed spec is the only source of truth ; measure the runtime-coupling gain where the ablation fails by construction

**When :** Transfer-Phase4 extension J4-P4, 2026-09-16 (E-W-C-P-L-A-T,
Phase 4 AGI), sealed spec SHA `827e8dc7…`. CE1-P4 20/20 determinism,
CE2-P4 0.830 (83/100, ≥ 0.60), **G_pooled = 0.731 ≥ δ = 0.20 on the pooled
conventional-tie subset** (CIBLE 3+4+5), G(C4) = 0.833 ≥ 0 with 95 % CI
(0.535, 1.132), G(C5) = 0.714 ≥ 0 with 95 % CI (0.380, 1.049), CE3-P4
100 % honesty / 0 forcing. Verdict : **POSITIF.**

**Context / tension :** the CP J4 GO formulated « G_pooled ≥ δ = 0.20 sur
l'ensemble du holdout » (whole 100-task holdout). The sealed spec §3.1/§5
defines G_pooled **on the pooled conventional-tie subset** (CIBLE 3+4+5).
The Dev team escalated the divergence BEFORE measuring (Lesson 30 : no
threshold move — the two readings give G = 0.731 vs G = 0.190 and would
arbitrate POSITIF vs NÉGATIF on the same data). The CP recognised the GO
formulation error and arbitrated **Option 1 — the sealed spec primes**.
Three corrections aligned : the spec is the only source of truth ; the
tie+probe overlap count was 2 in the GO but is 3 empirically (88714 added,
C3 reference probe with empty pair) ; and the anti-dilution diagnostics
(G full, G excl. 2, G excl. 3, actual-predicate tie subset) are all
published alongside the verdict measure.

**Lesson :** 1) **the sealed spec is the only source of truth** — a CP GO
that reformulates a sealed protocol cannot override it : on divergence, the
spec primes (Lesson 53) and the team escalates **before** measuring ;
2) **never move a threshold to reconcile a GO reading with a spec reading**
— the fix is restoring the sealed measurement subset, δ stays fixed ;
3) **a runtime-coupling gain gate is measured on the subset where the
ablation fails by construction** (conventional ties) — measuring on the
holdout dilutes the signal with non-tie tasks where the gain is
structurally null (0.190 full vs 0.731 tie subset on the same 100 tasks) ;
4) **publish the divergent readings** (tie-subset verdict + full-holdout +
overlap-excluded diagnostics) so a reader cannot accuse the team of
picking the flattering subset — anti-dilution transparency is part of the
measure, not decoration ; 5) **classify overlaps by the actual tie
predicate, not the is_mirrored flag** (J3-P4) — a probe-overlap keeps an
empty pair and routes as a data tie ; 6) Lesson 55 closes Phase 4
scalability : **×3 → ×5 validated with per-CIBLE benefit on both new
families — the frozen runtime-A mechanism is scale-invariant.**

**Application :** 1) when a GO conflicts with the sealed text, stop, write
the risk, request arbitration, and measure under the spec reading —
escalation is a required step, not optional diligence ; 2) define in every
J0 the task class where the no-coupling baseline is at zero by construction
and commit to measuring the gain there pre-holdout (dev E1/E2) ; 3) keep the
honesty registry and the overlap inventory on the very subset that carries
the gain, and publish every alternative G reading raw ; 4) record the
arbitration (GO vs spec, option, justification) in the J4 report — the
decision record is part of the artefact ; 5) for every "consumption at
scale" claim, add a per-family benefit column so the pooled gain cannot be
carried by one legacy class.