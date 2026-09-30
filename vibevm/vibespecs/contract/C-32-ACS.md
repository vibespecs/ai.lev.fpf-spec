# C.32.ACS - Architecture Characteristic Criteria Set {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Architecture characterization pattern under C.32
> **Status:** Stable
> **Normativity:** Normative unless explicitly marked informative

## C.32.ACS:1 - Problem frame {#problem-frame}

Use this pattern when a project must turn architecture-characteristic pressure into a small project criteria set for architecture improvement, candidate synthesis, residual optimization, and later eval work.

Primary working reader: an architect or architecture-responsible practitioner turning broad quality names into project criteria rows for the next improvement cycle.

Typical entry phrases:

```text
"Maintainability matters, but which bearer and scale make it an architecture criterion here?"
"We can optimize only a few rows; which characteristics drive optimization and which guard against loss?"
"Architecture around a Method, local system-role kind, separate System-classification judgment, assignment, AI workflow, or built asset has trustworthiness or teachability pressure; what is the exact characteristic bearer and which Q-Bundle slot or ACS row is current?"
```

**First-minute use slice.** A product-family architect has HCS starter heads and source catalogue names for maintainability, substitutability, evidence reuse, safety, availability, latency, and scale amenability. Using C.32.ACS, the practitioner builds project rows and gives each row its bearer, exact `U.ClaimScope`, relevant A.2.6 `U.ContextSlice` membership, effective reference scheme and plane, qualification or evaluation window, scale form, proxy risk, protected losses, and source-return condition. Maintainability, substitutability, and evidence reuse become optimization indicators; safety and availability remain monitored guardrails. The source phrase "scale amenability" remains only a starter cue until ACS admits a concrete characteristic row, such as exception growth or interface-grammar variation, with its bearer and scale form; a claim that one alternative is preferable under a declared scale window remains a separate `C.31.ASAP` object. C.32 can now synthesize candidates against declared criteria instead of a loose list of quality words.

This pattern concerns one project architecture-characteristic criteria-set record for improvement cycles. Its rows can supply C.32 synthesis, C.32.MLAO residual work, C.32.ACE eval programs, and later patterns for the next questions. The set and its rows are C.32.ACS-local record forms, not new `U.*` kinds; starter packs, `U.Characteristic` values, Q-Bundles, measurement methods and results, eval programs and results, candidate palettes, comparison rules, selection results, G.5 result declarations, actual publications, local choices, and architecture decisions remain separate objects.

Ordinary working move: make one row per project architecture characteristic, bind its bearer and scale, mark whether it drives optimization, guards against loss, or only gives context, and record what eval reading can reopen synthesis.

The first useful output is `ArchitectureCharacteristicCriteriaSet@Project`:

For a first pass, fill the described holon, architecture use, a small set of draft row names, and for every row the bearer or selected structure, exact claim scope and selected context slices, reference scheme and plane, qualification or evaluation window, scale form, use class, protected losses, receiving use, and reopen condition. Add readings, target bands, and eval-program references only when the current receiving use needs them; add a selected `BoundedModelUseStructure` only when it independently changes interpretation of the row use.

```text
ArchitectureCharacteristicCriteriaSet@Project:
  projectWorkOccurrenceRef?: U.EntityRef constrained to U.Work
  architectureCriteriaProjectUseRelationRef?: U.RelationRef governed by the exact criteria-use or work-use pattern
  describedHolonRef:
  architectureUseRef:
  holonFamilyStarterPackRef?:
  sourceCatalogueRefs?:
  draftProjectCriteriaRows:
    - architectureCharacteristicRef:
      sourceHeadOrStarterPackRef?:
      bearerOrSelectedStructureRefs:
      rowClaimScopeRef: U.EntityRef referencing one U.ClaimScope
      selectedContextSliceRefs:
      modelUseStructureRef?:
      effectiveReferenceScheme:
      referencePlane?:
      qualificationOrEvaluationWindow:
      endpointShape: singleCharacteristic | qBundle | qBundleSlot | sourceVocabularyOnly
      qBundleRef?:
      architectureQuestion:
      scaleFormRef:
      polarity:
      useClass: optimizationIndicator | monitoredGuardrail | contextOnly
      currentReadingRef?:
      targetBandOrStopCondition?:
      readingMethodRefOrNoReadingReason:
      evalProgramRefs?:
      proxyRisk:
      protectedCounterCharacteristicRefs:
      receivingUseRef:
      sourceReturnCondition:
  optimizationIndicatorRowRefs:
  monitoredGuardrailRowRefs:
  contextOnlyRowRefs?:
  improvementCycleRef?:
  reopenCondition:
```

For `ArchitectureCharacteristicCriteriaSet@Project` and `ArchitectureCharacteristicImprovementRow@Project`, `@Project` is a compatibility and retrieval cue only; it establishes no project entity, composite-work identity, context, authority, viewpoint, or parthood. A criteria set or improvement row local to one actual project names both the exact composite `U.Work` in `projectWorkOccurrenceRef` and the obtaining direct use relation for that exact record in `architectureCriteriaProjectUseRelationRef`; either field alone is insufficient, and a relation occurrence about the set is not silently reused for a distinct row. Otherwise the record remains retrieval-only and no project locality is asserted.

`draftProjectCriteriaRows` are draft project criteria rows. They are not candidate architectures, selected architectures, or a selected set returned by `A.19.SelectorMechanism`.

What goes wrong if C.32.ACS is missed: the team says that the architecture should be more maintainable, scalable, modular, safe, or evolvable, but no one can say which selected structures carry the characteristic, which few rows are criteria for the next optimization, which rows only guard against loss, which C.25 Q-Bundle is involved, or which eval result can reopen synthesis.

What C.32.ACS buys in practice: the practitioner can reduce broad catalogue and starter-pack material to draft project criteria rows, then to three to five optimization indicators, while keeping other important characteristics as monitored guardrails against Goodhart-style proxy loss.

Adoption test: after using C.32.ACS, the project can name the few rows that drive optimization, the guardrail rows that protect against loss, and the bearer, scale, proxy risk, receiving use, and reopen condition for each live row.

Not this pattern when the current work is choosing the holon-family starter pack, modeling a Q-Bundle, validating a measurement method, designing an eval program, synthesizing candidates, comparing or selecting candidates, choosing locally, declaring a selected-set result, publishing it to an audience, or deciding the project architecture.

Common exits by claim kind:

- `C.32.HCS` for holon-family starter packs.
- `C.25` for Q-Bundles and composite quality families.
- `C.16` for measurement templates, readings, units, thresholds, or comparability claims.
- `C.32.ACE` for eval-program framing and typed-result classification over declared rows; obtain each actual result separately under the pattern that defines and tests its kind and exact predicate or constraint.
- `E.13` when an indicator, score, or dashboard starts replacing the declared architecture concern.
- `E.22` and `E.23` for improvement-question framing and repeated improvement method.
- `C.32` for candidate synthesis and `C.32.MLAO` for residual-reducing candidates.
- `A.19.CPM` for explicit comparison, `A.19.SelectorMechanism` for set-returning selection, `C.11` for local choice, and `G.5` for selected-set result declaration. For publication, use `E.17` for a source-backed face and source return and `E.24.PUB` for the publication occurrence and audience availability.
- `A.10` for source recovery and bounded reliance, `G.6` when an addressable provenance path is needed, and `B.3` for an actual named assurance claim; use the direct pattern that defines or tests any additional evidence or validity claim.
- `C.32.PAD` for project decision.

## C.32.ACS:2 - Problem {#problem}

Architecture synthesis needs criteria. A multi-criteria or multilevel optimization phrase is empty until the criteria are named. In C.32-family work, those criteria are admitted architecture-characteristic rows or declared C.25 Q-Bundle slots of the described holon, each bound to its exact bearer, `U.ClaimScope`, relevant A.2.6 `U.ContextSlice` membership, effective reference scheme and plane, qualification or evaluation window, and receiving use. A broad domain or bounded-context label supplies none of those bindings.

Architecture characteristics are not the same as user functions. Functional demand says what the holon must do. An architecture characteristic says whether the selected structures make that demand maintainable, controllable, replaceable, observable, evolvable, scalable, affordable, safe enough, or otherwise acceptable.

Source catalogues and textbooks can offer hundreds of possible quality or architecture terms. A project may inspect dozens. The actual optimization loop should normally use only a few indicatorized rows, often three to five. Other important rows remain monitored guardrails or context-only rows so that optimizing one visible measure does not damage functional adequacy, safety, evidence, maintainability, or another protected architecture concern.

C.32.ACS supplies the project criteria set and scale rows. It does not create the holon-family starter pack, define a Q-Bundle, validate a measurement method, run an eval, compare candidates, choose an architecture, or decide the project architecture.

## C.32.ACS:3 - Forces {#forces}

| Force | Tension |
|---|---|
| Catalogue breadth vs project attention | Many quality names are available, but a project needs a small criteria set for the next improvement cycle. |
| Holon recurrence vs bearer rebinding | Characteristic heads can recur across holon families or declared holon levels, but each project row must bind the project bearer and scale. |
| Optimization indicator vs guardrail | A row can drive optimization, protect against loss, or only provide context. These uses must not collapse. |
| Architecture characteristic vs function | Functional adequacy constrains synthesis, but functional characteristics are not architecture criteria by name. |
| Q-Bundle richness vs row use | Composite quality families belong to C.25, while ACS admits rows or slots for architecture work. |
| Eval program vs criterion | An eval program can read or compare rows, but it is not the row and not the project criterion. |

## C.32.ACS:4 - Solution {#solution}

Build an `ArchitectureCharacteristicCriteriaSet@Project` from starter heads, source catalogues, architecture constraints, and the project improvement question.

### C.32.ACS:4.1 - Kind settlement {#kind-settlement}

`ArchitectureCharacteristicCriteriaSet@Project` is a C.32.ACS-local project working record: it holds criteria-row references and use classifications for improvement work. Each `draftProjectCriteriaRows` entry is another local record form, not the referenced `U.Characteristic`, Q-Bundle slot, scale, predicate, measurement result, eval program, or eval result. The set and rows create no new `U.*` kind and replace none of those direct objects.

An architecture characteristic is the property or quality-like head under discussion. A C.25 Q-Bundle is the structured form for a composite quality family. A scale row binds one characteristic or Q-Bundle slot to a bearer, scale form, use class, and receiving use. A row whose scale form exposes exception growth, interface variation, or another scale-sensitive characteristic remains a criterion row; a preference between architecture alternatives over a declared scale window is a separate `C.31.ASAP` claim. An architecture-characteristic eval program belongs to `C.32.ACE`; it frames evaluation of one declared row, coupled rows, Q-Bundle slots, or C.32 candidate palettes while each actual typed result remains under the pattern that defines and tests that result.

### C.32.ACS:4.2 - Criteria-set construction {#criteria-set-construction}

Work in this order:

1. Name the described holon, architecture use, and improvement cycle or one-pass eval use. For every proposed row, bind the exact claim scope and selected context slices, effective reference scheme and plane, and qualification or evaluation window. Designate a selected A.1.1 `BoundedModelUseStructure` only when it independently changes that row's interpretation.
2. Start from a `C.32.HCS` starter pack when the project has no draft criteria rows yet. Use source catalogues only as input, not as the criteria set.
3. Build draft project criteria rows. There may be dozens of draft rows when broad scanning is needed, but each row must have a possible bearer, use reason, and pattern for the next question.
4. For each source or starter head, decide whether it is one architecture characteristic, one C.25 Q-Bundle, one Q-Bundle slot, or only source vocabulary.
5. Narrow the optimization-indicator core. The ordinary target is three to five rows. More rows require an explicit reason, such as a regulated trade-off study or a multi-team decision use.
6. Classify remaining admitted rows as `monitoredGuardrail` or `contextOnly`. A guardrail protects against a loss caused by optimizing another row; a context-only row helps interpretation but does not drive optimization now.
7. Bind each admitted row to bearer or selected structure, scale form, polarity, current reading or no-reading reason, proxy risk, protected counter-characteristics, receiving use, and source-return condition.
8. Reference `C.32.ACE` only after the row exists and an eval program is needed for current characterization, candidate comparison, monitoring, or preparing inputs for `A.19.SelectorMechanism`.
9. Reopen the criteria set when the holon family changes, a B.2 whole reidentification changes the bearer, a guardrail degrades, an eval program no longer fits its declared parity frame, or the source-currentness relation changes the acceptable trade-off.

### C.32.ACS:4.3 - Row use classes {#row-use-classes}

Use `optimizationIndicator` only when the row can responsibly guide architecture changes now. A project normally carries only three to five such rows.

Use `monitoredGuardrail` when the row protects against a loss caused by optimizing another row. Guardrails can have readings and eval results, but they do not define the cycle's optimization direction.

Use `contextOnly` when the row helps interpretation but should not drive improvement, comparison, or selection in the current cycle.

**Stop condition.** Stop C.32.ACS when the criteria set names draft rows, use class, bearer or selected structure, scale form, proxy risk, protected counter-characteristics, receiving use, source-return condition, and any C.32.ACE or Q-Bundle reference that the current use actually needs.

**Lowering condition.** Lower an `optimizationIndicator` to `monitoredGuardrail` or `contextOnly` when it no longer guides the next architecture change or its proxy risk is not controlled. Lower a draft row to source vocabulary when bearer, scale form, use reason, receiving use, or protected counter-characteristics are missing. Use `C.32.HCS` when the holon-family starting point is wrong, `C.25` when the row is really composite, and the named pattern for the next question when measurement, eval, comparison, publication, local choice, evidence, assurance, or decision work is current.

### C.32.ACS:4.4 - Improvement-cycle use {#improvement-cycle-use}

When a row is used inside an improvement cycle, add:

```text
ArchitectureCharacteristicImprovementRow@Project:
  projectWorkOccurrenceRef?: U.EntityRef constrained to U.Work
  architectureCriteriaProjectUseRelationRef?: U.RelationRef governed by the exact improvement-row-use or work-use pattern
  criteriaRowRef:
  rowClaimScopeRef: U.EntityRef referencing one U.ClaimScope
  selectedContextSliceRefs:
  modelUseStructureRef?:
  effectiveReferenceScheme:
  referencePlane?:
  qualificationOrEvaluationWindow:
  useClass:
  currentArchitectureReadingRefOrQualitativeState:
  evalResultRefs?:
  intendedArchitectureChangeDirection:
  candidateSelectedStructureChangeRefs?:
  expectedGain:
  protectedLosses:
  observedReadingAfterChange?:
  nextSynthesisTrigger?:
  stopContinueOrSourceReturnCondition:
```

The row prepares improvement work. It does not carry a claim outside its declared scale and use. A reading or other typed eval result over a declared row retains its result kind and conditions; another pattern may use it as source material for bounded claim reliance under A.10, improvement feedback, comparison input, selection input, or decision input only when that pattern for the next question is named by value. It does not become the characteristic, the declared architecture concern, the architecture choice, or the optimization direction.

## C.32.ACS:7 - Conformance requirements {#conformance-requirements}

| Requirement | Required result |
|---|---|
| `CC-ACS-1` | @fact:CC-ACS-1 The criteria set names the described holon, architecture use, and receiving use; every row names its exact `U.ClaimScope`, relevant A.2.6 `U.ContextSlice` membership, effective reference scheme and plane, and qualification or evaluation window. @status:spec/done |
| `CC-ACS-2` | @fact:CC-ACS-2 Source catalogue, HCS starter pack, draft project criteria rows, optimization indicators, monitored guardrails, and context-only rows remain distinct. @status:spec/done |
| `CC-ACS-3` | @fact:CC-ACS-3 The ordinary optimization core is three to five rows, or the text states why more are needed. @status:spec/done |
| `CC-ACS-4` | @fact:CC-ACS-4 Each row names a bearer or selected structure. A characteristic without a bearer is not admitted as an architecture criteria row. @status:spec/done |
| `CC-ACS-5` | @fact:CC-ACS-5 User function, architecture characteristic, Q-Bundle, scale row, reading, eval program, and eval result remain separate. @status:spec/done |
| `CC-ACS-6` | @fact:CC-ACS-6 Any composite quality family belongs to `C.25`; ACS may reference the Q-Bundle or one declared slot. @status:spec/done |
| `CC-ACS-7` | @fact:CC-ACS-7 Each optimization row names proxy risk and protected counter-characteristics before it is used in C.32, C.32.MLAO, C.32.ACE, or E.23. @status:spec/done |
| `CC-ACS-8` | @fact:CC-ACS-8 Eval-program construction belongs to `C.32.ACE`; eval programs are not used as criteria rows. @status:spec/done |
| `CC-ACS-9` | @fact:CC-ACS-9 The criteria set does not compare, select, publish, decide, certify, or carry an architecture-adequacy claim by itself. @status:spec/done |
| `CC-ACS-10` | @fact:CC-ACS-10 A project-local criteria set or improvement row names both `projectWorkOccurrenceRef` and the obtaining `architectureCriteriaProjectUseRelationRef` for that exact record; the suffix or either reference alone asserts no locality. @status:spec/done |
| `CC-ACS-11` | @fact:CC-ACS-11 A criteria row remains distinct from its referenced characteristic or Q-Bundle slot, scale, predicate, measurement result, eval program, eval result, and receiving decision object. @status:spec/done |
| `CC-ACS-12` | @fact:CC-ACS-12 `modelUseStructureRef` appears only when an independently selected `BoundedModelUseStructure` changes the row interpretation; it never replaces row claim scope or context-slice membership. @status:spec/done |
| `CC-ACS-13` | @fact:CC-ACS-13 A scale-sensitive ACS row names the exact characteristic or Q-Bundle slot, bearer, scale form, and use class; any preference between alternatives over a scale window is separately governed by `C.31.ASAP`. @status:spec/done |

## C.32.ACS:9 - Consequences {#consequences}

| Consequence | Benefit | Cost |
|---|---|---|
| Architecture optimization gets declared criteria. | C.32 and C.32.MLAO can use multi-criteria language without unnamed criteria. | The project must admit and type rows before synthesis or optimization claims. |
| The 300-to-3 problem is handled by staged admission. | Broad catalogues inform the project without serving as the project criteria set. | Some familiar qualities must be guardrails or context rows. |
| Anti-Goodhart guardrails are explicit. | Optimization can protect functional adequacy and other architecture concerns. | A single convenient score cannot govern choice by itself. |
| Measurement and eval stay clean. | C.16 and ACE keep readings, eval programs, and eval results separate from criteria. | Some eval programs require additional receiving-pattern work before they can drive action. |
| Q-Bundle structure stays clean. | Composite quality families keep their C.25 structure. | ACS cannot shortcut a composite family into one scalar row. |

## C.32.ACS:12 - Relations {#relations}

- **Builds on:** `C.32.HCS`, `A.17`, `A.18`, `A.2.6`, `A.19`, `C.16`, `C.16.P`, `C.25`, `C.30`, `C.30.P`, `C.31`, `C.31.ASAP`, `E.13`, `E.22`, and `E.23`; uses A.1.1 only when a selected `BoundedModelUseStructure` changes one row's interpretation.
- **Receiving uses:** `C.32.P2S` problem-to-structure architecturing flow, `C.32` candidate synthesis, `C.32.MLAO` multilevel residual work, `C.32.CONWAY` correspondence frames, `C.32.FAIL` repair cues, `C.32.ACE` eval programs, `A.19.CPM` comparison inputs, `A.19.SelectorMechanism` selection inputs, `C.11` local choice inputs, inputs for selected-set result declaration under `G.5`, source-backed publication-face and source-return inputs under `E.17`, publication-occurrence and audience-availability inputs under `E.24.PUB`, and architecture-decision inputs for `C.32.PAD`.
- **Starter-pack boundary:** Use `C.32.HCS` when the project needs a holon-family starting set before criteria rows exist.
- **Q-Bundle boundary:** Use `C.25` when the architecture characteristic is really a composite quality family with several measures, scope slots, mechanisms, statuses, qualification windows, or evidence.
- **Scale-preference boundary:** Use `C.31.ASAP` when a project claims that one architecture alternative is preferable over another under a declared scale window; the ACS row supplies a criterion, not that preference.
- **Eval boundary:** Use `C.32.ACE` when a project wants eval-program framing over declared rows, Q-Bundle slots, candidates, or selected-structure changes; state each actual typed result separately under the pattern that defines and tests its kind and exact predicate or constraint.
- **Measurement boundary:** Use `C.16` when a reading, coordinate, unit, threshold, score, or cross-case comparability claim is made.
- **Structural-information boundary:** Use `C.33` or `C.34` when the issue is captured structure, lost structure, or preservation adequacy before a criterion row exists. Use C.32.ACS only when that structural-information or preservation concern becomes a declared architecture-characteristic criterion row. Use `C.35` only for kind restoration and architecture-use adequacy of a generated or discovered result before C.32 or ACS uses a criteria-bearing claim based on that result.
- **Proxy boundary:** Use `E.13` when an optimization indicator, score, eval result, or dashboard state begins to replace the declared architecture concern.
- **Synthesis boundary:** Use `C.32` after criteria rows exist and the next useful work is to synthesize candidate selected-structure changes.
- **Decision and publication boundary:** Use `A.19.CPM` for comparison, `A.19.SelectorMechanism` for selection, `C.11` for choice, `G.5` for selected-set result declaration, and `C.32.PAD` for an architecture decision. For publication, use `E.17` for a source-backed face and source return and `E.24.PUB` for the publication occurrence and audience availability.


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/C-32-HCS#root, spec://ai.lev/fpf-spec/contract/C-25#root, spec://ai.lev/fpf-spec/contract/C-16#root, spec://ai.lev/fpf-spec/contract/E-13#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/C-32#root, spec://ai.lev/fpf-spec/contract/C-32-ACE#root, spec://ai.lev/fpf-spec/contract/C-32-PAD#root, spec://ai.lev/fpf-spec/contract/E-22#root, spec://ai.lev/fpf-spec/contract/E-23#root, spec://ai.lev/fpf-spec/contract/A-19-CPM#root, spec://ai.lev/fpf-spec/contract/G-5#root, spec://ai.lev/fpf-spec/contract/C-11#root, spec://ai.lev/fpf-spec/contract/A-10#root, spec://ai.lev/fpf-spec/contract/B-3#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/C-32#root, spec://ai.lev/fpf-spec/contract/C-32-ACE#root, spec://ai.lev/fpf-spec/contract/C-32-ADA#root, spec://ai.lev/fpf-spec/contract/C-32-CONWAY#root, spec://ai.lev/fpf-spec/contract/C-32-HCS#root, spec://ai.lev/fpf-spec/contract/C-32-MLAO#root, spec://ai.lev/fpf-spec/contract/C-32-PAD#root, spec://ai.lev/fpf-spec/contract/C-35#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/C-32-ACS
