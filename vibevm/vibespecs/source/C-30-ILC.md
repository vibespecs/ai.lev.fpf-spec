# C.30.ILC - Cross-Scope Architecture Residual Triage: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## C.30.ILC:5 - Archetypal Grounding {#archetypal-grounding}

| Archetype | Without C.30.ILC | With C.30.ILC |
|---|---|---|
| Holon levels | A residual across component, system, episteme, publication-use, control, environment, or product-line scopes is called generic complexity. | The affected declared holon levels or declared scopes, the level-bearing structure, the residual, and the first architecture move are named. |
| Episteme as described holon | A diagram, measurement note, or conflict memo has its own structure, but a second description about it is interpreted as if it already selected a repair. | The episteme can be the described holon; the description of that episteme remains separate from decision, evidence, measurement, selection, or mediation and is governed by the subject pattern when those claims are being made. |

## C.30.ILC:6 - Bias-Annotation {#bias-annotation}

* **Local-success bias.** A local improvement is treated as whole-architecture improvement. Repair by naming the wider declared holon level or declared scope and the residual.
* **Pseudo-level bias.** `Level`, `layer`, or `scope` sounds precise but no declared holon level or declared scope exists. Repair through `declaredHolonLevelRefs` or `declaredScopeRefs`.
* **Generic-structure-conflict bias.** A conflict between selected structures is treated as interlevel conflict even though no declared holon level, scale window, or coarse-graining relation is recoverable. Repair by keeping the case in `C.30`, `C.30.ASV`, or the subject pattern unless the structures are assigned to different declared holon levels or scale windows.
* **Frustration-ontology bias.** A useful conflict or frustration entry label becomes a new first-order architecture kind, physics ontology, biology ontology, or psychology claim. Repair by recovering declared holon levels or declared scopes, the level-bearing structure, conflict carriers, residual-bearing locus, and the subject pattern for any lens, proof, evidence, mediation, or synthesis claim.
* **Global-optimizer bias.** Local optimization in one declared holon level or declared scope is used as if the architecture literally optimizes one global function. Repair by keeping the local optimization claim as a triage input unless `C.29` supplies an admissible mathematical-lens use with recoverable level mapping or scale mapping and the candidate-set or decision pattern carries any synthesis or selection claim.
* **Measurement-first bias.** A residual is measured before its level-bearing structure and scope grounding are declared. Repair by applying `C.16` or the characteristic pattern governing the characteristic under evaluation only after triage names the affected characteristic or measurement relation.
* **Mediation-default bias.** Every conflict is treated as ethical mediation or negotiation. Repair by checking whether the use under repair is architecture structure, allocation, interface grammar, control, work or evidence scope, source-return, or another declared level-bearing architecture relation.
* **Synthesis-jump bias.** A local residual immediately triggers candidate generation. Repair by identifying the first admissible architecture move before applying `C.32.MLAO` and `C.32`; use `G.5` only when selected-set result declaration is current.

The conformance checklist below verifies the preceding guidance after the practitioner has chosen the repair action; it is not a required project control form and not a substitute for the card, note, view, relation, or repair guidance above.

## C.30.ILC:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Symptom | Repair |
|---|---|---|
| Generic complexity bucket | Everything becomes `complexity` or `interlevel conflict`. | Name declared holon levels or declared scopes, level-bearing structure, residual, and first architecture move. |
| Structure conflict as interlevel conflict | Two structures are in tension, but no declared holon level, scale window, or coarse-graining relation is recoverable. | Use `C.30`, `C.30.ASV`, `D.3`, `D.4`, `C.28`, evidence, assurance, or decision patterns as applicable; use C.30.ILC only when the conflict is across declared levels or scopes. |
| Frustration-as-ontology | `Frustration` is treated as a new FPF kind, psychological state, physics kind, biology kind, assurance score, or proof. | Keep frustration as an entry label; recover `FrustrationResidual`, conflict carriers, residual-bearing locus, and subject patterns for `C.29`, evidence, assurance, causal, mediation, or synthesis claims when those claim kinds are being made. |
| Optimization-as-global-proof | A local optimization claim is treated as proof that the whole architecture optimizes one global objective. | Record local and wider-scope claims separately; use `C.29` only for an admissible mathematical lens with recoverable level mapping or scale mapping and use candidate-generation, comparison, or decision patterns for synthesis and selection. |
| Measurement-first conflict | The team starts measuring before declaring what is in conflict. | Run ILC triage first; apply `C.16` or the characteristic pattern governing the characteristic under evaluation only when the measured characteristic is under evaluation. |
| Risk color as cross-scope decision | A red, yellow, or green risk cell, risk matrix, or maturity score decides the cross-scope architecture move or resource-allocation priority. | Recover declared holon levels or declared scopes, structure kind under consideration, the residual, the loss, hazard, or threat relation, selected source, evidence, or relation interpretation, characteristic scale, comparator, gate pattern, and first admissible architecture move; do not treat ordinal risk color as architecture adequacy, evidence sufficiency, causal proof, assurance proof, resource-allocation priority, or gate passage. |
| Mediation-only conflict | A structural residual is treated as ethical mediation with no architecture move. | Use `D.3` only when an interlevel ethical conflict needs a description and `D.4` only when that description is being mediated or used in a decision. |
| Hidden candidate generation | The residual immediately spawns many designs. | State the first admissible move; apply `C.32.MLAO` and `C.32` only when residual-reducing candidate work is being claimed, and apply `G.5` only when selected-set result declaration is current. |
| Scope word without scope record | The text says `level`, `layer`, `scale`, or `scope` without a declared field. | Recover the declared holon level or declared scope named by value, or demote the phrase to ordinary recognition. |

## C.30.ILC:10 - Rationale {#rationale}

Interlevel conflict and frustration are useful Plain entry labels because they point to a recurrent architecture failure: local repair in one declared holon level or declared scope leaves a residual in another. They are dangerous as generic labels because they can hide which level, scope, level-bearing structure, relation, conflict carrier, or source-return condition bears the residual.

A local optimum or successful local repair is therefore not treated as whole-architecture adequacy. It becomes relevant to C.30.ILC triage only when the residual-bearing locus is recoverable and the next architecture use can be named.

`C.30.ILC` keeps the entry label but recovers the architecture relation or structure claim. It treats conflict or frustration as architecture-shaping only when declared holon levels or declared scopes, the level-bearing structure, conflict carriers, and residual-bearing loci are named. This lets FPF preserve the practical intuition without introducing a second ontology of levels, a hidden measurement pattern, a physics or biology transfer, a global optimizer proof, or a prescribed architecture work order.

## C.30.ILC:11 - SoTA-Echoing {#sota-echoing}

| SoTA and practice source | What it contributes | FPF adoption stance | Practitioner implication |
|---|---|---|---|
| Scenario-based architecture trade-off practice, with ATAM-like reasoning used here as lineage and practice source for concern, scenario, sensitivity point, and trade-off recognition rather than as a decision or evidence method. | Architecture work often starts from cross-concern and cross-scope trade-offs rather than one local measurement result. | Adopt and adapt: use the conflict cue for triage, require declared holon levels or scopes, level-bearing structure, and subject patterns for final selection, evidence, assurance, and gate passage. | A residual can start an architecture move without becoming a decision, proof, or safety case. |
| Vanchurin, Wolf, Katsnelson, and Koonin multilevel learning and frustration line, plus the Akhtyrchenko, Katsnelson, and Ustyuzhanin 2026 MSPD paper as selected source pressure rather than full-literature ranking. | Local optimization at one declared holon level, scope, or level-bearing structure relation can create persistent residual in another; frustrated optimization and MSPD-like reasoning can be candidate mathematical lenses when a level mapping or scale mapping is recoverable. | Adopt and adapt: `C.30.ILC` uses this line for architecture triage only. `C.29` with `MLU.Description@MultilevelLearningFrustration` carries mathematical-lens adequacy with preserved structure and lost structure; no `U.Frustration`, universal architecture metric, physics or biology ontology transfer, global optimizer proof, causal proof, assurance proof, or ethical-mediation takeover. | First recover holon levels or scopes, level-bearing structure, conflict carriers, residual-bearing locus, local repair, and the first architecture move. Apply `C.29` only when the lens mapping is being claimed; apply `C.32.MLAO` and `C.32` only when residual-reducing candidate work is current; apply `G.5` only when selected-set result declaration is current. |
| Control and cyber-physical systems practice. | Local autonomy, feedback, supervisor relations, and rate separation can create cross-scope conflict. | Reuse through `C.30.LCA`, `B.2.5`, `C.27`, and `A.3.3`; do not let ILC carry control proof. | A control conflict is governed by control-structure or dynamics patterns only when those claims are being made. |
| FPF source-return and semantic-coarsening discipline. | Compressed views and reusable records can hide distinctions that matter in a wider scope. | Adopt: add `sourceReturnCondition?` when hidden distinctions carry the residual. | A bounded exception or source-return trigger may be the correct first move. |


## C.30.ILC:End {#end}
