# A.19.ULSAM - Unified Lawful Scale Aggregation Mechanism (ULSAM): depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## A.19.ULSAM:0 - At a glance (didactic, informative) {#at-a-glance-didactic-informative}

* **Suite stage:** `fold_Γ?` (ordering lives only in `A.19.CHR:suite_protocols`; `mechanisms[]` membership is a set, not an order).
* **Input surface:** an admitted `MeasureSetSlot`, `CNSpecSlot`, `CGSpecSlot`, and `GammaFoldSlot`, with the grouping or membership basis, fold and policy editions, claim scope and selected slices, qualification window, evidence basis, contributors, and intended result declared by those inputs; `MinimalEvidenceSlot?` may override the CG-Spec minimum.
* **Output surface:** `AggregatedMeasureSlot` (+ optional `ContributorSetSlot?` as an explanation surface).
* **Non‑goals:** no scoring, no comparison, no selection, no “method catalog”, no hidden defaults, no hidden thresholds.
* **P2W seam:** an A.15.2 baseline selects the fold, evidence policy and their editions. A.15.3 typed filling applies only to independently declared receiving positions under the CHR P2W hook. Actual fold arguments bind under §4.1; a planned value does not establish that binding.
* **Failure mode:** tri‑state guard `GuardDecision := {pass|degrade|abstain}`; unknown/insufficient evidence never coerces to “pass”.
* **Rule of thumb:** if you are about to “average/sum/roll up”, you probably need an explicit ULSAM `Fold_Γ` stage (or a justified decision to *not* fold).

**What this mechanism is.** `ULSAM` is the CHR mechanism that makes **aggregation explicit**: it performs an explicit **Γ‑fold** over a set of **admitted measures**, producing an **aggregated measure** (and optionally a contributor surface) under **declared admissibility**.

**What this mechanism is not.**
- It is **not** a scoring method (that is `USCM`).
- It is **not** a comparison mechanism (that is `CPM`).
- It is **not** a selection mechanism (that is `SelectorMechanism`).
- It is **not** a “method catalog”: method specifics belong to SoTA packs and wiring (`G.*:Ext.*`), not here.
- It is **not** a place to hide defaults (“implementation default fold”) or hidden thresholds.

**When you need ULSAM.**
- You want to “roll up” multiple measures into one measure (e.g., an overall reliability/assurance coordinate, a single aggregated risk measure, an aggregate score coordinate).
- You need the fold to be **auditable** (what contributed; what was excluded by evidence/admissibility).
- You need the fold to be **scale-lawful** (no ordinal arithmetic; no illegal mixing of units).
- You need the fold to be **policy-bound and edition-stable** (replayability and pin traceability).

**Choosing the fold.** If the law for the intended result or a required property is unresolved, use A.9 or reuse a sufficient domain result. When the result selects a fold, its law and conditions supply the basis for the explicit fold reference; ULSAM still governs admission of the measures, scale lawfulness and the actual mechanism operation.

**Where it sits in CHR.**
- In the CHR suite protocol, ULSAM corresponds to the optional stage `fold_Γ?` (i.e., **explicitly optional** and never hidden inside `score/compare/select`).

**60‑second script for engineer-managers.**
> "If you're about to average, sum, or otherwise compress multiple measures into one, stop. Ask: (i) do we have a declared Γ‑fold policy and SCP admissibility, (ii) are the measures admissible and scale-compatible, (iii) what do we do if evidence is missing? If you cannot answer with explicit pins/refs, you are not folding -- you are smuggling an assumption. Use ULSAM's `Fold_Γ`, record the effective Γ‑fold and contributor set, and keep the fold as an explicit step."

## A.19.ULSAM:5 - Archetypal grounding (didactic, informative) {#archetypal-grounding-didactic-informative}

### A.19.ULSAM:5.1 - Tell {#tell}

- In CHR, ULSAM exists to keep the stage `fold_Γ?` **explicit**: if a pipeline wants folding, it invokes `ULSAM.Fold_Γ`; otherwise it skips the stage. Folding MUST NOT be smuggled into `USCM.Score`, `CPM.Compare`, or `SelectorMechanism.Select`.
- For a `U.System` decision: ULSAM explicitly folds the admitted measures about the named System, under the declared grouping or membership basis and CG-Spec fold policy, only when that aggregate result is actually needed.
- For a `U.Episteme` assessment: ULSAM explicitly folds the admitted evidential or measurement set about that episteme into an aggregate coordinate, using an aggregation model justified for that exact quantity and support dependence; reliability-like wording alone supplies no weakest-link law.

### A.19.ULSAM:5.2 - Show {#show}

**Scenario A (manager-facing): “roll up” a multi-metric readiness into one reliability-like coordinate.**
1. A CHR pipeline produces a set of admitted measures (post-`USCM` or directly from characteristic measures):
   `MeasureSetSlot = {m₁, m₂, …, m_k}`.
2. The team wants a single “readiness” measure `m_ready` to be used as an input to later comparison/selection.
   The temptation is to “just average” or “just do weighted sum”.
3. ULSAM forces three explicit questions before folding:
   - **Admissibility:** Is the fold admissible under `CGSpecSlot.SCP` (units/scale) and `CGSpecSlot.Γ_fold` (declared fold kinds)?
   - **Evidence:** Is the evidence posture sufficient under `MinimalEvidence`? If not, do we `degrade` or `abstain`?
   - **Policy identity:** What is the identity of the fold (which ΓFoldRef, which edition)?
4. Only then, the pipeline performs:
   `Fold_Γ(MeasureSetSlot, CNSpecSlot, CGSpecSlot, GammaFoldSlot, MinimalEvidenceSlot?) → (AggregatedMeasureSlot, ContributorSetSlot?)`.
   The audit records `ΓFoldRef` and (optionally) the contributor surface.

**Scenario B (engineer-facing): proposed aggregation across different bases.**
- A project tries to fold measures with different bearers, membership rules, scales, comparison bases, or reference planes. ULSAM first checks whether one admitted set and lawful fold can be stated. If the conclusion relies on an F.9 Bridge, kind relation, aggregation or membership relation, or plane relation, the project cites that exact obtaining relation and its loss; otherwise it constitutes separate folds or fails closed.

## A.19.ULSAM:6 - Bias-Annotation (informative) {#bias-annotation-informative}

This pattern intentionally biases CHR authoring toward **explicit aggregation boundaries** and against “scalarization by convenience”.

* **Gov (governance).** Bias toward auditable folds (editions, effective ΓFoldRef, contributor surfaces). Risk: perceived overhead. Mitigation: keep the signature stable and move method specifics to SoTA wiring.
* **Arch (architecture).** Bias toward keeping `fold_Γ` a distinct stage (no leakage into score/compare/select). Risk: longer pipelines. Mitigation: the stage is explicitly optional (`fold_Γ?`) and can be omitted when not required.
* **Onto/Epist (ontology/epistemology).** Bias toward scale-lawful aggregation (no illegal ordinal arithmetic; SCP-bound). Risk: forbids many informal “single-number” habits. Mitigation: use partial orders and set-return selection unless a lawful fold is truly needed.
* **Prag (practice).** Bias toward policy-bound defaults (no “implementation default Γ‑fold”). Risk: teams must name policies. Mitigation: provide conservative defaults in `CG‑Spec.Γ_fold` and keep overrides explicit.
* **Did (didactic).** Bias toward one-governing pattern readability (this pattern is the governing pattern; no scavenger hunt). Risk: duplication temptation elsewhere. Mitigation: enforce Tell+Cite canonicalization.

## A.19.ULSAM:8 - Common anti-patterns (didactic, informative) {#common-anti-patterns-didactic-informative}

| Anti-pattern | Symptom | Why it fails in FPF | How to avoid |
|---|---|---|---|
| Hidden rollup inside scoring | “Our score already averages everything.” | Violates the “no hidden aggregation” law and hides Γ‑fold identity. | Keep `USCM.Score` scoring-only; use `ULSAM.Fold_Γ` as an explicit stage. |
| Averaging ordinals | Means on ranks/levels, or unitless mixing | Illegal under CSLC/SCP unless explicitly allowed. | Keep ordinal outputs as ordinal; compare via CPM; if folding is required, use an ordinal-legal fold explicitly declared by Γ_fold policy. |
| Implementation default Γ‑fold | "If not specified, we use X." | Breaks replayability and violates Γ‑fold admissibility. | Require `GammaFoldSlot` to resolve to `CGSpecSlot.Γ_fold` or pinned override. |
| Coercing unknown to a number | “Missing metric becomes 0.” | Violates tri-state guard discipline; silently changes meaning. | Use `FoldEligibility_Γ` with `{pass|degrade|abstain}` and record the effective evidence policy. |
| Folding after the admitted set or basis changed | Measures with different bearers, membership rules, scales, scopes or windows, comparison bases, or planes are folded “as-is” | The result no longer follows from one declared set and lawful fold; relation labels cannot repair that gap. | Re-establish the admitted set and eligibility. Cite an obtaining relation and supported loss only when the fold or receiving use actually relies on it; otherwise keep separate folds or abstain. |
| Treating fold_Γ as mandatory | Always folding even when not needed | Unnecessary aggregation can hide distinctions needed by the receiving use. | Keep `fold_Γ?` explicitly optional in protocols; prefer vector+CPM+Selector when possible. |

## A.19.ULSAM:10 - Rationale (didactic, informative) {#rationale-didactic-informative}

Aggregation is a **semantic commitment**: it changes a set/vector of measures into a single measure, and therefore changes what later comparison/selection can legitimately claim. In CHR, that commitment must be explicit, admissibility-gated, and auditable.

Keeping ULSAM as its own mechanism preserves:
- the strict boundary between **method choice** (SoTA packs) and **operation declaration**,
- the strict boundary between **planned baseline** (pins chosen in WorkPlanning) and **run-time audit** (what actually executed),
- and the engineer-facing clarity that “we folded here, not everywhere”.

## A.19.ULSAM:11 - Known uses (didactic, informative) {#known-uses-didactic-informative}

- CHR suite optional stage `fold_Γ?` (explicitly optional; never hidden).
- Folding a trust/assurance quantity only under its justified model and applicable policy; a declared default alone supplies no numerical warrant.
- Any project that requires an auditable “roll-up” measure prior to lawful comparison/selection.
- In E.18 transformation-flow structures: ULSAM appears as a mechanism instance node whose `ΓFoldRef` / `MinimalEvidenceRef` are bound in planned baseline (P2W), while Audit records the effective pins used at run time.

## A.19.ULSAM:12 - Builds on / Relates to {#builds-on-relates-to}

**Builds on (cite, don’t duplicate).**
- `A.6.1` (operation declarations and actual application/binding rules).
- `A.6.1 §4.2` (operation-local argument/result declarations as the source of SlotIndex).
- `A.19.CHR` (CHR suite boundary; stage `fold_Γ?`; CHR SlotKind Lexicon).
- `G.0` (`CG-Spec.Γ_fold`, `CG-Spec.SCP`, `CG-Spec.MinimalEvidence`; admissibility gate).
- `A.18` (CSLC).
- `B.3` (support dependence and the justified model for any `R_eff` calculation).

**Relates to (coordination, not governing-pattern assignment).**
- `A.19.CN` (`CN‑Spec`), via `CNSpecSlot.acceptance` gating in admissibility.
- `A.19.UINDM`, `A.19.USCM`, `A.19.CPM`, and `A.19.SelectorMechanism` as adjacent CHR stages (Uses contour; no governing-pattern assignment transfer).
- Part G SoTA packs and wiring (`G.2` + `G.*:Ext.*`) for method family selection and edition/policy binding.

## A.19.ULSAM:13 - SoTA-Echoing (informative; not a center of gravity) {#sota-echoing-informative-not-a-center-of-gravity}

SoTA here is treated as **method-family source publications and `G.2` claim sheets to be wired** through `G.*:Ext.*` wiring, not as kernel semantics. ULSAM’s contribution is the stable boundary: explicit, admissible, auditable folding.

**SoTA vs popular note.** This section records alignment to post‑2015 evidence‑backed practice. It is **not** a mandate to use fashionable methods; method semantics stay in SoTA packs (`G.2`) and wiring modules, while this pattern fixes the stable mechanism boundary.



| SoTA practice pointer (post‑2015+) | Primary source | Where it connects | Adoption status |
|---|---|---|---|
| Permutation‑invariant set aggregation as a *method family* (set → summary) | Zaheer et al., “Deep Sets” (2017) [1] | Candidate `ΓFold` families can include permutation‑invariant folds; ULSAM keeps them admissibility-gated and policy-pinned. | **Adapt** (keep admissibility/pins explicit; do not treat learned folds as implicit defaults). |
| Attention-based permutation‑invariant set aggregation as a *method family* | Lee et al., “Set Transformer” (2019) [4] | Alternative learnable set folds (pooling by attention); still requires explicit policy binding and admissibility gating. | **Adapt** (publish as method family in SoTA pack; pin editions/policies; keep kernel unchanged). |
| Robust aggregation under uncertainty/outliers as a *policy-selectable fold family* | Rahimian & Mehrotra, “Distributionally Robust Optimization: A Review” (2019) [2] | Treat “worst‑case / risk‑aware” folds as explicit Γ‑fold options (policy-bound), not as hidden safety margins. | **Adapt** (policy‑bound and SCP/CSLC‑gated). |
| Governing-pattern discipline for architectural statements | ISO/IEC/IEEE 42010:2022 [3] | Supports the “one governing pattern” rule: ULSAM intension content lives here; other places cite. | **Adopt** (principle-level; applied to FPF pattern governing-pattern assignment). |

**Reminder.** “SoTA” means best known methods; it is not a synonym for “popular right now”. SoTA material should be curated and versioned in SoTA packs and connected via wiring modules, not embedded into kernel mechanism signatures.

[1]: https://arxiv.org/abs/1703.06114 "Zaheer et al., Deep Sets, 2017"
[2]: https://arxiv.org/abs/1908.05659 "Rahimian & Mehrotra, Distributionally Robust Optimization: A Review, 2019"
[3]: https://www.iso.org/standard/74393.html "ISO/IEC/IEEE 42010:2022 — Systems and software engineering — Architecture description"
[4]: https://arxiv.org/abs/1810.00825 "Lee et al., Set Transformer, 2019"


## A.19.ULSAM:End {#end}
