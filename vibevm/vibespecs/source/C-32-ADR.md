# C.32.ADR - Architecture Decision Record Projection: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## C.32.ADR:5 - Archetypal Grounding {#archetypal-grounding}

**Software ADR.** A team publishes an ADR for event-carried integration. The record uses local headings, but the function rows recover context, options, selected outcome, rationale, consequences, method-use instruction for event schema work, confirmation eval, and supersession. Developers can see what to implement and when the decision reopens.

**Manufacturing trade-study record.** A fixture decision is published as an engineering trade-study memo rather than a Markdown ADR. The memo carries candidate fixture variants, selected universal-fixture scope, accepted setup-time loss, cell-design method instruction, evidence links, and reopen threshold. C.32.ADR admits the memo because it projects the decision description for the intended reader.

**Certification rationale.** A regulated product records a safety-architecture decision in a certification rationale. The record carries the decision outcome, rationale, evidence refs, architecture-description refs, and confirmation path, while evidence and assurance claims stay in `A.10` and `B.3`.

**Method-use record.** A project decision requires reviewers to use an evidence handoff pattern before final review. The ADR-like record cites the Method description and expected evidence-structure effect; the instruction does not by itself establish performed review Work.

## C.32.ADR:6 - Bias-Annotation {#bias-annotation}

| Risk handled | How C.32.ADR handles it |
|---|---|
| Template-first writing | The record starts from a PAD decision relation and section functions, not from a blank template. |
| Publication-as-decision drift | The ADR projection cites the decision relation and remains a publication object. |
| Architecture-copy drift | Architecture descriptions are cited through `C.30.AD`; the record carries only decision-relevant references. |
| Method prose drift | Method-use instruction is typed through `A.15`, `E.8`, or `E.11.PUR` when live. |
| History loss | Status and supersession are record functions; old records stay recoverable unless governed archival policy says otherwise. |
| Software-only overread | ADR-like projection is generalized by section function and reader use, not by software tool convention. |

## C.32.ADR:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Symptom | Repair |
|---|---|---|
| `BlankTemplateADR` | A template is filled with plausible prose but no PAD relation can be cited. | Draft or recover `ArchitectureDecisionRelation@Project` with `C.32.PAD`; then project it into the record. |
| `ArchitectureDescriptionDump` | The ADR copies diagrams, views, or model text and the decision outcome is hard to find. | Keep the record small; cite architecture-description refs and restore decision outcome, rationale, consequences, and work effects. |
| `OptionsInventedInRecord` | The ADR lists options that were not part of candidate synthesis or accepted decision basis. | Use `C.32`, `A.19.CPM`, or PAD; update the decision relation before updating the record. |
| `MethodInstructionHiddenInRationale` | A decision requires developers to change their practice, but the instruction is buried in rationale prose. | Record the prospective content through the exact plan, policy, commitment, permission, decision, responsibility, authority, or other direct relation that states it, with Method refs, intended Systems, expected structure effect, and readiness or gate exit; otherwise return its exact missing governor. Do not manufacture a current assignment or performed Work. If performance later occurs, recover every precise performer's A.13 core and independently admit the Work under A.15.1; add F.6 only when precise assignment-bound attribution is current, and add only the other direct relations that independently obtain. |
| `NoConfirmationPath` | Future teams cannot tell whether the decision still holds or has been violated. | Add confirmation, eval, guardrail, source-return, or supersession condition; use the receiving evaluation or governance pattern. |
| `PackageOrderAsGovernance` | The latest file by number is treated as active without explicit status or supersession. | Add package map or status fields; make active, proposed, superseded, and related relations explicit. |

## C.32.ADR:10 - Rationale {#rationale}

ADR practice is valuable when it makes architectural decisions communicable and revisitable. It becomes weak when a record is treated as the decision itself or when a template substitutes for decision work.

C.32.ADR therefore uses the record as a projection. The decision relation is made in `C.32.PAD`; the record publishes a decision description for a declared reader. This preserves the strongest ADR practice, small and updateable records, while adding FPF kind control for architecture descriptions, method descriptions, evidence, assurance, gate, publication, and performed work.

The pattern also generalizes ADR practice beyond software by using section functions rather than software-specific carrier assumptions. A record can be a Markdown file, engineering memo, or certification rationale if it projects the decision description and keeps receiving claims with their subject patterns.

## C.32.ADR:11 - SoTA-Echoing {#sota-echoing}

These sources inform the section functions, projection boundaries, and update conditions used below.

| Source to inspect | Why this source is load-bearing here | Transfer into ADR projection | Concrete ADR mutation | Blocked overread |
|---|---|---|---|---|
| Michael Nygard, `Documenting Architecture Decisions` (`https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions`) | Foundational practitioner source for small decision records with context, decision, status, and consequences. | Preserve the small-record and future-reader practice. | C.32.ADR requires status, context, decision outcome, consequences, and supersession or reopen condition. | The ADR record is not the decision relation or the architecture description. |
| MADR 4.x (`https://adr.github.io/madr/`) | Current Markdown ADR practice with options, outcome, status, links, and confirmation. | Use options, outcome, links, and confirmation as section functions rather than fixed FPF ontology. | Required section functions include candidate options, decision outcome, confirmation or eval exit, and package links. | "Any decision" scope is not imported as architecture-decision kind expansion. |
| ISO/IEC/IEEE 42010:2022 official standard (`https://www.iso.org/standard/74393.html`; IEEE page `https://standards.ieee.org/ieee/42010/6846/`) with the 42010 companion site as secondary reading (`https://iso-architecture.org/42010/`) | Current official source for architecture descriptions, viewpoints, views, correspondence, and rationale. | Keep architecture views as cited description refs inside the ADR projection. | ADR rows carry `architectureDescriptionRefs` and publication boundary instead of copying view content wholesale. | A 42010 architecture description is not an ADR projection and not a PAD relation. |
| 2026 ADR violation-detection research (`https://arxiv.org/abs/2602.07609`) | The study reports higher LLM violation-detection accuracy for explicit, code-inferable decisions and lower accuracy for implicit or deployment-oriented decisions that depend on deployment configuration or organizational knowledge. | Make confirmation, violation-detection scope, and non-code source refs explicit. | ADR section functions require confirmation or eval exit, source-return condition, and method or deployment refs when live. | LLM-detectability is not evidence, assurance, or gate passage. |
| Current FPF `E.8`, `E.17`, `E.24.PUB`, `A.15`, `A.10`, `B.3`, `C.30.AD`, and `C.32.PAD` | Existing FPF patterns define or constrain pattern form, publication, method work, evidence, assurance, architecture description, and decision relation. | Keep ADR projection thin and typed. | The record maps section functions while every neighboring claim retains its exact predicate, defining or constraining ClaimGraph, and non-semantic pattern locator. | ADR projection does not duplicate pattern language, MVPK, method, evidence, assurance, gate, or description doctrine. |
| NASA Systems Engineering Handbook, decision analysis and trade-study practice (`https://www.nasa.gov/wp-content/uploads/2018/09/nasa_systems_engineering_handbook_0.pdf`) plus domain certification-rationale practice where governed locally | Non-software engineering decisions are commonly recorded through trade studies, engineering memos, review records, safety cases, or certification rationale. NASA supplies a concrete source for alternatives, criteria, assumptions, recommendation, impacts, and decision documentation. | Generalize by record function and reader use rather than by Markdown file convention. | `publicationCarrierRef` identifies the carrier used to present the memo, trade-study record, certification rationale, or design-review record, while section functions still recover problem frame, options, outcome, rationale, consequences, confirmation, source return, status, and supersession. | Non-software record form does not change the PAD decision relation or section functions. |

**Source-currentness boundary.** Recheck a source row when ADR template practice, decision-record tooling, violation-detection practice, architecture-description practice, FPF publication patterns, or project governance changes the section function or update rule used by C.32.ADR.

## C.32.ADR:13 - Footer marker {#footer-marker}

C.32.ADR closes when `ArchitectureDecisionRecordProjection@Project` cites the decision relation and decision description, names carrier, readers, scope, status, section-function mapping, decision outcome, rationale, consequences, method and work refs when live, confirmation or eval exit, publication boundaries, and update or supersession condition.


## C.32.ADR:End {#end}
