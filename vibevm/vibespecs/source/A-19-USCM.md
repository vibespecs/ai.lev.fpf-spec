# A.19.USCM - Unified Scoring Mechanism, USCM: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## A.19.USCM:0 - At a glance — didactic, informative {#at-a-glance-didactic-informative}

* **Suite stage:** `score` (ordering lives only in `A.19.CHR:4.5` / `suite_protocols`; suite membership is a set in `A.19.CHR:4.2`).
* **Inputs, conceptual:** an admitted measure profile for the exact evaluated bearer, plus `CNSpecRef`, `CGSpecRef`, and `ScoringMethodDescriptionRef`; their editions name the criteria, claim scope and selected slices, qualification window, comparison or reference basis, evidence policy, and intended result use. `MinimalEvidenceRef` may override the CG-Spec minimum.
* **Output:** `ScoreProfileSlot` = a set of score measures (vector scores are first‑class; a scalar score is allowed only if explicitly declared).
* **Non‑goals:** does **not** normalize (UNM), aggregate (ULSAM), compare (CPM), select (SelectorMechanism), threshold, publish, or emit telemetry; it is a scoring step with explicit admissibility and evidence surfaces.
* **P2W seam:** an A.15.2 baseline selects editions and policies, including ScoringMethodDescriptionRef when USCM is used. A.15.3 typed filling applies only to independently declared receiving positions under A.19.CHR:4.7.2. Actual Score bindings obtain under §4.1; Audit records the effective refs and pins.
* **Failure mode:** tri‑state guard (`pass|degrade|abstain`); unknown never coerces to `pass`, and MUST NOT be coerced to `0/false`.
* **Quick rule of thumb:** if `CGSpecSlot.SCP` is missing → `ScoreEligibility = abstain` (fail‑closed); if `ScoringMethodDescriptionSlot` is missing → `ScoreEligibility = abstain` (no implicit scoring method); if `CN‑Spec.comparability` requires normalization‑based comparability → normalization MUST be explicit in choreography (Uses/pins), never hidden inside `Score`.

## A.19.USCM:5 - Archetypal Grounding — informative {#archetypal-grounding-informative}

### A.19.USCM:5.1 - Tell {#tell}

Think of USCM as **admissibility‑gated scoring**:

* Input: “an admitted profile of measures for this exact bearer, criteria, scope and window, comparison basis, evidence policy, and result use, plus the CN-Spec and CG-Spec editions that declare those bounds”
* Output: “a set of score measures that downstream steps may compare/select on”

The key didactic boundary is: **USCM is allowed to transform measures only within the admissibility surface (SCP+CSLC), and it must not hide normalization, aggregation, or ordering.**

### A.19.USCM:5.2 - Show — U.System {#show-u-system}

A program manager evaluates competing rollout plans for a product launch.

* The admitted profile includes measures like `{Cost, LeadTime, Reliability, RiskExposure, CarbonPerUnit}`.
* The CG‑Spec’s `SCP` admits only scale‑lawful transforms (e.g., monotone transforms on ratio/interval measures, explicit unit alignment rules, and prohibited operations on ordinal measures).
* USCM runs `Score(...)` and outputs a score profile such as `{UtilityScore, RiskScore}` rather than forcing a single number.
* A plan lacks sufficient evidence for `RiskExposure` for the named planning bearer, selected claim slices, and qualification window; `ScoreEligibility` returns `degrade`, and the audit records the effective MinimalEvidence policy and the exact CN-Spec and CG-Spec editions.

Downstream steps can now compare and select with an explicit audit trail, instead of pretending that “the score was objective.”

### A.19.USCM:5.3 - Show — U.Episteme {#show-u-episteme}

A research lead compares several model families for deployment across heterogeneous environments.

* Indicators include calibration and robustness metrics; scoring is done using a calibrated probabilistic score plus uncertainty‑aware score dimensions.
* A post‑2015 practice example is to keep monotonicity and interpretability constraints explicit (e.g., monotone additive models or monotone deep lattice style models) and to treat uncertainty as first‑class (e.g., conformal set‑valued scoring that yields intervals rather than point scores).
* USCM produces a score profile that can remain vector‑valued and uncertainty‑aware, and it refuses to coerce “unknown” into a point score. Comparisons and selections occur downstream using set‑valued semantics where appropriate.

## A.19.USCM:6 - Bias-Annotation — informative {#bias-annotation-informative}

* **Gov (governance).** Bias toward explicit admissibility and evidence surfaces (`CGSpecRef`, `SCP`, `MinimalEvidence`) rather than "standard practice" arithmetic. Risk: perceived overhead. Mitigation: keep the kernel signature small and push method specifics into SoTA packs and wiring modules.

* **Arch (architecture).** Bias toward stable interfaces and strict step boundaries (no implicit UNM; no hidden scalarization). Risk: reduced room for ad‑hoc shortcuts. Mitigation: allow richer scoring method families via wiring, without mutating the USCM intension.

* **Onto/Epist.** Bias toward treating scores as measures with declared semantics, not as “the truth.” Risk: teams accustomed to one‑number rankings may resist. Mitigation: treat scalarization as an explicit, auditable commitment, not as the default.

* **Prag (pragmatics).** Bias toward fail‑closed guards and traceability under uncertainty. Risk: more `degrade/abstain` outcomes early. Mitigation: couple `degrade` with explicit downstream behavior policies, rather than silent coercion.

* **Did (didactics).** Bias toward “one place to learn the mechanism”: the problem/forces/solution narrative is co‑located with the canonical Mechanism.Intension.

## A.19.USCM:8 - Common Anti‑Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

* **Hidden normalization inside scoring.** Scoring silently normalizes or aligns measures. Avoid by making UNM explicit in choreography and keeping USCM's `Score` admissibility‑only.

* **Weighted sum across mixed or non-admissible scales.** Treating “weights + sum” as universal. Avoid by requiring SCP+CSLC admissibility; if the scale operation is not scale-admissible, it is not admissible.

* **Silent scalarization.** Collapsing vector scores or partial orders into a single “overall score” via an untracked tie‑breaker. Avoid by leaving vector scores intact, and making scalarization an explicit declared commitment.

* **Implicit scoring method (“we just use the standard formula”).** The scoring method is assumed rather than declared and pinned. Avoid by requiring `ScoringMethodDescriptionSlot` and edition pinning in planned baseline; treat “identity scoring” (if ever needed) as an explicit method description, not a hidden default.

* **Unknown → 0 coercion.** Treating missing evidence as zero, false, or “good enough.” Avoid by tri‑state guards and explicit failure behavior, with auditable effective evidence policy.

* **Shadow CG‑Spec.** Hard‑coding admissibility rules inside a scoring method description instead of citing `CGSpecSlot.SCP`. Avoid by keeping admissibility in CG‑Spec and treating method details as wiring.

* **Telemetry or publish leakage.** Treating scoring as a reporting step. Avoid by keeping publish/telemetry outside suite closure and using the appropriate post-suite mechanisms.

* **SlotKind drift.** Renaming or re‑purposing slots across specializations or across mechanisms. Avoid by using the suite SlotKind lexicon and the `⊑/⊑⁺` discipline.

## A.19.USCM:10 - Rationale {#rationale}

Scoring is a frequent source of semantic precision loss: it is easy to smuggle normalization, illegal arithmetic, implicit thresholds, and uncertainty coercion into “a simple scoring function.” USCM prevents that by forcing a clean boundary:

* **Admissibility first:** all transforms are justified by `CG‑Spec.SCP` and CSLC.
* **No hidden steps:** normalization is explicit (UNM), aggregation is explicit (ULSAM), ordering is explicit (CPM/SelectorMechanism).
* **Uncertainty is visible:** admissibility is tri‑state; unknown is not coerced.
* **Audit is minimal yet decisive:** effective editions and effective evidence policy are always traceable.

This increases both evolvability (stable interface, externalized method semantics) and didactic usability (a single place to learn USCM’s boundary and obligations).

## A.19.USCM:11 - SoTA-Echoing {#sota-echoing}

**SoTA vs popular note.** This section records alignment to post‑2015 evidence‑backed practice. It is **not** a mandate to use fashionable methods; method semantics stay in SoTA packs (`G.2`) and wiring modules, while this pattern fixes the stable mechanism boundary.



### A.19.USCM:11.1 - SoTA alignment map {#sota-alignment-map}

| SoTA practice pointer, post‑2015+                                             | Primary source examples, post‑2015+                                                                                                               | Where it connects to USCM                                                                                                                                        | Adoption status |
| ----------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------- |
| Prefer monotone and interpretable scoring surfaces where appropriate          | Explainable additive and monotone model lines, e.g., Lou et al. 2016; Nori et al. 2019; monotone deep lattice style models, e.g., You et al. 2017 | Expressed as **admissibility‑bounded transform freedom** via `CGSpecSlot.SCP` and explicit scalarization rules; method details stay out of the kernel                 | Adapt           |
| Treat probabilistic scores as measures requiring calibration, not raw outputs | Calibration practice, e.g., temperature scaling (Guo et al. 2017) and successors                                                                  | Expressed as “score is a measure on an explicit scale,” bounded by SCP+CSLC and evidence gating; calibration itself is wired as method semantics, not kernel law | Adapt           |
| Keep uncertainty explicit and allow set‑valued scoring when appropriate       | Modern conformal prediction practice, e.g., Romano et al. 2019; Barber et al. 2021                                                                | Expressed as “vector scores allowed; unknown not coerced; no hidden scalarization,” enabling downstream set‑valued comparison/selection                          | Adapt           |
| Keep architectural commitments traceable to one governing pattern                     | ISO/IEC/IEEE 42010:2022 architecture description discipline                                                                                       | Expressed as explicit governing-pattern assignment and Tell+Cite stubs elsewhere (no competing semantics)                                                                  | Adopt           |

**Notes per row**

1. USCM does not "implement a particular scoring model"; it preserves a stable, admissibility‑gated surface on which such models can be wired.
2. Calibration is treated as a lawful transform family that must live within SCP+CSLC; the kernel does not mandate a specific calibration method.
3. Set‑valued scoring aligns with USCM’s “vector first, scalar by declaration” law, and is naturally consumed by CPM/SelectorMechanism without forcing a spurious total order.
4. Governing-pattern traceability is used here to keep the spec teachable and non-duplicative; it does not add new governance cards or admissibility gates.


## A.19.USCM:End {#end}
