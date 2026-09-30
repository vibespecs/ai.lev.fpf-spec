# C.32.ADA - Architecture Decision Adequacy Scales: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## C.32.ADA:5 - Archetypal Grounding {#archetypal-grounding}

**Developer-work readiness.** A service architecture decision has strong candidate traceability and trade-off rationale, but the ADR only says "teams should use events". ADA gives `MethodAndWorkDockingAdequacy = 2 partiallyExpressedForDeclaredUse` because the acting Systems, MethodDescription, expected structure effect, and readiness condition are not recoverable from the instruction. In this case the ADR also expressly requires accountable implementation under an exact assignment, so the absent assignment species/current occurrence and F.6 relation are additional attribution defects; a Work-only instruction would not require them. Any responsibility claim must cite its direct domain predicate or exact missing governor.

**ADR-publication readiness.** A manufacturing architecture decision is clear, but the trade-study memo omits status and supersession. ADA gives `PublicationProjectionAdequacy = 2 partiallyExpressedForDeclaredUse` and `EvolutionAndReopenConditionAdequacy = 3 sufficientlyExpressedForDeclaredUse`. The repair states the missing record-status and supersession assertions using C.32.ADR.

**Architecture review.** A method-family architecture decision has candidate options and Method instructions, but no declared architecture characteristics. ADA gives `ArchitectureCharacteristicTradeoffAdequacy = 0 absent`. The repair states the missing characteristic assertions using C.32.ACS and C.25 before review can judge the decision.

**Governance enforcement.** A toolchain-product correspondence decision depends on team and tool structures. ADA evaluates `TransformerTransformedCorrespondenceAdequacy`; if the correspondence refs are absent, the repair states the missing correspondence assertion using C.32.CONWAY before institutional governance can constrain Method use.

## C.32.ADA:6 - Bias-Annotation {#bias-annotation}

| Risk handled | How C.32.ADA handles it |
|---|---|
| Record completeness as adequacy | ADR projection is one coordinate, not the whole evaluation. |
| Average-score drift | Coordinate values are not averaged; weak coordinates drive repair. |
| Generic review prose | Each weak coordinate names a governing repair pattern. |
| Gate confusion | ADA does not approve, certify, assure, or pass a gate. |
| Hidden method failure | Method and work docking has its own coordinate. |
| Evolution blindness | Reopen, supersession, and source-return have explicit coordinates. |

## C.32.ADA:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Symptom | Repair |
|---|---|---|
| `DecisionAdequacyAverage` | Strong rationale and readable ADR produce a high average despite absent method docking. | Remove the average; use weakest triggered coordinates to choose repair. |
| `ADRCompletenessAsDecisionAdequacy` | The record has all headings, so the decision is treated as adequate. | Evaluate PAD relation, method docking, trade-off, source-return, and reopen conditions separately. |
| `ReviewCommentWithoutRepairPattern` | The reviewer says "unclear" or "not enough detail" without a target repair pattern. | Assign the weak coordinate to `C.32.PAD`, `C.32.ADR`, `A.15`, `C.30.AD`, `C.32.ACS`, or another exact subject pattern. |
| `GateByScale` | A value of `4` or `5` is treated as approval or certification. | Keep ADA as evaluation; use `A.21`, `A.10`, `B.3`, or governance patterns for gate, evidence, assurance, and enforcement claims. |
| `NotTriggeredAsConvenience` | A difficult coordinate is marked not triggered to close the review. | Require a declared-use reason and receiving-pattern boundary; otherwise score it and repair. |
| `MethodDockingSkipped` | The decision is adequate for architecture discussion but then used to direct developer work. | Re-declare use as developer-work readiness and evaluate method docking, work split, and publication handoff. |
| `SystemRoleLabelAsEvaluator` | A reviewer system-role kind, assignment, or ADA record is treated as the performer of evaluation. | Recover the exact admitted evaluator System through A.13 and let A.15.1 independently admit the dated evaluation Work. Add assignment species, occurrence, and F.6 only when precise assignment-bound attribution is expressly represented. Keep any responsibility relation, result episteme, and operation application separate. |
| `ContextLabelAsEvaluationScope` | A project, domain, or bounded-context label stands in for the evaluation boundary. | Bind the exact `U.ClaimScope`, selected context slices, scheme and plane, evaluation window, and decision-question input projection. |

## C.32.ADA:10 - Rationale {#rationale}

C.32.ADA exists because architecture-decision adequacy is not one property. It is a family of recoverability and use-readiness coordinates across decision relation, selected structures, architecture characteristics, method docking, work split, publication projection, evidence or eval exits, and evolution.

The pattern follows the same discipline as FPF quality evaluation: declared use first, complete coordinate set, ordinal values with rationale, no average, and targeted repair. It remains architecture-specific because the coordinates are tied to PAD, ADR projection, architecture descriptions, candidate synthesis, method-use instructions, and architecture-characteristic trade-offs.

## C.32.ADA:11 - SoTA-Echoing {#sota-echoing}

These sources inform the coordinates, value meanings, stop conditions, and repair exits used below.

| Source to inspect | Why this source is load-bearing here | Transfer into ADA | Concrete ADA mutation | Blocked overread |
|---|---|---|---|---|
| Current FPF `E.21` scale discipline | Existing FPF pattern for declared-use evaluation, exact `0 absent` through `5 exceptionallyExpressedForDeclaredUse` labels, complete coordinates, adjacent-value rationale, and no averaging. | Reuse the value domain and evaluation discipline for architecture decisions without copying pattern-quality coordinates. | ADA requires declared use, complete coordinate set, E.21 value labels with adjacent rationale, no average, and use-specific stop conditions. | E.21 pattern-quality status and coordinates are not architecture-decision adequacy. |
| `C.32.PAD` and `C.32.ADR` | PAD and ADR define the decision relation and publication projection being evaluated. | Make relation adequacy and projection adequacy separate coordinates. | ADA can say a PAD relation is usable while ADR projection needs repair, or the reverse. | A complete ADR does not make the decision relation adequate. |
| ISO/IEC/IEEE 42010:2022 official standard (`https://www.iso.org/standard/74393.html`; IEEE page `https://standards.ieee.org/ieee/42010/6846/`) with the 42010 companion site as secondary reading (`https://iso-architecture.org/42010/`) | Current official source for architecture descriptions, viewpoints, views, correspondence, and rationale; the companion site is used only as secondary reading. | Add coordinates for affected structure, architecture-description adequacy, and source-return. | ADA identifies `C.30.AD` and `C.30.ASV` as subject-pattern locators for weak description assertions. | Architecture-description adequacy does not decide or approve the architecture. |
| Ford, Parsons, Kua, and Sadalage, `Building Evolutionary Architectures`, 2nd ed. (`https://www.oreilly.com/library/view/building-evolutionary-architectures/9781492097532/`) | Current practitioner source for architecture feedback and incremental change under eval-like mechanisms. | Add evolution, reopen, guardrail, and confirmation coordinates. | ADA checks reopen and eval exits before a decision is used for long-running work. | Source-side fitness-function wording is not imported as ADA object naming. |
| Ford, Richards, Sadalage, and Dehghani, `Software Architecture: The Hard Parts` (`https://www.oreilly.com/library/view/software-architecture-the/9781492086888/`) | Current practitioner source for trade-off analysis under competing characteristics. | Add architecture-characteristic trade-off adequacy and accepted-loss repair. | ADA identifies ACS, ACE, C.16, C.25, C.31, or C.31.ASAP as subject-pattern locators for the exact weak trade-off assertion. | Trade-off discussion is not an assurance claim or governance approval. |
| 2026 ADR violation-detection research (`https://arxiv.org/abs/2602.07609`) | LLM detection in the study was more accurate for explicit decisions checkable from code than for decisions left implicit or requiring deployment settings or organizational context. | Add confirmation, source-return, method, deployment, and organization refs to adequacy checks when live. | ADA scores confirmation and method docking separately and blocks hidden organizational knowledge from passing as ready. | Automated violation detection is not proof, evidence, assurance, or gate passage. |

**Source-currentness boundary.** Recheck a source row when FPF evaluation discipline, architecture-decision practice, ADR violation checking, evolutionary-architecture eval practice, or project governance changes a coordinate, value meaning, or repair exit.

## C.32.ADA:13 - Footer marker {#footer-marker}

C.32.ADA closes when `ArchitectureDecisionAdequacyEvaluation@Project` declares the use and stop condition; binds the exact claim scope and selected context slices, reference scheme and plane, evaluation window, and decision-question input projection; cites the evaluated decision relation and optional projection; evaluates every coordinate with an E.21 value label and rationale or grounded not-triggered status; names weakest blocking coordinates, repair patterns, and repair instructions; avoids average-score replacement; and, when actual evaluation is claimed, keeps the A.13-qualified evaluator System, independently admitted A.15.1 Work, operation application, any responsibility relation, and result episteme separately identified. Assignment species, occurrence, and F.6 attribution are present only when the record expressly represents that precise attribution.


## C.32.ADA:End {#end}
