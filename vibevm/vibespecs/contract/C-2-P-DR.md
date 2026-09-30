# C.2.P.DR - Repair Claims Based on Declarative Form Alone (Declarative Representation Precision Restoration) {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** C.2.P precision-restoration child pattern for declarative-representation overread
> **Status:** Stable
> **Normativity:** Normative unless a section is explicitly informative

## C.2.P.DR:0 - Use this when {#use-this-when}

Use this pattern when a declarative representation is about to guide action, reliance, gate, release, evidence, method, mechanism, work, or pattern-application claims by its shape alone.

**First useful move.** Recover the visible expression or artifact; exact current direct object or relation; any current representation or correspondence use; current source or publication relation; tempting stronger action claim; recovered subject pattern; retained use; blocked stronger action claim; and stop or reopen condition. Return the repaired wording and needed stop or subject-pattern return. Use a `DeclarativeRepresentationRepair` note only when the receiving use needs the repair to remain inspectable.

**Quick example.** A heat-flow graph in a reactor-cooling review can show preserved and lost flow relations. It does not authorize a valve change by graph shape. The repair keeps the graph path as graph structure, returns release or gate reliance to the gate, source, and evidence patterns, and blocks the hidden work-permission claim.

Use this pattern especially when:

- a graph path, `PathSlice`, flow valuation, transformation-flow structure line, or graph expression over such a structure is overread as a prescribed work route or workflow;
- an `A.10` evidence path is overread as approval, permission, release, gate passage, or assurance;
- a query, access path, query plan, table, dashboard, schema, checklist predicate, or API description is overread as method, work plan, performed work, gate, permission, or proof;
- a publication face, source-chain relation, carrier file path, mathematical representation, method-description representation, or FPF pattern relation is overread as call, dispatch, invocation, send, receive, route, or pattern application;
- method-like wording hides whether the current claim concerns `U.Method`, `U.MethodDescription`, formal substrate, mathematical-lens use, `U.Mechanism`, `U.WorkPlan`, dated `U.Work`, evidence relation, source relation, or quote-only source wording.

**What goes wrong if missed.** The representation appears to do work it cannot do. A path "routes" a decision, a query "calls" a pattern, a dashboard "authorizes" release, a checklist predicate "runs" a process, an evidence path "permits" action, or a program-looking text becomes "the method" without recovering method semantics, method description, formal substrate, mechanism, work plan, work, evidence, or source-use relation.

**What this buys.** The working reader keeps a visible expression useful without making it magical or hiding its subject pattern. Graph paths and structures, evidence or provenance relations, queries and formal objects, publication faces, and pattern relations keep their own kinds. When a graph, file, tile, table, or face represents one of them, the exact representation or correspondence use is stated separately. For method-like wording, the reader identifies the direct object or relation, any represented object or claim, and the exact relation that gives the expression its current use before selecting method, method description, formal substrate, mechanism, plan, work, evidence, source, gate, or release guidance.

**Not this pattern when.**

- If the graph path, `PathSlice`, or flow valuation is already current as graph structure, use `E.18` directly.
- If the evidence relation or provenance relation for a claim is already current, use `A.10` directly.
- If the publication face or source-use relation is already current, use `E.17`, `E.17.EFP`, `C.2.P`, or the direct publication pattern.
- If the current claim concerns a semantic way of doing, use `A.3.1`; if it concerns the description of that way, use `A.3.2`.
- If the current claim concerns operation algebra, laws, admissibility predicates, transport, audit, or governing-definition assignment, use `A.6.1` or `E.20`.
- If the current claim concerns planned work or dated work, use `A.15.2` or `A.15.1`.
- If the word is only quoted source wording or ordinary navigation prose with no FPF-governed claim, keep it quote-only or ordinary.

## C.2.P.DR:1 - Problem frame {#problem-frame}

FPF work meets many declarative-looking expressions and many direct objects or relations: graph and table artifacts; paths and selected structures; state predicates and values; dashboard and publication faces; evidence, provenance, source, and pattern relations; formal substrates; and method descriptions. Some visible expressions represent a separately governed object or claim; other named items are themselves the current direct object or relation. Their common declarative appearance does not make them peers in one kind.

The recurring failure is a category shift. Because some representations look like paths, pipelines, calls, dispatches, states, gates, or control programs, the prose starts granting them operational effects. A representation then seems to authorize work, pass a gate, enact a method, prove a result, release a system, or select a pattern by its shape alone.

This pattern repairs that shift. It does not build a general theory of representation. It only restores the exact FPF-governed object, relation, or claim and its subject pattern when declarative-looking wording is overread as imperative or operational.

## C.2.P.DR:2 - Problem {#problem}

Without this repair:

1. **Graph path becomes work route.** A path or path slice in `E.18` is treated as an ordered work narrative, even when no work occurrence, work plan, or method description is current.
2. **Evidence path becomes permission.** An evidence relation or provenance relation is treated as approval, gate passage, release, safety, or authority rather than as evidence for a named claim or effect.
3. **Query becomes method.** A query, access path, query plan, or dashboard is treated as the semantic way of doing, rather than as a representation, method description, evidence relation, source relation, or ordinary source wording.
4. **Pattern relation overread as dispatch.** Pattern application prose starts saying that one pattern exits to, routes to, calls, invokes, receives, owns, or dispatches another, hiding declarative pattern relations and subject pattern selection.
5. **Programming-paradigm label becomes ontology.** Imperative, functional, logical, constraint, object-centric event, effect-handler, pipeline, orchestration, or workflow wording is treated as the FPF kind rather than as one representation style or source label.
6. **Mechanism, method, and work collapse.** A method-like expression is repaired to `method` or `mechanism` by vocabulary rather than by the current claim: way of doing, description, formal substrate, law-governed mechanism, plan, occurrence, evidence, or quote-only wording.

## C.2.P.DR:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Representation usefulness and action overread | Graphs, queries, predicates, and dashboards are useful precisely because they expose structure; their shape does not supply hidden work, permission, or release. |
| Legitimate path words and metaphor repair | `A.10 evidence path`, `E.18` graph path, and carrier file paths may be legitimate; `path` becomes a defect only when it carries a stronger action or authority claim by metaphor. |
| Method generality and subject discipline | Algorithms, programs, solver models, proofs, SOPs, and process models can all be useful, but first identify the direct object or relation, the current claim, and any exact representation use. Select `U.MethodDescription` only after the claim-bearing episteme passes the A.3.2 membership test; representation form alone selects nothing. |
| Declarative and imperative labels are too crude | Current programming and process practice includes effects, handlers, constraint models, object-centric events, e-graphs, and process theories; the repair names the direct object or relation, current claim, any representation use, and subject pattern rather than choosing one programming-paradigm slogan. |
| Subject pattern and local repair | When `E.18`, `A.10`, `A.3.1`, `A.3.2`, `A.6.1`, `A.15.2`, `A.15.1`, `E.17`, or another pattern already governs the current claim, this pattern names only the overread and leaves the next claim to that pattern rather than duplicating it. |

## C.2.P.DR:4 - Solution {#solution}

Repair declarative-representation overread by separating the visible expression, the direct object or relation, and any representation use before naming the subject pattern for the current claim.

The repair order is:

1. **Name the visible expression or artifact.** Quote or identify the graph highlight, file, query text, predicate display, dashboard tile, table, publication face, path diagram, carrier path, mathematical expression, method-description expression, or pattern sentence that prompted the overread.
2. **Recover the exact current direct object or relation.** Name the graph structure, `PathSlice`, flow valuation, evidence or provenance relation, state predicate or value, query or formal object, publication face or occurrence, formal substrate, claim-bearing episteme, source relation, carrier-side object, pattern relation, or other direct outcome under its own governor. This is a list of alternative recovery outcomes, not representation kinds in one ontology.
3. **Distinguish the direct object from any representation or correspondence use.** When the visible expression represents a separately identified object or claim, name the exact relation and target. When the direct object or relation itself is current and no separate representation claim is needed, keep that direct use; do not relabel the direct object as a representation kind. Record `none` only when the receiving use needs an inspectable account of that distinction.
4. **Recover source or publication relation when current.** If a face, source chain, generated explanation, copied text, dashboard, file path, or publication unit is current, use the publication pattern or source-use pattern governing that relation.
5. **Name the tempting stronger action claim.** Say what the visible expression is being asked to do by resemblance: route, call, dispatch, invoke, run, flow, send, receive, authorize, release, prove, prescribe, execute, select, pass a gate, or record work.
6. **Select the subject pattern.** Use the direct pattern when the object or relation is already recovered; otherwise use this pattern only long enough to recover the direct outcome, any representation use, and the blocked stronger claim.
7. **State retained use.** Keep the weaker useful use: graph structure, evidence relation, source-finding, state predicate, publication face, exact representation use, formal-substrate input, candidate method reading, or pattern relation.
8. **State the blocked stronger action claim.** Block only the stronger claim that is not recoverable.
9. **Stop or reopen.** Stop when the subject pattern can carry the next claim. Before stopping, ask what claim, evidence relation, gate relation, safety relation, method relation, work relation, or source relation would become less reviewable if the visible expression were accepted as the stronger claim. Reopen if a later source changes the visible expression, direct object or relation, representation relation or target, source currentness, subject pattern, or intended use.

### C.2.P.DR:4.1 - DeclarativeRepresentationRepair note {#declarativerepresentationrepair-note}

Use this compact note only when the receiving use needs an inspectable repair of FPF-governed wording:

```text
DeclarativeRepresentationRepair:
  VisibleExpressionOrArtifact:
  CurrentDirectObjectOrRelation:
  RepresentationOrCorrespondenceUse: <exact relation and represented target> | none
  SourceOrPublicationRelation:
  TemptingStrongerActionClaim:
  RecoveredGoverningPattern:
  RetainedUse:
  BlockedStrongerActionClaim:
  StopOrReopenCondition:
```

The ordinary result is the repaired wording, exact direct outcome, any current representation use, retained use, blocked stronger claim, and needed stop or reopen condition. The optional note records these values when the receiving use needs them to remain inspectable. If the subject pattern already supplies a suitable record, use it without duplicating the repair note here.

Use four plain questions before the claim-and-pattern table: What visible thing am I looking at? What direct object or relation is current? What, if anything, does it represent? What stronger action claim must remain blocked?

| Visible expression or artifact | Exact current direct object or relation | Representation or correspondence use | Stronger action claim blocked |
| --- | --- | --- | --- |
| highlighted graph path | exact E.18 graph path or `PathSlice`, with any flow valuation kept separate | the graphic rendering corresponds to that path when the relation is current; otherwise `none` when the `PathSlice` itself is under inspection | no prescribed route, valve work, or release by the highlight |
| dashboard tile | exact status or state value with its bearer and value frame, plus any current source or publication relation | the tile represents that value only through an exact current relation; otherwise `none` when the publication face itself is the direct object | no gate passage or release permission from green appearance |
| evidence-path expression | descriptive A.10 evidence-provenance path for the named claim or bounded use, citing independently established direct relations | a diagram may represent that descriptive path through an exact current correspondence; otherwise `none` when the path itself is under inspection | no approval, permission, assurance, or release from path shape |
| solver file | exact publication form or carrier-side object, and whichever formal substrate, claim-bearing episteme, method, mechanism declaration, plan, run, or evidence relation is independently current | the solver expression corresponds to separately identified claims or a formal object when that relation is stated; otherwise `none` | no method, mechanism, performed work, result, or evidence by file form or executability |
| publication table | exact publication face or form and source relation, with table values or claims kept under their subject patterns | the table corresponds to a separately identified object or claim only when the exact relation is current; otherwise `none` | no evidence, approval, gate passage, or action authority from table layout |

### C.2.P.DR:4.2 - Subject pattern selection {#subject-pattern-selection}

| If recovery shows... | Use this subject pattern | Keep this boundary |
| --- | --- | --- |
| graph object, graph path, `PathSlice`, crossing, flow valuation, transformation-flow structure relation, or graph expression over that structure | `E.18`, `E.18.2`, or `E.18.1` when P2W carry-through is current | Graph structure or path structure is not work route, method narrative, evidence result, or pattern dispatch by layout. |
| evidence relation or provenance relation for a claim, effect, or reliance use | `A.10` | Evidence path is not approval, permission, gate passage, release, safety, work occurrence, or assurance by itself. |
| state, status value, readiness, validity, or predicate-like value whose bearer and value frame is hidden | `A.19.SPR` or the direct status-value or state-value pattern | A predicate or state-like value is not a workflow, gate, or proof unless the subject pattern says so. |
| publication face, source expression, generated explanation, dashboard face, publication unit, or source-chain relation | `E.17`, `E.17.EFP`, `C.2.P`, `A.15.4`, or source-use pattern named by value | Publication and source visibility do not create work, evidence, authority, release, or gate passage. |
| mathematical representation, formal object, formal substrate, invariant, or mathematical-lens output | `A.6.0`, `C.29`, or direct mathematical pattern | Mathematical representation is not method, mechanism, proof of project result, or work execution until that claim is separately recovered. |
| context-local semantic way of doing | `A.3.1 U.Method` | A method claim is not closed by code, diagram, proof script, plan, run, or mechanism declaration; use `E.10.ARCH:3.1` only to recover the project concern and then recover each linked typed value under its own subject pattern. |
| already identified `U.Episteme` with one admitted `U.Method` as its exact `EntityOfConcern` and at least one substantive claim about that method as a way of doing | `A.3.2 U.MethodDescription` | Code, SOP, proof-script, solver-model, process-model, protocol, recipe, and diagram forms are clues only. A name, citation, approval, runnable form, or representation correspondence does not establish membership. |
| law-governed operation algebra, laws, admissibility predicates, transport, audit, realization, or governing-definition assignment | `A.6.1` and `E.20` | Mechanism meaning is not selected by saying "algorithm" or "method"; it needs mechanism fields. |
| planned work, intended window, resource budget, acceptance criterion, or source “role requirement” | `A.15.2 U.WorkPlan` for the plan. Resolve a “role requirement” separately to its exact local system-role kind, separate System-classification judgment, future assignment condition, capability, participant relation, or other direct condition; if unresolved, use `E.10.ROLE`. | A plan is not a Method, MethodDescription, evidence, gate passage, performed Work, or assignment occurrence. A required kind or condition does not create the future assignment. |
| exact dated Work occurrence | Recover every exact actual performer and its obtaining A.2.1 system-role assignment through A.13, then let `A.15.1 U.Work` independently identify the dated occurrence, enacted Method, time, and containing System. A representation claiming the exact Work keeps every actual performer named or recoverable. Keep the underlying assignment facts recoverable; include an assignment identifier in the representation only when the receiving use needs it. Add an F.6 relation through that same obtaining assignment only when the representation or receiving use expressly represents precise assignment-bound attribution. Missing or failed F.6 leaves the Work intact and blocks only that attribution. | The Work occurrence is not its trace, record, binding, resource use, result, diagram, plan, MethodDescription, source cue, or evidence path. |
| run trace or performed-work record | `C.2.1` for the exact trace or record episteme, plus its direct description, publication, source-use, or evidence-use pattern only when that claim is current | The episteme may designate exact `W`, `RA`, holder `S`, and `performedUnderAssignment(W, RA)` when it makes that attribution; it neither is the Work occurrence nor makes the relation obtain. |
| concrete parameter or participant binding | the exact direct subject-relation pattern, or `A.6.1` for one independently identified operation application and its actual argument or result binding | A declaration, call position, trace field, or type-compatible token establishes no actual binding. |
| performed resource use | the exact direct resource-use relation involving the already identified Work occurrence; use `B.1.6` only when aggregation is current | Resource use is a separately obtaining relation, not a Work field, record field, or result. |
| result or output | identify the exact result entity or episteme first; use `A.15.PROD` when production, entity inception, or production completion is current, and `A.6.RCD` only when the needed direct result relation has no current governor | A binding, record field, Work occurrence, or nearby output label does not identify the result or establish production. |
| FPF pattern application, pattern relation, neighboring-pattern relation, or placement cue | `E.8`, `F.19`, `E.10.ARCH`, or the direct pattern relation named by value | Pattern relations are declarative references or applications. Exit, receiver, route, call, owner, home, or dispatch wording must express a clear ordinary or technical relation; wording alone supplies no action or control semantics. |
| quoted source wording or ordinary navigation | quote-only or ordinary prose | Do not repair ordinary words into FPF terms when no FPF-governed claim is being made. |

### C.2.P.DR:4.3 - Legitimate path and route settlement {#legitimate-path-and-route-settlement}

`path` is not banned.

`A.10 evidence path for <claim, effect, or use>` is legitimate when the evidence relation or provenance relation for the named claim, effect, or reliance use is current. `E.18` graph path and `PathSlice` are legitimate when the graph object, path, slice, crossing, or flow valuation is current. Carrier file paths, URLs, mathematical paths, and quoted source paths are legitimate when their notation, source-use function, or use relation is current.

The defect is not the word. The defect is hidden ontology: the sentence treats a representation as if something literally ran, flowed, executed, authorized, released, proved, selected, or prescribed action without first naming the exact direct object or relation and its subject pattern.

When the representation is route-shaped, loop-shaped, graph-shaped, diffusion-like, or workflow-like, ask first which object is current:

| Current object | Subject pattern |
| --- | --- |
| constraint-governed `U.Structure` across several constrained loci | `A.22.CGUS` |
| transformation-flow structure, path, path slice, crossing, guard, or valuation | `E.18` and `E.18.3` when unfolding use is current |
| description, diagram, table, graph, route card, slide, README line, or narrative that renders the structure | `A.22.CGUS:4.4` for descriptions of a qualified CGUS and post-qualification demonstrative slices, including the wording `ConstraintGovernedUnfoldingStructureDescription@Context` or `DemonstrativeUnfoldingSlice@Context`; `A.6.3.NAR` for narrative rendering; `E.17` for publication; or the direct description subject pattern |
| reusable semantic way of doing, or a claim-bearing episteme that passes the A.3.2 MethodDescription membership test | `A.3.1` for the method; `A.3.2` for the qualifying episteme |
| work plan, work readiness, or performed work | A.15 family |
| evidence, assurance, gate, decision, architecture, publication, or currentness-refresh claim | the subject pattern for that claim |

Do not repair route-shaped wording by replacing it with another route-shaped word. Always recover the visible expression, exact direct object or relation, representation or correspondence use or `none`, retained use, blocked stronger action claim, subject pattern, and stop or reopen condition. When the representation use is `none`, do not require a represented target, preserved and lost structure, or a mathematical-lens admissible-use account. When an exact representation, mathematical-lens, or selected-structure use is current, also name its target, the preserved and lost structure, and the admitted and blocked uses required by C.29 or that structure's subject pattern.

### C.2.P.DR:4.4 - Method, algorithm, mechanism, plan, and work settlement {#method-algorithm-mechanism-plan-and-work-settlement}

Do not repair `algorithm`, `program`, `solver`, `proof`, `recipe`, `method`, `workflow`, `process`, `procedure`, `access path`, `query plan`, or `control strategy` by choosing one fashionable replacement.

**Method-description membership guard.** A code file, SOP, proof script, solver model, process model, protocol, recipe, diagram, or query plan is only a representation clue. First identify the claim-bearing episteme under C.2.1. Apply A.3.2 only when that same episteme has one admitted `U.Method` as its exact `EntityOfConcern` and at least one claim says how that method is done, such as its transformation or enactment concern, applicability, precondition, intended effect or preserved condition, bound, generic participant meaning, or internal method composition. A name, author, citation, approval, file form, runnable configuration, or representation correspondence alone is a near-miss. If the test fails, do not assign `U.MethodDescription`; keep the representation, publication, plan, dated work, result, formal substrate, mechanism declaration, evidence, or source use with its subject pattern. A representation or publication change does not decide membership. If claim content, exact method, or effective reference scheme changes, C.2.1 first identifies the resulting episteme; then apply A.3.2 to that individual.

Recover what the source is actually about and what it asserts:

| Current claim | Subject pattern |
| --- | --- |
| context-local semantic way of doing a transformation or enactment | `A.3.1 U.Method` |
| transformation or enactment kind stated inside a current method claim | keep it as one method-identity field or claim content under A.3.1; it is not a peer `U.Method` |
| independently grounded actual bounded change | `A.3.4 U.Transformation` |
| possible, required, desired, intended, planned, predicted, modeled, or asserted change | keep it as claim content under the exact requirement, architecture, capability-gap, functional-view, method, work-plan, dynamics-model, publication, or other subject pattern; wording alone admits no `U.Transformation` |
| already identified episteme whose exact `EntityOfConcern` is one admitted `U.Method` and whose claims include at least one substantive way-of-doing claim | `A.3.2 U.MethodDescription` |
| formal substrate, signature, postulates, laws, or mathematical declaration | `A.6.0`; use `C.29` when mathematical-lens use is current |
| operation algebra, admissibility predicates, transport, audit, realization, or mechanism-governing-definition assignment | `A.6.1` and `E.20` |
| planned work | `A.15.2 U.WorkPlan` |
| dated performed work | `A.15.1 U.Work` |
| evidence relation or provenance relation for a claim | `A.10` |
| wording quoted from source with no FPF-governed use | quote-only source wording |

**Cooling contrast.** A reusable cooling procedure can be `U.Method` only after the context-local way of doing, its transformation or enactment kind, transformed referent or structure, preconditions, and intended effects are recovered. “Required cooling effect” alone is claim content, not a method. If a later cooling episode actually changes the governed loop state, that occurrence remains a separate A.3.4 `U.Transformation` and needs its own changed referent, boundary, conditions, actual facts, and continuity or reidentification basis.

When the source label hides method, mechanism, formal-substrate, work, evidence, gate, result, or temporal claims, use `E.10.ARCH:3.1` to state the project concern in ordinary words, then identify each exact object and claim separately. Use this pattern to repair only the representation overread and name the subject pattern for the current claim; linked values remain under their own subject patterns rather than becoming one representation-repair claim.

### C.2.P.DR:4.5 - Programming-paradigm and process-model settlement {#programming-paradigm-and-process-model-settlement}

Imperative, functional, logical, constraint, object-centric event, effect-handler, pipeline, orchestration, Declare-style, SQL-like, e-graph, hypergraph, or process-mining wording is a clue to identify the visible expression, direct object or relation, any representation use, and current claim. It is not a decision procedure by itself.

Current practice makes the old contrast between imperative and declarative labels too weak as a final ontology:

- constructor and process-theory lines keep computation, information, dynamics, and procedure close to possible or impossible transformations and compositional realization;
- scoped effects and handlers separate operation syntax, semantic handling, scopes, resources, equations, type information, and effect information;
- Declare-style process models and object-centric event logs distinguish constraints, events, objects, relations, ingestion, transformation, storage, and analysis;
- e-graph and monoidal-rewriting work shows that computation or process representation may be equivalence or composition structure rather than instruction order.

Use those lines as guardrails: recover the exact FPF-governed object, relation, claim, or representation use and its subject pattern instead of replacing one programming-paradigm label with another.

## C.2.P.DR:6 - Conformance checklist {#conformance-checklist}

| Check | Requirement |
| --- | --- |
| `CC-C2PDR-1` | @fact:CC-C2PDR-1 A repair separately names the visible expression or artifact, the exact current direct object or relation, and any current representation or correspondence use. Record `none` for the representation branch only when the receiving use needs an inspectable account. No field types structures, relations, formal objects, publication objects, or carrier-side objects as one family of representation kinds. @status:spec/done |
| `CC-C2PDR-2` | @fact:CC-C2PDR-2 When a representation use is current, the repair names its exact represented EntityOfConcern or claim and, for a mathematical-lens or selected-structure use, the preserved and lost structure and admitted and blocked uses required by its subject pattern; any current source or publication relation is named independently. When `RepresentationOrCorrespondenceUse` is `none`, no represented-target, preserved/lost-structure, or lens-use account is required. @status:spec/done |
| `CC-C2PDR-3` | @fact:CC-C2PDR-3 The tempting stronger action claim is explicit: route, call, dispatch, invoke, run, flow, send, receive, authorize, release, prove, prescribe, execute, select, pass a gate, or record work. @status:spec/done |
| `CC-C2PDR-4` | @fact:CC-C2PDR-4 The recovered subject pattern is named by value, or the case is demoted to quote-only, ordinary prose, reduced-use cue, blocked use, or incomplete rewrite. @status:spec/done |
| `CC-C2PDR-5` | @fact:CC-C2PDR-5 Legitimate `A.10 evidence path`, `E.18` graph path, `PathSlice`, carrier file path, URL, or mathematical path use is preserved when its exact evidence, provenance, graph, carrier/source, or mathematical object or relation is current. @status:spec/done |
| `CC-C2PDR-6` | @fact:CC-C2PDR-6 Method-like and algorithm-like wording identifies the visible expression, direct object or relation, current claim, and any exact representation use before selecting a subject pattern. If A.3.2 is selected, one already identified C.2.1 episteme has one admitted `U.Method` as its exact `EntityOfConcern` and at least one substantive way-of-doing claim; code, SOP, proof, solver, workflow, process, procedure, recipe, protocol, model, or diagram form alone does not pass. @status:spec/done |
| `CC-C2PDR-7` | @fact:CC-C2PDR-7 An `E.10.ARCH:3.1` project-concern recovery may connect method, mechanism, formal-substrate, work values, evidence relations, source relations, gate relations, or result relations, but each connected value keeps its own subject pattern and typed claim. @status:spec/done |
| `CC-C2PDR-8` | @fact:CC-C2PDR-8 The repair leaves one retained use and one blocked overread; type-correct but inert wording is incomplete. @status:spec/done |
| `CC-C2PDR-9` | @fact:CC-C2PDR-9 The pattern does not become a general representation theory, API pattern, schema pattern, legal framework, workflow framework, or generic admissibility pattern. @status:spec/done |
| `CC-C2PDR-10` | @fact:CC-C2PDR-10 Subject patterns keep their invariants. This pattern only restores representation use and blocked overread before those patterns carry their own claims. @status:spec/done |

## C.2.P.DR:8 - Relations {#relations}

- **Builds on:** `E.10`, `E.10.ARCH`, `C.2.P`, `A.7`, `E.17`, `E.8`, and `F.19`.
- **Coordinates with:** `E.18`, `E.18.1`, `A.10`, `A.19.SPR`, `A.3.1`, `A.3.2`, `A.6.0`, `C.29`, `A.6.1`, `E.20`, `A.15.2`, `A.15.1`, `A.15.4`, `A.20`, `A.21`, `B.3`, and direct publication, gate, authority, release, evidence, method, work, and assurance patterns when those claims are being made.
- **Specializes:** `C.2.P` for one recurring case: declarative representation and imperative-metaphor overread.
- **Used by:** `E.10.ARCH` applicability-row distribution and full-pattern text precision restoration when route, path, workflow, call, or dispatch wording hides representation use.

## C.2.P.DR:9 - Consequences {#consequences}

- FPF can keep useful graph, path, query, table, dashboard, publication, and pattern-relation vocabulary without banning ordinary words.
- The repair blocks hidden authority, release, gate, evidence, method, mechanism, work, and pattern-dispatch claims by requiring the subject pattern named by value.
- Method and mechanism claims become easier to compose because `E.10.ARCH:3.1` keeps separately recovered values connected only by the exact direct relations and participant meanings supplied by their subject patterns, without treating source labels as alternate ontology.
- The cost is this recovery, with a small note only when the receiving use needs an inspectable repair. Ordinary navigation, source quotation, and already-governed graph or evidence paths do not need the note.


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/C-2-P#root, spec://ai.lev/fpf-spec/contract/E-10#root, spec://ai.lev/fpf-spec/contract/E-10-ARCH#root, spec://ai.lev/fpf-spec/contract/F-19#root, spec://ai.lev/fpf-spec/contract/C-29#root, spec://ai.lev/fpf-spec/contract/C-2-1#root, spec://ai.lev/fpf-spec/contract/A-3-1#root, spec://ai.lev/fpf-spec/contract/A-3-2#root, spec://ai.lev/fpf-spec/contract/A-3-4#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/E-18#root, spec://ai.lev/fpf-spec/contract/E-18-1#root, spec://ai.lev/fpf-spec/contract/A-10#root, spec://ai.lev/fpf-spec/contract/E-17#root, spec://ai.lev/fpf-spec/contract/A-6-1#root, spec://ai.lev/fpf-spec/contract/E-20#root, spec://ai.lev/fpf-spec/contract/A-15-1#root, spec://ai.lev/fpf-spec/contract/A-15-2#root, spec://ai.lev/fpf-spec/contract/C-16#root, spec://ai.lev/fpf-spec/contract/A-19#root, spec://ai.lev/fpf-spec/contract/A-21#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-3-1#root, spec://ai.lev/fpf-spec/contract/A-3-4-P#root, spec://ai.lev/fpf-spec/contract/A-6-RSIR#root, spec://ai.lev/fpf-spec/contract/B-2-3#root, spec://ai.lev/fpf-spec/contract/C-37#root, spec://ai.lev/fpf-spec/contract/E-10-ARCH#root, spec://ai.lev/fpf-spec/contract/E-24-CD#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/C-2-P-DR
