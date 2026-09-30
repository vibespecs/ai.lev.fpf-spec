# A.19.CHR - CHRMechanismSuite: Shared Rules for Characterization and Selection: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## A.19.CHR:6 - Bias-Annotation {#bias-annotation}

The following trade-offs matter when using the suite:

* **Gov.** Bias toward fail-closed admissibility and explicit auditability (applicable relation/crossing references, pinned spec refs, guard–gate separation). Mitigation: the tri-state `GuardDecision` allows uncertainty to degrade or abstain without forcing gate-level blocking; exploration can still proceed via explicit SoS‑LOG policy branches.
* **Arch.** Bias toward explicit node-level composition (E.18) and explicit planned baselines and conditional typed fillings. Mitigation: the suite fixes only the universal core; discipline-specific generators and extensions remain separate mechanisms connected by `Uses`, keeping the suite compact.
* **Onto/Epist.** Bias toward a strict separation of CN‑Spec and CG‑Spec spec refs, mechanisms (A.6.1), and planning epistemes (A.15.2; A.15.3 for typed fillings). Mitigation: specialization is explicitly supported (`⊑/⊑⁺`) and does not require inventing new kernel constructs; method diversity is expressed via MethodDescription refs and ComparatorSpec refs.
* **Prag.** Bias toward conservative uncertainty handling (unknown does not coerce to pass) may reduce decisiveness. Mitigation: “probe-only” and “sandbox” behaviors are permitted as explicit, audited degrade modes (policy-id + branch-id), not as silent coercions.
* **Did.** Bias toward explicit terminology and pins increases authoring surface area. Mitigation: this pattern provides a canonical protocol and ordinary baseline content with reusable references so authors can reuse a stable template rather than re-inventing local prose conventions.

## A.19.CHR:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Why it fails | Avoid / repair |
|---|---|---|
| Using `MechFamilyDescription` as a suite container | Collapses “many implementations of one mechanism” into “many mechanisms”, mixing levels and breaking reuse constraints | Use `MechSuiteDescription` for multi-mechanism sets; use `MechFamilyDescription` only for multiple implementations of a single `U.Mechanism` |
| Embedding a second CG‑Spec or CL/Φ/Φ_plane tables inside the suite or plan item | Duplicates the governing spec refs and creates drift between planning, gates, and audit | Publish refs and pins only (`CGSpecRef`, `BridgeCardRef`, policy-id pins); keep tables in their canonical registries and cite them |
| Implicit UNM/UINDM/ULSAM “inside” score/compare/select | Breaks auditability and violates the suite protocol explicitness obligation | Make dependencies explicit as protocol steps (`Uses`) and cite the chosen mechanism instances in the planned baseline and audit pins |
| Hidden thresholds or weights in CHR core | Moves acceptance criteria into the wrong layer, defeating the declared defaults source and traceability | Keep thresholds in AcceptanceClauses, TaskSignature, or GateProfile; if a policy is needed, mint a policy-id and cite it explicitly |
| Scalarizing partial orders “for convenience” | Violates set-return semantics and hides incomparability | Keep comparisons set-valued via CPM and selectors set-returning; any scalar summary must be declared as report-only telemetry or as an explicit lawful comparator |
| Treating planned baseline as a launch witness | Smuggles execution facts into planning and blurs P2W separation | Record the edition/reference baseline in A.15.2; add A.15.3 fillings only for declared positions and keep actual bindings and launch witnesses in enactment |
| Using `CompareGuard` / `LaunchGuard` as mechanism lexemes | Collides with reserved gate-level pins and blurs guard vs gate responsibilities | In mechanisms use `…Eligibility` / `…Admissibility`; reserve `USM.CompareGuard` and `USM.LaunchGuard` for gate-visible pins |

## A.19.CHR:10 - Rationale {#rationale}

This pattern deliberately fixes the CHR core as a **description object** rather than a new “meta-mechanism” so that:

1. **Level separation stays clean.** The suite is a D-episteme that enumerates mechanisms and obligations; the mechanisms remain A.6.1 declaration epistemes with their own arguments, results, laws and admission conditions. This prevents a “god object” that re-implements A.6.1 inside a new container.

2. **Spec refs remain centralized.** CN-Spec and CG-Spec already define the governance card and admissibility gate that own comparability, normalization, indicatorization policy, and numeric admissibility. The suite requires those specs as pins and forbids duplicating them, making “one center of gravity” operational rather than rhetorical.

3. **P2W integration becomes explicit without turning planning into execution.** Ordinary A.15.2 content records the edition/reference baseline. Typed A.15.3 filling is needed only for an independently declared position; only enactment supplies actual bindings and launch witnesses.

4. **Uncertainty handling is made safe by construction.** Tri-state guard decisions are a minimal guard-decision form that supports admissible abstention and degradation while keeping gate decisions and decision logs in their proper place (OperationalGate(profile)).

In short: *governing specs are cited, not copied; plans are declared, not executed; and admissibility is a first-class surface, not a hidden tail.*

## A.19.CHR:11 - SoTA-Echoing {#sota-echoing}

**Working question.** How should a team connect normalization, indicator choice, scoring, comparison and selection so that the final result still follows from the selected scales, evidence and method conditions when one of them changes?

For this question, **adapt** declaration-first workflow composition, the selected line compared in A.6.7 §11. [CWL v1.2.1's process references, requirements and abstract operations](https://www.commonwl.org/v1.2/Workflow.html#Operation) supply the substantive external model for distinguishing a described operation from a concrete process. The CHR adaptation makes the shared CN/CG conditions and each operation's result bindings explicit. CWL supplies neither these FPF laws nor the justification of the offer comparison.

The serious alternative is one pinned executable estimator pipeline, exemplified by [scikit-learn 1.9.1 Pipeline](https://scikit-learn.org/stable/modules/generated/sklearn.pipeline.Pipeline.html). It is attractive when fitting and sequential transformation already express the whole task. For the same five used CHR stages, compare it with the suite while holding the methods, data, policy and evidence requirements fixed. Both can calculate the two offers correctly. A pipeline plus explicit checks can also reject expired normalization. Its executable composition alone, however, does not state the case's scale-preservation argument or resolve the separately governed selection policy; those facts still need an inspectable account.

**Adopt** explicit method/specification resolution and **reject** a stage-name-only chain as sufficient justification. The suite accepts the extra reference cost to expose these conditions before choosing implementations. This is a trade-off in explanation and reuse, not a claimed runtime benefit or measured authoring saving. If a single existing pipeline already exposes every condition needed by the receiving use, reuse its account; creating another suite copy adds no gain.

The concrete effect is in §§4.0, 4.5 and 4.8.1: choose each contract before using a stage, retain every transformation's basis through the actual comparison, and stop the normalization-based path when its selected validity window fails. The final {A,B} remains a set even though the five stages could be packaged behind one callable interface. That packaging cannot add a singleton preference or purchase approval.

The two primary specifications are source models and a serious comparator; the choice for CHR is an explicit local architectural inference. They establish no empirical superiority of this pattern. Reopen the comparison if the receiving task becomes one fully self-contained executable pipeline, if its account already makes the same conditions cheaper to recover, or if a changed member contract makes the common baseline insufficient.


## A.19.CHR:End {#end}
