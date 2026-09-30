# C.32.ADR - Architecture Decision Record Projection {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Architecture publication pattern under C.32
> **Status:** Stable
> **Normativity:** Normative unless explicitly marked informative

## C.32.ADR:1 - Problem frame {#problem-frame}

Use this pattern when an `ArchitectureDecisionRelation@Project` or equivalent project architecture decision must be published as an ADR-like record, decision memo, trade-study record, certification rationale, or similar decision-description record.

Primary working reader: an architect or architecture-responsible practitioner preparing a decision record for developers, reviewers, maintainers, operators, certifiers, or future architects.

Typical entry phrases:

```text
"The project decision is made; now we need an ADR that future developers can use."
"The record must show options, decision, rationale, consequences, and confirmation without becoming the decision itself."
"This is not a software project; can a trade-study memo play the ADR role?"
"The ADR package must link to architecture views without duplicating the whole architecture description."
"A future team must know when this decision is superseded or violated."
```

**First-minute use slice.** A platform architect has a C.32.PAD decision relation selecting event-carried integration with a bounded exception. Using C.32.ADR, the architect creates an ADR projection with section functions for problem frame, candidate options, decision outcome, rationale, consequences, method-use instruction, work split, confirmation eval, source-return links, and supersession. The file is short enough for developers to read, but it remains a publication projection of the decision description, not the decision relation and not the architecture itself.

The primary `EntityOfConcern` is `ArchitectureDecisionRecordProjection@Project`: a publication projection of `ArchitectureDecisionDescription@Project` into an ADR-like record or package. Select this pattern only when the work is to publish or package that decision description for a declared reader use; generic ADR advice that cannot be mapped to decision-section functions stays outside C.32.ADR.

`ArchitectureDecisionRecordProjection@Project` is not a new `U.*` kind and not a new root publication ontology. It is a project publication projection with filled section-function rows. Use `E.17` and `E.24.PUB` for publication-face and publication-use claims; use `C.32.PAD` for the decision relation.

What goes wrong if C.32.ADR is missed: the project either publishes a record-shaped text that hides the actual architecture decision, or it copies architecture descriptions, diagrams, and method material into a record without telling the reader what decision was made and what work must change.

What C.32.ADR buys in practice: a decision record can be small, readable, updateable, and still tied to candidate synthesis, selected structures, architecture characteristics, method-use instructions, work split, confirmation evals, and source-return.

Ordinary working move: start from a PAD decision relation, select the record's publication scope, map each necessary section to the decision content it carries, then publish only what the reader needs to use, check, or reopen the decision.

Adoption test: after using C.32.ADR, a future reader can recover the decision question, considered options, outcome, rationale, consequences, required method or work change, confirmation or eval path, source links, and supersession condition without mistaking the record for the architecture or the decision relation.

Not this pattern when the decision relation is not yet recoverable, the current work is architecture-description adequacy, the record is a general MVPK publication face, or the claim is evidence, assurance, gate passage, local choice, performed work, or pattern authoring. Use the pattern for the next question named in `Relations`.

The first useful output is `ArchitectureDecisionRecordProjection@Project`:

```text
ArchitectureDecisionRecordProjection@Project:
  projectWorkOccurrenceRef?: U.EntityRef constrained to U.Work
  architectureDecisionRecordProjectUseRelationRef?: U.RelationRef governed by the exact record-use, publication-use, or work-use pattern
  projectionId:
  architectureDecisionRelationRef:
  architectureDecisionDescriptionRef:
  publicationCarrierRef:
  publicationScopeRef:
  intendedReaderRefs:
  status:
  sectionFunctionRows:
    - sectionFunction:
      sectionHeadingOrCarrierSlot:
      sourceDecisionSlotRefs:
      requiredReaderUse:
      omittedByDesign?
      sourceReturnCondition?
  architectureDescriptionRefs:
  methodAndWorkRefs:
  confirmationOrEvalRefs:
  supersedesRecordRefs?
  supersededByRecordRef?
  updateOrReopenCondition:
  publicationUseRefs?
```

Here `@Project` is a compatibility and retrieval cue only. It does not make the projection a project, project work, or the architecture decision relation. When this record projection is genuinely local to one actual project, `projectWorkOccurrenceRef` identifies the exact composite `U.Work`, while `architectureDecisionRecordProjectUseRelationRef` identifies the direct relation by which the record is published for, relied on by, or otherwise used in that work under the corresponding subject pattern. The decision relation, its description, the publication projection, any publication occurrence, and the composite project work remain separately identifiable.

## C.32.ADR:2 - Problem {#problem}

ADR practice is useful because it makes architectural decisions small enough to read and update. It is also easy to misuse. A record can become a substitute for the decision relation, a loose essay about architecture, a copied architecture description, or a method prescription with no recoverable target structure.

C.32.ADR treats ADR as a publication projection. The project decision relation belongs to `C.32.PAD`. The architecture description belongs to `C.30.AD` and related view patterns. The method description or pattern-use recommendation belongs to `A.15`, `E.8`, and `E.11.PUR` when those claims are live. The ADR-like record publishes a decision description for a declared reader and use.

For a principle framework, use C.32.ADR only in the exceptional case where the accepted framework-architecture answer is also an exact project architecture decision with the `ArchitectureDecisionRelation@Project` and `ArchitectureDecisionDescription@Project` required by this pattern. Its prior basis may then cite the accepted answer and the exact `E.9` DRR that records it; acceptance remains a separate decision, and `E.4.PFAD` only profiles the framework-specific content. An ADR-like publication may project the question, selected answer, alternatives, rationale, consequences, status, links, and supersession conditions for declared readers. That projection remains separate from the answer, its acceptance, the DRR, framework realization, pattern quality, and publication adequacy. When the principle-framework answer is not an exact project architecture decision, publish the selected decision episteme or a reader-specific projection through `E.17` and `E.24.PUB`; do not use C.32.ADR.

The section question is therefore not "which headings are allowed?" The section question is "which decision functions must a reader recover?" A heading can vary by organization or industry, but the record must carry the decision question, candidate options or reason no candidate set is live, outcome, rationale, consequences, method-use instruction when the decision guides work, work split, confirmation or eval path, source-return, status, and supersession or reopen condition.

ADR-like projection is not software-only. Engineering trade-study records, safety-certification rationale, design review memos, BIM decision logs, method-governance records, and organization-design records can play the same publication role after the project decision relation and record use are typed. The source form may differ; the FPF section functions stay recoverable.

## C.32.ADR:3 - Forces {#forces}

| Force | Tension |
|---|---|
| Reader economy | The record should be short enough to use, but not so short that decision content disappears. |
| Section variation | ADR templates and engineering memos differ, while the decision functions must remain recoverable. |
| Publication and decision separation | The record publishes a description of the decision; it does not become the decision relation. |
| Architecture and method coupling | A record often needs to cite both target structures and required developer methods. |
| Evolution | Supersession, violation detection, and update conditions must be visible without making the record a governance system. |
| Cross-domain use | Software ADR practice must generalize to other holon kinds without importing software-only assumptions. |

## C.32.ADR:4 - Solution {#solution}

Create `ArchitectureDecisionRecordProjection@Project` from an existing `ArchitectureDecisionRelation@Project` and `ArchitectureDecisionDescription@Project`. If the decision relation is missing, require `C.32.PAD` before writing the record.

Work in this order:

1. Name the publication carrier and intended readers. Use a file or other carrier for the Markdown ADR, decision memo, trade-study record, engineering change note, certification rationale, design-review record, or other decision-description form.
2. Cite the decision relation and decision description. If the record cannot cite them, draft them first.
3. Choose the smallest record scope that lets intended readers use the decision. Avoid copying architecture descriptions or full method descriptions; cite them by value where possible.
4. Map section functions to headings or carrier slots. Use local headings if needed, but keep the function rows recoverable.
5. Carry the candidate basis. Record candidate options from `C.32` or the reason no candidate-set question is live. Do not invent options in the ADR after the decision.
6. Carry the decision outcome. State the selected architecture option, bounded exception, or supersession relation from PAD.
7. Carry rationale, accepted losses, and consequences. Include architecture-characteristic trade-offs and guardrails, not only benefits.
8. Carry method-use instruction and work split when the decision guides developer work. Cite `A.15`, method descriptions, pattern-use refs, readiness exits, and expected structure effects rather than burying them in prose.
9. Carry confirmation, eval, or violation-detection exits. Use `C.32.ACE`, `C.16`, `A.10`, `B.3`, `A.21`, or governance patterns when those claims are live.
10. Carry publication and source-return boundaries. Use `E.17` for source-backed publication faces and source return, `E.24.PUB` for publication occurrences and audience availability, and `C.30.AD` for architecture-description claims.
11. Carry status, supersession, and update conditions. Old records remain useful as history when superseded; the active decision relation tells which one governs current work.

### C.32.ADR:4.1 - Required section functions {#required-section-functions}

The following section functions are required unless the decision relation states why the function is not live for this record use.

| Section function | What the record must let the reader recover |
|---|---|
| Identity and status | Record id, title, status, date or version, relation to superseded or superseding records. |
| Problem frame and decision question | The bounded architecture question, described holon, context, and current reader use. |
| Forces and architecture characteristics | The architecture characteristics, constraints, concerns, and trade-offs that made the decision nontrivial. |
| Candidate options | Candidate options, rejected options, bounded exception, or stated reason no candidate-set question is live. |
| Decision outcome | The selected architecture option and affected selected structures. |
| Rationale | Why this outcome is acceptable now, including accepted losses and protected guardrails. |
| Consequences | Expected effects on structures, methods, teams, costs, risks, evidence, operation, and later change. |
| Method-use instruction | Required style, pattern use, method description, or work practice, when the decision changes developer work. |
| Work split | Prospective allocation or instruction content through the plan, policy, commitment, permission, decision, responsibility, authority, or other direct relation that actually states it; otherwise the exact missing governor. Also show readiness or gate exits and the source-return condition. Professional titles are audience cues, not ownership predicates. |
| Confirmation or eval exit | How the decision can be checked, evaluated, monitored, or found violated. |
| Publication boundary | Links to architecture descriptions, views, evidence, assurance, and source material without making the ADR the source object. |

### C.32.ADR:4.2 - ADR package use {#adr-package-use}

When several records form a package, create a package map that names active, proposed, superseded, and related records. A package map is a publication navigation aid. It does not merge decisions, replace PAD relations, or decide record priority by file order alone.

When one decision changes another, use explicit supersession or amendment links. Do not rewrite history by deleting the old record unless the project has a governed archival policy.

## C.32.ADR:7 - Conformance Checklist {#conformance-checklist}

| Requirement | Required result |
|---|---|
| `CC-ADR-1` | @fact:CC-ADR-1 The record cites an `ArchitectureDecisionRelation@Project` or states the equivalent accepted decision relation by value. @status:spec/done |
| `CC-ADR-2` | @fact:CC-ADR-2 The record's publication carrier, intended readers, scope, and status are explicit. @status:spec/done |
| `CC-ADR-3` | @fact:CC-ADR-3 Section functions are mapped to headings or carrier slots. @status:spec/done |
| `CC-ADR-4` | @fact:CC-ADR-4 Problem frame, forces, candidate options, outcome, rationale, consequences, confirmation or eval exit, and supersession or update condition are recoverable. @status:spec/done |
| `CC-ADR-5` | @fact:CC-ADR-5 Method-use instruction and work split are included when the decision guides developer work. @status:spec/done |
| `CC-ADR-6` | @fact:CC-ADR-6 Architecture descriptions, views, evidence, assurance, gate, method, work, and publication claims exit to their subject patterns. @status:spec/done |
| `CC-ADR-7` | @fact:CC-ADR-7 The record does not create new candidate options, new architecture-description adequacy, or new evidence authority by prose. @status:spec/done |

## C.32.ADR:9 - Consequences {#consequences}

| Consequence | Benefit | Cost |
|---|---|---|
| ADR is a publication projection. | Records stay readable while decision authority remains in PAD. | Authors must maintain the relation between record and decision. |
| Section functions are stable even when headings vary. | Software ADR, engineering memo, and certification rationale can be compared by function. | Local templates must be mapped rather than copied blindly. |
| Method and work effects are visible. | Developers can act on the decision instead of only reading rationale. | Records may need exact method refs and work-split refs. |
| Supersession is explicit. | Future readers can distinguish history from current decision. | Record packages need simple upkeep. |

## C.32.ADR:12 - Relations {#relations}

- **Builds on:** `C.32.PAD`, `C.32.P2S`, `C.30.AD`, `C.30.ASV`, `E.17`, `E.24.PUB`, `A.15`, `E.8`, `E.11.PUR`, and `C.32.ADA`.
- **Decision boundary:** Use `C.32.PAD` for the project architecture decision relation. C.32.ADR publishes an `ArchitectureDecisionDescription@Project`; it is not generic ADR guidance and not a second decision authority.
- **Structural-information boundary:** ADR-like projections may cite `C.33` or `C.34` to show captured structure, lost structure, or preservation adequacy behind the projected decision. Cite `C.35` for the exact generated or discovered result, the obtaining or proposed organization, its next-use condition, and the limit or return. Resolve representation, publication-form, or carrier questions separately when the receiving use depends on them. The ADR projection publishes a decision description; use `C.32.PAD` for the decision relation and `C.35` for the cited result's admissible architecture use.
- **P2S docking:** P2S may cite an ADR projection as one stage where decision, rationale, method expectation, and source-return are published for readers; ADR does not carry the whole architecturing flow.
- **Architecture-description boundary:** Use `C.30.AD` and `C.30.ASV` for architecture-description and view adequacy. ADR carries refs and reader-use slices, not full description authority.
- **Pattern and method boundary:** Use `E.8` when the published object is an FPF pattern, `E.11.PUR` for pattern-use recommendation, and `A.15` for method and work claims.
- **Publication boundary:** Use `E.17` for MVPK faces and source return, and `E.24.PUB` for publication occurrences, forms, carriers, bounded use, and audience availability.
- **Evaluation boundary:** Use `C.32.ADA` for decision adequacy; use `C.32.ACE`, `C.16`, `A.10`, `B.3`, or `A.21` for eval, measurement, evidence, assurance, or gate claims.
- **Package boundary:** A record package map aids navigation among records. It does not decide active architecture by file order; PAD relations and status refs remain governing.


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/C-32-PAD#root, spec://ai.lev/fpf-spec/contract/C-30-AD#root, spec://ai.lev/fpf-spec/contract/C-30-ASV#root, spec://ai.lev/fpf-spec/contract/E-17#root, spec://ai.lev/fpf-spec/contract/E-24-PUB#root, spec://ai.lev/fpf-spec/contract/A-15#root, spec://ai.lev/fpf-spec/contract/E-8#root, spec://ai.lev/fpf-spec/contract/E-11-PUR#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/C-32-ADA#root, spec://ai.lev/fpf-spec/contract/A-10#root, spec://ai.lev/fpf-spec/contract/B-3#root, spec://ai.lev/fpf-spec/contract/A-21#root, spec://ai.lev/fpf-spec/contract/C-16#root, spec://ai.lev/fpf-spec/contract/C-25#root, spec://ai.lev/fpf-spec/contract/C-29#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/C-30#root, spec://ai.lev/fpf-spec/contract/C-32-ADA#root, spec://ai.lev/fpf-spec/contract/C-32-PAD#root, spec://ai.lev/fpf-spec/contract/C-33#root, spec://ai.lev/fpf-spec/contract/C-34#root, spec://ai.lev/fpf-spec/contract/C-35#root, spec://ai.lev/fpf-spec/contract/E-4-PFAD#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/C-32-ADR
