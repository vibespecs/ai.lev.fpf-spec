# C.32.PAD - Project Architecture Decision After Candidate Synthesis {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Architecture decision pattern under C.32
> **Status:** Stable
> **Normativity:** Normative unless explicitly marked informative

## C.32.PAD:1 - Problem frame {#problem-frame}

Use this pattern when a project has synthesized candidate architecture configurations and must make the project architecture decision that will guide later design, implementation, construction, operation, governance, or change work.

Primary working reader: an architect or architecture-responsible practitioner who has enough candidate synthesis, comparison input, and architecture-characteristic pressure to decide what architecture will be pursued now.

Typical entry phrases:

```text
"We have three candidate architecture configurations; which one becomes the project decision?"
"The candidate improves maintainability but worsens evidence reuse; what is the accepted trade-off?"
"Developers need to know which architectural style, method, or pattern use is now required."
"The architecture decision must say which structure is fixed by this decision and which refinement remains open."
"The ADR cannot be written yet because the decision relation is not clear."
```

**First-minute use slice.** A product-family architect has a C.32 candidate palette with three module, placement, and evidence-structure variants. C.32.ACS names maintainability, substitutability, and evidence reuse as optimization indicators, and C.32.ACE has evaluated the candidates under one parity frame. Using C.32.PAD, the architect records the exact composite project work, selected configuration, affected selected structures, accepted loss in evidence reuse, method-use instruction for product teams, structures fixed by the decision, refinement left open, source-return condition, and reopen trigger. The result is not an ADR file yet; it is the architecture decision relation concerning that project work which an ADR or another publication form can describe.

The primary `EntityOfConcern` is `ArchitectureDecisionRelation@Project`: an architecture decision relation over one bounded architecture question with one exact composite project `U.Work` as a participant. It links that work, the decision subject, candidate basis, selected architecture option, affected structures, architecture characteristics, rationale, accepted losses, consequences, method and work expectations, publication projection, evidence or eval exits, and reopen conditions.

`ArchitectureDecisionRelation@Project` is not a new `U.*` kind. `@Project` is a compatibility and retrieval cue, not the source of project identity or scope. The relation is project-local only when `projectWorkOccurrenceRef` identifies the exact composite `U.Work` that participates in it. When another slot becomes load-bearing as an FPF object, recover the subject pattern for that object.

When this decision designates a **project system-of-interest**, `projectSystemOfInterestRef?` names only an independently admitted existing `U.System`. Before identity inception, keep the intended referent in `intendedProjectSystemClaimRef?` as `U.WorkPlan`, decision, system description, or other claim content. A local kind is named separately in `systemOfInterestKindRef?`, while `systemOfInterestClassificationRef?` cites an independently obtaining classification judgment; neither entails an assignment. A current assignment uses separate species and occurrence refs, and the occurrence's holder is that System. Route any source phrase such as `SystemOfInterestRole` through `E.10.ROLE` before filling these fields. A taxonomy or scheme is not assignment content. Designation, kind, classification, assignment, Work, change, use facts, and the decision remain distinct. The decision neither establishes a compound project-selection truth nor repairs its missing constructor; when that one truth is required, retain every direct fact and record the A.15.6 result `missing-substrate[project-selection-conjunction]`.

When the decision uses a transformation-flow network, `transformationFlowStructureNetworkRef?` names only an independently selected E.18.NET `TransformationFlowStructureNetwork@Context <: U.Structure`; `projectNetworkSelectionResultRef?` may cite the separate C.2.1 judgment about why that network answers the project question, and `architectureTransformationFlowStructureRelationRef?` cites C.30.TFS-REL when architecture use is current. A network record, a C.32.CONWAY frame or exact pair row, and this decision create no network member, cross-flow occurrence, architecture-influence occurrence, architecture relation, or other world-side fact.

What goes wrong if C.32.PAD is missed: a team writes an architecture record, diagram, shortlist, ranking, or local choice without a recoverable architecture decision relation to exact project work. Later workers cannot tell which architecture configuration is selected, which structures are affected, which method they must use, which losses were accepted, or when the decision must be reopened.

What C.32.PAD buys in practice: practitioners performing the project work can turn a candidate palette into one governed decision relation that is strong enough to guide work, publish an ADR-like record, support review, and reopen under architecture evolution.

Ordinary working move: recover the live decision question, cite the candidate basis, select the architecture option or bounded exception, record the trade-off over declared architecture characteristics, then bind the decision to method-use expectations, work split, source-return, and reopen conditions.

Adoption test: after using C.32.PAD, another practitioner can answer: what architecture option was selected, from which candidate basis, for which affected structures, under which architecture-characteristic trade-off, with which method and work consequences, and under which reopen condition.

Not this pattern when the current work is candidate synthesis, architecture-description adequacy, ADR publication projection, adequacy evaluation, evidence, assurance, gate passage, local choice, or performed work. Use the pattern for the next question named in `Relations` for those claims.

The first useful output is `ArchitectureDecisionRelation@Project`:

```text
ArchitectureDecisionRelation@Project:
  decisionId:
  projectWorkOccurrenceRef: U.EntityRef constrained to exact composite U.Work
  projectSystemOfInterestRef?: U.EntityRef constrained to one independently admitted existing U.System
  intendedProjectSystemClaimRef?: U.WorkPlan, decision, system-description, or other claim episteme ref before identity inception
  systemOfInterestKindRef?: U.KindRef resolving to one exact local system-role kind
  systemOfInterestClassificationRef?: U.RelationRef resolving to the exact classification judgment for projectSystemOfInterestRef under systemOfInterestKindRef
  systemOfInterestAssignmentSpeciesRef?: U.RelationKindRef constrained under U.SystemRoleAssignment
  systemOfInterestAssignmentOccurrenceRef?: U.RelationRef constrained to an obtaining occurrence of systemOfInterestAssignmentSpeciesRef, with actual participants, applicability, extent, and projectSystemOfInterestRef as holder recoverable
  decisionSubjectRef:
  describedHolonRef:
  decisionQuestion:
  intendedDecisionUse:
  claimScopeRef: U.ClaimScope
  decisionWindowRef:
  candidateBasisRefs:
  comparisonOrSelectionRefs?
  structuralInformationLensUseRefs?
  holonTransitionOrBOSCTriggerRefs?
  architectureInfluenceCorrespondenceRef?: C.32.CONWAY frame or exact pair-row ref
  transformationFlowStructureNetworkRef?: exact independently selected E.18.NET TransformationFlowStructureNetwork@Context ref
  projectNetworkSelectionResultRef?: exact C.2.1 result episteme whose EntityOfConcern is transformationFlowStructureNetworkRef
  architectureTransformationFlowStructureRelationRef?: exact C.30.TFS-REL use/trace ref when architecture uses that network
  selectedArchitectureOptionRefs:
  selectedStructureEffects:
    - structureKindRef:
      selectedStructureRef:
      decisionEffect:
      relationFunctionClaimRef:
  architectureCharacteristicTradeoffs:
    - architectureCharacteristicRef:
      criteriaRowRef?
      expectedGain:
      acceptedLoss:
      evalResultRef?
      guardrailRef?
  rationaleRefs:
  rejectedOptionRefs:
  consequenceRows:
  architectureDescriptionRefs:
  methodUseInstructions:
    - methodDescriptionRefOrPatternRef:
      expectedStructureEffect:
      intendedPerformerSystemRef?: U.EntityRef constrained to U.System
      intendedPerformerKindRef?: U.KindRef
      intendedPerformerClassificationRef?: U.RelationRef resolving to an exact classification judgment
      currentPerformerAssignmentSpeciesRef?: U.RelationKindRef constrained under U.SystemRoleAssignment
      currentPerformerAssignmentOccurrenceRef?: U.RelationRef constrained to an obtaining occurrence of currentPerformerAssignmentSpeciesRef, with actual participants, applicability, extent, and intendedPerformerSystemRef as holder recoverable
      intendedAssignmentRequirementRef?: plan, policy, or decision-content ref stating a prospective assignment requirement; does not assert an assignment, commitment, or permission occurrence
      actualImplementationWorkRef?: U.EntityRef constrained to U.Work
      actualImplementationWorkAttributionRef?: U.RelationRef constrained to one obtaining F.6 performedUnderAssignment relation, only when the instruction expressly represents attribution
      responsibilityRelationRef?: U.RelationRef resolving to an independently obtaining admitted domain relation
      responsibilityMissingGovernor?: exact A.6.RCD result when responsibility is required but no predicate is admitted
      authorityRelationRef?: U.RelationRef resolving to an independently obtaining admitted domain relation
      authorityMissingGovernor?: exact A.6.RCD result when authority is required but no predicate is admitted
      permissionRelationRef?: U.RelationRef resolving to an independently obtaining admitted domain relation
      permissionMissingGovernor?: exact A.6.RCD result when permission is required but no predicate is admitted
      commitmentRelationRef?: U.RelationRef resolving to an independently obtaining admitted domain relation
      commitmentMissingGovernor?: exact A.6.RCD result when commitment is required but no predicate is admitted
      workBoundaryRef:
      readinessOrGateExitRef?
  architectDeveloperSplit:
    decisionFixedStructureRefs:
    openRefinementScopeRefs:
    sourceReturnCondition:
  publicationProjectionRef?
  evidenceOrAssuranceExitRefs?
  governanceExitRefs?
  reopenConditions:
  supersedesDecisionRefs?
  status:
```

The filled `ArchitectureDecisionRelation@Project` is the decision result. Its selected option, affected structures, criteria and trade-offs, scope, window, consequences, and status make that result recoverable; a second generic result or context record would only duplicate it.

The field names in this first-output form are publication-friendly filled-reference fields. Durable relation positions must be expressible through `A.6.5` SlotSpecs: each position has a local `SlotKind`, an admitted `ValueKind`, and a by-value or concrete `RefKind` filling mode. A field name such as `decisionSubjectRef` is not a SlotKind, not a U-kind, and not an ADR heading; it is the filled-reference field by which this relation record points to the value governed by the slot-bearing relation.

When an instruction cites actual implementation Work, recover each exact actual performer through A.13 and let `actualImplementationWorkRef` name the `U.Work` occurrence independently admitted through A.15.1. Assignment species and occurrence fields remain optional neighboring claims. Add `actualImplementationWorkAttributionRef` only when the instruction or receiving use expressly represents precise assignment-bound attribution through the same obtaining A.13 assignment; missing or failed F.6 leaves the Work ref intact. The decision record creates none of these facts.

## C.32.PAD:2 - Problem {#problem}


Architecture synthesis produces candidates; the Systems performing project Work still need a decision, while any local system-role kind, direct assignment species, authority, or responsibility claim remains a separate fact established through its own pattern. The decision is not the candidate palette, the declared selected-set result, its publication, the architecture description, or the ADR file. It is the architecture decision relation that identifies the composite project Work, says which architecture option is now pursued for it, and records what follows from that selection.

The problem is difficult because architecture decisions sit between structures and Methods. C.30 keeps an obtaining `ArchitectureRelation` with its holon and selected `U.Structure` separate from an `ArchitectureClaim` carrying candidate, required, desired, or expected content. A project architecture decision can tell intended developer Systems which Method description, architectural style, pattern use, or work boundary to follow so that later work aims to produce or preserve the intended structures. For example, "use the client-server style here" is a Method-use instruction whose intended result is a module and interaction structure of the described System. The decision relation must keep actual or modal structure content, intended Systems, local kinds, separate System-classification judgments, assignment requirements and current assignment occurrences, plans and commitments, permissions and authority, and actual Work as separate branches. Route unresolved role wording through `E.10.ROLE`. When C.32.CONWAY supplies an influence-source architecture or selected structure, that source remains non-agentive and does not become the performer.

The problem is also multilevel. The architecture decision may fix selected structures at one holon level while leaving lower-level refinement open. It must therefore say which structure is fixed, which refinement remains open, which source detail must remain recoverable, and which result can reopen the decision. If that boundary is missing, the decision becomes either empty advice or uncontrolled micro-management.

Finally, architecture decisions are evolutionary. They are made under current candidate knowledge, current characteristic criteria, current eval readings, and current organization or tool constraints. They should be explicit enough for present work and cheap enough to supersede when a better candidate, changed characteristic pressure, or architecture-influence/transformed-side fit changes.

C.32.PAD solves the post-synthesis decision problem by making the decision relation explicit before any ADR-like publication projection is written.

## C.32.PAD:3 - Forces {#forces}

| Force | Tension |
|---|---|
| Candidate plurality | Several candidate configurations can be valid under different trade-offs, while project work needs one current direction or a bounded exception. |
| Trade-off visibility | Architecture characteristics compete; a decision that hides accepted losses cannot be responsibly executed or reopened. |
| Structure and method coupling | The decision must govern actual or modal structure content for the described or transformed-side holon and may also prescribe developer methods intended to produce or preserve those structures. |
| Work split | Structures fixed by the decision and refinement left open must be separated without severing source return. |
| Evolution | A decision must close enough work for now while staying reopenable when context, eval readings, or candidates change. |
| Publication pressure | Teams often want an ADR file before the decision relation is recoverable. |

## C.32.PAD:4 - Solution {#solution}

Create `ArchitectureDecisionRelation@Project` before writing an ADR-like publication record. Treat it as the architecture decision relation that includes the exact composite project `U.Work` and binds it to the candidate basis, selected architecture option, affected structures, architecture-characteristic trade-offs, rationale, consequences, method expectations, work split, and reopen conditions.

Work in this order:

1. Name the composite project `U.Work` participant and the decision subject: described holon, decision question, intended use, ClaimScope, decision window, and status. If the decision designates a project system-of-interest, cite the existing `U.System` or the pre-inception intended-system claim. Add a local kind only when it is current, add a separate System-classification judgment only when that judgment independently obtains, and add an assignment only through its separately declared A.2.1 species and obtaining occurrence whose holder is that System. Route `SystemOfInterestRole` source wording through `E.10.ROLE`; establish every Work, change, and use fact through its own predicate and pattern. A decision designation proves no compound project-selection truth; return `missing-substrate[project-selection-conjunction]` when that stronger truth is required.
2. Cite the candidate basis. Use `C.32` for the candidate palette, `C.32.MLAO` for residual-reducing multilevel candidate frames, `C.32.CONWAY` when an influence-source architecture and transformed-side architecture content shaped the candidate, and `C.32.FAIL` for repaired candidate errors. Cite a C.32.CONWAY synthesis frame while either side is modal or the direct influence relation is unresolved; cite an exact pair row only for its already obtaining direct occurrence and two obtaining C.30 architecture-relation participants.
3. Cite comparison or selection input only when it exists. Use `A.19.CPM` for explicit comparison, `A.19.SelectorMechanism` for set-returning selection, `G.5` for selected-set result declaration, and `C.11` for local choice. For publication, use `E.17` for a source-backed face and source return and `E.24.PUB` for the publication occurrence and audience availability.
4. State the selected architecture option or bounded exception. Name the affected selected structures and the subject pattern for each structure claim.
5. Record the architecture-characteristic trade-off. Use criteria rows from `C.32.ACS`, eval results from `C.32.ACE`, measurement support from `C.16`, Q-Bundles from `C.25`, modularity or scale support from `C.31`, and `C.29` structural-information lens uses for compressed recoverable structure, accepted description loss, hidden dependency, and source-return. None of those lenses, measures, or bundles decides the architecture by itself.
6. Record rationale, rejected options, accepted losses, and consequences. A rejected option can remain useful as a stepping stone or archive item; do not turn it into a failure unless the receiving failure pattern is triggered.
7. Bind the decision to architecture descriptions. Use `C.30.AD` for architecture-description adequacy and `C.30.ASV` for selected-structure view adequacy. A diagram, model, file, or view can describe the decision basis; it does not become the decision relation.
8. Bind the decision to method-use instructions when the architect needs developers to use a method, pattern, style, toolchain step, or work practice so the described or transformed-side holon is intended to gain or preserve the named structure. Use `A.15`, `A.15.1`, `A.15.2`, `A.15.5`, `A.6.M`, `E.8`, `E.11.PUR`, and `C.24` according to the live claim.
9. State the architecture-to-refinement boundary. Name selected structures fixed by the decision, refinement scopes left open, source-return conditions, readiness exits, and patterns for any later governance question. When the boundary depends on holon level, changed whole, or BOSC-triggered pressure, fill `holonTransitionOrBOSCTriggerRefs?` through `B.2.P` claim-kind recovery or `B.2` whole reidentification instead of leaving a generic level note.
10. Choose a publication projection only after the decision relation is clear. Use `C.32.ADR` for ADR-like projection, `E.17` for a source-backed publication face and source return, and `E.24.PUB` for the publication occurrence and audience availability.
11. Add evidence, assurance, gate, and governance exits only when those claims are being made. Use `A.10`, `B.3`, `A.21`, and the local governance pattern rather than adding those statuses to the decision relation by name.
12. Write reopen and supersession conditions. Reopen when the candidate basis changes, a protected architecture characteristic crosses its guardrail, an independently typed influence-source structure or arrangement no longer fits the transformed-side actual or modal architecture content, a stronger source changes the accepted loss, or the decision's method-use instruction proves unusable.

If one project question uses an E.18.NET network, first preserve that network's independent A.22/E.18.NET selection. A persistent project-network judgment stays in its C.2.1 result episteme under A.15.6, and architecture use docks through C.30.TFS-REL. A C.32.CONWAY exact pair row may be cited in `architectureCorrespondenceRowRefs[]` of a network record, but that citation is only a qualified reading: it adds no network member or cross-flow occurrence, and PAD repeats none of the network's member, relation, constraint, endpoint, or use-frame fields.

### C.32.PAD:4.1 - Decision readiness {#decision-readiness}

A C.32.PAD decision is ready to draft when the current decision relation identifies the composite project `U.Work` participant and can cite at least one candidate basis, one affected selected structure, one architecture-characteristic trade-off or declared reason for no live trade-off, one expected work consequence, one reopen condition, and any triggered `holonTransitionOrBOSCTriggerRefs?` or `structuralInformationLensUseRefs?` needed to preserve source return. When system-of-interest local-kind, separate System-classification, assignment, architecture-influence, or network fields are present, the applicable A.15.6, A.2 and A.2.1, C.32.CONWAY, E.18.NET, and C.30.TFS-REL preconditions must already be satisfied or the reference remains absent.

If the candidate basis is absent, require `C.32`. If architecture-characteristic rows are absent, require `C.32.ACS` or `C.25`. If the decision only says "the metric is best", require `C.32.ACE`, `C.16`, or `A.19.CPM` before deciding. If the intended work method is not recoverable, require `A.15`. If an existing system, role assignment, project-network judgment, network selection, architecture use, or influence pair is unresolved, require its subject pattern and keep only the truthful designation, modal claim, candidate frame, or explicit stop in PAD.

### C.32.PAD:4.2 - Constructive architecture decision path {#constructive-architecture-decision-path}

Some architecture decisions are constructive: they prescribe Methods that intended developer Systems are expected to use so that later work aims to produce or preserve intended structures. A decision may name intended Systems, local-kind requirements, separate classification requirements, assignment requirements, plans, commitments, permissions, or authority before any assignment or Work obtains. Admit that path only when the decision keeps those claims separate and names:

- the obtaining architecture relation and selected structure to be preserved, or the exact modal `ArchitectureClaim` stating the intended production or preservation effect;
- the method description, architectural style, pattern use, or work practice to be used;
- the intended System when known; an optional local kind and an independently optional System-classification judgment; any current assignment through separate species and obtaining-occurrence refs whose holder is that System; and any merely intended assignment as plan, policy, or decision content rather than an occurrence;
- any responsibility or authority relation only when its admitted direct predicate, actual participants, applicability, and identity obtain; otherwise record the exact A.6.RCD missing governor instead of calling the system-role kind or assignment responsible;
- the expected structure effect on the described or transformed-side holon, kept modal until its direct C.30 architecture predicate obtains;
- the work-planning boundary and readiness or gate exit;
- the source-return condition and reopen trigger.

These requirements connect the architecture decision to work while keeping its expected structure effect distinct from any independently established actual effect.

### C.32.PAD:4.3 - Minimum sufficient relation and slot-change impact {#minimum-sufficient-relation-and-slot-change-impact}

A small complete PAD instance can be this short:

```text
ArchitectureDecisionRelation@OrderFlow:
  decisionId: OrderFlowArchitectureDecision-2026Q3
  projectWorkOccurrenceRef: ProductFamilyQ3OrderArchitectureWork, exact admitted composite U.Work
  decisionSubjectRef: order-integration architecture for product-family Q3
  describedHolonRef: product-family order-flow system
  decisionQuestion: which candidate architecture should guide Q3 order-flow implementation?
  intendedDecisionUse: direct the Q3 implementation work while preserving the stated refinement boundary
  claimScopeRef: order-flow architecture for ProductFamilyQ3OrderArchitectureWork
  decisionWindowRef: accepted for Q3 implementation; reopen on a listed trigger or superseding decision
  candidateBasisRefs: [C32CandidatePalette:order-flow-2026-06]
  selectedArchitectureOptionRefs: [event-carried integration with payment exception]
  selectedStructureEffects:
    - structureKindRef: module structure
      selectedStructureRef: order events between service modules
      decisionEffect: preserve service substitutability, accept added event-schema governance
      relationFunctionClaimRef: C.30.ASV
  architectureCharacteristicTradeoffs:
    - architectureCharacteristicRef: substitutability
      criteriaRowRef: C.32.ACS order-flow substitutability criterion
      expectedGain: service replacement without order-flow rewrite
      acceptedLoss: additional schema-version coordination
      guardrailRef: version-skew eval band
  methodUseInstructions:
    - methodDescriptionRefOrPatternRef: event-schema change method
      expectedStructureEffect: compatible event schemas across service modules
      intendedPerformerSystemRef: the named service-team System intended by the project decision
      intendedPerformerKindRef: ServiceTeamDeveloperSystemRole
      intendedPerformerClassificationRef: the separate classification judgment, when it obtains
      intendedAssignmentRequirementRef: decision content requiring a suitable service-team assignment before implementation Work
      workBoundaryRef: schema refinement left open inside the event boundary fixed by the decision
  architectDeveloperSplit:
    decisionFixedStructureRefs: [event boundary, payment exception]
    openRefinementScopeRefs: [schema fields inside approved event boundary]
    sourceReturnCondition: return to PAD when refinement changes event boundary or version-skew band
  holonTransitionOrBOSCTriggerRefs?: [B.2.P: no new operational whole claimed for team-local schema refinement]
  structuralInformationLensUseRefs?: [C.29: event-flow view compresses deployment and rollout structure; source-return keeps model refs recoverable]
  publicationProjectionRef?: C.32.ADR:order-flow-adr
  reopenConditions: [payment latency guardrail crossed, schema-version coordination cost guardrail crossed]
  status: acceptedForDeveloperWork
```

When a filled field changes, repair the smallest declaration or claim record that carries the changed content:

| Changed filled field | Immediate repair locus |
|---|---|
| `candidateBasisRefs` or `selectedArchitectureOptionRefs` | Use `C.32`, `C.32.MLAO`, comparison or selection inputs, then update PAD before ADR projection. |
| `projectSystemOfInterestRef?`, `intendedProjectSystemClaimRef?`, `systemOfInterestKindRef?`, `systemOfInterestClassificationRef?`, `systemOfInterestAssignmentSpeciesRef?`, or `systemOfInterestAssignmentOccurrenceRef?` | Use A.15.6 for actual-versus-intended designation and the compound-selection stop, C.3/A.2 for the exact local kind and its separate classification judgment, and A.2.1 for the directly declared assignment species and its separately obtaining occurrence. Route unresolved role wording through `E.10.ROLE`. Keep every independently obtaining Work, change, and use fact; remove any reference the decision alone was being used to prove. |
| `architectureInfluenceCorrespondenceRef?` | Use C.32.CONWAY. Keep a frame for modal or unresolved sides and cite an exact pair row only for the already obtaining direct occurrence and its exact C.30 architecture-relation participants. |
| `transformationFlowStructureNetworkRef?`, `projectNetworkSelectionResultRef?`, or `architectureTransformationFlowStructureRelationRef?` | Use E.18.NET for exact network identity, A.15.6/C.2.1 for the project-question judgment, and C.30.TFS-REL for architecture use. Update or remove only the affected refs; do not copy or repair network members, relations, constraints, endpoints, or use frame inside PAD. |
| `selectedStructureEffects` | Repair the architecture claim or selected-structure view in `C.30`, `C.30.AD`, or `C.30.ASV`; then update PAD consequences. |
| `architectureCharacteristicTradeoffs` | Repair `C.32.ACS`, `C.32.ACE`, `C.25`, `C.16`, or comparison input before relying on the decision. |
| `methodUseInstructions` or `architectDeveloperSplit` | Repair Method, plan, intended-System, local-kind, separate System-classification, assignment, actual-Work, readiness, and work-boundary claims through their subject patterns. Route unresolved role wording through `E.10.ROLE`; use `A.15`, `E.8`, `E.11.PUR`, or `C.24` only for the claim that pattern defines, constrains, or tests. |
| `holonTransitionOrBOSCTriggerRefs?` | Use `B.2.P` for wording and claim-kind recovery; use `B.2` only when the decision depends on whole reidentification. |
| `structuralInformationLensUseRefs?` | Use `C.29` to state which structure is preserved, compressed, hidden, or recoverable; return to source when the accepted loss changes. |
| `publicationProjectionRef?` | Repair only the projection through `C.32.ADR`, the source-backed publication face and source return through `E.17`, and the publication occurrence and audience availability through `E.24.PUB`; do not rewrite the decision by template pressure. |
| `reopenConditions` or `supersedesDecisionRefs?` | Update PAD and the active ADR-like projection; old decisions remain historical unless a governed archival policy says otherwise. |

## C.32.PAD:7 - Conformance Checklist {#conformance-checklist}

| Requirement | Required result |
|---|---|
| `CC-PAD-1` | @fact:CC-PAD-1 The exact composite project `U.Work` participant, decision subject, described holon, decision question, intended decision use, ClaimScope, and decision window are explicit. @status:spec/done |
| `CC-PAD-2` | @fact:CC-PAD-2 The decision cites candidate basis from `C.32` or a named receiving candidate pattern, or states why no candidate-set question is live. @status:spec/done |
| `CC-PAD-3` | @fact:CC-PAD-3 The selected architecture option or bounded exception is named. @status:spec/done |
| `CC-PAD-4` | @fact:CC-PAD-4 Affected selected structures are named with subject pattern refs. @status:spec/done |
| `CC-PAD-5` | @fact:CC-PAD-5 Architecture-characteristic trade-offs, accepted losses, and guardrails are recorded. @status:spec/done |
| `CC-PAD-6` | @fact:CC-PAD-6 Architecture-description refs, method-use instructions, and performed-work boundaries remain distinct. @status:spec/done |
| `CC-PAD-7` | @fact:CC-PAD-7 The architect-developer split, source-return condition, and reopen conditions are recorded. @status:spec/done |
| `CC-PAD-8` | @fact:CC-PAD-8 Triggered holon-transition or BOSC boundary pressure cites `B.2.P` or `B.2`, and structural-information loss or compression cites `C.29`. @status:spec/done |
| `CC-PAD-9` | @fact:CC-PAD-9 ADR-like publication, evidence, assurance, gate, comparison, selection, selected-set result declaration, audience publication, local choice, and work claims exit to their patterns for the next questions. @status:spec/done |
| `CC-PAD-10` | @fact:CC-PAD-10 Any project system-of-interest ref denotes one independently admitted existing `U.System`; a pre-inception intended referent stays in claim content. `SystemOfInterestRole` wording is recovered through `E.10.ROLE`; any local kind, separate classification judgment, and separately obtaining A.2.1 assignment are cited independently. Decision designation, kind, classification, assignment, and direct facts neither entail one another nor establish the missing compound project-selection truth. @status:spec/done |
| `CC-PAD-11` | @fact:CC-PAD-11 Any network ref resolves to one independently selected E.18.NET structure, its project-question judgment stays in a separate C.2.1 episteme, and architecture use docks through C.30.TFS-REL. A PAD decision, network record, C.32.CONWAY frame, or exact pair row creates no member, cross-flow occurrence, influence occurrence, architecture relation, or actual structure effect. @status:spec/done |

## C.32.PAD:9 - Consequences {#consequences}

| Consequence | Benefit | Cost |
|---|---|---|
| The architecture decision relation to exact composite project work is explicit before publication. | ADRs, design memos, and governance files can describe a recoverable decision rather than inventing one. | The architect performs decision work before publication work. |
| Structure and method are coupled without collapsing. | Developers can see both intended architecture structures and required methods. | The decision record needs enough detail to avoid empty method instructions. |
| Trade-offs and accepted losses are recorded. | Later teams can reopen the decision under changed characteristics instead of guessing the original rationale. | Decisions may look less tidy because loss is visible. |
| Architect-developer split is stated. | Team refinement can proceed without losing source return. | Architecture governance must maintain split and reopen conditions. |

## C.32.PAD:12 - Relations {#relations}

- **Builds on:** `A.15.6`, `A.2`, `A.2.1`, `C.30`, `C.30.ASV`, `C.30.AD`, `C.30.TFS-REL`, `E.18.NET`, `C.32.P2S`, `C.32`, `C.32.MLAO`, `C.32.ACS`, `C.32.ACE`, `C.32.CONWAY`, `C.32.FAIL`, `C.25`, `C.16`, `C.29`, `C.31`, and `C.31.ASAP`.
- **Comparison and selection boundary:** Use `A.19.CPM` for comparison, `A.19.SelectorMechanism` for set-returning selection, `G.5` for selected-set result declaration, and `C.11` for local choice. When audience availability is current, use `E.17` for a source-backed publication face and return to source and `E.24.PUB` for the publication occurrence, form, carrier, audience, bounded use, and availability. PAD records the architecture decision relation with its exact composite project-work participant after those inputs are sufficient.
- **Description boundary:** `C.30.AD` and `C.30.ASV` govern architecture-description and selected-structure view adequacy. PAD may cite those descriptions but does not replace them.
- **Structural-information boundary:** Use `C.33` and `C.34` for captured structure, lost structure, and preservation adequacy used by the decision relation. Use `C.35` for the exact generated or discovered result, the obtaining or proposed organization, its next-use condition, and the limit or return. Resolve representation, publication-form, or carrier questions separately when the decision's use depends on them. Use PAD for the decision relation, rationale, consequences, accepted losses, Method consequences, Work consequences, source return, repair, and supersession claims.
- **Publication boundary:** Use `C.32.ADR` to project an `ArchitectureDecisionDescription@Project` into ADR-like form, `E.17` for a source-backed publication face and source return, and `E.24.PUB` for the publication occurrence and audience availability.
- **Adequacy boundary:** `C.32.ADA` evaluates a PAD decision relation, method docking, and publication projection for a declared use.
- **P2S docking:** P2S reaches PAD only when implementation commitment is live; PAD records the decision relation and returns reopen conditions to P2S when actual structures, eval results, or source-return change the architecture question.
- **Project system-of-interest boundary:** Use `A.15.6` for composite project Work, actual-versus-intended System designation, independent Work, change and use facts, project-network judgment, and `missing-substrate[project-selection-conjunction]`. `E.10.ROLE` recovers `SystemOfInterestRole` wording; use `A.2` and `A.2.1` separately for local kind, classification, and obtaining assignment. PAD cites those objects only when the architecture decision uses them and proves none of them.
- **Network and architecture-influence boundary:** use `E.18.NET` to identify the selected network, its members, obtaining cross-flow occurrences, constraints, endpoints, and use frame; `C.30.TFS-REL` defines architecture use; `C.32.CONWAY` is the pattern for the synthesis frame and exact qualified pair row. PAD cites the smallest exact refs and never turns a record or row citation into network membership, a direct relation occurrence, actor identity, performance, or actual structure effect.
- **Method and work boundary:** `A.15`, `A.15.1`, `A.15.2`, `A.15.5`, `E.8`, `E.11.PUR`, and `C.24` govern method descriptions, work plans, readiness, pattern-use recommendations, and agentic tool-use work.
- **Evidence, assurance, and gate boundary:** `A.10`, `B.3`, and `A.21` govern evidence relations, assurance calculus, and gate profiles when those claims are current.


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/C-32#root, spec://ai.lev/fpf-spec/contract/C-32-MLAO#root, spec://ai.lev/fpf-spec/contract/C-32-CONWAY#root, spec://ai.lev/fpf-spec/contract/C-32-FAIL#root, spec://ai.lev/fpf-spec/contract/A-19-CPM#root, spec://ai.lev/fpf-spec/contract/A-19-SelectorMechanism#root, spec://ai.lev/fpf-spec/contract/C-11#root, spec://ai.lev/fpf-spec/contract/G-5#root, spec://ai.lev/fpf-spec/contract/C-30#root, spec://ai.lev/fpf-spec/contract/C-30-AD#root, spec://ai.lev/fpf-spec/contract/C-30-ASV#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/C-32-ADR#root, spec://ai.lev/fpf-spec/contract/C-32-ADA#root, spec://ai.lev/fpf-spec/contract/C-32-ACS#root, spec://ai.lev/fpf-spec/contract/C-32-ACE#root, spec://ai.lev/fpf-spec/contract/C-16#root, spec://ai.lev/fpf-spec/contract/C-25#root, spec://ai.lev/fpf-spec/contract/C-29#root, spec://ai.lev/fpf-spec/contract/A-15#root, spec://ai.lev/fpf-spec/contract/E-8#root, spec://ai.lev/fpf-spec/contract/E-11-PUR#root, spec://ai.lev/fpf-spec/contract/E-17#root, spec://ai.lev/fpf-spec/contract/E-24-PUB#root, spec://ai.lev/fpf-spec/contract/A-10#root, spec://ai.lev/fpf-spec/contract/B-3#root, spec://ai.lev/fpf-spec/contract/A-21#root, spec://ai.lev/fpf-spec/contract/B-2#root, spec://ai.lev/fpf-spec/contract/B-2-P#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/B-1-2#root, spec://ai.lev/fpf-spec/contract/C-30#root, spec://ai.lev/fpf-spec/contract/C-30-ILC#root, spec://ai.lev/fpf-spec/contract/C-31-ASAP#root, spec://ai.lev/fpf-spec/contract/C-32#root, spec://ai.lev/fpf-spec/contract/C-32-ACE#root, spec://ai.lev/fpf-spec/contract/C-32-ACS#root, spec://ai.lev/fpf-spec/contract/C-32-ADA#root, spec://ai.lev/fpf-spec/contract/C-32-ADR#root, spec://ai.lev/fpf-spec/contract/C-32-CONWAY#root, spec://ai.lev/fpf-spec/contract/C-32-FAIL#root, spec://ai.lev/fpf-spec/contract/C-32-HCS#root, spec://ai.lev/fpf-spec/contract/C-32-MLAO#root, spec://ai.lev/fpf-spec/contract/C-33#root, spec://ai.lev/fpf-spec/contract/C-34#root, spec://ai.lev/fpf-spec/contract/C-35#root, spec://ai.lev/fpf-spec/contract/E-4-PFAD#root, spec://ai.lev/fpf-eng-oce/contract/OCE-4#root, spec://ai.lev/fpf-eng-oce/contract/OCE-7#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/C-32-PAD
