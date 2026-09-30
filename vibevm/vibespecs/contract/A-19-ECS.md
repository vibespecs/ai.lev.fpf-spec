# A.19.ECS - Evaluation CharacteristicSpace Construction: Define What Counts as Better {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method pattern
> **Status:** Stable
> **Normativity:** Normative

**Use this pattern when.** Use this pattern when an object version is to be improved or judged, but the evaluation that says what "better" means is not yet available, not yet explicit, or not yet adequate for the object.

## A.19.ECS:1 - Problem frame {#problem-frame}

Use `A.19.ECS` when an object version is to be improved or judged, but the evaluation that says what "better" means is not yet available, not yet explicit, or not yet adequate for the object.

`A.19` says how a `CharacteristicSpace` is structured: declared characteristics, declared scales, slots, value sets, declared coordinate groups, and no hidden normalization or aggregation. `A.19.ECS` says how to make such a `CharacteristicSpace` for the evaluated object, so that an evaluation can later evaluate that object and `E.23` can run an improvement loop without inventing values.

The ordinary output is an evaluation characteristic-space specification: a grouped set of characteristics, scales, value meanings, evidence-basis rules, missingness rules, result-row shape, calibration points, coordinate-specific evidence payloads, protected trade-offs, status meanings, and stop or reopen conditions for one evaluated object kind and use scope.

**Not this pattern when.** If a suitable evaluation already exists, cite it and use `E.22` for question framing or `E.23` for repeated improvement. Use `A.17`, `A.18`, and `C.16` when the live problem is one characteristic, one scale, or measurement admissibility and scale lawfulness. Use `C.16.P` first when candidate coordinate wording still hides whether the use under repair is a characteristic, scale, coordinate, score, metric label, quality-term repair, or subject-pattern relation. Use `A.19` when the live problem is the structure of `CharacteristicSpace` itself. Use `C.25` when the evaluated EntityOfConcern is a composite engineering quality family that already fits Q-Bundle form. Use `F.18` when the live problem is durable naming. Use `E.21`, `E.9.DA`, or `E.2.DA` when the evaluated EntityOfConcern is respectively one FPF pattern version, one `DRR`, or one FPF-level Pillar-adequacy evaluated EntityOfConcern.

**First useful move.** State the sentence: "good as what kind of object, for which use, against which contrast cases?" Then name the evaluated object kind, the use scope, and at least three contrast cases: one admissible evaluated object, one below-floor evaluated object, and one outside-declared-object-kind boundary case that should return to evaluation selection before the evaluation is opened or receive an explicit object-kind-fit defect/value when that evaluation has already been invoked.

**Existing-evaluation boundary.** If the answer is "use this existing evaluation" and the evaluated object kind, use scope, floor, protected trade-offs, and stop meanings are already recoverable, do not construct a new `CharacteristicSpace`.

**What goes wrong if missed.** A team says "improve this" and then chooses convenient scores. A scale set appears from nowhere. Chairs, coal plants, nuclear plants, and FPF patterns all get compared on coordinates that do not distinguish the evaluated object kind. One visible value improves while the intended use gets worse. A review can say "better" but cannot say which object property changed, what trade-off was protected, or why improvement may stop.

**What this buys.** `A.19.ECS` gives improvement work a way to create the missing evaluation before the loop starts. It keeps `E.23` universal and simple: `E.23` changes the object and asks an evaluation to re-evaluate it; `A.19.ECS` helps build that evaluation when none is yet adequate.

**Primary EntityOfConcern in plain terms.** The primary EntityOfConcern is the construction of one evaluation `CharacteristicSpace` for one evaluated object kind and declared use.

**Primary working reader.** The first reader is the engineer, analyst, pattern author, evaluator, steward, or method designer who must define what counts as improvement for an evaluated object before running an improvement loop.

## A.19.ECS:2 - Problem {#problem}

FPF already has named patterns for single characteristics, scales, coordinate values, Q-Bundles, and repeated improvement. The gap is the construction of a useful grouped scale set for an evaluated object kind.

Recurring failures:

1. **Scale set from air.** An evaluation lists coordinates because they are familiar, not because they discriminate the evaluated object kind or use.
2. **Wrong-kind comparison.** Objects outside the declared kind are scored as if they were weak objects under improvement, or are silently skipped, instead of being returned to evaluation selection before opening or handled by an explicit object-kind-fit defect/value after opening.
3. **One-score collapse.** Several independent characteristics are averaged into one score, hiding object-kind-fit defects and trade-offs.
4. **Unstated polarity.** Readers cannot tell which direction is preferred or when a value has no preferred direction.
5. **No floor or exceptional meaning.** Values are recorded, but nobody can say what is viable, exceptional, or still inadmissible for the declared use.
6. **No evidence or missingness rule.** A coordinate value is asserted without saying what observation, content locus, test, example, source, or judgment can justify it, or what absence means.
7. **No protected trade-off.** The evaluation encourages improvement on visible coordinates while damaging safety, usability, affordability, source preservation, entry cost, neighbour fit, or another value that should constrain the change.
8. **No stop or reopen condition.** Improvement continues forever or stops after a convenient checklist closure, not because the evaluation says the evaluated object has reached the declared aim.
9. **Specification underdeclaration.** A new evaluation is mentioned in prose, table, rule, or local rubric, but its declared specification does not make evaluated object kind, coordinate set, value meanings, status meanings, relations, and non-use boundaries recoverable.
10. **Result-form underdeclaration.** The evaluation has coordinates, but the returned result can be a prose impression, a two-column value table, or a checklist count without evidence basis, adjacent-value rationale, calibration discipline, or coordinate-specific payload.
11. **Evidence-basis leakage.** Evidence needed to justify the evaluation result, corpus projection, currentness, retrieval, or parity is written as if it were the evaluated object's own method or user action.

## A.19.ECS:3 - Forces {#forces}

| Force | Tension |
|---|---|
| **evaluated-object-kind discrimination vs broad reuse** | The evaluation must fit the evaluated object kind, but it should reuse existing FPF characteristic and scale discipline where possible. |
| **Small first version vs enough coordinates** | A useful first evaluation can be compact, but it needs enough coordinates to block false improvement and wrong-kind comparison. |
| **Measurement admissibility and scale lawfulness vs ordinal judgment** | Some coordinates are measured through `C.16`; others are evidence-backed ordinal content values. The evaluation must say which is which. |
| **Improvement direction vs trade-off protection** | Preferred movement must be visible without turning every coordinate into an optimization command. |
| **Contrast cases vs overfitting** | Contrast cases are needed to test the scale set, but the evaluation must not become a list of examples only. |
| **Reusable specification vs local use** | A reusable evaluation must make the same evaluation characteristic-space elements recoverable across uses. A local project can use a smaller specification when the use is bounded and non-reusable. |
| **Local stop vs open-ended improvement** | A loop may stop for the declared use while the object and the scale set remain improvable under a new use, source, or comparison concern. |

## A.19.ECS:4 - Solution {#solution}

Construct an evaluation `CharacteristicSpace` by declaring the evaluated object kind, use scope, contrast cases, characteristic slots, scale bindings, value meanings, evidence-basis and missingness rules, result-row shape, calibration points, coordinate-specific evidence payloads, protected trade-offs, status meanings, and stop or reopen conditions.

`EvaluationCharacteristicSpaceSpec := <EvaluatedObjectKindRef, ObjectVersionUnderImprovementRef?, DeclaredUseScope, WorkingReaderScope, QualificationWindow, DiscriminatingCaseSet, ObjectKindFitRule, CharacteristicSlotSet, ScaleBindingSet, PolarityAndPreferredMovement, FloorAndExceptionalMeaningSet, EvaluationEvidenceBasisRule, EvidenceAndMissingnessRule, ResultRowShape, AdjacentValueRationaleRule, CalibrationPointSet, CoordinateSpecificEvidencePayloadRule?, ProtectedTradeoffSet, DominanceOrComparisonRule?, StatusValueSet, StopOrReopenCondition, NeighborPatternExitSet, E22QuestionFrameUse?, E23StartCondition>`

### A.19.ECS:4.1 - Local names and kind settlement {#local-names-and-kind-settlement}

| Local name | Use | Non-use boundary |
|---|---|---|
| `EvaluationCharacteristicSpaceSpec` | Local specification for constructing one evaluation `CharacteristicSpace`. | Not a score sheet, review packet, work plan, gate, evidence record, or project approval. |
| `EvaluatedObjectKindRef` | Exact kind of object the evaluation evaluates. | Not a vague artifact, file bundle, campaign, chat, or source collection. |
| `DeclaredUseScope` | Use for which the evaluated object is being judged or improved. | Not all possible uses. |
| `DiscriminatingCaseSet` | Positive, below-floor, and outside-declared-object-kind boundary cases used to test whether the characteristic space distinguishes the evaluated object kind and use. | Not a substitute for the coordinate set. |
| `ObjectKindFitRule` | Rule for admissible evaluated object, below-floor evaluated object, and outside-declared-object-kind boundary case. | Not permission to omit declared coordinates after an evaluation has been invoked. |
| `CharacteristicSlotSet` | The grouped slots, each binding one characteristic to one scale. | Not an arbitrary checklist and not hidden aggregation. |
| `ScaleBindingSet` | The chosen scale and value meaning for each characteristic slot. | Not a metric dashboard unless a distance or measurement claim is explicitly declared by the neighbour. |
| `PolarityAndPreferredMovement` | Direction of preferred movement for each coordinate, or a statement that the coordinate has no simple preferred direction. | Not permission to optimize one coordinate while damaging protected trade-offs. |
| `FloorAndExceptionalMeaningSet` | Viable-for-use and exceptional-for-use value meanings for declared coordinates. | Not a maturity ladder and not proof that future improvement is impossible. |
| `EvaluationEvidenceBasisRule` | The checked evidence loci required for the result: object version, corpus/projection loci when corpus-facing, source-currentness loci when currentness is valued, comparator loci when parity is valued, worked-case loci when case coverage is valued, and missing or unchecked loci when they affect values. | Not a separate "not evaluated" alternative, not permission to infer values from reputation, review state, or absence of visible defects, and not the evaluated object's own method or user action. |
| `EvidenceAndMissingnessRule` | What justifies a value and how missing, censored, unknown, object-kind-fit, or boundary-return cases are handled. | Not project evidence, assurance, or gate proof by itself. |
| `ResultRowShape` | Required result row fields for the evaluation, including coordinate, value, and a short rationale; some evaluations may add evidence-locus or payload fields. | Not a free-form review paragraph and not a two-column coordinate/value table. |
| `AdjacentValueRationaleRule` | Rule that each result rationale says why the lower adjacent value would understate the evidence and why the higher adjacent value would overstate it, or for the top value what would lower or reopen the claim. | Not verbosity for its own sake. |
| `CalibrationPointSet` | Reusable 3/4/5 or equivalent adjacent-value calibration points for common evaluator disagreements. | Not a second score system and not a shortcut around the declared scale. |
| `CoordinateSpecificEvidencePayloadRule` | Extra payload that a coordinate needs when a category label can fake discharge: comparator plus selected ingredient plus current locus, source plus adopted payload plus currentness window, projection locus plus retrieval cue, or another payload named by value. | Not administrative burden, not the evaluated object's method, and not live evaluated-object text unless the evaluated object itself is an evaluation result or projection carrier. |
| `ProtectedTradeoffSet` | Qualities or neighbour claims that must be checked when visible coordinates improve. | Not a hidden veto without a declared evaluation pattern or value meaning. |
| `PrecisionRepairKindRule` | Rule for checking pre-repair and post-repair evaluated object kind, characteristic kind, relation or claim kind, current ontic slot, relation position, use relation, admissible use, and scope when coordinate or evaluation wording is repaired; when another pattern description contains the defining or constraining content, cite its `subjectPatternLocator` and exact ClaimGraph. | Not a lexical substitution table and not permission to change object kind or slot, relation position, use relation, or claim kind by cleaner wording. |
| `StatusValueSet` | Local admissible-use result values for the evaluation. | Not release state, gate status, or evaluator praise. |
| `E23StartCondition` | Minimum condition for using this evaluation inside `E.23`. | Not the improvement loop itself. |

These names are local to this pattern. They do not mint kernel `U.*` kinds, measurement templates, gate states, evidence kinds, or release states.

### A.19.ECS:4.2 - Construction moves {#construction-moves}

Use these moves when constructing or repairing an evaluation. They are not a mandatory work sequence; each move is a required content question whose answer must be recoverable before the evaluation is used for improvement.

1. **Name the evaluated object kind and use.** Say what object kind is being evaluated and for which declared use. If the evaluated object kind is not recoverable, stop before choosing coordinates.
2. **Build the discriminating cases.** Include at least one evaluated object that should pass, one object of the same general family that should fail the floor, and one different object kind that should return to evaluation selection before opening or receive an explicit object-kind-fit defect/value if this evaluation has already been invoked.
3. **Choose candidate characteristics.** Draw candidates from the object kind's real failure modes, first-principles structure, user or operator harms, domain tradition, current `SoTA`, existing evaluations, and FPF neighbouring patterns named by value.
4. **Bind each slot.** For each candidate, state the characteristic, chosen scale, value set, admissible domain, missingness semantics, and whether the value is a measurement claim or an ordinal content evaluation.
5. **Remove false coordinates.** Drop coordinates that do not change admissible action, do not discriminate the evaluated object, duplicate another coordinate without a different repair action, or belong to another exact evaluation.
6. **Split compound coordinates.** If a coordinate mixes two repair actions, two object kinds, or two incompatible scales, split it or assign one part to the neighboring pattern governing the claim that governs it.
7. **State preferred movement and trade-offs.** For each declared coordinate, state the preferred direction or explain why no simple direction exists. Name the protected trade-offs that must be checked when the coordinate improves.
8. **Define result form, evidence basis, and calibration.** State the required result row shape, evidence basis, adjacent-value rationale rule, calibration points for common disagreements, and any coordinate-specific payload needed for high or floor-reaching values.
9. **Define floor, exceptional, status, and stop.** State the viable-for-use floor, exceptional-for-use meaning, status values, and local stop or reopen condition.
10. **Record subject assertions and their rule loci.** When the coordinate depends on evidence, assurance, gate, work, decision, publication, naming, quality-bundle, measurement, OEE/NQD, or mathematical-lens content, name the exact subject, relation function, defining or constraining ClaimGraph, and subject assertion. A `subjectPatternLocator` may help find that ClaimGraph but asserts no governance relation; do not rewrite the dependency as routing or package-placement prose.
11. **Start `E.23` only after evaluation values exist.** A repeated improvement loop can start only when the evaluated object version, evidence basis, result form, and evaluation are recoverable enough for re-evaluation.

### A.19.ECS:4.3 - Evaluation specification minimum {#evaluation-specification-minimum}

A.19.ECS does not prescribe a publication or record form. It states which evaluation characteristic-space elements must be recoverable before an evaluation characteristic space is reusable for judgement or improvement. The selected publication or record form may be an FPF pattern, local engineering standard, rubric, table, review form, model card section, protocol note, or project rule, but that form is not governed here. The evaluation characteristic-space specification must make these items recoverable by value:

| Specification item | Required content |
|---|---|
| `Evaluation problem frame` | Evaluated object kind, declared use, first useful move, existing-evaluation boundary, and what goes wrong if no evaluation exists. |
| `Non-use boundary` | Boundaries to single-characteristic, measurement, Q-Bundle, naming, evidence, assurance, gate, work, decision, publication, and loop-method patterns. |
| `Local names and kind settlement` | Local field names, use named by values, and non-use boundaries. |
| `Evaluation record shape` | The local record or bundle shape used by the evaluation. |
| `Object-kind fit rule` | Admissible evaluated object, below-floor evaluated object, and outside-declared-object-kind boundary handling before and after invocation. |
| `Evaluation evidence basis` | Loci named by value that must be checked or named when a value depends on object version, corpus projection, source currentness, mature comparator, worked case, retrieval, or other external evidence. |
| `Result-row shape` | Required result row fields, at minimum coordinate, value, and short rationale; any required evidence-locus or coordinate-specific payload fields are declared here. |
| `Coordinate set` | Coordinate heads, properties of the evaluated object, evaluated-object properties and use conditions, scale/value meanings, evidence loci, and protected trade-offs. |
| `Calibration and payload rules` | Adjacent-value calibration points and coordinate-specific payloads that prevent impressionistic `3`/`4`/`5` assignment or category-list discharge. |
| `Status and stop condition` | Admissible-use statuses, local stop meanings, and reopen conditions. |
| `Worked slices` | At least one passing evaluated object, one below-floor evaluated object, and one outside-declared-object-kind boundary case. |
| `Common anti-patterns` | The false interpretations or values the evaluation must block. |
| `Neighbouring-pattern claim assignment` | Neighbouring FPF patterns named by value and the claims being made that each pattern defines or constrains. |

This minimum is a content requirement, not a file-format requirement. For an FPF pattern publication form, `E.8` still governs the authoring form. `A.19.ECS` only states what the evaluation must make recoverable so that `E.22` can frame an improvement-oriented quality evaluation and `E.23` can run a repeated improvement loop.

When construction or repair changes coordinate wording or evaluation wording, the evaluation characteristic-space specification records `PrecisionRepairKindRule` or an equivalent result-row requirement. The check compares the pre-repair and post-repair evaluated object kind, characteristic kind, relation or claim kind, current ontic slot, relation position, use relation, admissible use, and scope; when another pattern description contains the relevant definition or constraint, it cites that exact ClaimGraph and may add a non-semantic subject-pattern locator. A cleaner phrase that changes those items, treats a coordinate position as an object kind, or loses the value's slot, relation position, use relation, or claim kind is a changed evaluation decision, not a wording repair.

### A.19.ECS:4.4 - Discriminating-case test {#discriminating-case-test}

An evaluation is not ready if it cannot distinguish these three outcomes:

1. **Admissible evaluated object.** The object is of the evaluated object kind and can meet or exceed the floor under the declared use.
2. **Below-floor evaluated object.** The object is of the evaluated object kind or a declared comparable family, but fails one or more floors.
3. **Outside-declared-object-kind boundary case.** Before the evaluation is opened, the object should return to evaluation selection or construction rather than be treated as the evaluated object kind. If the evaluation has already been invoked for that object, the result is an explicit object-kind-fit defect/value or repair status, not omitted coordinates.

Example: for a nuclear-plant adequacy evaluation, a nuclear plant can vary along safety, output, maintenance, regulatory, thermal, waste-handling, grid, and resilience coordinates. A coal plant may be a power-generation alternative only when the declared use explicitly compares power-generation options across plant kinds. A chair or FPF pattern is outside the nuclear-plant evaluated-object kind: before opening the evaluation it returns to a suitable evaluation; after a forced invocation, the record shows an object-kind-fit defect/value rather than pretending the chair has weak nuclear-plant quality or silently skipping coordinates.
### A.19.ECS:4.5 - Scale-set improvement {#scale-set-improvement}

The evaluation characteristic space itself can be improved. In that case, the evaluated object is the current `EvaluationCharacteristicSpaceSpec` version, not the original evaluated object.

Use `E.23` for the repeated improvement method over the scale set when the improvement aim is live. The evaluation for that meta-level improvement may be:

- this pattern's conformance checklist for whether the scale set is constructible and usable;
- `E.21` when the evaluation characteristic-space specification is itself an FPF pattern version;
- `E.9.DA` when the decision record selecting the scale set is the `DRR` decision-adequacy object being evaluated;
- `E.2.DA` when the scale set changes FPF-level Pillar adequacy;
- `F.18` when the live problem is name choice for the scale-set heads;
- `C.16`, `A.17`, `A.18`, or `A.19` when the live problem is measurement admissibility, scale lawfulness, or characteristic-space admissibility.

Do not improve an evaluated object by silently changing its evaluation. If the evaluation changes, the loop record names the changed evaluation version and states whether earlier object-version values remain comparable, need a bridge, or must be retired for the new use.

## A.19.ECS:6 - Conformance checklist {#conformance-checklist}

| Check | Requirement | Why |
|---|---|---|
| `CC-A19ECS-1` | @fact:CC-A19ECS-1 An evaluation characteristic-space specification SHALL name evaluated object kind, use scope, reader scope, and qualification window. @status:spec/done | Prevents context-free quality claims. |
| `CC-A19ECS-2` | @fact:CC-A19ECS-2 It SHALL include admissible, below-floor, and outside-declared-object-kind boundary contrast cases. @status:spec/done | Tests evaluated-object-kind discrimination. |
| `CC-A19ECS-3` | @fact:CC-A19ECS-3 Each coordinate SHALL bind one characteristic to one scale, including for an ordinal content evaluation. State separately whether the value is a measurement claim or a content evaluation. @status:spec/done | Preserves A.17/A.18/C.16/A.19 discipline. |
| `CC-A19ECS-4` | @fact:CC-A19ECS-4 Each coordinate SHALL state value meanings, polarity or no-simple-direction value rule, evidence rule, and missingness rule. @status:spec/done | Makes values replayable. |
| `CC-A19ECS-5` | @fact:CC-A19ECS-5 The specification SHALL state floor, exceptional, status, stop, and reopen meanings for the declared use. @status:spec/done | Lets improvement stop locally without claiming final perfection. |
| `CC-A19ECS-6` | @fact:CC-A19ECS-6 Protected trade-offs SHALL be named when improving visible coordinates can harm another live value. @status:spec/done | Blocks Goodhart-style improvement. |
| `CC-A19ECS-7` | @fact:CC-A19ECS-7 The specification SHALL not average ordinal coordinates or turn undeclared coordinates into hidden pass, waiver, or failure. @status:spec/done | Preserves non-scalar comparison. |
| `CC-A19ECS-8` | @fact:CC-A19ECS-8 Wrong-kind objects SHALL return to evaluation selection before opening, or receive an explicit object-kind-fit defect/value when the evaluation has already been invoked. @status:spec/done | Keeps the declared coordinate table complete after invocation and prevents false low scores before the suitable evaluation is selected. |
| `CC-A19ECS-9` | @fact:CC-A19ECS-9 If made reusable beyond one local use, the evaluation characteristic-space specification SHALL make the minimum items in `A.19.ECS:4.3` recoverable by value. If the selected publication form is an FPF pattern, `E.8` also applies to that publication form. @status:spec/done | Prevents underspecified evaluations. |
| `CC-A19ECS-10` | @fact:CC-A19ECS-10 If the evaluation itself changes during improvement, the loop record SHALL name the changed evaluation version and the comparability effect on earlier object-version evaluations. @status:spec/done | Prevents silent value drift. |
| `CC-A19ECS-11` | @fact:CC-A19ECS-11 The evaluation characteristic-space specification SHALL state any evidence, assurance, gate, work, decision, publication, naming, measurement, Q-Bundle, OEE/NQD, mathematical-lens, or related claim as an exact subject assertion or named relation by value when that claim is being made. The coordinate Solution carries the evaluation construction itself; a subject-pattern locator, reference boilerplate, architecture-placement rationale, and neighboring content stay in relations, rationale, source-basis, or decision-rationale material unless they change a coordinate. @status:spec/done | Prevents an evaluation from becoming a second ontology or reference boilerplate. |
| `CC-A19ECS-12` | @fact:CC-A19ECS-12 A reusable evaluation characteristic-space specification SHALL state what would lower, reopen, or retire the evaluation: missing contrast case, changed use, changed source-use relation or source-currentness status, hidden trade-off loss, or corrected neighbouring-pattern claim assignment. @status:spec/done | Makes high-value evaluation claims falsifiable instead of permanent praise. |
| `CC-A19ECS-13` | @fact:CC-A19ECS-13 A reusable evaluation characteristic-space specification SHALL define the result-row shape and require a short rationale for every coordinate value. @status:spec/done | Prevents prose impressions and two-column tables from being mistaken for evaluation results. |
| `CC-A19ECS-14` | @fact:CC-A19ECS-14 It SHALL define the evaluation evidence basis and any coordinate-specific evidence payload needed for source-currentness, comparator, corpus-projection, worked-case, retrieval, or external-currentness claims. Apply the declared missingness rule when evidence is missing or unchecked. Lower a value for that absence only when the coordinate's value rule evaluates evidence adequacy or otherwise makes that absence a lower value; do not infer a low property value merely from an unknown value. @status:spec/done | Makes values replayable while preserving missingness and the declared coordinate coverage. |
| `CC-A19ECS-15` | @fact:CC-A19ECS-15 It SHALL publish calibration points for common adjacent-value disagreements whenever the evaluation is expected to be reused by different evaluators. @status:spec/done | Keeps `3`, `4`, and `5` from drifting into evaluator temperament. |
| `CC-A19ECS-16` | @fact:CC-A19ECS-16 It SHALL declare where result evidence, corpus-projection evidence, retrieval evidence, comparator evidence, currentness evidence, and quality-status evidence live. These payloads SHALL stay in the evaluation result, evidence basis, projection carrier, or selected publication carrier unless the evaluated object itself is that carrier. If the payload implies a user-facing action for another evaluated object, publish that move or boundary, not the carrier proof. This is an evaluation-payload placement rule, not a lexical ban: evidence-use payloads do not enter live evaluated-object text merely because they are true or useful to authors or evaluators. @status:spec/done | Prevents evaluation evidence from leaking into the evaluated object's method or live text. |
| `CC-A19ECS-17` | @fact:CC-A19ECS-17 If construction or repair changes coordinate wording or evaluation wording, the specification SHALL require a pre/post kind-restoration check for evaluated object kind, characteristic kind, relation or claim kind, current ontic slot, relation position, use relation, admissible use, and scope, plus the exact defining or constraining ClaimGraph when another pattern description contains it. @status:spec/done | Prevents coordinate cleanup from changing what the evaluation evaluates. |

## A.19.ECS:8 - Consequences {#consequences}

A conforming `A.19.ECS` result lets `E.22` ask a useful improvement-oriented quality-evaluation question and lets `E.23` run a repeated improvement loop without inventing values during the loop. It also gives object-specific evaluation patterns such as `E.21`, `E.9.DA`, `E.2.DA`, and `F.18` a common construction shape: evaluated object kind, use, contrast cases, coordinates, value meanings, evidence basis, result-row shape, calibration points, coordinate-specific payloads, protected trade-offs, status meanings, and local stop or reopen condition.

The cost is intentional. A reusable evaluation is heavier than a local checklist, because it must prevent wrong-kind use, hidden value drift, proxy-for-value substitution, neighbour theft, and false stop claims. When a local rubric is enough, keep the rubric local. When reuse is needed, carry the evaluation by value.

## A.19.ECS:11 - Relations {#relations}

| Pattern | Relation |
|---|---|
| `A.19` | Defines `CharacteristicSpace`. `A.19.ECS` gives the method for constructing one evaluation `CharacteristicSpace` for an evaluated object. |
| `A.17`, `A.18`, `C.16` | Govern characteristics, scales, scale values, coordinates, measures, units, measurement admissibility, and scale lawfulness. `A.19.ECS` uses them by reference for each slot. |
| `C.25` | Governs Q-Bundle normal form for composite engineering quality families. `A.19.ECS` may select or repair the characteristic-space part before a Q-Bundle endpoint is used. |
| `E.22` | Frames one improvement-oriented quality-evaluation question after an evaluation is declared. `A.19.ECS` constructs the missing or inadequate evaluation. |
| `E.23` | Governs repeated improvement after evaluated object version and evaluation are declared. `A.19.ECS` provides the evaluation when it is missing or underdesigned. |
| `E.21` | Existing evaluation for one FPF pattern version. `A.19.ECS` explains the construction shape but does not replace `E.21`. |
| `E.9.DA` | Existing evaluation for one `DRR` decision-adequacy claim. `A.19.ECS` does not replace it. |
| `E.2.DA` | Existing evaluation for FPF-level Pillar adequacy. `A.19.ECS` explains why it must publish evaluated object, coordinates, values, evidence loci, status, and stop meanings. |
| `F.18` | Existing naming discipline with a grouped lexical quality vector. Use `F.18` for durable term and name improvement. |
| `C.16.P`, `C.16.Q`, `E.10`, `A.6.P`, `C.2.P` | Repair overloaded characteristic/scale/score, quality, lexical, relation, and source-use wording before it becomes a coordinate or status value. |
| `C.18`, `C.19`, `G.5`, `G.9`, `G.11` | Govern OEE/NQD novelty, diversity, archive, pool, selected-set, parity, and refresh semantics. An evaluation may supply `Q` values, but it does not govern the rest of OEE/NQD. |
| `C.29` | Governs mathematical-lens use when a mathematical structure is used to define or justify coordinates. |
| `A.10`, `B.3`, `A.20`, `A.21`, `A.15` | Govern evidence, assurance, local CV, gates, and work when an evaluation result is reused for those claims. |


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: A.17-A.19, spec://ai.lev/fpf-spec/contract/C-16#root, spec://ai.lev/fpf-spec/contract/F-18#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/E-22#root, spec://ai.lev/fpf-spec/contract/E-23#root, spec://ai.lev/fpf-spec/contract/C-25#root, spec://ai.lev/fpf-spec/contract/E-21#root, spec://ai.lev/fpf-spec/contract/E-9-DA#root, spec://ai.lev/fpf-spec/contract/E-2-DA#root, spec://ai.lev/fpf-spec/contract/E-8-ECSPF#root, spec://ai.lev/fpf-spec/contract/F-19#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/C-16-P#root, spec://ai.lev/fpf-spec/contract/C-17#root, spec://ai.lev/fpf-spec/contract/E-2-DA#root, spec://ai.lev/fpf-spec/contract/E-21#root, spec://ai.lev/fpf-spec/contract/E-22#root, spec://ai.lev/fpf-spec/contract/E-23#root, spec://ai.lev/fpf-spec/contract/E-24-CD#root, spec://ai.lev/fpf-spec/contract/E-4-DPF-DA#root, spec://ai.lev/fpf-spec/contract/E-8-ECSPF#root, spec://ai.lev/fpf-spec/contract/E-9-DA#root, spec://ai.lev/fpf-eng-hcd/contract/HCD-18#root, spec://ai.lev/fpf-eng-mdpe/contract/MDPE-12#root, spec://ai.lev/fpf-nstd/contract/NSTD-6#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/A-19-ECS
