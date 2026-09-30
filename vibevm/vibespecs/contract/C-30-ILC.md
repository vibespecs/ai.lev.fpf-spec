# C.30.ILC - Cross-Scope Architecture Residual Triage {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Architectural subpattern under C.30
> **Status:** Stable
> **Normativity:** Normative for FPF pattern, companion-text, and project-description use that claims architecture-specific residuals across declared scopes.

## C.30.ILC:1 - Problem frame {#problem-frame}

Use this pattern when a project situation contains a cross-scope architecture residual for a described holon, often described in project speech as:

```text
"Optimization at the component scope breaks the wider holon."
"We added modularity, but integration exceptions grew."
"Local agent autonomy conflicts with the control or policy scope."
"At one scale window the architecture is stable; at the next, bespoke bridges appear."
"The team optimizes latency, but the evidence or assurance scope becomes unrepairable."
"We may need to add, split, or mediate a declared holon level, declared scope, control layer, interface grammar, work scope, or evidence scope, but it is not clear which architecture move is admissible."
```

**First-minute use slice.** A robotics team says a local controller upgrade made each arm faster, but cell-level stoppages and audit exceptions grew. Before drawing another architecture view, C.30.ILC records: described holon = assembly cell; declared levels and scopes = arm controller, cell control, evidence scope; level-bearing selected structure = control and evidence-reuse structure; residual-bearing locus = control-rate conflict plus evidence-reuse failure; local repair already attempted = retuned each arm controller; first architecture move = add or change mediator relation or control-layer relation and apply `C.30.ASV` for the selected structural view.

The first useful move is `CrossScopeArchitectureResidualTriageRecord@Context`: name the affected declared holon levels or declared scopes, the selected structure in which those levels or scopes are recoverable, residual-bearing locus, local repair already attempted, why local repair is insufficient, and the first admissible architecture move or subject-pattern application.

The primary `EntityOfConcern` is the cross-scope or interlevel architecture residual in the described holon or holon family for a named architecture concern and intended use. The described holon may be an admitted system, organization-as-system, episteme, work occurrence, discipline, or another admitted holon kind. Publication-family material uses the episteme and publication patterns. A MethodDescription is an episteme; a Method uses `A.3.1` and the relations claimed for it. A phrase in a description, a diagram label, or a mathematical-lens output may make the residual visible, but it is not the residual itself and does not become the center of this pattern.

`InterlevelConflict@Context` applies when two or more declared holon levels, declared scopes, or level-bearing structure relations of the same described holon or holon family impose incompatible or tensioned constraints, objectives, admissibility conditions, tempos, resource allocations, information-transfer relations, or assurance requirements. Examples include declared system levels, declared episteme levels, aggregation scopes, typed control layers, declared organizational scopes, work scopes, evidence scopes, system scopes, environment scopes, description-use scopes, publication-use scopes, or other declared scopes. A selected structure matters here only when it carries, separates, or relates the declared levels or scopes. A conflict between structures belongs in C.30.ILC only when those structures are assigned to different declared holon levels, declared scopes, scale windows, or coarse-graining steps; a same-level, same-scope, or unassigned conflict between structures belongs elsewhere until a level, scope, scale-window, or coarse-graining assignment is recovered.

`FrustrationResidual` applies when a persistent cross-scope or interlevel residual remains after local repairs have been attempted or deemed insufficient: local optimization in one declared holon level or declared scope improves local fit while degrading, blocking, or destabilizing another declared holon level, declared scope, or level-bearing structure relation.

`ComplexityGrowthPressure` is admitted only as conditional architecture pressure: reducing an interlevel residual may require adding, splitting, mediating, or stabilizing a declared holon level, declared scope, aggregation scope, interface grammar, control loop, evidence scope, work-method scope, abstraction scope, source-return scope, or declared system level when that special case is being claimed. It is not a claim that complexity is good or that complexity necessarily grows.

Entry condition: if declared holon levels or declared scopes, the selected structure or architecture structure kind that carries them, one residual-bearing locus, and one first admissible architecture move cannot be named for the described holon in context, keep the issue at ordinary problem framing or `ProblemCard@Context`; do not claim `CrossScopeArchitectureResidualTriageRecord@Context` yet.

What goes wrong if C.30.ILC is missed: a local improvement, control layer, scale label, interface grammar, or evidence reuse is treated as whole-holon architecture adequacy while the residual moves into another declared holon level or declared scope.

What this buys: the practitioner can keep useful conflict or frustration language as an entry label while naming the residual-bearing locus, the affected declared holon levels or scopes, the selected structure that carries them, the local repair already attempted, and one first architecture move or subject-pattern application.

`Interlevel conflict` and `frustration` may appear in ordinary project descriptions, but the conforming record describes the residual through declared holon levels or declared scopes, the selected structure that carries them, and a residual-bearing locus. The pattern does not create a generic level scale or `U.Frustration`. It asks which declared holon level, declared scope, aggregation scope, control layer, organizational scope, work scope, evidence scope, system scope, environment scope, scale window, interface grammar, allocation boundary, publication section, or source-return condition bears the residual. A system level or episteme level is a special case of a declared holon level.

Not this pattern when the issue under repair is only ethical value framing, interlevel ethical conflict structure, ethical mediation or decision use, measurement, scale relation, coarse-graining relation, mathematical-lens validation, candidate generation, residual-reducing candidate-set work, final selection, causal outcome, evidence, or assurance. Use the subject pattern and keep C.30.ILC only to the architecture residual-bearing locus.

## C.30.ILC:2 - Problem {#problem}

Architecture work often starts from a residual: a local fix works in one declared holon level or declared scope and fails in another. Component optimization increases whole-holon or product-line integration cost. A new module boundary reduces local complexity and increases exceptions at the product-line scope. A control layer improves local safety and creates accountability or latency claims elsewhere. A reusable evidence set reduces repeated work and hides a new source-return condition.

The useful architecture intuition is narrower than a new `Frustration` kind: local optimization at one declared holon level or declared scope can create a persistent residual in another declared holon level, declared scope, or level-bearing structure relation. When a recoverable multilevel, scale, or coarse-graining mapping is claimed, use `C.29` to state and test that lens use. When the claim compares architecture alternatives over a declared scale window, use `C.31.ASAP`. Use `C.32.MLAO` and `C.32` for residual-reducing candidate work, and use `G.5` only to declare a selected-set result. If that result is made available to an audience, use `E.17` for a source-backed publication face and return to source and `E.24.PUB` for the publication occurrence, form, carrier, audience, bounded use, and availability. An ordinary conflict between structures is not enough for the RG lens or frustration mathematical lens, but a conflict between structures assigned to different declared holon levels or scale windows may be enough when the mapping, preserved-structure line, and lost-structure line are recoverable. The first C.30.ILC output is only the grounded triage record.

Without a pattern, teams either discuss the residual as vague `complexity`, treat it as an ordinary negotiation problem, jump into measurement, use mathematical frustration language as proof, or jump to candidate generation too early. `C.30.ILC` keeps the first move small: identify whether the residual is architecture-shaping and name the first admissible architecture move or subject-pattern application.

The practical work is often not to draw another view. It is to assign the residual to the locus named by value that can bear it: declared holon level, declared scope, level-bearing selected structure, structure kind, constraint, characteristic or Q-bundle, evidence-reuse boundary, source-return condition, or non-architecture claim kind.

## C.30.ILC:3 - Forces {#forces}

* Local optimization can be real and still be harmful at another declared holon level or declared scope.
* `Level`, `layer`, `scope`, `scale`, `abstraction`, `organization`, `system`, and `environment` labels can sound precise while naming different project-side entities, relations, scopes, or claim kinds.
* Frustration language can be useful because it points to incompatible constraints or fitness contributions, but it can also smuggle a physics, biology, psychology, or global-optimizer ontology into architecture prose.
* Measurement is tempting because the residual feels numeric, but a measure before declared-scope and structure-kind recovery can hide the real conflict.
* Ethical conflict or mediation may be present, but not every cross-scope residual is an ethical conflict or mediation problem.
* Architecture synthesis may be needed, but a small triage output often identifies a narrower move: split scope, add mediator, add interface grammar, change allocation, expose coupling, add evidence scope, accept bounded exception, or return to source.
* The pattern is not a prescribed sequence of moves; architecture work is often case-managed through loops, checks, and dead ends.

## C.30.ILC:4 - Solution {#solution}

Create a `CrossScopeArchitectureResidualTriageRecord@Context` when an architecture concern is carried by residuals across declared holon levels, declared scopes, or level-bearing structure relations.

```text
CrossScopeArchitectureResidualTriageRecord@Context ::= {
  describedHolonRef,
  architectureConcernCue,
  intendedArchitectureUse,
  claimScopeRef?: U.ClaimScope,
  qualificationWindowRef?,
  boundedModelUseStructureRef?,

  declaredHolonLevelRefs?: FinSet(DeclaredHolonLevelRef),
  declaredScopeRefs: FinSet(AggregationScopeRef | DeclaredSystemLevelRef |
                            ControlLayerRef | WorkEvidenceScopeRef |
                            OrganizationScopeRef | SystemEnvironmentScopeRef |
                            RateBandRef | ScaleWindowRef |
                            PublicationSectionRef | OtherDeclaredScopeRef),
  structureKindRefs: FinSet(ArchitectureStructureKindRef),

  interlevelConflictDescription?,
  conflictCarrierRefs?:
    FinSet(ConstraintRef | ObjectiveRef | AdmissibilityConditionRef |
           TempoRef | ResourceAllocationRef | InformationTransferRelationRef |
           AssuranceRequirementRef | OtherDeclaredConflictCarrierRef),
  localScopeOptimizationClaim?,
  widerScopeOptimizationClaim?,
  conflictingConstraintRefs?,
  conflictingCharacteristicRefs?,
  conflictingQBundleRefs?,

  symptom,
  crossScopeResidualDescription,
  crossScopeResidualLocusKind:
    hiddenCoupling | interfaceException | controlRateConflict |
    scaleWindowLoss | evidenceReuseFailure | regulatoryBespokeResidue |
    workMethodException | dataSemanticDrift |
    placementJurisdictionConflict | securityTrustBoundaryBreak |
    otherDeclared,
  frustrationResidualBefore?,
  complexityGrowthPressure?,
  localRepairAttempted?,
  whyLocalRepairInsufficient?,

  firstAdmissibleArchitectureMove:
    splitDeclaredHolonLevel | mergeDeclaredHolonLevel |
    splitDeclaredScope | mergeDeclaredScope |
    splitDeclaredSystemLevel | mergeDeclaredSystemLevel |
    addMediator | addInterfaceGrammar | addControlLayer |
    addEvidenceScope | addWorkMethodScope | changeAllocation |
    exposeHiddenCoupling | acceptBoundedException |
    applyD3D4 | applyC28 | noArchitectureMove,

  triggeredPatternLocators?,
  admissibleNextMove,
  stopCondition,
  sourceReturnCondition?
}
```

**Layer, level, tier, stack, and declared-scope labels.** `Declared holon level` is the general level-bearing recovery field for this pattern; system level and episteme level are special cases when the described holon or selected structure makes them relevant to the claim. `System level` may remain as ordinary recognition language when a practitioner would naturally use it, but the record recovers the project-side scope references through `declaredHolonLevelRefs` or `declaredScopeRefs`; a system level is not the default architecture level. When the source says layer, level, tier, or stack, recover exactly one or more of: `declaredHolonLevelRef`, `controlLayerRef`, `declaredSystemLevelRef`, `aggregationScopeRef`, `rateBandRef`, `organizationLevelRef`, `workEvidenceScopeRef`, `scaleWindowRef`, or `publicationSectionRef` when the wording only names a document layer. A move such as `splitDeclaredHolonLevel`, `splitDeclaredScope`, or, in the special system-level case, `splitDeclaredSystemLevel` is admissible only when the affected declared holon level, declared scope, selected structure, declared system level, aggregation scope, control layer, organization scope, work scope, evidence scope, system scope, environment scope, rate band, scale window, publication section, or source-return condition is named. A layer label is not a structure kind, not a system level, not a rate band, and not evidence of separation by itself.

**Interlevel conflict, frustration residual, and complexity-growth recovery.** A conflict is architecture-shaping only when the record names the declared holon levels or declared scopes, the selected structure or structure kind that carries them, and the conflict carrier: constraint, objective, admissibility condition, tempo, resource allocation, information-transfer relation, or assurance requirement. A frustration residual is architecture-shaping only when local repair or local optimization leaves a persistent residual in another declared holon level, declared scope, or level-bearing structure relation. Complexity-growth pressure is only a candidate reason to add, split, mediate, or stabilize structure when that change is expected to reduce the residual enough to justify the new cost and its own residue.

`crossScopeResidualDescription` is not enough by itself. A residual becomes architecture-shaping only when its residual-bearing locus is declared: hidden coupling, interface exception, control-rate conflict, scale-window loss, evidence-reuse failure, regulatory bespoke residue, work-method exception, data-semantics drift, placement or jurisdiction conflict, security trust-boundary break, or another declared locus.

**Multilevel optimization boundary.** First establish whether local optimization in one declared holon level or scope degrades another declared holon level or scope. This triage neither optimizes the architecture nor proves that one global function exists. Use `C.29` with `MLU.Description@MultilevelLearningFrustration` only when the mathematical representation supplies a recoverable mapping between declared levels, scopes, scale windows, or coarse-graining steps and states what structure is preserved and lost. Conflicting structures can enter this lens only when each structure is assigned to a declared holon level, scope, scale window, or coarse-graining step and the mapping shows why the conflict is interlevel. If scale window, RG relation, coarse-graining relation, preserved structure, lost structure, or conflict residual slope becomes an architecture scale-preference claim, use `C.31.ASAP` and keep any mathematical-lens claim in `C.29`. If the practitioner needs to generate residual-reducing candidate architecture moves, apply `C.32.MLAO` for the residual-reducing multilevel candidate frame and `C.32` for the candidate palette. Use `A.19.CPM` for comparison under a declared comparator, `G.5` only when selected-set result declaration is current, and `C.11` when final local choice is current. For audience publication, use `E.17` for a source-backed face and return to source and `E.24.PUB` for the publication occurrence and audience availability. Use `C.32.PAD` when a project architecture decision is current. Stop the C.30.ILC use at the residual and first admissible move. If the case is only a conflict between two selected structures with no declared multilevel or scale mapping, keep it in `C.30`, `C.30.ASV`, `D.3`, `D.4`, `C.28`, evidence, assurance, or decision patterns as applicable.

Anti-collapse rule: no generic frustration score, no risk-matrix residual, no ethical-mediation takeover, no physics or biology ontology transfer, no global-optimizer proof, no causal proof, and no assurance proof. A frustration or risk label does not govern the case until declared holon levels or declared scopes, the selected structure or structure kind that carries them, residual-bearing locus, and first architecture move are recoverable; `D.3` applies only when an interlevel ethical conflict needs an inspectable description; `D.4` applies only when mediation or decision use of that D.3 description is current.

**Stop condition.** Stop after `CrossScopeArchitectureResidualTriageRecord@Context` when it names the residual and the first admissible architecture move. It does not measure scale preference, generate candidate architectures, mediate ethical conflict, or select a decision. Apply a subject pattern only when a claim kind being made exists:

| Claim kind being made | Subject pattern to apply |
|---|---|
| measurement or characteristic claim | `C.16` or the characteristic pattern that defines or constrains the characteristic under evaluation |
| scale window, RG relation, coarse-graining relation, preserved structure, lost structure, or conflict residual slope | `C.31.ASAP` when an architecture scale-preference claim is being made; use `C.29` when mathematical-lens use is being claimed |
| multilevel learning or frustration mathematical-lens use with recoverable level mapping or scale mapping | `C.29` with `MLU.Description@MultilevelLearningFrustration` |
| candidate generation or residual-reducing candidate architecture moves | `C.32.MLAO` when the residual-reducing multilevel frame is current; `C.32` for the candidate palette; `G.5` when selected-set result declaration is current; `E.17` for a source-backed publication face and source return and `E.24.PUB` for the publication occurrence and audience availability when publication is current; `C.11` when final local choice is current; `C.32.PAD` when a project architecture decision is current |
| final local choice | `C.11` |
| causal outcome claim | `C.28` |
| evidence or assurance | `A.10` for source recovery and bounded reliance; `G.6` for addressable provenance paths; `B.3` when a named assurance claim is current |
| ethical conflict description, mediation, or decision use | `D.3` for the interlevel ethical conflict description; `D.4` for mediation and decision use of that description |

**D.3 and D.4 boundary.** A D.3 use identifies an interlevel ethical conflict-description episteme: it connects each ethical claim to the affected entity, declared level relation or scope, value-frame edition, expected consequence, horizon, and evidence use or uncertainty when current, then states the tension among the sides. A D.4 use takes that description into mediation, refusal, evidence demand, causal return, assurance return, architecture return, accepted residual, or bounded decision use. `C.30.ILC` handles architecture-specific recognition: whether the conflict or residual is borne by declared holon levels or declared scopes within a selected structure. Such a residual may concern allocation, interfaces, control rates, work reuse, evidence reuse, scale windows, or coarse-graining loss. Structural views may help describe the selected structure and locate the residual. `C.30.ILC` is a triage and architecture-move pattern, not an ethical mediation pattern.

**Architecture-move examples.**

| Cue | Admissible architecture move | Non-admissible overread |
|---|---|---|
| Component optimization breaks integration | expose hidden coupling; add interface grammar; change allocation | Treat local performance as whole-holon adequacy. |
| Modularity reduces local work and increases exceptions | accept bounded exception; revise module boundary; add work scope or evidence scope | Average exceptions into a modularity score without declared scope, comparator, and measurement relation. |
| Local autonomy conflicts with control scope | add control layer; change allocation; apply `C.30.LCA` | Treat autonomy label as causal or safety proof. |
| Evidence reuse hides source loss | add evidence scope; add source-return condition; use `A.10` for source recovery and bounded reliance, and `G.6` when the provenance path must remain addressable | Treat reused evidence as automatically valid in the wider scope. |
| A scale window changes the residual | apply `C.31.ASAP`, with `C.29` when scale-lens use is being made | Treat two observations as a universal scale law. |
| A frustration lens with recoverable level mapping or scale mapping makes candidate moves comparable | use `C.29` for lens adequacy; use `C.32.MLAO` and `C.32` when a residual-reducing candidate palette is current; use `G.5` only when selected-set result declaration is current | Treat an unassigned or same-scope structure conflict as RG mathematics or frustration mathematics, or treat an interlevel residual without recoverable mapping as a global optimizer, proof, or selected architecture. |

**Worked slice A - clean module layout, bad flow.** A product team redraws modules so each component has an explicit responsibility relation or enactor relation, but order-to-cash flow now crosses more work transfers and exceptions rise. `C.30.ILC` names the module structure, transformation-flow structure, affected work scope, cross-scope residual, and first move: expose hidden coupling or apply `C.30.TFS-REL`. It does not turn the exception count into a modularity measure until `C.16` or the characteristic pattern governing the characteristic under evaluation is applied.

**Worked slice B - AI agent control conflict.** A local agent optimizes its local objective and violates a supervisor's allowed-mode constraint. `C.30.ILC` names the agent scope, supervisor scope or control scope, control relation, local optimization claim, residual-bearing locus, and local repair attempted. The first move may be add control layer, change allocation, or apply `C.30.LCA`. Safety, causality, and gate claims use their subject patterns.

**Worked slice C - evidence scope residue.** A reusable certification evidence set removes repeated evidence work for several product variants, but one variant has a hidden environment difference. `C.30.ILC` names the work scope or evidence scope and source-return condition. The practitioner uses `A.10` for source recovery and bounded reliance, and `G.6` when the provenance path must remain addressable. Whether the evidence meets the certification requirements for that variant is tested under the applicable certification rule.

**Worked slice D - frustration residual before synthesis.** Several decompositions reduce local module work but each creates a different integration, control-rate, or evidence-reuse residual in another declared scope. `C.30.ILC` records the residuals and first architecture moves. If the team needs a residual-reducing candidate palette, stop the C.30.ILC use and apply `C.32.MLAO` for the residual-reducing frame and `C.32` for the candidate palette. Use `G.5` only when the palette or retained set must be declared as a selected-set result for downstream use. If the team claims a multilevel-learning lens or frustration lens, `C.29` carries the lens-use fields and stop condition only after the level mapping, scope mapping, scale-window mapping, or coarse-graining mapping and preserved structure and lost structure are recoverable.

## C.30.ILC:7 - Conformance Checklist {#conformance-checklist}

| ID | Check | Why it matters |
|---|---|---|
| CC-ILC-1 | @fact:CC-ILC-1 A conforming use names `describedHolonRef`, the architecture concern, intended use, ClaimScope or qualification window when each changes the result, and any independently selected bounded model-use structure actually relied on. @status:spec/done | Keeps the triage grounded without narrowing architecture to systems or making a generic context field supply locality. |
| CC-ILC-2 | @fact:CC-ILC-2 A conforming use names declared holon levels or declared scopes, not only `level`, `layer`, `scope`, or `scale` prose. @status:spec/done | Prevents pseudo-level and pseudo-scope reasoning. |
| CC-ILC-3 | @fact:CC-ILC-3 A conforming use names the selected structure or structure kind that carries, separates, or relates the declared levels or scopes affected by the residual. @status:spec/done | Keeps the residual interlevel rather than merely a same-level, same-scope, or unassigned conflict between structures. |
| CC-ILC-4 | @fact:CC-ILC-4 A conforming use records conflict carriers, local repair attempted, and why local repair was insufficient when a conflict or local repair is claimed. @status:spec/done | Prevents premature synthesis and repeated local fixes. |
| CC-ILC-5 | @fact:CC-ILC-5 A conforming use states one first admissible architecture move or `noArchitectureMove`. @status:spec/done | Makes the output action-guiding without candidate generation. |
| CC-ILC-6 | @fact:CC-ILC-6 Evidence, assurance, measurement, causal, ethical, selection, scale, RG, coarse-graining, mathematical-lens, and residual-reducing candidate-set claim kinds use their subject patterns. @status:spec/done | Prevents triage from becoming proof, lens adequacy, mediation, synthesis, or selection. |
| CC-ILC-7 | @fact:CC-ILC-7 If a source-return condition is needed, the record states what hidden or lost distinction triggers return to the source. @status:spec/done | Protects compressed and extracted views. |
| CC-ILC-8 | @fact:CC-ILC-8 The stop condition is visible. @status:spec/done | Prevents the triage pattern from expanding into a hidden prescribed sequence. |
| CC-ILC-9 | @fact:CC-ILC-9 If multilevel learning or frustration is used as mathematics, the record names `C.29`, `MLU.Description@MultilevelLearningFrustration`, the recoverable level mapping or scale mapping, and preserved structure and lost structure; if residual-reducing candidate moves form a candidate set being used, the record names `C.32.MLAO` and `C.32`; if the retained-set result is being declared, it names `G.5`; if that result is made available to an audience, it names `E.17` for a source-backed publication face and source return and `E.24.PUB` for the publication occurrence and audience availability. @status:spec/done | Preserves the useful multilevel optimization line without importing ontology, proof, or a hidden selector. |

## C.30.ILC:9 - Consequences {#consequences}

The gain is an early architecture move that is small and precise. The practitioner can preserve useful problem language such as conflict, frustration, level, layer, or local optimization while recovering the FPF fields that keep the claim reviewable.

The cost is that `C.30.ILC` refuses to solve the whole problem. It identifies the first architecture move or subject-pattern application. Measurement, scale relation, RG relation, coarse-graining relation, mathematical lens use, ethical mediation, candidate generation, evidence, assurance, and final choice remain outside until those claims are being made.

This makes multilevel optimization usable rather than decorative. Use `C.30.ILC` to identify the residual that makes optimization relevant, `C.29` for an admissible mathematical-lens use only when level or scale mapping and preserved and lost structure are recoverable, `C.32.MLAO` and `C.32` for residual-reducing candidate frames and palettes, `G.5` for selected-set result declaration, and `C.32.PAD` for a project architecture decision. For publication, use `E.17` for a source-backed face and source return and `E.24.PUB` for the publication occurrence and audience availability.

## C.30.ILC:12 - Relations {#relations}

* Builds on `C.30` and `C.30.ASV` for grounded architecture, selected-structure, and structural-view adequacy.
* Uses `A.22` for selected-structure grounding.
* When the residual concerns flow, control, function, allocation, module, or interface structure, use the applicable pattern: `C.30.TFS-REL` for the bounded architecture-use record connecting an architecture locus to a transformation-flow structure or network; `C.30.LCA` for the selected control structure, its description, and view conformance when current; `A.6.F` for function-use repair; and `A.6.M` for module-interface claim repair.
* Applies `C.16` or the characteristic pattern that defines or constrains the characteristic under evaluation for measurement or characteristic claims.
* Applies `C.29` with `MLU.Description@MultilevelLearningFrustration` only when multilevel learning or frustration is used as a mathematical lens with recoverable level mapping or scale mapping and preserved structure and lost structure; applies `C.31.ASAP` for architecture scale-preference claims and `C.29` for mathematical-lens claims when scale, RG, coarse-graining, preserved structure, lost structure, or scale-window adequacy is being claimed.
* Applies `C.32.P2S` when residual triage must continue through problem-to-structure architecturing; applies `C.32.MLAO` for residual-reducing multilevel candidate frames and `C.32` for candidate palettes; applies `G.5` only when selected-set result declaration is current.
* Applies `C.11` for final local choice, `C.28` for causal outcome claims, `A.10` for source recovery and bounded reliance, `G.6` for addressable provenance paths, `B.3` when a named assurance claim is current, `D.3` for the interlevel ethical conflict description, and `D.4` for mediation and decision use of that description.

When audience availability is current, use `E.17` for a source-backed face and return to source and `E.24.PUB` for the publication occurrence, form, carrier, audience, bounded use, and availability. Use `C.30.ILC` only to triage a cross-scope architecture residual.


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/C-30#root, spec://ai.lev/fpf-spec/contract/C-30-ASV#root, spec://ai.lev/fpf-spec/contract/A-22#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/C-32-MLAO#root, spec://ai.lev/fpf-spec/contract/C-32#root, spec://ai.lev/fpf-spec/contract/C-32-PAD#root, spec://ai.lev/fpf-spec/contract/C-31-ASAP#root, spec://ai.lev/fpf-spec/contract/C-16#root, spec://ai.lev/fpf-spec/contract/C-29#root, spec://ai.lev/fpf-spec/contract/G-5#root, spec://ai.lev/fpf-spec/contract/C-11#root, spec://ai.lev/fpf-spec/contract/C-28#root, spec://ai.lev/fpf-spec/contract/A-10#root, spec://ai.lev/fpf-spec/contract/B-3#root, spec://ai.lev/fpf-spec/contract/G-6#root, spec://ai.lev/fpf-spec/contract/D-3#root, spec://ai.lev/fpf-spec/contract/D-4#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-1-CSD#root, spec://ai.lev/fpf-spec/contract/B-2#root, spec://ai.lev/fpf-spec/contract/B-2-P#root, spec://ai.lev/fpf-spec/contract/C-30#root, spec://ai.lev/fpf-spec/contract/C-30-AD#root, spec://ai.lev/fpf-spec/contract/C-30-AD-BA#root, spec://ai.lev/fpf-spec/contract/C-30-ASV#root, spec://ai.lev/fpf-spec/contract/C-30-P#root, spec://ai.lev/fpf-spec/contract/C-30-STRAT#root, spec://ai.lev/fpf-spec/contract/C-31-ASAP#root, spec://ai.lev/fpf-spec/contract/C-32#root, spec://ai.lev/fpf-spec/contract/C-32-MLAO#root, spec://ai.lev/fpf-spec/contract/D-2#root, spec://ai.lev/fpf-spec/contract/D-3#root, spec://ai.lev/fpf-spec/contract/D-4#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/C-30-ILC
