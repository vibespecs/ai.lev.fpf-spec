# A.22.CGUS - Which Continuations Are Available? — Constraint-Governed Unfolding Structure (CGUS) {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** A.22 specialization of `U.Structure`
> **Status:** Stable
> **Normativity:** Normative unless explicitly marked informative

## A.22.CGUS:0 - Use This When {#use-this-when}

Use this pattern when a diagram or explanation shows several possible next actions, but readers may mistake one displayed path for the required work sequence. Start with one ordinary question:

> Which alternatives are available now, and what condition blocks each one?

Name the decision or question, the visible alternatives, the condition for each alternative, and the facts available now. If a needed fact or rule is missing, mark that alternative `unknown` and stop when this answers the practical question. A useful explanation need not first become a formal record or an admitted structure.

Open the formal branch only when the team must qualify, persist, compare, publish, or rely more strongly on the structure. A `ConstraintGovernedUnfoldingStructure` (CGUS) is one A.22 `U.Structure` whose locally named loci, constituents, obtaining relations, and constraints define at least two potential continuations across the cases allowed by those constraints. A separate result says which alternatives are enabled, disabled, unknown, or error for one case and time window.

Do not use CGUS merely because a card, graph, table, narrative, prompt path, or README line looks route-shaped. A single recommendation or displayed sequence is not enough. The structure may branch, join, cycle through subject relations, remain partially ordered, or leave several alternatives live at once. A result with zero or one enabled alternative can still concern that same branching structure.

**What changes in practice.** Practitioners correct the visible alternatives and their conditions before completing formal fields. They keep potential structure separate from the result for the present case, and they mark an affected alternative `unknown` at its first unresolved fact or rule instead of inventing a continuation. Display order alone neither prescribes nor performs Work.

## A.22.CGUS:1 - Problem Frame {#problem-frame}

FPF often needs to explain how several identified things and relations constrain what may follow without turning that explanation into a workflow. The shared object is one A.22 structure. CGUS adds local loci and a membership test for potential branching; a continuation judgement then evaluates one case.

Descriptions, publication forms, evidence, assurance, authorization, work plans, performed Work, architecture claims, and mathematical models can be used alongside that structure. They remain separate objects and claims under the patterns that define or test them.

## A.22.CGUS:2 - Problem {#problem}

A route-shaped explanation can hide the relations and constraints that make an alternative available. Readers then follow the displayed order as if it were a required procedure, or they treat a condition label as proof that the condition is true now.

The opposite repair is also harmful: authors replace the simple decision question with a large admission, replay, publication, and assurance package. The formal package becomes harder to use than the misleading card it was meant to correct.

## A.22.CGUS:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Useful explanation vs workflow overread | A visible path helps a reader, but actual Work may be nonlinear, interrupted, iterative, or arranged by another Method or plan. |
| Potential structure vs present result | The structure can retain several possible branches while the present case enables none, one, or several. |
| Plain entry vs formal replay | An ordinary correction should be cheap; qualification and replay still need enough identity and relation detail to be checked later. |
| Description vs described structure | A card, graph, table, or narrative can describe a structure without creating it. |
| Reuse vs copied mini-patterns | CGUS needs direct exits to relation, transformation-flow, work, publication, and assurance patterns without copying their architectures. |

## A.22.CGUS:4 - Solution {#solution}

### A.22.CGUS:4.1 - Ordinary branch {#ordinary-branch}

Write the smallest useful answer in domain language:

1. name the decision or question;
2. list the real alternatives;
3. state the condition for each alternative;
4. state the facts known for this case;
5. mark each alternative `available`, `blocked`, or `unknown`, and name the first missing fact or rule.

For example, a design review has two alternatives: accept the design or repair it. Acceptance needs both checks to pass. Repair needs at least one failed check and a repair proposal that concerns this design.

| Alternative | Present facts | Result shown on the card |
| --- | --- | --- |
| Accept the design | Thermal check failed; service check passed. | `blocked — thermal check failed` |
| Repair the design | A check failed and a repair proposal exists, but the proposal-to-design relation has not been established. | `unknown — proposal target not established` |

That corrected card is already useful. It keeps both potential alternatives visible and refuses to invent the missing relation. Continue only if a named later use needs formal structure identity or replayable results.

#### A.22.CGUS:4.1.1 - Conditions through constituent and encompassing work {#conditions-through-constituent-and-encompassing-work}

When a continuation is a way of performing work, recover the part of its Method/Work vertical that can change availability. Ask what constituent actions must be performable and what encompassing work is being done through them. B.1.5.EW supplies that recovery; knowing a Method's description does not supply the capability or resources to perform it.

Distinguish conditions needed at entry, conditions that must remain satisfied during combined performance, and the result required by the encompassing use. In particular:

- a constituent may be individually performable but fail in the needed coordination;
- adequate local resources may be insufficient when constituents share them;
- a constituent result may satisfy its own postcondition while leaving the whole's result unresolved.

For each relevant condition, state what it concerns and how it affects this continuation. Reuse an understood connection or adequate existing basis. A missing condition blocks or leaves unknown the dependent alternative; it need not block an independent way to learn, obtain support or change the arrangement. Capability belongs to its performer and conditions under A.2.2; prospective resources and support remain prospective until available.

In the formal branch, express these dependencies with the existing constituents, selected relations, applied constraints and continuation judgements. A temporal edge alone cannot express that one action constitutes part of another ongoing work. Nor does a nested flow position establish Method or Work parthood. A diagram may show the relations together when their meanings remain recoverable.

A constituent's postcondition supports the encompassing conclusion only through the relevant composition and result-use conditions. An expected postcondition is not an observed result. If the displayed account omits conditions needed to perform the whole, state the narrower question it answers. A constituent hierarchy without potential alternatives does not require CGUS qualification.

### A.22.CGUS:4.2 - Formal qualification branch {#formal-qualification-branch}

Use the four A.22 discriminators to identify one `U.Structure`:

- its constituent references;
- the obtaining relation occurrences it selects;
- the applied constraint claims;
- the named selection-use frame: the question, admissible action, and stop or return condition. Any optional explanatory overread follows F.19:4 and remains outside the identity basis.

CGUS membership adds locally declared loci and bindings that expose how those constituents matter to the unfolding question. The selected relations and constraints must define at least two potential continuation candidates across allowed cases. The current continuation result, a description, or a publication field adds no structure-identity discriminator.

```text
selectedCGUSRef: one A.22 U.Structure
A22IdentityBasis:
  selectedConstituentRefs[]
  selectedObtainingRelationOccurrenceRefs[]
  appliedConstraintClaimRefs[]
  namedSelectionUseFrame:
    questionOrAction: exact selection question
    admissibleAction
    stopOrReturnCondition
forbiddenOverread?: optional explanation outside A22IdentityBasis
constraintGovernedProfileBasis:
  locusBindingRows[]:
    locusRef: <selectedCGUSRef, locusId>
    locusMeaning: why this constituent matters to this question
    selectedConstituentRef
  potentialContinuationRows[2..*]:
    continuationCandidateRef
    constrainingRelationOccurrenceRefs[]
    appliedConstraintClaimRefs[]
```

`forbiddenOverread?` and `groundedForbiddenOverread?` name the same optional explanation. Use F.19:4's plausible-reader test to decide whether it is useful here.

A CGUS locus belongs to this structure, not to a reusable relation declaration:

```text
CGUSLocusRef := <selectedCGUSRef, locusId>
CGUSLocusBinding := <selectedCGUSRef, locusId, locusMeaning, selectedConstituentRef>
```

The constituent must already belong to the A.22 identity basis. A locus binding neither changes that constituent's kind nor creates a relation. Do not use an A.6.5 `SlotSpec` as a free-standing structure position.

When replay must identify one participant in a relation occurrence, retain the direct relation definition, the occurrence, the participant order, and the participant binding:

```text
RelationParticipantLocator := <relationDefinitionRef, relationOccurrenceRef, participantOrder, participantRef, relationSignatureRef?, slotSpecRef?>
```

Add a `RelationSignature` and its declaration-local `SlotSpec` together only when an existing reusable declaration is itself needed for replay. Neither declaration value substitutes for the obtaining occurrence. The CGUS has no ambient context field.

Judge each continuation separately. An immediate local use may keep the following values in the explanation; persistence or replay may place them in an ordinary C.2.1 result episteme.
```text
ContinuationJudgementResult:
  selectedCGUSRef
  continuationCandidateRef
  basisRows[]:
    basisKind: conditionEvaluation | obtainingRelation
    conditionEvaluation?:
      conditionPredicateOrTestRef
      applicabilityResult
      caseInputRefs[]
      currentFactOrEvidenceRefs[]
      requiredPolarity
      observedOutcome: satisfied | notSatisfied | unknown | error
    obtainingRelation?:
      relationDefinitionRef
      relationOccurrenceRef
      participantRefsInPredicateOrder[]
      currentFactOrEvidenceRefs[]
    dependentSelectedRelationOccurrenceRefs[]
  qualificationWindow
  result: enabled | disabled | unknown | error
  reason

CurrentContinuationSetResult:
  selectedCGUSRef
  caseInputRefs[]
  qualificationWindow
  judgementResultRefs[]
  enabledContinuationCandidateRefs[]
  disabledContinuationCandidateRefs[]
  unknownContinuationCandidateRefs[]
  stopOrNextAction
  recheckConditions[]
```

A claim reference identifies the claim being applied; it does not show that the test applies or that its condition is satisfied. An obtaining relation is not a condition claim. Keep these two basis branches distinct and derive the case result only from completed judgements.

The membership test concerns potential topology. Changed facts, evidence, test outcomes, or time windows normally change a judgement and the current set, not the structure. Reidentify the A.22 structure when a constituent, selected obtaining relation occurrence, applied constraint, or named use frame changes. Reapply CGUS membership when a locus binding or potential-continuation row changes.

### A.22.CGUS:4.3 - Four separate decisions {#four-separate-decisions}

Do not turn qualification, case evaluation, description adequacy, and downstream reliance into one score.

| Decision | Passing basis | Honest lower result |
| --- | --- | --- |
| A.22 identity and CGUS membership | The four A.22 discriminators identify one structure; its local loci, relations, and constraints define at least two potential continuations across allowed cases. | Name the missing discriminator, binding, relation, constraint, or candidate. Keep the artifact as an explanation. |
| Continuation result for this case | Each candidate has an applicable test or obtaining-relation basis, case inputs, facts, required polarity, time window, and an `enabled`, `disabled`, `unknown`, or `error` result. | Mark the affected candidate unknown or stop on the missing value. Do not revoke an independently established structure. |
| Description or demonstrative-slice adequacy | The description says what it shows and omits for its declared use. Use C.33 only when a carrier's loss affects a declared architecture use within C.33's scope. | Narrow or correct the description. Missing publication or loss material does not deny the structure. |
| A stronger neighboring claim | The method, Work, evidence, assurance, gate, architecture, publication, currentness, or mathematical claim passes its own definition or test. | Stop only that stronger use and name its missing rule or basis. |

Potential branches and joins remain part of the structure even when the present case enables one or none. A linear teaching slice neither removes the other topology nor fixes the order of performed Work.

### A.22.CGUS:4.4 - Explanations, descriptions, and the non-workflow boundary {#explanations-descriptions-and-the-non-workflow-boundary}

Before qualification, an ordinary explanation is about the domain question or proposed alternatives. If persistence is needed, its C.2.1 `EntityOfConcern` remains that question or proposed set, not a CGUS that has not yet qualified.

After qualification, a whole-structure description may describe loci, bindings, relations, constraints, potential branches, case results, and relevant omissions. A separate demonstrative slice may show one traversal for a declared teaching or comparison use. That slice is a C.2.1 episteme: its exact claim content, the qualified CGUS as `EntityOfConcern`, and its effective `U.ReferenceScheme` jointly recover its identity. `DemonstrativeUnfoldingSlice@Context` is readable lineage for this possibility, not a `U.Kind` or an exact slice by itself. The slice neither creates nor reidentifies the structure. Use C.33 only when hidden or lost structure in its carrier matters to a declared architecture use within C.33's scope.

Where a slice shows one selected pattern use, it may recall the difficulty through the pattern's `Problem frame` or `Problem`, or recall the way of addressing it through the `Solution`. To show that same use in either form, preserve the selected pattern, working subject and question or proposed use, current conditions, expected result, stop or continuation, and relevant locus bindings. Changing between those formulations changes only the description when the selected pattern use and the qualified structure remain the same. A.22 structure identity still depends on its constituents, selected obtaining relations, applied constraints and named selection-use frame; CGUS membership additionally depends on its locus bindings and at least two potential continuations. Question or action labels establish neither.

Displayed words such as *move*, *next*, and *path* remain ordinary language unless a stronger claim requires another kind. A proposed action, a plan item, a `U.WorkPlan`, dated `U.Work`, and an actual `U.Transformation` are different values. Use `E.10.MOVE`, A.15, and A.3 only when that distinction changes the claim; a display performs and authorizes nothing.

For a transformation-flow use, apply `E.18.3`. It owns the choice among one TFS, one parent-relative `SubflowRef`, or an E.18.NET network and the corresponding position and demonstration locators. CGUS keeps only its local locus bindings and potential topology; it does not copy the network's members, positions, valuations, Work, transformations, or tags.

Cite another pattern only when its content supplies a needed definition, constraint, test, method, evidence rule, or assurance rule. For example, use C.30 for an architecture claim and C.32 for architecture-candidate synthesis, E.23 for repeated quality improvement under a declared evaluation, G.11 for source currentness, C.29 for a mathematical-lens claim, A.10 for claim-bound evidence reliance, or B.3 for an actual named assurance claim.

If a durable name or a relation between local senses is the question, use F.17, F.18, or F.9 after the value has been recovered. Do not copy their naming or Bridge procedures into this pattern. Entry cards and publication faces remain under E.11 and E.17.

### A.22.CGUS:4.5 - Replay and change localization {#replay-and-change-localization}

Replay structure identity from the four A.22 discriminators. Replay CGUS membership from the local locus bindings and potential topology. Replay the case result from each candidate's basis, inputs, facts, polarity, dependent occurrences, time window, outcome, and reason.

Localize change before reopening wider work. A changed constituent, selected occurrence, constraint, or use frame can reidentify the A.22 structure. A changed locus binding or potential-continuation row reopens CGUS membership. A changed fact, evidence item, test result, or time window normally reopens only the affected judgement and current set. A changed omission reopens the affected description use. A changed neighboring claim stays with the pattern that defines or tests it.

## A.22.CGUS:7 - Conformance Checklist {#conformance-checklist}

| ID | Passing condition | Failed-check repair |
| --- | --- | --- |
| **CC-CGUS-1 Identity and profile.** | @fact:CC-CGUS-1 The four A.22 discriminators identify one `U.Structure`; local locus bindings, relations, and constraints define at least two potential continuations across allowed cases. @status:spec/done | Recover the missing value or keep the artifact as an explanation. |
| **CC-CGUS-2 Local loci and relation participants.** | @fact:CC-CGUS-2 Every `CGUSLocusBinding` uses a locus declared inside this CGUS and binds one constituent for a stated meaning. A needed relation participant retains its definition, occurrence, order, and binding; `RelationSignature` and `SlotSpec` appear together only for declaration-level replay. @status:spec/done | Restore the locus or complete relation-participant basis. Never use a free-standing `SlotSpec` as a structure position. |
| **CC-CGUS-3 Explanation and description separation.** | @fact:CC-CGUS-3 An ordinary or persisted provisional explanation concerns the domain question or proposed alternatives. Post-qualification descriptions and slices concern the CGUS. None is the structure or a membership condition. @status:spec/done | Restore the right `EntityOfConcern` or keep the explanation ordinary. |
| **CC-CGUS-4 Current continuation result.** | @fact:CC-CGUS-4 Each judgement retains its test or obtaining-relation basis, applicability, inputs, facts, polarity, dependent occurrences, window, outcome, and reason. The enabled set may contain zero, one, or several alternatives. @status:spec/done | Mark the affected candidate unknown or stop on the missing value. |
| **CC-CGUS-5 Separate decisions.** | @fact:CC-CGUS-5 Identity and membership, case result, description adequacy, and each neighboring claim are judged separately. @status:spec/done | Reopen only the affected decision. |
| **CC-CGUS-6 Work-order boundary.** | @fact:CC-CGUS-6 The selected structure and display expose branches and conditions. @status:spec/done | Put any prescribed or performed Work order under the Method, work-plan, or Work pattern that establishes it. |
| **CC-CGUS-7 Graph-shaped coverage.** | @fact:CC-CGUS-7 Branches, joins, cycles, partial order, and live alternatives are preserved or explicitly omitted for the declared use. @status:spec/done | Keep a chain provisional or state what its demonstrative slice omits. |

## A.22.CGUS:9 - Consequences {#consequences}

CGUS preserves the usefulness of a route-shaped explanation without making it a workflow. Ordinary use is cheap: decision, alternatives, conditions, facts, honest result, and stop. Formal use costs more because structure identity, CGUS membership, the case result, and any description or neighboring claim must remain separately checkable.

This separation prevents a changed fact from reidentifying a stable structure and prevents a missing publication, evidence, or assurance value from erasing a useful ordinary answer.

## A.22.CGUS:12 - Relations {#relations}

Specializes: one A.22 `U.Structure` whose local locus bindings, obtaining relations, and constraints define at least two potential continuations across allowed cases. Continuation judgements, descriptions, slices, loss notes, and neighboring claims are separate results or uses.

Specialized by: `E.18.3` when the same structure also satisfies its transformation-flow condition. Local applications include architecture, abduction, improvement, narrative, grounding, currentness, and first-entry uses only when their own constituents, relations, constraints, and use frames are recoverable.

Coordinates with: `A.6.P` and A.6.5 for relation occurrence and reusable declaration precision; `E.18`, `E.18.NET`, and `E.18.3` for transformation-flow substrates; `A.3` and `A.15` for Method, plan, Work, and Transformation claims; `A.10` for claim-bound evidence reliance, `B.3` for an actual named assurance claim, `A.20` for internal-constraint validity, and `A.21` for gate decisions; `C.30` for architecture claims and C.32 for architecture-candidate synthesis; `E.23` for repeated quality improvement under a declared evaluation; `G.11` for currentness; `C.29` for mathematical-lens use; `C.33` for description loss that affects a declared architecture use; `E.11` for entry, `E.17` for a source-backed reader face, and `E.24.PUB` for publication occurrence, form, carrier, audience, bounded use, and availability; and `F.17`, `F.18`, and `F.9` for source-local sense, durable naming, and Bridge claims.

Does not replace any pattern that supplies the definition, constraint, test, method, evidence rule, or assurance rule for a neighboring claim.

Use `F.19` for ordinary precise-plain-language repair and the plausible-reader test for an optional explanatory overread.


## Dependencies {#dependencies}

- @fact:SPECIALIZES Specializes: spec://ai.lev/fpf-spec/contract/A-22#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/E-18-NET#root, spec://ai.lev/fpf-spec/contract/E-18-3#root, spec://ai.lev/fpf-spec/contract/E-18-1#root, spec://ai.lev/fpf-spec/contract/E-23#root, spec://ai.lev/fpf-spec/contract/C-32-P2S#root, spec://ai.lev/fpf-spec/contract/E-11#root, spec://ai.lev/fpf-spec/contract/F-17#root, spec://ai.lev/fpf-spec/contract/C-33#root, spec://ai.lev/fpf-spec/contract/C-35#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-1-STM#root, spec://ai.lev/fpf-spec/contract/A-22#root, spec://ai.lev/fpf-spec/contract/A-3-3-TR#root, spec://ai.lev/fpf-spec/contract/B-1-5-EW#root, spec://ai.lev/fpf-spec/contract/E-10-MOVE#root, spec://ai.lev/fpf-spec/contract/E-11#root, spec://ai.lev/fpf-spec/contract/E-18-3#root, spec://ai.lev/fpf-spec/contract/E-18-NET#root, spec://ai.lev/fpf-spec/contract/E-23#root, spec://ai.lev/fpf-spec/contract/F-17#root, spec://ai.lev/fpf-eng-me/contract/ME-20#root, spec://ai.lev/fpf-nstd/contract/NSTD-2#root, spec://ai.lev/fpf-eng-ops/contract/OPS-11-1#root, spec://ai.lev/fpf-eng-syse/contract/SYSE-20#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/A-22-CGUS
