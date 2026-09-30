# E.4.PFR - Pattern-Framework Relation and Edition Discipline: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## E.4.PFR:4 - Archetypal Grounding {#archetypal-grounding}

### E.4.PFR:4.1 - Ordinary subject assertion without PFR {#ordinary-subject-assertion-without-pfr}

In one CGUS position, `selectedConstituentRef` designates `result-42`. The exact C.11 `ChoiceResult` definition classifies that record from its stated disposition, selected option, comparison basis, rule, and stop-probing reason; A.22.CGUS constrains the position locator and selected-constituent reference. That sentence is the first useful output. It adds no owner field, PFR row, actual-use predicate, or basis analysis.

If a later Core relation-function maintenance replay must enumerate every CGUS position whose constituent-kind assertion cites a defining ClaimGraph, add one compact row for this position with the governed use, subject assertion ref, and exact C.11 definition ClaimGraph ref. That named receiver—not the importance of the relation—opens PFR.

### E.4.PFR:4.2 - Framework edition dependency {#framework-edition-dependency}

Start with the readable dependency assertion:

> `CodexProcessFramework@current` uses the selected `FPFCorePatternSet@current` authoring and quality rules as required constraints on local process authoring. Without those rules, or after a relevant change to them, the affected local guidance cannot remain current without recheck. `CodexProcessFramework@current` therefore depends on that exact Core content for local process authoring.

Choose the representation from the receiver's job. A cross-relation comparison may use one generic PFR row. An edition-impact or refresh receiver may use one dependency-specific record. This receiver needs the relied-on content and refresh fields, so it uses only the dependency record:

```text
FrameworkEditionDependencyRecord@CodexProcessFramework:
  subjectAssertionRef: CodexProcessFramework-CoreDependencyAssertion
  dependencyPredicateClaimRef: E.4.PFR:3.4-framework-edition-dependency-predicate
  directionConstraintClaimRef: E.5.3-local-to-Core-direction-and-Core-acyclicity
  dependentEditionRef: CodexProcessFramework@current
  reliedOnEditionRef: FPFCorePatternSet@current
  reliedOnContentRefs: [selected_Core_authoring_and_quality_rules]
  namedUse: local_process_authoring
  dependencyDirection: local_to_Core
  dependencyReason: the selected Core rules are required constraints on the affected local guidance; removing or relevantly changing them invalidates or reopens that guidance
  refreshConditionRefs: [G.11-Core_pin_or_selected_rule_change]
```

If one named cross-relation receiver also needs the generic view, add one `PatternFrameworkRelationRecord`, give both forms the same `subjectAssertionRef`, and set the dependency record's `genericRelationRecordRef` to that row. In the generic row, `relationFunctionClaimRef` points to the E.4.PFR:3.4 dependency predicate, `dependencyOrEditionEffect` states the E.5.3-constrained direction, and `refreshOrSupersessionCondition` cites the G.11 refresh condition. Derive their shared endpoints, use, direction/effect, and refresh condition from the subject assertion. A change to that assertion refreshes both views together; neither carries an independently maintained copy of the dependency fact.

If this same pair also has a supported compatibility result for an overlapping use, state that C.2.1 assertion separately. Add its ref to `compatibilityClaimRefs` only when the named edition-impact receiver must traverse from this dependency record to that claim. The dependency record proves neither dependency nor compatibility, and E.5.3 does not own either edition.

### E.4.PFR:4.3 - Source and decision reuse {#source-and-decision-reuse}

```text
PatternFrameworkRelationRecord@HydroponicCucumberDomain:
  relationId: PFR-HC-SRC-001
  sourceRef: G2-HC-nutrient-source-pack
  targetRef: HC.NutrientMonitoringPattern@draft
  relationFunction: Source or decision reuse
  governedUse: the solution uses selected source-pack claims by value for nutrient-monitoring guidance
  subjectAssertionRef: HC-NutrientSourceUseAssertion
  relationFunctionClaimRef: exact G.2 bounded source-use ClaimGraph
  preservationOrAdmissionRef: C.33-source-pack-summary-loss-note
  blockedStrongerReading: not framework dependency, specialization, publication, derivation, evidence, or assurance
  sourceReturnCondition: reconsider when including an omitted rival horticulture tradition could change the selected source answer or bounded nutrient-monitoring use
```

A hydroponic framework may separately carry a Core-edition dependency, publication relation to its all-in-one carrier, access relation to a grower-assistant skill pack, specialization relation for a narrowed authoring pattern, and quality relations for evaluated drafts. Each remains a different assertion and optional row.

### E.4.PFR:4.4 - Genuine overlap conflict {#genuine-overlap-conflict}

A named automated replay receiver whose contract requires acceptance and witness has two exact, accepted, witnessed, independently sufficient bases for the same subject, use, scope, and time cell, and their consequences conflict. Lane 1 can state the conflict but cannot give that receiver a stable closed family-plus-pairwise result. The basis analysis retains both alternatives, records the exact pairwise conflict, returns `established-conflict`, and leaves unrelated work available. It selects no winner, grants no permission, and changes no actual-use fact.

### E.4.PFR:4.5 - Establishment, minimality and a total answer {#establishment-minimality-and-a-total-answer}

For a receiving derivation of p under ordinary premise introduction, both {p} and {p,q} are sufficient without any undeclared premise. Both can be established when their required axes are true; only {p} is inclusion-minimal among their sub-bases. If the receiver requires a minimal family and that additional search is incomplete, the minimal-family answer stays qualified while establishment of these two bases survives.

| Bounded cell case | Exactly one disposition and retained distinction |
| --- | --- |
| Closed universe {{p},{p,q}}, required axes true, both yield p and their required pair is compatible | `established-compatible`; optional minimality can remain unknown without changing that result. |
| Closed universe with one otherwise sufficient candidate and an unknown witness required by this receiver | `open-no-established`; the missing witness leaves the conjunction unresolved. |
| Closed universe with one candidate whose exactness is false and required witness unknown | `closed-insufficient`; false exactness decisively defeats it. |
| One established candidate in an open universe | `established-with-open-candidates`; retain the candidate while admitting further alternatives may matter. |
| Two independently sufficient, established bases with known incompatible consequences for the same overlapping use | `established-conflict`, even if another candidate is unresolved; neither established basis is deleted. |
| Closed empty universe and an exact supported absent-needed-content claim | `missing-candidates`. |
| Closed empty universe with no supported claim that content is needed | `closed-empty-unresolved-need`. |

In evaluate mode, criterion “value ≥ 80” and an applicable exact value 70 suffice to obtain `fail` under that evaluation rule. With the other required axes true, the candidate is established even though the evaluated object fails. The criterion/value set's sufficiency says nothing about whether a particular evaluation actually selected and used it; Lane 3's actual-use predicates still need their own facts.

## E.4.PFR:5 - Bias-Annotation {#bias-annotation}

**Scope.** The assertion-first discipline is **Universal within this pattern's subject**: every claimed relation starts as a readable assertion with its subject, relation function, basis, polarity, and current facts. The reusable row, dependency record, package manifest, and high-cost basis analysis are **limited** tools for a named framework-maintenance use whose next action needs them; none is a prerequisite for ordinary relation prose.

| Lens | Boundary |
| --- | --- |
| **Gov** | A row or analysis grants no authority, acceptance, permission, or reliance. |
| **Arch** | Assertions, relations, records, editions, publications, carriers, and access routes stay distinct. |
| **Epist** (Epistemological and Ontological) | A representation cites an assertion but neither creates the relation nor proves more than its bounded basis. |
| **Prag** | Stop after the direct assertion unless a named next action needs more structure; keep high-cost analysis exceptional. |
| **Did** | Lead with the readable assertion and introduce optional machinery only through a concrete receiving use. |

The first drift is relation-word overread: words such as *depends*, *uses*, *supports*, *governs*, or *profiles* are treated as if they settled relation function. Recover the exact subject assertion and blocked stronger readings.

The second drift is record prestige: a standardized row is required before the assertion can count. Keep the direct assertion as default and demand a named receiver for every row.

The third drift is software-package analogy: compatibility, endpoints, and access carriers are useful, but framework relations are not build imports, module calls, APIs, runtime routes, permissions, or performed Work.

The fourth drift is basis inflation: definition, citation, evidence, or later sufficiency is mistaken for actual formal-premise use or criterion selection, and every actual-use claim receives a complete analysis. Keep actual use exact and open analysis only for its high-cost receiver.

## E.4.PFR:7 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | What fails | Repair |
| --- | --- | --- |
| Related-pattern flattening | A relation list hides subject, function, predicate, and blocked reading. | Recover the exact subject assertion first; add a relation-specific row only for a named PFR receiver. |
| Mandatory row for every relation | Representation burden becomes an ontology and ordinary authoring becomes record-first. | Keep lane 1; open lane 2 only above its receiver threshold. |
| Pattern owner or governor | A pattern locator becomes a semantic owner, authority, or relation participant. | Cite the exact defining or constraining ClaimGraph and state the subject assertion. |
| Dependency as specialization | Edition reliance is read as child-pattern inheritance. | Use the exact dependency assertion; add a dependency-specific record only when a named dependency-impact or refresh receiver needs it, and state specialization separately if it also obtains. |
| Compatibility folded into dependency | A dependency sentence or record carries `compatibilityBoundary` and makes one relation stand for two claims. | State dependency and pairwise compatibility separately; add only an optional ref from the dependency record when a named maintenance consumer needs the link. |
| Compatibility by version label | An edition number is assumed to settle compatibility. | Inspect the exact pair, overlapping use, difference or interface, impact, and reopen condition; otherwise make no positive compatibility claim. |
| Generated graph as authority | A search or graph artifact decides relation meaning. | Apply C.35 when the exact generated or discovered result is to inform architecture work, and test the exact subject predicate independently. |
| Callable route as dependency | A skill, endpoint, or assistant integration is treated as framework dependency, method order, permission, or Work. | State only the exact bounded access relation; keep runtime/tool/work/currentness claims separate. |
| Source prose as basis truth | "supports" is read as formal-premise use, evidence, or sufficiency. | Separate bounded G.2 source use, actual-use predicate, evidence, and candidate evaluation. |
| Silent conflict winner | One sufficient base overwrites another in the same cell. | Preserve both and record pairwise conflict; return `established-conflict` and open bounded E.9. |
| Analysis as permission | A compatible or established family is treated as authorization or reliance. | Use the separate A.10/B.3 and authority/permission claims required by the attempted use. |

## E.4.PFR:9 - Rationale {#rationale}

FPF pattern ecosystems are declarative relation systems. Their descriptions state predicates, constraints, dependencies, publication and access arrangements, quality relations, and source uses; the patterns themselves do not act on one another. A sequence of pattern descriptions may describe a method or constrain a separately admitted transformation-flow structure, but displayed order alone performs no Work and admits no Transformation or flow.

The assertion-first rule follows C.2.1 identity and A.22.CGUS declarativity. It avoids building a second ontology of pattern ownership while retaining exact relations already supplied by the Core. PFR is a projection for named maintenance use, not the semantic source.

The three-lane split also controls cost. Lane 1 dominates whenever it closes the task. Lane 2 adds standardized form only for a consumer. Lane 3 separates actual-use truth from optional basis analysis and keeps its output non-permissive.

## E.4.PFR:10 - SoTA-Echoing {#sota-echoing}

| Source and status | Useful pressure | FPF mutation and boundary |
| --- | --- | --- |
| Official Dyad changelog, Components, and Analyses documentation, moving `/stable/` pages observed with release 3.2.0 dated 2026-07-08 | Current implementation comparator: reusable component declarations and connections remain distinct from analyses, solution objects, and generated artifacts. | Use the separation to stress declaration, actual use, analysis, and carrier boundaries. The moving pages are neither edition-pinned source nor FPF ontology; no Dyad object or dependency enters FPF. |
| Modelica Language Specification 3.6 | Historical acausal-modeling lineage illustrates declarative equations and connections distinct from solver execution. | Retain as lineage only, not the current comparator or SoTA claim. Import neither class-model, equation, solver, simulation, nor package ontology. |
| SysML v2, deliberately excluded | For this comparison it is neither a current practice comparator nor useful lineage; treat it as an intentionally excluded historical dead end, not as SoTA by search prominence or by the word “systems”. | Import no UML/SysML metamodel, diagram, package, or workflow semantics. Reopen only if concrete working-project evidence shows a non-dominated gain for this exact relation-maintenance question. |
| Semantic Versioning 2.0.0 and Chen et al., *Breaking Changes in Software Ecosystems: A Systematic Literature Review* (2026) | Compatibility requires explicit boundaries and impact inspection rather than labels alone. | Adapt compatibility, deprecation, supersession, and impact discipline to framework editions; reject binary/build dependency semantics. |
| Nazar, *Software Product Line Engineering: Adoption, Tooling and AI Era Challenges* (2026) | Related product families need core assets, variability, and evolution discipline. | Adapt stable-Core and variation reasoning to FPF/domain/local framework editions without making them software product lines. |
| Riehle, Harutyunyan, and Barcomb, *Pattern Discovery and Validation Using Scientific Research Methods* (2021) | Mined or proposed patterns require validation before reuse. | Generated or discovered results proposed for architecture use remain candidates under C.35; exact subject assertions and source-use decisions remain separate. |
| ISO/IEC/IEEE 42010:2022 | Narrow architecture-description comparator distinguishes architecture, description, viewpoints, and views. | Use only for the C.30.AD architecture-description boundary. General entity/description and structure/description separation already comes from C.2.1, E.10.D2, A.22, and A.22.CGUS; ISO 42010 does not found a parallel description ontology. |


## E.4.PFR:End {#end}
