# A.19.CPM - Compare Admitted Profiles under a Declared Comparator (CPM): depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## A.19.CPM:0 - At a glance (didactic, informative) {#at-a-glance-didactic-informative}

CPM is the CHR comparison kernel: it compares two admitted profiles under an explicit, admissibility‑gated comparator and returns a **set‑valued** comparison outcome.

**One-screen purpose (manager-first).** CPM answers: "Given two admitted profiles and an explicit comparator, what relation holds under the declared admissibility frame?" It does **not** answer: "Which one should we pick?" (selection) nor "What is the score?" (scoring).

**Use this when.** Use CPM when the current project question is comparison under one declared comparator, not scoring, folding, selection, publication, or work authorization.

**What this buys.** The practitioner gets one set-valued comparison outcome that downstream selection can consume. The actual `Compare` application keeps the profile pair, comparator, claim scope and selected context slices, optional A.19 predicate, reference plane, evaluation window, policies, and output binding recoverable. Partial order, incomparability, missing evidence, and scale limits remain explicit instead of becoming a hidden scalar winner.

**First output.** Read the by-value set bound to `ComparisonResultSlot`: only the relation or poset tokens. Read comparator, comparison scope, predicate when used, plane, window, eligibility value, and evidence use from the actual operation application and their direct neighboring relations; they are not fields hidden inside the output.

**Manager quick checklist (before you trust a comparison):**
* **Comparator is explicit:** do we have a `ComparatorSpecRef`, and is it admitted by `CG‑Spec.ComparatorSet`?
* **Admissibility is declared:** do we cite `CG‑Spec` (and `SCP` when numeric ops exist) and treat violations as `degrade|abstain`?
* **Evidence is not faked:** are missing or unknown inputs treated as `degrade|abstain` under the effective MinimalEvidence policy (never as `pass`)?
* **Partiality is preserved:** are we willing to accept incomparability and ties as first‑class outcomes (set‑valued result), rather than forcing a winner?

* **Suite stage:** `compare` (pipeline order lives in `A.19.CHR:4.5`, not in the `mechanisms[]` enumeration).
* **Input (conceptual):** left profile, right profile, `CN-Spec`, `CG-Spec`, an explicit `ComparatorSpec`, one `U.ClaimScope` with selected A.2.6 `U.ContextSlice` members, an optional A.19 `CharacteristicSpacePredicate` when the comparison depends on one, effective reference plane, explicit evaluation window, and optional explicit `MinimalEvidence` override.
* **Output (conceptual):** the by-value `ComparisonResultSlot` set of relation or poset tokens. It is not a score, selected set, result episteme, work-result relation, evidence record, or container for replay metadata.
* **Planned use:** an A.15.2 baseline selects ComparatorSpecRef editions and policy ids. A.15.3 and SlotFillingsPlanItem apply only to independently declared receiving positions under A.19.CHR:4.7.2. The actual Compare application carries its argument and result bindings under §4.1. Any dated comparison Work and A.10 evidence-provenance account retain their independent grounds.
* **Reproducible comparisons:** for parity and benchmark style runs that require a stable run package plus report record (editions, windows, parity pins), use `G.9` (Parity and Benchmark Harness). CPM stays kernel-only.
* **What CPM does not do (strict distinction):**

  * does **not** normalize (`UNM`);
  * does **not** choose indicators (`UINDM`);
  * does **not** score (`USCM`);
  * does **not** fold or aggregate (`ULSAM`);
  * does **not** select (“pick best”) — that is `SelectorMechanism`.
* **Core safety commitments:** admissibility gate via `CG-Spec.ComparatorSet` + `CG-Spec.SCP` + CSLC; tri-state admissibility (`pass|degrade|abstain`); unknown never coerces to “pass” or to a fabricated outcome; no silent scalarization or totalization.
* **Where method details live:** in editions of `ComparatorSpec` and their SoTA wiring (Part G packs and extensions), not inside CPM’s kernel semantics.
* **Quick rule of thumb:** use `USCM` when you need scores from a declared scoring method and `SelectorMechanism` when you need a selected candidate set. Obtaining measured values follows the applicable C.16 measurement method; normalization follows UNM. CPM compares admitted profiles and returns relation tokens.

## A.19.CPM:5 - Archetypal Grounding — informative {#archetypal-grounding-informative}

### A.19.CPM:5.1 - Tell {#tell}

Think of CPM as a declaration for a **replayable, relation-producing comparison operation**:

* Input: "two admitted profiles + an explicit comparator spec + declared admissibility and evidence declarations"
* Output: “a **set‑valued** relation outcome that preserves incomparability and uncertainty”

The key didactic boundary is: **CPM compares; it does not decide.**

### A.19.CPM:5.2 - Show (U.System) — comparing two supplier options without faking a total order {#show-u-system-comparing-two-supplier-options-without-faking-a}

A program manager compares Supplier‑A vs Supplier‑B for a safety‑critical component. The team tracks a profile of measures (cost, lead time, defect rate, assurance, sustainability), but not all measures are strictly comparable across regions (different reporting regimes, different units).

* The project has a declared `CN‑Spec` (admission and comparability declarations) and a declared `CG‑Spec` that lists admissible comparators in `ComparatorSet` and evidence rules in `MinimalEvidence`.
* The comparator is `ParetoDominanceComparatorSpecRef@edition`, declared in `CG-Spec.ComparatorSet`.
* The actual application binds the two supplier profiles; the claim scope `supplier options for the named component and procurement decision`; its selected regulatory and reporting `U.ContextSlice` members under A.2.6; `ComparisonPredicate = none` because Pareto dominance is supplied by the comparator; the stated procurement reference plane; and the explicit comparison interval.
* CPM runs `Compare(...)`; a changed component, scope member, comparator, plane, or interval is another comparison rather than an update to the same output.

  * If Supplier‑A is better in cost but worse in defect rate and incomparable on assurance due to missing evidence, CPM does **not** invent “A wins” or “A loses”.
  * `CompareEligibility` returns `degrade` or `abstain` under the evidence policy. On `abstain`, no comparison tokens are fabricated. When an explicit `degrade` policy permits a bounded partial comparison, `ComparisonResultSlot` contains only the justified relation tokens and preserves incomparability.
* The downstream `SelectorMechanism` can then return a selected set (e.g., keep both suppliers in the candidate set) rather than forcing a single winner by hidden tie‑break rules.

### A.19.CPM:5.3 - Show (U.Episteme) — uncertainty‑aware comparison with set‑valued outcomes {#show-u-episteme-uncertainty-aware-comparison-with-set-valued}

A research lead compares two proposed methods for a system component. Both methods have performance estimates with uncertainty bounds (e.g., distributions or prediction intervals). The team uses a SoTA uncertainty quantification package (post‑2015 conformal families are a common example) to avoid overstating confidence.

* `USCM` produces score profiles that are interval‑valued (or otherwise uncertainty‑annotated) rather than point estimates.
* The chosen comparator is uncertainty‑aware and declared as a `ComparatorSpec` (edition‑pinned) in `CG‑Spec.ComparatorSet`.
* `CompareEligibility` returns its guard value separately. If comparison proceeds, CPM returns justified relation tokens such as `not worse` or `incomparable`; if it abstains, no `abstain` token is smuggled into `ComparisonResultSlot`.
* The dated comparison `U.Work`, actual `Compare` application with its effective comparator, evidence-policy, and `ComparisonResultSlot` bindings, and A.10 evidence-provenance path let later readers reproduce why the comparison abstained or degraded instead of mistaking missing evidence for equality.

## A.19.CPM:6 - Bias-Annotation — informative {#bias-annotation-informative}

CPM is a comparison *kernel*; it does not remove bias by itself, but it prevents the most common bias‑amplifying failure modes (hidden thresholds, hidden tie‑breakers, unknown coercion).

Typical bias risks and mitigations:

* **Comparator choice encodes value judgments.** Weights, priority orders, thresholds, and “tie‑break” conventions can encode organizational bias. CPM forces these to live in explicit, edition‑pinned `ComparatorSpec` records or policy records rather than in invisible code or informal reasoning.
* **Missing evidence is rarely random.** If evidence is systematically missing for certain contexts or groups, naive “unknown → worse” is a bias amplifier. CPM’s tri‑state guard avoids coercion; but teams must still define policy‑bound failure behavior and be explicit when abstention is acceptable.
* **Cross-scheme comparisons can embed structural unfairness.** A comparison that relies on a semantic relation between two exact F.17 `SchemeSenseCell` values cites the obtaining F.9 `Bridge` and its separate bounded-use claim; together they expose the tested correspondence or difference and tolerated loss. A plane-only crossing cites the applicable ReferencePlane relation and policy. Neither branch replaces comparison scope, predicate, comparator, or time.
* **Overconfidence via scalarization.** Collapsing partial orders into scalars often overstates certainty and hides tradeoffs. CPM makes set‑valued outcomes first‑class, so the human or managerial decision can remain honest about tradeoffs.

## A.19.CPM:8 - Common Anti‑Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

* **Anti‑pattern: “Comparison returns a score.”**
  *Symptom:* `Compare(x,y)` returns a numeric margin or a single rank position.
  *Avoid:* keep numeric scoring in `USCM`; CPM returns relation tokens (set‑valued). If a numeric comparator is desired, it must be an explicit `ComparatorSpec` and still yields relation tokens as the kernel output.

* **Anti‑pattern: “CPM picks the winner.”**
  *Symptom:* comparison logic embeds winner selection or selected-set truncation.
  *Avoid:* CPM only compares; selection is `SelectorMechanism`, which consumes comparison outcomes and remains policy‑bound.

* **Anti‑pattern: “Comparator by prose or code default.”**
  *Symptom:* comparator choice is implicit (e.g., “we usually do lexicographic by safety then cost”), not edition‑pinned.
  *Avoid:* require an explicit `ComparatorSpecRef` from `CG-Spec.ComparatorSet`; dated comparison `U.Work` binds the effective edition as an occurrence parameter, and A.10 supplies its evidence-provenance path.

* **Anti‑pattern: “GateDecision leakage.”**
  *Symptom:* the `compare` step emits or assumes GateDecision, GateLog, or DecisionLog records as part of suite closure, or uses reserved gate‑lexemes (`…Guard`) for mechanism‑level predicates.
  *Avoid:* keep `CompareEligibility` as the mechanism-level tri-state predicate and assign gate decisions to their governing pattern. Keep dated comparison `U.Work`, the actual `Compare` operation application and its result binding, any result episteme, A.10 evidence-provenance, G.11 currentness, and publication relations separate from CPM declaration content.

* **Anti‑pattern: “SlotKind drift.”**
  *Symptom:* renaming or re‑purposing `LeftProfileSlot`, `RightProfileSlot`, `ComparatorSpecSlot`, or `ComparisonResultSlot` across specializations or across CHR layers.
  *Avoid:* use the suite SlotKind lexicon (`A.19.CHR:4.2.1`) and keep SlotIndex as a derived projection.

* **Anti‑pattern: “Smuggling plan‑binding into CPM.”**
  *Symptom:* hard‑coding comparator editions, policy ids, or “launch values” inside the CPM intension or pattern prose.
  *Avoid:* select intended editions and policies in the A.15.2 baseline; use A.15.3 typed filling only for independently declared positions. Establish actual Compare bindings under §4.1 and cite Work/provenance only under their own grounds.

* **Anti‑pattern: “Tie‑breakers as hidden constants.”**
  *Symptom:* forced total order via untracked thresholds, epsilons, or “if equal then compare cost” logic.
  *Avoid:* make tie-break policy part of explicit comparator and acceptance policies, pin their editions, and record their effective use in the dated comparison occurrence.

* **Anti‑pattern: “Unknown coerces to outcome.”**
  *Symptom:* missing evidence treated as equal, zero, or worse, producing decisive comparisons from absent information.
  *Avoid:* tri‑state guard; fail‑closed on missing evidence; explicit failure behavior via evidence policy.

* **Anti-pattern: `ComparisonResultSlot` as a replay record.**
  *Symptom:* comparator, scope, predicate, window, evidence, or currentness fields are placed inside the set-valued output.
  *Avoid:* keep the output to relation or poset tokens; recover effective arguments from the actual operation application and direct neighboring relations.

* **Anti-pattern: Using one F.9 Bridge rule for both semantic and ReferencePlane crossings.**
  *Symptom:* an F.9 Bridge is required merely because reference schemes or planes differ; the separate C.2.1 bounded-use claim is absent; or `CL` and a bare `R_eff` penalty are treated as mandatory.
  *Avoid:* cite an obtaining F.9 Bridge and separate bounded-use claim only for the semantic branch; cite the applicable ReferencePlane relation and policy for the plane branch; state both when both facts are current. Make only actually consumed refs recoverable with the dated `U.Work` and actual `Compare` application. Add `CL` only when needed. Open B.3 only for an actual named assurance claim, and use a local `R_eff` only if its declared domain model and calculation define it. Use A.10 for evidence provenance and ordinary bounded reliance, not to establish either crossing relation.

## A.19.CPM:10 - Rationale {#rationale}

1. **Set‑valued by design:** partial orders are common in multi‑criteria settings; pretending they are total creates false certainty and brittle decisions.
2. **ComparatorSet gating:** declaring which comparisons are admissible, and under what scale or evidence rules, prevents “algorithm by convenience”.
3. **Tri‑state guards:** explicit `pass|degrade|abstain` preserves epistemic honesty: unknown is not silently converted into an outcome.
4. **Strict distinction:** separating compare from score and select prevents hidden semantic coupling and improves evolvability (methods change via wiring; kernel stays stable).
5. **Single governing pattern:** keeping one governing pattern eliminates near-duplicate comparison descriptions that drift apart and destroy usability.

## A.19.CPM:11 - SoTA-Echoing {#sota-echoing}

**SoTA vs popular note.** This section records alignment to post‑2015 evidence‑backed practice. It is **not** a mandate to use fashionable methods; method semantics stay in SoTA packs (`G.2`) and wiring modules, while this pattern fixes the stable CPM mechanism boundary.

Concrete comparator-family SoTA packages are cited through their current Part G pack or claim sheet when one governs the use. CPM's kernel semantics remain unchanged.

| SoTA practice pointer (post‑2015)                                                                                                   | How it connects to CPM                                                                                                                                           | Adoption status in FPF                                                                                                |
| ----------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| **Fair ranking and constrained ranking** (e.g., Zehlike et al., 2017; Biega et al., 2018)                                             | Reinforces the “no hidden tie‑breaks and thresholds” stance: fairness constraints belong in explicit comparator and acceptance policies, not as silent kernel constants. | Integrate via `ComparatorSpec` editions in `CG‑Spec.ComparatorSet` + policy pins; CPM remains unchanged.              |
| **Uncertainty-aware and set-valued inference** (e.g., Romano et al., 2019; Barber et al., 2021)                                       | Supports “comparison may abstain” and “set‑valued outcomes are honest”: uncertain profiles should not be coerced into point‑comparisons.                         | Model as comparator families (or supporting method families) packaged in `G.2`; wired into declared `ComparatorSpec`. |
| **Differentiable sorting and learned comparators** (e.g., Grover et al., 2019; Blondel et al., 2020) | When comparators are learned, explicit comparator specs, edition and policy bindings in the actual operation application, its `ComparisonResultSlot` binding, and A.10 evidence-provenance become even more important for replay and drift control. | Treated as method implementations behind `ComparatorSpec` (wiring-only in Part G); CPM kernel stays stable. |
| **Robust multi‑criteria decision support under partial orders** (modern robust outranking and preference-learning variants post‑2015) | Emphasizes preserving incomparability and explicitly encoding thresholds and preferences as declared artifacts.                                                      | Packaged as comparator families; admissibility and evidence remain gated by `CG‑Spec`.                                     |

### A.19.CPM:11.1 - Currentness and smallest reopen rule {#currentness-and-smallest-reopen-rule}

**Qualification basis and window.** The stable kernel claim is qualified by the current editions of A.6.1 operation declarations and actual binding rules, A.19/A.18 space and scale semantics, A.19.CN comparability, G.0 comparator and evidence admissibility, A.2.6 scope semantics, and the exact current G.2 comparator pack or claim sheet cited by an actual use. For that use, the effective qualification window is the intersection of those bound editions' currentness and any validity interval declared by the comparator pack or claim sheet; `post-2015` is an orientation label, not an indefinite freshness claim.

**Reopen the CPM kernel only when.** Reopen the smallest affected CPM rule when a direct governor changes binary `Compare` application identity or bindings, `ComparisonResultSlot` kind, comparator admission, scale or normalization admissibility, tri-state eligibility, comparison scope, or the separation of output, evidence, provenance, and result epistemes, or when qualified evidence contradicts one of those kernel commitments. A new algorithm family, learned model, fairness constraint, uncertainty method, threshold, or robustness technique that still satisfies those commitments changes its G.2 pack, `ComparatorSpec`, `CG-Spec`, or policy binding rather than CPM.

**Smallest affected locus.** A signature or result-kind change reopens only the corresponding direct-signature, operation-local argument/result declaration, or `OperationAlgebra` passage in `A.19.CPM:4.1`; an admissibility or failure-semantics change reopens the matching `LawSet` or `AdmissibilityConditions` clause. Update only the nearest exercising case in `A.19.CPM:5.2` or `:5.3` and the corresponding `CC-A19CPM` row. Source-family churn that changes no kernel commitment updates the direct pack or claim sheet and, when its summary is stale, only the affected row in this SoTA map.


## A.19.CPM:End {#end}
