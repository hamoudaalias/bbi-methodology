---
title: "Lesson 57 — An inferred correspondence table must be LOCKED with a committed canonical SHA before the holdout is opened (0 re-inference after) ; and a fold/honesty gain diagnostic is comparator-relative, never a regression"
type: lesson
project: BBI
tags: [lesson, inference, correspondence-from-scratch, phase-6-agi, e-w-c-p-l-a-t-i, mi-lock, canonical-sha, cross-validation, byte-identical, holdout, comparator-relative, fold-gain, honesty-class, lecon57, en]
date: 2026-09-16
lesson: 57
source: "Methodological Lessons Corpus (BBI).md"
---

# Lesson 57 — Lock the inferred table before the holdout ; a fold/honesty gain is comparator-relative, not a regression

**When :** Inference-Phase6 J3-P6 + J4-P6, 2026-09-16 (E-W-C-P-L-A-T-I,
Phase 6 AGI), sealed spec SHA `ecc31748…`. J3-P6 locked the inferred
correspondence table `M_I` (canonical SHA-256 `64d393e6…`) after an H4
cross-validation proving `M_I(half 1) == M_I(half 2) == M_I(full)`
byte-identical on all three families, **before** the holdout was opened.
J4-P6 on the virgin holdout 89700-89799 : CE1-P6 20/20 determinism,
CE2-P6 = 0.830 (83/100, ≥ 0.50), **G_pooled = 0.848 ≥ δ = 0.10** on the
pooled conventional-tie subset (CIBLE 9+10+11, n = 66), G(C9) = 0.864 CI
(0.720, 1.007), G(C10) = 0.818 CI (0.657, 0.979), G(C11) = 0.864 CI
(0.720, 1.007) — three new families, three strictly positive CI lower
bounds — CE3-P6 100 % honesty / 0 forcing, CE4-P6 I-coherence 1.000.
Verdict : **POSITIF (the `I` layer of `E-W-C-P-L-A-T-I` validated).**

**Context / tension :** Phase 6 is the first phase where the *thing being
tested is itself estimated from data* — the correspondence table is
inferred by component `I` instead of sealed by the designer. That creates a
new integrity hazard absent from Phases 2-5 : the inference is a
**measurement-adjacent artifact**. If `M_I` were re-inferred after seeing
the holdout — even "just to stabilise it" — the evaluation would be
circular (the analog of post-measurement feature engineering, Lesson 45).
The CP mandate therefore required `M_I` to be **locked with a committed
SHA** before any holdout measurement, and the lock to be a *canonical*
serialisation (JSON, `sort_keys=True`, compact separators) so that any
drift — a channel re-ranking, a dropped role, a re-run — is detectable to
the byte, across platforms and dict orders. The lock lives in **code**
(`m_i_lock.py`), not in a regenerable data artifact, so J4 reads a frozen
constant and contains no call to `infer6`. Two facts made the lock
trustworthy rather than ceremonial : (a) the H4 cross-validation showed the
two DEV halves agreed **byte-identically** on every mapped role, so the
table was not a knife-edge fit ; (b) the recovered table matched the sealed
generator permutation exactly (C9 (2,0,3) · C10 (1,2,0) · C11 (3,2,0)), so
the lock was provably the right object, not merely a stable one.

The second tension was inherited, not new. At J3 the mandate's fold
diagnostic E4 asserted `G_fold == 0.000` — true in P5, where the ablation
was a *correct-predicate* purge that matched `plant` on every fold. In P6
the ablation is by design the sealed `DEFAULT_PRIOR` seam (source- and
structure-blind, §3.1), which is wrong on the whole discriminant class
(CE2-BASE = 0.000), while the honest route **absorbs** the folded
`reference` as `source_amb` (CE2-P6 = 1.000) → **G_fold = 1.000**. The
temptation was to "fix" the number by redefining the comparator until the
fold gain read 0.000. That would have been a post-hoc threshold move on the
sealed phase's comparator — the exact failure mode of Lessons 30/55.

**Lesson :** 1) **when the tested object is itself estimated from data,
lock it with a committed SHA before the holdout opens** — the lock must
cover the *canonical* serialisation, be stored in a non-regenerable place
(code, not a re-runnable artifact), and the evaluation must be structurally
incapable of re-inferring it (no `infer6` call, a hard-failing integrity
gate that recomputes the SHA) ; 2) **a lock is only trustworthy if it is
both stable and correct-identifiable** — require a cross-validation that is
*byte-identical* across data halves (not merely "close"), and check the
recovered object against the generative ground truth where one exists, so
"we locked something reproducible" cannot hide "we locked the wrong
something" ; 3) **state the coherence/totality metric of the locked object
explicitly** — CE4-P6 (I-coherence = fraction of tasks where the locked
table resolves every mapped role, 1.000) answers *is the inferred table
total?*, a different question from *is it correct?* (CE2-P6 / G) : publish
both and never let totality stand in for correctness ; 4) **a gain
diagnostic is comparator-relative, and a diagnostic that changes value when
the comparator changes is not a regression** — G_fold 0.000 (P5) → 1.000
(P6) is fully explained by the ablation changing from a correct-predicate
purge to a blind `DEFAULT_PRIOR` ; report the two comparators side by side,
re-derive *why* the number moved, and let the CP arbitrate — do **not**
redefine the sealed comparator to restore an inherited expectation ; 5)
**separate the honesty invariants from the gain value** — the load-bearing
claims about folds are "0 forcing" and "`source_amb` absorbed 4/4", which
held ; the gain *value* is a diagnostic and must not be promoted to a
falsifier ; 6) **the honest move on an unexpected number is to publish it
and alert, not to force it** — a NÉGATIF or a PARTIEL verdict is a valid
outcome (Lessons 30/55), and a self-reported deviation with a structural
explanation is worth more than a silently-retuned grid.

**Application :** 1) at every J0 for a phase that infers its own object (a
table, a mapping, a threshold), seal in the spec *what* gets locked, *how*
it is serialised, and *when* (before the first holdout access) ; 2) put the
lock in version-controlled code + a canonical-SHA constant, and make the
evaluation import the constant only — the integrity gate recomputes the SHA
and exits non-zero on drift ; 3) implement the H4 cross-validation as a
*byte-identical* assertion on disjoint data halves, and anchor the recovered
object to generative ground truth when available ; 4) publish both the
totality metric and the correctness/gain metric of the locked object, with
explicit definitions in the report and the result JSON ; 5) when a carried
diagnostic's expected value does not reproduce, publish both the literal and
the measured value, derive the comparator change that explains it, and
request CP arbitration — never retune the sealed comparator post-measurement ;
6) keep the verdict grid's load-bearing invariants (determinism, honesty,
cut-offs) separate from comparator-relative diagnostics, so an arbitrated
diagnostic deviation can never silently flip a verdict.
