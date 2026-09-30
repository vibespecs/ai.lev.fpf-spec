# A.19.CPM - Compare Admitted Profiles under a Declared Comparator (CPM) {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Architectural (A)
> **Status:** Stable
> **Normativity:** Normative (unless explicitly marked informative)
> **Placement:** Part A, CN-Spec cluster (A.19), CHR mechanism-governing patterns
> **Source:** FPF, CHR mechanism-governing patterns
> **Modified:** 2026‑01‑20
>
> **Governing-pattern note:** this pattern governs the canonical `U.Mechanism` declaration for `CPM.IntensionRef` (CHR suite stage `compare`). Mechanism-intension semantics are governed by explicitly designated governing patterns (`E.20`).
> `A.6.1` governs the semantic content of a `U.Mechanism` declaration. This pattern specialises that content for CPM through the exact `EntityOfConcernRef`, effective `U.ReferenceScheme`, operation-local argument/result declarations, `OperationAlgebra`, `LawSet`, `AdmissibilityConditions`, Applicability, and an optional `SignatureManifest`. An obtaining F.9 `Bridge`, its separate C.2.1 bounded-use claim when consumed, any applicable ReferencePlane relation and policy, dated comparison `U.Work`, actual `Compare` operation application with its `ComparisonResultSlot` binding, an A.10 account of exact sources, independently established support relations, currentness and bounded use, G.11 currentness relation, and optional G.9 `ParityPlan` and `ParityReport` remain neighboring objects and relations.
> Other descriptions of CPM cite `A.19.CPM:4.1` rather than restating its declaration content or absorbing those named neighboring objects and relations into mechanism fields.

## A.19.CPM:1 - Problem frame {#problem-frame}

FPF's Characterization (CHR) suite treats comparison as a **distinct** mechanism stage (`compare`) with suite‑wide obligations that forbid hidden scalarization or totalization, require tri‑state guards, and enforce admissibility declarations for numeric operations. Comparison must therefore be described as:

* a **mechanism** (an operation declaration under `A.6.1`),
* that is **suite‑conformant** (per CHR obligations and protocol closure in `A.19.CHR`),
* and **governing-spec-ref-respecting** (comparability and admission are governed by `CN-Spec` and admissibility is gated by `CG-Spec` rather than re-invented locally).

Within suite protocols, CPM appears as the explicit `compare` stage: it consumes admitted left and right profiles, including scores and folded measures when those upstream stages are present, and produces an admissible, replayable comparison result that downstream selection can consume without CPM smuggling selection or scoring semantics into comparison.

## A.19.CPM:2 - Problem {#problem}

Engineering teams frequently need to compare two options (designs, methods, vendors, trajectories, hypotheses, etc.) across multiple measures and under incomplete evidence. Without a canonical comparison mechanism, teams predictably fall into one or more of these failure modes:

* **Hidden scalarization:** forcing a single number (or a single winner) from multi‑criteria reality, erasing incomparability and ties.
* **Silent totalization:** inventing an implied total order by convenience tie‑breakers or implicit thresholds, even when only a partial order is warranted.
* **Inadmissible arithmetic:** comparing across measures using operations that are not scale-admissible (CSLC‑violating) or not admitted by the declared admissibility frame.
* **Comparator drift:** “the comparator” exists only as prose or code intuition; different teams compare the same option set and measure set differently because the comparator spec is not explicit and edition‑pinned.
* **Unknown coercion:** missing or unknown evidence is coerced into an outcome (e.g., `missing = equal`), producing comparisons that look decisive but are epistemically unsafe.
* **Comparison-boundary drift:** the same result label is reused after the profile pair, comparator, A.19 predicate, claim scope, selected context slices, reference plane, or evaluation window changed.
* **Cross-scheme or cross-plane leakage:** a comparison relies on a semantic relation between two exact F.17 `SchemeSenseCell` values without an obtaining F.9 `Bridge` and its separate bounded-use claim, or crosses exact ReferencePlanes without the applicable plane relation and policy. The relation or policy needed by the comparison is then unrecoverable.

CPM exists to make comparison explicit, admissibility-gated, set-valued, and replayable, so downstream selection can remain a separate policy-bound step.

## A.19.CPM:3 - Forces {#forces}

1. **Usability vs correctness:** engineers want a "simple compare" function; correctness demands explicit admissibility, explicit comparator choice, and explicit handling of incomparability and unknown evidence.
2. **Total order convenience vs partial order truth:** total orders simplify downstream selection; partial orders are often the faithful representation (especially in multi‑criteria settings).
3. **Evolvability vs stability:** comparator methods evolve (SoTA churn); kernel semantics and slot field sets must remain stable and wiring‑friendly.
4. **Replayability vs speed of discussion:** teams want fast decisions; replay requires the dated comparison `U.Work`, the actual `Compare` operation application with exact edition, policy, argument, and result bindings, and an A.10 evidence-provenance path.
5. **Cross-scheme reasoning vs Bridge and ReferencePlane discipline:** a comparison that relies on a semantic relation between two exact F.17 `SchemeSenseCell` values requires an obtaining F.9 `Bridge` and a separate C.2.1 bounded-use claim; a plane-only crossing requires the applicable ReferencePlane relation and policy. Neither branch supplies scope, predicate, plane, or time from an umbrella context label.
6. **Avoiding “second centers of gravity”:** mechanism semantics must have a governing pattern; otherwise the suite, `A.6.1` archetypes, and Part‑G wiring drift apart.

## A.19.CPM:4 - Solution {#solution}

CPM is an exact A.6.1 U.Mechanism declaration whose core commitments are:

* **Comparator admissibility is declared and gated** (`CG-Spec.ComparatorSet`, and `CG-Spec.SCP` when numeric operations are involved; scale admissibility via CSLC).
* **Results are set‑valued relation or poset tokens**; partial orders remain partial; no silent scalarization or totalization.
* **Admissibility is tri‑state and fail‑closed** on missing admissibility and evidence; unknown never coerces into a fabricated outcome.
* **Comparison remains distinct from selection**; CPM produces relation outcomes; `SelectorMechanism` consumes them.

This pattern defines (governing-pattern, wiring‑friendly):
1. a **stable mechanism boundary** for admissible comparison: `Compare(...) → ComparisonResultSlot` plus a tri‑state `CompareEligibility` guard;
2. a **stable SlotKind field set** (by suite lexicon tokens) that downstream selection and Part‑G wiring can rely on without SlotKind drift;
3. an **admissibility and evidence responsibility split**: admissibility is gated by `CG-Spec` (and CSLC), while admission and comparability relations are cited from `CN-Spec`;
4. a minimal **replay basis**: the identified Compare application, its actually bound arguments and returned ComparisonResultSlot value, with an A.10 evidence-provenance path when the receiving reliance requires it;
5. **planned and actual use:** an A.15.2 plan selects editions and policies; A.15.3 typed filling applies to independently declared receiving positions. Actual arguments and results belong to the comparison application; a dated U.Work claim is independently governed;
6. an explicit **comparison-use boundary**: claim scope, selected A.2.6 context slices, optional A.19 predicate, reference plane, and evaluation window are occurrence bindings, not generic context, comparator content, output fields, or an optional model-use structure.

### A.19.CPM:4.1 - Operation declaration (normative) {#operation-declaration-normative}

`CPM.IntensionRef` cites the exact A.6.1 declaration episteme presented here. CHR resolves compare to its local Compare operation. A changed argument, comparator law or guard requires explicit selection of the changed declaration; another realizer of the same declaration changes no suite member.

* **Declaration boundary:** this A.6.1 mechanism intension declares `Compare` and `CompareEligibility`; it does not publish telemetry or create dated work, an actual operation application, comparison scope, result episteme, evidence use, provenance path, currentness relation, or publication relation. Each neighboring object or relation uses its direct governor.
  * **Planned use:** A.15.2 selects the editions and policies for a proposed comparison. If a receiving position is independently declared, A.15.3 can specify its planned filling. Neither plan asserts an actual Compare argument or result binding.

* **IntensionHeader:** `id = CPM`, `version = 1.0.0`, `status = stable`.

* **IntensionRef:** `CPM.IntensionRef` designates this `U.Mechanism` episteme as the canonical suite member named in `A.19.CHR:4.2`; it is not the `EntityOfConcernRef` of the declared operation family.

* **SignatureManifest (optional; importability):** if a CPM publication is intended for reuse beyond the CHR suite, author SHOULD publish a `SignatureManifest` that records (i) the declared `Compare` stage‑op signature, (ii) the SlotKind field set (by lexicon tokens), and (iii) the explicit set‑valued output commitment (no silent scalarization or totalization).

* **Tell.** Lawful comparison producing **set‑valued** parity or poset outcomes (not a single scalar).

* **Purpose:** admissible comparison producing **set‑valued** parity or poset outcomes (not a single scalar).

* **Imports:** `G.0 (CG‑Spec.ComparatorSet, CG‑Spec.SCP, CG‑Spec.MinimalEvidence)`, `A.18 (CSLC)`, `A.19.CN (comparability and admission declarations)`, `A.19.CHR:4.2.1 (CHR SlotKind Lexicon)`.

* **EntityOfConcernRef:** the comparison operation family declared by `Compare` and `CompareEligibility` in this section.

* **Effective `U.ReferenceScheme`:** the CHR suite reference scheme in which the A.19.CHR SlotKind lexicon, CN-Spec, CG-Spec, and ComparatorSpec tokens are interpreted.

* **Direct signature components:**

  * **SubjectKind:** `U.Measure`, supplied by the measures in the left and right profiles.
  * **RangedValueKind:** CHR-typed profile values in a CG-Frame (see `CG-Spec.ComparatorSet`).
  * Results are declared per operation: a set of relation/poset tokens and a separate eligibility judgment.
  * Input qualification: comparison ranges over admitted left/right profiles in one exact U.ClaimScope. The selected U.ContextSlice values are its members under A.2.6; these qualifications do not define the calculation extent or add a duplicate membership relation.

  These are direct A.6.0 declaration components. They do not form an additional comparison-content container, and they do not absorb comparator admission, evaluation, evidence-use, or replay relations.

**Operation-local argument and result declarations**

Each argument meaning is declared separately for Compare and CompareEligibility. ByRef means one exact governed reference to the stated value and edition; ByValue carries the value itself. Cardinality is per application. A guard can assess an incomplete proposal with 0..1 of each required argument; a missing argument has no binding and prevents pass.

| Direction | Local designator | Meaning and ValueKind | Designation; cardinality |
| --- | --- | --- | --- |
| Argument | LeftProfileSlot | Left operand: set of U.Measure values with their exact basis positions, Characteristic and Scale | ByValue; 1 profile |
| Argument | RightProfileSlot | Right operand of the same kind, matched by the comparator or a separately justified basis mapping | ByValue; 1 profile |
| Argument | CNSpecSlot | CN-Spec governing admission and comparability of the operand pair | CNSpecRef; 1 |
| Argument | CGSpecSlot | CG-Spec governing comparator admission, SCP and default evidence conditions | CGSpecRef; 1 |
| Argument | ComparatorSpecSlot | ComparatorSpec supplying the comparison rule and any thresholds or tie-breakers | ComparatorSpecRef; 1 |
| Argument | MinimalEvidenceSlot | MinimalEvidence override used instead of CGSpecSlot.MinimalEvidence | MinimalEvidenceRef; 0..1 |
| Argument | claimScope | U.ClaimScope delimiting this profile pair and comparison claim | ByRef; 1 |
| Argument | selectedSlices | Set of selected U.ContextSlice members of claimScope under A.2.6 | ByValue set of exact slice references; 1 set |
| Argument | characteristicPredicate | A.19 CharacteristicSpacePredicate used to restrict this comparison, if any | ByValue; 0..1, explicitly absent when unused |
| Argument | referenceScheme | Effective U.ReferenceScheme used to interpret the comparison | ByRef; 1 |
| Argument | referencePlane | CHR:ReferencePlane value qualifying the comparison | ByValue; 1 |
| Argument | evaluationTime | Evaluation point or interval in the declared time basis, qualifying what is compared | ByValue; 1 |
| Compare result | ComparisonResultSlot | Set of relation or poset tokens returned by the declared comparator | ByValue; 1 set on completed admitted comparison, 0 without a result |
| CompareEligibility result | GuardDecision | Judgment determined by the eligibility predicates: pass, degrade or abstain | ByValue; 1 on completed evaluation |

The **argument bindingPredicate** for each row holds when that application actually uses the resolved value for the row's meaning: operand, comparison/admission rule, evidence condition or explicit comparison-use restriction. In particular, a scope, predicate or time appearing in nearby metadata is not bound unless it qualifies this comparison/evaluation. Each indicator-derived profile retains its selected UINDM positions and exact A.19 basis; equal indices or Characteristic names alone do not establish the comparator's required position/Scale match.

The **ComparisonResultSlot bindingPredicate** holds when that Compare application returns the comparator's lawful set-valued outcome for its bound operands and use restrictions. The guard's result predicate holds when that CompareEligibility application returns its evaluated judgment. Type compatibility, equal tokens or a copied audit record establish neither return. A.6.1 governs binding identity and continuous extent within the application; result binding begins at return. Evidence use and a result episteme remain separate relations or objects.

**SlotIndex (derived projection).** Project the above designators, ValueKinds, designation and cardinalities; the historical Slot suffix supports CHR lookup. The comparison-use arguments are declaration-local names, not new CHR SlotKinds. A.6.5 relation SlotSpecs are not the source of these operation meanings.

**OperationAlgebra.** The compare stage resolves to Compare with the six profile/specification arguments and the explicit comparison-use arguments above, returning ComparisonResultSlot. CompareEligibility uses those argument meanings to return GuardDecision.

**ApplicationPredicate.** Compare obtains when a comparison act actually applies the bound comparator to the bound left/right profiles under the bound scope, slices, optional predicate, scheme, plane and evaluation time, with its admission conditions satisfied by pass or an explicitly permitted degrade branch. A completed act returns the comparator's token set. CompareEligibility obtains when an evaluation actually assesses that proposal under the guard predicates and returns its judgment. An unexecuted proposal, passing guard or compatible saved token set does not establish a Compare act.

**ApplicationIdentityRule.** One application is one comparator invocation or guard-evaluation invocation at its calculation locus, from taking up its operands/rules through return or termination. Reidentification requires that same episode. Two independently begun invocations are distinct even if all their bindings and results agree. Law 7 also distinguishes a newly evaluated comparison after any listed binding changes; it cannot mutate a completed earlier application.

**ApplicationExtentRule.** Compare extends from actual use of the chosen operand pair under the comparator to token-set return or termination; CompareEligibility extends from proposal assessment to judgment or termination. An unfinished act has an open extent and no unreturned result binding. These actual calculation intervals can occur after, and can be repeated for, the same evaluationTime. A trace identifier only designates an established episode. Ordinary comparison mathematics creates no dated U.Work claim.

For example, an admitted Pareto comparison takes supplier A with cost 10 and quality 0.8, and B with cost 12 and quality 0.9, under declared lower-cost/higher-quality criteria. Neither dominates the other. Two separate invocations for the same procurement evaluation interval can return the same incomparability token set, while each has its own application and result binding. A stored compatible set does not determine which invocation returned it; the claimed binding requires that invocation's actual return. Describing the first comparison twice still identifies one application.

* **LawSet** (minimum; set-valued comparison, no hidden scalarization):

  1. **ComparatorSet gate:** `ComparatorSpecSlot` MUST be an element of `CGSpecSlot.ComparatorSet` (admissibility gate; cite `G.0`).
  2. **Set‑valued semantics:** `ComparisonResultSlot` is set‑valued (parity or poset tokens); partial orders remain partial — no silent totalization or scalarization.
  3. **CSLC+SCP admissibility:** any numeric ops implied by the comparator MUST be admissible under `CGSpecSlot.SCP` and CSLC-admissible (cite `G.0` + `A.18`).
  4. **Unknown is not coerced:** missing or unknown evidence MUST NOT be mapped to a comparison outcome; use tri‑state guards.
  5. **No hidden thresholds or tie-breakers:** any thresholds, epsilons, priority orders, or tie-break logic MUST live in the declared `ComparatorSpecSlot`, or in `CNSpecSlot.acceptance` as explicit acceptance clauses, and be edition-pinned for replay; CPM MUST NOT smuggle constants.
  6. **No implicit UNM:** CPM does not normalize or align internally. Normalization-based comparability requires already-normalized inputs, exact upstream refs and preservation of the distinctions used by this comparator. If it consumes classes, its query must be constant on them; an inherited operation needs its compatibility/availability argument. Missing support yields `degrade` or `abstain` under the declared rule.
  7. **No silent boundary change:** a `Compare` application does not silently change its profile pair, `U.ClaimScope`, selected context slices, optional A.19 predicate, comparator, reference scheme or plane, or evaluation window. A changed binding is a different application and requires a newly evaluated outcome.

* **AdmissibilityConditions** (tri‑state guard; fail‑closed on missing admissibility and evidence):

  * `CompareEligibility(LeftProfileSlot, RightProfileSlot, CNSpecSlot, CGSpecSlot, ComparatorSpecSlot, MinimalEvidenceSlot?; comparison-use bindings) → GuardDecision ∈ {pass|degrade|abstain}`.
  * `pass` requires: (i) comparator admission; (ii) scale-admissible operations; (iii) admitted and comparable profiles under the exact claim scope and selected A.2.6 context slices; (iv) an explicit evaluation point or interval and reference plane; (v) the same by-value A.19 predicate when one is used; and (vi) satisfaction of the effective MinimalEvidence policy.
  * If `CNSpecSlot.comparability` is normalization‑based (compare‑on‑invariants), `pass` additionally requires that the inputs are already in the required invariant and normalization regime and that the declared comparator can recover its answer from those results; CPM MUST NOT “make them comparable” by silent normalization.
  * If `MinimalEvidenceSlot` is absent, the guard MUST evaluate evidence against `CGSpecSlot.MinimalEvidence` (by explicit rule), and MUST NOT return `pass` when evidence is missing or unknown **or** fails the effective MinimalEvidence gate.

* **Applicability:**

  * Intended for the CHR stage `compare`: it may follow indicatorization or scoring and optional folding when those stages are present, and it precedes selection wherever selection occurs. It remains distinct from selection.
  * Applicable only when `CGSpecSlot` supplies the current admissibility and evidence-policy declarations. Missing declarations fail closed.
  * Inside the CHR suite, `A.19.CHR:4.5` alone determines stage ordering and optionality; CPM does not infer order from `mechanisms[]`.
  * Every actual comparison binds one exact `U.ClaimScope`, selected A.2.6 `U.ContextSlice` members, optional A.19 predicate, effective reference plane, and explicit evaluation point or interval. There is no implicit latest value and no default window inherited from the predicate.
  * When a comparison relies on a semantic relation between two exact F.17 `SchemeSenseCell` values, test the F.9 `BridgePredicateProfile`, cite the Bridge only when its direct predicate obtains, and state a separate C.2.1 bounded-use claim. If the predicate is false or unresolved and that semantic relation is required, `CompareEligibility` cannot be `pass`; follow the declared `degrade` policy when applicable, otherwise `abstain`. A plane-only crossing instead cites the applicable ReferencePlane relation and policy. If both facts are current, state both under their own predicates. Neither branch supplies claim scope, selected slices, predicate, comparator, or evaluation time.

* **Neighboring F.9 Bridge, C.2.1 bounded-use claim, and ReferencePlane relation and policy:**

  When profiles require interpretation across different semantic contexts, resolve the two exact F.17 `SchemeSenseCell` endpoints and test one F.9 `BridgePredicateProfile`. For an obtaining Bridge, state its exact endpoints and profile separately, then state suitability for the named comparison use in a C.2.1 assertion whose EntityOfConcern is that Bridge and whose ClaimGraph carries `<u,d,r,t>` and polarity. Include `CL` or an observed-loss note only when the receiving use consumes it; permitted loss remains `t` in the bounded-use claim. For a ReferencePlane crossing, cite the applicable plane relation and policy separately. Open A.10 only when bounded reliance is current and B.3 only when an actual named assurance claim is current. If that assurance argument consumes a locally declared `R_eff` calculation, cite its applicable domain model and calculation; neither the Bridge nor `CL` creates a penalty. Adding or changing any of these neighboring facts does not by itself change the CPM declaration.

* **Neighboring dated work, operation application, result binding, and evidence relations:**

  The identified Compare application binds the profile pair, comparator, comparison-use arguments, policies and returned ComparisonResultSlot. If the account also asserts dated comparison U.Work, A.15.1 independently admits that performance; its identity and extent are not automatically those of one Compare application. When the account asserts them or the receiving use consumes them, A.2.4 governs evidence use with its own evidence claim scope and relevance window, A.10 governs the evidence-provenance path and local `RelianceDisposition` for the same bounded use, and G.11 governs source or assertion-edition currentness. A durable result episteme, when needed, is governed by C.2.1, and any current entity-identity inception claim by A.15.PROD. No universal work-result or comparison-result relation is presumed. To replay the comparison, recover:

  * the two profile values or exact upstream refs, one `U.ClaimScope`, selected A.2.6 context slices, optional A.19 predicate, effective reference scheme and plane, and evaluation point or interval;
  * `CNSpecRef.edition`, `CGSpecRef.edition`, and the effective `ComparatorSpecRef`;
  * the effective MinimalEvidence policy, either the explicit override or `CGSpecSlot.MinimalEvidence`;
  * the realized `GuardDecision` and, for `degrade` or `abstain`, any current downstream-handling policy;
  * the effective upstream normalization dependency, or the explicit absence that caused degradation or abstention;
  * the comparison result; any obtaining F.9 `Bridge` and separate C.2.1 bounded-use-claim refs actually consumed by this occurrence; any optional `CL` or observed-loss-note ref actually used; any applicable ReferencePlane relation and policy refs; and, only when the comparison consumes an actual named assurance claim, that claim's B.3 `AssuranceResult` and declared domain-model and calculation refs.

  Use G.9 when a parity or benchmark use requires a stable run package and report record. These neighboring records support replay; none is CPM declaration content.

### A.19.CPM:4.2 - Interpretation notes — informative {#interpretation-notes-informative}

* **The output is a value, not a replay container.** The by-value set bound to `ComparisonResultSlot` contains relation or poset tokens only. Comparator, scope, predicate, plane, window, eligibility, evidence use, provenance, and currentness remain separate bindings or relations.
* **Set-valued output is the default, not a loophole.** “Set‑valued” means CPM preserves incomparability, ties, and partiality as first‑class outcomes; it does not authorize silent post‑processing into a scalar or a single winner.
* **Total orders are allowed only if declared by the comparator.** If a `ComparatorSpec` defines a total order, CPM still outputs a (singleton) set of relation tokens; the totalization is a property of the declared comparator, not an implicit kernel default.
* **Normalization is not smuggled into comparison.** If `CN‑Spec.comparability` declares normalization‑based invariants for comparison, that dependence must be represented explicitly via the suite protocol and, where needed, explicit Uses contours (CPM consumes admitted profiles; it does not silently normalize them).
* **Thresholds and tie-breakers are never kernel constants.** If thresholds exist, they belong to explicit policies or specs such as `ComparatorSpec` and `AcceptanceClauses`, are edition-pinned, and are recorded by the dated comparison occurrence for replay.

## A.19.CPM:7 - Conformance Checklist {#conformance-checklist}

Apply the declaration checks to a CPM publication and the application checks to an actual use, together with the applicable A.6.1 checks and, for CHR membership, `A.19.CHR:4.3`. Replay always requires the actual application and its local bindings. Neighboring Work, evidence-use, reliance, currentness and result-episteme checks apply only when the account asserts those objects or the receiving use consumes them:

| Check Id | Requirement (normative) | Notes (didactic and evidence) |
| :--- | :--- | :--- |
| **CC-A19CPM-0** | @fact:CC-A19CPM-0 **Mechanism declaration completeness.** One `U.Mechanism` episteme, its exact comparison-operation-family `EntityOfConcernRef`, effective `U.ReferenceScheme`, operation-local argument/result declarations, `OperationAlgebra`, `LawSet`, `AdmissibilityConditions`, Applicability, and optional `SignatureManifest` are recoverable. @status:spec/done | An obtaining F.9 `Bridge`, its separate C.2.1 bounded-use claim when consumed, any applicable ReferencePlane relation and policy, dated `U.Work`, actual operation application and result binding, any result episteme, A.10 evidence-provenance, G.11 currentness, and G.9 parity objects remain separate. |
| **CC‑A19CPM‑1** | **Single governing pattern.** The canonical CPM intension is governed here (`A.19.CPM:4.1`); other descriptions cite this section rather than restating the kernel law. | Prevents near-duplicate comparison semantics from drifting. |
| **CC‑A19CPM‑2** | **Suite stage alignment.** `Compare` is the canonical stage‑op for CHR stage `compare`; ordering and optionality are taken only from `A.19.CHR:4.5`. | Never infer order from `mechanisms[]`. |
| **CC‑A19CPM‑3** | **SlotKind discipline.** SlotKind tokens follow the suite lexicon (`A.19.CHR:4.2.1`). | No SlotKind drift across specializations and wiring. |
| **CC‑A19CPM‑4** | **Comparator admissibility gate.** `ComparatorSpecSlot ∈ CGSpecSlot.ComparatorSet` is enforced (fail-closed otherwise). | Admissibility is declared, not improvised. |
| **CC‑A19CPM‑5** | **Scale admissibility.** Any numeric operations implied by the comparator are admissible under `CGSpecSlot.SCP` and CSLC-admissible. | “Weighted sum” etc must be explicitly admissible. |
| **CC‑A19CPM‑6** | **Set‑valued semantics.** Outputs remain set‑valued; no silent scalarization or totalization is introduced. | Incomparability and ties are first‑class outcomes. |
| **CC‑A19CPM‑7** | **Tri‑state admissibility (fail‑closed).** `CompareEligibility(...) → {pass|degrade|abstain}` exists and does not return `pass` on missing admissibility and evidence. | Unknown never coerces to `pass`. |
| **CC‑A19CPM‑8** | **MinimalEvidence defaulting is explicit.** If `MinimalEvidenceSlot?` is absent, the effective evidence policy is `CGSpecSlot.MinimalEvidence` by explicit rule. | Avoid “implicit evidence policy.” |
| **CC‑A19CPM‑9** | **Gate and guard separation + lexeme discipline.** CPM does not publish `GateDecision` nor `DecisionLog`; mechanism predicates use `…Eligibility` (not reserved gate `…Guard`). | Aligns with suite obligations (`gate_decision_separation`, `guard_lexeme_reservations`). |
| **CC-A19CPM-10** | @fact:CC-A19CPM-10 **Bridge and reference-plane discipline.** A comparison that relies on a semantic relation between two exact F.17 `SchemeSenseCell` values cites an obtaining F.9 `Bridge` under a satisfied `BridgePredicateProfile` and a separate C.2.1 bounded-use claim; a plane-only crossing cites the applicable ReferencePlane relation and policy; both are stated when both facts are current. @status:spec/done | `CL` is optional. CPM supplies no default assurance penalty, fold, or `R_eff`; a local `R_eff` is admissible only for an actual named assurance claim under its declared domain model and calculation. These neighboring facts are not CPM declaration content. |
| **CC-A19CPM-11** | @fact:CC-A19CPM-11 **Replay basis completeness.** The actual `Compare` application and its profile, comparator, `U.ClaimScope`, selected A.2.6 context-slice, optional A.19 predicate, reference-scheme and plane, evaluation-window, policy, eligibility and returned `ComparisonResultSlot` bindings (or explicit absence) are recoverable. @status:spec/done | If asserted or consumed, independently recover dated comparison Work under A.15.1, evidence use under A.2.4, reliance and provenance under A.10, currentness under G.11 and a result episteme under C.2.1. These facts remain outside the output value. |
| **CC-A19CPM-12** | @fact:CC-A19CPM-12 **Planned-filling separation.** An A.15.2 baseline selects intended editions and policies; A.15.3 typed filling applies only to independently declared positions. Actual Compare applications carry their effective argument and result bindings. @status:spec/done | A dated comparison Work and any relied-on A.10 provenance remain separately established. |
| **CC-A19CPM-13** | @fact:CC-A19CPM-13 **No implicit UNM.** CPM uses the explicit upstream directed result and preservation/loss basis. A class-level comparison also passes its query/operation conditions under A.19.UNM; a reference or equal normalized numeral alone is insufficient. Unsupported comparisons follow `abstain` or the declared narrower `degrade` use. @status:spec/done | Keeps compare-on-invariants explicit. |
| **CC-A19CPM-14** | @fact:CC-A19CPM-14 **Comparison-scope completeness.** Every actual application binds one exact profile pair, `U.ClaimScope`, selected A.2.6 context slices, optional A.19 predicate, effective reference scheme and plane, and explicit evaluation point or interval. @status:spec/done | No generic context input, optional model-use structure, or label supplies these values. |
| **CC-A19CPM-15** | @fact:CC-A19CPM-15 **Outcome separation.** `ComparisonResultSlot` contains only the by-value set of relation or poset tokens; `GuardDecision` remains the separate eligibility value, and abstention fabricates no output token. @status:spec/done | Comparator, scope, plane, window, evidence, provenance, currentness, result episteme, and selection remain separate. |
| **CC-A19CPM-16** | @fact:CC-A19CPM-16 **No generic result relation.** The actual A.6.1 operation application binds the output; C.2.1 governs a durable result episteme when needed; direct subject patterns govern any other result relation. @status:spec/done | CPM mints no universal comparison-result or work-result link. |

## A.19.CPM:9 - Consequences {#consequences}

* **Improved usability (didactic):** CPM gives a single, engineer‑readable place to learn “what admissible comparison means” and what it does *not* mean.
* **Higher replayability:** comparison results remain traceable through dated comparison `U.Work`, the actual `Compare` application and its `ComparisonResultSlot` binding, the A.10 evidence-provenance path, any consumed obtaining F.9 `Bridge` with its separate bounded-use claim, and any applicable ReferencePlane relation and policy.
* **Reduced semantic drift:** teams cannot silently shift from Pareto to lexicographic to “weighted sum” without changing explicit comparator specs and pins.
* **Explicit tradeoffs:** set‑valued outcomes force downstream reasoning to acknowledge incomparability and uncertainty rather than hiding them.
* **Cost:** downstream consumers (notably selection) must handle sets, abstentions, and partial orders explicitly. This is intentional: it moves complexity from hidden heuristics into explicit policy‑bound mechanisms.

## A.19.CPM:12 - Relations {#relations}

**Builds on and cites (non‑exhaustive):**

* `A.6.1` (operation declarations and actual application/binding rules)
* `A.6.1 §4.2` (operation-local argument/result meanings and binding rules; SlotIndex projects those declarations)
* `A.19.CHR` (suite membership + obligations + `suite_protocols`; CHR SlotKind lexicon)
* `A.15.2` for the edition/policy baseline; `A.15.3` plus `A.19.CHR:4.7.2` for typed filling of independently declared positions.
* `A.19` for `CharacteristicSpace` and the optional by-value `CharacteristicSpacePredicate` used by one comparison
* `A.2.6` for `U.ClaimScope` identity and exact `U.ContextSlice` membership
* `A.19.CN` for CN-Spec comparability plus acceptance and admission declarations
* `G.0` (CG‑Spec: `ComparatorSet`, `SCP`, `MinimalEvidence`, CL and ReferencePlane framing)
* `A.18` (CSLC scale admissibility)
* `C.27.TA` for an explicit comparison-evaluation point or interval
* `A.2.4`, `A.10`, and `G.11` for evidence-use scope, provenance, and currentness, separately from comparison scope and outcome
* `E.10` (lexical and ontological authoring rules; kind suffix discipline)
* `E.19` (checks; authoring discipline)
* `E.20` (governing-pattern discipline)
* `F.18` (alias docking; ID continuity)
* `E.18` (project transformation-flow structures consume CPM instances; CPM does not create a parallel “card deck”)

**Relates to (typical named patterns in the CHR Uses contour):**

* `UNM.IntensionRef`, `UINDM.IntensionRef`, `USCM.IntensionRef`, `ULSAM.IntensionRef`, and `SelectorMechanism.IntensionRef` (downstream consumer of CPM results).
* `G.5` (selection conformance), `G.9` (parity and benchmark harness), `G.10` and PTM (publication and telemetry outside suite closure).


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/A-19-CN#root, spec://ai.lev/fpf-spec/contract/A-6-1#root, spec://ai.lev/fpf-spec/contract/A-6-5#root, spec://ai.lev/fpf-spec/contract/A-19-CHR#root, spec://ai.lev/fpf-spec/contract/G-0#root, spec://ai.lev/fpf-spec/contract/A-18#root. @status:spec/done
- @fact:USED-BY Used by: spec://ai.lev/fpf-spec/contract/A-19-CHR#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: UNM, USCM, ULSAM, SelectorMechanism, spec://ai.lev/fpf-spec/contract/G-2#root, spec://ai.lev/fpf-spec/contract/G-5#root, spec://ai.lev/fpf-spec/contract/G-9#root, spec://ai.lev/fpf-spec/contract/E-20#root, spec://ai.lev/fpf-spec/contract/F-18#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-19#root, spec://ai.lev/fpf-spec/contract/A-19-UNM#root, spec://ai.lev/fpf-spec/contract/C-19#root, spec://ai.lev/fpf-spec/contract/C-20#root, spec://ai.lev/fpf-spec/contract/C-30#root, spec://ai.lev/fpf-spec/contract/C-30-AD#root, spec://ai.lev/fpf-spec/contract/C-30-P#root, spec://ai.lev/fpf-spec/contract/C-32#root, spec://ai.lev/fpf-spec/contract/C-32-ACE#root, spec://ai.lev/fpf-spec/contract/C-32-ACS#root, spec://ai.lev/fpf-spec/contract/C-32-CONWAY#root, spec://ai.lev/fpf-spec/contract/C-32-FAIL#root, spec://ai.lev/fpf-spec/contract/C-32-PAD#root, spec://ai.lev/fpf-spec/contract/C-38#root, spec://ai.lev/fpf-eng-psd/contract/PSD-11#root, spec://ai.lev/fpf-eng-rhy/contract/RHY-14#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/A-19-CPM
