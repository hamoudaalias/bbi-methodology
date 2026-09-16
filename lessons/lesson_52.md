---
title: "Lesson 52 — A causal re-confirmation measure must ground the channel attribute, not re-win the rule on the perturbed state (construct validity)"
type: lesson
project: BBI
tags: [lesson, abstraction, phase-1-agi, j4, construct-validity, causal, ce2, positif, en]
date: 2026-09-15
lesson: 52
source: "Methodological Lessons Corpus (BBI).md"
---

# Lesson 52 — A causal re-confirmation measure must ground the channel attribute, not re-win the rule on the perturbed state (construct validity)

**Lesson (frozen formulation, CP 2026-09-15 — arbitration Option 1) :** *"A
loop confirmation criterion that re-extracts the roles on the state perturbed
by W and requires the same object to re-win its rule is INVALID BY CONSTRUCTION
for every role whose hypothesis acts on the role's own defining attribute
(reference = leftmost moved by H2, anchor = centered moved by H5) : the
intervention moves the object OFF its defining attribute, so re-extraction can
never confirm it. Such a measure produces a meaningless 0.000 — a
construct-validity artifact, not a real degradation. A valid causal
confirmation answers a different question : when the loop plans on the role's
channel and W predicts, does the CHANNEL ATTRIBUTE actually change as the
hypothesis claims? OUI → grounded. NON → honest indeterminate (never forced).
Verdicts are driven by the SEALED extraction criterion, never by an invalid
diagnostic."*

**Contexts :** workstream **Abstraction (E-W-C-P-L-A, Phase 1 AGI)** — Design
Doc [[Design Doc Abstraction J0 — Semantic role extraction by explicit rules
(E-W-C-P-L-A, Phase 1 AGI)]] sealed spec `238437d9…` (Addendum 1 re-seal, J1
8/8, J2-J3 11/11), **J4** sealed evaluation CE1-CE3 on virgin holdout
88250-88299 (report = [[Abstraction J4 Report]], digest `2c51ea8f…`).

**Measurements (J4, verdict POSITIVE) :**

1. **The first loop measure produced CE2_BOUCLE = 0.000 (0/50)** : A
   re-extracted roles on the W-perturbed state and confirmed a role only if
   the same object still won its rule. For every positional role the
   hypothesis displaces the defining attribute by design → re-extraction can
   never fire → 0/50. Escalated to the CP **before** any verdict, with three
   options (keep-faithful → NÉGATIF by artifact ; fix the measure ; CP
   arbitration).
2. **CP arbitration Option 1 validated (conditions strictes)** : the sealed
   spec §5 defines CE2 as an EXTRACTION criterion (A alone on the original
   grid) — the "boucle" measure is an added diagnostic that never drives the
   verdict. Verdict driven 100 % by **CE2_extraction = 0.860 (43/50)**, CE1
   10/10, CE3 100 % indeterminate / 0 forcing → **POSITIF**. Thresholds CE2
   ≥ 0.80 untouched (Lesson 30) ; A/W/C/P code untouched (Lesson 45) ;
   the buggy 0.000 **published in full** alongside the corrected measure
   (honesty, Lesson 44).
3. **Corrected grounding-gate measure : CE2_BOUCLE = 0.860 (43/50) = the
   extraction ceiling** — the loop plans on each role's channel (P), predicts
   (W), and the gate confirms the channel attribute moved per hypothesis. Loop
   does not degrade extraction. Baseline without A = 0.000 (no abstraction =
   no semantic signal). Bit-identical rerun, digest `2c51ea8f…`.
4. **Controlled contrast** : the exact same holdout gives (invalid re-win
   criterion) 0.000 → (grounding criterion) 0.860 → the 0.000 was entirely
   measure construct, not loop behaviour. The distinction "correcting a
   pre-verdict construct-validity bug ≠ moving a threshold post-measurement"
   is the CP's own guard : the first is rigor, the second is cheating.

**Application :** 1) **never let a diagnostic the spec does not seal drive a
verdict** — anchor verdicts to the sealed criterion, publish extra measures as
diagnostics (the "boucle < A" guard only fires on the VALID measure) ; 2) **a
causal re-confirmation must ground the channel attribute of the hypothesis
(does the intervention change the channel?), not require re-winning the rule
on the perturbed state** (invalid for self-moving hypotheses) ; 3) **escalate a
suspicious exact-0.0 diagnostic BEFORE interpreting it** — a measure that never
confirms anything is more likely a construct-validity artifact than a real
degradation (root-cause it before publishing it as science) ; 4) **publish the
buggy number with its explanation AND the corrected number** (transparency is
the antidote to every temptation) ; 5) Lesson 52 completes Lessons 30/44/45
with **measure construct validity : a criterion that cannot detect the signal
it studies by construction is not a measurement, it is a measuring-device bug**.