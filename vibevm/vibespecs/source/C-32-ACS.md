# C.32.ACS - Architecture Characteristic Criteria Set: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## C.32.ACS:5 - Worked slices {#worked-slices}

**Manufacturing cell.** HCS suggests maintainability, locality, function-bearer fit, change reach, and scale amenability. ACS keeps nine draft criteria rows, then marks setup-change reach, function-bearer fit, and exception growth as optimization indicators. ACS records safety and evidence reuse as monitored guardrails. C.32 later synthesizes universal-fixture candidates under those criteria.

**Method-family architecture.** HCS suggests repeatability, teachability, transferability, evidence reuse, exception growth, and change reach. ACS marks evidence reuse, exception growth, and transferability as optimization indicators. Teachability goes to C.25 because it depends on learner scope, measures, mechanisms, and evidence.

**AI-agent architecture.** HCS suggests evidence refresh, policy controllability, latency, observability, and rollback. ACS marks policy controllability, evidence refresh, and latency as optimization indicators. Benchmark performance is not an architecture characteristic by name; it can supply an eval reading only after the bearer, scale, parity frame, and receiving use are declared.

**Team and assignment architecture.** A hospital escalation team starts from coordination load, accountability clarity, decision latency, evidence custody, substitutability among local system-role kinds, and continuity of assignment occurrences and their holder Systems. ACS creates separate criteria because A.2.7 can compare or relate local kinds but does not substitute holders. The kind-substitutability row binds the exact local kind-relation structure and predicate; the assignment-continuity row binds the exact assignment occurrences, holder Systems, and continuity predicate. ACS marks decision latency, accountability clarity, and evidence custody as optimization indicators, keeps patient-safety loss and assignment-continuity loss as guardrails, and leaves staffing choice to the receiving decision pattern.

## C.32.ACS:6 - Kind and Receiving-Claim Boundary {#kind-and-receiving-claim-boundary}

C.32.ACS governs project criteria-set construction for architecture improvement. It does not govern:

- holon-family starter packs, governed by `C.32.HCS`;
- architecture-characteristic eval programs, governed by `C.32.ACE`;
- C.25 Q-Bundle normal form, governed by `C.25`;
- C.16 measurement templates or readings, governed by `C.16`;
- C.31 modularity and reusable-structure characteristic repair, governed by `C.31`;
- C.31.ASAP scale-preference claims, governed by `C.31.ASAP`;
- E.22 question framing and E.23 repeated improvement method, governed by `E.22` and `E.23`;
- C.32 candidate synthesis, governed by `C.32`;
- A.19.CPM comparison, A.19.SelectorMechanism selection, C.11 local choice, G.5 selected-set result declaration, E.17 source-backed publication-face and source-return work, E.24.PUB publication-occurrence and audience-availability work, or architecture-decision work for `C.32.PAD`.

## C.32.ACS:8 - Common failures and repairs {#common-failures-and-repairs}

| Failure | Working symptom | Repair |
|---|---|---|
| `CatalogueCopyAsCriteriaSet` | A project imports a long list of ilities and treats the list as architecture guidance. | Use HCS for starter heads, then build ACS rows, mark optimization indicators, and keep guardrails and context-only rows separate. |
| `TooManyOptimizationIndicators` | Dozens of rows drive optimization at once. | Keep the few rows that change the next synthesis step; demote the rest to monitored guardrails or context-only rows. |
| `FunctionGoalAsArchitectureCriterion` | A user-visible function is used as the architecture optimization criterion. | Recover the function claim through `A.6.F`; then name the architecture characteristic that makes the function sustainable. |
| `QBundleDuplicatedAsScaleSet` | Maintainability, availability, security, teachability, or trustworthiness is treated as one ACS row when the truth depends on several typed slots. | Open `C.25`, construct or reference the Q-Bundle, then select only the relevant slot for ACS use. Keep any report-only proxy outside the criteria row unless its bearer, scale, proxy risk, and receiving use are declared. |
| `EvalProgramAsCriterion` | A test, monitor, source-side fitness function, benchmark, dashboard, or eval result is named as the criterion. | Name the characteristic row first; eval-program construction belongs to `C.32.ACE` and measurement claims belong to `C.16`. |
| `BearerCarryoverWithoutRebinding` | An engineered-system row is copied to architecture around a Method, local system-role kind, separate System-classification judgment, assignment, or cultural-evolution case without changing the exact bearer, predicate, scale, or admissible use. | Return to HCS only if the described holon family changed. Otherwise stay in ACS and rebind the row to the actual bearer and selected structure; a Method, kind, or assignment is not forced into a holon family. |
| `LocalGainHidesCounterLoss` | A candidate improves one row while worsening evidence burden, control burden, source-return cost, or functional adequacy. | Add monitored guardrail rows and open `E.13` when proxy-to-value drift appears before comparison or next synthesis. |
| `ReadingAsDecision` | A better reading is treated as the selected architecture. | Keep the reading as feedback. Use `A.19.CPM` for explicit comparison, `A.19.SelectorMechanism` for set-returning selection, `C.11` for local choice, `G.5` for selected-set result declaration, and `C.32.PAD` for a project architecture decision. For publication, use `E.17` for a source-backed face and source return and `E.24.PUB` for the publication occurrence and audience availability. |
| `ContextLabelAsRowScope` | A domain, team, project, or bounded-context label is used as if it delimited every criterion row. | Bind each row's exact `U.ClaimScope`, selected A.2.6 context slices, scheme and plane, and window; add a selected model-use structure only when it changes interpretation. |

## C.32.ACS:10 - Rationale {#rationale}

Architecture optimization is meaningful only after the criteria are named. ACS supplies that middle object: not a generic quality catalogue, not a starter pack, not a Q-Bundle, not an eval program, and not a decision, but a project criteria set that can guide synthesis, residual reduction, and repeated improvement.

The pattern stays holonic by allowing starter heads to recur across holon families while requiring bearer and scale rebinding. It stays action-facing by limiting optimization indicators and keeping non-optimized criteria rows as guardrails.

## C.32.ACS:11 - SoTA-Echoing {#sota-echoing}

These rows document how source practice contributes to criteria-row fields, use-class rules, and receiving-pattern boundaries in C.32.ACS.

| Source to inspect | Why this source is load-bearing here | Transfer into ACS | Concrete ACS mutation | Blocked overread |
|---|---|---|---|---|
| FPF source presentation `ТриПрототипаТриОшибки` (2022-03-26) | The presentation distinguishes eval from test and requires characteristic cards, scale procedures, fair comparison, explicit indicatorization, hard constraints, optimization goals, and risk signals. | Put characteristic rows and use classes before any ACE eval program or explicit comparison. | ACS row shape carries use class, scale form, current reading or no-reading reason, proxy risk, protected counter-characteristics, receiving use, and source-return condition. | An eval, test, dashboard, score, or hard constraint is not the architecture characteristic or project criterion by itself. |
| ISO/IEC 25010:2023 (`https://www.iso.org/standard/78176.html`) and SQuaRE quality-model practice | Current standard source for product quality vocabulary and measurement context. | Use standards as source catalogue material that must be rebound to the described holon, bearer, scale, and use class. | ACS separates source catalogue, HCS starter pack, draft project criteria rows, optimization indicators, monitored guardrails, and context-only rows. | A standard quality-model characteristic is not automatically an FPF project criterion, scale row, eval program, or holon ontology. |
| Richards and Ford, `Fundamentals of Software Architecture`, 2nd ed. (`https://www.oreilly.com/library/view/fundamentals-of-software/9781098175504/`) | Current practitioner line treats architecture characteristics as criteria for success, trade-off analysis, scope, and governance. | Criteria rows must be admitted and typed before synthesis, residual optimization, measurement, or governance claims. | ACS rows supply the criteria consumed by `C.32`, `C.32.MLAO`, and later patterns for the next questions. | A broad architecture-characteristic list is not a project criteria set. |
| Ford, Richards, Sadalage, and Dehghani, `Software Architecture: The Hard Parts` (`https://www.oreilly.com/library/view/software-architecture-the/9781492086888/`) | Mature practitioner line for least-worst trade-offs among competing architecture characteristics. | Keep explicit protected losses; explicit comparison belongs to `A.19.CPM` when comparison is being made. | ACS requires use class, proxy risk, protected counter-characteristics, and downstream comparison boundary. | No single criterion or local gain may dominate without naming the losses it can hide. |
| Ford, Parsons, Kua, and Sadalage, `Building Evolutionary Architectures`, 2nd ed. (`https://www.oreilly.com/library/view/building-evolutionary-architectures/9781492097532/`), `Software Architecture Metrics` (`https://www.oreilly.com/library/view/software-architecture-metrics/9781098112226/`), and `C.32.ACE` | Current practitioner line for guided change and repeatable eval over architecture characteristics. | Restore source-side fitness-function wording as eval programs over declared ACS rows. | Row shape has `evalProgramRefs?` and names ACE for eval-program construction after the row exists. | An eval program or metric is not a characteristic kind, project criterion, selected architecture, or decision. |
| Current FPF `C.25` and `E.13` | Local receiving law for composite quality families and proxy-for-value drift. | Keep Q-Bundle structure and proxy repair outside ACS while carrying the needed links. | Row shape includes `endpointShape`, `qBundleRef?`, `proxyRisk`, and `protectedCounterCharacteristicRefs`; proxy drift requires `E.13`. | A composite quality family is not one scalar row, and a convenient indicator is not the declared architecture concern. |
| ATAM lineage and ATRAF 2025 (`https://arxiv.org/abs/2505.00688`) | Mature and current architecture-evaluation practice binds quality attributes to scenarios, trade-offs, sensitivity points, risks, and repeated refinement. | Admit a quality word as a project row with bearer, scale, polarity, counter-characteristics, and receiving use before it affects synthesis. | Explicit comparison belongs to `A.19.CPM`; composite quality bundles belong to `C.25`; ACS retains row preparation. | Scenario analysis and trade-off vocabulary do not compare or choose candidates until the receiving comparison, selection, choice, or decision pattern is being used. |

**Source-currentness boundary.** Use each source row only for the ACS field, use-class rule, or receiving-pattern boundary named in that row. Recheck the row when a named standard, book edition, source presentation, FPF pattern for the next question, or current architecture-evaluation line changes the transferred move. If the project wants measurement, eval-program design, comparison, selection, selected-set result declaration, actual publication, local choice, evidence, assurance, or decision use, leave ACS and open the pattern for the next question.

## C.32.ACS:13 - Footer marker {#footer-marker}

C.32.ACS closes when the project can name the starter-pack row or source-catalogue line, draft project criteria rows, optimization indicators, monitored guardrails, context-only rows, bearers, row claim scopes and selected context slices, reference schemes and planes, qualification or evaluation windows, scale forms, current reading or no-reading reason, protected counter-characteristics, receiving uses, and source-return conditions. Continue with the pattern whose use conditions match the next question. If later precise Work is asserted, recover each exact actual performer System through A.13 and let A.15.1 independently admit the dated Work and enacted Method; add an assignment occurrence, its declared species, and F.6 only when the ACS account or receiving use expressly consumes precise assignment-bound attribution through the same obtaining A.13 assignment. F.6 identifies neither assignment nor performer, missing or failed F.6 leaves the Work intact.


## C.32.ACS:End {#end}
