# C.32.CONWAY - Architecture-Influence and Transformed-Architecture Correspondence {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Architectural subpattern under C.32
> **Status:** Stable
> **Normativity:** Normative unless explicitly marked informative
> **Tech-name:** `Architecture-Influence and Transformed-Architecture Correspondence`
> **Plain cue:** compare an architecture that influences the change with the architecture being changed
> **Lineage and search cue only:** Transformer and Transformed Architecture Correspondence

## C.32.CONWAY:1 - Problem frame {#problem-frame}

Use this pattern when one architecture-side source — recovered as an exact described holon, selected `U.Structure`, and either an obtaining C.30 `ArchitectureRelation` or truthful modal `ArchitectureClaim` — or another independently typed Work arrangement, communication structure, constraint, or candidate-synthesis result influences the candidate architecture of a changed referent, and the practitioner must decide what to change on either side without mistaking influence for action.

Plain cue: **compare an architecture that influences the change with the architecture being changed**.

Primary working reader: an architect or architecture-responsible practitioner who must compare one independently typed influence source with the current or modal architecture content of the changed referent and prepare candidate changes without turning an `ArchitectureRelation`, selected structure, claim, or architecture-bearing holon into an actor.

Typical entry situations include:

- a desired product architecture cannot be produced and verified by the current manufacturing and certification arrangements;
- chosen service boundaries still force every delivery team to coordinate every release;
- a method family is proposed for changing documents, but the assigned review roles and evidence structure do not fit what the project must produce;
- an AI-agent toolchain is intended for Work on project products, but its control and evidence boundaries do not fit the changed product architecture; or
- the project needs a source-side, transformed-side, joint, or bounded-mismatch inverse-Conway candidate rather than another diagram of the desired target.

A clean-looking target architecture can still be unbuildable or unproducible, untestable, hard to maintain or evolve, or hard to certify. Existing production, communication, approval, control, evidence, and operating arrangements can constrain the candidate and shift coordination into shared releases, approvals, evidence reconciliation, or exception handling. Treat each such arrangement as an independently typed influence source and recover its direct influence relation when that relation is asserted; the source architecture does not act, and mirroring alone does not establish architecture adequacy.


Start with the domain action: a manufacturing system builds a product, a compiler compiles a program, a service team changes a service, a clinical team treats a patient, or an instructional system teaches a learner. Identify the changed referent first. Only then name an acting system, exact system-role assignment, and dated Work when those facts are current. Separately name the architecture or other source that influences the candidate and the exact relation by which it does so.

**First-minute use slice.** A product-family team wants independently replaceable field modules. It identifies the changed referent as `ProductFamilyFieldModuleBoundary@2026Q3`. The influence side is the obtaining C.30 `ArchitectureRelation(ManufacturingCertificationSystem@Plant-A, BatchLineSharedEvidenceStructure@Current)`; the transformed side is the obtaining C.30 `ArchitectureRelation(ProductFamily@Current, FieldModuleBoundaryStructure@Current)`. The exact holons and selected `U.Structure` participants remain visible, and any desired replacement structure stays only in a separate `ArchitectureClaim`. No direct architecture-influence kind or predicate has yet been recovered, so the team keeps the pairing as a provisional independent-change pressure with `missing-governor`. It prepares source-side, transformed-side, joint, and bounded-mismatch candidates without naming an acting system, system-role assignment, Work occurrence, or actual transformation. Those facts are added separately only if a later claim needs them.

The primary working object is a local candidate-synthesis frame. It can pair actual architecture sides through exact obtaining C.30 `ArchitectureRelation` refs or carry candidate, required, desired, or expected structure only through separately identified `ArchitectureClaim` refs. When one exact architecture-influence or correspondence relation already obtains between two actual architecture sides, C.32.CONWAY is also the pattern for one reusable `ArchitectureInfluenceTransformedArchitectureCorrespondenceRow@Context` episteme about that exact occurrence. The frame, row, architecture relations, claims, selected structures, changing system, Work, actual transformation, changed referent, candidate palette, and any network that later cites the row remain different objects.

What goes wrong if this pattern is missed: an architecture, organization chart, method family, toolchain, communication structure, or network record is called the transformer and silently receives agency, a system-role kind or assignment, Work, or participation in the change. Or the reverse happens: real performer and Work facts disappear behind a vague claim that one architecture shaped another.

What this buys in practice: the practitioner can prepare architecture candidates while preserving four independent questions—what changed, who acted or performed Work, which sources influenced the candidate, and which exact architecture pair the current correspondence row concerns.

Ordinary working move:

1. name the changed referent and, only when actual change is claimed, the independently admitted `U.Transformation`; keep every actor-side or Work-to-change relation separate;
2. name exact acting and performance facts only when current;
3. name each influence source with its kind and direct influence relation;
4. for an exact reusable row, select one pair of obtaining C.30 `ArchitectureRelation` occurrences and keep each holon and selected-structure participant visible; when either side is only candidate, required, desired, or expected, keep the pair in the frame with its exact `ArchitectureClaim` instead;
5. prepare source-side change, transformed-side change, joint change, or bounded mismatch candidates.

Adoption test: a reader can tell which exact case passes, which does not, what the practitioner changes next, and whether the result is only local synthesis material or a reusable exact pair row.

Not this pattern when the current work is only bounded-change identification, system-role assignment or Work attribution, module-interface repair, mathematical structural similarity, local choice, or an architecture decision. Use the subject pattern and return here only when one pair of an influence-source architecture and a transformed architecture changes candidate synthesis.

Common exits by claim kind:

- `A.3.4` or `A.3.4.P` for the bounded change and changed referent.
- `A.12` for acting-side externalization, `A.13` for exact actual-performer recovery, `A.15.1` for independent dated-Work admission and distributed-performer forms, `A.2.1` for an exact assignment occurrence when separately claimed, `F.6` for a later `performedUnderAssignment(W, RA)` relation only when precise assignment-bound attribution is expressly consumed, and the pattern that defines any direct actor-side or Work-to-change relation needed by the current use. F.6's holder projection only supports equality comparison with the already recovered performer; it identifies neither assignment nor performer.
- `A.6.M` for module-interface repair.
- `C.32.ACS` for current architecture-characteristic criteria rows and `C.25` for any composite Q-Bundle and exact slot used by the trade-off.
- `C.29` and the project-selected structural-equivalence pattern for structural similarity.
- `A.19.CPM` for explicit comparison and `A.19.SelectorMechanism` for set-returning selection.
- `G.5` for selected-set result declaration; `E.17` for a source-backed publication face and source return; `E.24.PUB` for the publication occurrence and audience availability; `C.18` and `C.19` for archive, front, or pool-treatment policy.
- `C.11` for fixed local choice and `C.32.PAD` for a project architecture decision.

The first useful output is `ArchitectureInfluenceTransformedArchitectureCorrespondenceFrame@Project`. It is a working record for candidate synthesis, not an acting entity, exact relation occurrence, architecture decision, or structural-equivalence claim.

For a first pass, fill only the synthesis question, intended correspondence use, ClaimScope when it changes the claim, independently identified changed referent, source-side and transformed-side exact holon and selected-structure refs, and either an obtaining C.30 `ArchitectureRelation` ref or a truthful modal `ArchitectureClaim` ref for each side. Add architecture-characteristic criteria refs or plain provisional heads, applicable candidate-form heads, evidence and the evolution window, and the next pattern. Assert an influence row only when its direct relation is current and both architecture sides are obtaining C.30 occurrences; otherwise keep one explicit provisional pressure in `provisionalArchitectureCharacteristicHeads[]` and its exact return. The first-minute case above can be filled as follows:

```text
ArchitectureInfluenceTransformedArchitectureCorrespondenceFrame@Project:
  intendedCorrespondenceUse: prepare architecture candidates for independent field-module replacement
  claimScopeRef?: product-family module-change architecture claims
  synthesisQuestion: which source-side, product-side, joint, or bounded-mismatch change can support independently replaceable field modules?
  changedReferentRef: ProductFamilyFieldModuleBoundary@2026Q3
  influenceSourceSelectedStructureMap[]:
    - influenceSourceHolonRef: ManufacturingCertificationSystem@Plant-A
      influenceSourceArchitectureRelationRef: C.30 ArchitectureRelation(ManufacturingCertificationSystem@Plant-A, BatchLineSharedEvidenceStructure@Current)
      influenceSourceArchitectureClaimRef?: omitted — the obtaining relation and current structure are enough for this use
      structureKindRef: BatchAndEvidenceResponsibilityStructure
      selectedStructureRef: BatchLineSharedEvidenceStructure@Current
      contributionToCandidatePressure: may prevent independent field-module replacement
      architectureCharacteristicPressure: provisional independent-change pressure
      relationFunctionClaimRef: C.30 plus A.22
      sourceReturnCondition: missing-governor — recover the direct architecture-influence kind and predicate
  transformedHolonRef: ProductFamily@Current
  transformedArchitectureRelationRef: C.30 ArchitectureRelation(ProductFamily@Current, FieldModuleBoundaryStructure@Current)
  transformedArchitectureClaimRef?: omitted — the obtaining relation and current structure are enough for this use
  transformedSelectedStructureMap[]:
    - structureKindRef: ModuleBoundaryStructure
      selectedStructureRef: FieldModuleBoundaryStructure@Current
      requiredStructureContribution: permit independent field-module replacement
      architectureCharacteristicPressure: provisional independent-change pressure
      relationFunctionClaimRef: C.30 plus A.22
  correspondenceClaims[]:
    - correspondenceId: BatchEvidence-to-FieldModulePressure
      influenceSourceArchitectureRelationRef: C.30 ArchitectureRelation(ManufacturingCertificationSystem@Plant-A, BatchLineSharedEvidenceStructure@Current)
      transformedArchitectureRelationRef: C.30 ArchitectureRelation(ProductFamily@Current, FieldModuleBoundaryStructure@Current)
      influenceSourceSelectedStructureRef: BatchLineSharedEvidenceStructure@Current
      transformedSelectedStructureRef: FieldModuleBoundaryStructure@Current
      correspondenceUse: prepare candidates; no exact pair row asserted
      pressureDirection: batch and evidence arrangements may constrain module independence
      provisionalArchitectureCharacteristicHeads[]: independent change for field modules
      receivingUsePatternLocator: C.32.ACS
      sourceReturnCondition: missing-governor — recover the direct influence kind and predicate
  candidateArchitectureConfigurations[]:
    - candidateRef: SourceSideChange@CellAndEvidenceStructures
    - candidateRef: TransformedSideChange@FieldModuleBoundary
    - candidateRef: JointChange@CellEvidenceAndModuleBoundary
    - candidateRef: BoundedMismatch@ExplicitExceptionCost
  evolutionWindowRef: ProductFamilyModuleChange@2026Q3
  evidenceRefs?: current batch-line evidence-structure and field-module boundary records
  nextQuestionPatternLocator: C.32.ACS
```

This sparse frame asserts no influence occurrence and no exact pair row. The four candidate refs are first-pass heads, not comparison-ready configurations. Add acting-system, exact system-role-assignment, dated-Work, exact-pair-row, C.29, network, publication, comparison-ready gain, loss, and preservation, and any additional source-return fields only when the corresponding claim becomes current; adding them refines this frame without changing its changed referent, architecture pair, or provisional pressure. The complete extension schema is:

```text
ArchitectureInfluenceTransformedArchitectureCorrespondenceFrame@Project:
  projectWorkOccurrenceRef?: U.EntityRef constrained to U.Work
  architectureCorrespondenceFrameProjectUseRelationRef?: U.RelationRef defined by the exact synthesis-use or work-use pattern
  synthesisQuestion:
  intendedCorrespondenceUse:
  claimScopeRef?: U.ClaimScope
  changedReferentRef:
  actualTransformationRef?: U.EntityRef constrained to U.Transformation, only when A.3.4 independently admits the bounded change of changedReferentRef
  performerRows[]?:
    actingSystemRef: U.EntityRef constrained to U.System; for performance, this is the exact actual performer recovered through performerA13CoreBasisRef
    performerA13CoreBasisRef?: required with workOccurrenceRef; cites the exact local kind and criterion, classification, same obtaining assignment, scope, working situation, window, and adequate core evidence
    workOccurrenceRef?: U.EntityRef constrained to U.Work, independently admitted by A.15.1 when performance is claimed
    actingSystemRoleAssignmentRef?: U.RelationRef constrained to U.SystemRoleAssignment, include when an obtaining assignment is separately represented and require the same A.13 assignment when attribution is represented
    performedUnderAssignmentRelationRef?: U.RelationRef governed by F.6, include only when this row expressly represents precise assignment-bound attribution; omit otherwise; missing or failed F.6 leaves workOccurrenceRef intact
    actorSideOrWorkToChangeRelationRefs[]: exact U.RelationRef values required by the current claim
  influenceSourceRows[]?: asserted influence facts only
    influenceSourceRef:
    influenceSourceKindRef:
    exactInfluenceRelationRef: U.RelationRef
    influencePatternLocator:
  influenceSourceSelectedStructureMap[]?:
    influenceSourceHolonRef:
    influenceSourceArchitectureRelationRef?: exact obtaining C.30 ArchitectureRelation ref
    influenceSourceArchitectureClaimRef?: exact C.30 ArchitectureClaimRef for actual, candidate, required, desired, or expected content not carried by an obtaining relation
    structureKindRef:
    selectedStructureRef:
    contributionToCandidatePressure:
    architectureCharacteristicPressure:
    relationFunctionClaimRef:
    sourceReturnCondition?:
  transformedHolonRef:
  transformedArchitectureRelationRef?: exact obtaining C.30 ArchitectureRelation ref
  transformedArchitectureClaimRef?: exact C.30 ArchitectureClaimRef for actual, candidate, required, desired, or expected content not carried by an obtaining relation
  transformedSelectedStructureMap[]:
    structureKindRef:
    selectedStructureRef?:
    requiredStructureContribution:
    architectureCharacteristicPressure:
    relationFunctionClaimRef:
    sourceReturnCondition?:
  evolutionWindowRef:
  evidenceRefs?:
  architecturePairRowRefs[]?: ArchitectureInfluenceTransformedArchitectureCorrespondenceRow@Context refs
  correspondenceClaims[]?: synthesis-local compound claims that have not yet met the exact-row assertion threshold
    correspondenceId:
    influenceSourceArchitectureRelationRef?:
    influenceSourceArchitectureClaimRef?:
    transformedArchitectureRelationRef?:
    transformedArchitectureClaimRef?:
    influenceSourceSelectedStructureRef?:
    transformedSelectedStructureRef:
    correspondenceUse:
    pressureDirection:
    affectedArchitectureCharacteristicRefs[]?: current C.32.ACS criteria-row refs; exact C.25 Q-Bundle slot refs when composite
    provisionalArchitectureCharacteristicHeads[]?: plain discovery cues pending C.32.ACS/C.25; never criteria refs
    expectedArchitectureGain?:
    knownArchitectureLoss?:
    preservedStructure?:
    lostOrHiddenStructure?:
    receivingUsePatternLocator:
    sourceReturnCondition:
  candidateArchitectureConfigurations[]:
    candidateRef:
    influenceSourceSideChange?:
    transformedArchitectureChange?:
    coordinationChange?:
    expectedArchitectureGain?:
    knownArchitectureLoss?:
    evolutionWindowRef?:
    receivingUsePatternLocator?:
    sourceReturnCondition?:
    stopOrEscalationCondition?:
  c29LensOrStructuralEquivalenceRef?:
  nextQuestionPatternLocator:
```

Project-local use keeps two separate fields. `@Project` remains a compatibility and retrieval cue only. If the frame is used in one actual project, `projectWorkOccurrenceRef` names the exact composite `U.Work` and `architectureCorrespondenceFrameProjectUseRelationRef` names the direct relation by which that Work uses the frame. The frame, synthesis Work, candidates, architecture relations, claims, selected structures, and project Work remain distinct. An `ArchitectureRelation` ref is affirmative only for an independently obtaining C.30 occurrence; candidate, required, desired, or expected architecture content stays in an `ArchitectureClaim` and cannot enter an exact pair row as though it already obtained.

`TransformerTransformedArchitectureCorrespondenceFrame@Project` and the former title “Transformer and Transformed Architecture Correspondence” are lineage and search cues only. They do not name the current Tech object, make any named value an actor, or establish an acting-system, system-role-kind, assignment, Work, or participation fact.

## C.32.CONWAY:2 - Problem {#problem}

Architecture influence and action often occur in the same story but are not the same fact. A manufacturing architecture can constrain a product candidate while a manufacturing system performs production Work. A communication structure can influence service boundaries while people or teams perform change Work only through their admitted exact `U.System` identities. A method description can influence a work-product architecture without being a worker. A toolchain architecture can constrain project-task candidates while an admitted execution system acts.

Transformer and transformed wording can hide these differences. It can leave the changed referent implicit, treat an architecture bearer as the performer, omit the exact system-role assignment and dated Work, or call a source influential without a direct relation. It can also stretch one local architecture pair into a whole recursive transformation-flow network.

C.32.CONWAY repairs the problem by keeping the changed referent, actor and performance facts, influence-source facts, and one exact architecture pair separately recoverable. Conway and inverse-Conway practice then supplies candidate pressure, not a universal relation and not evidence that any source acted.

## C.32.CONWAY:3 - Forces {#forces}

| Force | Tension |
|---|---|
| Domain action vs architecture influence | A system can act while its architecture or another selected structure influences the candidate; neither fact entails the other. |
| Performance detail vs candidate synthesis | Exact system-role assignment and dated Work matter when performance is claimed, but candidate architecture work must not invent them from an influence diagram. |
| Exact influence vs useful local frame | A local compound correspondence can guide candidate synthesis before a reusable episteme about an obtaining exact relation can be asserted. |
| One pair vs recursive network | One architecture pair can qualify a network reading, but the pair is neither the network nor a cross-flow relation by citation. |
| Desired transformed architecture vs source-side constraint | The transformed architecture may need a structure the current influence-side arrangement cannot sustain. |
| Evolution window | A correspondence that works now can fail when either selected architecture, the direct relation, or the changed referent changes. |

## C.32.CONWAY:4 - Solution {#solution}

Build the local synthesis frame first. Admit a relation kind only through the applicable E.24-family admission pattern and direct settlement. Use that pattern's predicate and applicability to test the current pair. If current facts or constituting history satisfy the predicate affirmatively, one world-side occurrence obtains and the row may cite its exact identity. If the predicate is false, no exact pair row is asserted. If the current facts do not decide it, keep the correspondence synthesis-local and name the missing grounding or information-sufficiency boundary. Use `missing-governor` only when no direct relation kind and predicate govern the intended pair and use.

### C.32.CONWAY:4.1 - Keep acting, influence, and correspondence facts separate {#keep-acting-influence-and-correspondence-facts-separate}

1. **Name the domain action and changed referent.** Identify `changedReferentRef` independently. Add `actualTransformationRef` only when A.3.4 independently admits one bounded change of that same continuing referent; keep actor-side and Work-to-change relations under their subject patterns. Architecture influence identifies none of those facts.
2. **Add acting and performance facts only when claimed.** Every precise actual performer is one exact `U.System` recovered through A.13. Claimed performance requires one exact dated `U.Work` independently admitted through A.15.1 and the exact actor-side or Work-to-change relation needed by the claim. Add an obtaining occurrence of a directly admitted `U.SystemRoleAssignment` species under A.2.1 and F.6 `performedUnderAssignment(W, RA)` only when this frame or its receiving use expressly consumes precise assignment-bound attribution through the same obtaining A.13 assignment; then compare `S` with `RA.HolderSystemSlot`. F.6 identifies neither assignment nor performer, and missing or failed F.6 leaves the Work intact. Use A.15.1 `CC-A15.1-17` when several systems jointly perform the top-level Work or when the use instead needs a parent Work with separately performed child occurrences.
3. **Name every influence source by kind.** Architecture, selected structure, Work, communication, constraint, and candidate-synthesis results retain their kinds and direct influence relations. Influence alone supplies no system identity, system-role kind or assignment, Work, performer status, changed-referent identity, or transformation participation.
4. **Select one architecture pair.** For an exact row, name one obtaining influence-source C.30 `ArchitectureRelation` and one obtaining transformed-side C.30 `ArchitectureRelation`, with each exact holon and selected-`U.Structure` participant. Their architecture-bearing holons may differ from every acting system. Record equality only when independent actor and architecture-bearer facts establish it. If either side is only candidate, required, desired, or expected, keep its exact `ArchitectureClaim` and the pair in the synthesis frame; do not assert an exact pair row.
5. **Map only structures and characteristics that change the candidate.** Name the source-side selected structure, transformed-side selected structure, expected gain, known loss, evolution window, pattern for the next question, and source-return condition. For each affected characteristic, reference only the few current `C.32.ACS` criteria rows and any declared `C.25` Q-Bundle slots that make this trade-off real.
6. **Prepare four candidate forms.** Change the influence-source side, change the transformed architecture, change both, or keep a bounded mismatch with an explicit cost and reopen trigger.
7. **Use C.29 only for structural-similarity claims.** A correspondence row does not establish homomorphism, equivalence, or architecture adequacy.
8. **Stop at the next governed claim.** Send comparison, selection, publication, choice, decision, evidence, assurance, gate, Work, or organization-governance claims to their direct patterns.

### C.32.CONWAY:4.2 - Exact reusable architecture-pair row {#exact-reusable-architecture-pair-row}

```text
ArchitectureInfluenceTransformedArchitectureCorrespondenceRow@Context <: U.Episteme:
  entityOfConcernRef: exactArchitectureInfluenceOrCorrespondenceRelationOccurrenceRef
  entityOfConcernKindRef: exactArchitectureInfluenceOrCorrespondenceRelationKindRef
  relationFunctionClaimRef: subject pattern of that exact relation kind and occurrence
  influenceSourceArchitectureRelationRef: one exact obtaining C.30 ArchitectureRelation
  influenceSourceHolonRef: the exact architectureBearingHolonRef participant of influenceSourceArchitectureRelationRef
  influenceSourceSelectedStructureRef: the exact selectedArchitectureStructureRef participant of influenceSourceArchitectureRelationRef
  influenceSourceArchitectureClaimRef?: exact C.30 ArchitectureClaimRef when the current use also needs claim content about that same holon, relation, or structure
  transformedArchitectureRelationRef: one exact obtaining C.30 ArchitectureRelation
  transformedHolonRef: the exact architectureBearingHolonRef participant of transformedArchitectureRelationRef
  transformedSelectedStructureRef: the exact selectedArchitectureStructureRef participant of transformedArchitectureRelationRef
  transformedArchitectureClaimRef?: exact C.30 ArchitectureClaimRef when the current use also needs claim content about that same holon, relation, or structure
  changedReferentRef: exact independently identified referent of the current change
  actualTransformationRef?: U.EntityRef constrained to U.Transformation, only when A.3.4 independently admits the bounded change of changedReferentRef
  performerRows[]?:
    actingSystemRef: U.EntityRef constrained to U.System; for performance, this is the exact actual performer recovered through performerA13CoreBasisRef
    performerA13CoreBasisRef?: required with workOccurrenceRef; cites the exact local kind and criterion, classification, same obtaining assignment, scope, working situation, window, and adequate core evidence
    workOccurrenceRef?: U.EntityRef constrained to U.Work, independently admitted by A.15.1 when performance is claimed
    actingSystemRoleAssignmentRef?: U.RelationRef constrained to U.SystemRoleAssignment, include when an obtaining assignment is separately represented and require the same A.13 assignment when attribution is represented
    performedUnderAssignmentRelationRef?: U.RelationRef governed by F.6, include only when this row expressly represents precise assignment-bound attribution; omit otherwise; missing or failed F.6 leaves workOccurrenceRef intact
    actorSideOrWorkToChangeRelationRefs[]: U.RelationRef
  additionalInfluenceSourceRows[]?:
    influenceSourceRef:
    influenceSourceKindRef:
    exactInfluenceRelationRef: U.RelationRef
    influencePatternLocator:
  affectedArchitectureCharacteristicRefs[]: current C.32.ACS criteria-row refs; exact C.25 Q-Bundle slot refs when composite
  evolutionWindowRef:
  correspondenceUse:
  expectedArchitectureGain:
  knownArchitectureLoss:
  receivingUsePatternLocator:
  sourceReturnCondition:
  networkCrossFlowRelationRowRef?: E.18.NET NetworkCrossFlowRelationRowRef
```

The row is a `U.Episteme` about one already obtaining direct influence or correspondence relation whose exact participants include the two obtaining C.30 architecture-relation occurrences required by this use. Because those occurrences fill participant positions of another relation, each is explicitly individuated under A.6.REL for this receiving use. The row neither creates the influence occurrence nor mints a universal Conway relation. Each C.30 occurrence keeps its exact holon and selected-`U.Structure` participants; the influence occurrence keeps its identity under its direct relation pattern and A.6.REL. This row only describes them for the current correspondence use. `entityOfConcernRef`, its kind, its governor, both C.30 occurrences and their participant pairs, and the changed referent are required. If the practitioner has only a useful local compound correspondence claim, or either architecture side is modal rather than obtaining, keep it in the frame for candidate synthesis. Assert the row only after the admitted influence relation kind's direct predicate is applicable and current facts satisfy it affirmatively. If the predicate is false, assert no row; if facts are unresolved, keep the frame and name that boundary; if the kind or predicate is absent, return `missing-governor`. None of these branches permits inferring a relation from two architecture claims, structures, diagrams, or names.

### C.32.CONWAY:4.3 - Qualified network reading {#qualified-network-reading}

The same exact pair row may appear in `architectureCorrespondenceRowRefs[]` of several `TransformationFlowStructureNetworkRecord@Context` values while its pair, relation occurrence, evolution window, correspondence use, and claim scope remain current. Each citation contributes only one qualified architecture reading. The row's optional singular `networkCrossFlowRelationRowRef`, when present, qualifies only the exact current record edition named by that locator; it does not qualify the row's citations from other records. No citation makes the pair row the network, adds a member, or satisfies the network's exact cross-flow-relation discriminator.

Set `networkCrossFlowRelationRowRef` only when the pair row's exact influence occurrence and architecture-relation participants are independently grounded in member-flow positions and the locator's `transformationFlowStructureNetworkRecordRef` names the same exact current record whose `architectureCorrespondenceRowRefs[]` citation this mapping is intended to qualify. Resolve that record first, then require exactly one `crossFlowRelationRow` to match the occurrence and complete ordered endpoint-binding identity. That row must preserve the same kind, governor, participant order, endpoints, and bindings as this correspondence row. Zero or several matches, a different record, or a stale record edition leaves the locator unresolved. Do not reuse one locator to qualify another record's citation. A record citation alone infers none of those facts.

Acting-system identity, system-role assignment, F.6 attribution, Work, actual transformation, actor-side or Work-to-change relation, influence relation, and network cross-flow relation remain separately governed even when one case cites all of them.


### C.32.CONWAY:4.4 - Candidate moves and repair rows {#candidate-moves-and-repair-rows}

Plain text begins with the domain action—builds, assembles, repairs, configures, treats, teaches, compiles, or evaluates. It then names the acting system and Work only when those facts are current. In a separate sentence it says which architecture or other source influences which candidate through which exact relation. `Creator`, `creation`, `producer`, `transformer architecture`, and `uses` remain ordinary cues, not universal technical labels.

Choose only pressures that change the candidate or protect against a concrete loss. Every `affectedArchitectureCharacteristicRefs[]` value in an exact pair row or comparison-ready candidate must resolve to a current `C.32.ACS` criteria row; when the pressure is one slot of a composite quality family, also resolve the declared `C.25` Q-Bundle and that exact slot. If those governed objects do not yet exist, put plain heads such as independent change, substitutability, evidence reuse, latency, coupling or cohesion, coordination load, and source-return cost only in the local frame's `provisionalArchitectureCharacteristicHeads[]`; never place them in `affectedArchitectureCharacteristicRefs[]`. These heads are discovery cues, not a universal catalogue and not criteria refs. Use `C.32.ACS` or `C.25` before making a stronger comparison, selection, or decision claim.

| Correspondence repair row | Use | Minimum repair against overread |
|---|---|---|
| `changedReferentRecovery` | The story names a team, line, tool, method, or organization but not what changes. | Identify the exact continuing changed referent; when actual change is asserted, identify its A.3.4 `U.Transformation`; keep actor-side and Work-to-change relations separately governed. |
| `performerRecovery` | A source is said to build, design, repair, or operate. | Recover each exact actual performer through A.13 and let A.15.1 independently admit the dated `U.Work`; add the exact A.2.1 assignment, F.6 `performedUnderAssignment` occurrence, and holder-equality check only when this frame or receiving use expressly consumes precise assignment-bound attribution through the same obtaining A.13 assignment. Add direct actor-side or Work-to-change relations separately; use A.15.1 `CC-A15.1-17` when several systems perform. |
| `influenceSourceRecovery` | An architecture or structure is said to shape a candidate. | Name its exact kind and direct influence relation; otherwise keep it as a candidate cue. |
| `architecturePairRecovery` | Two architectures are compared or linked. | Apply the direct relation pattern. With no kind/predicate, return `missing-governor`; with unresolved facts, keep the pair synthesis-local and name the missing grounding; with a false predicate, assert no occurrence; with a satisfied predicate, name the exact obtaining occurrence and pair. |
| `inverseConwayRetargeting` | The desired transformed architecture is sound, but the current source-side arrangement cannot sustain it. | Change selected influence-source structures and record migration cost, new burden, and stop condition. |
| `transformedArchitectureRetargeting` | The source-side arrangement is fixed or too expensive to change in the current window. | Change the transformed architecture candidate and record the lost desired property or exception. |
| `jointCorrespondenceSynthesis` | Neither side alone can carry the architecture characteristic. | Change both sides and record preserved structure, lost structure, and coordination burden. |
| `boundedCorrespondenceMismatch` | A mismatch is tolerable for now. | State exception cost, bounded-use limit, source-return condition, and reopen trigger. |

**Stop condition.** A first-pass frame may stop when it names the changed referent, separately typed source and transformed architectures, one selected structure on each side, either governed affected-characteristic refs or visibly provisional heads with their exact return, the applicable candidate-form heads, and the next subject pattern. Every acting, performance, or influence fact that is asserted must already have its direct basis. Before a candidate enters comparison or reliance, complete its source-side change, transformed-side change, expected gain, known loss, evolution window, pattern for the next question, source-return condition, and stop. An exact pair row additionally requires its direct relation predicate to be satisfied and its obtaining occurrence to be identified. A provisional pressure stays in `correspondenceClaims[]` with the exact reason visible: missing governor, unresolved grounding or information sufficiency, or a false predicate.

**Lowering condition.** Lower an exact row to synthesis-local correspondence material when its influence occurrence, either C.30 architecture-relation occurrence or participant pair, changed referent, evolution window, or receiving use is missing or stale. Retire a candidate when its source-side change, transformed-side change, bounded mismatch, or known loss no longer belongs to the declared evolution window. Use A.3.4 or E.18 when the actual transformation, changed referent, or flow relation is not recovered; A.12, A.2.1, A.15.1, and F.6 when the issue is acting side, assignment, Work, or attribution; and C.29 when the current claim is structural similarity or preservation.

## C.32.CONWAY:7 - Conformance Checklist {#conformance-checklist}

| ID | Requirement | Failed-check repair |
|---|---|---|
| `CC-C32.CONWAY-1` | @fact:CC-C32-CONWAY-1 `changedReferentRef` is independently identified; any claimed actual bounded change has one A.3.4 `actualTransformationRef`, while actor-side and Work-to-change relations retain their direct governors. @status:spec/done | Recover those exact objects and relations or keep the change description provisional. |
| `CC-C32.CONWAY-2` | @fact:CC-C32-CONWAY-2 Every claimed actor is an admitted `U.System`; every claimed work-facing assignment names an occurrence and its declared A.2.1 species. The occurrence's holder matches the separately named acting System; the species defines the local assigned-kind domain, predicate, applicability, participant meanings, and occurrence identity. @status:spec/done | Add the System, species, and assignment occurrence or remove the acting or assignment claim. |
| `CC-C32.CONWAY-3` | @fact:CC-C32-CONWAY-3 Claimed performance has every exact actual performer recovered through A.13 and exact dated Work independently admitted through A.15.1. An exact A.2.1 assignment, F.6 `performedUnderAssignment(W, RA)` occurrence, and `S = RA.HolderSystemSlot` appear only when precise assignment-bound attribution is expressly represented; missing or failed F.6 leaves Work intact. Direct actor-side or Work-to-change relations remain separate, and several performers use A.15.1 `CC-A15.1-17` forms. @status:spec/done | Restore the independent performer and Work basis; add attribution only for a consuming claim, or remove the unsupported performance or attribution claim. |
| `CC-C32.CONWAY-4` | @fact:CC-C32-CONWAY-4 Every influence source retains its exact kind and direct obtaining occurrence; influence entails no actor, system-role kind or assignment, Work, changed-referent, or transformation-participation fact. @status:spec/done | Apply the direct predicate: a missing kind or predicate returns `missing-governor`, unresolved facts stay provisional, and a false predicate excludes the occurrence claim; delete inferred acting facts. |
| `CC-C32.CONWAY-5` | @fact:CC-C32-CONWAY-5 One exact pair row names two obtaining C.30 `ArchitectureRelation` occurrences, each exact holon and selected-`U.Structure` participant, the changed referent, exact obtaining influence or correspondence occurrence, admitted relation kind, direct predicate and governor, and a satisfied affirmative case. Modal architecture content remains an `ArchitectureClaim` in the frame. @status:spec/done | Complete the satisfied actual pair; otherwise keep only the synthesis-local frame and state modal status, `missing-governor`, unresolved grounding, or false predicate exactly. |
| `CC-C32.CONWAY-6` | @fact:CC-C32-CONWAY-6 Equality between an architecture bearer and an actor is recorded only from independent facts. @status:spec/done | Separate the refs and remove equality inference. |
| `CC-C32.CONWAY-7` | @fact:CC-C32-CONWAY-7 The two project-use fields retain their exact Work identity and direct use-relation meaning. @status:spec/done | Add both facts when project use is claimed or keep `@Project` retrieval-only. |
| `CC-C32.CONWAY-8` | @fact:CC-C32-CONWAY-8 Each comparison-ready candidate states source-side change, transformed-side change, expected gain, known loss, evolution window, pattern for the next question, source-return condition, and stop; a first-pass candidate head is visibly outside comparison. @status:spec/done | Complete the candidate before comparison or keep only its `candidateRef` as a first-pass head. |
| `CC-C32.CONWAY-8a` | @fact:CC-C32-CONWAY-8a Every `affectedArchitectureCharacteristicRefs[]` value resolves to a current C.32.ACS criteria row and, when composite, the exact C.25 Q-Bundle slot; a local discovery cue appears only in `provisionalArchitectureCharacteristicHeads[]` and supports no comparison, selection, or decision. @status:spec/done | Resolve the governed ref, move the cue to the provisional-head field and use C.32.ACS/C.25, or remove the stronger claim. |
| `CC-C32.CONWAY-9` | @fact:CC-C32-CONWAY-9 Structural-similarity claims use C.29 or the selected structural-equivalence pattern. @status:spec/done | Remove similarity entailment or apply the direct pattern. |
| `CC-C32.CONWAY-10` | @fact:CC-C32-CONWAY-10 A network record cites the pair only as a qualified reading; any `networkCrossFlowRelationRowRef` names that same exact current citing record, resolves exactly one row there, and its independently grounded occurrence and endpoint bindings agree with this pair. The singular locator qualifies no other record citation. @status:spec/done | Remove the network link or repair the citing record, occurrence, and ordered endpoint-binding locator. |
| `CC-C32.CONWAY-11` | @fact:CC-C32-CONWAY-11 Source-return and evolution-window conditions are present. @status:spec/done | Add the changed values and reopen trigger. |

## C.32.CONWAY:9 - Consequences {#consequences}

| Positive consequence | Cost or trade-off |
|---|---|
| Architecture influence can guide synthesis without granting agency. | Actor, Work, changing, and influence relations must be grounded separately. |
| Exact pair rows can be reused across current network records. | Each reuse must preserve pair, relation occurrence, qualification window, and claim scope. |
| Inverse-Conway work produces explicit candidate changes and bounded mismatches. | Some familiar “transformer architecture” shorthand must be expanded into several facts. |
| Changed referent and transformed architecture stay recoverable. | A useful local frame may remain below exact-row assertion when the governor is missing or case facts remain unresolved. |
| Network recursion remains with E.18.NET. | One pair row cannot stand in for the whole network or its cross-flow relations. |
| Candidate architectures are checked against source-side production, testing, maintenance, evidence, and evolution arrangements. | Changing the influence-source side can be expensive; an attractive transformed-side candidate may therefore be rejected for the current evolution window. |
| Organization, Work, method, tool, and module claims are routed to their subject patterns instead of being hidden in an architecture-pair result. | This separation may require the practitioner to follow several separately governed exits before comparison. Mirroring supplies candidate pressure, not architecture adequacy; use C.29 when the claim is structural similarity or preservation. |

## C.32.CONWAY:12 - Relations {#relations}

- **Builds on:** `C.32` for candidate architecture synthesis; `C.30` for exact described holons, obtaining `ArchitectureRelation` occurrences, selected `U.Structure` participants, and modal `ArchitectureClaim` content; `A.3.4` and `A.3.4.P` for the continuing changed referent and actual bounded transformation; `A.12` for acting-side externalization; `A.13` for exact actual-performer recovery; `A.15.1` for independent dated-Work admission and distributed-performer forms; `A.2.1` for assignment occurrence identity when separately represented; `F.6` for a later `performedUnderAssignment(W, RA)` relation only when precise assignment-bound attribution is consumed; direct subject relation patterns for actor-side, Work-to-change, and influence occurrences; `A.6.REL` when this episteme consumes occurrence identity; `E.18` for one TFS; and `E.18.NET` for network identity and exact cross-member relations. F.6's holder projection only compares equality with the already recovered performer.
- **Uses:** `C.32.ACS` for current architecture-characteristic criteria rows; `C.25` for composite Q-Bundles and their declared slots; `C.32.MLAO` for a cross-scope residual; `C.32.FAIL` for a correspondence repair failure; `C.29` when structural similarity, preservation, mapping, or equivalence is claimed; and `A.6.P.WMR` and `A.6.RCD` when a required direct relation cannot be recovered.
- **Patterns for the next questions:** `A.19.CPM` for explicit comparison, `A.19.SelectorMechanism` for set-returning selection, `G.5` for selected-set result declaration, `E.17` for a source-backed publication face and source return, `E.24.PUB` for the publication occurrence and audience availability, `C.18` and `C.19` for archive, front, or pool treatment, `C.11` for fixed local choice, `C.32.PAD` for architecture decisions, `A.10` for evidence, `B.3` for assurance, `A.21` for gate decisions, the applicable authority or permission relation for release, and the direct method, Work, or organization-governance patterns when those claims are current.
- **Network boundary:** an `ArchitectureInfluenceTransformedArchitectureCorrespondenceRow@Context` may be cited as one qualified reading in `architectureCorrespondenceRowRefs[]`; it is not the network and does not satisfy an E.18.NET cross-flow relation without the separately grounded obtaining occurrence and endpoint bindings. Its optional singular row locator qualifies only the exact current citing record it names.
- **P2S docking:** `C.32.P2S` may use C.32.CONWAY when a problem-to-structure flow needs one exact architecture-influence/transformed-architecture pair. It does not infer performer or influence facts from the flow card.
- **Boundary:** C.32.CONWAY governs correspondence framing and one exact reusable architecture-pair episteme inside candidate synthesis. It does not govern actor identity, Work occurrence, organization redesign, authority, evidence sufficiency, assurance, gate passage, release, structural-equivalence theory, final architecture decision, or transformation-flow-network identity.


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/C-32#root, spec://ai.lev/fpf-spec/contract/A-3-4#root, spec://ai.lev/fpf-spec/contract/A-12#root, spec://ai.lev/fpf-spec/contract/A-15-1#root, spec://ai.lev/fpf-spec/contract/A-22#root, spec://ai.lev/fpf-spec/contract/C-30#root, spec://ai.lev/fpf-spec/contract/C-32-ACS#root, spec://ai.lev/fpf-spec/contract/C-25#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/E-18-NET#root, spec://ai.lev/fpf-spec/contract/C-30-TFS-REL#root, spec://ai.lev/fpf-spec/contract/C-32-MLAO#root, spec://ai.lev/fpf-spec/contract/C-32-FAIL#root, spec://ai.lev/fpf-spec/contract/C-32-PAD#root, spec://ai.lev/fpf-spec/contract/A-19-CPM#root, spec://ai.lev/fpf-spec/contract/G-5#root, spec://ai.lev/fpf-spec/contract/C-11#root, spec://ai.lev/fpf-spec/contract/A-10#root, spec://ai.lev/fpf-spec/contract/B-3#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/C-30#root, spec://ai.lev/fpf-spec/contract/C-30-P#root, spec://ai.lev/fpf-spec/contract/C-30-TFS-REL#root, spec://ai.lev/fpf-spec/contract/C-32#root, spec://ai.lev/fpf-spec/contract/C-32-FAIL#root, spec://ai.lev/fpf-spec/contract/C-32-MLAO#root, spec://ai.lev/fpf-spec/contract/C-32-PAD#root, spec://ai.lev/fpf-spec/contract/E-18-NET#root, spec://ai.lev/fpf-eng-oce/contract/OCE-7#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/C-32-CONWAY
