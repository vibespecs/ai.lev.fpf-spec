# A.19.UINDM - Indicatorization (UINDM): Select Indicators Under a Declared Policy: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## A.19.UINDM:0 - At a glance (didactic, informative) {#at-a-glance-didactic-informative}

* **Suite stage:** `indicatorize` (ordering lives only in `A.19.CHR:suite_protocols`).
* **Inputs (conceptual):** exact `U.CharacteristicSpaceRef`, `CNSpecRef`, and `IndicatorChoicePolicyRef`, with the bearer, claim scope and selected slices, qualification window, evidence basis, and intended use declared by those editions; when the selected policy is evidence-gated, also supply `CGSpecRef` and, optionally, a `MinimalEvidenceRef` override.
* **Output:** `IndicatorSetSlot` = `S⊆I`, a set of positions in the exact A.19 space declaration's ordered basis I. Each position retains its Characteristic, Scale and meaning. The selection is not a measurement or conversion.
* **Non‑goals:** does **not** normalize, score, compare, aggregate, threshold, publish, or emit telemetry; it only selects a subset under explicit policy.
* **P2W seam:** the A.15.2 baseline records concrete space/spec/policy editions; A.15.3 typed filling applies only to independently declared positions. Actual use retains its effective refs and pins in Audit.
* **Failure mode:** tri‑state guard (`pass|degrade|abstain`); unknown never coerces to `pass`.
* **Quick rule of thumb:** if `CN‑Spec.indicator_policy` is absent → `IndicatorizeEligibility = abstain` (fail‑closed); if the selected policy is evidence‑gated → `CGSpecRef` MUST be available and the effective MinimalEvidence MUST be explicit (override or `CG‑Spec.MinimalEvidence`).

## A.19.UINDM:5 - Archetypal Grounding (informative) {#archetypal-grounding-informative}

### A.19.UINDM:5.1 - Tell {#tell}

Think of UINDM as a **policy‑bound projection**:

* Input: “the declared characteristic basis for this exact bearer, claim scope and selected slices, qualification window, evidence basis, and intended use, plus an explicit indicator choice policy”
* Output: “the selected positions of this exact basis, each retaining its Characteristic, Scale and meaning for downstream use”

The key didactic boundary is: **UINDM chooses coordinates; it does not alter coordinates.**

### A.19.UINDM:5.2 - Show (U.System) — cross‑unit engineering dashboard {#show-u-system-cross-unit-engineering-dashboard}

A program manager maintains a `U.CharacteristicSpace` for manufacturing sites, including ~30 characteristics (quality, safety, cost, throughput, sustainability).

* The CN‑Spec’s `indicator_policy` for the “weekly executive dashboard” selects a subset:
  `{DefectRate, IncidentRate, UnitCost, LeadTime, EnergyPerUnit, OnTimeDelivery}`.
* In this example each named Characteristic has one basis position. UINDM resolves the six names to those exact positions and returns S; each position retains its original Scale.
* One site lacks reliable incident reporting for the last week. The indicator policy is evidence‑gated; `IndicatorizeEligibility` returns `degrade` (not `pass`), and the audit records the effective MinimalEvidence and the edition pins used.

Downstream mechanisms can now be held to the invariant: **they may only score/compare/select using the declared indicator profile (or explicitly abstain/degrade).** This avoids “dashboard drift” where different teams silently score on different subsets.

### A.19.UINDM:5.3 - Show (U.Episteme) — robust evaluation across environments {#show-u-episteme-robust-evaluation-across-environments}

A research lead wants indicators for model robustness under distribution shift (different hospitals, sensors, geographies).

* The declared characteristic-space basis includes many candidate metrics (accuracy slices, calibration, subgroup error, OOD detection quality).
* The indicator choice policy is “invariance‑driven”: prefer indicators whose semantics remain stable under environment changes; deprioritize proxy metrics known to be environment‑sensitive.
* UINDM returns an indicator set used by the scoring and comparison stages; uncertain indicators are handled via tri‑state guarding rather than coerced to zero or silently dropped.

### A.19.UINDM:5.4 - One Characteristic at two Scale positions {#one-characteristic-at-two-scale-positions}

Let the exact space declaration `CS7` have ordered positions `i1=(Temperature, Celsius)` and `i2=(Temperature, kelvin)`, followed by an unrelated cost position. A state contains `x_i1=20 °C` and `x_i2=293.15 K`. The policy “select Celsius temperature” returns `S={i1}`. The explicit all-matches policy “all Temperature positions” returns `{i1,i2}`, with `x|_S` in the original order and both Scale meanings retained. UINDM converts neither value.

For the first policy, a separately admitted USCM scoring use can read the Celsius value under its declared method `g_C(c)=(c-0)/(40-0)` on Celsius interval `[0,40]`, returning `0.5` at 20. The interval endpoints are part of this illustrative scoring declaration. Supplying 293.15 as though it were Celsius violates that method's input basis; a TemperatureRef alone would not reveal the error. All-matches selection requires a receiving method that accepts those two Scale-specific positions, or a narrower selection; it is not a universal default.

Suppose a new declaration `CS8` reverses these two positions. Resolving “Celsius temperature” now selects its CS8-local position i2. Reusing CS7's naked integer 1 would select kelvin and is invalid. If the policy merely says “Temperature” and supplies no rule for the two matches, return its unresolved/abstain disposition. A missing indicator policy retains the defined abstain result, and evidence gating still applies only when the selected policy requires it.

## A.19.UINDM:6 - Bias-Annotation (informative) {#bias-annotation-informative}

* **Gov (governance).** Bias toward explicit policy surfaces (`IndicatorChoicePolicyRef`, edition pins, auditable outcomes) rather than tacit “expert choice.” Risk: perceived extra work. Mitigation: keep the mechanism minimal (selection‑only) and push method detail into wiring modules.

* **Arch (architecture).** Bias toward stable interfaces: SlotKind tokens come from the suite lexicon and evidence gates are explicit inputs. Risk: reduced “quick hacks.” Mitigation: allow `⊑⁺` extensions for richer outputs (e.g., justification) without mutating the kernel signature.

* **Onto/Epist.** Bias toward a strict distinction between “measurable characteristic” and “indicator under policy.” Risk: teams accustomed to “everything measurable is an indicator” may resist. Mitigation: embed this as an explicit LawSet clause (“No implicit NCV⇒indicator”).

* **Prag (pragmatics).** Bias toward fail‑closed guards and traceability under uncertainty. Risk: more `abstain/degrade` outcomes early. Mitigation: couple `degrade` with explicit downstream behaviors (policy‑bound) rather than silent coercions.

* **Did (didactics).** Bias toward “one place to learn the mechanism”: the problem/forces/solution narrative is co‑located with the operation declaration.

## A.19.UINDM:8 - Common Anti‑Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

* **“NCV ⇒ indicator.”** Treating all measurable characteristics as indicators. Violates “No implicit NCV⇒indicator.”

* **Indicatorization hidden in scoring.** A scoring method silently ignores some characteristics or introduces an implicit “feature selection” without an explicit indicator set.

* **Characteristic reference substituted for a position.** Temperature occurs at Celsius and kelvin positions, but the returned set contains only TemperatureRef. Resolve the policy to the requested position or its explicitly selected all-matches set before returning S.

* **Silent emptying.** When evidence is insufficient, returning an empty indicator set (or treating missing evidence as “pass”) without a tri‑state guard decision.

* **Reusing an indicator set after its basis or use changed.** Reusing it for another bearer, scope and window, evidence basis, reference plane, or intended use without a new eligibility decision; or naming Bridge or plane-relation pins without an actual obtaining relation.

* **Smuggling plan‑binding into the mechanism.** Binding concrete edition pins / planned slot fillings (“launch values”) inside the UINDM description instead of using the P2W seam (WorkPlanning) and recording only effective refs/pins in `Audit`.

* **GateDecision leakage.** Emitting or implying GateDecision/GateLog as part of the `indicatorize` step (gate decisions are separated from suite steps; keep UINDM at guard+audit level).

## A.19.UINDM:10 - Rationale {#rationale}

Indicatorization is separated because it is a different kind of commitment than scoring or comparison:

* Indicatorization commits to **which coordinates are allowed to matter** under policy.
* Scoring/aggregation/comparison commit to **how** allowed coordinates are transformed, folded, or ordered under admissibility gates.

By making indicatorization selection‑only, UINDM avoids “semantic alchemy” (changing meanings while claiming to merely “pick indicators”) and supports the CHR suite’s broader discipline: explicit spec refs, explicit crossings, and explicit handling of uncertainty via tri‑state guards.

## A.19.UINDM:11 - SoTA-Echoing — choose indicators for their intended use {#sota-echoing-choose-indicators-for-their-intended-use}

**Practice question.** Which coordinates should a dashboard or receiving method use when several available columns are plausible indicators? The selected line makes the phenomenon and intended use govern an explicit choice policy, then checks the selected positions and their Scale meanings. A serious alternative ranks available features by a statistical score and keeps the best k. That alternative is useful for its declared predictive or exploratory objective; its ranking alone does not decide which quantities a particular dashboard must report.

The European Commission JRC's [10 Step Guide, steps 1–2](https://knowledge4policy.ec.europa.eu/composite-indicators/toolkit_en/navigation-page/10-step-guide_en), published as a navigation guide in March 2025, supplies the purpose-led line for composite indicators: define the conceptual basis and choose relevant, analytically sound, obtainable indicators. **Adapt** that ordering to `CN-Spec.indicator_policy`, the IndicatorChoicePolicy argument in §4.1 and the selection-only law. UINDM selects existing coordinates; the guide's later normalization, weighting and aggregation steps belong to their separately declared mechanisms. The guide does not prove that any particular policy is adequate or stable under distribution shift.

The [scikit-learn SelectKBest documentation](https://scikit-learn.org/stable/modules/generated/sklearn.feature_selection.SelectKBest.html) supplies the concrete statistical alternative: choose k features using a declared scoring function; equal scores can be resolved in an unspecified way. **Adopt** statistical selection when the intended use actually chooses that criterion, with the data, scoring rule and treatment of ties declared in the policy. **Reject** substituting a top-k result for an undeclared semantic choice. The documentation establishes the selector's behavior, not the meaning or fitness of the selected indicators.

The two Temperature positions in §5.4 expose the distinction. Suppose the Celsius and kelvin columns receive equal statistical scores and k=1. Either could be retained under an unspecified tie rule, while the downstream Celsius scoring method accepts only the Celsius position. At comparable effort, the explicit Celsius policy resolves the required input directly; when prediction is the real objective, the statistical policy can instead choose a position and bind its actual Scale to an appropriate receiving method. This changes checklist items 3–4 in §7: retain the exact selected position, and resolve an action-changing tie by the policy or return its unresolved result. A promise that both columns concern Temperature is insufficient.

The trade-off is deliberate: a purpose-led policy makes the required indicator meaning inspectable, but it does not by itself optimize prediction. A statistical policy needs data and a justified score, and its selected subset can vary with them. Neither approach permits UINDM to silently rescale values. Reopen the comparison when the receiving question changes, evidence shows that the selected indicators fail that question, or a rival policy preserves the needed meaning with better usefulness at comparable effort.


## A.19.UINDM:End {#end}
