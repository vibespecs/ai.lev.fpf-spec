# A.6.M - Module and Interface Claim Repair {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Architectural pattern
> **Status:** Stable
> **Normativity:** Normative unless explicitly marked informative

## A.6.M:1 - Problem frame {#problem-frame}

Use this pattern when an architecture or engineering text says "module", "component", "interface", "port", "platform", or "open architecture", and the phrase is doing more than ordinary orientation. If a stratification or architecture-operation source label covered by `C.30.STRAT` is doing the work, apply `C.30.STRAT` first; use A.6.M only when that repair recovers module-interface claim content. Use A.6.M when the question under repair is whether one holon is being claimed as a replaceable, reusable, or separately changed structural unit of a larger holon under the exact `VP.ModuleInterface` viewpoint episteme. The note or claim does not make a direct module relation obtain.

The first useful output is `ModuleRelationRepairNote`, a claim-repair note rather than a relation occurrence:

```text
ModuleRelationRepairNote:
  wholeHolonRef:
  candidateModuleHolonRef:
  effectiveReferenceScheme: U.ReferenceScheme, byValue
  claimScope?: U.ClaimScope, byValue
  modelUseStructureRef?: only when one selected model-use structure changes module meaning
  moduleInterfaceViewpointRef?: VP.ModuleInterface
  selectedDependencyStructureRef?: U.StructureRef
  boundaryRef:
  interfaceSpecificationRef?: U.EpistemeRef constrained to InterfaceSpecification
  interfaceSpecificationGap?: exact missing-specification result
  admissibilityConditions:
  substitutabilityPolicyRef?:
  changePolicyRef?:
  directModuleRelationDisposition:
    noDirectRelationClaimed | admittedRelationAndOccurrence | missingGovernor
  admittedRelationKindOrDeclarationRef?:
  obtainingRelationOccurrenceRef?: U.RelationRef
  missingRelationParticipantRefs?:
  proposedPredicate?:
  affectedUse?:
  futureDefinitionNeed?:
  definingPatternLocator?: PatternID used only as a locator
  claimBoundary:
  notAModuleBecause:
  governedNonModuleClaimPatternRefs:
  stopCondition:
```
Exactly one of `interfaceSpecificationRef` and `interfaceSpecificationGap` is current. `noDirectRelationClaimed` leaves every direct-relation field empty. `admittedRelationAndOccurrence` requires an exact admitted relation kind or defining declaration plus one separately obtaining occurrence. `missingGovernor` names the actual participants, proposed predicate, affected use, and missing definition or declaration; a PatternID may locate an applicable rule but cannot fill any of those positions.

Ordinary use stops when the whole, candidate module, boundary, interface specification, admissibility conditions, substitutability policy, change policy, blocked false interpretation, relation disposition, and neighboring work, procedural, role, or enactor subject-pattern choice are clear enough to choose the next architecture move. Use the fuller `ModuleInterfaceClaim` record only when substitutability, conformance, publication, evidence, assurance, change policy, repeated reuse, or cross-team coordination requires durable claim content.

What goes wrong if A.6.M is missed: a functional link becomes a module interface; a signature becomes an implemented interface; a port label becomes proof of integration; "open" becomes a decoration; a platform label hides the actual extension rules; a stratification or architecture-operation source label bypasses `C.30.STRAT` and mints a false local kind; autonomy-like wording is confused with separate module change policy; and a module diagram starts being used for claims governed elsewhere.

What A.6.M buys in practice: the practitioner can repair one module or interface phrase into usable claim content, distinguish it from an independently admitted direct relation occurrence, see which FPF pattern defines or constrains any remaining non-module claim, and stop before full measurement, evidence, or mechanism-suite records are needed.

Not this pattern when the question under repair is the general architecture claim, selected architecture structure kind, structural view, stratification wording or source-label recovery, function wording, procedural or work-package wording, role or enactor wording, autonomous operation, independent acting, unsupervised decision or action, measurement, modularity characterization, or reusable-structure residue. Use `C.30`, `C.30.ASV`, `C.30.STRAT`, `A.6.F`, `A.15`, `A.2`, `E.16`, `C.31`, `C.16`, or `C.31.RSA` as appropriate. For any other claim being made, apply the governing FPF pattern and keep A.6.M only for the module-relation and interface-specification portion.

**E.10.ARCH relation.** A.6.M is the precision-restoration pattern for module-interface relation wording, interface-specification wording, platform-grammar wording, substitutability wording, change-policy wording, and open-architecture module-interface claims. `E.10`, `E.10.ARCH`, or `C.30.STRAT` applies A.6.M only after the recovered result is a module-interface relation, interface specification, platform grammar, substitutability policy, change policy, or open-architecture module-interface claim. If the source wording is still a stratification or architecture-operation source label covered by `C.30.STRAT`, apply `C.30.STRAT` first. If the claim being made is non-module work, role, evidence, assurance, gate, decision, characteristic, flow, autonomy, component, mechanism, or mathematical-lens use, apply the subject pattern named in `A.6.M:12` and keep A.6.M only for the module-interface slice when that module-interface relation remains the claim being made.

## A.6.M:2 - Problem {#problem}

Engineering teams use module language for several different things:

- a component in a part-whole decomposition;
- a replaceable unit under a declared interface;
- a functional element;
- a software package, neural-network block, hardware board, chiplet, subsystem, service, team boundary, or delivery unit;
- a published API, protocol, signature, port, connector, or endpoint;
- a platform extension point;
- a control relation, deployment scope, or stratification or architecture-operation source label that still needs `C.30.STRAT` recovery;
- an open-architecture claim.

These are useful ordinary words, but they do not establish the same FPF claim. A module claim is not created by a label. A conforming module-interface claim names the candidate `U.Holon`, larger `U.Holon`, exact `VP.ModuleInterface` viewpoint episteme when needed, boundary, interface specification, admissibility conditions, substitutability policy when replacement is claimed, change policy when separate change is claimed, and any exact evidence, conformance, or admissible-use claim being made. It remains claim content unless a separate direct relation pattern has admitted a module relation and its obtaining predicate is satisfied.

The practical question is: does this phrase name a module relation, component relation, functional allocation, procedural or work-package relation, exact system-role-assignment occurrence, direct domain responsibility relation, deployment or placement structure, interface specification, signature declaration, port or endpoint slot, transformation-flow crossing, mechanism realization, platform grammar, control relation, autonomy-like operation claim, source label governed first by `C.30.STRAT`, or only plain source wording?

## A.6.M:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Engineering convenience vs relation precision | Practitioners need short words such as module and interface, but claim-bearing use must recover both holons, the boundary, interface specification, admissible use, and whether an independently admitted direct relation is actually current. |
| Module claim vs root or relation kind | A candidate module keeps its direct holon kind. Neither the source word nor a `ModuleInterfaceClaim` record admits `U.Module` or a general direct module relation; a reusable relation needs its own A.6.RCD settlement. |
| Interface label vs interface specification | An API name, port label, connector label, or signature may substantiate an interface claim, but it is not by itself substitutability or conformance. |
| Function-flow-module proximity vs false identity | Functions, E.18 flow relations, control relations, mechanisms, and module interfaces often meet at the same artifact, but each has a different subject pattern. |
| Open architecture payoff vs open label overread | MOSA and open-system practice make open interfaces useful only with standards, conformance expectations, replacement or change policy, and data or access constraints when those conditions are part of the claim being made. |
| Team boundary vs module boundary | Conway's law and mirroring practice make team communication boundaries and delivery-responsibility scopes architecture-relevant, but they do not turn a team boundary, delivery unit, system-role assignment, or responsibility relation into a module interface by identity. Assignment also does not establish responsibility: cite an admitted direct domain predicate with its actual participants or the exact A.6.RCD missing governor. |
| Parallel decomposition vs serial bottleneck | Amdahl-style reasoning makes serial work, synchronization, communication overhead, and shared resource limits visible; more modules, teams, or parallel transformation-flow paths do not automatically improve throughput or evolvability. |
| Cheap repair vs full evidence pack | Most cases need a relation repair note, not a full conformance, evidence, assurance, gate, or mechanism-suite record. |

## A.6.M:4 - Solution {#solution}

A.6.M specializes `A.6.P` for module, component, interface, platform, and open-architecture wording when the recovered result is module-interface claim content, an interface specification, platform grammar, substitutability claim, or open-architecture module-interface claim. Stratification or architecture-operation source labels covered by `C.30.STRAT` are governed by `C.30.STRAT` until that repair recovers this module-interface content. A.6.M neither mints root kinds from those labels nor admits a direct module relation from record syntax.

A candidate module is an exact `U.Holon` used in a claim that treats it as a replaceable, reusable, or separately changed structural unit of a larger `U.Holon`, ordinarily under the exact `VP.ModuleInterface` viewpoint episteme. The claim names its boundary, interface specification, admissibility conditions, substitutability policy when replaceability is claimed, and change policy when separate change is claimed. Effective `U.ReferenceScheme` and `U.ClaimScope` qualify the claim; an optional selected model-use structure appears only when its organization changes module meaning. None replaces the two holons or makes a module relation obtain. A `FunctionalElementClaim` is different: it is view-local claim content inside a functional structural-view episteme, not a root kind and not a module relation. It binds required behaviour or effect to bearer or candidate bearer, capability, functional ports, and allocation claims when those claims are current; required or desired content is not an actual `U.Transformation`. The relation between functional and module claims is separately governed allocation or correspondence, not identity. One module candidate can correspond to many functional elements; many module candidates can correspond to one functional element; a functional element can remain unallocated; and a module candidate can be present in a module-interface view with no current functional behaviour in the functional view.

Functional ports and module interfaces may both use `U.Signature` discipline, but they govern different claims. A functional port constrains input condition, output condition, accepted-state, and produced-state slots for a functional behavior or transformation. A module interface constrains boundary, substitutability, compatibility, protocol references, schema references, version policy, change policy, and conformance expectations for a module relation. Do not move a functional-port claim into module-interface structure unless a module-interface or substitution claim is actually being made.

For modular synthesis, A.6.M supplies only the module-interface claim slice. A synthesis action may align required functional claims under `VP.Functional`, transformation-flow topology under `E.18` and `C.30.TFS-REL`, control structure under `C.30.LCA`, procedures and work packages under `VP.Procedural`, and module and interface claims under `VP.ModuleInterface`. `VP.AllocationResponsibility` is only a recognition cue for allocation or responsibility concerns: a positive responsibility claim needs its admitted direct domain predicate, actual participants, applicability, and occurrence identity, or the exact A.6.RCD missing-governor result. Use A.6.M to repair claims about modules and their interfaces; non-module candidate generation, allocation, responsibility, evidence, assurance, decision, Work, and characteristic claims remain with their direct patterns.

### A.6.M:4.1 - `ModuleInterfaceClaim` record {#moduleinterfaceclaim-record}

Use `ModuleInterfaceClaim` only when the light repair note is not enough and durable claim content is needed. Its Plain reading is *claim about a module and its interface in a larger whole*.

The F.18 comparison also covered `ModuleUseClaim`, `ModuleInWholeClaim`, and `ModuleRelationClaim`. The selected pair keeps the claim and interface visible without predicate syntax. `ModuleUseClaim` can suggest operational use, `ModuleInWholeClaim` can suggest a spatial or part-whole predicate, and `ModuleRelationClaim` can suggest that a direct relation has already been admitted. Reopen the naming choice only if the governed content changes or repeated reader error shows that this distinction is still not recoverable.

```text
ModuleInterfaceClaim:
  claimEpistemeRef: U.EpistemeRef
  entityOfConcernRef:
    moduleHolonRef | selectedDependencyStructureRef |
    admittedDirectModuleRelationOccurrenceRef
  effectiveReferenceScheme: U.ReferenceScheme, byValue
  claimScope?: U.ClaimScope, byValue
  modelUseStructureRef?: U.StructureRef
  moduleHolonRef: U.HolonRef
  wholeHolonRef: U.HolonRef
  viewpointRef?: U.ViewpointRef = VP.ModuleInterface
  selectedDependencyStructureRef?: U.StructureRef
  boundaryRef: BoundaryRef
  interfaceSpecificationRef?: U.EpistemeRef constrained to InterfaceSpecification
  interfaceSpecificationGap?: exact missing-specification result
  functionalCorrespondenceRelationRefs?: FinSet(U.RelationRef)
  transformationFlowStructureRefs?: FinSet(U.StructureRef)
  transformationFlowRelationOccurrenceRefs?: FinSet(U.RelationRef)
  mechanismRefs?: FinSet(U.EntityRef constrained by the selected mechanism pattern)
  dependencyRelationOccurrenceRefs?: FinSet(U.RelationRef)
  substitutabilityPolicyRef?: U.EpistemeRef
  changePolicyRef?: U.EpistemeRef
  variabilitySlotRefs?: FinSet(SlotSpecRef)
  evidenceOrSourceRelianceRelationRefs?: FinSet(U.RelationRef)
  directModuleRelationDisposition:
    noDirectRelationClaimed | admittedRelationAndOccurrence | missingGovernor
  admittedRelationKindOrDeclarationRef?:
  obtainingRelationOccurrenceRef?: U.RelationRef
  missingRelationParticipantRefs?:
  proposedPredicate?:
  affectedUse?:
  futureDefinitionNeed?:
  definingPatternLocator?: PatternID used only as a locator
  admissibleUse
  nonAdmissibleUse
```

This form is claim content in one C.2.1 episteme. Its identity uses that content, the one exact `entityOfConcernRef`, and the effective `U.ReferenceScheme`. `claimScope` qualifies the claim when its coverage matters. `modelUseStructureRef` is present only when one independently selected model-use structure changes the meaning of *module* for this claim; it is not a module participant, whole, boundary, or source of relation obtaining. `VP.ModuleInterface` is a reference to the exact viewpoint episteme when viewpoint use matters; citing it does not make this claim a `U.View`. The interface-specification and direct-relation fields obey the same exclusive branches as `ModuleRelationRepairNote`. If `entityOfConcernRef` names an admitted direct module-relation occurrence, the disposition is `admittedRelationAndOccurrence` and `obtainingRelationOccurrenceRef` resolves that same occurrence. Under the other two dispositions, `entityOfConcernRef` stays with the module holon or selected dependency structure.

A `ModuleInterfaceClaim` record, package path, file boundary, graph edge, list position, common name, or publication does not make a world-side module relation obtain. Current A.6.M admits no general direct module relation kind. If repeated engineering use genuinely needs one direct module relation occurrence, first use the applicable subject rule and `A.6.RCD` to recover the exact module and whole participant meanings, obtaining predicate, applicability, recurrence rule, and occurrence-identity rule. Use `A.6.REL` only after that relation is admitted and a later use must distinguish one obtaining occurrence from another. A separately constituted `RelationSignature` may then declare reusable SlotSpecs; neither the signature nor this claim creates the occurrence.

Well-formedness: the claim names both holons, one exact EntityOfConcern, an effective reference scheme, one boundary, and exactly one of an interface-specification reference and an explicit interface-specification gap. Its direct-relation disposition has exactly the fields required by the selected branch. Optional structure, relation, evidence, mechanism, policy, conformance, source, and reliance references are used only when those exact objects and claims are current under their direct rules.

### A.6.M:4.2 - Interface specification is not a label {#interface-specification-is-not-a-label}

A.6.M calls the independently identified specification episteme an `InterfaceSpecification`. It is one `U.Episteme` under C.2.1 whose `EntityOfConcern` is the exact boundary named by the module claim. Its identity is `<exact ClaimGraph, that one EntityOfConcern, effective U.ReferenceScheme>`. Its claim content may include:

```text
InterfaceSpecification claim content:
  signatureRefs?: FinSet(SignatureRef)
  slotSpecSetRefs?: FinSet(SlotSpecSetRef)
  portEndpointSpecRefs?: FinSet(PortEndpointSpecRef)
  protocolRefs?: FinSet(EpistemeRef)
  schemaRefs?: FinSet(EpistemeRef)
  admissibilityConditions
  semanticConditions
  versionPolicyRef?
  changePolicyRef?
  conformanceExpectationRefs?
  evidenceOrSourceRelianceRefs?
  nonAdmissibleUse
```

`interfaceSpecificationRef` is one `U.EpistemeRef` constrained to that specification form. Under the effective reference scheme it resolves one already identified `InterfaceSpecification`; it carries none of the specification content itself. Two spellings or serialized references may resolve the same unchanged specification. Retargeting the reference selects another already identified specification without changing the previous one. Changing identity-bearing specification content, its `EntityOfConcern`, or its effective reference scheme yields another episteme. When no complete specification is established, keep an explicit `interfaceSpecificationGap` rather than a partly filled reference.

A signature declares vocabulary, laws, and applicability. A slot or endpoint record names positions and field structure. A protocol or schema constrains interaction. A mechanism reference can substantiate a realization relation. Evidence relations, source relations, reliance relations, and conformance expectations substantiate reliance only when the corresponding evidence, source-use, assurance, or conformance claim is being made. None of these, alone, is the module interface.

### A.6.M:4.3 - Repair applications for overloaded words {#repair-applications-for-overloaded-words}

| Source wording | Governing repair application |
| --- | --- |
| `component` | First recover the claim actually made under `A.14`: for example `ComponentOf`, `ConstituentOf`, `PortionOf`, belonging under the collection's own rule, or `PhaseOf`. Apply A.6.M only when a module-interface relation is being claimed. |
| `module` | Recover a `ModuleInterfaceClaim` or `ModuleRelationRepairNote` over exact `U.Holon` refs under the exact `VP.ModuleInterface` viewpoint episteme when needed. Do not infer a direct relation occurrence; use an admitted direct relation only when its defining rule exists and current facts make its predicate obtain. |
| `functional element` | Keep it as `FunctionalElementClaim` inside a functional structural-view episteme; use `A.6.F` to repair wording and connect it to module-interface structure only through an exact allocation or correspondence relation. Keep required or desired behaviour as claim content. Cite an actual `U.Transformation` only when A.3.4 independently supplies its changed referent, boundary, conditions, actual before/during/after facts, and continuity basis. |
| `work package`, `delivery unit`, or `team boundary` | Keep Work, Method, WorkPlan, exact system-role kind and assignment, and responsibility claims separate. Use `A.15`, `A.2`, and `VP.Procedural` for their own objects; treat `VP.AllocationResponsibility` only as a cue, then cite the direct allocation or responsibility predicate or the exact missing governor. Relate those facts to module-interface structure only through a declared correspondence, allocation, or boundary relation. |
| `deployment scope` or `placement` | Recover a deployment or placement structure under `C.30` or `C.30.ASV` when that deployment or placement structure is being claimed. Relate it to module-interface structure only through declared correspondence or boundary relation. |
| `interface` | Recover the independently identified `InterfaceSpecification` episteme and an `interfaceSpecificationRef` that resolves it, not a wire, API label, port label, E.18 transformation-flow relation, or function by itself. |
| `signature` | Keep as A.6.0 declaration. It is not an implemented interface, mechanism, gate, evidence row, or substitution policy. |
| `port` or `endpoint` | Recover `SlotSpec`, endpoint field, or interface-specification field when the claim is being made. It is not a module, graph edge, transformation-flow crossing, or proof of integration. |
| `functional link` | Keep it as claim content in a functional structural-view episteme; relate it to module claims only through an exact correspondence, allocation, or retargeting relation. |
| `E.18 transformation-flow relation` or `path` | Keep under `E.18` and `C.30.TFS-REL`; it may inform an architecture-to-transformation-flow relation, but it is not an interface specification. |
| `platform` | Recover `PlatformGrammarRef`: extension rules, variability slots, interface specifications, substitution policy, and conformance expectations when platform extension, variation, substitution, or conformance use is being claimed. |
| stratification or architecture-operation source label | Apply `C.30.STRAT` first. Use A.6.M only when the recovered result is a module-interface relation, interface specification, platform grammar, substitutability policy, change policy, or open-architecture module-interface claim. Otherwise apply `C.30.LCA`, `C.30.ASV`, `A.6.F`, `E.18`, `C.16.P`, `C.29`, `C.2.P`, or use ordinary source-label disposition when no FPF-governed claim remains. |
| `open architecture` | Recover an `OpenArchitectureClaim` episteme: published interface specifications, substitution rules, change policy, data-rights or access constraints when those constraints are part of the claim, and exact conformance, evidence, source, or reliance relations only when that stronger reliance claim is being made. |

### A.6.M:4.4 - First repair sequence {#first-repair-sequence}

1. Name the phrase and the practical situation.
2. Select the whole holon and candidate module holon.
3. State whether the source phrase is module relation, component relation, function allocation, procedural or work-package relation, exact system-role-assignment occurrence, direct responsibility relation, deployment or placement structure, interface specification, signature, port or endpoint, transformation-flow crossing, mechanism realization, platform grammar, control relation, autonomy-like operation claim, `C.30.STRAT` source-label case, or open-architecture claim.
4. State the boundary and the declared interface specification or explicit interface-specification gap.
5. State the admissibility conditions, substitutability policy, and change policy, or mark any of those fields not established by the repair.
6. State the subject pattern for any non-module claim being made: `C.30`, `C.30.ASV`, `A.6.F`, `A.15`, `A.2`, `E.18`, `C.30.TFS-REL`, `C.31`, `C.31.RSA`, `C.16`, `A.10`, `B.3`, `A.20`, `A.21`, `C.28`, `E.20`, `G.5`, or `C.11`.
7. Stop when the claim, direct-relation disposition, and next use are explicit. Do not open A.6.RCD or A.6.REL unless a named receiving use genuinely needs a reusable direct relation or distinguishable obtaining occurrence.

### A.6.M:4.5 - Worked slices {#worked-slices}

**Ports line up.**

```text
Phrase:
  "The ports line up, so the modules are compatible."

ModuleRelationRepairNote:
  wholeHolonRef: VehicleControlSystem
  candidateModuleHolonRef: BrakeControllerPackage
  effectiveReferenceScheme: VehicleControlInterfaceScheme-2026Q2
  claimScope: BrakeControllerReleaseUse-2026Q2
  directModuleRelationDisposition: noDirectRelationClaimed
  boundaryRef: BrakeControlBoundary
  interfaceSpecificationGap: endpoint names are present, but protocol and semantic conditions are still missing
  admissibilityConditions: not yet declared
  substitutabilityPolicyRef: missing
  changePolicyRef: missing
  claimBoundary: interface-spec repair; no evidence or gate claim yet
  notAModuleBecause: port labels alone do not establish implemented interface compatibility
  governedNonModuleClaimPatternRefs: A.6.5 for endpoint slots; A.6.B only if L, A, D, or E boundary-package statement classification is current; A.6.M only if a module-interface or substitution claim remains
  stopCondition: endpoint slots and missing interface-spec fields are visible
```

**Open platform claim.**

```text
Phrase:
  "This is an open platform."

OpenArchitectureClaim:
  architectureClaimRef:
  platformGrammarRef:
  interfaceSpecificationRefs:
  variabilitySlotRefs:
  substitutabilityPolicyRef:
  changePolicyRef:
  conformanceExpectationRefs:
  evidenceOrSourceRelianceRefs?:
  nonAdmissibleUse:
    "open" does not by itself prove substitutability, interoperability,
    assurance, procurement suitability, or architecture quality
```

The first slice repairs the claim without requiring measurement. The second slice applies MOSA-like conformance expectations and substitution policy only for the conformance or substitution claim being made.

Supplier-diversity, procurement suitability, use-context compatibility, business constraint, policy authorization, and provider-selection claims are not module-interface fields. If those claims are being made, A.6.M names only the module-interface slice; non-module selection, procurement, work, role, evidence, assurance, gate, release, and mechanism claims are governed by the patterns named in `A.6.M:12`.

**Team boundary claim.**
```text
Phrase:
  "The team communication boundary matches the module boundary."

ModuleRelationRepairNote:
  wholeHolonRef: PaymentsPlatform
  candidateModuleHolonRef: SettlementService
  effectiveReferenceScheme: PaymentsPlatformInterfaceScheme-2026Q2
  claimScope: SettlementServiceProductLineUse-2026Q2
  directModuleRelationDisposition: noDirectRelationClaimed; team/module correspondence remains diagnostic
  boundaryRef: SettlementServiceBoundary
  interfaceSpecificationGap: the service API exists, but semantic versioning, data schema, and semantic conditions are incomplete
  admissibilityConditions: admitted team-delivery and on-call responsibility predicates obtain for their actual Systems, scopes, and intervals; otherwise record the exact missing governor; substitutability not established
  substitutabilityPolicyRef: missing
  changePolicyRef: missing
  claimBoundary: exact system-role assignment, direct responsibility relation, Work, and procedural correspondence first; module-interface relation only after boundary and interface specification are declared
  notAModuleBecause: team communication boundary and an independently obtaining delivery-responsibility relation do not by themselves establish module interface, substitutability, or compatibility
  governedNonModuleClaimPatternRefs: A.15 and A.2 for team and work claims; C.29 if the team-to-module correspondence is claimed as homomorphism-like or almost-same structure; A.6.M only for the declared module-interface relation
  stopCondition: the correspondence is usable as an architecture diagnostic, not as proof
```

The third slice uses Conway-like mirroring as a diagnostic prompt. It does not make organization structure, communication relations, a system-role assignment, or delivery responsibility into module-interface structure by identity. The responsibility claim remains valid only through its own admitted direct predicate or returns the exact missing governor.

Proxy-cost replay: if a repair proposes more modules, more open interfaces, or more parallel transformation-flow paths, name what may get worse before claiming improvement. Synchronization work, communication overhead, conformance work, shared-resource pressure, hidden exception cost, or cross-boundary change cost can become the claim being made. A.6.M repairs only the module-interface relation; speedup, bottleneck, modularity, measurement, work, and quality tradeoffs are governed by `C.29`, `E.18`, `C.31`, `C.16`, `A.15`, or the related subject pattern named by value when that related claim is being made.

### A.6.M:4.6 - Lowering and Reopen Conditions {#lowering-and-reopen-conditions}

Lower an A.6.M repair to reduced-use cue, quote-only wording, blocked use, or incomplete rewrite when the module-interface relation, interface specification, admissibility conditions, substitutability policy, or change policy cannot be stated by value.

Reopen the repair when any of these change: the whole holon, candidate module holon, boundary, interface specification, explicit interface gap, substitutability policy, change policy, platform grammar, conformance expectation, relied-on evidence relation, relied-on source relation, source-label recovery from `C.30.STRAT`, team-boundary correspondence, work correspondence, or the subject pattern for a related claim being made.

If the reopened material is no longer a module-interface relation, A.6.M keeps only the previous repair as source context and the claim being made is governed by the pattern named in `A.6.M:12`.

## A.6.M:7 - Conformance Checklist {#conformance-checklist}

| ID | Check |
| --- | --- |
| `CC-A6M-1` | @fact:CC-A6M-1 The text names the whole holon, candidate module holon, effective reference scheme, claim coverage when it matters, and exact module-interface viewpoint episteme when used, or explicitly stops at ordinary non-claim-bearing wording. No context suffix or optional model-use structure supplies those objects. @status:spec/done |
| `CC-A6M-2` | @fact:CC-A6M-2 The repair states whether the phrase is a module relation, component relation, function allocation, procedural or work-package relation, exact system-role-assignment occurrence, direct responsibility relation, deployment or placement structure, interface specification, signature, port or endpoint, transformation-flow crossing, mechanism realization, platform grammar, control relation, autonomy-like operation claim, `C.30.STRAT` source-label case, or open-architecture claim. @status:spec/done |
| `CC-A6M-3` | @fact:CC-A6M-3 No root kind is created for module, interface, platform, or open architecture, and `ModuleInterfaceClaim` is not treated as an independently admitted direct relation. The three direct-relation dispositions remain distinct. A needed reusable relation requires its defining rule and `A.6.RCD`; occurrence identity uses `A.6.REL` only after that relation is admitted and obtains. @status:spec/done |
| `CC-A6M-4` | @fact:CC-A6M-4 The independently identified `InterfaceSpecification` episteme, its exact C.2.1 identity, and an `interfaceSpecificationRef` that resolves it are recoverable when interface compatibility, substitutability, or conformance is claimed. A missing specification remains an explicit gap. @status:spec/done |
| `CC-A6M-5` | @fact:CC-A6M-5 Substitution or change policy is declared when replaceability, alternate supplier, upgrade, or platform extension is being claimed. Substitutability not established by the repair is marked as not established, not implied by wording. @status:spec/done |
| `CC-A6M-6` | @fact:CC-A6M-6 Function, transformation-flow, control, work, evidence, assurance, gate, decision, causal, and mechanism claims use their subject patterns. @status:spec/done |
| `CC-A6M-7` | @fact:CC-A6M-7 A failed check gives a repair action or subject-pattern application, not only a rejection. @status:spec/done |
| `CC-A6M-8` | @fact:CC-A6M-8 A current `G.2` source row for MOSA, open systems, platform practice, Conway correspondence, team-boundary correspondence, or Amdahl-style decomposition limits appears before guidance from that source is used for practitioner-facing claims being made. @status:spec/done |
| `CC-A6M-9` | @fact:CC-A6M-9 RFC keywords are used only for pattern users, records, claims, conformance items, or publication records, evidence records, or assurance records. Modeled modules and interfaces are not written as agents with duties. @status:spec/done |
| `CC-A6M-10` | @fact:CC-A6M-10 Lower or reopen the repair when whole holon, module holon, boundary, interface specification, interface gap, substitutability policy, change policy, platform grammar, conformance expectation, relied-on evidence relation, relied-on source relation, source-label recovery, team-to-work correspondence, or neighboring subject pattern changes. @status:spec/done |

## A.6.M:9 - Consequences {#consequences}

Benefits:

- Module and interface talk becomes usable without minting false root kinds.
- Practitioners get a cheap relation repair before measurement or evidence work.
- MOSA and open-system claims become precise enough to make real substitution and change reasoning admissible.
- Functional, flow, control, mechanism, work, evidence, assurance, gate, decision, and causal claims stay with their subject patterns.

Costs:

- Ordinary architecture prose loses the convenience of treating boxes, ports, interfaces, and modules as one kind.
- Interface claims sometimes require additional records before substitutability can be relied on.
- "Open architecture" becomes harder to claim because interface publication alone is not enough.

## A.6.M:12 - Relations {#relations}

| Pattern | Relation |
| --- | --- |
| `A.6.P` | A.6.M is an RPR specialization for module-interface claim and interface-specification language; its record forms do not create a direct relation occurrence. |
| `A.6.RSIR` | Bare interface-like wording is recovered before A.6.M is applied; A.6.M governs only recovered module-interface claim content, interface specification, platform grammar, substitutability policy, change policy, or open-architecture slice. |
| `A.6.RCD` and `A.6.REL` | A needed reusable direct module relation requires its subject pattern and A.6.RCD for participants, obtaining, applicability, recurrence, and identity. A.6.REL applies only after the direct relation is admitted and a later use must distinguish obtaining occurrences. |
| `C.2.1`, `A.2.6`, and `A.22` | Govern the `ModuleInterfaceClaim` episteme, the separate `InterfaceSpecification` episteme, effective reference scheme, ClaimScope, and any independently selected dependency or model-use structure. None creates a module relation. |
| `C.30.STRAT` | Recovers stratification and architecture-operation source labels before A.6.M governs only recovered module-interface relation cases. |
| `E.16` | Governs autonomy-budget, autonomous operation, independent acting, unsupervised decision or action, and freedom-of-action claims when those description or view uses are being made; A.6.M keeps only the module-interface relation, boundary, interface specification, and substitution or change-policy slice. |
| `A.14` | Component and part-whole wording uses A.14 first unless a module-interface relation is being claimed. |
| `A.6.0` and `A.6.5` | Signatures, slots, ports, endpoints, and field structure remain governed by signature and slot discipline. |
| `A.6.B`, `A.6.C`, and `A.6.P:4.11a` | Boundary, interface-specification, API, protocol, service, promise, and duty wording uses A.6.M only when the claim is module-interface relation, interface specification, substitutability, change policy, platform grammar, or open-architecture module-interface claim. |
| `C.30` and `C.30.ASV` | Architecture claims and module-interface structural views stay architecture-governed. |
| `C.33`, `C.34`, and `C.35` | Use these only when a module carrier, interface carrier, view, source label, generated map, or discovered structure needs architecture-specific captured-structure adequacy, lost-structure adequacy, preservation adequacy, or generated-carrier admission support. Use A.6.M for module-interface relation, interface specification, substitutability, change-policy, and platform-grammar claims. |
| `A.6.F` | Function and functional wording stays distinct from module allocation. |
| `A.15` and `A.2` | Method, WorkPlan, performed Work, exact system-role-kind and assignment claims, team-boundary wording, and delivery-unit wording keep their own defining or constraining patterns. Responsibility claims use an admitted direct domain predicate or the exact A.6.RCD missing-governor result; `VP.AllocationResponsibility` is only a recognition cue. Use A.6.M only for a recovered module-interface relation or correspondence. |
| `E.18` and `C.30.TFS-REL` | E.18 transformation-flow relations, path slices, crossings, and flow valuations are not interface specifications. |
| `C.31` | Modularity and reusable-structure characteristics are governed by C.31 after relation repair when characteristic or measurement use is being made. |
| `C.31.RSA` | Reusable-structure accounting is governed by C.31.RSA when reusable loci, bespoke residue, or report-only share claims are being made. |
| `C.16` | Measurement, score, scale, unit, comparability, and evidence-stub admissibility remain C.16-governed. |
| `A.10`, `B.3`, `A.20`, `A.21`, `C.28`, `E.20`, `G.5`, `C.11` | Evidence, assurance, gates, causal use, mechanism suites, set-return selection, and local decisions use their subject patterns; they are not A.6.M claims. |


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/A-6-P#root, spec://ai.lev/fpf-spec/contract/A-6-5#root, spec://ai.lev/fpf-spec/contract/A-6-B#root, spec://ai.lev/fpf-spec/contract/C-30#root, spec://ai.lev/fpf-spec/contract/C-30-ASV#root, spec://ai.lev/fpf-spec/contract/A-6-F#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/C-31#root, spec://ai.lev/fpf-spec/contract/C-31-RSA#root, spec://ai.lev/fpf-spec/contract/E-18#root, spec://ai.lev/fpf-spec/contract/C-30-TFS-REL#root, spec://ai.lev/fpf-spec/contract/A-10#root, spec://ai.lev/fpf-spec/contract/B-3#root, spec://ai.lev/fpf-spec/contract/A-20#root, spec://ai.lev/fpf-spec/contract/A-21#root, spec://ai.lev/fpf-spec/contract/C-28#root, spec://ai.lev/fpf-spec/contract/E-20#root, spec://ai.lev/fpf-spec/contract/G-5#root, spec://ai.lev/fpf-spec/contract/C-11#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-3-4-P#root, spec://ai.lev/fpf-spec/contract/A-6-F#root, spec://ai.lev/fpf-spec/contract/A-6-RSIR#root, spec://ai.lev/fpf-spec/contract/B-1-2#root, spec://ai.lev/fpf-spec/contract/B-2-4#root, spec://ai.lev/fpf-spec/contract/C-30-AD#root, spec://ai.lev/fpf-spec/contract/C-30-AD-BA#root, spec://ai.lev/fpf-spec/contract/C-30-ASV#root, spec://ai.lev/fpf-spec/contract/C-30-STRAT#root, spec://ai.lev/fpf-spec/contract/C-31#root, spec://ai.lev/fpf-spec/contract/C-31-ASAP#root, spec://ai.lev/fpf-spec/contract/C-31-RSA#root, spec://ai.lev/fpf-spec/contract/C-32#root, spec://ai.lev/fpf-spec/contract/C-32-FAIL#root, spec://ai.lev/fpf-spec/contract/C-33#root, spec://ai.lev/fpf-spec/contract/C-34#root, spec://ai.lev/fpf-spec/contract/C-35#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/A-6-M
