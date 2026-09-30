# A.19.SelectorMechanism - Unified Selection Kernel, SelectorMechanism: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## A.19.SelectorMechanism:0 - At a glance — didactic, informative {#at-a-glance-didactic-informative}

* **What it is:** a universal **set-returning** selection kernel: it takes candidates, admissible comparison outcomes, and explicit criteria, and returns a **selected set**, not a forced single winner.
* **What it is not:** it is not a hidden scoring model, not a comparator, not a gate, and not a telemetry or publishing step.
* **Why it exists:** to prevent three recurring failure modes: **hidden thresholds**, **silent scalarization**, and **winner‑take‑all defaults** under partial orders and uncertain evidence.
* **Use this when:** the current project question is selection from admitted candidates under explicit criteria after comparison has already been made or cited.
* **What this buys:** the practitioner gets one selected-set value whose criteria, finite basis of exact upstream binary CPM applications, required comparison coverage, token provenance, scope, predicate basis, plane, window, and policy bindings are explicit. `degrade` and `abstain` remain eligibility values, not selected-set members or alternative result kinds.
* **First output:** read the by-value candidate set bound to `SelectionSlot`. Read the candidate universe, finite upstream CPM application basis, required pair coverage, derived comparison-token union, selection conditions, claim scope and context slices, reference plane, evaluation window, eligibility value, and evidence use from the actual `Select` application and direct neighboring relations; they are not fields inside the selected set.
* **How it evolves:** method semantics and SoTA algorithm families connect via `G.2` packs and wiring modules; the kernel signature stays stable and teachable.
* **Suite stage:** `select` (ordering lives only in `A.19.CHR:4.5` and `suite_protocols`; suite membership is a set in `A.19.CHR:4.2`).
* **Inputs (conceptual):** admitted candidates; a finite by-value basis of exact upstream binary CPM applications, each with its exact pair, realized `GuardDecision`, and own `ComparisonResultSlot` binding when produced; the exact union of justified relation or poset tokens from those bindings; explicit `CriteriaSlot`, `CNSpecSlot`, `CGSpecSlot`; one `U.ClaimScope` with selected A.2.6 `U.ContextSlice` members; the same A.19 predicate basis when one governs the comparisons or selection criteria; effective reference plane; explicit evaluation window; and optional TaskSignature and MinimalEvidence policy refs.
* **Output (conceptual):** the by-value `SelectionSlot` candidate set. A singleton is allowed only under explicit selection conditions or an admissible upstream total order. The output is not a decision log, guard value, result episteme, generic result relation, publication, or replay record.
* **Non-goals:** does **not** normalize (UNM), indicatorize (UINDM), score (USCM), fold (ULSAM), compare (CPM), define acceptance thresholds, publish, or emit telemetry; it is a selection step over already-admissible inputs.
* **Planned use:** an A.15.2 baseline selects editions and policies. A.15.3 and SlotFillingsPlanItem apply only to independently declared receiving positions under A.19.CHR:4.7.2. The actual Select application carries its effective arguments and SelectionSlot binding under §4.1. Dated selection Work and an A.10 provenance account retain their independent grounds.
* **Transformation-flow use:** an E.18 node cites this declaration. Planned refs use A.15.3 typed filling only for independently declared receiving positions; actual Select bindings remain governed by §4.1.
* **Failure mode:** tri‑state guard (`pass|degrade|abstain`); missing or unknown evidence never coerces to `pass`.
* **Mental model:** `SelectEligibility` gates the step; `Select` applies explicit criteria to set‑valued comparison outcomes; the result is a selected set whose “single winner” behavior must be explicit.

---

## A.19.SelectorMechanism:5 - Archetypal Grounding — informative {#archetypal-grounding-informative}

### A.19.SelectorMechanism:5.1 - Tell {#tell}

When comparisons are partial or set-valued, selection must not pretend there is a single best candidate by default. `SelectorMechanism` makes selection explicit, policy-bound, and replayable: it returns a set unless criteria explicitly demand otherwise.

### A.19.SelectorMechanism:5.2 - Show, U.System example {#show-u-system-example}

**Scenario.** A platform team must pick a set of deployment options for a subsystem under multiple criteria: latency, cost, and regulatory risk. Comparisons are multi-criteria and do not induce a total order.

* `CandidateSetSlot = {OptionA, OptionB, OptionC}`.
* `CriteriaSlot` requires Pareto selection over the three unordered pairs `{A,B}`, `{A,C}`, and `{B,C}`, returns all non-dominated admissible candidates, and preserves the full selected set unless an explicit current criterion requires a singleton.
* The finite upstream comparison-application basis covers all three required pairs:

  * exact `Compare(OptionA, OptionB, ...)` has `GuardDecision = pass`: OptionB is strictly better than OptionA on latency, while OptionA is strictly better than OptionB on cost under the declared comparator. Its `ComparisonResultSlot` records those strict opposite wins, so neither dominates the other;
  * exact `Compare(OptionA, OptionC, ...)` has `GuardDecision = degrade` because OptionC lacks the required risk attestation, and its output binding contributes no relation token about OptionC; and
  * exact `Compare(OptionB, OptionC, ...)` has the same explicit `degrade` basis and likewise contributes no relation token about OptionC.

  The Selector's `ComparisonResultSlot` argument is exactly the union of those justified member outputs, so its two tokens both trace to the `{A,B}` CPM application. No equality, worse-than, or `abstain` token is fabricated for OptionC.
* `MinimalEvidenceSlot?` is absent, so evidence is evaluated against `CGSpecSlot.MinimalEvidence`.
* The actual selection binds the three exact CPM applications and their pair, eligibility, and output bindings; the required-pair coverage and token trace; the deployment-option claim scope and selected regulatory `U.ContextSlice` members; the same predicate basis or explicit `none`; the reference plane and evaluation interval; and a `degrade` policy that permits exclusion of OptionC.

**Outcome.**

* Under that explicitly bound `degrade` policy, `SelectEligibility` returns `degrade`, excludes OptionC without coercing unknown evidence, and `SelectionSlot` returns `{OptionA, OptionB}`.
* If either required comparison involving OptionC instead had `GuardDecision = abstain`, that basis member would have no output binding, `SelectEligibility` would return `abstain`, and no selected-set value would be created. Neither guard value is a member of `ComparisonResultSlot` or `SelectionSlot`.
* The dated selection `U.Work`, actual `Select` application, finite CPM application basis, evidence-policy and `SelectionSlot` bindings, and A.10 evidence-provenance path preserve why the reduced-set branch proceeded and why the abstain branch did not.

### A.19.SelectorMechanism:5.3 - Show, U.Episteme example {#show-u-episteme-example}

**Scenario.** A methods group selects a declared set of analysis methods for a task. Candidates are method family refs. The group wants diversity in the selected set, but does not want diversity metrics to silently become dominance criteria.

* `CandidateSetSlot` = `{Family1, Family2, Family3, Family4}`
* The selection conditions declare which binary method-family comparisons are required. A finite basis identifies every relied-on CPM application, its exact pair, eligibility value, and own output binding; the Selector's `ComparisonResultSlot` argument is their exact justified-token union.
* `TaskSignatureSlot` is present and is the single policy-default slot or ref:

  * `PortfolioMode` and dominance regime,
  * budgeting and telemetry hooks (when used).
* `CriteriaSlot` declares that diversity signals are telemetry unless explicitly promoted by policy.

**Outcome.**

* `SelectionSlot` returns a selected set; any archive‑style behavior is a specialization and policy choice, not a hidden kernel default.
* The dated selection `U.Work`, actual `Select` application with its `TaskSignatureRef.edition` and `SelectionSlot` bindings, and A.10 evidence-provenance path support later explanation without embedding tool tokens into the kernel.

---

## A.19.SelectorMechanism:6 - Bias-Annotation — informative {#bias-annotation-informative}

This pattern intentionally biases selection authoring toward explicitness and admissibility.

* **Governance bias.** Bias toward explicit criteria and policy-reference records rather than implicit constants. Risk: perceived overhead. Mitigation: keep criteria records minimal, and centralize defaults via `TaskSignatureSlot` when used.
* **Architecture bias.** Bias toward set‑return semantics and against forced total orders. Risk: consumers may expect a single winner. Mitigation: make single‑winner selection an explicit criterion or a declared comparator outcome, not an implicit kernel behavior.
* **Epistemic bias.** Bias toward fail‑closed evidence handling and against unknown coercion. Risk: more `degrade` or `abstain` early. Mitigation: improve evidence pins and policy clarity; do not relax the kernel.
* **Practice bias.** Bias against embedding telemetry and publication into selection. Risk: teams want one step to select and report. Mitigation: keep those relations under their governing patterns; retain replay through dated selection work, the actual `Select` application and result binding, A.10 evidence provenance, and G.11 currentness.
* **Didactic bias.** Bias toward one governing pattern and “Tell + Cite” elsewhere. Risk: refactoring work. Mitigation: the result is a spec that can be read and taught without scavenger hunts.

---

## A.19.SelectorMechanism:8 - Common Anti-Patterns and How to Avoid Them — informative {#common-anti-patterns-and-how-to-avoid-them-informative}

| Anti-pattern                 | What it looks like                                                              | Remedy                                                                                                                                              |
| ---------------------------- | ------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| GateDecision leakage | `Select` emits `GateDecision` or writes a decision log | Keep gate decisions in their governing patterns. `SelectEligibility` remains the mechanism predicate; dated selection work records the realized eligibility value and direct replay basis. |
| Forced single winner         | `Select` always returns exactly one candidate even under incomparability        | Return a declared selected set by default; if single winner is required, make it explicit in `CriteriaSlot` and ensure the induced order is admissible and declared |
| Hidden tie-breakers          | “If incomparable, pick lower cost” without declaring that as policy             | Move tie-breakers into explicit criteria or into declared comparator policies; never embed inside the kernel                                        |
| Scalarization by convenience | Replace set-valued comparison with a scalar “summary score” treated as decisive | Keep summaries report-only unless explicitly declared as admissible comparator outputs                                                                  |
| Unknown coerced to pass      | Missing evidence treated as acceptable                                          | Use tri-state `SelectEligibility`; unknown maps to `degrade` or `abstain`                                                                           |
| Selection does comparison    | Selection stage recomputes scoring or comparison internally                     | Keep comparisons upstream; `SelectorMechanism` binds exact CPM applications and consumes only their justified-token union in `ComparisonResultSlot` |
| One binary comparison treated as a batch | One `Compare(left,right)` application is said to cover three or more candidates, or a token union loses its producing applications | Bind a finite basis of exact binary CPM applications, derive required pair coverage from the selection conditions, and trace every consumed token to a member output |
| Selected set as replay record | Candidate universe, comparison ref, criteria, scope, evidence, or currentness are placed inside `SelectionSlot` | Keep `SelectionSlot` to selected candidates; bind use arguments on the actual application and use direct evidence, provenance, and currentness relations |
| Boundary drift | Selection reuses a token union after comparison-basis membership, coverage, member pair or eligibility, predicate, scope, selected slices, plane, or window changed | Treat it as another selection application and perform the required binary comparisons again when their governed basis changed |
| Publish inside selection | Selection emits a publication or telemetry relation as part of mechanism semantics | Keep publication and telemetry under their governing patterns; dated work and direct relations retain replay |

---

## A.19.SelectorMechanism:10 - Rationale {#rationale}

Selection is where many systems accidentally convert admissible but nuanced information into an unjustified scalar decision. Making selection a separate, explicit mechanism boundary achieves two things that matter for engineering management:

1. **Technical integrity:** it enforces admissibility and evidence discipline at the decision boundary without smuggling heuristics.
2. **Organizational clarity:** it makes defaults and thresholds discussable, reviewable, and maintainable as explicit policy references.

The set‑returning default is not a preference for large retained sets; it is a correctness safeguard when the order is not total. Single‑winner outcomes remain possible, but only by explicit criteria or declared admissible comparators.

---

## A.19.SelectorMechanism:11 - SoTA-Echoing {#sota-echoing}

**SoTA vs popular note.** This section records alignment to post‑2015 evidence‑backed practice. It is not a mandate to use fashionable methods; method semantics stay in SoTA packs (`G.2`) and wiring modules, while this pattern fixes the stable selection boundary.

Concrete selector-family SoTA packages are cited through their current Part G pack or claim sheet when one governs the use. They connect through `CriteriaSlot` and `TaskSignatureSlot` references while kernel semantics remain unchanged.

### A.19.SelectorMechanism:11.1 - SoTA alignment map (normative) {#sota-alignment-map-normative}

| SoTA practice pointer, post‑2015+                                                                               | Primary source examples, post‑2015+                                                                           | Where it connects to SelectorMechanism                                                                             | Adoption status |
| --------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------ | --------------- |
| Treat the Pareto set or declared selected set as a first-class output under multi-criteria partial orders       | Quality Diversity as a decision framing, e.g., Pugh et al. 2016; Vassiliades et al. 2018                      | Expressed as set‑return default and explicit set-return criteria; method details live in specializations and wiring | Adapt           |
| Use archive-based retained sets where diversity is part of the result, but do not silently promote it to dominance | Modern QD and archive practices post‑2015, including map-elites descendants and archive insertion policies | Expressed as policy‑bound criteria and report‑only telemetry unless explicitly promoted                            | Adapt           |
| Pair environments and methods in open-ended or co-evolutionary settings without breaking kernel semantics       | Open-ended environment-method pairing, e.g., Wang et al. 2019 and successors                                  | Expressed as candidate and criteria structuring plus admissible specializations; kernel unchanged                      | Adapt           |
| Include an explicit abstain or reject option under uncertainty rather than forcing a decision                   | Selective prediction and rejection-option practice, e.g., Geifman and El‑Yaniv 2017; follow-on selective nets | Expressed as tri-state `SelectEligibility` with fail-closed discipline                                             | Adopt           |
| Keep architecture commitments traceable to one governing pattern                                                        | ISO/IEC/IEEE 42010:2022 architecture description discipline                                                   | Expressed as explicit governing-pattern assignment and Tell+Cite stubs elsewhere                                             | Adopt           |

**Notes per row** (1–2 sentences; why to adopt, adapt, or reject):
* **Selected-set-as-output (QD framing):** adopt the *decision framing* (declared selected set as a first-class result) while keeping concrete QD or retained-set algorithms out of the kernel; they belong in `G.2` packs and wiring modules, preserving evolvability.
* **Archive retained sets (diversity as result):** adapt archive thinking by keeping diversity and illumination signals report‑only unless an explicit CAL policy promotes them to dominance; this prevents silent scalarization and preserves governing-pattern defaults (typically `G.5` and CAL).
* **Open‑ended environment–method pairing:** keep the kernel unchanged; open‑ended pairing is expressed by shaping candidates and criteria (and, when needed, admissible specializations `⊑` and `⊑⁺`) with explicit edition pins and transfer and validity rules in planned baseline, not by mutating `Select`.
* **Reject or abstain under uncertainty:** adopt the rejection‑option stance as a tri‑state guard with fail‑closed semantics; explicit abstain is preferable to forced choice under missing admissibility and evidence.
* **Governing-pattern architecture discipline:** adopt governing-pattern + Tell‑and‑Cite to keep the spec teachable and reviewable; this directly reduces drift and “second centers of gravity”.

---

### A.19.SelectorMechanism:11.2 - Currentness and smallest reopen rule {#currentness-and-smallest-reopen-rule}

**Qualification basis and window.** The stable kernel claim is qualified by the current editions of A.6.1 operation declarations and actual binding rules, A.19.CPM binary application and output semantics, A.19.CN and G.0 admission and evidence rules, G.5 selector-policy discipline, A.2.6 scope semantics, and the exact current G.2 selector pack or claim sheet cited by an actual use. For that use, the effective qualification window is the intersection of those bound editions' currentness and any validity interval declared by the selector pack, TaskSignature, or policy; `post-2015+` is an orientation label, not an indefinite freshness claim.

**Reopen the SelectorMechanism kernel only when.** Reopen the smallest affected selector rule when a direct governor changes set-return semantics, inherited SlotKinds or specialization constraints, criteria or policy binding, tri-state eligibility, the finite CPM application-basis and token-provenance boundary, selection scope, or the separation of selected set, evidence, provenance, result episteme, and publication, or when qualified evidence contradicts one of those commitments. A new selection algorithm, archive or diversity method, candidate-generation method, tie-breaker, `PortfolioMode`, rejection calibration, or domain policy that still satisfies those commitments changes its G.2 pack, G.5 policy, `CriteriaSlot`, `TaskSignature`, or other direct policy binding rather than this kernel.

**Smallest affected locus.** A signature, basis, coverage, or output change reopens only the corresponding direct-signature, selection-use-binding, `OperationAlgebra`, or `LawSet` passage in `A.19.SelectorMechanism:4.1`; an admissibility or failure-semantics change reopens the matching `AdmissibilityConditions` clause. Update only the nearest exercising case in `A.19.SelectorMechanism:5.2` or `:5.3` and the corresponding `CC-A19SelectorMechanism` row. Source-family or policy churn that changes no kernel commitment updates the direct pack, policy, or claim sheet and, when its summary is stale, only the affected row or note in this SoTA map.


## A.19.SelectorMechanism:End {#end}
