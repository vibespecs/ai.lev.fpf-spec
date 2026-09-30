# A.22.CGUS - Which Continuations Are Available? — Constraint-Governed Unfolding Structure (CGUS): depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## A.22.CGUS:5 - Complete Worked Case {#complete-worked-case}

Return to the design review from `4.1`. The ordinary card becomes formal only because the team now needs to retain and compare the review basis across editions.

```text
selectedCGUSRef: DesignReviewAlternatives@DR-27
A22IdentityBasis:
  selectedConstituentRefs[]:
    DesignCandidate-A
    RepairProposal-A
    AcceptCandidate-Continuation
    RepairCandidate-Continuation
  selectedObtainingRelationOccurrenceRefs[]:
    RepairProposalTargetsCandidate@DR-27
  relationOccurrenceRecoveryRows[]:
    - relationOccurrenceRef: RepairProposalTargetsCandidate@DR-27
      predicateDefinitionRef: RepairProposalTargetsDesignCandidatePredicate
      participantRefsInPredicateOrder[]: [RepairProposal-A, DesignCandidate-A]
  appliedConstraintClaimRefs[]:
    AcceptIfBothChecksSatisfied
    RepairIfAnyCheckViolatedAndProposalTargetsCandidate
  namedSelectionUseFrame:
    questionOrAction: which review continuations satisfy the two-check rule for DesignCandidate-A?
    admissibleAction: show enabled, disabled, unknown or error results for the current case
    stopOrReturnCondition: recheck a case when its result inputs or window change; reidentify the structure when its selected basis changes
forbiddenOverread?: displayed order as performed Work, or an available branch as authorization
constraintGovernedProfileBasis:
  locusBindingRows[]:
    - <DesignReviewAlternatives@DR-27, candidate, design under review, DesignCandidate-A>
    - <DesignReviewAlternatives@DR-27, repair-proposal, proposed repair, RepairProposal-A>
    - <DesignReviewAlternatives@DR-27, accept, accept continuation, AcceptCandidate-Continuation>
    - <DesignReviewAlternatives@DR-27, repair, repair continuation, RepairCandidate-Continuation>
  potentialContinuationRows[]:
    - AcceptCandidate-Continuation, constrained by AcceptIfBothChecksSatisfied
    - RepairCandidate-Continuation, constrained by RepairIfAnyCheckViolatedAndProposalTargetsCandidate
caseBasis:
  checkResultRefs: [ThermalCheckResult-A, ServiceCheckResult-A]
  resultAboutCandidateOccurrences:
    - <ThermalCheckAboutCandidate@DR-27, CheckResultAboutDesignCandidatePredicate, [ThermalCheckResult-A, DesignCandidate-A]>
    - <ServiceCheckAboutCandidate@DR-27, CheckResultAboutDesignCandidatePredicate, [ServiceCheckResult-A, DesignCandidate-A]>
continuationJudgements[]:
  - candidate: AcceptCandidate-Continuation
    basisKind: conditionEvaluation
    predicateOrTest: AcceptIfBothChecksSatisfied
    applicability: both named results concern DesignCandidate-A
    caseInputs: [ThermalCheckResult-A, ServiceCheckResult-A]
    currentFacts: [thermal violated, service satisfied]
    requiredPolarity: both satisfied
    observedOutcome: notSatisfied
    dependentOccurrences: [ThermalCheckAboutCandidate@DR-27, ServiceCheckAboutCandidate@DR-27]
    window: ReviewWindow-DR-27
    result: disabled
    reason: thermal check is violated
  - candidate: RepairCandidate-Continuation
    basisKind: conditionEvaluation
    predicateOrTest: RepairIfAnyCheckViolatedAndProposalTargetsCandidate
    applicability: the proposal concerns DesignCandidate-A
    caseInputs: [ThermalCheckResult-A, ServiceCheckResult-A, RepairProposal-A]
    currentFacts: [thermal violated, service satisfied, RepairProposalTargetsCandidate@DR-27 obtains]
    requiredPolarity: at least one violation and the targeting relation obtains
    observedOutcome: satisfied
    dependentOccurrences: [ThermalCheckAboutCandidate@DR-27, ServiceCheckAboutCandidate@DR-27, RepairProposalTargetsCandidate@DR-27]
    window: ReviewWindow-DR-27
    result: enabled
    reason: one check is violated and the repair proposal concerns this design
currentContinuationSet: enabled [RepairCandidate-Continuation]; disabled [AcceptCandidate-Continuation]; unknown []; error []
stopOrNextAction: show repair as available; recheck when the case results or window change
```

The structure has two potential continuations although this case enables only repair. The selected proposal-to-design relation belongs to its identity basis. Thermal and service result epistemes, and their about-candidate relations, belong to the current case basis; they are not constituents or selected relation occurrences of this structure.

If the proposal-to-design relation cannot be established, this exact formal structure claim remains provisional. The ordinary explanation can still report repair as unknown. Do not treat an unknown identity-bearing relation as an established constituent of a qualified CGUS.

A later passing thermal check is a different result episteme and supplies a new case input. With service still satisfied, acceptance becomes enabled and repair becomes disabled. The selected design, proposal, continuation candidates, proposal-to-design relation, constraints, use frame, loci and potential topology are unchanged, so the same CGUS remains available for that new case.

### A.22.CGUS:5.1 - A missing intermediate capability changes the continuation {#a-missing-intermediate-capability-changes-the-continuation}

In this constructed learning case, a dancer has the strength and static axis control needed by a figure and can recall its sequence. The known limitation is maintaining balance during its required rotation. The figure's continuation depends on that coordinated performance, not just on adequate strength and memory.

| Alternative | Relevant conditions in this case | Present result |
| --- | --- | --- |
| Perform the complete figure under its intended conditions. | The required balance during rotation cannot yet be sustained. | Unavailable for the intended performance; naming the figure or its steps does not remove the gap. |
| Practise the rotational coordination under a suitable reduced demand. | A domain-appropriate exercise, suitable space and the needed support are available in the stipulated case. | Available as practice of the intermediate performance. It does not establish ability to perform the full figure. |

During the rotation, balance coordination would constitute part of turning; that turn would constitute part of the figure. These are connections through current performance, not three successive tasks. The practice alternative can exercise the first connection without already performing the intended figure.

When the coordination can be sustained, return to the encompassing figure and vary the relevant conditions before drawing a broader capability conclusion. The case condition and its continuation judgement can change without changing the potential alternatives. The subject's training Method supplies the exercise and assessment; CGUS makes their effect on the available continuation explicit.

## A.22.CGUS:6 - Bias-Annotation {#bias-annotation}

| Bias risk | Mitigation |
| --- | --- |
| Workflow bias | Ask about alternatives and conditions; use work and method patterns only for actual work-order or way-of-doing claims. |
| Display bias | Treat cards, graphs, tables, narratives, and entry lines as explanations or descriptions, not as the structure. |
| Formality bias | Start with the ordinary decision answer and open formal qualification only for a named later use. |
| Consumer bias | Keep transformation-flow, architecture, improvement, currentness, evidence, and publication details in their direct patterns. |
| Lexical bias | Words such as *route*, *path*, *loop*, *workflow*, *graph*, or *sequence* establish no CGUS by themselves. |

## A.22.CGUS:8 - Common Anti-Patterns And Repairs {#common-anti-patterns-and-repairs}

| Anti-pattern | Symptom | Repair |
| --- | --- | --- |
| **Pretty route as ontology** | A card or graph is treated as the structure. | Keep it as an explanation; qualify the structure independently. |
| **Condition label as result** | A label or claim reference is treated as proof that a continuation is enabled. | Apply the test or recover the obtaining relation and facts; otherwise return `unknown`. |
| **One enabled branch as one-branch structure** | The present result erases other potential continuations. | Keep potential topology and the case result separate. |
| **Formal package or field count first** | A simple correction requires replay fields, or authors add references merely to raise schema completion. | Use the ordinary branch and stop when it answers the question. In formal use, retain only fields consumed by qualification or replay and test whether readers recover the right alternatives and smallest repair. |
| **Displayed order as Work** | A teaching slice becomes a project procedure or authorization. | Use the applicable Method, work-plan, or Work pattern for work order, A.21 for an actual gate decision, and the direct permission or authority rule for authorization, only when that claim is actually made. |
| **Consumer architecture copied inward** | CGUS repeats transformation-flow locators, naming procedures, or catalogs of neighboring claims. | Keep the local structural rule and exit directly to the pattern that defines or tests the other claim. |

## A.22.CGUS:10 - Rationale {#rationale}

The recurring object is a thin specialization of A.22 `U.Structure`, not a new root kind. Constraint-based process modeling, object-centric querying, artifact-centric modeling, acausal modeling, and FPF pattern use all distinguish a constraint-bearing structure from a performed trace, work order, view, publication, solver run, or example path.

The same distinction appears in acausal engineering models: component relations and constraints can be stated before an analysis chooses a calculation direction. FPF adopts only that general separation. Mathematical models, analyses, executions, results, and publications keep their own kinds and rules.

## A.22.CGUS:11 - SoTA-Echoing {#sota-echoing}

| Source or practice anchor | FPF adoption | Boundary |
| --- | --- | --- |
| Aaron Küsters and Wil M.P. van der Aalst, [“OCPQ: Object-Centric Process Querying & Constraints”](https://arxiv.org/abs/2506.11541), 2025 | Current research comparator for typed objects, joins, many-to-many dependencies, and relation-preserving constraint queries. | A query or result is not the CGUS. |
| JuliaHub, Dyad 3.2 component and analysis documentation, 2026 | Current engineering comparator for reusable relation-first components separated from analyses and their solution objects. | FPF imports neither Dyad ontology nor its tools. Modelica 3.7 is retained only as historical acausal-modeling lineage. |
| Declare/MP-Declare, DCR, artifact-centric/GSM, and CMMN work | Lineage for declarative constraints, live alternatives, stages, guards, and weakly structured case work. | These are not current authority for a universal FPF process calculus; their notation and workflow ontology are not imported. |
| FPF pattern-language practice | Ordinary explanations may precede qualification; descriptions and demonstrative slices may follow it. | An entry card, example, or publication is neither admission evidence nor the specification. |

As of 2026-08-04, OCPQ and Dyad are the current comparators used here. Modelica, Declare, DCR, artifact-centric/GSM, and CMMN remain lineage where their distinctions are useful. Reopen this choice when a newer object-centric constraint method or relation-first engineering language changes the treatment of objects, relations, analyses, or live alternatives.


## A.22.CGUS:End {#end}
