# C.31.RSA - Reusable Structure Accounting {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Characterization pattern
> **Status:** Stable
> **Normativity:** Normative unless explicitly marked informative

## C.31.RSA:1 - Problem frame {#problem-frame}

Use this pattern when a practitioner needs to locate where reusable structure lives, where bespoke residue grows, which accounting basis is being used, what can be refactored, and what remains a bounded exception or source-return condition. A report-only share supports a separate use only when that use meets the conditions defined by its applicable pattern.

Claim-use boundary: any use that relies on the RSA account to make a claim beyond reusable-structure accounting is outside RSA. Examples include comparison, publication, evidence validity, assurance or safety-case reliance, gate use, architecture scale preference, causal use, selected-set result declaration, candidate synthesis, and local decision. Record with C.31.RSA only the reusable locus, bespoke residue, accounting basis, report-only share, repair direction, and source-return condition. Add another claim only after naming and applying the pattern that defines and tests it.

The first useful move is `ReusableStructureTriage`:

```text
ReusableStructureTriage:
  describedHolonRef:
  reuseQuestion:
  deploymentBoundary?:
  intendedAccountingUse:
  claimScopeRef?: U.ClaimScope
  qualificationWindowRef?:
  architectureClaimRef?:
  structureRefs:
  structuralAspectRefs?:
  accountingRelationRefs:
  evidenceRefs:
  whereReusableStructureCurrentlyLives:
  whereBespokeResidueCurrentlyGrows:
  residueRefactoredInto:
    template | interfaceSpecification | methodDescription |
    workStructure | evidencePackage | assuranceArgumentStructure | otherDeclared
  residueAcceptedAsBoundedException:
  sourceReturnCondition?:
  relatedClaimPatternsIfClaimed:
  stopCondition:
```

Use the fuller accounting description only when an accounting basis and structure references are declared. Ordinary use stops when the practitioner knows where reusable structure lives, where bespoke residue grows, what can be refactored, and what remains a bounded exception.

What goes wrong if C.31.RSA is missed: a reusable share is treated as a proof of modularity; one-off work is hidden under a reuse label; evidence reuse is counted without validity context; hidden residual uncertainty is averaged with reusable templates; and "more reusable structure" is treated as always better.

What C.31.RSA buys in practice: the practitioner can state where structure is reusable, where it is bespoke, what source-side distinctions must remain reachable, and when the result is only report-only accounting.

Not this pattern when the question under repair is source-label recovery, module-interface relation repair, modularity-characteristic selection, measurement or comparability admissibility, architecture scale preference, mathematical-lens use, or any outside-RSA use named above. Use `C.30.STRAT`, `A.6.M`, `C.31`, `C.16`, `A.10`, `B.3`, `G.6`, `C.31.ASAP`, `C.29`, `G.5`, or `C.11` as appropriate; do not treat C.31.RSA as the synthesis or selector pattern.

## C.31.RSA:2 - Problem {#problem}

Architecture teams often say that structure is reusable, repeated, templated, common, standardized, or bespoke. Those phrases are useful, but they do not say what is being counted, described, or compared. Structure can be selected from functions, flows, control relations, module interfaces, work methods, evidence packages, regulatory arguments, data schemas, deployment constraints, or exception networks.

Functional, flow, control, module-interface, work, evidence, and assurance structures may be included only under their declared `accountingBasisRef`. Name any evidence, assurance, or source relation being claimed by value, and state any source-return condition relied on by the account.

The practical question is: which reusable loci matter, which bespoke residue remains, what source distinctions are lost by accounting, and what repair or source return follows?

## C.31.RSA:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Reuse visibility vs false proof | Reusable loci should be visible, but a share is not proof of quality, assurance, or architecture adequacy. |
| Accounting convenience vs heterogeneous structure | Templates, interface grammars, work methods, and evidence packages do not automatically share one unit. |
| Residue repair vs useful exception | Some bespoke residue should be refactored; some should remain a bounded exception. |
| Compression vs source return | Accounting can summarize structure, but downstream action may require return to source-side records. |
| Local triage vs cross-case comparison | A local report-only share can guide repair; comparison needs declared scale, unit interpretation, admissible comparability relation, and comparator admission named by value. |
| Reuse value vs reuse cost | More reusable structure can increase interface cost, evidence decay, or loss of needed variation. |

## C.31.RSA:4 - Solution {#solution}

C.31.RSA governs reusable-structure accounting as a typed description over declared structures and structural aspects. It starts with `ReusableStructureTriage`; it uses `ReusableStructureAccountingDescription@Context` only when the accounting basis is declared.

### C.31.RSA:4.1 - Typed accounting description {#typed-accounting-description}

```text
ReusableStructureAccountingDescription@Context:
  accountingBasisRef:
  structureRefs: FinSet(U.StructureRef)
  structuralAspectRefs: FinSet(StructuralAspectDescriptionRef)
  reusableStructureSlots:
  bespokeResidueSlots:
  hiddenOrResidualUncertaintySlots:
  slotBasisRefs?:
  admissibleAggregationRuleRef?:
  reportOnlyShares?:
  sourceReturnCondition?:
  admissibleUse:
  nonAdmissibleUse:
```

`accountingBasisRef` identifies the accounting rule. The rule may concern description length, dependency edges, work items, evidence package count, cost share, template instances, interface variants, regulatory case sections, or another declared basis. The accounting rule is not implied by the word "reuse".

Well-formedness: every slot is over declared `structureRefs`, declared `structuralAspectRefs`, and one declared accounting basis. Slot labels are explanatory; they are not root kinds and are not automatically commensurable.

### C.31.RSA:4.2 - Explanatory slot labels {#explanatory-slot-labels}

A local accounting description may use explanatory slot labels such as:

```text
S_function
S_flow
S_control
S_type
S_interface
S_scale
S_work
S_evidence
S_changePolicy
S_unique
S_crossScopeUnique
H_residual
```

These labels are local slots, not FPF ontology. `H_residual` is residual uncertainty or unmodelled variance under the accounting basis. Its value is not automatically commensurable with counts or other measures of interface grammars, work templates, evidence packages, or regulatory arguments.

### C.31.RSA:4.3 - Report-only shares {#report-only-shares}

```text
ReusableStructureShare:
  report-only share over declared structureRefs and structuralAspectRefs
  under accountingBasisRef; not an architecture amount

BespokeResidueShare:
  report-only share under accountingBasisRef

HiddenOrResidualShare:
  report-only uncertainty or residue interpretation under accountingBasisRef
```

Numeric shares require a declared `accountingBasisRef`, declared scale or unitless-value rule, unit when relevant, polarity when relevant, admissible comparability relation, and comparator admission named by value such as `CG-Spec`, `ComparatorSetRef`, or a comparator-governing reference named by value before they can guide outside-RSA use such as comparison, ranking, selection, gate use, or decision use. Without that, the share remains local report-only guidance.

### C.31.RSA:4.4 - Pseudo-sum boundary {#pseudo-sum-boundary}

An explanatory decomposition may be useful:

```text
total-described-structure under accountingBasisRef:
  reusable slots
  bespoke residue slots
  hidden or residual uncertainty slots
```

This is a readable decomposition of one declared accounting description, not an equation defining an architecture amount. If the slots do not share a declared accounting basis and comparability rule, they cannot be summed or ranked.

### C.31.RSA:4.5 - Structure-relocation actions {#structure-relocation-actions}

RSA is useful because it points to relocation and repair actions:

| Situation | Repair direction |
| --- | --- |
| Repeated delivery work contains structure that is not explicit in the work or method description being used. | Move repeated structure into `MethodDescription`, work structure, or reusable work relation. |
| Repeated interface exceptions are handled one by one. | Add or revise interface grammar, variability slots, or substitution policy; use A.6.M when this is a module-interface claim. |
| An undocumented dependency crosses module or view boundaries. | Expose the dependency, revise boundary, add correspondence, or add source-return condition. |
| Evidence is recreated for each instance. | Move repeatable evidence into an evidence package, assurance argument record, or validity-context note. |
| Regulatory or safety-case residue remains one-off. | Split reusable argument structure from context-specific exception; apply B.3 to the assurance claim, including a claim about safety-case support, and G.6 when a citable provenance path is needed. |
| Compression hides needed distinctions. | Reduce compression, add source-return condition, or apply C.29 for lens-governed compression or reduction claims. |
| Bespoke residue protects necessary local variation. | Keep it as a bounded exception with admissible use and non-admissible use. |

A high reusable-structure share is not always good. The architecture question is where structure lives—for example, in reusable templates, interfaces, flows, control relations, work methods, evidence packages, or unique exception networks and hidden coupling—and what action follows.

After a relocation or reuse move, ask what got worse:

| Reuse move may improve | Check what may worsen |
| --- | --- |
| Template reuse | Loss of needed variation, hidden local exception, or stale source-return condition. |
| Interface grammar | Interface relation cost, conformance work, change cost, migration cost, or substitution constraint. |
| Work-method reuse | Context mismatch, extra handoff cost, slower local response, or hidden work exception. |
| Evidence-package reuse | Evidence decay, validity-window mismatch, missing context witness, or assurance overread. |
| Assurance-argument reuse | Weakest-link dependency, certification-window mismatch, or unexamined regulatory exception. |
| Compression or lens-backed accounting | Lost source distinction, observer-budget dependency, or C.29 stop-condition breach. |
| Bespoke-residue reduction | Reduced resilience, local-fit loss, or new hidden coupling. |

A conforming RSA move states the reusable locus, the bespoke or residual locus, the accounting basis, the first repair direction, and the first cost, loss, or source-return condition that can make the move inadmissible.

### C.31.RSA:4.6 - Triage and accounting use boundary {#triage-and-accounting-use-boundary}

Use only `ReusableStructureTriage` when:

- there is one local case;
- no outside-RSA use is being made;
- the practitioner only needs a repair direction;
- no numeric share is being relied on.

Use `ReusableStructureAccountingDescription@Context` when:

- the accounting basis is declared;
- a report-only share is useful;
- structure refs or structural aspects need to be compared inside one declared `accountingBasisRef`;
- source-return conditions matter;
- reusable structure or bespoke residue is used for outside-RSA use such as cross-case report, publication, assurance, architecture scale preference, or decision.

### C.31.RSA:4.7 - Reopen and lowering conditions {#reopen-and-lowering-conditions}

An RSA result remains valid only inside its declared accounting basis, structure edition, source-return condition, and comparator admission. Reopen the triage or lower the admissible use when any of the following changes:

- a hidden source distinction becomes action-relevant;
- the accounting basis changes or proves heterogeneous;
- the selected structure, structural aspect, interface grammar, evidence package, work method, or assurance argument changes edition;
- a comparator set, CG-Spec, or outside-RSA use is added after a report-only share was recorded;
- downstream reliance uses the RSA result for outside-RSA evidence, assurance, gate, causal-use, scale-preference, or decision work that the RSA note did not admit;
- evidence validity, assurance window, or source-return condition decays;
- a local bounded exception becomes repeated enough to require refactoring;
- a reuse move improves one locus while worsening interface cost, variation loss, evidence decay, assurance work, source-return cost, or hidden bespoke residue.

Lower the result to report-only when outside-RSA comparison, ranking, selection, gate use, or decision use lacks comparator admission named by value. Lower it to quote-only or source cue when the accounting basis cannot be recovered. Mark it blocked when the reusable locus and bespoke-residue locus cannot be separated.

## C.31.RSA:7 - Conformance Checklist {#conformance-checklist}

| ID | Check |
| --- | --- |
| `CC-C31.RSA-1` | @fact:CC-C31-RSA-1 The text starts from `ReusableStructureTriage` unless an accounting basis and structure refs are already named. @status:spec/done |
| `CC-C31.RSA-2` | @fact:CC-C31-RSA-2 Any accounting description names `accountingBasisRef`, `structureRefs`, `structuralAspectRefs`, reusable slots, bespoke residue slots, residual uncertainty slots, admissible use, and non-admissible use. @status:spec/done |
| `CC-C31.RSA-3` | @fact:CC-C31-RSA-3 Report-only shares are marked report-only unless every outside-RSA use being made and named in the claim-use boundary meets the conditions defined by its applicable pattern. @status:spec/done |
| `CC-C31.RSA-4` | @fact:CC-C31-RSA-4 No text treats RSA as proof of modularity, quality, or any outside-RSA use named in the claim-use boundary. @status:spec/done |
| `CC-C31.RSA-5` | @fact:CC-C31-RSA-5 Heterogeneous slot labels are not summed unless a declared accounting basis and aggregation rule make the operation admissible. @status:spec/done |
| `CC-C31.RSA-6` | @fact:CC-C31-RSA-6 Each bespoke residue interpretation states a repair direction, bounded-exception condition, source-return condition, or governing-pattern application. @status:spec/done |
| `CC-C31.RSA-7` | @fact:CC-C31-RSA-7 For an evidence-validity claim, use `A.10` to recover its source-to-use basis and `G.6` when a citable provenance path is needed; use `B.3` for an assurance claim, including one about safety-case support. @status:spec/done |
| `CC-C31.RSA-8` | @fact:CC-C31-RSA-8 RSA does not duplicate the C.31 characteristic taxonomy; it uses C.31 only when a modularity characteristic under evaluation, such as bespoke residue, evidence reuse, or residual uncertainty, must govern the accounting interpretation. @status:spec/done |
| `CC-C31.RSA-9` | @fact:CC-C31-RSA-9 Source-return condition is present when accounting hides action-relevant source distinctions. @status:spec/done |
| `CC-C31.RSA-10` | @fact:CC-C31-RSA-10 Outside-RSA comparison, ranking, selection, gate use, or decision use names comparator admission named by value such as `CG-Spec`, `ComparatorSetRef`, or a comparator-governing reference named by value; otherwise the RSA share remains report-only. @status:spec/done |
| `CC-C31.RSA-11` | @fact:CC-C31-RSA-11 The RSA note names reopen or lowering conditions for source distinction change, accounting-basis change, structure-edition change, implicit-interface change, comparator change, evidence or assurance decay, downstream reliance, repeated bounded exception, and reuse move side effects when those conditions are needed for the record. @status:spec/done |
| `CC-C31.RSA-12` | @fact:CC-C31-RSA-12 Source labels such as block, layer, expert, cache, router, gate, or pruning mask use `C.30.STRAT` before they become `structureRefs`, `structuralAspectRefs`, accounting-basis fields, repair actions, or source-return conditions. @status:spec/done |

## C.31.RSA:9 - Consequences {#consequences}

Benefits:

- Reusable structure and bespoke residue become visible without a false architecture amount.
- Practitioners get a cheap triage before accounting.
- Report-only shares can guide repair without becoming proof.
- Evidence reuse, work repeatability, interface grammar, and bounded exceptions can be separated instead of averaged.

Costs:

- Some attractive reuse reports remain report-only.
- Numeric shares require declared `accountingBasisRef`, declared scale or unitless-value rule, relevant unit and polarity, admissible comparability relation, and comparator admission named by value before they can guide outside-RSA comparison, ranking, selection, gate, or decision use.
- The pattern raises a source-return question whenever accounting hides distinctions needed by downstream action.

## C.31.RSA:12 - Relations {#relations}

| Pattern | Relation |
| --- | --- |
| `C.30.STRAT` | Recovers source labels such as layer, level, tier, stack, block, expert, cache, router, gate, and pruning mask before RSA uses recovered reusable loci, bespoke-residue loci, accounting-basis fields, repair actions, or source-return conditions. |
| `C.31` | Supplies modularity characteristics under evaluation; RSA does not duplicate the characteristic taxonomy. |
| `A.6.M` | Supplies module-interface claim repair when reusable interface or platform-grammar wording carries such a claim. |
| `C.30`, `C.30.AD`, and `C.30.ASV` | Supply architecture-claim, architecture-description-use, and structural-view context, respectively, for the structures being accounted over. |
| `C.16`, `A.17`, `A.18`, `A.19`, `A.19.CPM` | When RSA shares are used beyond report-only, use C.16 for measurement construction, A.17 for Characteristics, A.18 for scale, unit, and operation legality, including any score used; A.19 for a CharacteristicSpace or reusable space predicate when current; and A.19.CPM for comparison of admitted profiles under a declared comparator. |
| `C.25` | Governs broader quality-family bundles when reusable structure is used in a quality claim. |
| `A.10`, `B.3`, `G.6` | A.10 recovers sources and bounded reliance; G.6 makes an established provenance path citable; B.3 governs assurance claims, including claims about safety-case support. |
| `C.29` | Governs compression, epiplexity, RG, or other mathematical-lens claims when accounting depends on a lens. |
| `C.27`, `C.28`, `C.31.ASAP`, `C.18.1`, `C.19.1` | For claims arising from residue growth or reuse movement, use C.27 for temporal-claim adequacy, C.28 for causal use, C.31.ASAP for architecture alternatives under a declared scale variable and window, C.18.1 for scaling-law lens binding, and C.19.1 for scale-based preference or declared generality policy; a generality preference for architecture structure remains a declared local analogy or policy. |
| `C.32.P2S` | RSA rows may supply reusable structure, bespoke residue, evidence reuse, or source-return pressure to an architecturing flow. Candidate synthesis, selected-set result declaration, and architecture decisions remain outside RSA. |
| `G.5`, `E.17`, `E.24.PUB`, `C.11` | Use `G.5` for selected-set result declaration, `E.17` for a source-backed publication face and source return, `E.24.PUB` for the publication occurrence and audience availability, and `C.11` for local decision. Candidate synthesis stays with `C.32`; RSA defines or tests none of these uses. |


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/C-31#root, spec://ai.lev/fpf-spec/contract/C-30#root, spec://ai.lev/fpf-spec/contract/C-30-ASV#root, spec://ai.lev/fpf-spec/contract/C-16#root, spec://ai.lev/fpf-spec/contract/A-19#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/A-6-M#root, spec://ai.lev/fpf-spec/contract/C-31-ASAP#root, spec://ai.lev/fpf-spec/contract/C-29#root, spec://ai.lev/fpf-spec/contract/A-10#root, spec://ai.lev/fpf-spec/contract/B-3#root, spec://ai.lev/fpf-spec/contract/G-6#root, spec://ai.lev/fpf-spec/contract/C-27#root, spec://ai.lev/fpf-spec/contract/C-28#root, spec://ai.lev/fpf-spec/contract/G-5#root, spec://ai.lev/fpf-spec/contract/C-11#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-6-M#root, spec://ai.lev/fpf-spec/contract/C-31#root, spec://ai.lev/fpf-spec/contract/C-31-ASAP#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/C-31-RSA
