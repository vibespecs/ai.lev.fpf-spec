# E.18.NET - Network of Transformation-Flow Structures {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Tech-name:** **TransformationFlowStructureNetwork**
> **Plain-name:** Network of transformation-flow structures
> **Type:** Structural pattern for ontic relations (E)
> **Status:** Stable
> **Normativity:** Normative unless explicitly marked informative

## E.18.NET:1 - Problem frame — intent and first useful result {#problem-frame-intent-and-first-useful-result}

Use this pattern when one engineering question depends on two or more independently identified transformation-flow structures, or on nested networks of them, and at least one exact relation connects positions across their boundaries. Typical situations include a toolchain that builds another tool, a production system related to the product it helps produce, or an operating flow whose observation returns to a separate development flow.

Start with the practical choice, not with a graph:

1. decide whether the case is several valuations of one flow structure, an internal portion of one flow structure, or a network of independent flow structures;
2. identify each candidate member independently;
3. name the exact obtaining relation occurrences that connect positions in different members;
4. select only the members, relations, boundary exposures, and constraints needed for the current question; and
5. return one exact network reference, or stop at the proposed description and name either the exact relation-claim result returned by its governing pattern or the separate missing network discriminator.

The first useful result is therefore small. It is either:

```text
selectedNetworkRef: one exact TransformationFlowStructureNetwork
directMemberRefs[]: at least two refs to independently identified TransformationFlowStructure or E.18.NET-conforming TransformationFlowStructureNetwork values
selectedCrossFlowRelationOccurrenceRefs[]: exact selected obtaining cross-flow relation occurrences
selectedNetworkConstraintRefs[]: exact applied endpoint, boundary-exposure, and acyclic direct-member constraints
networkUseFrame:
  questionOrAction: the concrete question answered or action enabled
  admissibleUse: how the selected organization is used
  stopOrReturnCondition: the exact boundary at which this use stops or returns to its basis
forbiddenOverread?: an explanatory guard justified by F.19:4, outside networkUseFrame
returnCondition: the first member, relation, constraint, or use-frame change that reopens selection
```

or an exact stop such as:

```text
proposedNetworkDescriptionRef: current diagram or record
blockedClaim: "the compiler-building flow produces the compiler-use flow input"
exactRelationClaimResultRefOrOutcome: exact result returned by the pattern that governs this claim
```

When the relation claim has a positive obtaining result but a network endpoint is not bound, keep that positive result and state a separate E.18.NET selection blocker:

```text
obtainingRelationOccurrenceRef: exact positive occurrence returned by its governing pattern
networkSelectionBlocker:
  missingEndpointOrPositionBinding: exact participant, member, position, or binding that is absent
```

An unavailable fact yields the governing pattern's `missing-information` outcome; a sufficient case basis that fails its positive test yields `factually unsupported`. Neither outcome alone asserts a negative. Carry an inapplicable or negative result only when that pattern's applicable rule and case basis establish it. A missing member, applied constraint, or `networkUseFrame` remains its own network-selection blocker and never becomes a relation result. Keep `proposedNetworkDescriptionRef` until all four A.22 discriminators—members, selected obtaining relation occurrences, applied constraints, and use frame—are recoverable; only then assert `selectedNetworkRef`.

Do not use E.18.NET merely because one flow branches, contains a detailed portion, has several valuations, or is drawn as a network. Use E.18 for one selected `TransformationFlowStructure`, its valuations and internal `U.Transfer` relations; use E.18's `SubflowRef` for one parent-relative internal portion. Use E.18.2 when the current object is a graph, wiring diagram, tuple, category-theory expression, or another mathematical description. Use A.22.CGUS and E.18.3 when the current object is an admitted demonstrative traversal rather than the network itself.

## E.18.NET:2 - Problem {#problem}

Teams routinely connect flows that concern different objects, Work occurrences, architecture boundaries, valuation state, and change cadence. A development TFS has positions for the Work that produces or changes a tool; other TFS values have positions for its use and evaluation, with feedback to development. A manufacturing system is changed through one flow while products are made through another. A compiler is built by one toolchain and then participates in a later build.

A single picture can hide three different ontic answers:

| Working situation | What is actually selected | What to do |
| --- | --- | --- |
| Several valuations, paths, or slices share one exact TFS identity | one `TransformationFlowStructure` | stay in E.18; do not mint another structure |
| A detailed portion resolves through positions and internal `U.Transfer` occurrences of one exact parent TFS | one parent-relative `SubflowRef` | stay in E.18; return through the parent's boundary positions |
| Independently identified TFS or nested-network values are connected by exact obtaining relations across their boundaries | one `TransformationFlowStructureNetwork` | apply this pattern |

When the third case is treated as one giant TFS, local state appears global, an internal `U.Transfer` is asked to mean production, use, evaluation, feedback, correspondence, and dependency, and a change in one member appears to reidentify everything. When the first or second case is over-split into a network, the model invents members and relations that the engineering situation does not need.

## E.18.NET:3 - Forces {#forces}

| Force | Tension to hold |
| --- | --- |
| Local autonomy vs one engineering question | Members keep their identity and state while a selected structure makes their exact coordination inspectable. |
| Recursive reuse vs fixed levels | A member may itself be a network, but membership paths must remain finite and acyclic. |
| Plain diagrams vs exact relations | A readable edge helps recognition, but only an obtaining relation of an admitted kind contributes to identity. |
| Boundary exposure vs flattening | A parent can use a nested boundary position without copying the nested member's internal structure. |
| Useful local state vs false global state | Valuation, path slice, and `DesignRunTag` remain local to one leaf TFS position binding. |
| Stable selection vs evolving members | Reidentify only when an A.22 discriminator changes; records, renderings, and selection Work remain separate. |

## E.18.NET:4 - Solution {#solution}

### E.18.NET:4.1 - Select a dependent non-agentive structure {#select-a-dependent-non-agentive-structure}

`TransformationFlowStructureNetwork@Context` is a dependent, non-agentive specialization of `U.Structure` defined by E.18.NET and selected through the A.22 identity law. It is not a root U-kind, acting system, holon, workflow, graph, record, publication, `FlowValuation`, WorkPlan, or performed Work. The `@Context` suffix qualifies retrieval and use; it adds no identity discriminator.

For `N : TransformationFlowStructureNetwork`, recover exactly:

```text
StructureIdentity(N) = <
  directMemberRefs[],
  selectedCrossFlowRelationOccurrenceRefs[],
  selectedNetworkConstraintRefs[],
  networkUseFrame
>
```

The four field names have the same meanings as in the first-use result: exact direct members, exact selected obtaining cross-flow occurrence refs, exact applied network constraints, and one concrete use frame. `returnCondition` is not a fifth identity discriminator; it records when the current use must return and reselect. `stopOrReturnCondition` states the boundary of the action or use within `networkUseFrame`; `returnCondition` names a change that reopens selection.

`forbiddenOverread?`, also named `groundedForbiddenOverread?`, carries one optional explanatory guard under F.19:4's plausible-reader test. It remains outside `networkUseFrame` and structure identity. A change to that explanation alone leaves the network unchanged; if its content changes an applied constraint or a use-frame value, compare that existing discriminator.

The direct-member set contains at least two exact values. Each member is one independently identified `TransformationFlowStructure` or one independently identified E.18.NET-conforming `TransformationFlowStructureNetwork`. At least one selected relation occurrence binds positions in different direct members or in different leaf TFS members reached through them. The use frame states the concrete question or action, how this selection will be used, and its stop or return condition. “Current use”, “appropriate network”, and the title of a diagram are not use frames.

The direct-member discriminator identifies the selected members; record rows cite those independently identified values. If a future receiver needs a separately re-identifiable world-side membership occurrence, apply the direct relation pattern that defines its participants, predicate, applicability, and identity rule. When that governor is missing, reopen the relation question under A.6.RCD.

### E.18.NET:4.2 - Reidentification and change locality {#reidentification-and-change-locality}

Replacing a direct member, selected relation occurrence, applied endpoint or exposure constraint, acyclicity constraint, or named selection-use frame identifies another selected network. Reidentifying a nested member reopens every parent network that selects that exact member.

Changing only a name, reference designator, record edition, graph layout, mathematical description, publication, selecting system, selection Work, evidence item, `FlowValuation`, `PathSliceId`, or local `DesignRunTag` leaves the network unchanged when the four A.22 discriminators still resolve to the same values.

### E.18.NET:4.3 - Recurse through finite member paths {#recurse-through-finite-member-paths}

The selected direct-member nesting is acyclic. No direct or transitive member path from a network resolves back to that network, and every member path used by a reference is finite. This permits build-the-builder and supply-network recursion without inventing level-1, level-2, or level-3 network kinds.

Cycles among selected cross-flow relation occurrences remain possible when their applicable predicates and constraints permit them. Feedback from operation or evaluation to development is therefore compatible with acyclic membership: the cycle is among those relation occurrences, not in network containment.

`E.18` defines the complete `FlowPositionRef` identity. Import that tuple unchanged; E.18.NET defines only the `ExposedFlowPositionRef` extension needed for a boundary position reached through one finite member path:

```text
FlowPositionRef := <
  transformationFlowStructureRef,
  localFlowPositionId
>

ExposedFlowPositionRef := <
  networkStructureRef,
  memberPath[],
  leafFlowPositionRef
>
```

Every hop in `memberPath[]` resolves through the preceding network's direct members. Its final member is the TFS named by `leafFlowPositionRef`. When the path crosses a nested network, the leaf position must be one of the boundary positions that nested network exposes for the current higher-level use. Two different paths to the same leaf TFS position are two different exposures.

The parent network may compose the finite path and use the exposed boundary. It may not copy or silently flatten the nested member's internal structure. `FlowValuation`, `PathSliceId`, actual fillings, and `DesignRunTag` qualify use of a position; they are not part of `FlowPositionRef` or `ExposedFlowPositionRef` identity.

### E.18.NET:4.4 - Keep valuation and design/run state leaf-local {#keep-valuation-and-design-run-state-leaf-local}

Each `positionBindingRef` cites an E.18 position/valuation binding or a declaration-local binding whose pattern defines the needed participant meanings, value kind, and reference mode. A network introduces no universal cross-flow value kind.

`DesignRunTag` belongs to one exact position binding inside one exact leaf TFS. A network has no network-level `FlowValuation`, global design/run ladder, or automatic crossing that changes the carried entity's kind. If the same episteme fills local positions in different members—for example one position concerned with design work and another with production, verification, or later operation—record each leaf-local binding and the exact relation that obtains between them. Those ordinary member descriptions create no fixed TFS taxonomy or lifecycle phase.

### E.18.NET:4.5 - Preserve the direct cross-flow relations {#preserve-the-direct-cross-flow-relations}

For every relation used by the network, recover:

- the exact obtaining occurrence;
- the exact relation kind;
- the pattern that defines or tests its predicate, applicability, and occurrence-identity rule;
- the complete participant signature and participant order;
- the endpoint member and position binding for every participant; and
- direction only when the direct relation has direction.

An n-ary relation remains n-ary. Do not decompose it into invented binary arrows. A row, edge label, shared entity, temporal adjacency, operation result, plan row, or graph connection never makes the relation obtain.

`U.Transfer` remains E.18's internal relation kind for one TFS. It is not a universal relation between network members. For any production, use, participation, evaluation, correspondence, feedback, dependency, supply, or other cross-flow relation, the relation kind must already be admitted. Use its applicable relation pattern to recover the participant meanings, predicate, applicability, and occurrence-identity rule; current case facts or constituting history must satisfy the predicate affirmatively. Only then does one world-side occurrence obtain. Use A.6.REL only when a named use must distinguish that occurrence from another. For ordinary network selection, the PatternID and exact relation occurrence are enough; add `relationFunctionClaimRef` to the defining or constraining `ClaimGraph` only when comparison, migration, or reliance depends on that exact rule identity. The network selects only the exact already-obtaining occurrence ref.

If no admitted relation kind and applicable predicate cover the intended participants and use, carry `missing-governor` from the pattern governing the relation claim. If required case facts are unavailable, carry its `missing-information` result; if the available basis is sufficient to apply the positive test but that test fails, carry `factually unsupported`. Neither result by itself establishes a negative. Carry an inapplicable or negative result only when the governing pattern defines that outcome and its current basis establishes it. Only a positive obtaining occurrence may fill `selectedCrossFlowRelationOccurrenceRefs[]`.

After a positive occurrence is established, test the E.18.NET endpoint and position bindings separately. A missing binding blocks network selection but does not change the relation result. Missing members, applied constraints, and use-frame values are likewise separate network-selection blockers. A row, graph edge, or episteme neither admits a relation kind nor creates an occurrence. In none of these branches substitute `creates`, `produces`, `uses`, `input`, `output`, `result`, `handoff`, or `transfer` as a generic edge.

### E.18.NET:4.6 - Record the network without replacing it {#record-the-network-without-replacing-it}

When the selected answer must survive beyond the immediate work, describe it with a separate C.2.1 episteme:

```text
TransformationFlowStructureNetworkRecord@Context <: U.Episteme:
  entityOfConcernRef: one exact TransformationFlowStructureNetwork ref
  entityOfConcernKindRef: TransformationFlowStructureNetwork
  claimScope?: U.ClaimScope
  effectiveReferenceScheme: U.ReferenceScheme
  directMemberRows[]:
    memberRef: TransformationFlowStructureRef | TransformationFlowStructureNetworkRef
  exposedFlowPositionRows[]:
    exposedFlowPositionRef: ExposedFlowPositionRef
    memberPath[]
    leafTransformationFlowStructureRef
    leafFlowPositionRef
  crossFlowRelationRows[]:
    exactRelationOccurrenceRef: U.RelationRef
    exactRelationKindRef: U.KindRef
    subjectPatternLocator: U.EntityRef, locating the pattern that defines or tests this relation
    relationFunctionClaimRef?: U.EntityRef, referencing the exact defining or constraining ClaimGraph when the recorded use depends on that rule identity
    endpointRows[]:
      relationParticipantPositionRef
      memberRef
      flowPositionRef: FlowPositionRef | ExposedFlowPositionRef
      positionBindingRef
  architectureCorrespondenceRowRefs[]?: C.32.CONWAY episteme refs
  selectedNetworkConstraintRefs[]
  networkUseFrame
  preservedNetworkStructure
  lostOrHiddenNetworkStructure
  returnCondition
```

The record describes the network; it is not the network. Its member and relation rows cite objects that already exist and occurrences that already obtain. An architecture-correspondence row is a qualified reading only. It contributes no member or selected cross-flow relation unless an exact separately grounded relation occurrence and endpoint bindings also satisfy the network identity.

E.18.NET defines this composite locator for one nested cross-flow row:

```text
NetworkCrossFlowRelationRowRef := <
  transformationFlowStructureNetworkRecordRef: U.EpistemeRef, referencing one exact current TransformationFlowStructureNetworkRecord@Context edition,
  exactRelationOccurrenceRef: U.RelationRef,
  orderedEndpointBindingIdentity[]: <
    relationParticipantPositionRef,
    memberRef,
    flowPositionRef: FlowPositionRef | ExposedFlowPositionRef,
    positionBindingRef
  >
>
```

Resolve the record ref first, then match `crossFlowRelationRows[]` by the exact occurrence ref and the complete ordered endpoint-binding identity. Exactly one row must match. Zero matches or several matches leave the locator unresolved and stop that consumer; never fall back to the containing record, the occurrence alone, or a prose pointer. `NetworkCrossFlowRelationRowRef` is a reference shape, not a U-kind, episteme, or relation occurrence. Its `U.EpistemeRef` targets the containing record, never the nested row.

### E.18.NET:4.7 - Keep descriptions, demonstrations, architecture, and Work outside identity {#keep-descriptions-demonstrations-architecture-and-work-outside}

Use E.18.2 for a graph, hypergraph, network expression, wiring diagram, category-theory object, tuple, fold, or other mathematical description of the selected network. State what that description preserves and loses. A rendered graph or publication face remains under E.17 and C.29 as applicable.

Use A.22.CGUS and E.18.3 for an admitted network-aware `DemonstrativeUnfoldingSlice@Context`. Its finite paths must map to already admitted included positions, its cross-flow relations must cite admitted exact relation-reference epistemes, and its tags remain in leaf-local bindings. The slice demonstrates one traversal; it is neither the network nor an actual trajectory, WorkPlan, or Work occurrence.

Use C.30.TFS-REL when architecture uses the selected network. Name one exact containing holon whose `ArchitectureOf@Context` selects the network, or explicitly state the inter-holon use and its participating architecture claims without inventing a bearer. Use C.32.CONWAY only for its one-pair architecture-influence reading; the pair does not become the network.

Only admitted Systems perform Work. Selecting a network, writing its record, or drawing its graph may be Work when A.15.1 independently admits the occurrence after each precise performer has an A.13 core; none is performance by the network, and no Work claim is needed merely to select or discuss the network. When selection Work is material, cite those already established A.13 and A.15.1 results. Cite F.6 only when the current network account also needs precise assignment-bound attribution, and leave its proof with F.6. Keep the Method, performer, dated Work, result episteme, selection or decision relation, and any C.11 choice result separate. A result episteme is not a decision or accountability relation by form; state accountability, duty, responsibility, or authority only through the exact direct relation that obtains.

## E.18.NET:7 - Conformance Checklist {#conformance-checklist}

| ID | Requirement | Failed-check repair |
| --- | --- | --- |
| **CC-E18-NET-01 Three-way discriminator** | @fact:CC-E18-NET-01 The case is explicitly distinguished from several valuations of one exact TFS and from one E.18 `SubflowRef`. @status:spec/done | Return to member identity and relation basis; do not decide from diagram shape, team labels, or stage names. |
| **CC-E18-NET-02 A.22 identity** | @fact:CC-E18-NET-02 Exact direct members, selected obtaining cross-flow occurrences, applied constraints, and one concrete selection-use frame are recoverable. @status:spec/done | Recover the missing discriminator or stop at a proposed description. |
| **CC-E18-NET-03 Independent members** | @fact:CC-E18-NET-03 Every member keeps its own TFS or independently identified E.18.NET-conforming network identity, transformations, Work, valuations, boundaries, and local state. @status:spec/done | Split any merged object; reidentify each member under E.18 or E.18.NET and restore its own Work, valuation, boundary, and state. |
| **CC-E18-NET-04 Finite acyclic membership** | @fact:CC-E18-NET-04 Every member path is finite and no member path returns to the same network. @status:spec/done | Repair the selected member set or return the cyclic-membership blocker; do not add level kinds. |
| **CC-E18-NET-05 Exposed position** | @fact:CC-E18-NET-05 Every `ExposedFlowPositionRef` resolves hop by hop to an exposed leaf TFS position. @status:spec/done | Recover the missing member hop or boundary exposure; do not flatten the nested network. |
| **CC-E18-NET-06 Leaf-local state** | @fact:CC-E18-NET-06 Every valuation, path slice, and `DesignRunTag` remains attached to one exact leaf-TFS binding. @status:spec/done | Remove the network-global state field and restore the local bindings. |
| **CC-E18-NET-07 Direct relations** | @fact:CC-E18-NET-07 Every selected cross-flow relation has an admitted kind, applicable predicate, exact positive obtaining occurrence, complete participant order, and grounded endpoint bindings. The governing pattern's relation result remains distinct from E.18.NET selection blockers. @status:spec/done | Carry that pattern's exact `missing-governor`, `missing-information`, `factually unsupported`, or positive result; carry an inapplicable or negative result only when that pattern defines it and the case basis establishes it. After a positive result, name a missing endpoint binding separately; do not rewrite it as a relation failure. |
| **CC-E18-NET-08 N-ary preservation** | @fact:CC-E18-NET-08 Participant count, order, kinds, positions, and direction match the direct relation. @status:spec/done | Restore the direct participant signature and remove invented binary decompositions. |
| **CC-E18-NET-09 Record and row-locator separation** | @fact:CC-E18-NET-09 Member rows and relation rows describe already identified objects and occurrences; the record does not create them, and every `NetworkCrossFlowRelationRowRef` resolves exactly one nested row by record, occurrence, and ordered endpoint-binding identity. @status:spec/done | Separate the C.2.1 episteme from the selected `U.Structure`; repair or remove any locator that resolves zero or several rows. |
| **CC-E18-NET-10 Non-agentivity** | @fact:CC-E18-NET-10 The selected network is non-agentive. Its identity needs no actor or selection-Work claim; any actual selection Work has a separately identified System performer and occurrence. @status:spec/done | Describe the network through direct members, selected obtaining occurrences, endpoint bindings, applied constraints, and its use frame. If actual selection Work is current, cite every precise performer's A.13 core and the independent A.15.1 Work admission; cite F.6 only when exact assignment-bound attribution is also current. Keep result episteme, choice, decision, and accountability relations separate. |
| **CC-E18-NET-11 Representation boundary** | @fact:CC-E18-NET-11 Mathematical descriptions, graphs, views, publications, and demonstrations are identified separately and state preserved/lost structure when relied on. @status:spec/done | Apply E.18.2, C.29, E.17, A.22.CGUS, or E.18.3 as appropriate. |
| **CC-E18-NET-12 Useful result or stop** | @fact:CC-E18-NET-12 The practitioner receives one exact network ref and return condition, or a proposed description with one exact reason selection cannot close: the governing pattern's relation-claim result, or a separate absent member, applied constraint, use frame, endpoint, or position binding. @status:spec/done | Restore the exact result or blocker at its own layer; do not end with a local status taxonomy or make a network-selection blocker change the relation result. |

## E.18.NET:9 - Consequences {#consequences}

| Gain | Cost or trade-off |
| --- | --- |
| Independent flows can be coordinated without losing their identity or local change boundary. | Members and cross-flow relations must be grounded before the network can be claimed. |
| Recursive networks scale without numbered levels. | Exposed positions require finite path resolution and explicit boundary selection. |
| Cross-flow relations keep their participant meanings and n-ary signatures. | A missing relation kind or predicate remains visible instead of being hidden by a convenient generic edge. |
| Local valuations and tags remain usable without becoming global state. | A network record carries more explicit member and endpoint references than a simple graph. |
| Graphs and mantras remain useful descriptions. | Their distinct claims use E.18.2 or E.17 for descriptions and publications, A.22.CGUS or E.18.3 for demonstrations, C.30.TFS-REL for architecture use, A.15 for Work, and E.18.NET for the selected network. |

Adoption test: use E.18.NET only when the current question needs independently identified members and at least one exact relation across their boundaries. If one TFS or one parent-relative `SubflowRef` answers the question, the added network, endpoint, and member-path apparatus buys nothing and stays absent.

## E.18.NET:12 - Relations {#relations}

Builds on: `A.22` for selected-structure identity and non-agentivity; `E.18` for one TFS, internal `U.Transfer`, `FlowPositionRef`, valuations, paths, slices, and local state; `A.6.REL`, `A.6.RCD`, and `A.6.P.WMR` for exact relation recovery and `missing-governor`; `C.2.1` for the optional descriptive record; and `F.18` for the stable local name.

Coordinates with: `A.15.6` for actual project Work, project system-of-interest designation, and subject- or claim-centred case closure; `A.1.STM` for a Plain provisional long-mantra display and backward/forward attention use; `E.18.2` and `C.29` for mathematical descriptions; `A.22.CGUS` and `E.18.3` for admitted demonstrative slices; `C.30.TFS-REL` for architecture use; `C.32.CONWAY` for one qualified architecture-influence pair; `A.3.4`, `A.12`, and the A.15 family for actual transformation, causal or acting positions, Work, production, and work-to-change claims; `E.17` for publication; `E.11` for public entry and recognition; and `E.11.PUA` for using one already selected pattern to reach its first useful result.

Does not replace: the direct pattern that defines or constrains any selected production, use, participation, evaluation, feedback, dependency, correspondence, supply, evidence, assurance, gate, decision, causal, or work relation. E.18.NET selects already obtaining occurrences for one network use; it does not mint their kinds or make them obtain.


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/A-22#root, spec://ai.lev/fpf-spec/contract/E-18#root, spec://ai.lev/fpf-spec/contract/A-6-REL#root, spec://ai.lev/fpf-spec/contract/A-6-RCD#root, spec://ai.lev/fpf-spec/contract/C-2-1#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/A-15-6#root, spec://ai.lev/fpf-spec/contract/A-1-STM#root, spec://ai.lev/fpf-spec/contract/E-18-2#root, spec://ai.lev/fpf-spec/contract/A-22-CGUS#root, spec://ai.lev/fpf-spec/contract/E-18-3#root, spec://ai.lev/fpf-spec/contract/C-30-TFS-REL#root, spec://ai.lev/fpf-spec/contract/C-32-CONWAY#root, spec://ai.lev/fpf-spec/contract/A-3-4#root, spec://ai.lev/fpf-spec/contract/A-12#root, spec://ai.lev/fpf-spec/contract/A-15#root family, spec://ai.lev/fpf-spec/contract/E-11#root, spec://ai.lev/fpf-spec/contract/E-11-PUA#root, spec://ai.lev/fpf-spec/contract/E-17#root, spec://ai.lev/fpf-spec/contract/C-29#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-1-STM#root, spec://ai.lev/fpf-spec/contract/A-15-6#root, spec://ai.lev/fpf-spec/contract/A-22#root, spec://ai.lev/fpf-spec/contract/A-22-CGUS#root, spec://ai.lev/fpf-spec/contract/C-30-TFS-REL#root, spec://ai.lev/fpf-spec/contract/C-32-CONWAY#root, spec://ai.lev/fpf-spec/contract/E-11-PUA#root, spec://ai.lev/fpf-spec/contract/E-18#root, spec://ai.lev/fpf-spec/contract/E-18-2#root, spec://ai.lev/fpf-spec/contract/E-18-3#root, spec://ai.lev/fpf-eng-ops/contract/OPS-11#root, spec://ai.lev/fpf-eng-str/contract/STR-8#root, spec://ai.lev/fpf-eng-syse/contract/SYSE-18#root, spec://ai.lev/fpf-eng-syse/contract/SYSE-20#root, spec://ai.lev/fpf-eng-syse/contract/SYSE-3#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/E-18-NET
