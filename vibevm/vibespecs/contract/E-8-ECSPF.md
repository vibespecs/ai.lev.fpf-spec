# E.8.ECSPF - Author an FPF Pattern from an Accepted Evaluation CharacteristicSpace Specification {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Authoring method pattern
> **Status:** Stable
> **Normativity:** Normative

## E.8.ECSPF:1 - Problem frame {#problem-frame}

Use this pattern when an accepted `EvaluationCharacteristicSpaceSpec` constructed or repaired under `A.19.ECS` has been selected for durable FPF publication, and an author must turn it into a practitioner-facing pattern. The question is not "what values should this object be judged by?" but "how should the pattern teach this evaluation so its values remain usable, reviewable, and bounded?"

`A.19.ECS` guides an author in constructing or repairing the evaluation characteristic-space specification: evaluated object kind and, when needed, the object version; declared use, working reader, qualification window, contrast cases, object-kind-fit rule, coordinate and scale bindings, value meanings and preferred movement, evidence and missingness rules, result-row shape, adjacent-value rationales, calibration points, any triggered coordinate payload, protected trade-offs, any declared comparison rule, status meanings, neighbouring-pattern exits, and stop, reopen, `E.22`, and `E.23` conditions. `E.8` supplies the ordinary FPF authoring form. `E.8.ECSPF` tells the author how to carry the accepted specification into that form. The specification, its `CharacteristicSpace`, the authored pattern content, a later evaluation of an object, and the result of that evaluation remain different things.

**Not this pattern when.** Use `A.19.ECS` when the characteristic-space specification itself is missing or inadequate. Use `E.8` when the pattern is not an evaluation-characteristic-space pattern. Use `E.21`, `E.9.DA`, `E.2.DA`, `F.18`, `C.25`, or a project-local evaluation when one already supplies the value meanings for the evaluated object and use. Use `E.22` to frame one quality evaluation and `E.23` to run repeated improvement. Use a local rubric, table, or project rule instead of an FPF pattern when the evaluation is not intended for durable FPF reuse.

**First useful move.** Start from the accepted `A.19.ECS` specification. Before presenting coordinate tables or conformance rows, name the evaluated object kind, declared use, working reader, qualification window, and first action-guiding evaluation use in the pattern's recognition text.

**FPF-publication boundary.** If the evaluation is local, temporary, or project-specific, do not publish an FPF pattern. Keep the `A.19.ECS` specification in the local publication form and cite the FPF neighbouring patterns named by value it uses.

**What goes wrong if missed.** The pattern, the accepted specification, the evaluation, and its result collapse into one supposed object. The pattern then becomes a score sheet, review form, checklist, or taxonomy. The coordinate table appears before the working situation. Readers can see values but cannot tell when to use them, what to do after an evaluation result, which objects are outside the declared evaluated-object kind, or which neighbouring pattern supplies the needed evidence, assurance, gate, work, decision, naming, measurement, or improvement guidance.

**What this buys.** `E.8.ECSPF` lets an author publish evaluation guidance as a real pattern: practitioner-readable first, exact enough for review, and bounded enough for a later evaluator to use with the framing guidance in `E.22` or the repeated-improvement guidance in `E.23`.

**Primary EntityOfConcern in plain terms.** The primary EntityOfConcern is the authored FPF pattern content and its publication form for one accepted evaluation characteristic-space specification.

**Primary working reader.** The first reader is an FPF author or reviewer turning an accepted evaluation characteristic-space specification into a reusable FPF pattern for later practitioners, managers, and stewards.

## E.8.ECSPF:2 - Problem {#problem}

An author can use `A.19.ECS` to produce a good evaluation characteristic-space specification without yet having guidance on publishing that specification as an FPF pattern. The author can use `E.8` to produce a good generic FPF pattern without yet having guidance on where to place a coordinate set, object-kind-fit rule, evidence basis, result-row shape, calibration points, status set, and stop condition when they are the pattern's main content.

Recurring failures:

1. **Publication-form/content collapse.** The accepted specification, its `CharacteristicSpace`, the authored pattern, a later evaluation, and the evaluation result are treated as one object.
2. **Table-first pattern.** Coordinate rows arrive before evaluated object kind, use, first move, FPF-publication boundary, and object-kind boundary.
3. **Checklist substitution.** Conformance rows replace the `Solution` instead of checking a readable evaluation method.
4. **Underpublished values.** Coordinate names are present, but reader or qualification limits, value meanings, missingness, polarity, protected trade-offs, comparison rule, status meanings, neighbouring exits, or stop and reopen conditions are missing.
5. **Wrong-kind examples.** Worked cases show only passing examples, so the pattern cannot teach below-floor and outside-declared-object-kind boundary outcomes.
6. **Neighbour theft.** Claims about evidence, assurance, gates, work, decisions, naming, measurement, OEE or NQD, or mathematical lenses are carried as if this evaluation-characteristic-space pattern defined or justified them.
7. **Pattern-quality confusion.** The author uses `E.21` to judge whether the FPF pattern version is good, but forgets that the new pattern must still carry the accepted evaluation characteristic-space specification for one evaluated object kind by value.
8. **Quality-carrier leakage.** `E.21` values, corpus projection, README/ToC/E.11/I.2 alignment, retrieval, cold-reader evidence, monolith parity, landing evidence, or developer/reviewer/executor correspondence for the publication form are written into the evaluation pattern as if they were the evaluated object's method.

## E.8.ECSPF:3 - Forces {#forces}

| Force | Tension |
|---|---|
| **Recognition first vs coordinate completeness** | An evaluation-characteristic-space pattern needs tables, but the reader must first see the working situation and first evaluation use. |
| **Generic E.8 form vs evaluation content** | The canonical pattern skeleton stays fixed, but the evaluation has special content fields from `A.19.ECS`. |
| **Reusable FPF pattern vs local evaluation** | FPF publication is useful only when the evaluation is durable and reusable beyond one local project. |
| **Values named by value vs checklist feel** | Values and statuses must be named by value without making the pattern feel like an administrative form. |
| **Related-pattern statements vs second ontology** | For each outside claim, the pattern must state the concrete contribution it uses from neighbouring content, without forcing every contribution into one verb list or becoming a directory of possibly related patterns. |
| **Evaluation of object vs evaluation of FPF pattern version** | The evaluation judges its evaluated object; `E.21` may separately evaluate whether the authored FPF pattern publication form is good enough. |

## E.8.ECSPF:4 - Solution {#solution}

When an accepted `A.19.ECS` specification is selected for durable FPF publication, use `E.8` to write a pattern that teaches the specified evaluation, with these additional placement rules:

1. **Keep the objects separate.** The accepted specification says what the evaluation requires. The publication form arranges the pattern. The authored content teaches a later practitioner how to evaluate an object. That later evaluation produces a result. Neither the specification nor its `CharacteristicSpace`, the evaluation, the evaluated object, or the result becomes the pattern.
2. **Put recognition before coordinates.** The opening text names evaluated object kind, declared use, working reader, qualification window, first evaluation use, FPF-publication boundary, what goes wrong, and what the pattern buys before any dense table.
3. **Carry the complete accepted specification by value.** Put every required value, and every optional value whose trigger holds, where a practitioner needs it. Do not discharge this move by citing `A.19.ECS`, copying field names, or pointing to an author-only record. The `Solution` and its nearby practitioner-use sections carry the actual selected values from the accepted specification.
4. **Use worked slices as the discriminating-case test.** Archetypal Grounding and worked cases include a passing evaluated object, a below-floor evaluated object, and an outside-declared-object-kind boundary case.
5. **Keep ordinal coordinates separate and protect against proxy improvement.** Do not create an undeclared total, average, or “overall score” from ordinal coordinates. Whenever a visible value improves, ask whether any intended value or protected trade-off became worse. If the published guidance would reward that loss, stop the comparison and reopen the specification. If a bounded use genuinely needs scalarization, name the particular method, its use, any information loss, and its applicability and stop or return conditions; do not present that scalar as “the evaluation”.
6. **Keep checklist rows secondary.** Conformance checks verify that the evaluation is recoverable and usable. They do not become the user's method.
7. **State the concrete contribution used for each outside claim.** When `Relations` or a grounded local boundary makes a claim about, for example, evidence, assurance, work, naming, measurement, or improvement, cite the applicable `PatternID` and say in ordinary terms what its content contributes here. It may supply an evidence-use boundary, an assurance calculus, a gate decision rule, a measurement test, repair guidance, or something else; these are examples, not a closed vocabulary. The `PatternID` is enough for ordinary use. Name a particular assertion, episteme edition, or `ClaimGraph` only when interpretation, migration, conflict, publication, or reuse depends on that identity. Treat guidance as a `U.Method`, a qualifying `U.MethodDescription`, or a particular Method use only after its own admission test passes and the current claim needs that identity. Use `F.19` for ordinary wording repair. When a repair can change an FPF-governed meaning, confirm that the evaluated object and its kind, relation or claim kind, live ontic slot, relation position, use relation, admissible use, and scope remain recoverable before and after the repair, as applicable to the changed claim.
8. **Evaluate the authored pattern with `E.21`.** When the FPF pattern is under quality improvement, a reviewer uses `E.21` to evaluate that pattern version. A later evaluator uses the guidance published in the pattern to evaluate the declared object kind. The `E.21` result, corpus-projection evidence, README/ToC/E.11/I.2 alignment, retrieval or cold-reader evidence, monolith parity, landing evidence, and developer/reviewer/executor correspondence stay in the quality, review, projection, or release carriers unless the pattern's own `EntityOfConcern` and user-facing action are that evaluation or projection work.

The authoring flow and the quality-improvement flow are different. First an author carries an accepted specification into a pattern. Later a practitioner may use that pattern's guidance to evaluate an object and record a result. `E.22` and `E.23` provide guidance for framing or repeating that work. A reviewer's later `E.21` evaluation of this pattern is evidence about the authored pattern, not part of the object evaluation that the pattern teaches. That evidence may cause edits to recognition text, coordinates, cases, or boundaries, but it remains outside the pattern unless rewritten as user-facing evaluation guidance.

### E.8.ECSPF:4.1 - Canonical placement table {#canonical-placement-table}

| E.8 section | Evaluation-specific content |
|---|---|
| `Problem frame` | Evaluated object kind, declared use, working reader, qualification window, first useful evaluation use, FPF-publication boundary, what goes wrong without this evaluation, and what practical move the evaluation enables. |
| `Problem` | Failure modes that the evaluation prevents: wrong-kind scoring, hidden value drift, proxy value, one-score collapse, missingness confusion, or neighbour theft. |
| `Forces` | Tensions among reuse, coordinate count, readability, measurement admissibility, trade-off protection, local stop, and open-ended improvement. |
| `Solution` | Every required accepted-specification value and every triggered optional value: object and use, reader and qualification limits, cases and kind-fit, coordinate and scale bindings, value meanings and preferred movement, evidence and missingness, result form and calibration, coordinate-specific evidence, trade-offs and comparison, statuses, exits, and stop or reopen conditions. |
| `Archetypal Grounding` | At least one passing evaluated object, one below-floor evaluated object, and one outside-declared-object-kind boundary case. |
| `Bias-Annotation` | Known skew in source examples, reader family, domain tradition, measurement preference, benchmark preference, or FPF-internal reuse. |
| `Conformance Checklist` | Checks that the specification is recoverable, not that a reviewer likes the evaluated object. |
| `Common Anti-Patterns` | Score-sheet pattern, checklist-as-solution, table-first recognition failure, neighbour theft, one total score, hidden value drift. |
| `Consequences` | What changes in practice after a conforming evaluation use, its scope, next action, stop or reopen, and the concrete contribution supplied by neighbouring content for any outside claim. Add a denied consequence only when a plausible intended reader has an independent reason to infer it. |
| `Rationale` | Why this coordinate set and publication-form are selected, including relation to `A.19.ECS` and existing evaluations named by value. |
| `SoTA-Echoing` | Current practice that changes evaluated-object selection, coordinate choice, value meaning, missingness, comparison, or stop discipline. |
| `Relations` | `A.19.ECS`, `E.8`, `E.21`, `E.22`, `E.23`, and exact domain or neighbour patterns. |

### E.8.ECSPF:4.2 - Local names and kind settlement {#local-names-and-kind-settlement}

| Local name | Function | Non-use boundary |
|---|---|---|
| `AcceptedEvaluationCharacteristicSpaceSpec` | The accepted `A.19.ECS` specification selected for publication. | Not the pattern, the later evaluation, or its result. |
| `EvaluationPatternPublicationForm` | The `E.8` arrangement used to publish the guidance as an FPF pattern. | Not the accepted specification or the authored words, tables, and cases. |
| `AuthoredEvaluationPatternContent` | The recognition text, solution, value meanings, cases, result form, and boundaries through which the pattern teaches the evaluation. | Not an occurrence of evaluation work and not its result. |
| `LaterEvaluationUse` | A later practitioner judges an object using the published guidance and records a result. | Establish a particular `MethodDescription`, `Method`, assignment, or dated `Work` only when that identity matters to the receiving claim. |
| `EvaluationResult` | The coordinate rows, evidence, rationales, and status produced by that later evaluation. | Not the pattern and not the accepted specification. |
| `RecognitionEvaluationUseLine` | Early line saying what object is evaluated, for which use, and what the first admissible evaluation use does. | Not a slogan or pattern-title paraphrase. |
| `DiscriminatingCaseBank` | Passing, below-floor, and outside-declared-object-kind boundary worked slices. | Not only positive examples. |
| `RelatedPatternRelationBlock` | Statements of outside claims, each with the applicable pattern id and its concrete contribution in this use. | Not a general directory, a closed relation-verb vocabulary, or a list of presumed Methods. |
| `EvaluationResultFormBlock` | Published result-form discipline for this evaluation: required row fields, evidence basis, short rationale rule, and any coordinate-specific payload. | Not a review report, project status, or optional appendix. |
| `CalibrationAndPayloadBlock` | Published adjacent-value calibration points and payload rules for values that need comparator, source-currentness, corpus-projection, worked-case, or retrieval evidence. | Not extra bureaucracy and not a second score system. |
| `PatternVersionQualityEvaluation` | Optional `E.21` evaluation over the authored pattern publication form. | Not a replacement for the evaluation for one evaluated object kind and not publication-form method content. |

### E.8.ECSPF:4.3 - By-value carry-through {#by-value-carry-through}

Carry the accepted specification through the pattern in practitioner order. “By value” means that the reader can find the actual selected value and use it; a field name, an `A.19.ECS` citation, or an author-only attachment is not enough.

| Practitioner need | Accepted values that must be present |
|---|---|
| Recognize whether to enter | `EvaluatedObjectKindRef`, `DeclaredUseScope`, `WorkingReaderScope`, `QualificationWindow`, and `ObjectVersionUnderImprovementRef` when the evaluation is tied to one object version. |
| Test the boundary | `DiscriminatingCaseSet` and `ObjectKindFitRule`, including admissible, below-floor, and outside-kind outcomes. |
| Judge the object | `CharacteristicSlotSet`, `ScaleBindingSet`, `PolarityAndPreferredMovement`, and `FloorAndExceptionalMeaningSet`, with the actual coordinate and value meanings rather than their field labels. |
| Justify and record a result | `EvaluationEvidenceBasisRule`, `EvidenceAndMissingnessRule`, `ResultRowShape`, `AdjacentValueRationaleRule`, `CalibrationPointSet`, and `CoordinateSpecificEvidencePayloadRule` whenever a coordinate triggers such a payload. |
| Protect a useful result from false improvement | `ProtectedTradeoffSet` and `DominanceOrComparisonRule` whenever the accepted specification declares a comparison rule. |
| Continue, stop, or leave this evaluation | `StatusValueSet`, `StopOrReopenCondition`, `NeighborPatternExitSet`, `E22QuestionFrameUse` when selected, and `E23StartCondition`. |

The fields may be expressed in plain language, tables, or worked cases. Keep them close to the practitioner action they qualify. Do not hide required values in conformance rows, source notes, or review evidence.

## E.8.ECSPF:7 - Conformance Checklist {#conformance-checklist}

| Check | Requirement | Why |
|---|---|---|
| `CC-E8ECSPF-1` | @fact:CC-E8ECSPF-1 The pattern SHALL carry every required value from the accepted `EvaluationCharacteristicSpaceSpec` and every optional value whose trigger holds, including reader scope, qualification window, neighbouring exits, and the applicable `E.22` and `E.23` conditions. A citation or field-name list alone does not satisfy this requirement. @status:spec/done | Prevents loss between the accepted specification and practitioner-facing content. |
| `CC-E8ECSPF-2` | @fact:CC-E8ECSPF-2 Recognition text SHALL state evaluated object kind, declared use, working reader, qualification window, first evaluation use, FPF-publication boundary, and object-kind boundary before dense coordinate tables. @status:spec/done | Keeps the pattern usable before it becomes reviewable. |
| `CC-E8ECSPF-3` | @fact:CC-E8ECSPF-3 The `Solution` SHALL carry the accepted specification's values rather than leaving them only in conformance rows, SoTA rows, or examples. @status:spec/done | Prevents checklist substitution. |
| `CC-E8ECSPF-4` | @fact:CC-E8ECSPF-4 Worked cases SHALL include passing, below-floor, and outside-declared-object-kind boundary outcomes. @status:spec/done | Tests evaluated-object-kind discrimination. |
| `CC-E8ECSPF-5` | @fact:CC-E8ECSPF-5 Each coordinate SHALL state value meanings, polarity or no-simple-direction value rule, missingness rule, and protected trade-off when applicable to the declared evaluation use. @status:spec/done | Makes evaluation uses repeatable and bounded. |
| `CC-E8ECSPF-5a` | @fact:CC-E8ECSPF-5a The publication form SHALL prohibit an undeclared total or average over ordinal coordinates. Any admitted scalarization SHALL name its method, declared use, any information loss, applicability, and stop or return condition. @status:spec/done | Prevents a convenient number from replacing the evaluation. |
| `CC-E8ECSPF-5b` | @fact:CC-E8ECSPF-5b When one visible value improves, the evaluation use SHALL check whether an intended value or protected trade-off worsened and SHALL stop or reopen when the evaluation would reward that loss. @status:spec/done | Blocks proxy improvement and Goodhart-style degradation. |
| `CC-E8ECSPF-6` | @fact:CC-E8ECSPF-6 When the publication form makes an outside claim, `Relations` SHALL cite the applicable `PatternID` and state its concrete contribution in ordinary language. The contribution is not limited to a fixed verb list. A pattern citation SHALL NOT be retyped as a Method or MethodDescription. Simple relations stay free of phrase apparatus; retain use-changing architectural reasons under `E.8:4.2.3` and keep current development correspondence outside the pattern. @status:spec/done | Prevents a second ontology or apparatus-overwrapped publication form. |
| `CC-E8ECSPF-6a` | @fact:CC-E8ECSPF-6a Wording, naming, or precision-restoration repairs SHALL follow `F.19`. When a repair can change an FPF-governed meaning, it SHALL check the evaluated object and its kind, relation or claim kind, live ontic slot, relation position, use relation, admissible use, and scope before and after the repair, as applicable to the changed claim. For a claim outside this pattern, cite the applicable pattern id and state its concrete contribution. Require a particular assertion, episteme edition, `ClaimGraph`, `U.Method`, qualifying `U.MethodDescription`, or Method use only when its admission test passes and the receiving claim depends on that identity. @status:spec/done | Prevents evaluation patterns from inheriting lexical cleanup as ontology drift or locator use as formal identity. |
| `CC-E8ECSPF-7` | @fact:CC-E8ECSPF-7 If the authored publication form is under improvement, a reviewer SHALL use `E.21` to evaluate FPF pattern-version quality separately from the evaluation's evaluated object result. @status:spec/done | Keeps pattern quality distinct from evaluated object quality. |
| `CC-E8ECSPF-8` | @fact:CC-E8ECSPF-8 An author SHALL not turn a local, temporary, or one-project evaluation specification into an FPF pattern unless its reuse scope is durable and the patterns used for outside claims are named with their concrete contributions. @status:spec/done | Blocks needless pattern growth. |
| `CC-E8ECSPF-9` | @fact:CC-E8ECSPF-9 The publication form SHALL state what would lower, reopen, or retire the accepted specification or the guidance that carries it: changed object kind or object version, changed use, reader, or qualification window, changed use of a cited source, changed source adoption, adaptation, or rejection decision, missing contrast case, coordinate-value drift, missingness or comparison-rule change, or a correction to an exit or outside claim. @status:spec/done | Makes maintenance of the pattern testable. |
| `CC-E8ECSPF-10` | @fact:CC-E8ECSPF-10 The publication form SHALL state the required result row shape and evidence basis. When a value needs external, comparator, projection, worked-case or currentness evidence, carry that basis and apply the accepted specification's missingness rule. Lower a value for absent or unchecked evidence only when that coordinate's value rule makes the absence a lower value. @status:spec/done | Preserves evidence-dependent values and missingness without converting an unknown property into a poor property value. |
| `CC-E8ECSPF-11` | @fact:CC-E8ECSPF-11 A reusable pattern that teaches an evaluation SHALL publish calibration points for common adjacent-value disagreements and any coordinate-specific evidence payload needed to reach floor or exceptional values. @status:spec/done | Makes the same evaluation guidance usable by more than one evaluator. |
| `CC-E8ECSPF-12` | @fact:CC-E8ECSPF-12 The publication form SHALL keep `E.21` values, `PatternQualityStatus`, corpus-projection evidence, README, ToC, E.11, and I.2 alignment, card or retrieval evidence, cold-reader evidence, monolith parity, landing evidence, Developer, Reviewer, and Executor correspondence, and other quality-carrier facts out of the pattern. These facts belong in the `E.21` result, `E.19` run record, README, ToC, E.11, or I.2, card, retrieval, or projection carrier, or release or landing evidence carrier unless the content-use test shows that the pattern's own `EntityOfConcern` and user-facing action are that evaluation or projection work. @status:spec/done | Prevents quality of the authored pattern from replacing the evaluation guidance it must teach. |

## E.8.ECSPF:9 - Consequences {#consequences}

A conforming `E.8.ECSPF` publication form makes evaluation guidance findable, teachable, and reusable inside FPF. It lets a practitioner frame an evaluation with `E.22` or repeat improvement with `E.23` without re-inventing values. It also makes the cost visible: a reusable evaluation pattern must publish more than a local rubric, because it must prevent wrong-kind use, hidden value drift, neighbour theft, and proxy-for-value substitution.

The pattern's output is bounded evaluation guidance and the form of its result. For product certification, release approval, an evidence claim, or an improvement decision, use the applicable pattern and establish the required result or decision.

## E.8.ECSPF:12 - Relations {#relations}

| Pattern | Relation |
|---|---|
| `E.8` | Defines the canonical FPF authoring form. `E.8.ECSPF` specializes that form for evaluation `CharacteristicSpace` pattern publication forms. |
| `A.19.ECS` | Guides an author in constructing or repairing the evaluation characteristic-space specification. `E.8.ECSPF` helps an author carry the accepted specification into an FPF pattern when durable reuse is selected. |
| `A.19`, `A.17`, `A.18`, `C.16` | Define the corresponding `CharacteristicSpace`, characteristic, scale, coordinate, and measurement-admissibility rules. |
| `E.21` | Guides a reviewer in evaluating the quality of the authored FPF pattern publication form. It does not replace the evaluation for one evaluated object kind. |
| `E.22` | Helps a practitioner frame one quality evaluation using the guidance published in the pattern. |
| `E.23` | Helps an acting system repeat improvement while reusing that published evaluation guidance. |
| `E.9.DA`, `E.2.DA`, `F.18`, `C.25` | Evaluations that may use this authoring specialization when their publication-form is being written or refreshed. |
| `A.10` | Supplies the bounded evidence-use and provenance discipline when an evaluation result is used as evidence. A recorded value alone does not establish an admissible evidence use. |
| `B.3` | Supplies the assurance calculus when an evaluation result supports an actual named assurance claim about an exact target claim. A favourable value alone creates neither assurance nor warranted reliance. |
| `A.20` | Tests a named internal constraint for a current transformation, operation application, or qualifying `A.6.4` assertion in a transformation-flow structure, for a stated case. An evaluation coordinate or status does not establish that constraint result. |
| `A.21` | Maps independently established check results under one applicable profile into a bounded `GateDecisionResult`. An evaluation result may supply a check input; it does not itself become the gate decision. |
| `C.11` | Supplies the general `ChoiceResult` form when an evaluation informs a choice. An evaluation result does not by itself select an option. |
| `A.15` | Supplies the distinctions needed when the claim depends on a particular `MethodDescription`, `Method`, assignment, or performed `Work`. Ordinary pattern use needs no such identity unless the receiving claim turns on it. |
| `C.17`, `C.18`, `C.19`, `G.5`, `G.9`, `G.11` | `C.17` governs novelty and diversity readings; `C.18` governs generation, front and archive records; `C.19` governs pool treatment; `G.5` declares selector-facing results; `G.9` supplies parity results and `G.11` governs currentness and refresh. Use each only for its current contribution. |
| `C.29` | Tests whether a mathematical lens is admissible, including which structure is preserved or lost and what stopping bounds follow. Use it only when such a lens actually supports the coordinate or comparison rule. |


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/E-8#root, spec://ai.lev/fpf-spec/contract/A-19-ECS#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/E-21#root, spec://ai.lev/fpf-spec/contract/E-9-DA#root, spec://ai.lev/fpf-spec/contract/E-2-DA#root, spec://ai.lev/fpf-spec/contract/E-22#root, spec://ai.lev/fpf-spec/contract/E-23#root, spec://ai.lev/fpf-spec/contract/F-18#root, spec://ai.lev/fpf-spec/contract/F-19#root, spec://ai.lev/fpf-spec/contract/C-25#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-19-ECS#root, spec://ai.lev/fpf-spec/contract/E-8#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/E-8-ECSPF
