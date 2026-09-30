# E.4.PFAD - Principle-Framework Architecture Decision {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Architectural (A)
> **Status:** Stable
> **Normativity:** Normative unless marked informative.

## E.4.PFAD:1 - Problem frame {#problem-frame}

Use this pattern when an author is choosing among a new or revised principle framework, a contribution to an existing framework, another product that is not a framework, a thinner publication or access route, and no new maintained product now, and that choice will settle an identity, edition, relation, intended-use, or publication decision that later work must use. The decision may concern the public field and first use, framework edition, dependencies, initial pattern placement or relations, the kind and identity or change rule of a non-framework product, or the publication or access consequence. Another author or reviewer must need the answer and its rationale for later action.

`E.4.DPF` may return this question before a public product name, PatternIDs, or pattern bodies exist. Open it when preliminary exact subtraction leaves exact ownership unresolved, a coherent connected remainder, or a material field, relation, source or refresh, publication, or access consequence that later work must use. Treat an incoming carrier or organizing cue—for example, a role account, MethodDescription, file, Card, mantra, shared topic, or missing authoring artefact—as evidence for that comparison. Decide the outcome from exact candidate contributions and the later-used consequence.

Here *product* has the Plain management meaning declared in `E.4:4.1`; it is not a technical kind. When a non-framework product is selected, the answer names its direct subject, kind, and the identity, current-state, provision, publication, availability, or other relations used by the decision. Name a maintenance relation only when that stronger claim separately obtains and changes the answer. If a kind or relation that can change the answer is unresolved, keep it as an explicit decision question and do not invent `U.Product`.


A proposed new or substantially revised DPF also needs an answer about its field boundary. That answer says who can first use the framework and for what, which connected problem families and useful results it covers, what the current FPF and admitted DPFs already provide, and what remains uncovered. It compares serious alternatives, tests one representative case that crosses problem families, states where the evidence runs out, and names the change that will require a refresh. Together these must support one independently usable pattern language. One pattern or a narrow authoring slice is not a DPF merely because it has a broad title or a coherent carrier.

If a cheap search, curated reading route, useful contribution to an existing framework, suitable non-framework product, or stop answers the immediate need without settling such a boundary, use that result and stop. Reserve the framework-architecture DRR for a later-used boundary.

When the architecture question is live, use `E.4.PFAD` to state the framework-specific content of one ordinary `E.9` DRR. The decision-maker selects the answer during decision Work; that DRR is its decision record. This practitioner-facing profile locates the questions and answer content inside the DRR, while acceptance remains a separate decision.

## E.4.PFAD:2 - Problem {#problem}

Framework authors repeatedly need to decide whether a recurring practitioner problem calls for a new framework, an existing framework contribution, another product such as a programme, service, or evidence package, a thinner access result, or no new maintained product now. When a framework is selected, later work needs its public field promise, first-edition boundary, FPF Core dependency, problem-family coverage, first patterns and their material relations, representative use, important omissions, and publication or access consequence. Generic decision prose can hide those choices.


A small coherent authoring slice creates a common false positive: its few current patterns and neat structure are mistaken for a field-scale pattern language. Source diagrams create another: one list or hierarchy is copied into the DPF although Methods, Work, subjects, descriptions, capabilities, providers, and cultural change may have different structures. A large framework-specific form creates the opposite problem by making proposal, acceptance, DRR, edition, authoring, quality review, and publication look like one extra decision object.

The useful result is one readable answer whose framework consequences and limits are visible without adding a second decision stage or making cheap exploratory work produce decision paperwork.

## E.4.PFAD:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Discoverability | Authors need a recognizable framework question, but a locator must not become another decision object. |
| Framework scale | A narrow pattern set can be useful, but a broad public framework needs connected problem-family coverage, a first use that does not depend on unpublished authoring context, and a stated reason for later refresh rather than a pattern count. |
| Several structures | A decision needs one coherent practice-architecture answer, but Method, Work, subject, description, capability, provider, and cultural structures need not line up one-for-one. |
| Decision memory | Later work needs rationale and consequences, but the DRR is not the accepted answer, performed authoring, or framework edition. |
| Framework detail | Edition, dependency, pattern placement, relations, omissions, the sources that later authors must be able to revisit, and publication consequences matter, but unrelated quality, naming, and package apparatus must stay conditional. |
| Cheap exit | A suitable non-framework product, small access result, or existing-framework contribution may solve the immediate problem without a framework decision. |
| Relation precision | Initial pattern relations may shape the architecture, but a row or schema does not make those relations obtain. |
| Evolution | The answer needs a reopen condition without turning every refresh concern into a mandatory field. |
| Attainable benefit | A useful method can remain unusable because its audience cannot find, understand, learn or enact it; more explanation can also burden an already prepared reader. |
| Whole cost and distribution | Repeated use can repay learning and authoring, while costs, gains and the ability to pay can fall on different participants. |
| Sharing and independence | Shared methods can reduce duplicate work while accumulating exceptions and propagating changes into otherwise independent uses. |

## E.4.PFAD:4 - Solution {#solution}

### E.4.PFAD:4.1 - Decide whether the architecture question is open {#decide-whether-the-architecture-question-is-open}

Ask whether choosing a framework, a non-framework product, a thinner route, an existing-framework contribution, or stop will settle at least one decision used by later authoring or review:


- the public field promise, a first use that does not depend on unpublished authoring context, or the problem-family coverage of a proposed DPF;
- an intended or existing framework edition;
- an FPF Core or other current edition dependency;
- initial pattern placement or a material relation among those patterns that changes the architecture;
- the direct subjects and identity or change rules for a continuing programme, an admitted service, or a separate editioned result, plus any maintenance relation when later work separately claims or uses it;

- a publication or access consequence; or
- for a proposed DPF Suite, the ecosystem use, which product series may belong, constitution, inclusion and removal rules, identity through change, source return, later-review and retirement conditions, exposure choice, any separate DPF Suite Reference product decision, and any maintenance relation only when separately claimed.


When `E.4.DPF` supplies a preliminary contribution account, use the contributions rather than their carrier as the input. If same-situation comparison shows that exact current FPF or admitted-DPF owners carry every action, first result, return, and source or refresh duty—or exact external results supply them—and no decision above remains, take the smallest useful result and close without PFAD. Keep the architecture question open when exact ownership remains unresolved, a coherent action-bearing remainder survives, or closure would erase a material relation or field or refresh responsibility that changes a later use. Carrier form, role label, shared topic, naming and PatternID state, and counts locate candidate contributions. The four dispositions and later-used consequence determine whether to close or select an outcome.

If none of these decisions and no receiving use are present, take the exploratory result as the answer. If one is present, the decision-maker selects a framework, non-framework product, thinner route, existing-framework contribution, or stop during decision Work, and one `E.9` DRR records that answer. The cheap exit and the architecture decision are alternative entry outcomes.

For every product alternative, use *product* only as the first management cue. Then compare the direct subjects at the same grain: the exact framework or package episteme, System, service arrangement, Method, programme description, carrier, or other admitted result, and the relations that later work will rely on. Use a quality-management, service-management, publication, or content-management scheme as a probe; use the FPF direct-subject patterns to settle the kind. If an unresolved kind can change the selected answer, keep the product proposed and make that kind the next decision question.


### E.4.PFAD:4.1.1 - Choose a contribution through attainable use and its whole cost {#choose-a-contribution-through-attainable-use-and-its-whole-cost}

Use this construction when the architecture choice turns on who can benefit from the proposed content, how that benefit becomes available, or which uses must change together. It supplies grounds for the compact answer in :4.2; it is not another record or an obligatory study before a small repair. If one adequate route already answers the question without a consequential boundary choice, keep the :4.1 cheap exit.

**Start with a useful occasion, not a catalogue of possible mistakes.** Describe a recurring or credibly anticipated situation, the result worth obtaining, the presently available way of obtaining it, and the consequential difficulty. Distinguish frequency of the occasion, frequency of failure conditional on that occasion, severity of its consequence, and the proposed remedy's effect. A frequently encountered task can justify assistance even when mistakes are rare; a rare severe failure can justify protection without being called frequent. Source occurrence is evidence that a method was described, not that the intended population needs another description. State which claims are observed, source-supported, estimated or still hypotheses. Use C.11.DUA to decide which uncertainty is worth investigating.

**Describe the actual reader and performer arrangement.** Separate general and domain education, skill in the relevant work, familiarity with FPF/DPF distinctions, and the means available on this occasion. Preparation can differ for recognizing, performing, checking, adapting and teaching the same Method. Use only differences that could change the arrangement; do not classify people or models by a single rank of intelligence.

| Arrangement | Recover the preparation and means that change this use | Comparison that prevents a false gain |
| --- | --- | --- |
| A human | What the person already understands and can perform; framework familiarity; accessible explanation, practice, feedback and help; the time available | Compare with this person's actual repertoire, including a suitable existing guide or competent provider. More explanation can support learning while burdening a familiar application. |
| A human using an AI tool | The relevant capabilities of each; who retrieves, interprets, chooses, performs and checks; how results cross that division; tool access, waiting and human oversight | Compare the proposed division with the relevant human-only and AI-only alternatives where those alternatives are allowed. Assisted output does not establish the human's acquired capability, and assigning a check to a person does not supply the ability to check. |
| An AI performer | What the selected system can recover and do under its actual context, retrieval, tools, permissions and computation budget; available retained state and any external checking | Compare with its existing performance and supplied context. A brief cue can restore use of an already available method; a longer pattern can supply missing distinctions. A model label establishes neither. |

These are common arrangements, not an exhaustive role taxonomy or three mandatory editions. A learner can later need only a reminder; an experienced practitioner can need the full reasoning when conditions change. If the intended result is the person's independent judgement, keep that result in the comparison instead of substituting a good answer delivered by the tool. If the intended result is obtaining the answer from a provider, do not require every recipient to learn the provider's Method.

**Follow the route by which the benefit could occur.** Begin with the work question the user recognizes, without silently supplying the PatternID. Follow discovery, recovery of the task-relevant distinctions and connections, selection of a suitable action, performance of the Method or obtaining the required result from a capable provider, and the receiving use of that result. E.11 and A.15.11 supply discovery and occasion; C.2.8 makes recovery relative to preparation, accessible material and effort. Find the first necessary contribution that the proposed arrangement cannot supply. It can be a missing method connection, inaccessible explanation, unacquired skill, unavailable assistance, or a result that does not serve the intended work. These require different repairs.

If the contribution cannot be found or its necessary structure cannot be recovered in this arrangement, the promised benefit through that route is unavailable; search and reading can still consume resources. This is a causal constraint on value, not a conversion of structural information into money. More extractable structure can also be irrelevant to the task. Distinguish an observed failed attempt, a reasoned walkthrough and an untested access assumption; unknown performance is not a measured zero.

**Construct serious alternatives for the same result.** Compare the available public method and no addition with the consequential alternatives: repairing discovery; a reminder or checklist for an already possessed capability; a developed pattern or composite; a pedagogical companion; external competent provision; or distinct variants with a small shared supplier. A checklist can prompt a judgement without teaching how to make it. A companion can supply explanation, practice and feedback without creating a different subject Method. E.8:4.2.1.1 assigns their respective content and tests whether teaching can be constructed without inventing the Method. A short route and a full explanation can belong to one architecture.

For a composite, compare the whole result and its necessary connections, not only its available constituents. For an unprepared audience, make learning or external help a real alternative with its costs and availability; do not hide it in an assumed expert reader. Conversely, do not force experts through elementary instruction that changes no relevant result. A result beyond the present capability and budget can warrant a different allocation, staged development or an honest unmet use.

**Compare the whole cost of obtaining and sustaining useful application.** Use a stated horizon and plausible number of users and occasions. Include only terms that can change the decision, but include them where they fall: developing and maintaining the contribution; finding and interpreting it; learning, practice and feedback; obtaining help; adapting and integrating it into work; recurring application, checking and recovery; and responding to consequential changes. For AI-supported work, computation and retrieval are costs alongside human prompting, checking, waiting and correction. Include displaced work and the cost of retaining a capability or dependence when those matter. A free document is not free use.

C.11.CRC compares complete configurations rather than summing isolated pattern merits. C.11.DUA compares added work with attainable gain; C.19.2 limits how much decision apparatus is worth applying. A useful ordinary calculation is one-time acquisition and setup, plus recurring cost over the horizon, plus consequential change and retirement costs. Count shared development once at the chosen population boundary; state any allocation to individuals. Do not charge an author's investment in full to every reader, count the same correction both as expected loss and paid rework, or amortize over an invented infinite audience. Human time, compute, money, delay and serious non-compensable losses need not collapse into one score. Use ranges or break-even conditions when a point estimate would pretend to knowledge.

Compare acceptable result quality and constraints together with these costs. Lower cost for a different or inadequate result is not a saving. Past learning is part of the available starting capability; further learning can create benefits beyond this one application. State those future uses as supported expectations or hypotheses. Identify who pays and who benefits: an aggregate saving can leave the intended user unable to afford adoption. A rare but unacceptable hazard is handled under its governing obligation, not traded away by a small average cost.

**Challenge sharing by an independent change.** Vary one premise that matters to one intended use or audience: a domain criterion, teaching prerequisite, available tool, or required outcome. Determine which explanations, interfaces, dependent uses and release obligations would actually need to change. Common ideas, reused Method descriptions and a common running implementation create different dependencies. Separate files alone do not create independent change; a shared carrier alone does not prove shared semantics.

Compare a shared supplier with a bounded interface, independent variants, and limited deliberate duplication. Retain sharing where it saves enough construction and maintenance while preserving useful independence. Split where accumulating exceptions, migration, compatibility or coordinated releases defeats that gain. C.31 supplies the relevant modularity and reuse characteristics; select those that answer the live question instead of maximizing reuse or requiring every coordinate. E.4.PFR handles edition dependence when that relation actually obtains.

**Spend the next effort where it could change the choice.** Try the smallest consequential uncertainty: can the intended reader find the contribution; can a prepared reader reconstruct a missing join; can a user complete a supported case; does a changed premise force unrelated variants to change? A prospective benefit is a hypothesis that can justify a bounded experiment, not a realized return. Separate a content-recovery probe from an effectiveness or learning trial. In a teaching claim, assisted performance and later independent performance can require different observations. Stop expanding the analysis when the available distinction already selects the next action, or when further inquiry costs more than the decision it could improve.

Return the selected contribution and arrangement, the useful result, preparation and support on which it relies, material costs and uncertainty, the chosen sharing boundary, and the observation that could reverse the decision. These are grounds for the existing :4.2 answer, not an extra universal form.

### E.4.PFAD:4.2 - State the compact framework answer {#state-the-compact-framework-answer}

When the architecture question is open, the framework-specific part of the DRR states:

1. the intended practitioner, public field name and promise, recurring problem, and bounded architecture question;
2. the selected outcome: a new or revised framework edition, a contribution to an existing framework, a non-framework product, a thinner publication or access route, or no new maintained product now; for a non-framework product, also the direct subject kind and the identity, current-state, provision, publication, availability, or maintenance relations actually used by the decision;
3. its field boundary: who can first use it without unpublished authoring context and for what; the connected problem families and useful results; what the current FPF and admitted DPFs already provide and what remains uncovered; serious alternatives, such as splitting or merging the proposed framework, using existing sources directly, contributing to one existing framework, composing exact contributions across several admitted DPFs and FPF, selecting a programme or service, selecting a separate evidence-package episteme, or selecting no new maintained product now; the limits of evidence; and what change will require a refresh;

4. the selected problem-family pattern sets, first patterns and their material relations, representative cross-problem application, and important omissions;
5. which practice structures change the answer and how their Methods, descriptions, patterns, direct subjects, and managed result boundaries fit together. When those structures do not line up one-for-one, use a completed `C.32.MWA` synthesis; use `E.23.CDI` only when capability development for a named Work family changes the answer;
6. the existing or intended-edition boundary, selected FPF Core dependency, and only the other exact edition dependencies required by this answer;
7. the sources to revisit for each important claim, whether the evidence supports, suggests, or only motivates it, the limits of that evidence, and the publication or access consequence; and
8. material alternatives, accepted costs or losses, practical consequences, the first authoring action or stop, and the reopen condition.

For any opened question, record only candidate contributions that can change the outcome. For each, state whether an exact current FPF or admitted-DPF owner carries its action, first result, return, and source or refresh duty; an exact external result supplies it; an action-bearing remainder survives; or ownership remains unresolved. A shared topic or broad framework name can locate candidates; assign a disposition only after exact contribution comparison.

When professional Method coverage can change point 5, the same compact framework answer projects five connected claim groups from points 1, 3, 4, 5, 7, and 8. The projection remains content of that one answer and its one ordinary `E.9` DRR. Fill each group to the grain that changes first use, using a representation suited to the case, before DPF authoring:

1. **Practice truth and first use:** identify every bounded practice claim or promised practice contribution by its exact subject and scope, mark that claim—not the answer as a whole—as obtaining or possible-future, and state practitioner, recurring or anticipated difficulty, sought result, first use, stop or wrong-turn return, qualification window, and receiving decision. Include only non-use boundaries admitted by `F.19`'s grounded-contribution test.
2. **Project and Method positions:** name the direct project subjects, use and environment, materially different solution forms, and Methods under their actual operational, system-change, solution, Method-of-interest, or Method-development relations. Keep incumbent Work, development or trial Work, candidate-practice Work, and intended Work distinct.
3. **Selected structures and correspondences:** include only the Method, Work, subject, transformation-flow, capability/provider, description, contribution, Method-development, and cultural structures whose correspondence, conflict, or non-isomorphism changes the answer.
4. **Pressures and evidence:** keep constraints, conflicts, failures, environment or interest changes, and observed, source-supported, estimated, contradicted, and missing links distinct from causal history and temporal unfolding.
5. **Contribution, subtraction, gaps, and reopen:** apply the four dispositions above, then name each receiving pattern and domain filling still needed, honest omissions and gaps, and the observation that reopens the architecture.

Within an existing-framework contribution or another answer that selects no new framework, distinguish one existing DPF receiving a contribution from a use that composes exact contributions supplied by several DPFs and FPF. Record the latter as cross-DPF composition under the selected one of the five outcomes, optionally exposed through a role-centred view or access route. Decide Suite membership separately.

One answer may contain several bounded practice claims with different truth status. Every selected practice question names the claim or claims it consumes, so an obtaining incumbent-practice claim can coexist with a possible-future candidate-practice claim without backdating the candidate or erasing current incumbent coverage. Independently obtaining A.13 agency claims and actual development or trial Work keep their own status; neither proves that the candidate practice obtains. Public coverage is another claim and remains limited to the exact obtaining or prospective contribution and later package evaluation.

For an obtaining practice claim, name actual recurring difficulties and representative actual Work. A precise Agent-performer branch first supplies A.13's core: the exact admitted System, local agential system-role kind and criterion, classification, obtaining assignment, and needed scope, working situation, and window. Add the agency-characteristic profile only when a Grade, autonomy or profile claim, a criterion-dependent characteristic, or a named assurance use consumes it. A.15.1 then independently admits the actual Work from its performance history, Method, extent, and containment. Only after admission does F.6 supply any precise assignment-bound attribution through that same obtaining assignment. State evidence limits; a missing F.6 relation leaves admitted Work intact and only the attribution unresolved.

For a possible-future practice claim, name intended use, incumbent Work or Method and observed problem evidence, candidate Methods and architecture, realization conditions, a planned representative trial, expected acceptance and failure observations, and reopen conditions. Any incumbent-practice or actual trial-Work claim stays independently obtaining when supported, but the candidate-practice Work, candidate-practice Agents, and current candidate-practice coverage remain unasserted until their own conditions obtain.

For every selected question, name its receiving pattern and the exact bounded practice claim or claims whose values change first use. If a required group or claim-to-question binding is absent at that grain, return a bounded PFAD gap to the architecture decision for completion before DPF authoring. A completed `C.32.MWA` synthesis is used only when several selected structures do not line up one-for-one, and `E.23.CDI` only when capability development changes the answer.

The answer is one identified claim-bearing episteme under C.2.1 and is recorded, with its rationale, in one ordinary E.9 DRR. The decision-maker selects that answer during decision Work. An authorized decision-maker accepts, redirects, rejects, or reopens it through a separately identified acceptance decision. Record that accepting decision separately and hand its exact accepted answer to E.4.DPF.

Common practice questions include:

| Practice question | Pattern that supplies or tests the answer |
| --- | --- |
| What contribution or effect is required? | `A.6.F`; use `C.30.ASV` only when a selected architecture view changes the answer. |
| Which Methods construct a larger Method, and which genuine interfaces matter? | `B.1.5`; use `A.6.M` only for a real module, port, or implemented-interface claim. |
| What changed, and how are the transformation-flow positions related? | `A.3.4`, `E.18`, and `C.30.TFS-REL`. |
| What Work occurred, which Method did it enact, and who performed it? | `A.13` followed by independent `A.15.1` admission; `F.6` only afterward for precise assignment-bound attribution, with the A.13 profile branch only when consumed. |
| Which System has the needed capability, and what did a provider actually contribute? | `A.2.2` plus the applicable Work, provision, or service pattern. |
| What cultural generation, transmission, reconstruction, recognition, selection, retention, or loss matters? | `C.36`. |

If another question changes the answer, name it and the pattern that handles it. A required contribution, transformation, performed Work, capability, provider contribution, or cultural change belongs to its own pattern; `B.1.5`'s complete relation predicate supplies Method parthood.
For a DPF Suite answer, an architecture decision takes effect to constitute the continuing collection. It selects the ecosystem use, which product series may belong, inclusion and removal rules, identity through change, alternatives, practical consequences, and the reopen condition. The same `E.9` DRR records that answer. Publication and availability of the first or a later edition are separate occurrences. A maintained-Suite claim separately identifies the maintenance relation, capable System, any commitment that actually obtains, and the refresh response. For any current or available Suite claim, apply `E.4:4.2`'s direct currentness, availability, and source-return conditions, including return to every product-series state presented as current. When the answer selects exposure, choose an independent Suite route, a bounded projection in a current DPF Suite Reference edition with source return, or a neutral combined carrier. Constituting and including the Reference product series, admitting its editions, publishing them, making them available, maintaining them, and refreshing their answers remain separate decisions and claims. Record a proposed result use or future constraint as such; apply `E.4.PFR` after edition-level case facts establish a dependency or compatibility relation.


For an existing-framework contribution, non-framework product, thinner route, or stop, state only the parts needed to explain that outcome and the later-used decision. A selected product still names its direct subjects and the relations used; a proposed product with an unresolved kind says so. The selected outcome determines which field-assessment or package content applies.


When the architecture keeps, merges, removes, reuses, or omits a load-bearing contribution, record the `E.8:4.1.3` same-situation disposition and the action or result that changed. Preserve a difference when it changes action at comparable effort without adding an unsupported or needless burden. A narrower label or example alone is not that difference.

When the answer treats a promised problem family as covered by a result supplied from outside the framework, name the exact result, its exact relied-on content and direct kind, supplying product and exact edition or current state, receiving use, practical discovery route, and every currentness or availability condition that can change that use. State that the result remains external, and state maintenance only when it changes the receiving use. When the receiving use requires an availability or compatibility result, name that exact result and its exact basis. If those facts are absent, or the result does not answer the promised use, record a gap or omission rather than relabelling the result as framework content, a MethodDescription, or source evidence. When the selected keep, merge, removal, profile, external reliance, or omission materially changes the stable set for a promised problem family, obtain a current `E.4.DPF.DA` `D12DomainProblemFamilyCoverageAdequacy` result for the resulting exact DPF or LPF edition. Reuse a matching current result while that exact resulting edition and basis are unchanged. Do not require proof that a revisit occurred.


Keep the ordinary `E.9` grounds, sources, affected loci, rationale, and consequences in the same DRR. Add naming, quality, admission, currentness, or package details only when they change this answer or a named later use requires them. Each added claim remains under the pattern that defines, constrains, or tests it and appears in PFAD for that named use.

### E.4.PFAD:4.3 - State initial pattern relations directly {#state-initial-pattern-relations-directly}

When an initial pattern relation changes the selected architecture, state the relation and its participants as an ordinary assertion. For example: `Pattern A frames the recurring problem; Patterns B and C specialize its reusable move for two stated situations.` Use the pattern that defines or constrains each relation function.

For the architecture answer, use the direct assertion under the relation's own predicate. Add an optional `E.4.PFR` row when a named maintenance use needs that representation.

### E.4.PFAD:4.4 - Keep the answer, DRR, authoring, and publication distinct {#keep-the-answer-drr-authoring-and-publication-distinct}

The decision-maker selects the answer during decision Work. The `E.9` DRR records that answer and its rationale. An authorized decision-maker accepts, redirects, rejects, or reopens it through a separately identified acceptance decision. Later authoring follows an accepted answer. A framework edition is the pattern-language episteme assembled from accepted sources; any maintenance relation obtains separately. Publish or project claims about these objects in the selected form—for example, an ADR-like document, site, or PDF—and identify its presentation carrier separately when needed.

When the answer uses `C.32.MWA` or `E.23.CDI`, keep each proposed Method distinct from the pattern that describes it, the Work in which it is performed, the result of that Work, the framework answer, the DRR, and the resulting edition. Use a proposal or evidence locator to find the supporting material.

Use `C.32.PAD` only when the question is an exact project architecture decision about a named composite project Work, and use `C.32.ADR` only to project that project decision. For an ordinary framework answer, publish the selected decision episteme or a reader-specific projection through `E.17` and `E.24.PUB`. None of these is a mandatory stage of principle-framework authoring.

## E.4.PFAD:7 - Conformance Checklist {#conformance-checklist}

| Check | Passing condition |
| --- | --- |
| CC-PFAD.1 Opening discriminator | @fact:CC-PFAD-1 A later-use field promise, edition, dependency, pattern placement or material relation, non-framework direct subject or identity/change rule, separately claimed maintenance relation, or publication or access decision makes the architecture question live. @status:spec/done |
| CC-PFAD.1a Carrier-neutral opening | @fact:CC-PFAD-1a A live question may arrive before a product name, PatternIDs, or pattern bodies. Carrier, role, topic, cue, and count supply evidence for locating candidate contributions. Exact subtraction plus a later-used consequence opens PFAD; when every contribution is carried or supplied externally and no such consequence remains, the cheap result closes. @status:spec/done |
| CC-PFAD.2 Cheap exit | @fact:CC-PFAD-2 A suitable available non-framework result or service, route, existing-framework contribution, or stop that settles none of those decisions closes without PFAD or a DRR. @status:spec/done |
| CC-PFAD.3 One decision record | @fact:CC-PFAD-3 During decision Work, the decision-maker selects a new or revised framework, contribution to an existing framework, non-framework product, thinner publication or access route, or no new maintained product now; one ordinary `E.9` DRR records it. @status:spec/done |
| CC-PFAD.3a Field boundary | @fact:CC-PFAD-3a A selected new or substantially revised DPF has a reviewed field-boundary assessment. It names the practitioner and a first use that needs no unpublished authoring context, connected problem families and results, what the FPF and admitted DPFs already provide, what remains uncovered, serious alternatives, representative cross-problem use, evidence limits, the decision that uses the assessment, and the later observation that reopens it. @status:spec/done |
| CC-PFAD.3b Coverage, contributions, and omissions | @fact:CC-PFAD-3b The answer names selected problem-family pattern sets, first patterns and material relations, one representative cross-problem application, important omissions, and the sources to revisit for important claims; no count or authoring slice proves adequacy. For each load-bearing contribution that it keeps, merges, removes, reuses, profiles, supplies externally, or omits, it applies `E.8:4.1.3` and names the resulting action. An external return names the exact result, exact relied-on content, and direct kind, supplying product and exact edition or current state, receiving use, discovery route, and material currentness or availability conditions, and says that the result remains external. For any required availability or compatibility result, name that exact result and its exact basis; an insufficient return remains a gap or omission. After a material promised-family change, the answer obtains the current `E.4.DPF.DA` `D12DomainProblemFamilyCoverageAdequacy` result for the resulting exact DPF or LPF edition and reuses it only while the exact resulting edition and basis remain unchanged, without asking for evidence that someone revisited it. @status:spec/done |
| CC-PFAD.3c Professional-practice projection and several structures | @fact:CC-PFAD-3c When professional Method coverage changes the answer, the same compact answer projects five connected groups by value: claim-scoped practice truth and first use; project and Method positions; selected structures and correspondences; pressures and evidence; and contribution, subtraction, gaps, and reopen. One answer may carry several bounded practice claims with different obtaining or possible-future status, and every selected question names the claim or claims it consumes. The answer, one ordinary E.9 DRR that records it, and the separately identified accepting decision remain distinct. A missing required group or claim-to-question binding returns a bounded PFAD gap before DPF authoring. `C.32.MWA` is used only when several selected structures do not line up one-for-one and `E.23.CDI` only when capability development changes the answer. `B.1.5`'s complete predicate supplies Method parthood. Realize the five claim groups by value in the one answer and ordinary DRR even when the source begins as a fixed view list, layout, or Method hierarchy. @status:spec/done |
| CC-PFAD.3d Direct-subject account | @fact:CC-PFAD-3d *Product* remains Plain management wording. A selected product names every direct subject and the identity, current-state, provision, publication, availability, or other relation used by the answer. It names a maintenance relation only when that claim separately obtains and changes the answer. A programme case also distinguishes any provider System, maintenance relation, accepted commitment, or admitted service state that independently obtains, together with bounded Work and evidence-package epistemes. An unresolved kind remains an explicit question, not `U.Product`. @status:spec/done |
| CC-PFAD.3e Exact subtraction and composition | @fact:CC-PFAD-3e Every outcome-changing candidate contribution is classified as carried by an exact current owner, supplied by an exact external result, an action-bearing remainder, or unresolved through same-situation action, first-result, return, and source-or-refresh comparison. A broad owner counts only when it carries those values. An existing-framework answer distinguishes one DPF receiving a contribution from cross-DPF composition. Record composition under one of the five outcomes and submit Suite membership to the Suite decision. @status:spec/done |
| CC-PFAD.4 Compact payload | @fact:CC-PFAD-4 The DRR carries only the applicable content groups in `E.4.PFAD:4.2` and ordinary E.9 grounds and rationale; the selected outcome determines the applicable fields for a non-framework product, thinner route, or stop. @status:spec/done |
| CC-PFAD.5 Direct relation assertions | @fact:CC-PFAD-5 Relations among initial patterns are stated directly under their actual relation functions; an optional PFR row represents them for a named maintenance use. @status:spec/done |
| CC-PFAD.6 Object boundaries | @fact:CC-PFAD-6 Answer, acceptance, DRR, authoring Work, Method results, edition, and publication remain distinct; proposal locators serve discovery. For a programme answer, the exact persisting subjects, any provider System, maintenance relation, accepted commitment, or admitted service state that independently obtains, each bounded inquiry Work occurrence, and each evidence-package edition remain distinct. @status:spec/done |
| CC-PFAD.7 Conditional apparatus | @fact:CC-PFAD-7 Naming, quality, admission, currentness, and package details appear only when they change the answer or serve a named use. @status:spec/done |
| CC-PFAD.8 Reopen condition | @fact:CC-PFAD-8 The DRR states what change in field boundary, framework architecture, evidence, or receiving use requires reconsideration. @status:spec/done |
| CC-PFAD.9 DPF Suite decision | @fact:CC-PFAD-9 A selected Suite answer states the ecosystem use, which product series may belong, Suite constitution, inclusion and removal rules, identity when product series change, source return, later-review and retirement conditions, exposure choice, alternatives, consequences, and reopen condition. It separately states edition-to-product belonging and whether a DPF Suite Reference product series has been constituted and included. A maintained-Suite or maintained-Reference claim separately states its supporting maintenance relation, refresh response, and evidence. Record belonging as collection membership; assert holonhood, constructive parthood, dependency, or compatibility only through its own complete predicate. @status:spec/done |


When audience access, whole cost or shared change can alter the architecture answer, apply :4.1.1: keep the promised result fixed, identify relevant preparation and support, compare an adequate available alternative, and expose the decisive cost or change dependency. This is a conditional substantive comparison, not a required numerical score.

## E.4.PFAD:9 - Consequences {#consequences}

Authors get a recognizable framework question, one cheap stop rule, one readable decision account, and one next action. Later authors can recover the public field promise, problem-family coverage, representative use, edition boundary, dependencies, initial pattern architecture, omissions, sources to revisit, publication or access consequence, rationale, and reopen condition without reconciling two decision objects.

A new or substantially revised DPF carries more architecture work than a suitable non-framework product, thin route, or existing-framework contribution, and the PFAD profile adds one locator to maintain. That cost makes field-scale evidence explicit before a public pattern language is selected. Conditional naming, package, quality, and machine-readable detail stays out until a named use needs it.

## E.4.PFAD:12 - Relations {#relations}

- **Uses:** `E.9` to record the one bounded answer selected by the decision-maker during decision Work.
- **Uses:** `C.11.DUA`, `C.11.CRC` and `C.19.2` for worthwhile comparison and its burden; `C.2.8` for attainable structure; `C.31` for the modularity and reuse questions that matter.
- **Coordinates with:** `E.8:4.2.1.1`, `E.11` and `E.11.PFP` for method explanation, pedagogical companions and usable publication/access routes.
- **Uses:** `E.4`, `E.4.DPF`, and `E.4.DPF.DA` for framework scale, authoring, field coverage, and package assurance; uses `E.4:4.2` when one decision selects a DPF Suite and `E.11.DSG` when that Suite has a separately constituted DPF Suite Reference product series.

- **Uses:** `C.32.MWA` when several practice structures need one readable synthesis; uses `E.23.CDI` only when capability development for a named Work family changes the answer.
- **Uses:** `A.6.RCD`, `A.6.REL`, and the exact relation patterns for material relation assertions among initial patterns.
- **Coordinates with:** `A.22`, `C.30.STRAT`, `B.1.5`, `A.15.1`, `C.30.AD`, and `C.36` for selected structures and exact architecture distinctions.
- **Coordinates with:** `E.4.PFR` for optional relation and edition maintenance representations.
- **Coordinates with:** `C.32.PAD` for an exact project architecture decision, `C.32.ADR` for its ADR-like projection, and `E.17` with `E.24.PUB` for publication of an ordinary framework answer.
- **Coordinates with:** `F.18`, `G.2`, `G.11`, `E.21`, `E.23`, and `E.19` only when naming, source synthesis, refresh, improvement, or admission is current for the selected answer.


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/E-4#root, spec://ai.lev/fpf-spec/contract/E-9#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/E-4-DPF#root, spec://ai.lev/fpf-spec/contract/E-4-PFR#root, spec://ai.lev/fpf-spec/contract/C-32-MWA#root, spec://ai.lev/fpf-spec/contract/C-32-PAD#root, spec://ai.lev/fpf-spec/contract/C-32-ADR#root, spec://ai.lev/fpf-spec/contract/E-17#root, spec://ai.lev/fpf-spec/contract/E-24-PUB#root, spec://ai.lev/fpf-spec/contract/F-18#root, spec://ai.lev/fpf-spec/contract/G-2#root, spec://ai.lev/fpf-spec/contract/G-11#root, spec://ai.lev/fpf-spec/contract/E-21#root, spec://ai.lev/fpf-spec/contract/E-19#root, spec://ai.lev/fpf-spec/contract/F-19#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/C-32-MWA#root, spec://ai.lev/fpf-spec/contract/E-11-DSG#root, spec://ai.lev/fpf-spec/contract/E-4#root, spec://ai.lev/fpf-spec/contract/E-4-DPF#root, spec://ai.lev/fpf-spec/contract/E-4-DPF-DA#root, spec://ai.lev/fpf-spec/contract/E-4-FPF#root, spec://ai.lev/fpf-spec/contract/E-4-PFR#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/E-4-PFAD
