# C.32.ACE - Architecture Characteristic Eval Programs {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Architecture eval-support subpattern under C.32
> **Status:** Stable
> **Normativity:** Normative unless explicitly marked informative

## C.32.ACE:1 - Problem frame {#problem-frame}

Use this pattern when an architecture team already has project architecture-characteristic rows and must evaluate the current architecture, compare candidate architectures, monitor evolution, or prepare a selection input.

Primary working reader: an architect or evaluator preparing readings over declared architecture-characteristic criteria without turning those readings into the criteria or the decision.

Typical entry phrases:

```text
"We have criteria rows; which eval reading shows how candidate A and candidate B compare under the same parity frame?"
"The monitor is useful, but is this a reading, a test failure, or a decision input?"
"Two methods, roles, system variants, or AI workflows need fair comparison against the same architecture characteristics."
```

**First-minute use slice.** A product-family team has ACS rows for substitutability, evidence reuse, and latency, plus safety as a monitored guardrail. Two candidate architectures look plausible. The practitioner writes one ACE program record with the same claim scope, selected context slices, reference scheme and plane, evaluation window, parity frame, and input projections for both candidates. `EvalService-7` first has the A.13 core for candidate evaluation, and A.15.1 independently admits `CandidateEvalWork-42`, which enacts `ArchitectureCandidateEvaluationMethod-7` and occurs within `ProductFamilyEvaluationService-7`. This first-minute record expressly represents evaluator accountability under `EvaluatorAssignment-3`, an obtaining occurrence of directly declared species `EvaluatorAssignment`, so it also includes the separate F.6 relation through the same A.13 assignment. A Work-only ACE record would omit those assignment and attribution refs, and failed F.6 would leave `CandidateEvalWork-42` intact. `CandidateLatencyReading-42` and `CandidateEvidenceScopeFinding-42` are typed results established through their result patterns. Those results can become inputs for `A.19.CPM` comparison or the next C.32 synthesis pass; neither the program record, Work, nor a result defines the criterion or decides the architecture.

This pattern concerns one architecture-characteristic eval-program record over declared criteria rows, Q-Bundle slots, candidates, bearers, or selected structures under a parity frame. It is a record in a C.32.ACE-local form, not a new `U.*` kind and not, by its `program` label, a `U.Method`, `U.MethodDescription`, `U.WorkPlan`, dated `U.Work`, or evaluation result. When measurement validity, comparison policy, a selection result, G.5 result declaration, publication, or architecture decision is current, use the definition and test for that claim.

Ordinary working move: choose the declared criteria rows, bind the claim scope, relevant context slices, reference scheme and plane, evaluation window, and input projections, and hold one parity frame for all variants. When evaluation actually occurs, recover each exact evaluator through A.13 and let A.15.1 independently admit the `U.Work` occurrence. Add `evaluationWorkAttributionRefs` only when the program or receiving use expressly represents precise assignment-bound attribution; missing or failed F.6 leaves the Work intact. Any A.6.1 operation application is an additional relation, not a substitute for the Method enacted by the Work. Return the typed results established through their result patterns as feedback for comparison or the next synthesis pass.

The first useful output is an `ArchitectureCharacteristicEvalProgram@Project`. This C.32.ACE-local working record states how one bounded architecture evaluation is to be framed over declared criteria. When a reusable way of evaluating is current, identify that separate `U.Method` under A.3.1; when a claim-bearing episteme describes that exact Method, test the same episteme for `U.MethodDescription` under A.3.2. A planned evaluation belongs to A.15.2, an actual dated evaluation to A.15.1, and each result to its direct measurement, comparison, evaluation, or assertion pattern. Use the record to frame readings of characteristics through rows, slots, candidates, or structures; it is not any of those neighboring objects.

For a first pass, fill the exact claim scope and selected context slices, reference scheme and plane, evaluation window and input projections, evaluated rows or Q-Bundle slots, evaluated candidates or structures, parity frame, eval purpose, intended eval operation, result form, receiving use, and refresh or retire condition. Add project-use refs only for a claimed project-local program; add Method, MethodDescription, actual evaluation Work, operation-application, and typed-result refs only when those separate objects are current.

```text
ArchitectureCharacteristicEvalProgram@Project:
  projectWorkOccurrenceRef?: U.EntityRef constrained to U.Work
  architectureEvalProgramProjectUseRelationRef?: U.RelationRef governed by the exact eval-program-use or work-use pattern
  claimScopeRef: U.EntityRef referencing one U.ClaimScope
  selectedContextSliceRefs:
  effectiveReferenceScheme:
  referencePlane?:
  evaluationWindow:
  inputProjectionRefs:
  evaluatedCriteriaSetRef:
  evaluatedCriteriaRowRefs:
  evaluatedQBundleSlotRefs?:
  evaluatedCandidateRefs?:
  evaluatedBearerOrSelectedStructureRefs:
  evalPurpose: characterizeCurrentArchitecture | compareCandidates | monitorEvolution | prepareSelection | triggerNextSynthesis
  evalQuestion:
  parityFrameRef:
  evalScope: singleCriterion | coupledCriteria | qBundleSlice | variantPortfolio | holisticUseSlice
  evalOperation: measurement | simulation | benchmark | scenarioWalkthrough | test | monitor | expertReview | evidenceAudit
  triggerMode: onePass | batchComparison | continual | onChange | manualOnDemand
  resultForm: reading | band | rank | dominanceRelation | tradeoffFront | qualitativeState | evidenceFinding
  runContext: designTime | laboratory | pipeline | production | workReview | decisionPrep
  measurementOrObservationMethodRefs:
  methodDescriptionRefs?:
  evaluationWorkRefs?: FinSet(U.EntityRef constrained to U.Work)
  evaluationWorkAttributionRefs?: FinSet(U.RelationRef constrained to obtaining performedUnderAssignment relations)
  evaluationOperationApplicationRefs?: subject-pattern relation or A.6.1 application references
  evaluationResultRefs?: typed result references accepted under the definition and test for each result
  uncertaintyAndMissingDataPolicy:
  proxyRisk:
  protectedCounterCharacteristicRefs:
  comparisonPolicyRef?:
  receivingUseRef:
  refreshOrRetireCondition:
```

Here `@Project` is a compatibility and retrieval cue only. It supplies no project entity, composite-work identity, context, authority, viewpoint, or parthood. A program local to one actual project names both the composite `U.Work` in `projectWorkOccurrenceRef` and the obtaining program-use relation in `architectureEvalProgramProjectUseRelationRef`; either field alone is insufficient. `evalOperation` states the intended operation family in the program record, not an actual run or application. Each `evaluationWorkRef` names one independently identified `U.Work` occurrence whose exact actual performers have A.13 cores and which A.15.1 admits independently. `evaluationWorkAttributionRefs` are optional and appear only when the record or receiving use expressly represents precise assignment-bound attribution; any present ref resolves through F.6 to the same obtaining A.13 assignment, and its absence or failure does not invalidate the Work ref. Any A.6.1 application binding and each typed result remain under the applicable patterns. A program, Method, MethodDescription, Work occurrence, operation application, assignment, attribution, and result never substitute for one another.

What goes wrong if C.32.ACE is missed: a project has architecture-characteristic rows but treats a test, monitor, dashboard, or source-side "fitness function" as the criterion or as the decision. The team may then reject useful losing variants as errors, optimize one indicator, or choose a candidate without fair comparison.

What C.32.ACE buys in practice: eval work is framed as typed evaluation over declared architecture criteria. A losing candidate can still add knowledge about the solution space, while an actual error remains a failure against an expectation that causes unplanned rework.

Adoption test: after using C.32.ACE, the record shows the candidates, bearers, or selected structures to be evaluated under the same parity frame, the declared result form, and which pattern for the next question may use the reading as feedback. When an actual result is claimed, the record cites that separately established result and its result form.

Not this pattern when the characteristic rows do not exist yet. Also not this pattern when the current work is measurement validity, composite-quality modeling, explicit comparison, set-returning selection, local choice, selected-set result declaration, actual publication, evidence, assurance, or project architecture decision.

Common exits by claim kind:

- `C.32.HCS` and `C.32.ACS` before characteristic rows exist.
- `C.16` for measurement validity, readings, units, uncertainty, or comparability claims.
- `C.25` for Q-Bundles and composite quality families.
- `E.13` when an eval result or dashboard starts replacing the declared architecture concern.
- `C.32` for candidate synthesis, `C.32.MLAO` for residual input, and `E.23` for repeated improvement feedback.
- `A.19.CPM` for explicit comparison, `A.19.SelectorMechanism` for set-returning selection, `C.11` for local choice, and `G.5` for selected-set result declaration. For publication, use `E.17` for a source-backed face and source return and `E.24.PUB` for the publication occurrence and audience availability.
- `A.10` and `B.3` when evidence or assurance claims are being made.
- `C.32.PAD` for project decision.

## C.32.ACE:2 - Problem {#problem}

Architecture synthesis is an optimization and learning activity under competing characteristics. It needs evals: deliberate measurement, simulation, benchmark, scenario, review, or monitoring runs that say how a current architecture or candidate architecture reads against declared criteria.

Testing for errors is a neighboring use. A test asks whether an expectation is violated. An eval asks how variants compare, how a candidate changes the trade-off front, which constraint is hit, or whether the next synthesis pass should open. A candidate that loses the eval is not automatically an error; it may be a deliberate probe that improves the architecture team's knowledge of the solution space.

Evolutionary-architecture sources often say "fitness function". In FPF that is source-side wording. The recoverable FPF object is an eval program over declared architecture-characteristic rows, Q-Bundle slots, candidate structures, and a parity frame. Some eval programs can specify automated tests or monitors, but automation does not change the kind of the program record.

## C.32.ACE:3 - Forces {#forces}

| Force | Tension |
|---|---|
| Variant learning | Candidate architectures may be valuable even when they lose the selection being made. |
| Fair comparison | Eval results are useful only when context, budgets, windows, units (when required by the scale), and missing-data treatment are explicit. |
| Trade-off pressure | Improving one architecture characteristic can worsen another. |
| Automation value | Frequent automated evals reveal drift early, but their results can be overread. |
| Error prevention | Some eval operations are tests, yet error checking must not replace variant comparison. |
| Evolution | A useful eval can expire when the source-currentness relation, environment, declared holon-level ref, or scale window changes. |

## C.32.ACE:4 - Solution {#solution}

Create an architecture-characteristic eval program only after the evaluated criteria rows exist in `C.32.ACS` or a declared C.25 Q-Bundle slot.

Work in this order:

1. Reference the evaluated ACS criteria set, evaluated rows, and any Q-Bundle slots.
2. State the eval purpose: current characterization, candidate comparison, portfolio-frontier work, post-change impact measurement, monitoring, or trigger for the next synthesis pass.
3. Name the candidates, bearers, and selected structures being evaluated.
4. Establish one exact `U.ClaimScope`, the relevant A.2.6 `U.ContextSlice` membership, effective `U.ReferenceScheme` and reference plane, evaluation window, input projections, resource budget, units (when required by the scale), admissible observation or evidence inputs, and missing-or-unknown policy. Record their parity requirement in `parityFrameRef`; the parity-frame record does not replace those bindings.
5. Choose eval scope: one criterion, coupled criteria, one Q-Bundle slice, a candidate portfolio, or a holistic use slice.
6. Choose eval operations. Use measurement, simulation, benchmark, scenario walkthrough, monitor, review, or evidence audit according to the claim. Use `test` only when the intended operation checks an expectation or hard constraint. When evaluation actually occurs, recover each exact evaluator through A.13 and let A.15.1 independently admit the `U.Work` occurrence and enacted Method. Add `evaluationWorkAttributionRefs` only when the record or receiving use expressly represents precise assignment-bound attribution. Independently identify the relation or A.6.1 application binding that obtains and the typed result; the program record itself does not run.
7. Declare the result form. Examples include a reading, band, rank, dominance relation, trade-off front, qualitative state, or evidence finding; use the definition and test for the actual result kind.
8. Name proxy risk and protected counter-characteristics before the eval result can drive work. Optimize only the cycle's chosen indicators; keep the remaining protected characteristics visible as guardrails or risk signals.
9. State the receiving use: `C.32` synthesis input, `C.32.MLAO` residual input, `E.23` improvement feedback, `A.19.CPM` comparison input, `A.19.SelectorMechanism` selection input, `C.11` choice input, input for a selected-set result declared under `G.5`, or architecture-decision input for `C.32.PAD`. For publication input, distinguish `E.17` source-backed face and source return from the `E.24.PUB` publication occurrence and audience availability.
10. Refresh or retire the eval program when the evaluated row, C.32 candidate palette, bearer, selected structure, environment, parity frame, or source-currentness relation changes.

**Stop condition.** Stop C.32.ACE when the eval program names evaluated rows or Q-Bundle slots, evaluated candidates or structures, parity frame, eval purpose, eval operation, result form, receiving use, proxy risk, protected counter-characteristics, and refresh or retire condition.

**Lowering condition.** Use the eval result for the current architecture work only while the evaluated rows, evaluated candidates or structures, parity frame, eval operation, result form, and receiving use still match the work being done. Limit use of the result to report-only when missing data, proxy risk, or parity-frame mismatch prevents the intended synthesis, comparison, selection, selected-set result declaration, actual publication, choice, evidence, assurance, or decision use. Retire the eval program when its evaluated row, bearer, selected structure, environment, source-currentness relation, or receiving use no longer belongs to the current architecture work. Use `C.32.ACS` when the criteria row is missing or wrong, `C.16` when measurement validity is current, `C.25` when the evaluated item is composite, and the named pattern for the next question when a stronger downstream claim is current.

## C.32.ACE:7 - Conformance requirements {#conformance-requirements}

| Requirement | Required result |
|---|---|
| `CC-ACE-1` | @fact:CC-ACE-1 Every eval references declared ACS rows or C.25 Q-Bundle slots. @status:spec/done |
| `CC-ACE-2` | @fact:CC-ACE-2 Every eval names evaluated candidates, bearers, or selected structures. @status:spec/done |
| `CC-ACE-3` | @fact:CC-ACE-3 Purpose, parity frame, scope, eval operation, trigger mode, result form, and run context are explicit. @status:spec/done |
| `CC-ACE-4` | @fact:CC-ACE-4 Measurement claims require `C.16`; composite quality claims require `C.25`. @status:spec/done |
| `CC-ACE-5` | @fact:CC-ACE-5 Proxy risk, missing-data policy, and protected counter-characteristics are named before a receiving synthesis, comparison, or selection pattern uses the eval result. @status:spec/done |
| `CC-ACE-6` | @fact:CC-ACE-6 Source-side "fitness function" wording is not used as the FPF object name in the record. @status:spec/done |
| `CC-ACE-7` | @fact:CC-ACE-7 A check or test is admitted only as one eval operation when an expectation or hard constraint is being inspected. @status:spec/done |
| `CC-ACE-8` | @fact:CC-ACE-8 The eval result does not select, decide, certify, or carry an architecture-adequacy claim by itself. @status:spec/done |
| `CC-ACE-9` | @fact:CC-ACE-9 A project-local program names both `projectWorkOccurrenceRef` and `architectureEvalProgramProjectUseRelationRef`; the suffix or either reference alone asserts no locality. @status:spec/done |
| `CC-ACE-10` | @fact:CC-ACE-10 The record separately identifies any reusable Method, MethodDescription, planned evaluation, dated evaluation Work, actual operation application, and typed result that the use needs; `evalOperation` or `resultForm` supplies none of those occurrences or identities. @status:spec/done |
| `CC-ACE-11` | @fact:CC-ACE-11 Every actual evaluation use binds one exact `U.ClaimScope`, relevant A.2.6 `U.ContextSlice` membership, effective reference scheme and plane, evaluation window, and input projections; `evalScope`, `runContext`, and `parityFrameRef` do not replace them. @status:spec/done |

## C.32.ACE:9 - Consequences {#consequences}

| Consequence | Benefit | Cost |
|---|---|---|
| Evals are typed evaluations over declared criteria. | Variant comparison can proceed without collapsing criteria, readings, and decisions. | The team must write the parity frame before using the result in a pattern for the next question. |
| Expectation-failure tests remain one eval operation when their expectation is declared. | Error prevention remains available without replacing optimization. | Some pass-fail dashboards can no longer drive decisions by themselves. |
| Losing variants remain useful. | Architecture exploration keeps stepping stones and source-space learning. | The variant archive needs deliberate upkeep. |
| Proxy and counter-characteristic risks are explicit. | Goodhart pressure is visible before eval results drive work. | More rows may remain monitored as guardrails rather than optimized. |

## C.32.ACE:12 - Relations {#relations}

- **Builds on:** `C.32.HCS`, `C.32.ACS`, `C.16`, `C.16.P`, `C.25`, `A.2.6`, `A.19`, `E.13`, `E.22`, `E.23`, and `A.19.CPM`; coordinates with A.3.1, A.3.2, A.15.2, A.15.1, and A.6.1 only for separately current Method, MethodDescription, planned Work, dated Work, or operation-application claims.
- **Receiving uses:** `C.32.P2S` actual-structure feedback and next-synthesis repair, `C.32` candidate synthesis, `C.32.MLAO` residual optimization, `C.32.CONWAY` correspondence frames, `C.32.FAIL` repair, `A.19.CPM` comparison, `A.19.SelectorMechanism` selection, `C.11` local choice, selected-set result declaration under `G.5`, source-backed publication-face and source-return work under `E.17`, publication-occurrence and audience-availability work under `E.24.PUB`, and architecture-decision work for `C.32.PAD`.
- **Measurement boundary:** Use `C.16` when a reading, coordinate, unit, threshold, score, uncertainty, or cross-case comparability claim is made.
- **Structural-information boundary:** For an eval, these contributions are available only after `C.32.ACS`, `C.16`, or `C.25` has declared what is being evaluated: `C.33` and `C.34` for captured structure, lost structure, and preservation adequacy, and `C.35` for recovering the kind of a generated or discovered result and assessing its adequacy for that architecture use. Use C.32.ACE for the eval-program frame, and accept each actual typed result under its own measurement, comparison, evaluation, or assertion definition and test. `C.33`, `C.34`, and `C.35` do not define eval programs.
- **Q-Bundle boundary:** Use `C.25` when the evaluated item is a composite quality family.
- **Test boundary:** Use `test` only as an eval operation for a declared expectation or hard constraint. Error recognition and architecture-synthesis repair use `C.32.FAIL`; non-architecture defects use the local defect-subject pattern.
- **Decision boundary:** An evaluation framed by an ACE record may reference separately admitted readings, ranks, dominance relations, trade-off-front descriptions, and other typed results. When such a result is current, identify the admitted System, dated evaluation Work, applicable operation application, and the definition and test used for that exact measurement, comparison, evaluation, or assertion result. Such a result may serve as source material for an A.10 evidence-provenance account when an evidence claim is current. Use `A.19.CPM` for explicit comparison, `A.19.SelectorMechanism` for set-returning selection, `C.11` for local choice, `G.5` for selected-set result declaration, and `C.32.PAD` for a project architecture decision. When audience availability is current, use `E.17` for a source-backed publication face and return to source and `E.24.PUB` for the publication occurrence, form, carrier, audience, bounded use, and availability.


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/C-32-ACS#root, spec://ai.lev/fpf-spec/contract/C-16#root, spec://ai.lev/fpf-spec/contract/C-25#root, spec://ai.lev/fpf-spec/contract/E-13#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/C-32#root, spec://ai.lev/fpf-spec/contract/C-32-MLAO#root, spec://ai.lev/fpf-spec/contract/C-32-PAD#root, spec://ai.lev/fpf-spec/contract/A-19-CPM#root, spec://ai.lev/fpf-spec/contract/G-5#root, spec://ai.lev/fpf-spec/contract/C-11#root, spec://ai.lev/fpf-spec/contract/A-10#root, spec://ai.lev/fpf-spec/contract/B-3#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/C-32#root, spec://ai.lev/fpf-spec/contract/C-32-ACS#root, spec://ai.lev/fpf-spec/contract/C-32-ADA#root, spec://ai.lev/fpf-spec/contract/C-32-HCS#root, spec://ai.lev/fpf-spec/contract/C-32-MLAO#root, spec://ai.lev/fpf-spec/contract/C-32-PAD#root, spec://ai.lev/fpf-spec/contract/C-33#root, spec://ai.lev/fpf-spec/contract/C-34#root, spec://ai.lev/fpf-spec/contract/C-35#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/C-32-ACE
