# C.31.ASAP - Which Architecture Is Preferable Under Scale? (Scale Amenability) {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Characterization pattern
> **Status:** Stable
> **Normativity:** Normative unless explicitly marked informative

## C.31.ASAP:1 - Problem frame {#problem-frame}

Use this pattern when a practitioner compares architecture alternatives under a declared scale variable or scale window and needs to avoid treating a modularity label, platform label, product-line label, reusable-structure share, or coarse-graining metaphor as an automatic scale-preference claim.

The first useful move is `ScaleClaimTriage`:

```text
ScaleClaimTriage:
  architectureAlternativeSetRef:
  describedHolonRef:
  claimScopeRef:
  selectedContextSliceRefs:
  modelUseStructureRef?:
  scaleVariableRef:
  scaleWindowRef:
  claimedPreferenceUnderScale:
  slopeEvidenceRef, scaleProbeEvidenceRef, or noProbeReason:
  expectedStableOrImprovingStructure:
  exceptionGrowthRisk:
  sourceReturnCondition:
  relatedClaimGovernanceIfClaimed:
  stopCondition:
```

Ordinary use starts by naming the alternatives and described holon, the exact `U.ClaimScope` and relevant A.2.6 `U.ContextSlice` membership, the scale variable and scale window, the claimed preference under scale, the available slope or scale-probe evidence or no-probe reason, the expected stable or improving structure, and the exception-growth risk. Name `modelUseStructureRef` only when one independently selected `BoundedModelUseStructure` changes this receiving interpretation; it never replaces the claim scope. Use `ArchitectureScaleAuditRecord@Project` only when the scale preference is being used to affect a comparison, selected set, publication, assurance input, or architecture decision.

What goes wrong if C.31.ASAP is missed: "modular", "platform", "product line", "reusable", "general", "open", "coarse-grained", or "RG-like" becomes a shortcut for a scale-preference claim; a locally hand-engineered solution is called debt even when safety, law-domain, or mission constraints justify it; exception growth is hidden until the architecture is already expensive to change; and coarse descriptions keep losing lower-scope safety or semantic distinctions without a source-return condition.

What C.31.ASAP buys in practice: the practitioner can say what is being scaled, where the scale claim holds, what structure is expected to remain stable or improve, what exceptions are allowed, what evidence or no-probe reason exists, which scale-preference claim stays in C.31.ASAP, and which pattern defines or tests any lens-use, evidence, assurance, selection, or decision claim being made.

Not this pattern when the question under repair is only module-interface relation repair, modularity-characteristic selection, reusable-structure accounting, mathematical-lens use, scale-law adequacy, method preference under general BLP, candidate architecture generation, selected-set return, or final local choice. Use `A.6.M`, `C.31`, `C.31.RSA`, `C.29`, `C.18.1`, `C.19.1`, `C.32`, `G.5`, or `C.11` as appropriate. C.31.ASAP governs architecture scale-preference claims; it does not select the architecture, prove the scale law, or certify the project.

## C.31.ASAP:2 - Problem {#problem}

Architecture work often asks whether one structure will scale better than another: a product-line architecture rather than bespoke variants, an open interface rather than a closed integration, a stable flow topology rather than repeated project exceptions, or a reusable evidence package rather than repeated assurance work.

These claims are useful only after the scale relation is declared. "Scales better" can mean fewer interface grammar variants, lower exception growth, better learning transfer, more reusable templates, more stable control relations, less source-return cost, fewer regulatory exceptions, or more freedom of action. Those are not the same claim.

C.31.ASAP turns architecture scale-preference talk into a declared scale variable or window, a preference claim, evidence or no-probe reason, expected stable or improving structure, exception-growth risk, and source-return condition. It does not turn scale preference into proof, selection, assurance, causal use, or a universal law.

## C.31.ASAP:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Fast architecture choice vs scale evidence | Practitioners often need a scale-aware preference before a full scale study exists. |
| Reusable structure vs useful exception | Reuse can improve scale behavior, but some bespoke residue is justified by safety, law-domain, mission, or context constraints. |
| Platform label vs scale mechanism | A platform or product-line name does not say which variability slots, extension rules, exception curve, or refactor trigger makes scale behavior better. |
| Coarse view vs source distinctions | Coarse-grained architecture descriptions can expose stable structure, but they can also hide lower-scope hazards. |
| Preference guidance vs selection authority | A scale preference can inform a candidate set or decision, but selection and choice remain with their governing patterns. |
| Architecture scope vs method BLP | Architecture scale amenability resembles BLP, but C.31.ASAP governs architecture alternatives and selected structures, not general method-family policy. |

## C.31.ASAP:4 - Solution {#solution}

C.31.ASAP specializes scale-amenability preference for architecture alternatives. It applies when an architecture alternative set, scale variable or scale window, and claimed preference under scale are named.

### C.31.ASAP:4.1 - Applicability fields {#applicability-fields}

C.31.ASAP applies only when all of the following are present:

1. a declared architecture alternative set, described holon, exact `U.ClaimScope`, and relevant A.2.6 `U.ContextSlice` membership;
2. a declared scale variable or scale window;
3. a claimed preference under scale;
4. slope evidence, scale-probe evidence, or a no-probe reason;
5. an expected stable or improving structure, exception-growth risk, or source-return condition that changes the next architecture move.

If those fields are absent, keep the claim in `C.31` as a temporal or scale-sensitive characteristic cue, in `C.31.RSA` as report-only accounting, in `C.29` as a bounded lens-use output, or in ordinary architecture prose.

### C.31.ASAP:4.2 - `ScaleClaimTriage` {#scaleclaimtriage}

Use `ScaleClaimTriage` before any heavier scale audit:

```text
ScaleClaimTriage:
  architectureAlternativeSetRef:
  describedHolonRef:
  claimScopeRef:
  selectedContextSliceRefs:
  modelUseStructureRef?:
  architectureClaimRef?:
  scaleVariableRef:
  scaleWindowRef:
  claimedPreferenceUnderScale:
  slopeEvidenceRef?:
  scaleProbeEvidenceRef?:
  noProbeReason?:
  expectedStableOrImprovingStructure:
  exceptionGrowthRisk:
  sourceReturnCondition:
  admissibleUse:
  nonAdmissibleUse?:
  relatedClaimGovernanceIfClaimed:
  stopCondition:
```

The triage is complete enough when it states the next admissible architecture move and the stop or return condition. Include `nonAdmissibleUse?` only when it passes F.19's plausible-reader test; `groundedScaleShortcut?` is an alias for that same optional value. It may stop at local guidance when no comparison, publication, assurance, selected-set, or decision use is being made.

`claimScopeRef` designates one exact `U.ClaimScope`; `selectedContextSliceRefs` records the A.2.6 membership relevant to this use. A scale window is the range of the scale variable for which the preference is claimed, not a substitute for either scope object. `modelUseStructureRef` is optional and is filled only when an independently selected A.1.1 `BoundedModelUseStructure` changes the interpretation of this exact preference use.

### C.31.ASAP:4.3 - Architecture scale-preference rule {#architecture-scale-preference-rule}

When architecture alternatives satisfy the same safety boundary, law-domain boundary, and assurance boundary, prefer the alternative whose reusable functional-structure, flow-structure, control-structure, module-interface, work-template, and evidence-package structure and learning-transfer slopes remain stable or improve over the declared scale window, unless an `ArchitectureScaleAuditRecord@Project` records a bounded exception.

C.31.ASAP defines the scale-preference claim and its boundary. Use `G.9` for a parity claim and `A.21` for a gate claim; the candidate, comparison, set-declaration, and choice uses are distinguished below.

A scale-preference claim may inform `C.32` candidate generation or supply one input to an `A.19.CPM` comparison by naming the scale variable, scale window, expected stable or improving structure, exception-growth risk, and source-return condition for candidate alternatives. Use `C.32` to construct the candidate architecture palette, `A.19.CPM` to compare alternatives, `G.5` to declare a selected-set result, `C.11` to make a final local choice, and `C.32.PAD` to record a project architecture decision. When audience availability is current, use `E.17` for a source-backed publication face and return to source and `E.24.PUB` for the publication occurrence, form, carrier, audience, bounded use, and availability. Apply the relevant evidence, assurance, gate, or release definition and test only when that claim is current.

When the same scale-sensitive pressure must also become a project criterion, `C.32.ACS` creates a separate row for the exact characteristic or Q-Bundle slot, bearer, scale form, and use class. That row may supply declared input to an ASAP preference. Use C.31.ASAP to state which alternative is preferable under the scale window; use C.32.ACS to admit and classify the criterion row as an optimization indicator, guardrail, or context-only row. Keep the preference record and criterion row separately referenced.

### C.31.ASAP:4.4 - Scale variables {#scale-variables}

Typical architecture scale variables include:

| Scale variable | Reading |
| --- | --- |
| `N_units` | repeated units or instances |
| `N_scopeCount` | aggregation scopes, coarse-graining scopes, or typed LCA control scopes |
| `N_sites` | deployments, sites, markets, or jurisdictions |
| `N_interfaceTypes` | distinct interface grammar variants |
| `N_requiredTransformationKinds` | distinct transformation kinds in the selected functional-structure view |
| `N_flowRelationKinds` | flow-relation or crossing variants in the selected flow-structure view |
| `N_moduleTypes` | module type library size |
| `N_workRepetitions` | delivery, operation, or test repetitions |
| `N_supplierOrVendorClasses` | substitutability or vendor class dimension |
| `N_regulatoryInstances` | approval, safety, or certification repeats |
| `freedomOfAction` | allowed design, search, or control variation |

The scale variable is not enough by name. The claim being made also needs a scale window, expected stable or improving structure, exception-growth risk, and source-return condition.

### C.31.ASAP:4.5 - Scale audit outputs {#scale-audit-outputs}

Use the heavier audit only when the scale preference changes comparison, publication, selected-set, assurance-input, or decision use:

```text
ArchitectureScaleAuditRecord@Project:
  projectWorkOccurrenceRef?: U.EntityRef constrained to U.Work
  architectureScaleAuditProjectUseRelationRef?: U.RelationRef governed by the exact audit-use or work-use pattern
  architectureAlternativeSetRef:
  claimScopeRef:
  selectedContextSliceRefs:
  modelUseStructureRef?:
  scaleVariableRefs:
  scaleWindowRef:
  ArchitectureSlopeVector:
  IsoScaleParityNote?:
  ASAPWaiverReason?:
  ArchitectureHeuristicDebt?:
  BespokeResidueRegisterRef?:
  SourceReturnCondition:
  admissibleUse:
  nonAdmissibleUse?:
  relatedClaimGovernanceIfClaimed:
  stopCondition:
```

For `ArchitectureScaleAuditRecord@Project` and `BespokeResidueRegister@Project`, `@Project` is a compatibility and retrieval cue. An audit local to one actual project names both the exact composite `U.Work` in `projectWorkOccurrenceRef` and the obtaining direct audit-use relation in `architectureScaleAuditProjectUseRelationRef`. `BespokeResidueRegisterRef` may cite the register episteme. Assert that register's project locality only after a separate direct register-to-work relation is governed, and cite that exact occurrence; the audit-use relation remains about the audit. Otherwise retain only retrieval use and make no audit or residue-register project-locality claim.

| Output | Meaning |
| --- | --- |
| `ArchitectureSlopeVector` | Slopes for reusable structure, interface variation, flow stability, control stability, work repeatability, bespoke residue, exception growth, and learning transfer. |
| `IsoScaleParityNote` | Comparison under equalized scale budgets where possible; if parity is not possible, the loss is named. |
| `ASAPWaiverReason` | Declared reason for not choosing the scale-amenable alternative. |
| `ArchitectureHeuristicDebt` | Report-only note for knowingly accepting a locally hand-engineered solution with less scale-amenable slope profile under the declared scale window. |
| `BespokeResidueRegister@Project` | Pattern-local exception inventory with expiry or refactor triggers. |
| `ScaleWindow` | Declared range where the preference claim holds. |
| `SourceReturnCondition` | Condition for returning from a compressed, coarse, extracted, indexed, or accounting representation to source-side structural evidence, source records, or a related source or evidence record with higher declared validation boundary. |

`ArchitectureScaleAuditRecord@Project` records the triage of an architecture scale-preference claim. An assurance proof, gate record, selected-set result declaration, publication occurrence, local decision, or work plan remains a separate result under its own pattern; use A.15.2 for the work plan.

### C.31.ASAP:4.6 - Waiver discipline {#waiver-discipline}

```text
ASAPWaiverReason:
  deontic constraint
  safety or law-domain boundary
  scale-probe overturn
  assurance infeasibility
  context-specific bounded exception
```

A deontic constraint, safety boundary, law-domain boundary, mission constraint, assurance infeasibility, or scale-probe overturn can justify a bounded exception without creating `ArchitectureHeuristicDebt`.

`ArchitectureHeuristicDebt` remains report-only unless tied to a decision, risk, work, evidence, assurance, or selected-set record through its governing pattern.

### C.31.ASAP:4.7 - Scale-refactoring moves {#scale-refactoring-moves}

Before scale-preference guidance becomes action-guiding, name at least one possible repair or stop:

| Scale symptom | Possible architecture move | Boundary |
| --- | --- | --- |
| interface variants grow without payoff | reduce interface alphabet or introduce interface grammar | A.6.M governs interface relation repair. |
| product-line or platform variants lack explicit variation points | introduce variability slots or extension rules | Platform label alone is not scale-preference evidence. |
| one aggregation scope hides lower-scope hazards | split the declared aggregation scope or architecture boundary | C.29 supplies lens-use fields only when coarse-graining is mathematical-lens use. |
| repeated work contains reusable structure | reuse a method template for subsequent work | Use `A.3.1` for a Method claim, `A.15` for Method–Work alignment, and `A.15.1` for actual Work. Use `A.15.4` only while appearance hides a work-relevant prerequisite. |
| regulatory or safety residue remains local and repeated | isolate regulatory residue or safety-specific exception register | Use `A.10` for source recovery and bounded reliance, `G.6` for addressable provenance, `B.3` when a named assurance claim is current, and `A.21` for a gate claim. |
| coarse representation loses safety, semantic, or source distinctions | return to lower-scope source-side evidence or narrow the scale window | Source-return condition is mandatory. |

### C.31.ASAP:4.8 - C.29 lens relation {#c-29-lens-relation}

When a scale preference depends on an RG, coarse-graining, epiplexity, graph, multilevel-learning, or frustration lens, use `C.29` for the mathematical-lens recovery and keep the architecture scale-preference claim in C.31.ASAP. Use C.18.1 for any scale-law claim.

For architecture use, the C.29 output should name `MLU.Description@RGArchitecture`, `MLU.Description@MultilevelLearningFrustration`, or another local MathLensUse output only when the lens changes the next admissible use. The C.31.ASAP side records the scale variable, scale window, slope or scale-probe evidence, exception-growth risk, and source-return condition. C.29 records candidate mathematical object, mapping mode, preserved structure, lost structure, visible payoff, declared use, stop condition, and any blocked overread justified through F.19.

## C.31.ASAP:7 - Conformance Checklist {#conformance-checklist}

| ID | Requirement | Purpose |
| --- | --- | --- |
| `CC-C31.ASAP-1` | @fact:CC-C31-ASAP-1 A C.31.ASAP use being made names the architecture alternative set, described holon, exact `U.ClaimScope`, relevant A.2.6 `U.ContextSlice` membership, scale variable or scale window, and claimed preference under scale. @status:spec/done | Prevents generic "scales better" and generic-context wording. |
| `CC-C31.ASAP-2` | @fact:CC-C31-ASAP-2 `ScaleClaimTriage` names slope evidence, scale-probe evidence, or a no-probe reason. @status:spec/done | Prevents preference claims without declared evidence or no-probe reason. |
| `CC-C31.ASAP-3` | @fact:CC-C31-ASAP-3 Expected stable or improving structure and exception-growth risk are stated. @status:spec/done | Keeps the pattern about architecture structure rather than scale vocabulary. |
| `CC-C31.ASAP-4` | @fact:CC-C31-ASAP-4 Source-return condition is present when any compressed, coarse, extracted, indexed, or accounting representation drops source-side distinctions. @status:spec/done | Prevents unsafe coarse descriptions. |
| `CC-C31.ASAP-5` | @fact:CC-C31-ASAP-5 Waiver reason is one of deontic constraint, safety or law-domain boundary, scale-probe overturn, assurance infeasibility, or context-specific bounded exception. @status:spec/done | Prevents false debt labels. |
| `CC-C31.ASAP-6` | @fact:CC-C31-ASAP-6 `ArchitectureHeuristicDebt` remains report-only unless a decision, risk, work, evidence, assurance, or selected-set record is being used under its governing pattern. @status:spec/done | Prevents shadow project authority. |
| `CC-C31.ASAP-7` | @fact:CC-C31-ASAP-7 Platform, product-line, modularity, reuse, open-interface, RG, and coarse-graining labels do not establish scale preference by themselves. @status:spec/done | Blocks source-label overread. |
| `CC-C31.ASAP-8` | @fact:CC-C31-ASAP-8 Mathematical-lens claims name C.29 output fields; C.31.ASAP governs only the architecture scale-preference side. @status:spec/done | Keeps C.29 and C.31.ASAP distinct. |
| `CC-C31.ASAP-9` | @fact:CC-C31-ASAP-9 Comparison, selected-set, local choice, evidence, assurance, gate, work, or release claims name the governing pattern. @status:spec/done | Prevents scale preference from becoming selection or assurance. |
| `CC-C31.ASAP-10` | @fact:CC-C31-ASAP-10 SoTA rows mutate at least one solution line, checklist item, boundary, relation, or worked slice. @status:spec/done | Keeps source use non-decorative. |
| `CC-C31.ASAP-11` | @fact:CC-C31-ASAP-11 Project-local audit use names both `projectWorkOccurrenceRef` and `architectureScaleAuditProjectUseRelationRef`; a residue register remains retrieval-only unless its own governed direct relation to the exact composite Work is cited. @status:spec/done | Prevents an `@Project` suffix, work reference, or borrowed audit relation from fabricating locality. |
| `CC-C31.ASAP-12` | @fact:CC-C31-ASAP-12 When an ACS criterion row and an ASAP preference are both current, each is separately referenced and neither substitutes for the other. @status:spec/done | Keeps criterion admission and alternative preference distinct. |

## C.31.ASAP:9 - Consequences {#consequences}

| Positive consequence | Cost or trade-off |
| --- | --- |
| Scale preference becomes inspectable before selection or decision. | The practitioner must name a scale variable and window instead of relying on a label. |
| Platform and product-line claims gain usable refactor triggers. | Some source language becomes only a recognition cue until variability slots and exception curves are declared. |
| C.29 lens use stays useful without turning into scale proof. | RG claims and coarsening claims need preserved and lost structure plus source-return condition. |
| Report-only debt notes remain bounded. | Decisions or risk records must use their governing patterns when reliance use is being made. |

## C.31.ASAP:12 - Relations {#relations}

- **Builds on:** `C.31`, `C.31.RSA`, `C.16`, `A.2.6`, `A.17`, `A.18`, `A.19`, `C.18.1`, `C.19.1`, and `C.29`; uses A.1.1 only when a selected `BoundedModelUseStructure` changes the receiving interpretation.
- **Coordinates with:** `A.6.M` for module-interface relation repair; `C.30`, `C.30.ASV`, `C.30.LCA`, and `C.30.ILC` for architecture and selected-structure questions; `C.33` and `C.34` when scale-amenability material needs captured-structure, lost-structure, preservation, or correspondence adequacy before candidate use; `C.35` for the generated or discovered result's kind and adequacy for candidate use; `C.32.P2S` when scale-amenability pressure must continue through problem-to-structure architecturing; `C.32.ACS` when the pressure is represented as a distinct project criteria row; `C.32` when scale preference informs candidate architecture generation; `A.19.CPM` when it supplies one input to explicit comparison; `A.10` for source recovery and bounded reliance, `G.6` for addressable provenance, and `B.3` for a named assurance claim; `G.5`, `G.9`, and `C.11` for selected-set, parity, and choice claims.
- **Boundary:** `C.31.ASAP` governs architecture scale-preference claims. `C.32.ACS` governs criteria-set and criteria-row construction; `A.19.CPM` governs explicit comparison. `C.31`, `C.31.RSA`, `C.29`, `C.18.1`, `C.19.1`, `G.5`, `G.9`, and `C.11` govern modularity-characteristic, reusable-structure accounting, mathematical-lens, scale-law, general method preference, selected-set, parity, and local-choice claims when those claims are being made.
- **Precision-restoration relation:** source wording recovered by `E.10`, `E.10.ARCH`, or `C.30.STRAT` is governed by C.31.ASAP only when the recovered claim being made is architecture scale preference over a declared alternative set, scale variable, and scale window.


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/C-31#root, spec://ai.lev/fpf-spec/contract/C-31-RSA#root, spec://ai.lev/fpf-spec/contract/C-16#root, spec://ai.lev/fpf-spec/contract/A-17#root, spec://ai.lev/fpf-spec/contract/A-18#root, spec://ai.lev/fpf-spec/contract/A-19#root, spec://ai.lev/fpf-spec/contract/C-18-1#root, spec://ai.lev/fpf-spec/contract/C-19-1#root, spec://ai.lev/fpf-spec/contract/C-29#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/C-32#root, spec://ai.lev/fpf-spec/contract/C-32-PAD#root, spec://ai.lev/fpf-spec/contract/A-6-M#root, spec://ai.lev/fpf-spec/contract/C-30#root, spec://ai.lev/fpf-spec/contract/C-30-ASV#root, spec://ai.lev/fpf-spec/contract/C-30-LCA#root, spec://ai.lev/fpf-spec/contract/C-30-ILC#root, spec://ai.lev/fpf-spec/contract/A-10#root, spec://ai.lev/fpf-spec/contract/B-3#root, spec://ai.lev/fpf-spec/contract/G-6#root, spec://ai.lev/fpf-spec/contract/G-5#root, spec://ai.lev/fpf-spec/contract/G-9#root, spec://ai.lev/fpf-spec/contract/C-11#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/C-30-ILC#root, spec://ai.lev/fpf-spec/contract/C-31#root, spec://ai.lev/fpf-spec/contract/C-31-RSA#root, spec://ai.lev/fpf-spec/contract/C-32-MLAO#root, spec://ai.lev/fpf-spec/contract/C-33#root, spec://ai.lev/fpf-spec/contract/C-34#root, spec://ai.lev/fpf-spec/contract/C-35#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/C-31-ASAP
