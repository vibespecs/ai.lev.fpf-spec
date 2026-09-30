# C.22.PFR - Problematic-For Relation {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Conceptual (C)
> **Status:** Stable
> **Normativity:** Normative unless marked informative

**Plain name.** Actual problem.

## C.22.PFR:1 - Problem frame {#problem-frame}

**Use this when.** Use this pattern when an actual condition may be adverse for one exact entity and use, and a receiving claim needs to distinguish the actual Problem from a signal, criterion description, evaluation, assessment claim, ProblemCard, or claim that no suitable method is currently known.

**First useful move.** Name the actual-condition relation. Then name the exact predicate, entity, scope, and interval for which that predicate applies. If the condition falls on the adverse side of that applicable predicate, say plainly: "This condition is a problem for this entity in this scope." Expose a PFR occurrence only when another claim needs that Problem identity.

**What goes wrong if missed.** A card or evaluation result is allowed to create a Problem; the same criterion is applied to the wrong entity or scope; a new description edition creates a false new Problem; or one continuously adverse episode is split every time evidence is sampled. Conversely, two adverse episodes separated by actual non-adverse behavior collapse into one occurrence.

**What this buys.** Actual Problems can exist before discovery, can be referenced while still ongoing, and can be distinguished across repeated adverse episodes. One exact applicability relation supplies the predicate, problem-for entity, claim scope, and declared criterion-applicability window used by PFR; its actual occurrence extent is separately derived from uninterrupted obtaining. Measurements, evaluations, evidence, claims, cards, and method search remain available without becoming Problem identity.

**Early battery stop.** A low terminal-voltage reading can be a useful signal and can justify a `ProblemCard`, but it is not itself the actual-condition participant. Until a direct voltage-state pattern supplies the exact relation kind, participant meanings, obtaining rule, temporal extent, recurrence, and occurrence identity, the battery case remains explicitly non-conforming: the reading, alarm, report, assertion, and card establish none of that world-side relation. Once such a governor exists, the applicability relation can connect its selected voltage predicate to the exact vehicle, intended-start `U.ClaimScope`, and declared criterion-applicability window; discovering a method still changes solvability rather than PFR actuality.

**Not this pattern when.** Use `C.22.2` when the current object is a problem-side card, signal, hypothesis, forecast, scenario, anticipated-condition claim, or reviewable formulation rather than an actual PFR. Use `C.27` when a rate, rhythm, recovery, or regime claim is being used to change action, `C.28` when causal support is at issue, or the exact direct forecast, scenario, counterfactual, or anticipated-condition governor when that claim is current. Use the selected A.19 comparison, `G.4` acceptance, state, gate, or measurement pattern when the current question is how to evaluate or support the adverse predicate. Use `E.18.1`, `E.23`, and the direct NQD or OEE patterns for repeated problematization, search, work, evaluation, and continuation.

## C.22.PFR:2 - Problem {#problem}

An actual Problem is neither a record nor a free-standing quality label. It depends on an actual condition and on a criterion that applies to one exact entity, scope, and interval. The relation obtains when the condition is on the adverse side of that applicable predicate.

FPF needs one identity for this dependent evaluative relation without copying values defined by `ProblemCriterionApplicabilityRelation` into additional writable PFR slots. It also needs to distinguish continuous adverse episodes from repeated episodes while refusing to infer a recovery from missing observations or evidence.

## C.22.PFR:3 - Forces {#forces}

| Force | Tension |
|---|---|
| Actuality vs discoverability | A Problem can obtain before anyone evaluates, notices, describes, or publishes it. |
| Readable problem talk vs typed dependence | Practitioners need a direct sentence, while load-bearing use needs exact condition and applicability occurrences. |
| One applicability relation vs duplicated participants | Predicate, problem-for entity, claim scope, and declared criterion-applicability window are useful independently of PFR but must not be writable both as applicability-relation participants and as PFR participants; the applicability occurrence extent remains derived. |
| Continuous identity vs repeated episodes | One adverse episode may receive many assessments; the same participants may also stand in later adverse episodes after a real recovery. |
| Open episode use vs final interval | Current work needs to reference a Problem before the adverse episode has ended. |
| Predicate truth vs epistemic support | Evaluation and evidence support claims about adverse truth but do not make the world-side dependent relation obtain. |
| Solvability vs Problem actuality | Finding a method changes what can be done, not whether the current condition remains adverse. |
| Anticipated-condition claim vs actual occurrence | A useful forecast, scenario, or hazard card can describe a possible condition before any actual-condition relation obtains. |

## C.22.PFR:4 - Solution {#solution}

Model an actual Problem as one obtaining `ProblematicForRelation`, a dependent evaluative `U.Relation` between exactly two relation occurrences: the actual condition and the applicability of a characteristic-space predicate.

### C.22.PFR:4.1 - Use one exact criterion-applicability relation {#use-one-exact-criterion-applicability-relation}

`CharacteristicSpacePredicate` is a by-value predicate used by an A.19 comparison, acceptance, state, gate, or other direct consumer. It is not a new U-kind, publication record, description edition, or comparison result. Its meaning is recoverable from the declared characteristic-space coordinates, scales, normalization or bridge values, operator, cut or band, polarity, and the selected direct consumer's governed comparator, admissibility, and predicate-use semantics. A separately performed evaluation remains `U.Work`; its result episteme and evidential-support relations remain separately governed, and none of these constitutes predicate meaning.

Before testing adversity, answer three plain questions: **what exact point or value does this condition supply, how is that point obtained, and why is it the input for this problem-for entity and use?** The by-value predicate therefore carries one `ConditionToPredicateInputRule` as part of its own semantics, not as another PFR participant:

- **Direct input:** the actual-condition participant is already a governed characteristic-assignment or state relation whose subject pattern exposes the exact characteristic-space coordinate, scale, and value used by the predicate.
- **Projected input:** when that relation does not itself expose the needed point, the rule cites one exact governed projection or bridge, its source relation kind and participant positions, target characteristic space, coordinate and scale, and the direct relation or predicate connecting that input to the problem-for entity and receiving use.

A relation reference alone is not a coordinate. If neither path yields the exact point and the problem-for link, adverse truth and PFR remain unestablished. When two projections are plausible, the rule names the selected one; identify the nearest inadmissible alternative only when one fails the declared input or problem-for-link conditions. `ConditionToPredicateInputRule` is a pattern-local by-value rule inside `CharacteristicSpacePredicate`; it is not a U-kind, relation occurrence, evaluation result, or copied PFR field.

**Public name settlement.** The following F.18 NameCard names the applicability relation kind.

```text
NameCard:
  NameCardId: NC-PROBLEM-CRITERION-APPLICABILITY-RELATION
  GovernedValueRef: ProblemCriterionApplicabilityRelation under C.22.PFR
  SubjectPatternLocator: C.22.PFR
  ReferenceScheme: FPFCoreReferenceScheme
  LocalSenseRef: obtaining relation saying that one characteristic-space predicate currently governs one exact problem-for entity and claim scope under one declared criterion-applicability window, independently of whether an actual condition presently satisfies the adverse predicate; repeated occurrences with the same four participants are distinguished by maximal continuous actual applicability
  TechLabel: ProblemCriterionApplicabilityRelation
  PlainLabel: problem-criterion applicability
  CandidateSet: ProblemCriterionApplicabilityRelation; CriterionApplicabilityRelation; ProblemCriterionUseRelation; ApplicableProblemCriterion
  RejectedCandidates: CriterionApplicabilityRelation overclaims a universal criterion ontology; ProblemCriterionUseRelation hides obtaining applicability behind use wording; ApplicableProblemCriterion turns a relation into an adjective-headed value
  SelectionRationale: preserve distinct applicability occurrences for different exact entities, scopes, or declared windows and after actual loss and restoration of applicability, without making a predicate-description edition identity-bearing
  PublicRowStatus: pending
  LineageEntries: replaces description-edition and generic criterion-use identity proposals
  RefreshCondition: reopen if the four fixed participants plus maximal continuous actual applicability cannot distinguish applicability occurrences, or if the direct rule no longer separates criterion governance from adverse-condition satisfaction
```

Use one individuable dependent `U.Relation` for applicability:

```text
ProblemCriterionApplicabilityRelation:
  ProblemCriterionPredicateSlot: CharacteristicSpacePredicate, byValue
  ProblemForEntitySlot: U.Entity, byRef with an exact local ValueKind
  PredicateClaimScopeSlot: U.ClaimScope, byValue
  DeclaredCriterionApplicabilityWindowSlot: DeclaredCriterionApplicabilityWindow, byValue; use an explicit unbounded value when no finite bound is intended
```

This relation states that one exact predicate currently governs one exact entity and claim scope under one declared criterion-applicability window. Its direct applicability predicate is satisfied while that criterion remains selected and governing for that entity, scope, and window; it does not ask whether any actual condition is presently on the adverse side. The applicability occurrence can therefore continue across adverse, non-adverse, and later adverse condition intervals. It ceases when the criterion is withdrawn or replaced for that use, the entity or claim scope changes, the declared window no longer covers the use, or another direct applicability condition fails. One occurrence is identified by the four fixed participants plus the maximal continuous period of actual applicability. Changing a participant yields another occurrence; actual loss and later restoration of applicability yields distinct occurrences even when all four participants stay fixed. A coextensional description edition or carrier change does not change either the predicate participant or the occurrence. Assessment windows, evidence-relevance intervals, description editions, claim-currentness windows, and adverse-truth intervals remain with their own claims and relations.

A semantic predicate change selects a different predicate participant; it is not an edition-only repair. If the new predicate replaces the old predicate for the same use and the old applicability therefore ceases, the old applicability occurrence ends and a new occurrence begins only if the new predicate actually applies. The PFR dependent on the old occurrence can then end, and another PFR can begin under the new occurrence when adverse truth obtains. If both predicates remain applicable, two applicability occurrences may coexist; a new criterion description alone does not prove replacement or cessation.

### C.22.PFR:4.2 - Keep the PFR signature reduced to two participants {#keep-the-pfr-signature-reduced-to-two-participants}

**Public name settlement.** The following F.18 NameCard names the actual dependent evaluative relation kind.

```text
NameCard:
  NameCardId: NC-PROBLEMATIC-FOR-RELATION
  GovernedValueRef: ProblematicForRelation under C.22.PFR
  SubjectPatternLocator: C.22.PFR
  ReferenceScheme: FPFCoreReferenceScheme
  LocalSenseRef: actual dependent evaluative relation with one actual-condition relation occurrence and one problem-criterion-applicability relation occurrence as its only non-derived participants, individuated by those participants plus the actual inception of each maximal continuous adverse episode
  TechLabel: ProblematicForRelation
  PlainLabel: actual problem
  CandidateSet: ProblematicForRelation; AdverseCriterionAssessmentRelation; ProblemUseRelation; ProblemRelation; ProblemSituationRelation
  RejectedCandidates: AdverseCriterionAssessmentRelation omits the problem-for relation; ProblemUseRelation hides the actual adverse condition; ProblemRelation hides criterion applicability; ProblemSituationRelation falsely requires situation
  SelectionRationale: make ordinary Problem recoverable without copying applicability participants and distinguish repeated adverse episodes without requiring a universal adverse-evaluation relation occurrence
  PublicRowStatus: pending
  LineageEntries: situation-first, card-as-world, bearer-duplicating, and description-edition identity proposals retired
  RefreshCondition: reopen if participant references plus actual adverse inception cannot keep one stable occurrence reference through closure or distinguish later adverse episodes, or if the predicate's condition-to-input rule no longer yields one unambiguous characteristic point and problem-for link
```

**No-mint disposition for root `U.Problem`.** Do not introduce a second problem entity beside the obtaining `ProblematicForRelation` occurrence. That occurrence is the actual Problem; a `ProblemCard`, criterion description, assessment claim, or local Plain label may describe or designate it but does not supply another world-side identity.

The complete non-derived participant set is:

```text
ProblematicForRelation:
  ActualConditionRelationSlot: U.Relation, byRef
  ProblemCriterionApplicabilityRelationSlot: U.Relation, byRef
```

The first reference resolves to the exact obtaining relation that constitutes the actual condition under its direct pattern. The second resolves to the exact obtaining applicability relation from C.22.PFR:4.1.

PFR has no separately writable condition-bearer, predicate, problem-for-entity, claim-scope, applicability-window, assessment-window, or description-edition slot. The actual-condition relation fixes its condition participants, and the applicability relation fixes the predicate, problem-for entity, claim scope, and declared applicability window. Assessment windows and description editions remain with their own claims. A readable claim projects the applicability values from that participant:

```text
PFR.problemCriterionPredicate
  := PFR.problemCriterionApplicabilityRelation.problemCriterionPredicate
PFR.problemForEntity
  := PFR.problemCriterionApplicabilityRelation.problemForEntity
PFR.predicateClaimScope
  := PFR.problemCriterionApplicabilityRelation.predicateClaimScope
PFR.declaredCriterionApplicabilityWindow
  := PFR.problemCriterionApplicabilityRelation.declaredCriterionApplicabilityWindow
PFR.problemCriterionApplicabilityExtent
  := maximal continuous obtaining extent of PFR.problemCriterionApplicabilityRelation
```

This is a derivation from one participant, not a consistency check between copies.

### C.22.PFR:4.3 - Use predicate truth as the obtaining condition {#use-predicate-truth-as-the-obtaining-condition}

`ProblematicForRelation` obtains exactly when all three conditions hold:

1. The exact `ActualConditionRelation` obtains under its direct pattern.
2. The exact `ProblemCriterionApplicabilityRelation` obtains because its criterion remains governing for the exact entity and claim scope under the declared criterion-applicability window, independently of whether the actual condition is adverse.
3. For the actual-condition participant, the predicate's exact `ConditionToPredicateInputRule` must yield the declared characteristic-space point or value and the direct link to the problem-for entity and use; that point falls on the adverse side under the selected scale, comparator, cut or band, polarity, and admissibility semantics.

The selected direct consumer supplies the governed input projection or consumes the direct characteristic assignment, then governs the comparator and admissibility semantics. An evaluation may calculate or support a claim that the resulting point is adverse. Comparison outcomes, acceptance outcomes, state or gate results, measurements, evidence, and assessment claims are not automatically PFR participants, and producing them does not make PFR obtain.

A Problem can therefore obtain unnoticed. Later detection can involve work, evidence, and claims about the already obtaining relation; it does not create retroactive actuality.

When evaluation is actually performed, recover every exact actual performer `U.System` through A.13, independently admit the dated evaluation `U.Work` under A.15.1, and name the `U.Method` actually followed. Name any declared A.6.1 operation application separately when its returned-value binding is claimed. Add F.6 only when the evaluation account or a receiving use expressly consumes precise assignment-bound attribution through the same obtaining A.13 assignment; missing or failed F.6 leaves the evaluation Work intact. A short PFR explanation may omit an assignment identifier that no later claim uses. That Work may return the separate evaluation result `true`, `false`, or `unknown` defined by the selected evaluation pattern; a C.2.1 assertion may state the result. A.10 governs evidence use for reliance on that assertion, B.3 governs any named assurance claim, and G.11 may qualify the assertion's current edition. The practitioner may rely on the assertion for the receiving Work, decline or defer that reliance, or reopen its basis. `unknown` is an evaluation result, never a world-side PFR value; test PFR obtaining through the three conditions in §4.3.


### C.22.PFR:4.4 - Identify repeated adverse episodes from world-side continuity {#identify-repeated-adverse-episodes-from-world-side-continuity}

The direct occurrence rule is ontic. With the two participant occurrences fixed, one PFR occurrence is the maximal continuous episode during which both participants obtain and the selected condition point is actually on the adverse side. Actual cessation of either participant or actual movement to the non-adverse side ends that occurrence. Later renewed adverse truth starts a later PFR occurrence. Measurement, evaluation, demonstration, assessment, and evidence availability neither start nor end either occurrence.

Use this world-side identity basis:

```text
<actualConditionRelationRef,
 problemCriterionApplicabilityRelationRef,
 adverseEpisodeStart>
```

`adverseEpisodeStart` is the episode's actual inception under the declared temporal reference, not the first observation or report time. When admitted time grain cannot distinguish co-inceptions, or when a receiving history must keep one reference while a claim about inception remains revisable, explicitly individuate the occurrence under A.6.REL and assign a stable `pfrOccurrenceId` that designates it. The resolution record may carry the current boundary claim, but neither its asserted start nor its asserted end becomes a mutable identifier field. The PFR's `actualAdverseExtent` is derived from the world-side episode: its end becomes fixed when the episode actually ceases, and a later claim may recover or correct that boundary. The recovered end and completed extent describe the occurrence; they do not replace it or change its assigned reference. This applies A.6.REL's participant-plus-episode rule without making a currently known boundary constitutive.

Participant references alone remain insufficient because the same participants can enter adverse, non-adverse, and later adverse episodes. A universal evaluation reference is also insufficient because an unnoticed PFR can obtain and several assessments can support one occurrence.

### C.22.PFR:4.5 - Keep world-side occurrence and current boundary claim separate {#keep-world-side-occurrence-and-current-boundary-claim-separate}

Use `[adverseEpisodeStart, open]` only in a current claim whose evidence supports that this same PFR occurrence still obtains at the claim's stated reference time. `open` is a claim-side endpoint sentinel, not the clock time, an identity field, or a substitute for missing evidence. The stable occurrence reference remains unchanged when a later claim records the recovered actual end.

A current assertion or description distinguishes three cases in ordinary words:

- **supported current:** the evidence supports continuous adverse obtaining from the episode's actual inception through the stated reference time; publish `[adverseEpisodeStart, open]`;
- **supported closed:** the evidence supports actual cessation at an exact boundary; publish `[adverseEpisodeStart, adverseEpisodeEnd]` for the same occurrence reference;
- **continuity unresolved:** the available evidence does not decide whether an unobserved cessation or restart occurred; retain the recoverable earlier occurrence reference and the supported segments, but assert neither one continuous occurrence nor two occurrences across the gap.

Later evidence may revise the assertion, including its claimed start, end, or continuity, without creating or changing the world-side episode. If it supports an earlier actual cessation, complete the extent of the earlier occurrence at that boundary. If it also supports later renewed adverse truth, identify the later occurrence from its own actual inception. Until that distinction is supported, do not attach the later adverse segment to either the old or a new occurrence by default.

Use the A-B-C regression while holding one continuously obtaining applicability occurrence fixed. The criterion remains governing for the same entity, scope, and declared window through A, B, and C; only world-side adverse truth changes:

- During A, the condition is actually adverse, so the first PFR obtains from `A.start` until its actual cessation at `A.end`.
- During B, the condition is actually non-adverse, so the first PFR does not obtain.
- During C, the condition is actually adverse again, so a later PFR begins at `C.start` with the same two participant references and a different stable occurrence reference.

Evidence that supports A, B, and C warrants the corresponding two-occurrence assertion. A missing assessment, unavailable measurement, stale evidence item, or support gap warrants `continuity unresolved`; it neither proves recovery nor licenses continuity. Adjacent or overlapping assessment windows likewise do not split or join world-side episodes by themselves.

### C.22.PFR:4.6 - Keep assertions, reliance, anticipated conditions, solvability, and cards separate {#keep-assertions-reliance-anticipated-conditions-solvability-and}

An assertion about the exact PFR obtaining predicate has affirmative or negative claim polarity. An affirmative assertion may designate an independently established occurrence; a negative assertion denies predicate satisfaction for the named participants and qualification but does not erase or reidentify an earlier occurrence. A.10 governs the evidence-use account for treating that assertion as supported, refuted, or unresolved in one receiving use; B.3 applies only when a named assurance claim is current. Assertion polarity, support, and reliance therefore answer different questions.

A possible or anticipated problem remains an exact forecast, scenario, counterfactual, or anticipated-condition claim in `ProblemCard` or another episteme until an actual-condition relation, an applicability relation, and adverse predicate truth all obtain. `C.2.1` governs its assertion identity and polarity. Use `C.27` when a rate, rhythm, recovery, or regime claim is being used to change action and `C.28` when causal support is at issue. The exact direct claim pattern defines or constrains assumptions, horizon, and non-actual semantics. None of those claim-side facts establishes a current PFR.

A `ProblemCard` is one C.2.1 episteme with one exact ClaimGraph, one independently identified `EntityOfConcern`, and one effective `U.ReferenceScheme`. It may carry claims designating several PFR occurrences only when those claims are jointly about that one EntityOfConcern under the direct pattern that identifies it. When two PFR references lack such a joint concern, split the ClaimGraph and card. Conversely, several cards may designate the same PFR through different ClaimGraphs, schemes, viewpoints, or receiving uses. Card count, merge or split, currentness, assessment window, publication, carrier, and edition change neither PFR actuality nor identity. C.22.2:20.1b replays all three branches with exact objects: two Robot-7 PFR episodes share one A.1-identified `Robot-7` and one card; Robot-7 and Robot-8 PFRs have no direct joint EntityOfConcern and force two ClaimGraphs and cards; and two differently qualified cards retain the unchanged `PFR-InspectionAssignment-17` reference.

A claim that no supported method is currently available concerns the admitted method set, evidence, constraints, and intended use. Selecting or discovering a method changes current solvability; it does not end PFR while the actual condition remains adverse. Performed repair work can end PFR only when an independently recovered actual change makes a participant cease or moves the selected condition point to the non-adverse side.

Repeated problematization, method search, work, evaluation, and continuation occur in work and transformation flows governed by `E.18.1` and `E.23`. A claim or plan may carry a reference to the same PFR while work and transformation occurrences participate in a selected transformation-flow structure. Neither that reference use nor any flow-structure relation enters PFR identity. A later PFR is a later occurrence because a participant changes or because actual adverse truth begins again after actual cessation, not because another card, assessment, or flow visit exists.

### C.22.PFR:4.7 - Preserve the lightweight path {#preserve-the-lightweight-path}

For a first use, name only what decides the case:

1. the exact obtaining condition and the value or point it supplies;
2. the criterion that makes that point adverse, including the selected input path and cut or band;
3. the entity for which it is a Problem, the use or claim scope, and the applicability window.

Then write one ordinary sentence:

> `<condition and value>` misses `<criterion>` for `<entity and use>` during `<applicability window>`; therefore it is an actual Problem for that entity and use.

Stop there when the next work only needs to recognize the Problem. Cite the direct condition and criterion patterns, but do not fill a PFR record, repeat either relation signature, or assign a PFR identifier. The NameCards and signatures above define reusable semantics; they are not a mandatory user form.

Add explicit identity only when another claim must compare, qualify, change, nest, plan from, or refer back to this particular Problem occurrence. That receiving claim then names the exact actual-condition occurrence, exact applicability occurrence, actual adverse inception or stable PFR identifier when needed, claimed extent, and any evidence or assessment claim on which its reliance depends. The evidence remains separate from the world-side Problem.

## C.22.PFR:7 - Conformance Checklist {#conformance-checklist}

1. The actual condition is an explicitly individuated obtaining `U.Relation` under its direct pattern.
2. `CharacteristicSpacePredicate` is given by value and includes one exact `ConditionToPredicateInputRule`: either a direct governed characteristic assignment/state relation or a named governed projection/bridge to the exact coordinate, scale, and problem-for link. A criterion-description identifier, arbitrary relation reference, or plausible alternative projection is insufficient.
3. `ProblemCriterionApplicabilityRelation` has the predicate, exact problem-for entity, claim scope, and declared criterion-applicability window as its four participants. It obtains while that criterion governs those participants, independently of adverse-condition satisfaction; its occurrence extent is the maximal continuous period of actual applicability.
4. PFR has exactly two non-derived participant slots: actual condition and criterion applicability.
5. Predicate, entity, scope, declared criterion-applicability window, and actual applicability-occurrence extent are projected from applicability rather than copied into PFR.
6. The selected direct consumer obtains the exact point through the declared direct assignment or projection and governs comparator, cuts or bands, polarity, admissibility, evaluation, and support; the condition relation is never treated as a coordinate by itself.
7. Evaluation work, outcomes, measurements, evidence, assessment claims, descriptions, and cards do not create or identify PFR by default.
8. Repeated PFR occurrences use the two participant references plus actual adverse inception. Add a stable occurrence identifier only for co-inceptions or a receiving history that must survive revision of the claimed inception boundary; the currently asserted start, derived end, and completed extent are not mutable key fields.
9. `[adverseEpisodeStart, open]` is used only by a claim that supports current continuous obtaining; a later supported end completes the claimed extent on the same stable occurrence reference.
10. Actual non-adverse B between actual adverse A and C yields two world-side PFR occurrences. Evidence can support, refute, or leave that boundary unresolved; a gap alone proves neither one occurrence nor two.
11. Method availability and solvability claims remain separate from PFR actuality and identity.
12. Possible conditions remain exact forecast, scenario, counterfactual, or anticipated-condition claims under their direct governors until both participant relations and adverse predicate truth obtain; assertion polarity and reliance posture do not substitute for those obtaining conditions.
13. Ordinary readable use can stop before explicit PFR materialization when no receiving claim needs Problem identity.
14. Battery-voltage, proof-gap, clinical-condition, missed-transfer, and hot-surface cases remain explicitly non-conforming until their named direct condition and, where applicable, problem-for/applicability governors exist; a phrase, measurement, diagnosis, record, card, or structural transfer does not mint them.

## C.22.PFR:9 - Consequences {#consequences}

**Benefits.** PFR gives actual Problems stable identity without turning cards or evaluations into world-side constituents. Two entities or scopes can use one predicate without collision, repeated adverse episodes remain distinguishable, and ongoing episodes can be referenced before closure. Unknown evidence remains epistemically honest.

**Costs.** A load-bearing use must recover a by-value predicate, its exact condition-to-input rule and problem-for link, and one exact applicability relation. Direct consumer patterns must state how the selected point is obtained and how adverse truth is evaluated, including comparator and polarity semantics. Temporal identity requires a real recovery boundary rather than assessment timestamps.

**Limits.** C.22.PFR does not define domain criteria, measurement methods, comparator semantics, acceptance policy, evidence sufficiency, method search, repair work, or problem-card publication. It governs only actual Problem obtaining, dependence, projection, and occurrence identity.

## C.22.PFR:12 - Relations {#relations}

- `A.6.REL` governs explicit individuation of both PFR participants and PFR itself when a receiving use needs identity.
- `A.6.RCD` governs each missing direct-condition or applicability relation decision; C.22.PFR keeps the affected case non-conforming until an existing direct predicate closes it or a separately admitted direct subject pattern supplies obtaining, recurrence, and occurrence identity.
- `A.6.5` governs the two PFR participant SlotSpecs and the four applicability SlotSpecs.
- `A.19` governs the characteristic space used by `CharacteristicSpacePredicate`; the selected direct consumer governs its condition-to-input rule and comparator semantics, `A.19.CPM` governs comparison when that is the consumer, and `G.4` governs typed acceptance clauses when acceptance is the consumer.
- `C.16`, `A.18`, and direct condition or measurement patterns define or constrain characteristics, scales, actual characteristic assignments or state relations, and measurements. F.9 governs any semantic Bridge named by the input rule; none of these adds a PFR participant.
- `C.22` governs selector-facing task typing and TaskSignature assignment after a problem-side episteme is usable.
- `C.22.2` governs ProblemCard claims, signals, forecasts, scenarios, anticipated-condition cues, descriptions, next use, and publication without creating PFR; the exact direct claim pattern defines or constrains each claim carried there.
- `A.15.1` and `A.3.4` govern repair work and changes to the actual-condition relation.
- `E.18.1`, `E.23`, and direct NQD and OEE patterns define or constrain repeated problematization, method search, work, evaluation, and continuation; relations locating or ordering those occurrences in a transformation-flow structure do not enter PFR identity.
- `C.27.TA` governs temporal aspect statements when interval publication or temporal adequacy is current.
- `A.10`, `B.3`, and `G.11` govern evidence use, assurance, and source or claim currentness.


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/A-6-REL#root, spec://ai.lev/fpf-spec/contract/A-6-5#root, spec://ai.lev/fpf-spec/contract/A-19#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/C-22#root, spec://ai.lev/fpf-spec/contract/C-22-2#root, spec://ai.lev/fpf-spec/contract/A-15-1#root, spec://ai.lev/fpf-spec/contract/A-3-4#root, spec://ai.lev/fpf-spec/contract/E-18-1#root, spec://ai.lev/fpf-spec/contract/E-23#root, spec://ai.lev/fpf-spec/contract/A-10#root, spec://ai.lev/fpf-spec/contract/B-3#root, spec://ai.lev/fpf-spec/contract/G-11#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/C-22-2#root, spec://ai.lev/fpf-spec/contract/E-24-CD#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/C-22-PFR
