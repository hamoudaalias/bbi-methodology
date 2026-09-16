---
title: "Lesson 53 — Cross-domain transfer by structural correspondence is reachable by explicit deterministic rules (0 DL / 0 LLM)"
type: lesson
project: BBI
tags: [lesson, transfer, phase-2-agi, j4, cross-domain, structural-correspondence, ce2, oracle, positif, en]
date: 2026-09-15
lesson: 53
source: "Methodological Lessons Corpus (BBI).md"
---

# Lesson 53 — Cross-domain transfer by structural correspondence is reachable by explicit deterministic rules (0 DL / 0 LLM)

**When :** Transfer extension J4, 2026-09-15 (E-W-C-P-L-A-T, Phase 2 AGI),
sealed spec SHA `5be58b22…`. CE1-T 10/10 determinism, CE2-T 0.860 (43/50,
threshold ≥ 0.60, at the pre-sealed oracle ceiling D4 = 0.860), CE3-T 100 %
honesty / 0 forcing. Verdict : **POSITIF.**

**Context / tension :** the source-domain grids (Abstraction, seeds
88200-88249) are, per the sealed spec, the **semantic anchor** of the roles
and are *not re-processed during transfer evaluation* — the mapping table IS
the transfer hypothesis. The CP initially demanded T consume component A's
output at runtime ("Entrée : rôles sémantiques extraits par A"). Grep
proved that demand was not in the sealed spec (0 occurrence) — the spec
says the opposite twice (§1 and §3). The CP recognised the error. Option 1
(dual-channel) settlement : CE1-CE3 stay target-only (verdict arbiter), and
a **gated verification channel** (`transfer_source.py`, J3) proves the
functional A→T dependence — on the same target triplet,
`project_gated(roles_A_clean) ≠ project_gated(roles_A_amib)` (reference
idx → None under the 2/50 R2-probe source grids 88220/88248), purge
invariant except on the probe-paired targets. Honest propagation : source
ambiguity → target None → W refuses, P refuses a lever, C INDETERMINATE — 0
forcing.

**Lesson :** 1) **an attributed requirement must exist in the sealed spec —
verify by artifact (grep), not by memory** (CP authority is not above the
sealed text ; a correct block-and-escalate beats a compliant drift) ; 2) **the
correspondence/mapping table IS the transfer hypothesis** — re-processing the
source at evaluation time couples the target verdict to source geometry and
breaks target-only falsifiability ; 3) **source ambiguity adds information the
target alone cannot produce** (target reference is never ambiguous ; the
source probe forces an honest None where the target predicate would always
return an argmin) — this is what makes the dependence A→T *real*, not
coincidental ; 4) **keep the verdict arbiter sealed and immutable, and prove
the optional runtime coupling on a separate gated channel** — an honest
limitation disclosure (CE2 does not route through A ; runtime-A transfer =
future Phase 3 candidate) preserves both falsifiability and functional
claims ; 5) cross-domain semantic-role transfer by structural correspondence
reaches its pre-registered oracle ceiling exactly (measured CE2 = predicted
D4), confirming explicit declarative rules transfer without re-learning.

**Application :** 1) before any J0/J4 claim, tool-verify the spec quote (the
CP error above is the canonical cautionary tale) ; 2) route every "at
runtime" coupling through a stated channel whose verdict role is explicit
(arbiter vs diagnostic) ; 3) when a source-domain probe makes a role
ambiguous, propagate it as honest None, never a default ; 4) publish the
two-window probe-assignment subtlety (CE2 window 88350-88399 vs CE3 window
88360-88399) so cross-table seed reads do not look like seed-changing ;
5) Lesson 53 closes Phase 2 AGI transfer : **Phases 9-13 of the trajectory
validated on 2 target domains — Phase 3 (runtime-A transfer) is the next
candidate, under a NEW spec.**