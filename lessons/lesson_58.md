---
title: "Lesson 58 — Compose by discovering cross-source conjunctions, not by recovering the generator's rotation ; a rotation-symmetric composition has a depth ceiling on point-identifiability (d=3), yet the mechanism still transfers"
type: lesson
project: BBI
tags: [lesson, composition, compositionality, phase-7-agi, e-w-c-p-l-a-t-i-k, k-layer, discovery, point-identifiability, rotation-symmetry, depth-ceiling, m-comp-lock, anti-leak, anti-tautology, holdout, per-depth-decomposition, verdict-grid, threshold-discipline, lecon58, en]
date: 2026-09-17
lesson: 58
source: "Methodological Lessons Corpus (BBI).md"
---

# Lesson 58 — Lock the *discovery*, not the generator's rotation ; a symmetric composition has a depth ceiling on point-identifiability (d=3)

**When :** Compositionality J1-J4-P7, 2026-09-17 (E-W-C-P-L-A-T-I-K,
Phase 7 AGI), sealed spec SHA `5fd3e396…`, Addendum Constituants v1.1 §9
(feasible operating point), Addendum K2 `fa746aa1…` (real search, G6).
J3-P7 locked the **real K discovery** `M_comp`
(`m_comp_sha256 4dd1b947…`, 9/12 entries) — **not** the construction
rotation `M_comp*` — after the four causality assertions (A1 half-stability
9/9, A2 fidelity 1.000, A3 anti-leak 0 plant/0 rotation, A4 anti-tautology).
J4-P7 on the virgin holdout **89900-89999** : CE1 20/20 determinism,
**CE2-comp = 0.570** (`≥ 0.50`), **G_composition = 0.522** (`≥ 0.20`, CI
`(0.397, 0.648)`, n = 67), **G(d=2) = 0.235** (CI LB 0.063), **G(d=3) =
0.818** (CI LB 0.687), **G(pivot) = 0.310** (LB 0.125), **G(reference) =
0.711** (LB 0.566), **G(hierarchical) = 0.632** (LB 0.503), **CE3 13/13/0**
forcing, **CE4 1.000**. Verdict : **POSITIF (the `K` layer of
`E-W-C-P-L-A-T-I-K` validated).** G6 : `K == M_comp*` on **4/9** entries.

**Context / tension :** Phase 7 is the first phase where the composite
object is a **discovered cross-source conjunction** rather than a sealed
per-domain correspondence, and the sealed generator carries a **diagonal
rotation symmetry** (`M_comp*(r_i) = [(s_j, ROLE_ORDER[(i+j) mod 3])]`). The
pre-registered Addendum (§6, T5-P7) promised that K2's maximizer would
"reproduce `M_comp*`". On devel it reproduced only **4/9** entries ; on the
**5** disagreements every candidate sat at **fidelity 1.000**, with up to
**36** conjunctions (`d = 3`) achieving the *same* structural descriptor.
The naive reading is "K failed". The correct reading is that the
discriminant descriptor is **invariant under the rotation at d = 3** : the
structure is fully discriminant at `d = 2` but *under-determines* the
rotation at `d = 3`, so no leak-free mechanism can be forced to pick the
generator's representative. The wrong fix — pinning the rotation into K, or
scoring K against it — is exactly the tautology the Addendum's A3/A4
forbids. The lockable, evaluable object is therefore **K's discovery**, and
the load-bearing question is "does the discovered composition **transfer**?"
(CE2 / G on the holdout), not "does it match the generator?". A second,
smaller tension : the CP J4 GO message quoted `G ≥ 0.10` while the **sealed
spec §6** fixes `G ≥ 0.20` — resolved by publishing **both** readings,
keeping the sealed grid authoritative, and moving **no** threshold.

**Lesson :** 1) **when a composition is over-determined by a symmetry,
lock and evaluate the discovery, not conformity to the generative
rotation** — matching the generator is neither necessary for transfer nor
attainable without leakage ; 2) **publish the identifiability distribution
as a first-class result** (`n_at_max`, `|space|`, `K ↔ M_comp*` agreement) —
an equal-fidelity tie is a *finding about the task*, not a failure of the
mechanism ; 3) **separate *transfer validity* (CE2/G on the holdout) from
*parameter recovery* (`K ↔ M_comp*`)** — a mechanism can be valid, honest
and beneficial while non-point-identifiable ; never let recovery stand in
for the verdict ; 4) **make "matching the generator" unwinnable by
construction** — the anti-leak assertion (0 plant / 0 rotation in K's input,
verified statically and by runtime invariance) and the anti-tautology
assertion (empty/permuted map changes the seam output) are what let the
recovery gap be published without suspicion ; 5) **when a GO message
diverges from the sealed spec on a threshold, publish both readings and keep
the sealed grid authoritative** — 0 threshold move (Lessons 30/55), and
surface the divergence explicitly rather than silently picking the laxer
number ; 6) **publish the per-depth / per-role decomposition** (Lesson 56) —
here `G(d=3) = 0.818` vs `G(d=2) = 0.235`, a genuine depth asymmetry that a
pooled `G = 0.522` would hide.

**Application :** 1) at J0 for any phase whose target is a *discovered*
object under a symmetric construction, state in the spec that the lock
covers the **discovery**, and that conformity to the generator is a
**diagnostic**, never a criterion ; 2) seal the four causality assertions
(half-stability, fidelity floor, anti-leak, anti-tautology) and make them
hard-failing before the lock is written ; 3) publish the `K ↔ M_comp*`
distribution with `n_at_max` and the candidate-space size in every
report/JSON, and name the ceiling explicitly (`d = 3 → up to 36 equal-fidelity
candidates`) ; 4) keep *recovery* and *transfer* in separate sections, so a
reader cannot confuse "we recovered the generator" with "the composition
works" ; 5) draft the J4 GO from the sealed §6 grid, and when the GO wording
quotes a different threshold, compute and print **both** verdicts
(`verdict` = sealed, `verdict_grid.cp_message_reading` = GO wording) — the
sealed grid decides, the divergence is documented ; 6) always ship the
per-depth and per-role gain table with its CI lower bounds, not just the
pooled gain.
