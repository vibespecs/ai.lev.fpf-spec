# E.24.CD - Ontic Candidate Detection and First-Use Disposition: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## E.24.CD:5 - Archetypal Grounding {#archetypal-grounding}

### E.24.CD:5.1 - A candidate that genuinely opens E.24 {#a-candidate-that-genuinely-opens-e-24}

Before `C.2.1`, “description”, “view”, “claim set”, and “publication” repeatedly pointed to a claim-bearing object used across many patterns. The practical need was stable claim identity across description, evaluation, reference, and publication work. Existing patterns could not supply that shared identity and relation set independently.

That case opens E.24. E.24 then decides the durable ontic; C.2.1 governs the resulting `U.Episteme`; E.17.0, E.24.PUB, F.18, and C.29 keep viewpoint conformance, publication, naming, and representation separate. Cards and files do not become the episteme.

### E.24.CD:5.2 - Local cooling-pump classification {#local-cooling-pump-classification}

A maintenance team repeatedly asks whether Pump #14 counts as a cooling pump in plant slice S-14. Pump #14 and its flow, heat-transfer, and operating-state features already have direct governors. The needed outputs are a reusable local criterion and a candidate judgment, not a durable ontology unit.

Apply C.3.2. A `KindSignature` may declare the criterion for repeated use; the judgment can be `true`, `false`, or `unknown`; a current extension is materialized only for a named set-consuming use. A measurement supports a claim about Pump #14's features but does not create its membership.

### E.24.CD:5.3 - Problem card {#problem-card}

A `ProblemCard@Context` under `C.22.2` is a problem-side episteme. It may carry a signal, hypothesis, forecast, scenario, anticipated-condition claim, affected-entity reference, evidence cue, constraint, proposed direction, assignment cue, source reference, or gate cue without creating an actual Problem.

An actual Problem is one obtaining `ProblematicForRelation` under `C.22.PFR`. A card may assert that exact predicate, but it may designate a current Problem occurrence only after C.22.PFR independently establishes the actual-condition relation, criterion-applicability relation, adverse truth, and occurrence identity. Signals, hypotheses, forecasts, scenarios, anticipated conditions, and reviewable formulations remain under `C.22.2` or their exact forecast, scenario, temporal, or causal governor.

For a repair decision, keep the affected entity, evidence-use relation, any current local system-role kind and classification judgment, any exact obtaining system-role assignment, any separately governed responsibility relation, source-use relation, and gate or decision claim under their subject patterns. Apply `E.18.1`, `E.23`, and the exact Work, search, evaluation, or continuation pattern when repeated problematization or later action is current. Neither the card nor its acceptance or publication creates or ends an actual Problem. Open `E.24` only if a different reusable subject-identity or relation gap remains after these direct claims are recovered; do not rediscover the actual Problem as a new ontic.

### E.24.CD:5.4 - Record-shaped false candidate {#record-shaped-false-candidate}

A project schema contains:

```text
ChangeItem:
  status:
  owner:
  method:
  mechanism:
  evidence:
  result:
  target:
  source:
```

Treat the schema as source material, not as an ontology. A proposal episteme, method, mechanism declaration, work plan, intended-work claim, performed-work occurrence, holder system, state claim, evidence item, result, affected referent, and source remain different objects. Recover only those that the meeting actually uses:

| Field cue | Object and relation to recover |
| --- | --- |
| `owner` | Apply E.10's bounded `owner` recovery, then name the exact recovered relation and participants, ordinary or quoted non-use, or blocker. An established architectural owner—for example, the module designated for one functional-architecture object—keeps that direct architecture relation. Organizational, policy, source-maintenance or stewardship, legal ownership, responsibility, authority, and commitment uses keep their own recovered relations. Only a claim actually recovered as work-facing local classification or assignment proceeds through E.10.ROLE to A.2 or A.2.1. The field alone creates no System, kind, assignment, ownership occurrence, responsibility, or authority. |
| `status` | Name the exact bearer and the governed state or status value, claim, gate disposition, decision result, or other current relation. Field presence implies no readiness, validity, gate passage, work authorization, or release. |
| `method` and `mechanism` | Keep an admitted `U.Method` and any qualifying `U.MethodDescription` distinct from the A.6.1 `U.Mechanism` declaration episteme and its declared operation family. If the field concerns one use, identify the exact operation application and only its declaration-local argument or result bindings that obtain. If it concerns realization, identify the realizing entity and the obtaining mechanism-realization relation. Apply `A.6.1` when the row does not yet distinguish these readings. Shared wording identifies none of them. |
| plan, intended work, and actual work | Keep a `U.WorkPlan` or intended-work claim under `A.15.2`. Add a `U.Work` under `A.15.1` only for an independently grounded performed occurrence, whether ongoing with an open end or completed. A proposal, row, trace, or completion label does not make work occur. |
| `evidence` | First identify what the field points to; do not rename it to fit a pattern. Keep its direct kind: an episteme or evidence record, a carrier, the work that produced or interpreted evidence, a currentness relation, or a provenance relation. If it is an episteme and the meeting asks only about its bounded evidence-use or status-use for the claim, use `A.2.4` first. Use `A.10` when the evidence path must be retraceable; include only the record, carrier, work, currentness relation, and provenance relation needed for this claim. Use `B.3` only when a separate assurance claim is current. The field proves neither the claim nor the row's status. |
| `result` | Identify the result entity, value, or result episteme independently, then state the exact production, measurement, evaluation, decision, delivery, acceptance, or other result relation actually claimed. A result label creates no generic result object or relation. |
| `target` | Identify the affected referent and state an exact work-to-referent, change, effect, or other subject relation only when current. The field does not make the referent a work participant or changed entity. |
| `source` | Identify the source episteme or expression and the exact source-use relation. Source presence is not evidence, authority, or currentness by itself. |

Not every row has every listed object, not every filled field is claim-bearing, and co-presence in one row does not constitute a larger subject. The filled row is one C.2.1 episteme only when one exact ClaimGraph forms a claim-bearing whole about one truthful exact EntityOfConcern under one effective ReferenceScheme. Otherwise keep the epistemes separate and state only the exact collection, publication, representation, or meeting-use relation that actually obtains.

The column arrangement is a publication form only when selected to express an identified episteme for the meeting. The form is not a `U.ChangeItem`, and its columns are not ontic slots. If the project later needs a local kind of records for a query, `C.3.2` may classify those records as records. If several FPF patterns later demonstrate a different shared durable subject with its own identity and minimal relation set, that evidence can reopen `E.24`; the schema's shape cannot.

### E.24.CD:5.5 - Current configuration around a holon {#current-configuration-around-a-holon}

A maintenance review asks about “the current configuration around Pump #14.” Identify Pump #14 under its system governor, then recover only the characteristic or state claims, actual part relations, temporal phase, and other direct relations that the maintenance decision uses. If the work compares a possible configuration, identify the possible-state episteme and its direct state or configuration claims rather than asserting current actuality.

A separate C.2.1 description episteme may provide claim-bearing orientation. Its exact EntityOfConcern and any grounding holon in a separately current `EpistemeEmpiricalGroundingRelation` neither identify Pump #14 nor turn the surrounding claims into one world-side object. The holon and those current relations answer the question; their conjunction is not `U.Situation`.

### E.24.CD:5.6 - Operating pump with connected parts {#operating-pump-with-connected-parts}

Pump #14 is operating while a sensor, valve, and controller are connected. `Operating` first cues a governed state claim; it does not establish `U.Work` or `U.Transformation`. Connectedness does not establish parthood. Identify the pump and connected entities, state the exact connection relations, and use `A.14` only for part relations whose predicates actually obtain.

Add dated maintenance or control `U.Work` only after every precise performer has an A.13 core and A.15.1 independently identifies the Work's performance history, Method, time, containing System, and performers. Add F.6 only when the recovered situation account also needs precise assignment-bound attribution. A local system-role kind and its classification remain separate. A short situation-recovery sentence may omit identifiers its receiving use does not need. If maintenance or control is merely intended, keep it as an A.15.2 WorkPlan or other modal claim; it creates neither Work nor assignment. Add an actual bounded change under `A.3.4` only when its changed referent, boundary, conditions, and change facts obtain. No bundle of system, state, connection, work, and change becomes a situation entity.

### E.24.CD:5.7 - Multi-party emergency {#multi-party-emergency}

An emergency report mentions a leaking vessel, an overheated subsystem, a suppression system, and response teams. Recover each participating System and each actual change separately. For every dated response claimed as `U.Work`, recover each precise performer's A.13 core and independently admit the occurrence under A.15.1 as stated in `E.24.CD:5.6`; add F.6 only when the current account also needs exact assignment-bound attribution. Keep any local system-role classification separate. Keep an intended response as a plan or other modal content until it occurs. State temporal relations through their temporal patterns and a causal relation through `C.28` only when that claim is current and supported.

Use a C.2.1 emergency-description episteme only when the receiving work needs claim-bearing orientation across those objects. The emergency word, the record, and the co-presence of several systems and works identify neither `U.IncidentSituation` nor another bundled whole. Stop decomposition once the response decision has the exact subjects and relations it needs.

### E.24.CD:5.8 - Mathematical inconsistency under a declared formal substrate {#mathematical-inconsistency-under-a-declared-formal-substrate}

Two specification epistemes state constraints that cannot both hold under one declared `FormalSubstrate` and applicability. Identify the exact claims or epistemes, name that formal substrate, and state the exact inconsistency or consequence relation under its direct formal governor. Use `C.29` only when the formalism is also being used as a mathematical lens for another declared use.

The formal relation may guide a later decision or repair-work occurrence, but it establishes no project-world event, work, transformation, causal relation, adverse episode, actual Problem, or situation entity. Formal consequence is not causation. Inconsistent descriptions do not make their world-side subjects inconsistent without a separately governed bridge claim. If the exact relation or substrate cannot be named, leave the formal claim unresolved rather than letting the word `inconsistency` stand for it.

### E.24.CD:5.9 - Architecture diagram {#architecture-diagram}

An architecture diagram may carry claims about selected structures of one holon. If the diagram is selected as one claim-bearing whole, C.2.1 identifies that episteme. The same episteme has `U.View` membership only when E.17.0 conformance obtains; its publication form and carrier use E.24.PUB; selected graphical elements use C.29 only with explicit correspondence to independently recovered objects.

The diagram does not become the architecture, structure, or ontic by being visible. If the current work is simply to correct one architectural claim, apply the architecture and structure patterns directly.

### E.24.CD:5.10 - Broad source word {#broad-source-word}

A source says that a method “supports” production. If the author can recover a specific required-effect, method-use, work-enactment, capability, evidence-use, or other direct claim, apply its subject pattern. If the source word still compresses several claims, use E.10 and E.10.ARCH to retain it only with its bounded meaning or in quote-only or reduced use.

Do not open E.24 merely because `support` recurs, and do not invent `SupportRelation` as the candidate.

### E.24.CD:5.11 - Score table and characteristic space {#score-table-and-characteristic-space}

A score table can serve as the publication form of an evaluation-result episteme over a `U.CharacteristicSpace`, or it may be only a local report. Use A.19 when the characteristic space itself must be identified and A.19.ECS when the work is constructing the evaluation characteristics for a contested comparison. Use C.29 when readers calculate, compare, infer, navigate, or inspect through the table's mathematical structure and those available operations matter.

The table does not admit `U.CharacteristicSpace` by appearance and does not require another candidate ontology beside the current A.19 subject pattern.

## E.24.CD:6 - Bias-Annotation {#bias-annotation}

Lenses tested: **Onto**, **Arch**, **Epist**, **Prag**, **Did**.

This pattern intentionally biases toward early recovery of the real subject and the blocked work. It resists:

- **publication-form bias:** treating a card, schema, table, or record as the subject matter;
- **wording bias:** treating a repeated word as a kind or relation decision;
- **registry bias:** collecting possible ontics instead of disposing the current case;
- **scoring bias:** rating a candidate before its subject, identity rule, direct relations, and practical use are known;
- **semio-bias:** discussing forms and labels while the governed subject and claim disappear.

The mitigation is concrete: name the work, subject, needed claim, pattern that states it, applicable disposition, next action, and stop or return. Open E.24 only when several named patterns need the same subject identity or relation rules.

## E.24.CD:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Symptom | Repair |
| --- | --- | --- |
| Card-to-kind jump | A useful card is promoted into a `U.*` kind because it has repeated fields. | Recover its claims, subject, form, and carrier; use C.2.1 or E.24.PUB as triggered. |
| Structural U-kind jump | A heading, title, filename, or ToC row keeps `U.*` because the spelling is convenient. | Recover the subject and use E.24.UK for the admission question; naming follows the result. |
| Column-to-participant jump | A field label is treated as a relation-participant meaning, or a filled field as an actual participant; either is called a `SlotSpec` because of column position. | Recover the direct predicate, its relation-participant meanings, and its actual participants first. Keep the field as a representation element or participant designation; under `A.6.5`, declare a `SlotSpec` only inside a needed `RelationSignature` for that already recovered relation. |
| One-word candidate | A broad word is renamed and treated as settled. | Recover the subject and predicate; use F.19 when only wording remains and E.10 for unresolved meanings. |
| Local-kind inflation | A useful project criterion is promoted to durable public ontology. | Use C.3.2 and keep the local kind, declaration, judgment, and extension distinct. |
| Registry trap | The author keeps a list of possible ontics without deciding the blocked case. | State the work, apply one truthful subject pattern or name one precise unresolved stop, and stop. |
| Scoring before identity | A score form is filled before the subject and direct relation gap are known. | Recover the subject, identity rule, dependent uses, and missing coordination; use A.19.ECS only for an actual comparison. |
| Repetition-as-admission | Several forms or patterns share a label, so an ontic is inferred. | Require the E.24 entry facts: one subject identity and minimal relation set reused by named dependent patterns. |
| Negative-catalogue repair | The text lists only what the candidate is not. | State the positive subject, claim, direct pattern, and next action. |

## E.24.CD:10 - Rationale {#rationale}

Ontic candidates rarely arrive as pure ontology. They appear through the forms people use: project tables, cards, schemas, diagrams, source packets, draft rows, examples, and repeated words. Those forms reveal working concerns, but they do not decide what exists, what relation obtains, or what FPF kind is needed.

The pattern therefore asks for one first-use disposition instead of a candidate record. Keep direct claims in their direct patterns; use C.2.1 only when one exact ClaimGraph, one truthful EntityOfConcern, and one effective ReferenceScheme constitute an episteme; and use C.3.2 for local classification. Keep publication in E.24.PUB and representation in C.29. Use C.2.P.DR to block action inferred from declarative form; resolve ambiguous wording through A.6.RSIR, A.6.F, A.6.P, or E.10; and name only an already governed value through F.18. Open E.24 only when named dependent patterns need one stable subject identity and minimal relation set that those simpler applications cannot preserve.

This order keeps the first move affordable and falsifiable. Another author can see which fact selected the applicable pattern or unresolved stop and what to do next. A list of candidate fields or scores would make the form look authoritative and invite optimization of the record instead of settlement of the subject.

## E.24.CD:11 - SoTA-Echoing {#sota-echoing}

| Source family | Current lesson for E.24.CD | FPF decision |
| --- | --- | --- |
| Shimizu and Hitzler 2024, and Eells, Dave, Hitzler, and Shimizu 2024. | Current modular-ontology and micropattern work favors ontology units that are understandable, extensible, aligned, reusable, and small enough to assemble. | Inspect repeated subject identity and direct-relation rules across named dependent uses; do not treat word frequency, common nouns, or record fields as admission evidence. |
| Norouzi, Hertling, Waitelonis, and Sack 2025. | Current process-ontology ODP extraction work shows that process-like and workflow-like forms can expose implicit design patterns that domain experts need to examine. | Recover the objects and predicates hidden by process, record, card, and field-list forms and check them against their subject patterns; do not reopen transformation-flow decisions or import imperative motion metaphors. |
| Nayyeri et al. 2025, and Oyewale and Soru 2026. | Current data-model-to-ontology and enterprise-KG work shows that schemas, documentation, relations, provenance, and validation can reveal ontology candidates while also encouraging schema-shaped overreads. | Treat project databases, tables, schemas, and enterprise data models as source material and detection cues for selecting the applicable subject pattern, not as ontology decisions; require bounded scope, agreement with each current subject pattern, and expert validation. |
| CYC microtheory line. | Lineage-only caution: context-bounded knowledge modules are a useful analogy for contradiction locality and scope-bounded ontology fragments. | Do not cite CYC as current decisive support for FPF ontic design and do not import CYC architecture as FPF law. |
| OWL, SKOS, RDF, and triple-store practice. | Infrastructure and expression lineage: these lines carry ontology descriptions, vocabulary links, queries, and serialization forms. | Use them as expression and publication caution only; they do not substitute for `U.Ontic`, do not show that labels are ontology, and do not answer FPF ontic modularization by themselves. |

Smallest source-currentness reopen trigger: reopen this SoTA slice when a newer ontology-engineering or data-model-to-ontology source changes the selected criteria for reusable subject identity, minimal relation sets, bounded scope, validation, or source-form overread; do not reopen it merely because a new vocabulary, serialization, or KG tool appears.


## E.24.CD:End {#end}
