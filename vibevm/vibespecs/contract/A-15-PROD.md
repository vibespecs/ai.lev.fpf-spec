# A.15.PROD - Production Work, Entity-Identity Inception, and Production Completion Recovery {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Architectural (A)
> **Status:** Stable
> **Normativity:** Normative unless marked informative

**Plain name.** Separate production work, when this exact entity first exists, and when production was completed.

**At a glance.** Production wording often compresses three questions: is this dated Work the whole production Work or only a declared part; when did changes attributed to that Work first make the applicable identity rule true so this entity began to exist; and, for completion, which subject state satisfied the criterion and which separate governor made that satisfaction close the exact production Work? This pattern answers each question with separate local claims. It introduces no universal production relation or production-work kind. Call one specification or criterion an edition of another only when their exact C.2.1 `EpistemeEditionRelation` obtains.

**Plain claim-record gloss.** A local compound relation-bearing claim is one checkable statement for one selected question, built from already governed facts. It is neither an omnibus production record nor a new relation kind. Whole production work, first existence, and completion therefore remain three separate claims even when they cite overlapping facts.

## A.15.PROD:1 - Problem Frame {#problem-frame}

**Use this when.** Practitioners **SHOULD** use this pattern when work is said to have *made*, *produced*, *built*, *assembled*, *grown*, *generated*, *finished*, or *completed* something and the receiving decision needs to know which exact production question is true. They **SHOULD** prefer it when one work occurrence is nested in larger work, several work parts occur concurrently, an entity becomes identifiable before all work ends, or completion is being confused with delivery, acceptance, release, publication, or availability.

**Primary EntityOfConcern by selected branch.** Production wording is the umbrella. A production-work-participation claim concerns exact `currentWork`; an entity-inception claim concerns exact `producedEntity` after inception. Completion needs two claims when Work closure is asserted: the state-satisfaction claim concerns exact `completionSubject`, while the production-work-completion claim concerns exact `productionWork` and cites the separate closure governor. Keep each in its own C.2.1 episteme when persisted; never manufacture a union concern.

**Primary working reader.** A practitioner or modeler responsible for settling one of these production, identity, or completion questions for a current engineering, manufacturing, construction, lifecycle, audit, or scientific use before relying on delivery, acceptance, release, publication, or availability.

**Primary viewpoint.** The practitioner **SHOULD** recover the smallest receiver-relevant claim: select one branch, identify its exact `EntityOfConcern`, and stop when that branch is decided or its exact blocker is known. This pattern is not a form to fill in.

**First useful move.** The practitioner **SHOULD** first ask which answer the receiving action or decision needs now:

1. Is this dated Work the whole production Work for this use, or a declared proper part of it?
2. Which identity rule applies to the candidate, and at what boundary did changes attributed to this Work first make that rule true so this entity began to exist?
3. Which subject state satisfies the applicable completion criterion, and which declared predicate or local claim makes that satisfaction close the exact production Work at this boundary?

The practitioner **MUST NOT** substitute one branch's conclusion for another branch's answer. Shared facts may support more than one branch only through each branch's own predicate and applicability.

**What goes wrong if missed.** Any work-caused change is called production; an entity is treated as existing before its identity rule first holds; a finishing operation is mistaken for entity creation; a plan, log, post-state picture, or first observation is treated as the change-producing link; and a later delivery or acceptance claim is used to revise historical completion without a new basis and claim.

**What this buys.** Teams can attribute production work at the right work boundary, state when one entity first exists, and preserve historical completion without inventing a universal relation kind. Narrow and larger production readings can coexist through exact work-part relations. Identity, completion, rework, delivery, acceptance, release, publication, and availability remain independently inspectable.

**Cross-domain recognition test.** These three non-exhaustive recognition situations show that the same three production questions remain separate across heterogeneous practice:

| Recognition situation | First current question | Blocked overread |
| --- | --- | --- |
| A fastening step is said to have "produced Car 42". | Is the step whole production work or a proper part, did Car 42 already exist, and which completion criterion is current? | The last visible step establishes neither first existence nor completion by narrative order. |
| A culture run or spontaneous biological process is said to have "produced Batch B17". | Does the case satisfy the common performer/Work route in section 4.2; only then, which identity or completion branch is current? | Growth or reaction may ground an actual transformation, while production through Work still requires independently admitted Work and its own attribution basis. |
| A build pipeline is said to have "produced ReleaseBinary 12". | Which dated build work and governed effects first established the exact artifact identity, or satisfied the build-completion criterion? | Build success, publication, release, deployment, and availability remain different claims. |

**First worked replay — Car 42.** Apply the common performer/Work route in section 4.2 to `FasteningCell-7`, `NutFasteningWork-42`, and their enacted fastening Method. The named Work-to-change predicate, finishing-state criterion, and separate closure rule establish that the Work completed the required fastening; Car 42 already existed. A missing Work-to-change or Work-closure governor returns the exact blocker shown in case 5.1 while preserving the independently established Work, transformation, or state-satisfaction claim.

**So-what adoption test.** Would replacing the separate branch answers by one broad production sentence change what the receiver may rely on, schedule, audit, accept, release, or reopen? If yes, the practitioner **SHOULD** apply this recovery. If only one already-governed neighboring claim is current, the practitioner **SHOULD** use its direct pattern instead.

**Not this pattern when.** Practitioners **SHOULD** use `A.15.1` directly when the only question is what work occurred; `A.3.4` when the only question is what actually changed; `A.3.1` when the only question is the reusable way of doing; the direct identity pattern when only entity identity is current; or the direct evaluation, delivery, acceptance, release, publication, availability, evidence, or assurance pattern when only that neighboring claim is current. This pattern coordinates those objects only for a selected production-recovery question.

**No-mint disposition.** Authors and modelers **MUST NOT** introduce `U.ProductionWork` as a U-kind. They **MUST NOT** introduce `WorkProducesEntityRelation`, `EntityIdentityInceptionByWorkRelation`, `ProductionWorkRelation`, or `ProductionCompletionRelation` as universal relation kinds. The default result is one local C.2.1 claim episteme per selected question under A.6.RCD disposition 2. Repeated use of the same predicate with the same participant meanings in one subject practice may justify one reusable predicate-definition episteme in the pattern that defines it for that practice. Consider a derived relation-kind candidate only when a named later action must refer again to the same obtaining relation occurrence rather than merely reuse the predicate; A.6.RCD and later admission govern that continuation.

## A.15.PROD:2 - Problem {#problem}

Production speech crosses several ontological boundaries. Dated Work is an occurrence. A transformation is the bounded change of a referent. An identity-specification episteme states when a candidate counts as the entity in question; a named applicability predicate or filled local claim applies it to the candidate basis and boundary. Entity-identity inception is the first boundary at which that applicable rule becomes true. For completion, a criterion first tests the state of `completionSubject`; a separate closure predicate or local claim says whether that satisfaction closes `productionWork`. A measurement or evaluation result is a separately defined value or episteme about its own concern; it is neither the produced entity nor Work completion itself.

These boundaries often differ. A ship can first exist while outfitting continues. A car can already exist before a required nut is fastened. A finished product can later be damaged, delivered, rejected, repaired, republished, or made unavailable. One broad production predicate hides those differences and also hides the exact missing governor when attribution cannot be established.

## A.15.PROD:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Familiar production language vs exact claim identity | One sentence often carries work participation, entity inception, completion, and later acceptance at once. |
| Narrow work vs containing work | A finishing occurrence may itself be production work for one bounded use and a proper part of a larger production occurrence for another. |
| Product-class identity before the entity exists | Entity-inception recovery remains blocked unless the exact identity-specification episteme and either a named applicability predicate or a filled local claim apply it to the candidate basis, subject context, and inception boundary before inception; no surrogate future entity is introduced. |
| Actual work effects vs observation | Logs, deltas, pictures, and first observations may support a claim; exact named predicates and obtaining facts establish the Work-to-change or change-to-identity links. |
| Work composition vs transformation composition | A.15.1 may ground composite work while no accepted transformation-composition governor exists. |
| First existence vs completion | Identity and completion may coincide, but neither criterion entails the other. |
| Historical truth vs later state | Index earlier completion by its exact criterion, applicability basis, boundary, and state; later damage, loss, rework, delivery, or acceptance receives a separate claim. |
| Reusable language vs ontology economy | Repeated domain use may justify predicate semantics, but a convenient production label does not justify a universal relation kind. |

## A.15.PROD:4 - Solution {#solution}

The practitioner **MUST** choose one of the three production questions, name the Work and the affected referent, candidate basis, or produced entity involved, and gather only the facts that decide that question. The practitioner **MUST** state each answer as a separate local compound relation-bearing claim and **MUST** stop or return an exact blocker when a required predicate, criterion, applicability rule, boundary fact, work granularity, or transformation-composition rule is missing. If another person, tool, or later decision must reuse the answer, identify that claim as one C.2.1 episteme. When the receiving use also depends on availability to an audience through a form or carrier, establish the separate E.24.PUB publication occurrence.

**Core and branch cut.** The common recovery core is receiver-first question selection, exact-object recovery, closure through declared predicates or one local claim selected under A.6.RCD disposition 2, and a deliberate stop. The production-work, entity-identity-inception, and production-completion branches add only their own `EntityOfConcern`, criterion or boundary, and branch-specific base. One branch neither inherits facts from another nor turns the common method into an omnibus production object. Work identity, transformation identity, subject identity, evidence, assurance, delivery, acceptance, release, publication, and availability remain with their subject patterns.

### A.15.PROD:4.1 - Split the three questions before recovering evidence {#split-the-three-questions-before-recovering-evidence}

| Question | Claim content | Ordinary stopping result | What it does not establish |
| --- | --- | --- | --- |
| Production-work participation | exact `currentWork` is itself `productionWork`, or exact `currentWork` is a declared proper work part of exact `productionWork` | one local positive or negative compound claim, or an exact work-grounding blocker | entity inception, completion, delivery, acceptance, or a universal production-work kind |
| Entity-identity inception | governed actual effects of exact `identityClosingWork` made exact `producedEntity` satisfy the rule in exact applicable `productIdentitySpecification` for the first time at exact `inceptionBoundary` | one local inception claim after the entity exists, plurality of incomparable minimal claims, or an exact blocker | production completion, later persistence, acceptance, or a reusable binary relation kind |
| Production completion | exact `completionSubject` satisfies exact applicable `productionCompletionCriterion` at `completionBoundary`, and a separate declared closure predicate or local claim connects that satisfaction to exact `productionWork` | one state-satisfaction claim plus, when asserted, one historically indexed Work-completion claim; otherwise the exact closure blocker | entity inception, delivery, acceptance, release, publication, or availability |

The three claims may cite overlapping facts. They remain different claims because they answer different receiving questions and can have different boundaries, criteria, and truthful C.2.1 `EntityOfConcern` values.

### A.15.PROD:4.2 - Recover the smallest exact base {#recover-the-smallest-exact-base}

The practitioner **MUST** use only objects needed by the selected branch:

| Working name | Exact object and governor | Required contribution |
| --- | --- | --- |
| `productIdentitySpecification` | one exact C.2.1 predicate-definition episteme whose subject pattern states the identity rule; any continuing-edition relation to another specification episteme is stated separately | states the identity rule before inception without pretending that a future entity exists |
| identity-specification applicability basis | one named applicability predicate with its actual participants and boundary facts, or one filled local compound claim selected under A.6.RCD disposition 2 | applies the exact specification episteme to the candidate basis, subject context, and candidate `inceptionBoundary`; it introduces no universal applicability relation |
| `producedEntity` | one exact `U.Entity`, designated only after inception | is the entity whose identity rule first became true |
| `productionMethod` | one exact `U.Method` under A.3.1 | states the governed way of doing, intended production effect, applicability, and relevant identity or completion criterion meaning |
| `currentWork` | one exact Work individual admitted under `U.Work` by A.15.1 | designates the world-side dated occurrence. Recover every exact actual performer through A.13, then let A.15.1 independently admit the Work from its history, at least one obtaining `enactsMethod` relation, extent, and at least one obtaining locally declared containing-system relation. Only when this production claim also consumes precise assignment-bound attribution name the obtaining occurrence of the exact declared `U.SystemRoleAssignment` species and the separate F.6 relation through the same A.13 assignment. Missing or failed F.6 preserves the Work and lowers only that attribution. Name an additional enactment, binding, resource-use, or affected-referent relation only when the production claim uses that independently obtaining fact; none is a field stored in the occurrence. |
| `productionWork` | one exact Work individual admitted under `U.Work` by A.15.1 | designates either the same occurrence as `currentWork` or the exact larger Work occurrence of which `currentWork` is a declared proper part |
| `actualTransformation` | one or more independently identified `U.Transformation` occurrences under A.3.4 | names what changed without becoming the work or the produced entity |
| work-to-change basis | one named domain predicate with exact Work and transformation participants and obtaining case facts, or one filled local compound claim selected under A.6.RCD disposition 2 | establishes that selected actual changes are effects of exact work; coincidence is insufficient |
| `completionSubject` | the exact state-bearing entity or continuing referent judged by the completion criterion | keeps the criterion's subject explicit instead of applying a product-state test to Work |
| `productionCompletionCriterion` | one exact C.2.1 predicate-definition episteme whose subject pattern states the state-satisfaction rule; any continuing-edition relation to another criterion episteme is stated separately | states what state of `completionSubject` counts as satisfying the production requirement at the candidate boundary |
| production-work closure governor | one declared subject predicate or one filled local A.6.RCD claim that connects exact criterion satisfaction for `completionSubject` to closure of exact `productionWork` at the boundary | states why the Work is complete; criterion satisfaction alone does not supply this link |
| local assertion | one C.2.1 episteme | carries only the state-satisfaction claim or the production-work-completion claim needed by the selected question |

A neighboring object enters only when a named predicate or filled local claim connects it to the selected Work, entity, or claim and omitting that connection would change the named action or decision. Otherwise keep method descriptions, work plans, objectives, commitments, product specifications, evaluation results, and E.24.PUB publication occurrences, forms, and carriers separate. None is constitutive of every production occurrence.

### A.15.PROD:4.3 - Select one production-work branch {#select-one-production-work-branch}

**Whole-work branch.** `currentWork = productionWork` is admissible only when that exact dated Work enacts `productionMethod`; the method states its intended production effect; a named applicability claim applies the method to this case's inputs and conditions; the named work-to-change predicates obtain for the exact Work and transformations; and the identity or completion criterion that decides the selected question is named and applicable. A familiar broader production label establishes no parent work.

**Proper-part branch.** Exact `currentWork` is admissible as a proper part of exact `productionWork` only when `OperationalPartOf_work` or another exact A.15.1 work-part relation with fitting occurrence semantics obtains. Interval overlap or concurrency is asserted separately and establishes neither parthood nor coordination. The containing Work must likewise enact the production method; the method must state its intended production effect; a named applicability claim must apply it to the containing case; the named work-to-change predicates must obtain; and the identity or completion criterion that decides the selected question must be named and applicable. A shared label, project membership, common referent, temporal containment, overlap, or adjacency in a plan establishes no work parthood.

The two branches can support different bounded uses. A nut-fastening occurrence can be the whole production work for a narrowly bounded finishing operation and also a proper part of a larger car-production occurrence, provided each local claim names its exact extent, criterion, and work relation. `productionWork` is a relation-defined reading of one Work occurrence admitted under `U.Work`, not an intrinsic kind.

### A.15.PROD:4.4 - Ground actual effects without inventing transformation composition {#ground-actual-effects-without-inventing-transformation}

The practitioner **MUST** first recover every actual transformation independently through A.3.4: changed referent, exact extent or formal boundary, boundary conditions, actual before/during/after facts, and continuity or reidentification rule. The practitioner **MUST** then name the declared domain predicate for each exact Work-to-transformation pair, state its participant order, and show the case facts that make it obtain. If no one direct predicate suffices, use a local compound claim selected under A.6.RCD disposition 2 only when its constructor, governed base predicates, actual participants, and case facts are recoverable. If neither route is present, keep the Work and transformation separate and return `missing-governor[work-to-change]`. Temporal overlap, a common changed referent, a delta expression, a log record, or a post-state picture may supply evidence for those facts; the declared predicate or compound claim and its obtaining facts establish the link.

One transformation identified at the resolution needed by the production claim establishes neither presence nor absence of finer transformation parts. Work parts, method parts, samples, temporal subdivisions, concurrent changes, and flow representations do not establish transformation parts or a composite transformation.

If the selected production claim uses only independently identified transformations, continue without a composition claim. If it asserts positive composite-transformation identity, transformation parthood, or transformation holonhood and no accepted governor supplies that basis, return the exact missing-governor blocker. Composite `identityClosingWork` under A.15.1 does not cure that blocker and does not imply an isomorphic composite transformation.

### A.15.PROD:4.5 - Recover entity-identity inception {#recover-entity-identity-inception}

**Definition: A15PROD-D1 (Entity-identity inception).** Entity-identity inception is the boundary at which exact `producedEntity` first satisfies the identity rule stated by exact `productIdentitySpecification` and a named applicability predicate or filled local claim applies that specification to the candidate basis, subject context, and boundary. Plain: **when this exact entity first exists**. `inceptionBoundary` is a case-local boundary designator, not a second technical term, claim kind, or relation kind.

For this branch, the practitioner **MUST** complete all five steps:

1. recover exact `productIdentitySpecification` as one C.2.1 predicate-definition episteme in the subject pattern that states the identity rule. Before inception, the governed question remains about exact work, method, actual effects, that specification episteme, and its candidate basis; no future `producedEntity` participant exists;
2. recover the named applicability predicate or filled local claim that applies that specification episteme to the exact candidate basis, subject context, and candidate `inceptionBoundary`, together with the exact actual effects of exact work and the declared links by which those effects bear on that rule;
3. find the earliest exact `inceptionBoundary` at which the rule in that applicable specification episteme becomes true and designate the resulting exact `producedEntity` only on the after-side of that boundary; the pre-inception candidate basis remains distinct from that entity;
4. identify exact `identityClosingWork`, using the one closing work occurrence when it exists or, for jointly necessary concurrent or nested work parts, their exact composite work under A.15.1 and its declared work-part relations; and
5. constitute a positive local inception claim as one C.2.1 episteme only after exact `producedEntity` exists and the claim names exact `productIdentitySpecification`, its named applicability predicate or filled local claim, exact `identityClosingWork`, exact `inceptionBoundary`, and all declared Work-to-change and change-to-identity predicates or compound bases. Add an E.24.PUB occurrence only when a receiving use also needs that episteme to be available through a named form or carrier.

A local inception claim **MUST** be indexed by the exact specification episteme and applicability basis used at `inceptionBoundary`. A later specification episteme does not silently rewrite that earlier claim. If an exact C.2.1 `EpistemeEditionRelation` connects the two specifications, the lineage can trigger refresh of a current dependent use, but the later specification still needs its own applicability basis at the boundary being judged. Without that relation, treat the later object as a non-continuing replacement and evaluate it independently. Changed applicability yields either a separately qualified claim under its new exact basis or an exact blocker; it does not move the earlier indexed boundary.

Supporting material, whether a representation, plan, record, rule episteme, or observation, enters one of the five steps only through its declared relation to that step; it does not replace the required Work, applicability, effect, or boundary predicate. Absence of recoverable work granularity for `identityClosingWork` yields a **work-granularity blocker**. Several incomparable minimal work composites yield several local inception claims and remain plural unless a separate selection rule applies.

**Regulated-identification boundary.** A persistent identifier is not an inception criterion. A current subject practice that allocates an identifier at build or registration while keeping allocation separate from entity status supplies designation and continuity only. First existence requires a separately applicable subject-identity rule; its absence yields the exact identity-governor blocker. An assigned number does not make the candidate basis the after-side entity.

### A.15.PROD:4.6 - Recover state satisfaction and historically indexed production completion {#recover-state-satisfaction-and-historically-indexed-production}

Completion wording often hides two claims. First ask whether the exact state-bearing subject satisfied the applicable criterion. Then ask whether the subject practice makes that satisfaction sufficient to close the exact production Work.

The **state-satisfaction claim** names:

- exact `completionSubject` whose state is judged;
- exact `completionBoundary`;
- exact `productionCompletionCriterion` episteme applicable to that subject and boundary;
- the named applicability predicate or filled local claim; and
- the actual boundary-state facts and the criterion predicate they satisfy.

When persisted, this C.2.1 episteme has `completionSubject` as its exact EntityOfConcern. It says nothing yet about whether Work is complete.

The separate **production-work-completion claim** names exact `productionWork`, the exact state-satisfaction claim, the same boundary, and the declared closure predicate or filled local A.6.RCD claim that makes this criterion satisfaction sufficient to close that Work. Its exact EntityOfConcern is `productionWork`. If no closure governor is available, keep the positive state-satisfaction claim and return `missing-governor[production-work-completion]`; do not apply a subject-state predicate to Work by metonymy.

Index every historical state-satisfaction and Work-completion claim by its exact criterion episteme, applicability basis, boundary, and boundary-state facts. Later damage, loss, destruction, delivery, rejection, acceptance, release, publication, or unavailability receives a separate claim. Rework or later production Work that closes under an applicable criterion at a later boundary receives another local Work-completion claim.

Entity-identity inception, criterion satisfaction, and production-Work completion remain separate even when they share a boundary. A later evaluation-result episteme may support one of these claims under a direct evidence-use relation; the branch's declared predicates and facts still establish its boundary, subject state, and Work closure.

Past Work and the two completion claims remain addressable after later destruction or evidence decay. A later assertion carries its own evidence currentness and reliance status. The produced entity, measurement or evaluation result, delivered entity, acceptance verdict, release, publication, availability, and downstream effect remain objects and claims defined and tested separately.

**Practice-specific criteria stay local.** NASA systems-engineering guidance, Scrum's Definition of Done, and similar authoritative practice sources can supply a criterion for the exact subject and practice use they address. Exact A.15.1 Work identity and a subject-practice closure predicate or local claim separately establish whether criterion satisfaction closes that Work. Transition, delivery, review, and release retain their own claims.

### A.15.PROD:4.7 - State one local claim and stop {#state-one-local-claim-and-stop}

The default A.6.RCD disposition is **local compound relation-bearing claim**. For an ordinary positive answer, the practitioner **MUST**:

1. name the receiving action or decision, state what it must decide, and select one production question;
2. recover the exact participants, direct predicates, applicability facts, and boundary facts needed by that question;
3. state the smallest readable conjunction of those governed facts and the one answer it supports, or return the exact missing-information, missing-governor, criterion, applicability, work-granularity, or boundary-state blocker; and
4. keep any durable answer in one truthful C.2.1 episteme with exact claim content, one exact `EntityOfConcern`, and an effective `U.ReferenceScheme`, then stop without introducing a relation kind, relation signature, or relation occurrence.

This ordinary positive branch does not require the practitioner to name a substrate document, constructor, hidden-witness policy, polarity algebra, or ordered-boundary operator. It requires the governed facts and a readable answer. Open author-side semantic replay only when A.6.RCD:4.2 requires a substrate pin—nontrivial, interoperability-facing, proof-bearing, high-consequence, or reusable use—or when the current negative claim or first-satisfying-boundary claim actually depends on negation, witness, ordering, or earliest-boundary semantics.

**Branch constructor semantics for the triggered replay.** These are branch-local claim constructors, not a universal production algebra:

| Branch | Least constructor over governed base claims | Hidden-participant, polarity, and time policy |
| --- | --- | --- |
| production-work participation | one typed conjunction over exact A.15.1 work identity, actual method enactment, method applicability and intended production effect, affected referent, direct work-to-change facts, the receiver's current criterion, and either exact work identity or one exact A.15.1 proper-part relation | every participant and conjunct remains named; no projection hides work, transformation, or criterion witnesses; a negative result requires the selected substrate's explicit negation law rather than absence of a base assertion |
| entity-identity inception | one time-indexed conjunction over identity-specification applicability, exact work and governed effects, direct work-to-change and change-to-identity links, and satisfaction of the applicable identity predicate, followed by the substrate's earliest-satisfying-boundary selection over its declared ordered candidate-boundary domain | the candidate basis remains distinct from the after-side entity; work parts and actual transformations remain named or follow the substrate's explicit witness policy; incomparable minimal work composites remain plural, and A.15.PROD supplies no arbitrary minimization rule |
| production completion | one boundary-indexed conjunction first states criterion satisfaction for exact `completionSubject`; a second conjunction states exact `productionWork`, that satisfaction claim, and the declared closure predicate or local closure rule | the claims keep their different entities of concern; no earliest-boundary operator is implied unless separately required, and missing closure semantics preserves satisfaction while blocking only Work completion |

For DPF or FPF authoring and every other pin-triggering use, the responsible author or modeler **MUST** name the exact selected substrate and edition and replay its constructor inputs, output claim, applicability, hidden witnesses, polarity law, and temporal policy. A negative or earliest-boundary claim **MUST** recover the specific negation, witness, ordering, or selection semantics it consumes even when no broader replay is needed. If no current substrate supplies semantics that the claim actually requires, return the exact **missing-substrate blocker**. A.15.PROD supplies no fallback operator.

For an ordinary positive result, the truthful `EntityOfConcern` is exact `currentWork` for production-work participation and exact `producedEntity` for entity-identity inception. Completion uses exact `completionSubject` for the state-satisfaction episteme and exact `productionWork` for a separate Work-completion episteme. A modeler **MUST** split claim content that cannot truthfully concern one exact entity and **MUST NOT** manufacture a union concern from work, method, transformations, criteria, evidence, and receivers.

Repeated use within one subject practice may justify one predicate-definition episteme, with the subject pattern locating the ClaimGraph that defines those participant meanings. Consider a subject-specific derived relation kind only when a named later action must also refer again to the same obtaining relation occurrence. The subject definition must then state obtaining, applicability, base dependencies, recurrence, and occurrence identity. A.6.RCD defines that candidate-construction branch; A.15.PROD defines no such kind admission by itself.

### A.15.PROD:4.8 - Separate recognition from assurance {#separate-recognition-from-assurance}

**Recognition branch for ordinary work.** Use the three questions in section 1, the branch outcomes in section 4.1, and the ordinary claim rule in section 4.7. Stop with one readable answer or exact blocker; open only the specific semantic replay needed for a negative claim, an earliest-boundary judgement, or an A.6.RCD:4.2 substrate pin.

**Assurance branch for authors and high-consequence use.** Replay the exact basis in six visible groups:

- **Work and Method.** Check exact work identity and every relied-on work-part relation, the actual `enactsMethod` relation, method applicability, and the intended production effect.
- **Actual change and entity inception.** Check every work-to-change and change-to-identity predicate and retain the explicit non-inference from work or method composition to transformation composition.
- **State satisfaction and Work closure.** Check every criterion-applicability fact and boundary-state satisfaction fact. Keep the state-satisfaction claim separate from the closure predicate or local claim that closes the Work.
- **Claim epistemes and their current basis.** Check the exact identity-specification and completion-criterion epistemes, the named applicability predicate or filled local claim for each episteme at its claimed boundary, any separately current C.2.1 `EpistemeEditionRelation`, C.2.1 identity, and the evidence-use relations actually relied on.
- **Positive and discriminating cases.** Replay both, so removal of one deciding fact blocks only the claim that consumes it.
- **Pinned author substrate.** When A.6.RCD:4.2 requires a pin, DPF and FPF authors **MUST** record the selected substrate and edition and expose direct base predicates, applicability, hidden participants, polarity law, boundary domain and ordering, witness policy, and every earliest-boundary rule used by the claim.

Assurance may warrant reliance on the claim. Work, change, entity inception, and completion remain established by their branch predicates and obtaining facts.

**Assurance scope by use.** Replay only what the actual reliance consumes. A model or declaration checks exact claim content, one truthful `EntityOfConcern`, reference scheme, participants, predicates, polarity, and boundary indexing. A conformance use checks that the selected branch reaches one grounded answer or blocker and stops. Pattern review additionally checks the worked and discriminating cases, direct-owner boundaries, checklist, and no-mint disposition. Each assurance use assesses the stated claim; it neither widens that claim nor replaces the branch predicates and facts.

### A.15.PROD:4.9 - Run the recovery sequence and stop deliberately {#run-the-recovery-sequence-and-stop-deliberately}

The ordinary sequence is section 4.7 applied to the selected branch. If several production questions are current, handle each as a separate claim. For production-work participation, choose the whole-work or proper-part branch in section 4.3; for inception or completion, use sections 4.5 or 4.6. Stop after the readable answer or exact blocker. If later reuse needs a durable claim, identify its C.2.1 episteme; if the receiving use also needs availability through a form or carrier, establish the separate E.24.PUB occurrence. Open delivery, acceptance, release, publication, availability, result, evidence, assurance, or relation-kind questions only when the named action or decision asks one of them; none follows from the production answer.

#### Triggered author replay {#triggered-author-replay}

Continue only for an A.6.RCD:4.2 pin-triggering use or when a negative or earliest-boundary answer consumes additional semantics:

1. name the branch-local constructor and, when a pin is required, the exact substrate and edition; expose only the inputs, applicability, hidden-participant or witness policy, polarity law, boundary domain and ordering, and temporal rule that can change this answer;
2. for entity inception, verify the ordered candidate-boundary domain and earliest-satisfying rule; for a negative claim, verify the applicable negation law; for completion, keep the claim indexed by its criterion, applicability basis, and boundary;
3. if one required operator or substrate is unavailable, return the exact missing-substrate blocker rather than lowering the absence to a negative production answer; and
4. stop after the author replay returns the same ordinary answer or blocker.

### A.15.PROD:4.10 - Pattern NameCard {#pattern-namecard}

This NameCard names the recovery pattern, not a relation kind. It uses F.18's expanded identity-bearing form with a direct local-sense claim because no separately recoverable F.17 SenseCell is current for this local naming settlement:

```text
NameCard:
  NameCardId: NC-A15-PROD-PATTERN
  GovernedValueRef: the A.15.PROD pattern that separates and recovers production-work participation, entity-identity inception, and production-completion claims
  SubjectPatternLocator: A.15.PROD
  ReferenceScheme: FPFCoreReferenceScheme
  ClaimContent: NC-A15-PROD-PATTERN.ClaimGraph — complete C.2.1 U.ClaimGraph constituted by all identity-bearing naming-settlement claims designated below
  LocalSenseRef: local expression `Production Work, Entity-Identity Inception, and Production Completion Recovery`; sense claim: the A.15.PROD recovery pattern asks which of the three production questions is current while keeping actual work, first existence, completion, delivery, acceptance, release, publication, and availability distinct under FPFCoreReferenceScheme
  TechLabel: Production Work, Entity-Identity Inception, and Production Completion Recovery
  PlainLabel: separate production work, when this exact entity first exists, and when production was completed
  CandidateSet: Production Work, Entity-Identity Inception, and Production Completion Recovery; Entity Production by Work; Entity-Identity Inception Through Work; Production Boundary Recovery
  CandidateCoverage: recovery-pattern, entity-production, entity-inception, and boundary-recovery head families; no plausible current family remains untested
  RejectedCandidates:
    Entity Production by Work: hides whether the claim concerns work participation, first existence of the entity, or completed production
    Entity-Identity Inception Through Work: omits production work before and after first existence and omits production completion
    Production Boundary Recovery: uses a generic boundary head and does not expose the three governed questions
  SelectionRationale: the selected title names the three distinctions that the pattern must recover and makes the completion kind explicit; it cannot be parsed as one binary or ternary production relation
  LineageEntries: initial durable settlement; the selected Tech and Plain labels are current; this card asserts no alias, rename, split, merge, or retirement
  RefreshCondition: reopen naming if repeated subject use justifies an admitted derived relation kind or one question needs a separate primary EntityOfConcern and recovery algorithm
```

## A.15.PROD:7 - Conformance Checklist {#conformance-checklist}

| Check | Requirement |
| --- | --- |
| `CC-A15.PROD-1` | @fact:CC-A15-PROD-1 The receiving use selects production-work participation, entity-identity inception, production completion, or an explicit subset. One branch conclusion is never another branch's answer; shared facts support each branch only through its own predicate and applicability. @status:spec/done |
| `CC-A15.PROD-2` | @fact:CC-A15-PROD-2 `currentWork` and `productionWork` designate exact A.15.1 Work occurrences admitted under `U.Work`, not plans, labels, projects, methods, logs, publications, or records that describe those occurrences. @status:spec/done |
| `CC-A15.PROD-3` | @fact:CC-A15-PROD-3 The whole-work branch names actual `enactsMethod`, method applicability and intended production effect, affected referent, exact work-to-change facts, and the criterion current for the receiver. @status:spec/done |
| `CC-A15.PROD-4` | @fact:CC-A15-PROD-4 The proper-part branch names an exact A.15.1 work-part relation and gives the containing work the same grounding required by the whole-work branch. @status:spec/done |
| `CC-A15.PROD-5` | @fact:CC-A15-PROD-5 Every actual transformation is independently identified under A.3.4; work, method, samples, temporal subdivision, and flow representations do not imply transformation composition. @status:spec/done |
| `CC-A15.PROD-6` | @fact:CC-A15-PROD-6 Every Work-to-change and change-to-identity link names a declared predicate with participant order and obtaining facts or a filled local A.6.RCD claim. Completion separately names the criterion-satisfaction predicate for `completionSubject` and the closure predicate or local claim for `productionWork`; neither substitutes for the other. @status:spec/done |
| `CC-A15.PROD-7` | @fact:CC-A15-PROD-7 Exact `productIdentitySpecification` is identified as a C.2.1 episteme before inception without a surrogate future `producedEntity`; a named applicability predicate or filled local claim applies it to the candidate basis, subject context, and exact `inceptionBoundary`, and the entity is designated only after that exact applicable rule first holds. Publication availability, when required, is a separate E.24.PUB occurrence. Any claim that this is an edition of another specification names an obtaining C.2.1 `EpistemeEditionRelation`. @status:spec/done |
| `CC-A15.PROD-8` | @fact:CC-A15-PROD-8 A positive inception claim satisfies `A15PROD-D1` and names exact `identityClosingWork`, exact `productIdentitySpecification`, its named applicability predicate or filled local claim, exact `inceptionBoundary`, exact `producedEntity`, and first satisfaction of that exact applicable specification's rule. @status:spec/done |
| `CC-A15.PROD-9` | @fact:CC-A15-PROD-9 Concurrent or nested identity-closing work is composed only through exact A.15.1 work-part relations; incomparable minimal composites remain plural, and each local inception claim retains its exact identity-specification episteme and applicability basis. @status:spec/done |
| `CC-A15.PROD-10` | @fact:CC-A15-PROD-10 A completion use first names exact `completionSubject`, criterion episteme, applicability, boundary-state facts, and state-satisfaction predicate. A separate Work-completion claim names exact `productionWork` and the closure predicate or local claim that makes that satisfaction sufficient to close it. Missing closure semantics blocks only Work completion. @status:spec/done |
| `CC-A15.PROD-11` | @fact:CC-A15-PROD-11 Historical state-satisfaction and Work-completion claims retain their exact criterion episteme, applicability basis, boundary, and boundary-state facts. Rework, a later criterion, damage, loss, delivery, acceptance, release, publication, or availability receives a separate claim. @status:spec/done |
| `CC-A15.PROD-12` | @fact:CC-A15-PROD-12 Each local assertion is one C.2.1 episteme with one truthful exact `EntityOfConcern`, claim content, effective reference scheme, and decided positive or negative polarity; no union concern is manufactured, and unresolved information sufficiency or reliance remains separately evaluated. @status:spec/done |
| `CC-A15.PROD-13` | @fact:CC-A15-PROD-13 An unresolved basis is returned as the exact missing-governor, work-granularity, criterion, applicability, boundary-state, or transformation-composition blocker, not as a third predicate value. @status:spec/done |
| `CC-A15.PROD-14` | @fact:CC-A15-PROD-14 The current no-mint result introduces no universal production relation kind, `U.ProductionWork`, relation signature, or relation occurrence and asserts no universal reducibility. A later subject-specific candidate requires A.6.RCD only when a named later action must reidentify the same obtaining relation occurrence; its definition states obtaining, applicability, base dependencies, recurrence, and occurrence identity. A primitive candidate additionally demonstrates failed lossless derivation, one action-facing distinction every accepted derivation loses, and independent receiving uses. @status:spec/done |
| `CC-A15.PROD-15` | @fact:CC-A15-PROD-15 Recognition and assurance remain separate. Evidence and evaluation can support a branch claim; the branch predicates and obtaining facts establish Work, transformation, entity inception, or completion. @status:spec/done |
| `CC-A15.PROD-16` | @fact:CC-A15-PROD-16 The produced entity, measurement or evaluation result, delivered entity, acceptance verdict, release, publication, availability, and downstream effect remain distinct; each positive claim names its declared predicate or its own subject pattern, and a missing predicate returns the corresponding blocker. @status:spec/done |
| `CC-A15.PROD-17` | @fact:CC-A15-PROD-17 A practice-specific source is used only for the branch question it answers: a stable identifier does not establish entity status or inception; a systems-engineering realization criterion does not collapse transition into completion; and a Scrum Definition of Done does not supply work identity, effects, review, or release. @status:spec/done |
| `CC-A15.PROD-18` | @fact:CC-A15-PROD-18 An ordinary positive local claim names its governed base facts, the exact Method and/or criterion applicability consumed by its branch, readable conjunction, answer, and stop without requiring a substrate document. A pin-triggering use names the exact substrate and edition and replays only the constructor semantics it consumes. A negative or earliest-boundary claim exposes its polarity, witness, boundary-domain, ordering, or selection law; unavailable required semantics returns the exact missing-substrate blocker. @status:spec/done |

## A.15.PROD:9 - Consequences {#consequences}

| Benefits | Trade-offs and mitigations |
| --- | --- |
| Production attribution becomes replayable at exact work boundaries. | More than one local claim may replace one familiar sentence; the three-question first move keeps ordinary use short. |
| Entity first-existence and production completion no longer overwrite each other. | The added cost is one exact identity-specification or completion-criterion episteme and its applicability basis for each current claim; name a separate C.2.1 edition relation only when lineage is current. Reuse the specification episteme already identified by the subject pattern instead of copying it. |
| Narrow and containing production work can coexist without a new kind. | Absence of exact work mereology yields an unresolved work-granularity blocker. |
| Historical completion survives later change while current evidence remains refreshable. | Boundary truth and present reliance stay separate; direct evidence and refresh patterns define or constrain current reliance. |
| Missing transformation composition no longer blocks independent production claims. | A composition-dependent claim stops at an explicit blocker; independently identified transformations and exact blockers remain useful results. |

## A.15.PROD:12 - Relations {#relations}

- **Builds on:** `A.13` for the exact actual performer; `A.15.1` for Work identity, Work parts, concurrency, continuity, and independent Work admission; `F.6` only for a production claim that consumes precise assignment-bound attribution through the same obtaining A.13 assignment; `A.3.1` for the production Method, intended effect, and applicability; `A.3.4` for actual transformations and the transformation-composition stop; `C.2.1` for local claim and predicate-definition epistemes; and `A.6.RCD` for disposition, derivation, blocker, and subject-specific continuation.
- **Coordinates with:** `A.1` and the subject-specific identity owner; `A.6.1` for an actual application and result binding without treating either as inception; `C.2.P` for exact source expressions; `A.15.2` for plans distinct from Work; `A.15.6` for project and process wording recovery; `A.10` for an evidence-use or bounded-reliance claim; `B.3` for assurance; `E.24.PUB` for availability through a publication occurrence, form, and carrier; and `G.11` when a pinned definition, substrate edition, or applicability settlement changes.
- **Coordinates with:** the exact characteristic-state, evaluation, completion-criterion, delivery, acceptance, release, availability, and refresh predicates or patterns selected by the current case.
- **Informs:** production attribution, manufacturing and construction histories, biological and informational entity inception, rework analysis, product-lifecycle records, completion audits, and P2W or P2S continuation when the receiving action or decision asks one of the three recovered questions.


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/A-13#root, spec://ai.lev/fpf-spec/contract/A-15-1#root, conditional spec://ai.lev/fpf-spec/contract/F-6#root, spec://ai.lev/fpf-spec/contract/A-3-1#root, spec://ai.lev/fpf-spec/contract/A-3-4#root, spec://ai.lev/fpf-spec/contract/C-2-1#root, spec://ai.lev/fpf-spec/contract/A-6-RCD#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/A-1#root, spec://ai.lev/fpf-spec/contract/A-6-1#root, spec://ai.lev/fpf-spec/contract/C-2-P#root, spec://ai.lev/fpf-spec/contract/A-15-2#root, spec://ai.lev/fpf-spec/contract/A-15-6#root, spec://ai.lev/fpf-spec/contract/A-10#root, spec://ai.lev/fpf-spec/contract/B-3#root, spec://ai.lev/fpf-spec/contract/E-24-PUB#root, spec://ai.lev/fpf-spec/contract/G-11#root, spec://ai.lev/fpf-spec/contract/A-6-P-WMR#root, spec://ai.lev/fpf-spec/contract/E-18-1#root, spec://ai.lev/fpf-spec/contract/F-18#root, and the direct identity, work-to-change, completion, delivery, acceptance, release, and availability patterns. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-1-1#root, spec://ai.lev/fpf-spec/contract/A-10#root, spec://ai.lev/fpf-spec/contract/A-15-1#root, spec://ai.lev/fpf-spec/contract/A-15-6#root, spec://ai.lev/fpf-spec/contract/A-3-4#root, spec://ai.lev/fpf-spec/contract/A-6-3#root, spec://ai.lev/fpf-spec/contract/A-6-P-WMR#root, spec://ai.lev/fpf-spec/contract/E-10#root, spec://ai.lev/fpf-spec/contract/E-10-ARCH#root, spec://ai.lev/fpf-spec/contract/E-18#root, spec://ai.lev/fpf-spec/contract/E-18-1#root, spec://ai.lev/fpf-spec/contract/G-6#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/A-15-PROD
