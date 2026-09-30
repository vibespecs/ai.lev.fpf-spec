# E.18.NET - Network of Transformation-Flow Structures: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## E.18.NET:5 - Archetypal Grounding — worked cases {#archetypal-grounding-worked-cases}

### E.18.NET:5.1 - Same surface vocabulary, different ontic answers {#same-surface-vocabulary-different-ontic-answers}

**Several valuations of one TFS.** A cooling-loop review compares nominal-load and emergency-load valuations of the same exact cooling-loop `TransformationFlowStructure`. Both valuations use the same structure positions and internal `U.Transfer` occurrences. The load value, path slice, and local tags differ; the TFS identity does not. E.18.NET is not used.

**Internal coffee subflow.** A coffee-brewing TFS exposes a preparation portion containing grinding, dosing, and wetting positions plus their parent-internal `U.Transfer` occurrences. Its entry and exit remain positions of the brewing TFS. The practitioner uses E.18's `SubflowRef`; no second TFS or network is created.

**Independent network.** A roastery-production TFS and a café-brewing TFS concern different objects and have separate Work occurrences, valuation boundaries, and architecture change cadence. The applicable supply pattern defines its predicate and applicability, and the current delivery-and-acceptance facts satisfy that predicate for a dispatch position in the first and an accepted-stock position in the second. For ordinary first use, fill the selected network directly:

```text
selectedNetworkRef: RoasteryCafeSupplyNetwork@CoffeeService
directMemberRefs[]:
  - RoasteryProductionTFS@Dispatch
  - CafeBrewingTFS@AcceptedStock
selectedCrossFlowRelationOccurrenceRefs[]:
  - SupplyOccurrence@Lot24Dispatch-to-CafeAcceptance
selectedNetworkConstraintRefs[]:
  - SupplyEndpointConstraint@Dispatch-to-AcceptedStock
  - SelectedExposureConstraint@RoasteryDispatch-and-CafeAcceptedStock
  - AcyclicDirectMemberConstraint@RoasteryCafe
networkUseFrame:
  questionOrAction: decide which accepted stock can enter the coffee-service brewing flow
  admissibleUse: use the selected supply relation to choose accepted coffee stock for the brewing flow
  stopOrReturnCondition: return to the supply claim when its delivery-and-acceptance basis no longer supports this stock choice
returnCondition: either member, the supply occurrence, an endpoint or exposure, acyclicity, or the coffee-service question changes
```

This filled basis is enough for the immediate selection; it is not a `TransformationFlowStructureNetworkRecord@Context`. Create that separate descriptive record only when the result must survive the current work. If the supply claim has no admitted relation kind or applicable predicate, carry the governing pattern's `missing-governor` result. If required facts are unavailable, carry `missing-information`; if a sufficient case basis fails the positive test, carry `factually unsupported`. Neither result asserts a negative. Only an applicable negative rule and satisfying case basis can supply a negative result. When the supply occurrence obtains but an endpoint binding is missing, keep the positive occurrence and name the missing binding as a separate E.18.NET selection blocker. A missing member, applied constraint, or coffee-service use frame is also a separate selection blocker.

### E.18.NET:5.2 - Project system-of-interest and recursive build-the-builder {#project-system-of-interest-and-recursive-build-the-builder}

For one project question, practitioners ask which independently identified flow structures must be considered together to connect production and later operation of the project system-of-interest, and which builder branches must also be visible. The actual project remains composite `U.Work`; the selected network is a non-agentive `U.Structure`. Project designation and `U.System` identity remain separate from any local system-role kind, classification, assignment, selection Work, or result episteme. None follows from a project or network label.

For the compiler-and-application use, identify five TFS values by the questions they answer:

1. `CompilerEditionPreparationTFS`, whose loci bind compiler-edition preparation and the obtaining source-use occurrences needed by the build;
2. `BootstrapCompilerBuildTFS`, whose loci bind Work on pre-existing build substrates and the separately grounded production and identity-inception claims for one bootstrap compiler;
3. `ApplicationBuildTFS`, whose loci bind application-production Work and the exact use of that admitted compiler;
4. `ReleaseAssuranceTFS`, selected for release-assurance questions; and
5. `DeploymentOperationTFS`, selected for deployment and operation after the application system exists.

These names designate independently identified TFS values, not lifecycle kinds. They assert no transformation of a not-yet-existing compiler or application. Use E.18 for each TFS, A.15.1 for any current Work occurrence, A.3.4 for a change of a continuing referent, A.15.PROD for production or identity inception, and the applicable relation pattern for each exact cross-member occurrence.

Select the nested network values from those already established inputs:

| Selected network | Direct members | Exact selected cross-member occurrence and ordered endpoint binding | Network use frame |
|---|---|---|---|
| `CompilerRealizationNetwork` | `CompilerEditionPreparationTFS`; `BootstrapCompilerBuildTFS` | `CompilerEditionSourceUsedByBootstrapBuild-1`: `CompilerSourceEditionReady` -> `BootstrapCompilerBuildInput` | connect the admitted source edition to the bootstrap-compiler build question |
| `ApplicationCompilerUseNetwork` | `CompilerRealizationNetwork`; `ApplicationBuildTFS` | `BootstrapCompilerUsedByApplicationBuild-1`: exposed `ExecutableCompilerResult` -> `ApplicationCompilerUsePosition` | connect the admitted compiler to the application-build question |
| `ReleaseAssuranceNetwork` | `ApplicationCompilerUseNetwork`; `ReleaseAssuranceTFS` | `ApplicationBuildEvaluatedForRelease-1`: exposed `ApplicationBuildResult` -> `ReleaseEvaluationSubject` | connect the application result to the release-assurance question |
| `DeliveryOperationNetwork` | `ReleaseAssuranceNetwork`; `DeploymentOperationTFS` | `ReleasedApplicationUsedByDeployment-1`: exposed `ReleasedApplicationPosition` -> `DeploymentApplicationInput` | connect the released application to the deployment-and-operation question |

Each named occurrence is independently established under its project predicate before selection. Each network applies its exact endpoint-binding and boundary-exposure constraints plus the acyclic direct-member constraint, and each keeps the use frame in its row. The local names select or add nothing by themselves.

No claim about who selected these networks is required. If the case also needs `CompilerNetworkSelectionWork-5`, cite each precise performer's independently established A.13 core and the Work's independent A.15.1 admission. Add F.6 only if the case also needs exact assignment-bound attribution; its assignment declaration and proof remain outside E.18.NET. Adding or removing the Work or attribution claim changes none of the four network identities above. The result episteme may describe the selected structures and cite a separate selection or decision relation, but it is not a decision or accountability relation by form. Any accountability claim needs its own exact predicate and participants.

A compiler-production case can close on separately grounded identity inception, production completion or readiness, evidence, and decision while naming the application-build position as the downstream use outside that closed case. Project-level reasoning continues into the member where the compiler later participates. The same joint-selection question recurs for a builder system: select the TFS in which that admitted builder performs exact Work together with the independently identified TFS or nested network concerning production and identity inception of the builder, or its later change after it exists. Shared identity creates no edge; use obtaining production, inception, participation, application, use, or other relation occurrences and their endpoint bindings.

The bootstrap compiler result is exposed from the outer network through one finite member path:

```text
ExposedFlowPositionRef:
  networkStructureRef: DeliveryOperationNetwork
  memberPath[]:
    - ReleaseAssuranceNetwork
    - ApplicationCompilerUseNetwork
    - CompilerRealizationNetwork
    - BootstrapCompilerBuildTFS
  leafFlowPositionRef:
    transformationFlowStructureRef: BootstrapCompilerBuildTFS
    localFlowPositionId: ExecutableCompilerResult
```

Each path entry is a direct member of the preceding network, the final entry is the TFS named by `leafFlowPositionRef`, and no network repeats. `FlowValuation`, path slices, and `DesignRunTag` remain leaf-local. “Builds”, “uses”, “evaluates”, and “delivers” are ordinary cues until each link resolves to an admitted relation kind, complete participant signature, obtaining occurrence, and endpoint bindings.

Before these identities and relations are grounded, A.1.STM may show the dependency only as a Plain provisional long-mantra map and must name the missing member, the exact relation-claim result returned by its governing pattern, or the separate missing occurrence, endpoint, or position binding. It is not yet an E.18.NET selection. Once the network is admitted, a separate A.22.CGUS demonstrative slice may traverse admitted positions and relation-reference epistemes; it remains a demonstration, not the project, network, case, or Work order.

### E.18.NET:5.3 - N-ary relation and feedback cycle {#n-ary-relation-and-feedback-cycle}

A manufacturing release relation has three participants defined by one admitted domain relation pattern: one product-definition position in a TFS selected to answer the development question, one equipment-readiness position in a TFS selected to follow the changes that establish equipment readiness, and one release-condition position in a TFS selected for assurance. Its network row keeps the three participants and their order. It is not replaced by three unlabeled arrows.

Later, an exact use-observation relation connects a position in a TFS selected for operation or use back to a position in a TFS selected to answer the development question. The relation occurrences form a feedback cycle, while the selected direct-member nesting remains acyclic. The feedback does not make the operation-or-use TFS a member of itself and does not turn observation into development Work.

### E.18.NET:5.4 - Architecture and two demonstrative boundaries {#architecture-and-two-demonstrative-boundaries}

For one containing holon, a current `ArchitectureOf@Context` claim may select the network among its structures. If the selected members belong to separately named holons and no containing bearer is grounded, record the use as inter-holon and name the participating architecture claims. Do not invent one system merely to fill the architecture field.

A Plain A.1.STM long-mantra map may display proposed members and a missing cross-member link before network admission. It names the intended final result and the absent member, relation kind or predicate, predicate result, occurrence, or endpoint binding; it asserts neither an E.18.NET structure nor a CGUS.

After the network is admitted, a separate teaching mantra may show one finite admitted dependency slice. The slice uses the network locator family, cites admitted positions and exact relation-reference epistemes, and keeps omissions and return visible. It does not prescribe project Work order, make the path the whole network, or turn a leaf-local `DesignRunTag` into a project phase.

## E.18.NET:6 - Bias-Annotation {#bias-annotation}

Bias risks considered: **Gov**, **Arch**, **Onto/Epist**, **Prag**, **Did**. Scope: **Universal** for uses of this pattern.

| Bias risk | Mitigation in this pattern |
| --- | --- |
| **Gov:** demanding a fully reusable relation occurrence can hide the cheaper local decision. | The first result permits a proposed description and one exact result from the pattern governing the relation claim, or one separate missing-discriminator blocker; it invents no common status kind or generic relation. |
| **Arch:** a network-shaped case can tempt the reader to invent one containing holon. | C.30.TFS-REL keeps named-containing-holon and explicit inter-holon uses separate. |
| **Onto/Epist:** a graph, record, or demonstrative slice can be mistaken for the selected network. | The four A.22 identity discriminators precede every description, record, rendering, architecture reading, and demonstration. |
| **Prag:** exact member, relation, endpoint, and constraint apparatus can crowd out first use. | The practitioner first produces one small network result or one exact stop; the durable record remains optional. |
| **Did:** the coffee and build-the-builder cases can be over-read as a closed domain ontology or a universal edge vocabulary. | The cases demonstrate boundary choices only; each cross-flow relation still needs an admitted kind, its applicable predicate, and exact participants. |

## E.18.NET:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Symptom | Repair |
| --- | --- | --- |
| One giant flow | Development, use, evaluation, and refresh are called valuations solely because they are coupled. | Test shared TFS identity; when independent members and a direct relation are needed, select a network. |
| Detail becomes a member | A zoomed diagram, team boundary, or named stage becomes another TFS. | Use E.18 `SubflowRef` while every position and internal transfer still resolves in one parent. |
| Universal cross-flow edge | `creates`, `produces`, `uses`, `input`, `result`, `handoff`, or `transfer` labels stand in for several relations. | Apply the pattern that defines or tests the exact relation and carry its result. Only after a positive occurrence, test endpoint bindings and other network discriminators separately. |
| Record makes the world | Filling `directMemberRows[]` or drawing edges is treated as establishing members and relations. | Ground members and relation occurrences first; keep the record descriptive. |
| Recursive flattening | A parent copies all nested positions and state into one global graph. | Keep finite member paths and expose only the boundary positions needed by the parent use. |
| Global design/run ladder | One `DesignRunTag` is assigned to the network. | Restore one tag per exact leaf position binding. |
| Network as actor or workflow | The network builds, evaluates, repairs, schedules, or authorizes. | Name the acting system and its Work, or the exact decision, gate, or assurance claim and result; keep the network non-agentive. |
| Pretty graph as network | A connected diagram is accepted without exact members, relations, constraints, and use frame. | Keep it as an E.18.2 or provisional description until all four A.22 discriminators are recoverable. |

## E.18.NET:10 - Rationale and naming {#rationale-and-naming}

The selected head preserves the established `TransformationFlowStructure` name, says that the members are structures rather than valuations, and supports recursion without fixed levels. The shorter cue “transformation-flow network” is retrieval wording only after the governed value is clear.

Mint vs reuse: E.18.NET mints the durable names `TransformationFlowStructureNetwork`, `TransformationFlowStructureNetworkRecord@Context`, `ExposedFlowPositionRef`, and `NetworkCrossFlowRelationRowRef` for the governed value family, separate description episteme, and two reference shapes defined here. It reuses `U.Structure`, `U.Episteme`, `TransformationFlowStructure`, `FlowPositionRef`, relation kinds, and relation occurrences without changing their meanings; labels, records, and references create none of those values.

```text
NameCard:
  NameCardId: NC-TRANSFORMATION-FLOW-STRUCTURE-NETWORK
  GovernedValueRef: TransformationFlowStructureNetwork@Context <: U.Structure
  SubjectPatternLocator: E.18.NET
  ReferenceScheme: FPFCoreReferenceScheme
  LocalSenseRef: recursive selected organization over independently identified TransformationFlowStructure or TransformationFlowStructureNetwork values and exact cross-flow relation occurrences, with member boundaries and locally exposed positions preserved
  TechLabel: TransformationFlowStructureNetwork
  PlainLabel: network of transformation-flow structures
  CandidateSet: TransformationFlowStructureNetwork; TransformationFlowNetwork; CrossFlowRelationStructure; TransformationFlowDependencyStructure; CoupledTransformationFlowStructure; FlowOfFlows; CreatorGraph; CreationStructure
  RejectedCandidates: TransformationFlowNetwork can mean one network-shaped TFS; CrossFlowRelationStructure hides the transformation-flow use; TransformationFlowDependencyStructure narrows to one projection; CoupledTransformationFlowStructure suggests one merged TFS; FlowOfFlows conflicts with FlowValuation; CreatorGraph confuses the ontic structure with a graph and narrows change to creation; CreationStructure excludes operation, repair, modification, and reuse
  SelectionRationale: preserve the established TransformationFlowStructure head, make structures rather than valuations the members, and permit recursive membership without numbered levels
  LineageEntries: flow-of-flows and creator-graph examples remain retrieval lineage for the stress cases; fixed two-level and one-giant-flow ontic readings are retired
  RefreshCondition: reopen if repeated use cannot distinguish one TFS with several valuations, one subflow, and a recursive network of independently identified TFS values
```

## E.18.NET:11 - SoTA-Echoing {#sota-echoing}

Each line below is inherited only while the cited current pattern version retains both the named body decision and the named source-use row for its declared use. E.18.NET relies on the currentness decision recorded with that source-use row; it does not independently turn the cited literature or tool practice into current authority. When one cited source-use row changes, reopen only the affected line here.

For the working reader, these lines support the boundary already exercised in the worked cases in sections 5.1–5.4: select a network only from independently identified members and exact relations, keep positions and state local to their leaf TFS, treat graphs as descriptions, and let a demonstrative path cite only already admitted positions and relation references.

| Current pattern version and exact source-use locus | E.18.NET disposition | Concrete mutation in E.18.NET | Qualification and smallest reopen |
| --- | --- | --- | --- |
| `A.22:4.1` and the `A.22:11` row beginning “FPF `C.2.1` and `E.10.D2` description discipline” | **Adopt** the four selected-structure discriminators and the separation of structure from its description, view, record, selecting system, and selection Work. | Network identity is the exact `directMemberRefs[]`, selected obtaining `selectedCrossFlowRelationOccurrenceRefs[]`, exact `selectedNetworkConstraintRefs[]`, and one `networkUseFrame`; the descriptive record and selection activity remain separate from the non-agentive network. | Applies while A.22 keeps those four discriminator meanings and that description/view boundary. Reopen this line if A.22 changes a discriminator or allows a description, view, record, or selection activity to identify or authorize the structure. |
| `E.18:5.1` through `E.18:5.3` and the `E.18:12` rows `Applied category theory and compositional open systems`, `Operads, wiring diagrams, and hypergraph categories`, and `Open-graph and string-diagram rewriting` | **Adapt** one-TFS typed positions, valuation locality, exact internal `U.Transfer`, interface exposure, and replay-local rewrite discipline to recursively selected members. | A network keeps leaf-TFS position and valuation identity, resolves each exposed position through a finite member path, and leaves `U.Transfer` inside the TFS that contains it; cross-flow relations remain obtaining world-side occurrences under their applicable predicates. | Applies while E.18 keeps those position, valuation, `U.Transfer`, crossing, and replay-locality decisions. Reopen this line if E.18 changes any of them or its named source-use rows no longer support typed interfaces and localized rewrites. |
| `E.18.2:4.1` through `E.18.2:4.3` and the `E.18.2:9` rows `FPF strict-distinction, selected-structure, architecture-description, and view apparatus` and `Applied category theory, wiring diagrams, and graph rewriting` | **Adopt** the subject/description/lens separation and **adapt** the permitted expressions to member paths, n-ary relation views, quotients, and folds. | A mathematical description may expose or compare network structure only after naming its network subject, declared use, preserved structure, lost structure, and stop; it neither creates nor reidentifies the network or its relation occurrences. | Applies while E.18.2 keeps the five-way discriminator and the named rows' preserved/lost-structure and C.29 lens-use boundary. Reopen this line if the selected subject branch, preserved/lost account, mapping mode, or C.29 return condition changes. |
| `A.22.CGUS:4.4` and its `A.22.CGUS:11` rows on OCPQ and JuliaHub Dyad 3.2 with Modelica 3.7 as historical lineage; plus `E.18.3:4.2a`, `E.18.3:4.4`, and its `E.18.3:11` OCPQ and ModelingToolkit/FMI rows | **Adapt** typed object-and-relation structure, Dyad's current separation of reusable component models from separately selected analyses, and post-admission demonstration discipline to a network locator. | A network-aware demonstration consumes already admitted positions and exact relation-reference epistemes, keeps member-local state, branches, omissions, and return visible, and never turns the displayed path into the network, model, analysis, WorkPlan, or performed Work. | Applies while A.22.CGUS keeps Dyad as its current engineering comparator and Modelica only as historical lineage, and while CGUS and E.18.3 keep post-admission slices and exact locator admission. Reopen this line if those object-relation, model-analysis, admission, or locator decisions change. |

The F.18 NameCard entries `flow-of-flows` and `creator-graph` remain naming and stress-example lineage only; they authorize no current ontology or practice claim. A new need for cyclic member identity, a separately re-identifiable membership occurrence, or cross-flow semantics that cannot preserve the direct relation and its endpoints reopens the E.18.NET architecture decision itself, not the source-currentness status of every row above.


## E.18.NET:End {#end}
