# C.32.MLAO - Architecture Candidates to Reduce Cross-Scope Residuals {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Architectural subpattern under C.32
> **Status:** Stable
> **Normativity:** Normative unless explicitly marked informative

## C.32.MLAO:1 - Problem frame {#problem-frame}

Use this pattern when a practitioner has a recoverable cross-scope or interlevel architecture residual and needs candidate architecture changes that reduce that residual under a declared evolution window.

Primary working reader: an architect or architecture-responsible practitioner who has already recovered a residual and must prepare candidate changes without calling a local improvement a whole-holon optimum.

Typical entry phrases:

```text
"The local architecture improvement made another scope worse."
"The platform helps product teams but grows evidence exceptions."
"Local agent autonomy conflicts with the control or policy scope."
"The method template speeds authoring and slows review."
"A graph, residual vector, or Pareto front can inform comparison only after selected structures, residuals, losses, and the pattern for the next question are declared; it is not the architecture."
```

**First-minute use slice.** A regulated product-family team has used `C.30.ILC` to name a residual: local product variants are quicker to ship, but certification evidence grows at the family scope. Using C.32.MLAO, the practitioner frames three residual-reducing candidate changes: add evidence scope, narrow interface grammar, or accept a bounded exception with a reopen trigger. Each candidate states the residual it reduces and the new burden it creates. The team now has explicit inputs for `A.19.CPM`, `C.11`, `A.19.SelectorMechanism`, or `G.5` when comparison, local choice, selection, or selected-set result declaration is current.

The primary `EntityOfConcern` is a residual-reducing candidate frame for one grounded architecture question. In plain working terms, the frame asks where a local architecture improvement moved the cost and which candidate can reduce that moved cost without hiding its new burden. The described holon can be a system, organization-as-system, discipline, AI-agent setup, built asset, episteme, work occurrence, or an instance of another admitted holon kind. Recover source labels such as practice, culture, tradition, style, or method before architecture use. Use `E.10.ROLE` for unresolved `role` wording: it may resolve to a local system-role kind, an assignment occurrence, a participant position in a direct relation, a function claim, an organization or representation position, or ordinary wording. Carry only the recovered object or relation, never a generic role-side structure. Candidate Systems, assignments, Methods, plans, and structures remain modal content until their own facts obtain; a publication family appears only under its applicable pattern. Use `E.17` for a source-backed publication face and source return and `E.24.PUB` for the publication occurrence and audience availability. C.32.MLAO is not a universal optimizer, adequacy claim, selector, decision, assurance argument, publication pattern, or software-system-only pattern.

What goes wrong if C.32.MLAO is missed: local success is called whole-holon architecture success, or an optimization phrase hides the residual that shifted to another declared holon-level ref or declared scope ref.

What C.32.MLAO buys in practice: the practitioner can prepare residual-reducing architecture candidates for later comparison by naming residual reduced, new burden created, affected scope, preserved structure, lost structure, and source-return condition.

Ordinary working move: name where the local improvement moved the cost, name the selected structure and scope that now carry the residual, then prepare candidate changes that reduce that residual while making the new burden explicit.

Adoption test: after using C.32.MLAO, a reader can see the residual reduced, the new burden, the affected scope, the preserved structure, the lost structure, and the evolution-window stop condition for each candidate.

Use C.32.MLAO only after residual triage. Do not use it to recover the residual itself, justify a mathematical lens, compare or select candidates, choose locally, declare a selected-set result, publish it to an audience, or decide the project architecture.

Common exits by claim kind:

- `C.30.ILC` when the residual is not recoverable yet.
- `C.32.ACS` when architecture-characteristic criteria rows are missing.
- `C.32.ACE` when eval programs or eval results are the current claim.
- `C.29` when mathematical-lens use is being claimed.
- `A.19.CPM` for explicit comparison, `A.19.SelectorMechanism` for set-returning selection, `C.11` for local choice, and `G.5` for selected-set result declaration.
- `C.18` and `C.19` for archive, front, pool treatment, or stepping-stone retention.
- `C.30.AD` for architecture-description work, `E.17` for a source-backed publication face and source return, and `E.24.PUB` for the publication occurrence and audience availability.
- `C.32.PAD` for project decision.

The first useful output is `MultilevelArchitectureResidualOptimizationFrame@Project`. The frame is a working record for residual-reducing candidate framing. It records residual movement and candidate burdens; it is not a universal optimizer, scalar optimum, C.29 lens result, or architecture decision:

For a first pass, fill only the described holon, optimization question and objective basis, residual-triage ref, affected level or scope refs, selected structures, residual-bearing loci, criteria rows, ClaimScope when needed, evolution window, residual-reducing candidates with residual reduced and new burden, pattern for the next question, and stop condition. Add front, archive, NQD, OEE, C.29 lens, ideality, scale-amenability, function-bearer, and architecture-influence-correspondence refs only when that support is current for the candidate being framed.

```text
MultilevelArchitectureResidualOptimizationFrame@Project:
  projectWorkOccurrenceRef?: U.EntityRef constrained to U.Work
  residualOptimizationFrameProjectUseRelationRef?: U.RelationRef defined by the exact synthesis-use or work-use pattern
  describedHolonRef:
  optimizationQuestion:
  objectiveBasisRefs:
  claimScopeRef?: U.ClaimScope
  residualTriageRef:
  declaredHolonLevelRefs?:
  declaredScopeRefs:
  selectedStructureRefs:
  residualBearingLoci:
  candidatePaletteRef:
  architectureCharacteristicCriteriaSetRef?:
  architectureCharacteristicCriteriaRowRefs:
  qBundleRefs?:
  evolutionWindowRef:
  dynamicFrontOrArchiveRef?:
  nqdOrOeeSupportRef?:
  steppingStoneRefs?:
  architectureIdealityPressureRef?:
  scaleAmenabilityPolicyRef?:
  functionBearerFeasibilityRef?:
  architectureInfluenceCorrespondenceRef?: C.32.CONWAY frame or exact pair-row ref
  residualReducingCandidates:
    - candidateRef:
      selectedStructureChanged:
      affectedLevelOrScope:
      affectedArchitectureCharacteristicRefs:
      affectedCriteriaRowRefs?:
      architectureCharacteristicEvalResultRefs?:
      residualReduced:
      newBurden:
      preservedStructure:
      lostOrHiddenStructure:
      sourceReturnCondition:
  comparisonInputRefs?:
  receivingOperationPatternRef?:
  c29LensOutputRef?:
  metaHolonTransitionRef?:
  stopCondition:
```

Here `@Project` is a compatibility and retrieval cue only. It establishes no project entity, composite-work identity, context, authority, viewpoint, or parthood. When the frame is genuinely used in one actual project, `projectWorkOccurrenceRef` identifies the exact composite `U.Work` and `residualOptimizationFrameProjectUseRelationRef` identifies the direct relation by which that work uses the frame. The frame, the residual-reducing synthesis work, the candidate architectures, and the project work remain distinct.

## C.32.MLAO:2 - Problem {#problem}

Many architecture problems are residual problems. A local module boundary improves one team and creates integration exceptions elsewhere. A control relation improves response and creates audit or timing burden. A platform improves reuse and creates evidence decay. A method family speeds authoring and harms transfer.

The tempting shortcut is to call the local improvement optimized. C.32.MLAO blocks that shortcut by asking: where did the residual shift, which selected structure carries it, and which candidate change reduces it enough to be worth its new burden?

## C.32.MLAO:3 - Forces {#forces}

| Force | Tension |
|---|---|
| Local fit | A candidate may help one scope while harming another. |
| Optimization language | Objective, residual, front, and matrix language sounds decisive before the claim is typed. |
| Declared-level recognition | Level and scope words are useful only after they are declared as holon-level refs or scope refs, or restored as stratification terms through `C.30.STRAT` before selected-structure use. |
| Candidate action | When performing repair work, the practitioner must use the residual triage to prepare candidate changes. |
| New burden | A residual-reducing candidate can create another cost or loss; inspect the affected scopes rather than presuming either losslessness or a positive new burden. |

## C.32.MLAO:4 - Solution {#solution}

Build a residual-reducing frame around one recoverable residual.

Work in eight steps:

1. Start from a `C.30.ILC`-compatible residual triage.
2. Name the affected declared holon-level refs or declared scope refs and the selected structures that carry the residual.
3. Name the architecture-characteristic criteria rows and any Q-Bundle slots that make the residual worth reducing.
4. Create or reference a C.32 candidate palette.
5. For each candidate, state the residual it reduces, the selected structure changed, and the criteria rows affected.
6. Assess the new burden, loss, exception, or source-return load that the candidate could create within the declared evolution window. State what is expected and unresolved; if none is identified, say which affected structures, scopes, and criteria were inspected.
7. Record the evolution window and any support that only keeps candidate plurality or directionality alive, such as NQD, OEE, an archive or front, stepping-stone retention, ideality, or BLP.
8. Stop at the frame, or name the pattern for the next question when a later claim is current: use `A.19.CPM` for explicit comparison, `A.19.SelectorMechanism` for set-returning selection, `G.5` for selected-set result declaration, `C.11` for local choice, `C.32.PAD` for an architecture decision, `C.30.AD` for architecture-description work, and `C.29` for mathematical-lens use. For publication, use `E.17` for a source-backed face and return to source, then `E.24.PUB` for the actual occurrence, form, carrier, audience, bounded use, and availability.

Admit a residual-reducing candidate only when it answers the working questions: which declared holon-level ref or declared scope ref is affected, which selected structure changes, which architecture-characteristic row or Q-Bundle slot is at stake, what residual is reduced, what structure is preserved or lost, and what new burden is expected or why none is currently identified.

| Candidate change family | Use when | Repair it provides |
|---|---|---|
| `splitScope` | One scope carries incompatible tempo, functional demand, constraint, or admissibility condition. | Separates the conflict and names coordination cost. |
| `mergeScope` | Mediation creates more burden than separation saves. | Removes unnecessary boundary and names coupling risk. |
| `addMediator` | Direct cross-scope dependency is brittle. | Adds mediation and names mediator failure mode. |
| `addControlStructure` | Rate, feedback, policy, or supervisor conflict persists. | Adds or changes control relations, states timing burden, and names any direct control-responsibility predicate with actual participants; if none is admitted, records the exact missing governor instead of inferring responsibility from the control structure. |
| `addInterfaceGrammar` | Variation grows through unmanaged interface variants. | Names allowed variation, conformance expectation, and exception risk. |
| `repairFunctionBearerGap` | A residual-reducing functional change has no feasible bearer at the affected declared holon-level ref or scope ref. | Adds or changes an admitted bearer, splits the function, changes placement, resource access, or control relations, or rejects the candidate. Any responsibility change uses its direct domain predicate or exact missing governor. |
| `addEvidenceScope` | Reusable candidate bearer lacks reusable evidence scope. | Makes evidence maintenance part of the candidate. For a current evidence use, apply `A.10` for source recovery and bounded reliance, and the applicable subject rule to judge whether the evidence supports the named claim or meets the named requirement. |
| `addWorkMethodScope` | Repeated work remains bespoke because method structure is missing. | Proposes reusable method structure for the repeated work and names review or training burden. |
| `repairArchitectureInfluenceCorrespondence` | The residual is carried by mismatch between one exact typed influence-side architecture source and transformed-side architecture content for the changed referent. | Open `C.32.CONWAY`; keep the changed referent and any actual A.3.4 `U.Transformation` separate, then prepare candidate alternatives that change the influence-source side, change the transformed side, change both, or keep a bounded mismatch. |
| `acceptBoundedException` | Eliminating the residual costs too much now. | Records exception, source-return condition, and reopen trigger. |

**Comparison-input boundary.** C.32.MLAO prepares comparison inputs; it does not run the comparison or choose a candidate. Its output rows are candidate records with residual reduced, new burden, selected structures, preserved structure, lost structure, source-return condition, and optional C.29 lens-output references.

Those references are diagnostic inputs only.

Admitted profiles and a `ComparatorSpec` belong to the receiving explicit-comparison pattern.

If the current claim is explicit comparison, use `A.19.CPM` with admitted profiles and a declared `ComparatorSpec`. If the claim is local choice over an existing option set, use `C.11`. If the claim is set-returning selection, use `A.19.SelectorMechanism`. If the claim is selected-set result declaration, use `G.5`. For publication, use `E.17` for a source-backed face and source return and `E.24.PUB` for the publication occurrence and audience availability.

**Lens-output discipline.** Graphs, fronts, residual vectors, DSMs, RG-like descriptions, and frustration language are C.29 lens outputs, structural descriptions, or diagnostic signals after their architecture use is typed. The real failure is proxy preference: a candidate is preferred because the output looks better while selected structures, lost structure, architecture characteristics, and pattern for the next question remain unnamed. The repair is to interpret the output over selected structures and state what residual or loss it exposes; any comparison, selection, or choice claim then belongs to its pattern for the next question.

**Method, culture, and episteme discipline.** For a Method-family, culture, practice, or episteme case, first name the described holon, optimization question and use, selected structures, and the pattern that defines or constrains each load-bearing claim. If a publication family or publication face is in view, decide whether it is the described holon, a selected structure, an architecture description, or an MVPK face before using it. C.32.MLAO defines only the residual-reducing architecture candidate frame; use the applicable patterns for Method, Work, publication, evidence, ethical, and decision claims.

**Dynamic candidate discipline.** A preferred or retained candidate is bounded by an evolution window, source conditions, and the pattern for the next question that admitted the preference or retention. NQD, OEE, C.18, and C.19 can keep a front, archive, pool, or stepping stone visible; they do not select the architecture and they do not turn a front member into a durable optimum.

**Ideality and BLP discipline.** TRIZ ideality can suggest residual-reducing candidate changes: remove a support bearer, transfer a useful function onto an existing resource, or generalize a bearer so fewer selected structures carry more useful functions. BLP can prefer a more general scale-amenable bearer only inside its declared scale window and audit boundary. Both lines guide candidate generation; neither removes the need to state new burden, lost structure, and pattern for the next question.

**Functional-bearer feasibility discipline.** A residual-reducing candidate must name a bearer that could perform the function under the declared module, placement, resource, control, information, and evidence constraints. This is a design-time feasibility claim, not proof that the System, assignment, or Work already exists. An assignment supplies neither capability, functioning, function bearing, nor performance. If no feasible bearer can be proposed, add or change a candidate bearer, split the function, change placement, resource access, or control relations, reduce the demand, or mark the C.32 candidate unfit. Responsibility still needs an admitted direct predicate or the exact missing governor.

**Architecture-influence and transformed-side discipline.** When a residual is carried by one independently typed architecture-side source constraining architecture content for a changed referent, use `C.32.CONWAY`. For each actual side, keep the exact C.30 described holon, obtaining `ArchitectureRelation`, and selected `U.Structure` together; keep candidate, required, desired, or expected content in an exact C.30 `ArchitectureClaim`. Keep the changed referent and any actual A.3.4 `U.Transformation` separate. Then prepare residual-reducing candidates that change the influence-source side, the transformed side, both sides, or a bounded mismatch as comparison inputs or downstream candidate alternatives. Influence, transformation, flow, Work, and module-interface claims belong to their exact relation pattern, `A.3.4`, `E.18`, `A.15`, or `A.6.M` when current. Structural-similarity claims belong to `C.29` only when they are current.

**Level, stratification-term, and whole-reidentification discipline.** If the case uses `level`, `system level`, `holon level`, `layer`, `tier`, or another stratification term, first use `E.10.ARCH` and `C.30.STRAT` unless the subject pattern and recovered neighborhood are already named by value. If the case uses `BOSC`, `MHT`, `MET`, `MFT`, emergence-family, boundary-crossing, or promotion-like wording, first use `E.10` and `B.2.P` to recover the claim kind. Use `B.2` only when a whole-reidentification question remains after the existing-whole explanation check; otherwise use the subject pattern for architecture, boundary, capability, function, measurement, publication, work, or lens claims.

**Stop condition.** Stop after the frame names residual, affected declared holon-level refs or declared scope refs, candidate changes, new burdens, preserved and lost structure, source-return conditions, and patterns for the next questions.

**Lowering condition.** Keep the frame as C.32.MLAO work only while the residual triage, affected level or scope refs, selected structures, criteria rows, evolution window, residual reduced, new burden, and pattern for the next question remain current. Lower a candidate to a diagnostic note when the residual is not recoverable, the selected structure is unknown or stale, the architecture characteristic is missing, the new burden is not named, or the pattern for the next question cannot use the row. Retire a candidate when its evolution window closes or a stronger residual triage replaces it. Use `C.30.ILC` when the residual itself is missing, `C.32.ACS` when criteria rows are missing, `C.32.ACE` when eval results are needed but not current, `C.29` when the current claim is a mathematical-lens claim, and `A.19.CPM`, `A.19.SelectorMechanism`, `C.11`, `G.5`, or `C.32.PAD` when the downstream claim is current.

## C.32.MLAO:7 - Conformance Checklist {#conformance-checklist}

| ID | Requirement | Purpose |
|---|---|---|
| `CC-C32.MLAO-1` | @fact:CC-C32-MLAO-1 The use starts from a recoverable residual triage. @status:spec/done | Prevents premature optimization. |
| `CC-C32.MLAO-2` | @fact:CC-C32-MLAO-2 Affected declared holon-level refs or declared scope refs and selected structures are named. @status:spec/done | Keeps multilevel wording reviewable. |
| `CC-C32.MLAO-3` | @fact:CC-C32-MLAO-3 Each candidate names residual reduced, architecture characteristic affected, and new burden. @status:spec/done | Prevents one-sided optimization. |
| `CC-C32.MLAO-4` | @fact:CC-C32-MLAO-4 Comparison inputs, comparison results, selection results, and choice results name their pattern for the next question. @status:spec/done | Keeps C.32.MLAO from performing comparison, selection, or choice locally. |
| `CC-C32.MLAO-5` | @fact:CC-C32-MLAO-5 Lens-backed claims use C.29 when mathematical-lens use is being claimed. @status:spec/done | Keeps mathematical adequacy outside this pattern. |
| `CC-C32.MLAO-6` | @fact:CC-C32-MLAO-6 Source-return condition is present when compression hides distinctions. @status:spec/done | Keeps later source-use or decision-use claims tied to recoverable sources. |
| `CC-C32.MLAO-7` | @fact:CC-C32-MLAO-7 Evolution window, dynamic front or archive relation, and any NQD or OEE support are typed as retention or generation support only. @status:spec/done | Blocks static-optimum and selector overread. |
| `CC-C32.MLAO-8` | @fact:CC-C32-MLAO-8 Influence-source and transformed-side architecture content stay distinct through exact C.30 holon, obtaining-`ArchitectureRelation`, selected-structure, or modal-`ArchitectureClaim` refs; the changed referent and any actual A.3.4 transformation stay separate; `C.32.CONWAY` is used when correspondence candidates are being prepared. @status:spec/done | Preserves kind distinction among architecture content, influence, Work, actual transformation, and structural similarity. |

## C.32.MLAO:9 - Consequences {#consequences}

| Positive consequence | Cost or trade-off |
|---|---|
| Residual-reducing architecture candidates are made explicit. | The practitioner must name the affected levels or scopes, selected structures, residuals, preserved structure, lost structure, new burdens, and the pattern for the next question for any comparison or choice claim. Use `C.30.STRAT` or `B.2.P` first when level wording or whole-reidentification wording is not yet typed. |
| Optimization language is usable without carrying architecture adequacy. | No scalar selector or architecture decision is available by wording alone. |
| Holonic breadth is preserved. | Non-software cases must still recover their selected structures and patterns for the next questions. |
| Residual triage and candidate framing stay distinct. | The team may need both `C.30.ILC` and C.32.MLAO. |
| Compressed representations can guide action. | Source-return triggers must be visible. |

## C.32.MLAO:12 - Relations {#relations}

- **Builds on:** `C.30.ILC` for residual triage, `C.32` for palettes, `C.32.ACS` for architecture-characteristic criteria rows, `C.32.ACE` for eval programs and eval results, `C.29` for mathematical-lens use when claimed, `A.19.CPM` for explicit comparison, `A.19.SelectorMechanism` for set-returning selection, `C.11` for local choice over an existing option set, `G.5` for selected-set result declaration, `C.19.1` for scale-amenability preference claims, and `C.31` or `C.31.ASAP` for characteristic or scale-preference claims.
- **Uses:** `E.10.ARCH` and `C.30.STRAT` when stratification terms hide the recovered neighborhood; `E.10` and `B.2.P` when BOSC, emergence-family, MHT, MET, MFT, boundary-crossing, or promotion-like wording hides the claim kind; `B.2` when the candidate creates, reidentifies, splits, joins, or changes the relevant whole after existing-whole explanations are insufficient; `C.32.CONWAY` when residual reduction requires co-synthesis of exact influence-source and transformed-side architecture content; `A.6.M`, `C.30.LCA`, `C.30.TFS-REL`, and method or work patterns when their structures are the affected selected structures.
- **Patterns for the next questions:** `A.19.CPM` for explicit comparison, `A.19.SelectorMechanism` for set-returning selection, `G.5` for selected-set result declaration, `C.11` for fixed local choice, `C.30.AD` for architecture-description work, `E.17` for a source-backed publication face and source return, `E.24.PUB` for the publication occurrence and audience availability, and `C.32.PAD` for project architecture decisions.
- **P2S docking:** `C.32.P2S` uses MLAO when cross-scope, interlevel, interlayer, or meta-holon residual pressure must become candidate-synthesis and repair content inside the wider architecturing flow.
- **Boundary:** Use C.32.MLAO only for residual-reducing architecture candidate frames after residual triage. Use the applicable patterns for mathematical-lens adequacy, evidence, assurance, gate passage, ethical mediation, causal claim adequacy, work authorization, and final selection.


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/C-30-ILC#root, spec://ai.lev/fpf-spec/contract/C-32#root, spec://ai.lev/fpf-spec/contract/C-32-ACS#root, spec://ai.lev/fpf-spec/contract/C-32-ACE#root, spec://ai.lev/fpf-spec/contract/C-29#root, spec://ai.lev/fpf-spec/contract/C-31-ASAP#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/C-32-CONWAY#root, spec://ai.lev/fpf-spec/contract/C-32-FAIL#root, spec://ai.lev/fpf-spec/contract/C-32-PAD#root, spec://ai.lev/fpf-spec/contract/C-18#root, spec://ai.lev/fpf-spec/contract/C-19#root, spec://ai.lev/fpf-spec/contract/G-5#root, spec://ai.lev/fpf-spec/contract/C-11#root, spec://ai.lev/fpf-spec/contract/A-10#root, spec://ai.lev/fpf-spec/contract/B-3#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/C-30#root, spec://ai.lev/fpf-spec/contract/C-30-AD#root, spec://ai.lev/fpf-spec/contract/C-30-ILC#root, spec://ai.lev/fpf-spec/contract/C-30-P#root, spec://ai.lev/fpf-spec/contract/C-32#root, spec://ai.lev/fpf-spec/contract/C-32-ACE#root, spec://ai.lev/fpf-spec/contract/C-32-CONWAY#root, spec://ai.lev/fpf-spec/contract/C-32-FAIL#root, spec://ai.lev/fpf-spec/contract/C-32-PAD#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/C-32-MLAO
