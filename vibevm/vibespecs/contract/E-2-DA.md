# E.2.DA - Evaluate How FPF Realizes Its Pillars (Pillar-Adequacy CharacteristicSpace) {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

Status: Core.

## E.2.DA:1 - Problem frame {#problem-frame}

Use `E.2.DA` when the object under improvement is an FPF-level object and the question is whether it realizes the `E.2` Pillars adequately for a declared use. The object can be a monolith edition, selected pattern host set, pattern family, projection set, README/Preface/ToC publication change, access-carrier exposure such as a skill or MCP-backed route, release candidate, or whole-FPF edition.

Use it after a broad cleanup, new pattern family, projection repair, source-use repair, FPF-form change under `E.4.FPF`, or corpus-level improvement when local pattern quality is not enough. A set of good local patterns can still harm FPF entry, naming, layering, source use, projection integrity, or open-ended evolution.

Not this pattern when the evaluated object is one authored pattern version, one `DRR`, one local wording repair, or one pattern-use entry problem. Use `E.21`, `E.9.DA`, `F.19`, or `E.11` respectively. Open `E.10` or a precision-restoration neighbor for an unresolved FPF-specific wording question.

First useful move: name the FPF object under improvement by value, declared use, reader family, and qualification window; then evaluate all eleven Pillar coordinates. If a Pillar seems unaffected, give it a value and a short rationale saying what is preserved.

What goes wrong if missed: FPF can become locally polished but globally worse. Readers may find fewer useful entry points, precision repairs may erase the working move, source rows can turn decorative, or several patterns can grow local variants of the same doctrine.

Primary EntityOfConcern in plain terms: the scoped FPF object under improvement as an `E.2` Pillar-realizing language object.

## E.2.DA:2 - Problem {#problem}

`E.2` gives the Pillars and their constitutional meaning. It does not by itself evaluate whether a concrete FPF object realizes those Pillars well enough for a concrete use. Without `E.2.DA`, corpus-level reviews tend to collapse into local pattern scores, process state, review praise, or broad claims that "FPF improved."

The specific failures are:

1. Local pattern quality is averaged into FPF adequacy.
2. Entry projections and companion files become separately maintained sources of definitions, constraints, or tests supplied by pattern bodies.
3. Precision repair improves terminology but damages first-use comprehension or changes the FPF kind carried by the repaired text.
4. Source and SoTA rows are counted rather than checked for changes in FPF moves.
5. Front-like words such as `all 5s`, `exceptional`, `Pareto`, `SoTA`, `NQD`, or `shortlist` become loose synonyms.
6. Corpus-level stop claims hide what became worse.
7. Pillar values become repair targets, so the corpus gains projection proof, entry apparatus, source rows, or review evidence while the FPF object becomes less usable, less layered, or less decisive.

## E.2.DA:3 - Forces {#forces}

| Force | Tension |
|---|---|
| Constitutional meaning vs evaluation | Pillar meanings stay in `E.2`; values over realized adequacy are evaluated here. |
| Whole-FPF quality vs local quality | One strong pattern can still sit in a weak corpus ecology. |
| Discoverability vs precision | Real readers search ordinary words, while claim-bearing wording must preserve its FPF kinds and point to the content that defines, constrains, or tests the claim. |
| Didactic force vs semantic admissibility | The text must teach the move without smuggling new ontology into examples or projections. |
| Breadth vs affordability | Eleven Pillars are complete enough for FPF; affordability comes from compact evidence, not omitted coordinates. |
| Open-ended evolution vs release stop | FPF can improve forever, but one scoped object needs a local stop condition. |

## E.2.DA:4 - Solution {#solution}

`E.2.DA` is the Pillar-adequacy specialization of `A.19.ECS`. An evaluator applies its questions to one FPF object under improvement against all eleven `E.2` Pillars for a declared use.

An `E.2.DA` result gives every Pillar coordinate a value, short rationale, evidence locus, and shared evidence basis for the FPF object being evaluated. Local pattern quality, `DRR` adequacy, and wording repair use their own object-under-improvement questions. A bounded diagnostic may borrow selected Pillar questions, but makes neither an E.2.DA-result nor an FPF-adequacy status claim.

### E.2.DA:4.1 - Local names and kind settlement {#local-names-and-kind-settlement}

| Local name | Kind and use |
|---|---|
| `FPFPillarAdequacyEvaluation` | Authored evaluation record over one scoped FPF Pillar-adequacy claim. |
| `FPFObjectUnderImprovementRef` | FPF object version named by value being evaluated. |
| `FPFAdequacyUseScope` | Declared FPF-level use the object must serve. |
| `FPFAdequacyReaderScope` | Primary reader family and working situation for the adequacy claim. |
| `FPFAdequacyQualificationWindow` | Edition, source-currentness, neighbour, release, or comparison window for which the values hold. |
| `FPFPillarAdequacyCoordinateSet` | The eleven required Pillar coordinates in this pattern. |
| `FPFPillarAdequacyEvidenceBasis` | Checked loci named by value in the scoped FPF object: pattern bodies, host or monolith sections, projections, README scenarios, ToC rows, `E.11` entry-distribution loci, `I.2` expanded entry-disambiguation cases, source rows, relation rows, companion files, evaluation results, and missing or unchecked loci that affect values. |
| `FPFPillarValueRationales` | Required result rows: Pillar coordinate, value, short rationale, and evidence locus named by value. |
| `PillarAdequacyEvidenceRefs` | Loci named by value in patterns, projections, source rows, entry rows, relation rows, or findings used as value evidence. |
| `FPFKindRestorationEvidence` | For broad wording or precision repair, identifies the changed span and its pre- and post-repair object kind, relation or claim kind, admissible use, and scope; when part of the changed FPF-governed claim, also the current ontic slot, relation position, and use relation. It names the concrete contribution of any cited pattern content and the preserved, split, intentionally changed, or blocker disposition. |
| `FPFPillarAdequacyStatus` | Admissible-use result for the scoped FPF Pillar-adequacy claim. |
| `FPFPillarAdequacyFront` | Optional non-dominated set of FPF variants or edit packages under the declared coordinate set. |

These names are local to the evaluation unless `F.18` promotes a durable name. They name FPF content objects and evaluation fields, not release state, review state, or project evidence.

### E.2.DA:4.2 - Evaluation record {#evaluation-record}

```text
FPFPillarAdequacyEvaluation:
  FPFObjectUnderImprovementRef: <object and version named by value>
  FPFAdequacyUseScope: <entry | authoring | review | project use | source absorption | corpus release | other use named by value>
  FPFAdequacyReaderScope: <primary reader and working situation>
  FPFAdequacyQualificationWindow: <edition, source, neighbour, release, or comparison window>
  FPFPillarAdequacyEvidenceBasis: <checked pattern, host, monolith, projection, README, ToC, E.11, or I.2 entry locus, source, relation, companion, evaluation-result, and missing loci that affect values>
  FPFPillarAdequacyCoordinateTable: <all eleven coordinates, values, short rationales, evidence loci>
  FPFKindRestorationEvidence: <for broad wording or precision repair: changed span; pre- and post-repair object kind, relation or claim kind; current ontic slot, relation position, and use relation when part of the changed FPF-governed claim; admissible use and scope; concrete contribution of any cited pattern content; preserved, split, intentionally changed, or blocker disposition>
  FPFPillarAdequacyStatus: <status>
  StopOrRepairCondition: <local stop, first repair, Pillar decision, or architecture decision, and the smallest reopen locus or condition>
```

`E.22` may frame the evaluation purpose when the caller needs floor evaluation, exceptional improvement, trade-off inspection, open-question discovery, absorption, or proposal portfolios. `E.23` governs repeated improvement after the evaluation returns findings or candidate proposals.

### E.2.DA:4.3 - Ordinal coordinate scale {#ordinal-coordinate-scale}

| Value | Label | Meaning |
|---:|---|---|
| 0 | `absent` | The Pillar is not realized for the declared FPF object and use. |
| 1 | `namedOnly` | The Pillar is named but cannot guide the FPF-level use. |
| 2 | `partiallyExpressedForDeclaredUse` | The Pillar is present but incomplete, fragile, or too local. |
| 3 | `sufficientlyExpressedForDeclaredUse` | The Pillar is realized enough for the declared use, with known limits visible. |
| 4 | `wellExpressedForDeclaredUse` | The Pillar is clear across relevant loci and protected from common loss. |
| 5 | `exceptionallyExpressedForDeclaredUse` | The Pillar is exceptionally realized with reinforcing loci, heterogeneous cases, and no hidden FPF-level loss. |

The values are ordinal content evaluations. They are not an aggregate scalar score, maturity ladder, release gate, or proof that development ends.

### E.2.DA:4.4 - Required Pillar coordinates {#required-pillar-coordinates}

| Pillar coordinate | Evaluation question | Good state |
|---|---|---|
| `P1CognitiveEleganceAdequacy` | Does the object expose decisive structure without ornamental formalism? | The reader sees the smallest structure that changes the action. |
| `P2DidacticPrimacyAdequacy` | Does human comprehension stay ahead of formal, tooling, or review purity? | Working situation, recognition reason, first move, and payoff stay visible. |
| `P3ScalableFormalityAdequacy` | Can informality mature toward formal assurance without forks or rewrites? | Plain, Tech, Formal, and mathematical strengthening remain staged. |
| `P4OpenEndedKernelAdequacy` | Do kernel concepts stay meta-level while domain knowledge stays in patterns? | New content extends FPF without smuggling domain doctrine into the kernel. |
| `P5FPFLayeringAdequacy` | Do modular pattern layering and neighbour authority stay intact? | Patterns can be added, replaced, or removed without shadow authority. |
| `P6LexicalStratificationAdequacy` | Are Plain, Tech, Formal, and mathematical registers recoverable for the declared use? | Decision-governing wording maps to fields named by value, kinds, lenses, or neighbours. |
| `P7PragmaticUtilityAdequacy` | Do proofs, measures, models, and reviews change real admissible action? | The object changes prediction, decision, diagnosis, design, repair, stop, or assignment. |
| `P8CrossScaleConsistencyAdequacy` | Do composition, aggregation, boundary, emergence, and method-side relation structures stay consistent across scales? | Cross-scale claims name preserved structure, lost structure, lens or algebraic representation, and boundary. |
| `P9StateExplicitnessAdequacy` | Are states, transitions, currentness, editions, and qualification windows explicit for the declared use? | Readers can tell what version and state are being used and what changes them. |
| `P10OpenEndedEvolutionAdequacy` | Can improvement continue cheaply and safely without pretending development ends forever? | Local stop conditions coexist with reopen conditions for new use, source, comparison, or failure evidence. |
| `P11SoTAAlignmentAdequacy` | Does current knowledge discipline the object without citation theatre? | Current sources change moves, boundaries, examples, checks, or stop rules. |

### E.2.DA:4.5 - Evidence and coordinate separation {#evidence-and-coordinate-separation}

One evidence locus may support several coordinates, but the rationale must say what property it supports in each coordinate. The following distinctions carry most repairs:

| Distinction | Use |
|---|---|
| `P1` vs `P2` | smallest decisive structure vs reader comprehension and first move. |
| `P2` vs `P6` | usable recognition text vs recoverable register mapping. |
| `P5` vs `P7` | placement of the content that defines, constrains, or tests the claim vs useful change in action. |
| `P7` vs `P11` | practical payoff vs current source contribution. |
| `P8` vs `P9` | cross-scale invariant vs state, transition, edition, and currentness. |
| `P10` vs `E.23` | evolvability of the FPF object vs repeated improvement method. |

If a distinction cannot be recovered from the FPF object, lower the affected coordinate and state the first repair. Do not add a new local doctrine table to explain around the missing content.

`E.21` and `E.9.DA` results are evidence loci for `E.2.DA`, not inputs to be averaged. A pattern-quality value can support a Pillar only by pointing to the evaluated pattern's beneficial or harmful FPF-level effect.

### E.2.DA:4.5a - Result-row discipline and calibration {#result-row-discipline-and-calibration}

An `E.2.DA` result uses this table shape:

| Pillar coordinate | Value | ShortRationale | EvidenceLocus |
|---|---:|---|---|
| `<E.2.DA coordinate>` | `<0..5>` | `<assigned-value basis and the applicable adjacent-value rationale below>` | `<pattern section, monolith section, host, README scenario, ToC row, E.11 entry-distribution locus, I.2 expanded case, projection, source row, relation row, companion file, evaluation result, or missing locus named by value>` |

For values `1..4`, explain why the lower adjacent value would understate the evidence and the higher adjacent value would overstate it. For `0`, explain why `1` would overstate the evidence and what would raise the value or reopen it. For `5`, explain why `4` would understate the evidence and what would lower the value or reopen it.

A Pillar essay, local-quality average, two-column table, or result whose value depends on unchecked corpus, projection or source evidence is draft evaluation material. Check the needed evidence before assigning the affected value. An observed defect lowers a value according to its coordinate meaning; absence of a check does not by itself establish that defect. A completed E.2.DA result still evaluates all eleven coordinates.

Common calibration points:

| Pillar family | `3` | `4` | `5` |
|---|---|---|---|
| Entry, usability, and projection Pillars | The object can be used with visible limits, but projection or first-use evidence is partial. | Relevant defining, constraining, or testing content and projections are coherent enough for declared use. | The use is replayable across pattern content, the public-entry form selected under E.11, and cold-reader or retrieval evidence, with an explicit stop or return and any independently grounded non-use boundary. |
| Layering and semantic authority Pillars | Neighbours are plausible, but some shadow-spec risk remains. | The pattern content that defines, constrains, or tests each claim is named by value and distinguishable from source-linked projections. | Pattern bodies, relations, projection rows, and anti-fragmentation cases keep each concrete contribution recoverable without shadow semantics. |
| Source and evolution Pillars | Source or reopen language exists, but currentness, contribution, or smallest-reopen basis is compact. | Source contribution, currentness window, and reopen condition are explicit for declared use. | Source-front movement and future reopen are replayable without freezing development after a local stop. |

### E.2.DA:4.6 - Status and stop condition {#status-and-stop-condition}

| Status | Meaning |
|---|---|
| `admissibleForDeclaredFPFUse` | All eleven coordinates meet the declared floor for the scoped use. |
| `repairBeforeFPFUse` | One or more coordinate floors fail for the declared use. |
| `holdForPillarDecision` | The defect requires an `E.2` Pillar amendment or precedence decision. |
| `holdForArchitectureDecision` | The defect requires pattern split, object-under-improvement, source-use, projection-use, or naming architecture decision. |
| `refreshNeeded` | A source, pattern, entry use, projection, relation, or vocabulary change invalidates a previous evaluation. |

The stop condition states the declared floor, values, smallest reopen locus, and first repair when the declared use is not yet admissible. Add a non-use boundary only when an independently grounded reading by a plausible intended reader changes a named use.

### E.2.DA:4.7 - Compact result form {#compact-result-form}

```text
E.2.DA result:
  FPF object under improvement: <FPFObjectUnderImprovementRef>
  Declared use and reader: <scope>
  Qualification window: <window>
  Evidence basis checked: <FPFPillarAdequacyEvidenceBasis>
  Status: <FPFPillarAdequacyStatus>
  Coordinate table: <Pillar coordinate | Value | ShortRationale | EvidenceLocus for all eleven Pillars>
  First repair or stop: <repair | hold | local stop>
  Reopen if: <smallest changed locus or condition>
```

For a small release decision, the coordinate table may be compact. It is still complete. Status is not assigned from prose, a checklist count, a local-pattern average, a two-column table, or a result missing evidence loci needed by its values.

When `E.22`, `E.23`, absorption, or exceptional-improvement framing asks for improvement, below-floor Pillar coordinates return findings or repair. Above-floor coordinates receive proposal rows only for substantive non-dominated FPF-level content opportunities inside the declared use: for example, better entry recognition, placement of defining, constraining, or testing content, source-currentness carry-through, projection thinning, corpus-ecology repair, kind-preserving precision restoration, open-ended evolution support, or deletion or relocation of apparatus that weakens the FPF object. Apparatus-only additions do not qualify. Do not treat every value below `5` as a defect. A `4` may be the correct stop value only with loci showing why further Pillar-content movement is dominated, unavailable, or outside scope.

## E.2.DA:7 - Conformance checklist {#conformance-checklist}

| Check | Requirement |
|---|---|
| `CC-E2DA-1` | @fact:CC-E2DA-1 Name `FPFObjectUnderImprovementRef`, use scope, reader scope, and qualification window. @status:spec/done |
| `CC-E2DA-2` | @fact:CC-E2DA-2 Preserve `E.2` as the source of Pillar meaning. @status:spec/done |
| `CC-E2DA-3` | @fact:CC-E2DA-3 Evaluate all eleven Pillar coordinates with values, short rationales, and evidence loci, using the required result-row shape. @status:spec/done |
| `CC-E2DA-4` | @fact:CC-E2DA-4 Justify values from FPF content, not review praise, landing, monolith placement, or absence of visible defects. @status:spec/done |
| `CC-E2DA-5` | @fact:CC-E2DA-5 State declared use, status, stop or first repair, and reopen condition; add a non-use boundary only when an independently grounded reading changes that use. @status:spec/done |
| `CC-E2DA-6` | @fact:CC-E2DA-6 Keep the pattern-derived rules in projections, packets, companions, and entry rows traceable to the supplying pattern bodies. Each authored definition, constraint, test, method instruction, or publication rule stays in its pattern body. Preserve E.11's distinct locator, ordinary-entry, and Practical-Use Card functions, including the first-use guidance admitted for that form. @status:spec/done |
| `CC-E2DA-7` | @fact:CC-E2DA-7 Treat `E.21` and `E.9.DA` as evidence loci only where they change Pillar realization. @status:spec/done |
| `CC-E2DA-8` | @fact:CC-E2DA-8 State what became worse when visible coordinates improved. @status:spec/done |
| `CC-E2DA-9` | @fact:CC-E2DA-9 State the `FPFPillarAdequacyEvidenceBasis`. For every value, check the host, publication, projection, entry, source, relation or evaluation evidence it actually needs. Keep an unsubstantiated value and its evidence gap in draft material; do not assign an E.2.DA status until all eleven values are justified. @status:spec/done |
| `CC-E2DA-10` | @fact:CC-E2DA-10 Use the value-appropriate adjacent comparison in E.2.DA:4.5a for every assigned value, including its endpoint rule for `0` or `5`. @status:spec/done |
| `CC-E2DA-11` | @fact:CC-E2DA-11 For broad wording, naming, or precision cleanup, state `FPFKindRestorationEvidence` for changed FPF-governed meanings. Preserve the pre- and post-repair object kind, relation or claim kind, admissible use, and scope; also preserve the current ontic slot, relation position, and use relation when they are part of the changed claim. When the changed position depends on cited pattern content, name its concrete contribution. An unaccepted semantic change lowers the affected Pillar coordinates and keeps the repair blocking. @status:spec/done |
| `CC-E2DA-11a` | @fact:CC-E2DA-11a When the evaluated FPF object includes ontic architecture, evaluate FPF-level effect, not ontic apparatus volume: reduced duplicate ontology or type explosion, clearer `EntityOfConcern` and SlotRelation boundaries, correct description-publication separation, thinner projections, and improved entry, authoring, review, or project use. Missing effect lowers the affected `P1`, `P2`, `P4`, `P5`, `P6`, `P7`, or `P8` coordinates. @status:spec/done |
| `CC-E2DA-12` | @fact:CC-E2DA-12 Keep Pillar values as ordinal evaluation results, not repair targets. Below-floor values require FPF-level findings or repair. Above-floor improvement requires substantive non-dominated proposal rows when requested; it cannot close by adding projection proof, entry apparatus, source volume, review praise, monolith parity evidence, or all-`5` result framing that does not improve Pillar realization for the declared FPF use. A no-proposal or stay-at-current-value disposition must name loci and why no worthwhile Pillar-content improvement remains. @status:spec/done |

## E.2.DA:9 - Relations {#relations}

| Pattern | Relation |
|---|---|
| `E.2` | Supplies Pillar names and meanings. |
| `A.19.ECS` | Supplies construction discipline for object-under-improvement evaluation characteristic spaces. |
| `E.4.FPF` | Identifies FPF itself as a first-principles framework edition and defines its form and publication or access-carrier assembly; `E.2.DA` supplies the resulting whole-FPF Pillar-adequacy questions. |
| `E.21` | Evaluates one pattern version; may supply evidence loci. |
| `E.9.DA` | Evaluates one `DRR`; may supply evidence loci. |
| `E.24`, `E.24.CD`, `E.24.PUB` | Govern ontic concept introduction, candidate detection, ontic-description and publication discipline, and publication-boundary repairs whose FPF-level Pillar effect may be evaluated here. |
| `E.22` | Frames the quality-evaluation purpose when needed. |
| `E.23` | Describes repeated improvement after values or proposal rows exist. |
| `E.13` | Governs pragmatic utility and proxy-to-value alignment when Pillar values, corpus indicators, review result, or projection evidence become substitutes for realized FPF value. |
| `E.10`, `A.6.P`, `C.2.P`, `C.16.Q`, `F.18` | Govern local precision and naming repair. |
| `F.19` | Supplies the connected precise-language reading, repair, and local revalidation; E.2.DA evaluates its FPF-level Pillar effect. |
| `E.11`, `E.17`, `I.2` | Govern entry, projection, publication, description, and expanded entry-disambiguation uses that may affect Pillar adequacy. |
| `C.18`, `C.19`, `G.5`, `G.9`, `G.11` | Govern OEE, NQD, pool, selected-set, parity, and refresh semantics when those semantics are claimed. |
| `C.29`, `C.16`, `A.17`, `A.18`, `A.19` | Govern mathematical-lens, characteristic, scale, measurement, and characteristic-space admissibility when those claims are being made. |

## E.2.DA:12 - Consequences {#consequences}

| Consequence | Benefit | Cost |
|---|---|---|
| FPF-level adequacy becomes measurable by content. | Release and corpus decisions no longer rely on local praise or review state. | Evaluators must name the FPF object and declared use by value. |
| Complete Pillar evaluation blocks partial-good stories. | Hidden losses in entry, layering, source use, and evolution become visible. | Even compact evaluations must touch all eleven coordinates. |
| Local evaluation patterns keep their authority. | `E.21`, `E.9.DA`, and `E.10` are evidence or repair neighbours, not substitutes. | Users must choose the right object under improvement before evaluating. |


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/E-2#root, spec://ai.lev/fpf-spec/contract/A-19-ECS#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/E-21#root, spec://ai.lev/fpf-spec/contract/E-9-DA#root, spec://ai.lev/fpf-spec/contract/E-22#root, spec://ai.lev/fpf-spec/contract/E-23#root, spec://ai.lev/fpf-spec/contract/E-11#root, spec://ai.lev/fpf-spec/contract/E-10#root, spec://ai.lev/fpf-spec/contract/F-18#root, spec://ai.lev/fpf-spec/contract/F-19#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-19-ECS#root, spec://ai.lev/fpf-spec/contract/E-13#root, spec://ai.lev/fpf-spec/contract/E-19#root, spec://ai.lev/fpf-spec/contract/E-21#root, spec://ai.lev/fpf-spec/contract/E-22#root, spec://ai.lev/fpf-spec/contract/E-23#root, spec://ai.lev/fpf-spec/contract/E-4-DPF-DA#root, spec://ai.lev/fpf-spec/contract/E-4-FPF#root, spec://ai.lev/fpf-spec/contract/E-8-ECSPF#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/E-2-DA
