# A.6.P.WMR - Exact Relation Recovery for Method and Work Claims {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Plain label:** recover the exact relation hidden by input, result, and handoff wording
> **Type:** Architectural precision-restoration pattern (A)
> **Status:** Stable
> **Normativity:** Normative unless explicitly marked informative
> **Specializes:** `A.6.P` Relational Precision Restoration

## A.6.P.WMR:1 - Problem Frame {#problem-frame}

**Use this when.** Practitioners **SHOULD** use this pattern after `A.6.P` generic relation recovery has isolated one current method-or-work boundary claim and the exact entity is already in view, but words such as `input`, `raw material`, `source data`, `source material`, `output`, `result`, `outcome`, `deliverable`, or `handoff` still do not reveal the direct relation that makes the sentence true. They **SHOULD** also use it when method, intended-work, actual-work, production, evaluation, delivery, acceptance, transfer, or receiving-use wording leaves that claim's participant meaning or orthogonal claim dimensions unclear.

The primary EntityOfConcern is one relation-bearing claim in an episteme. The trigger word helps a practitioner notice the problem; it is not the governed object, a participant kind, a relation kind, or a universal family of inputs and results.

**Primary working reader, concern, and viewpoint.** The primary reader is a practitioner or engineer whose current task is to make one boundary-word claim safe for a named use. Their concern is which exact relation and claim dimensions can be stated safely for that use now; the viewpoint is that use. The `SubjectPatternLocator` identifies the pattern description containing the defining or constraining ClaimGraph, while current case facts determine whether the relation obtains.

**First useful result.** Start at the boundary-word sentence and answer three ordinary questions: what exact thing is being named, relative to what exact method, plan, work, operation application, transformation, delivery, or receiving use, and what direct verb can safely be said now—or why can it not yet be said.

For example, a note says, `inspection report R-17 is the result of inspection`. `R-17` is an exact report episteme. If the current related object is independently identified inspection application `P-17` and its declaration-local result-binding predicate actually holds, write: `Inspection application P-17 returned report R-17.` Then stop unless the current use separately asks about report inception, inspection Work, evidence, publication, delivery, or acceptance.

The nearest three failures keep the same thing and related object while changing only the deciding deficit:

- if the binding governor is known and the case facts fail its positive predicate, the proposed positive binding is `factually unsupported`;
- if the governor is known but the fact needed to decide whether P-17 returned R-17 is unavailable, return `missing-information`;
- if no current result-binding predicate or direct report relation governs that pair, return `missing-governor` and name the exact participants, proposed predicate, affected use, and absent definition; name a future pattern or declaration need only when one is actually identifiable.

Only when another reading could change the answer should the practitioner make the formal distinctions explicit: reusable declaration versus intended, committed, current, or historical subject relation; exact extent; polarity; and whether the claim is assertable. A direct relation additionally names its exact `RelationKind` and resolving direct pattern or relation-declaration episteme. An operation binding or local claim instead names its declaration-local or admitted predicate and defining declaration. These assurance details check the ordinary answer; they are not prerequisites for understanding a simple positive past-tense sentence.

**What changes in practice.** The engineer stops debating which broad word is correct. They name the thing, the exact object it is relative to, and the direct verb they can safely say now; if no verb is yet justified, they state the exact failed fact, unavailable fact, or absent governor. Formal claim dimensions and assurance apparatus appear only when they can change or check that answer. Planning, actual participation, production, evaluation, delivery, acceptance, and transfer no longer inherit one another through vocabulary.

**Adoption test.** Given one compressed sentence, the reader can replace it with either the shortest direct sentence under its exact governor or an exact factually-unsupported, missing-information, or missing-governor result, without turning a plan, description, binding, record, or label into actuality.

**What goes wrong if missed.** A plan is read as actual participation; a method description is treated as a work occurrence; an operation result binding is mistaken for a produced entity; a changed continuing entity becomes a new output; a delivery or handoff package is treated as the transfer; or a convenient missing relation is replaced by a new universal kind.

**Ordinary non-use boundary.** Practitioners **SHOULD NOT** use this pattern when the exact direct relation and all claim dimensions needed by the receiving use are already readable; they **SHOULD** apply that direct pattern and stop. They **SHOULD** use `C.2.P` first when the unresolved question is which source expression, episteme, publication, or source-to-use relation is current; `A.15.PROD` directly when the only current question is production-work participation, entity-identity inception, or production completion and its participants are already exact; and the direct measurement, evaluation, commitment, delivery, acceptance, transfer, resource, premise, transformation, method, planning, or work pattern when that relation is already selected.

## A.6.P.WMR:2 - Problem {#problem}

Boundary words are useful in ordinary language because they compress a relation into a role-like label. The compression becomes unsafe when a later claim depends on which relation actually obtains. The same entity can be a resource used by work, an argument bound in one operation application, an affected referent changed by work, a constituent of another entity, a premise used in reasoning, a newly constituted episteme, a delivered item, or an object used by receiving work. Those are not interchangeable positions.

The repair preserves ordinary readability without manufacturing a universal work-result ontology. It also recovers, without collapsing them, the claim subject, modality and temporal extent, polarity, and recovery or support state. A reusable declaration, an intended relation, an obtaining commitment, an actually obtaining or historically obtained subject relation, and an unresolved claim can overlap across those dimensions; they are not one posture axis. A sentence can be ontologically precise and still be false or unsupported; evidence and assurance remain separate questions.

## A.6.P.WMR:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Ordinary language vs exact relation | Practitioners need short sentences, while the receiving use needs exact participants and an obtaining condition. |
| Method semantics vs dated work | A reusable way of doing and its description can name participant roles without assigning or binding an entity in one actual occurrence. |
| Plan vs actuality | Intended work and planned fillings guide action but do not establish dated work or actual participation. |
| Operation binding vs work relation | An `A.6.1` application can bind an argument or result value without producing that entity or identifying the surrounding work. |
| Change vs production | Work can cause an actual change without constituting a new entity or completing production. |
| Readability vs ontology economy | A familiar label is cheap, but one universal input, output, result, or handoff kind would erase direct subject semantics. |
| Local blocker vs broad invention | A missing governor stops only the affected claim; independent claims continue, and ontology does not expand by convenience. |

## A.6.P.WMR:4 - Solution {#solution}

**Normative method boundary.** The Conformance Checklist states each method requirement once; the explanatory sections add none. A generic prescription states what one exact policy or other normative episteme requires; it does not create an individual duty bearer or commitment occurrence. A claim that one actual System or separately governed party has that duty instead cites one separately obtaining A.2.8 `U.Commitment`. WMR opens that individual branch only when the source sentence actually makes that claim. Ontic identity, obtaining, polarity, non-entailment, and admissibility remain declarative.

**Stable WMR lens.** Treat the boundary wording as one use-specific claim about an exact thing relative to an exact object. Recover the direct verb or reason-specific stop first. Keep claim subject, time, polarity, and assertability independently recoverable when any of them can change the answer; do not turn the wording into a participant kind, relation kind, or universal input or result family.

The method handles one relation-bearing claim at a time. The trigger word stays in view only until the exact thing, related object, and safe direct verb or stop are recoverable. The result replaces the compressed phrase with the shortest ordinary sentence. If a neighboring claim is still needed, apply the pattern whose Solution answers that exact question.

### A.6.P.WMR:4.0 - Thin recovery core and conditional interfaces {#thin-recovery-core-and-conditional-interfaces}

The stable ordinary core is one `A.6.P`-isolated relation-bearing claim, one exact thing, one exact related object, one direct verb or reason-specific stop, exactly one of four truthful exit families, and one readable sentence. The fourth family is an exact non-assertability result whose reason is independently `factually unsupported`, `missing-information`, or `missing-governor`; only `missing-governor` is an ontology blocker that names the affected use and absent definition, applicability, or occurrence rule. It names a future pattern or declaration need only when one is actually identifiable.

Claim subject, modality and temporal extent, polarity, and recovery or support state remain four independent assurance controls. Their values must be recoverable whenever they can change the answer, but a practitioner does not have to recite the four labels when an ordinary sentence already makes the only material reading clear. WMR supplies this recovery and stop. It does not absorb the algorithms, checklists, or ontics of rules applied to a separate question.

| Additional question and applicable rule | Apply it only when | Result used here |
| --- | --- | --- |
| the rule that defines or tests the exact direct relation, or `A.6.1` | the exact relation or one declared operation application is the current question | one readable direct subject-relation claim, one exact declaration-local application binding, or its exact non-assertability result |
| `A.6.RCD` | no direct relation closes the named use, and a substrate-admitted compound claim, repeated predicate semantics, or relation-kind question is current | its lightest local claim, reusable-definition or conditional kind-admission continuation, or exact blocker; WMR does not reproduce the derivation or disposition algorithm |
| `A.15.PROD` | production-work participation, entity-identity inception, or production completion is explicitly the current question | one local production claim or that branch's exact blocker; WMR does not reproduce the branch basis |
| `A.15.1`, then `F.18` when naming is needed | an action nominal or plan-like label is being relied on as one performed occurrence | one exact Work occurrence admitted under `U.Work` at the required granularity or the exact lowered neighboring object or blocker; apply F.18 only after that result when durable naming is needed |
| `A.3.4` and the rule for the current transformation-composition claim | the current claim actually depends on an actual change or positive transformation composition | one independently identified transformation, one governed composition result, or the exact missing-governor or missing-substrate blocker |
| the rule for evidence use, assurance, naming, delivery, acceptance, transfer, publication, or another subject | the current use additionally needs that distinct claim | only the separately established claim, judgment, name, occurrence, or blocker; none becomes a WMR field or makes the recovered relation obtain |

The substantial interfaces retained below distinguish exits or show why tempting exits differ. Repetition of another rule's full basis is not evidence of correctness; use only the separately established result needed by the current claim.

### A.6.P.WMR:4.1 - Three ordinary questions and two conditional assurance questions {#three-ordinary-questions-and-two-conditional-assurance-questions}

| Ask | Write |
| --- | --- |
| 1. What exact thing is this? | Name one exact referent under its admitted kind. `Input`, `Output`, `Result`, `Outcome`, `Deliverable`, and `Handoff` do not become kinds. |
| 2. Relative to what exact object is it being named? | Name one exact method description, plan, dated Work, operation application, transformation, evaluation, delivery, transfer, receiving work, or another directly governed object. Split several current related objects into separate claims. |
| 3. What direct verb can be said now—or why not? | Write the shortest direct relation sentence, declaration-local binding, local claim, or reason-specific non-assertability result. A synonym, shared time, plan row, diagram edge, or nearby record is not the deciding relation. |
| 4. Could a claim dimension change the answer? | Only then state the material claim subject, modality and extent, polarity, or recovery or support distinction. Keep them independent. |
| 5. Does a named later use need the formal governor or assurance replay? | Name the PatternID locator for the defining or testing content, exact `RelationKind` and relation-declaration episteme, declaration-local predicate, or local-claim rule that makes the answer checkable. Add occurrence identity, evidence, publication, or assurance only when that later use needs it. |

The practitioner stops after question 3 when the ordinary answer has one clear reading and no named later use needs more apparatus. Questions 4 and 5 inspect or reuse that answer; they do not replace it.

### A.6.P.WMR:4.2 - Use the four claim dimensions only when they can change the answer {#use-the-four-claim-dimensions-only-when-they-can-change-the}

The four dimensions remain independent. Make a dimension explicit when two plausible values would change the sentence, the next action, or the stop. Otherwise let ordinary grammar carry it: `CF-17 was consumed by W-204 during I-204` already states a positive historical subject relation at one extent and does not require the reader to label four axes.

| Claim dimension | Recovered answer | Non-inference guard |
| --- | --- | --- |
| Claim subject | One reusable declaration, particular intended relation, commitment relation, or particular subject relation. | Selecting the subject decides neither whether it obtains nor its polarity, time, or support. |
| Modality and temporal extent | `generic`; `intended or planned`; `actually obtaining` at the current exact extent; or `historically obtained` at one exact past extent. State commitment fulfilment separately. | An obtaining commitment does not make the promised relation fulfilled; a past relation remains a historical claim at its governed extent. |
| Polarity | Positive or negative under one exact predicate, condition, and governor. | A governed negative claim individuates no obtaining relation occurrence. Absent support or missing information does not establish negative polarity. |
| Recovery or support state | `governed-and-assertable`, `factually unsupported`, `missing-information`, or `missing-governor`. | This state reports whether the selected claim can be asserted; it neither makes nor prevents the subject relation from obtaining. |

**Well-formedness constraint `WMR-WF1` — orthogonal claim dimensions.** Whenever one of the four dimensions can alter the result, its value must be separately recoverable from the sentence or its immediate governed basis. No dimension supplies another. Explicit axis vocabulary is required only for a material ambiguity, comparison, assurance replay, or reusable formalization; it is not a prerequisite for every simple direct sentence.

`Factually unsupported` applies when an applicable governor is known but the available facts fail to support the proposed assertion; no opposite polarity follows without its own basis. `Missing-information` applies when the governor is known but one named fact needed for the answer is unavailable. `Missing-governor` applies when the exact participants and question are known but no current direct predicate, condition, or defining pattern or declaration closes it.

A current commitment is expressible without collapsing fulfilment only when its exact commitment `RelationKind`, participant meanings, extent, obtaining predicate, and the `SubjectPatternLocator` for its defining or constraining content are named; a local id such as `COM-17` is not that settlement. The promised delivery remains intended and unfulfilled until its own exact token, fulfilment predicate, and facts establish fulfilment. A separately stated past case fact remains positive at its governed extent after its named participants satisfy the governor's predicate; it need not obtain now to remain historically true.

A change in any dimension is substantive. A plan does not become an actually obtaining relation because its date arrives; a later observation does not retroactively manufacture a missing relation; and stronger support does not substitute for the subject relation's own facts.

### A.6.P.WMR:4.3 - Choose one of four truthful exits {#choose-one-of-four-truthful-exits}

Choose by the kind of answer the receiving use needs:

1. If one direct subject pattern or declaration defines the relation between the exact participants, use the direct relation exit.
2. If the claim is only that one identified operation application used or returned one value, use the declaration-local `A.6.1` binding exit.
3. If the question is production-work participation, entity inception, production completion, or another substrate-admitted local conjunction, use the local `A.15.PROD` or `A.6.RCD` claim exit.
4. If none of those positive exits has its required basis, stop with the exact reason: failed fact, unavailable fact, or absent governor.

The exit determines the next action; it is not a fifth claim classification.

| Exit | Use it when | Result |
| --- | --- | --- |
| Exact direct subject relation claim | The direct governor supplies the `RelationKind`, participant meanings, predicate, applicability, and defining source. A positive claim has separate case facts satisfying the predicate. A negative claim additionally has an explicit applicable non-obtaining criterion and separate facts satisfying it. | The shortest positive or negative direct sentence. A positive occurrence, assertion episteme, local id, and evidence remain distinct; a governed negative claim individuates no occurrence. |
| Exact `A.6.1` operation-application binding | One identified application and exact bound value satisfy the declaration-local argument or result predicate, extent, kind, cardinality, and identity rule. | A sentence stating only the binding. It says neither that dated work occurred nor that work produced, constituted, delivered, or accepted the bound entity. |
| Local `A.15.PROD` or `A.6.RCD` claim | One local production question or another local compound question admitted by the selected substrate is current, and no new occurrence kind is needed. | The readable local claim under its exact base governors and the lightest sufficient disposition. |
| Exact non-assertability result | The governor is known but the required fact fails (`factually unsupported`) or is unavailable (`missing-information`), or no current direct relation, truthful binding, or admitted local claim closes the exact participants and use (`missing-governor`). | A sentence naming the proposed polarity and extent, then the known governor and failed fact, the known governor and unavailable fact, or the exact absent definition. Only `missing-governor` names the affected use; it names a future pattern or declaration need only when one is identifiable. No fallback relation or opposite polarity follows. |

A case-local positive direct relation needs two independent premises. An already published project relation-declaration episteme names the exact `RelationKind`, participant meanings, predicate, applicability, and defining source. A separate didactic world-side fact says that the exact participants at the exact extent satisfy that predicate. A positive sentence needs both. If the governor exists and the fact fails or is unavailable, return `factually unsupported` or `missing-information`; reserve `missing-governor` for absence of the governor. WMR neither publishes the token nor copies its declaration.

A governed negative sentence needs the analogous negative or non-obtaining criterion and separate facts satisfying it. Failure to support a positive claim, an absent record, or an unobserved event is not a negative premise.

The rejected `MethodDescriptionSlotFillingInWorkRelation` is not a fallback. A method-description field, planned filling, compatible type, stored reference, matching token, work-card row, or nearby result record establishes no actual participant relation by itself.

### A.6.P.WMR:4.4 - Ordinary sentence shapes {#ordinary-sentence-shapes}

These shapes are informative drafting aids. A practitioner **MAY** use one after the ordinary answer is known. Only distinctions current for the receiving use appear. In either direct-relation shape, the relation wording is an ordinary reading of one exact `RelationKind` with its resolving direct pattern or relation-declaration episteme; any assertion id remains outside that governor position. The actually-obtaining and historically-obtained shapes are available only after a separate fact says that their exact participants and extent satisfy the predicate; the compact sentence need not copy the fact fixture or evidence package.

```text
Reusable declaration:
  Under <applicability>, <exact declaration> declares that <exact entity position>
  has <participant or predicate meaning>; no particular intended or obtaining relation follows.

Particular intended relation:
  <exact WorkPlan or other intended-work episteme> states that <exact entity>
  is intended to <direct relation> <exact related object> under <condition>;
  actual obtaining remains open.

Actually obtaining now:
  <exact entity> <direct relation in ordinary words> <exact related object>
  during <current exact extent>; governed by <RelationKind token> under <direct pattern or relation-declaration episteme>.

Historically obtained:
  <exact entity> <direct relation in ordinary words> <exact related object>
  during <exact past extent>; governed by <RelationKind token> under <direct pattern or relation-declaration episteme>.

Governed negative:
  During <exact extent>, <exact entity> did not <direct relation in ordinary words> <exact related object>
  under <RelationKind token>, with defining or constraining content at <SubjectPatternLocator>; <separate case facts> satisfy
  <the direct pattern's or declaration's explicit negative or non-obtaining criterion or closure basis>,
  and no relation occurrence is individuated.

Obtaining `U.Commitment`, promised relation separate:
  <U.Commitment occurrence> obtains for <actual duty-bearing System or separately governed party>, with <modality>, <referents>, <scope>, and <validity interval>;
  <current prescription>, <exact constitutive rule>, <rule-required actual instituting basis>, and <actual facts> satisfy the A.2.8 direct predicate;
  the promised relation remains <intended | unfulfilled | fulfilled at exact extent> under its own <RelationKind token> and <SubjectPatternLocator>.

Factually unsupported:
  Under <known governor>, the <positive or negative> claim that <exact relation sentence> is not assertable
  because <available facts> fail <applicable named condition>; no opposite polarity follows.

Missing information:
  Under <known governor>, whether <exact entity> <candidate direct relation> <exact related object> obtains
  is unresolved because <named deciding fact> is unavailable.

Missing governor:
  Whether <exact participant> <proposed direct relation> <exact related participant> obtains
  is unresolved for <named use> because no current definition supplies <predicate, applicability, or occurrence rule>;
  name a future pattern or declaration need only when one is identifiable. No PatternID or case fact is required for a rule that does not exist.
```

For example, `CF-17 was not consumed by W-204` does not follow merely because the positive consumption fact fails or is unavailable. It closes as a governed negative sentence only if the direct pattern or declaration for machining resource consumption supplies an applicable non-consumption criterion or complete closure basis for the exact quantity, work, and extent and separate case facts satisfy it. Otherwise the proposed positive claim remains `factually unsupported` or `missing-information`, or the relation question remains `missing-governor`, according to the independently recovered deficit.

A practitioner **MAY** retain the trigger word as optional Plain orientation after the direct sentence is recoverable. The direct sentence and its dimensions, not the familiar label or support state, carry the claim into planning, work, evaluation, delivery, acceptance, transfer, or receiving use.

### A.6.P.WMR:4.5 - Composition and universal-result stop {#composition-and-universal-result-stop}

**Invariant `WMR-I1` — ontology economy.** No universal work-result, transformation-result, production, input, output, outcome, deliverable, handoff, evidence, actual-filling, or status relation or kind follows from boundary-word recovery. **Invariant `WMR-I2` — transformation non-entailment.** No actual transformation follows from a method, plan, desired state, model, description, evaluation result, publication, transfer, flow arrow, adjacency, shared work, or common affected referent.

When the repaired claim depends on transformation composition, state its exact participants and question, then apply `A.3.4` and the rule for that composition claim. Keep only the resulting independently identified transformations plus either one governed composition claim or the exact missing-governor or missing-substrate blocker. WMR does not restate or evaluate their contribution, compatibility, composition, or reidentification algorithm.

The blocker reaches only the composition-dependent claim; independent work, change, production, evaluation, delivery, acceptance, transfer, and receiving-use questions continue under their own governors.

### A.6.P.WMR:4.6 - Recognition and assurance remain separate {#recognition-and-assurance-remain-separate}

For ordinary recognition, the first three questions and one of four truthful exits are enough. Use the two assurance questions and explicit claim-dimension vocabulary only when they can change the answer or a named later use needs to inspect it.

A practitioner **MAY** open a separate assurance branch when the receiving use additionally needs evidence, warrant, assurance, gate, currentness, publication, or reliance. Apply the relevant evidence, assurance, gate, currentness, publication, or reliance check to the exact direct subject claim, `A.6.1` application binding, local `A.15.PROD` or `A.6.RCD` claim, or non-assertability result together with its governor. Preserve `factually unsupported`, `missing-information`, and `missing-governor` as different reasons; only the last can name a future pattern or declaration need, and only when that need is identifiable. Support or assurance changes neither polarity nor whether the subject relation obtains.

DPF or FPF authoring may trigger the applicable E.19, A.10, B.3, or other assurance checks. Those checks remain with their subject patterns rather than becoming a second WMR checklist.

### A.6.P.WMR:4.7 - Decide the main `result` readings before scanning examples {#decide-the-main-result-readings-before-scanning-examples}

When the trigger is `result`, use the deciding fact before any catalogue:

- if the same entity continues and changed, recover that continuing entity and its separately governed change;
- if an entity first began to exist, open A.15.PROD's entity-inception branch;
- if one operation application returned a value, state only its A.6.1 result binding;
- if the referent is a measured characteristic value, keep that exact value and its direct measurement relation; if it is a comparison, diagnosis, or evaluation claim, identify that exact C.2.1 episteme and its direct basis;
- if an entity was delivered or transferred, use the direct delivery or transfer occurrence;
- if the claim is a downstream effect, apply the pattern whose Solution answers that exact effect-relation question;
- if `result` names a `C.11` `ChoiceResult`, an acceptance verdict, a decision occurrence or record, an enduring condition, or another value, entity, fact, or claim already identified under its applicable identity or occurrence rule, keep that exact kind and write only the direct relation current for this use.

If no row has its deciding fact and governor, `result` remains unresolved and the answer is the reason-specific non-assertability result. These readings share no result kind or relation family.

The broader boundary-word palette below is an informative recognition aid. A row suggests a likely related object and candidate semantics; the result then leaves the palette for the direct governor. Several rows may apply to the same entity at different times or for different uses, and they remain separate claims.

| Encountered wording | Recovery direction |
| --- | --- |
| `input` | Name the exact entity and related object. Test the concrete affected-referent, resource-use, parameter-binding, constituent-supply, premise-use, reference-use, operation-argument, transformation-participation, planned-filling, or other direct relation current in the case. No input family follows. |
| `raw material` or physical `source material` | Keep the physical entity distinct from its constituent, affected-referent, consumed-resource, transfer, supply, or transformation relation. `Source` alone does not open C.2.P. |
| epistemic `source data` or `source material` | Let C.2.P recover the exact source expression, episteme, publication, and source-to-use relation; then recover the separate relation to the current method, plan, work, transformation, evaluation, or receiver. |
| `output` | Apply the `result` split above. A changed continuing entity is not newly constituted merely because it is called an output. |
| `result` | Apply the deciding branches above. Keep the referent under its own kind and write only the direct relation or binding that makes this use true. |
| `outcome` | Distinguish a downstream subject effect from a measured value, comparison, or evaluation verdict. Each has its own related object and governor. |
| `deliverable` | Recover the entity separately in each planning, commitment, delivery, and acceptance claim. Planned, produced, delivered, and accepted are not inherited from one another. |
| `handoff` | Recover the actual transfer work or direct transfer relation. A package or record is a separate episteme; transfer, delivery, and receiving use remain distinct. Use E.10.MOVE only when that exact process-move question is current. |

When no direct governor closes a selected row, name the exact participants, proposed predicate and question, affected use, and absent definition, applicability, or occurrence rule. Name a future pattern or declaration need only when one is identifiable. A broader hypernym, another boundary word, or a new universal record does not settle the missing relation.

### A.6.P.WMR:4.8 - Work-name grounding by morphology and occurrence {#work-name-grounding-by-morphology-and-occurrence}

An action nominal such as `testing`, `assembly`, `maintenance`, `evaluation`, or `inspection` is a morphology cue, not an occurrence identification or recovered kind. Placement in function- or flow-structure prose does not identify a `U.Function` or any other object by itself. When the use remains function-like and claim-bearing while its exact FPF object or relation is hidden, `A.6.F` is the next subject pattern. When the object is already recoverable, the label resolves to the exact `U.Method`, `U.MethodDescription`, required or desired behavior or effect claim, actual `U.Transformation` independently grounded under A.3.4, selected `TransformationFlowStructure`, selected functional `U.Structure` and its `ArchitectureStructuralView`, C.2.1 `FunctionalElementClaim` episteme, `FunctionalStructureViewUse`, candidate bearer, qualified ability claim about the bearer System under A.2.2, functional-port declaration, allocation or correspondence claim, plan content, performed Work occurrence admitted under `U.Work`, or another object actually defined by its direct pattern. The view branch cites these separate values; it does not create an individual from the action word. In a WBS element, activity, or Work Package the nominal ordinarily names plan or assignment content about intended work; none of these uses identifies an already performed Work occurrence.

A use that needs only the recovered method, method description, plan, structure, or other already governed value closes under that direct pattern. Only reliance on the label as one performed occurrence handles the candidate designation and required granularity under `A.15.1`.

For a performed-occurrence question, apply A.15.1 and use only its established result: one exact Work occurrence admitted under `U.Work` at the granularity needed by the current use, an exact lowering to the neighboring method, description, plan, evidence, telemetry, temporal, or other supported object, or an exact blocker. A materially needed `workContinuityPolicyRef` remains part of the A.15.1 identity judgment rather than a WMR field. Apply `F.18` only after one occurrence is established and needs a durable name.

Any output, result, outcome, production, delivery, or acceptance wording is a separate WMR claim only while its direct relation or claim dimensions remain hidden. Once readable, apply the rule for that relation or claim; it does not become part of work identity.

The preceding action-nominal classification is an FPF-scoped synthesis from recurring morphology-and-subject ambiguity, not a rule imported from PMI, PRINCE2, IDEF0, or IDEF3. A domain may conventionally use an action nominal as the durable name of an already grounded method, plan item, functional-view record, or dated work occurrence; that direct identity and exact predicate win over morphology. The synthesis reopens if repeated practice shows that the cue classifies a directly grounded value under the wrong predicate family, or if a trigger case cannot close through `A.6.F`, the exact subject predicate, or `A.15.1` without new ontology.

| Planning or description lineage | Bounded use here | Prohibited inference |
| --- | --- | --- |
| PMBOK WBS practice | Its deliverable-oriented naming pressure is used only to recognize that WBS elements and Work Packages are often named from expected deliverables. | The named plan element proves no dated occurrence, enacted method, actual participant, produced entity, result, or outcome. |
| PRINCE2 7 public Foundation page | The page is used only as currentness evidence that PeopleCert presents Version 7 and describes seven recurring project-management practices. It does not expose detailed product, product-description, activity, or Work Package distinctions, so those distinctions are not source authority here. | Neither the page nor PRINCE2 terminology supplies occurrence identity, a positive FPF kind inference, or any production, delivery, or acceptance claim. |
| IDEF0 historical recognition lineage (non-authoritative here) | A box label remains source-side function-model wording. A still-hidden FPF claim requires `A.6.F`; otherwise the label names the already recovered required-transformation or required-effect claim, actual `U.Transformation`, functional-view record, method description, `TransformationFlowStructure` locus, or other exact governed value under its direct pattern. | This lineage supplies no positive FPF kind inference: neither box form nor function wording identifies `U.Function` or supplies identity evidence for a performed Work occurrence admitted under `U.Work`. |
| IDEF3 Units-of-Behavior historical recognition lineage (non-authoritative here) | The terminology remains only as wording that may occur in inherited process descriptions. | This lineage supplies no positive FPF kind or relation inference; a Unit-of-Behavior description or label is never identity evidence for a dated Work occurrence admitted under `U.Work`. |

**Inspection contrast.** `inspection method` names the way of doing. `planned Pump-14 inspection work` is intended-work content. `Pump-14 inspection on 2026-07-15 09:10-09:34` becomes an exact performed occurrence only when applying A.15.1 establishes it at the required granularity; otherwise retain the lowered object or blocker. If the current question is whether the work first constituted an inspection-report episteme, apply A.15.PROD and use its local entity-identity-inception claim or exact branch blocker. A measured or diagnostic result uses its direct result rule, and a pass/fail verdict remains a separately governed evaluation-result episteme rather than the inspected entity or a downstream effect.

## A.6.P.WMR:7 - Conformance Checklist {#conformance-checklist}

| Check | Pass condition |
| --- | --- |
| `CC-A6PWMR-1` | @fact:CC-A6PWMR-1 A conforming practitioner **MUST** keep one exact relation-bearing claim as the `EntityOfConcern` and **MUST** treat trigger words only as recognition aids. @status:spec/done |
| `CC-A6PWMR-2` | @fact:CC-A6PWMR-2 A conforming practitioner **MUST** name the exact entity and admitted kind independently of its boundary-word role. @status:spec/done |
| `CC-A6PWMR-3` | @fact:CC-A6PWMR-3 A conforming practitioner **MUST** name the exact related object and **MUST** split several current related objects into separate claims. @status:spec/done |
| `CC-A6PWMR-4` | @fact:CC-A6PWMR-4 Before every positive direct relation, a conforming practitioner **MUST** establish two independent premises: (1) the exact `RelationKind` resolves through a direct rule or already published relation-declaration episteme to participant meanings, obtaining condition, applicability, and defining source; and (2) a separate case fact says that the exact participants at the exact extent satisfy that condition. The practitioner **MUST** keep that fact distinct from any token, declaration, work or transformation identity, chronology, record, assertion episteme, local id, or evidence item. A failed fact returns `factually unsupported`, an unavailable fact returns `missing-information`, and only an absent governor returns `missing-governor` with exact participants, proposed predicate, affected use, and absent definition. A future pattern or declaration need is named only when identifiable. @status:spec/done |
| `CC-A6PWMR-4a` | @fact:CC-A6PWMR-4a Before every governed negative direct-relation claim, a conforming practitioner **MUST** recover the current exact governor, its applicable negative or non-obtaining criterion or closure basis, and separate case facts satisfying that basis at the exact extent. The practitioner **MUST NOT** infer negative polarity from failure or unavailability of the positive fact and **MUST NOT** individuate an obtaining relation occurrence. @status:spec/done |
| `CC-A6PWMR-5` | @fact:CC-A6PWMR-5 A conforming practitioner **MUST** keep claim subject, modality and exact extent, polarity, and recovery or support state independently recoverable whenever any can change the answer and **MUST** check `WMR-WF1`. The practitioner **MUST NOT** require the four labels when a simple sentence already carries the only material reading. @status:spec/done |
| `CC-A6PWMR-6` | @fact:CC-A6PWMR-6 A conforming practitioner **MUST NOT** substitute a direct subject-relation claim, `A.6.1` operation-application binding, local `A.15.PROD` or `A.6.RCD` claim, and non-assertability result for one another. @status:spec/done |
| `CC-A6PWMR-7` | @fact:CC-A6PWMR-7 A conforming practitioner **MUST** return first the shortest ordinary direct sentence or exact factually-unsupported, missing-information, or missing-governor result and **MUST** open additional apparatus only for a named receiving use. @status:spec/done |
| `CC-A6PWMR-8` | @fact:CC-A6PWMR-8 Authors and modelers **MUST NOT** introduce a universal input, output, result, outcome, deliverable, handoff, evidence, production, actual-filling, status, work-result, or transformation-result kind or relation. This checks `WMR-I1`. @status:spec/done |
| `CC-A6PWMR-9` | @fact:CC-A6PWMR-9 A conforming practitioner **MUST NOT** infer an actual relation or transformation from a plan, description, token match, application record, work record, measurement, result episteme, adjacency, or shared referent. This checks `WMR-I2`. @status:spec/done |
| `CC-A6PWMR-10` | @fact:CC-A6PWMR-10 For a composition-dependent claim, a conforming practitioner **MUST** preserve independently grounded claims and **MUST** return either the direct composition result or its exact blocker without stopping those independent claims. @status:spec/done |
| `CC-A6PWMR-11` | @fact:CC-A6PWMR-11 When a label is relied on as performed work, a conforming practitioner **MUST** state its candidate designation and required granularity, apply A.15.1, and use only the established exact Work occurrence admitted under `U.Work`, lowered neighboring object, or blocker. After one exact occurrence is established, the practitioner **MAY** apply F.18 for durable naming. @status:spec/done |
| `CC-A6PWMR-12` | @fact:CC-A6PWMR-12 When entity-identity inception is current, a conforming practitioner **MUST** state the exact candidate entity or pre-inception basis, exact Work question, and receiving use, apply A.15.PROD, and use only the resulting local inception claim or blocker. The practitioner **MUST NOT** substitute Work, change, rendering, an identity rule, or proximity for that result. @status:spec/done |
| `CC-A6PWMR-13` | @fact:CC-A6PWMR-13 When evidence, warrant, assurance, gate, currentness, publication, or reliance is current, a conforming practitioner **MUST** apply the relevant check or use to the exact direct subject claim, exact `A.6.1` application binding, exact local `A.15.PROD` or `A.6.RCD` claim, or exact non-assertability result and **MUST** use only the separately established result. For non-assertability, the practitioner **MUST** preserve `factually unsupported`, `missing-information`, and `missing-governor` as independent reasons; only `missing-governor` may open an identifiable future definition need. The practitioner **MUST NOT** treat support or assurance as polarity, obtaining, or a field of the relation-bearing claim. @status:spec/done |

## A.6.P.WMR:9 - Consequences {#consequences}

- Practitioners retain short ordinary sentences while downstream users can recover the exact relation and its orthogonal claim dimensions.
- Method, plan, work, operation application, actual change, production, evaluation, delivery, acceptance, transfer, and receiving use remain independently inspectable.
- Local missing-governor blockers reveal where subject ontology is absent without forcing a new public kind.
- One compressed phrase may split into several claims; that is the cost of preserving different obtaining conditions and subject patterns.

## A.6.P.WMR:12 - Relations {#relations}

- **Specializes:** `A.6.P` for the focused method-and-work boundary-word recovery case.
- **Entry condition:** apply A.6.P.WMR after `E.10` and `E.10.ARCH` trigger and applicability checks only while the exact method-or-work boundary relation or a required claim dimension remains hidden; an already readable direct governor and complete claim dimensions need no WMR repair.
- **Uses:** `A.6.RCD` when exact participants are known but no direct relation closes the receiving claim; `C.2.P` for epistemic source expression and source-to-use recovery before the exact relation involving a Work occurrence is recovered.
- **Coordinates with:** `A.3.1` method identity and generic participant meanings; `A.3.2` method descriptions; `A.6.1` actual operation applications and declaration-local bindings; `A.15.1` dated work; `A.15.2` intended work and plans; `A.15.3` planned fillings; `A.3.4` actual bounded change; and `A.15.PROD` production-work, entity-identity-inception, and production-completion recovery.
- **Durable naming condition:** apply `F.18` only after the exact governed value from a direct subject relation, exact `A.6.1` application binding, or exact local `A.15.PROD` or `A.6.RCD` claim, together with its receiving use, is recovered. The fourth family—an exact non-assertability result independently reasoned as `factually unsupported`, `missing-information`, or `missing-governor`—does not authorize durable naming. Only `missing-governor` is an ontology blocker, and it names a future pattern or declaration need only when one is identifiable. A durable performed-work name additionally requires the `A.15.1` occurrence basis.
- **Neighboring assertions:** state the recovered measurement, evaluation, commitment, delivery, acceptance, transfer, resource, premise, source-use, Transformation, evidence, assurance, publication, gate, decision, or Work claim under its exact predicate; cite its `SubjectPatternLocator` only when the locator is needed.
- **Boundary:** A.6.P.WMR is the pattern for the recovery method and ordinary direct sentence. It does not define direct subject ontics, create the work occurrence, make an operation binding obtain, admit a relation kind, supply evidence or warrant, or decide downstream reliance.


## Dependencies {#dependencies}

- @fact:SPECIALIZES Specializes: spec://ai.lev/fpf-spec/contract/A-6-P#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/A-3-1#root, spec://ai.lev/fpf-spec/contract/A-3-2#root, spec://ai.lev/fpf-spec/contract/A-6-1#root, A.15.1-A.15.3, spec://ai.lev/fpf-spec/contract/A-3-4#root, spec://ai.lev/fpf-spec/contract/A-15-PROD#root, spec://ai.lev/fpf-spec/contract/A-6-RCD#root, spec://ai.lev/fpf-spec/contract/C-2-P#root, spec://ai.lev/fpf-spec/contract/E-10#root, spec://ai.lev/fpf-spec/contract/E-10-ARCH#root, spec://ai.lev/fpf-spec/contract/E-18-1#root, spec://ai.lev/fpf-spec/contract/F-18#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-15-6#root, spec://ai.lev/fpf-spec/contract/A-15-PROD#root, spec://ai.lev/fpf-spec/contract/A-6-P#root, spec://ai.lev/fpf-spec/contract/E-10#root, spec://ai.lev/fpf-spec/contract/E-10-ARCH#root, spec://ai.lev/fpf-spec/contract/E-18-1#root, spec://ai.lev/fpf-spec/contract/F-18#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/A-6-P-WMR
