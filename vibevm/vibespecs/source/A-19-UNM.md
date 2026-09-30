# A.19.UNM - Normalize Coordinate Values under Declared Invariants (UNM): depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## A.19.UNM:0 - At a glance — didactic, informative {#at-a-glance-didactic-informative}

**Intent.** Provide a single, explicit normalization mechanism for **coordinate values** in a `U.CharacteristicSpace`, so that **comparability** and downstream characterization steps can be stated as “**normalize-then-compare**” (governance), rather than as hidden arithmetic inside scoring/selection.

**Where it sits.**
- **CN-frame governance card:** `CN_Spec.normalization` + `CN_Spec.comparability.mode` route whether comparison is `coordinatewise` or `normalization-based`.
- **CHR suite role:** stage `normalize` (first-stage, when enabled by the suite protocol / comparability routing).

**Key outputs.**
- `NCV` (NormalizedCharacteristicValue) values for coordinates.
- When requested for a function `n:D→N`, the equality-of-output relation `x ≡_UNM y` iff `n(x)=n(y)` on its actual domain D. Its classes form a set quotient; preserving further operations or answers needs the additional tests below.
- An inverse only on the stated image of an invertible transformation; an operational quotient only for compatible operations and recoverable queries; a `NormalizationFixSpec` only when a representative of an established class is needed.

**Two IDs (do not conflate).**
- `UNM_id?` selects the **UNM mechanism instance** used by this CN‑frame (a `U.Mechanism` instance of type UNM; routing/governance level).
- `NormalizationMethodInstanceId` selects the **normalization method instance** applied to specific coordinate(s), with its validity window and evidence pins (method/application level).

**Minimum declaration set (didactic).**
- In `CN_Spec.comparability`: set `mode`, and (when UNM participates in acceptance/comparison) set `minimal_evidence`.
- In `CN_Spec.normalization`: declare `UNM_id?`, `methods`, `instances`, `method_descriptions`, `invariants`, and (if representatives are required) `fix`.
- In Audit: cite the chosen `NormalizationMethodInstanceId`, `NormalizationMethodDescriptionRef.edition`, characteristic-space and CN-Spec editions, bearer, scope/window, reference or comparison basis, invariants, evidence, and intended comparison. Cite a Bridge, kind relation, or plane relation only when the result or receiving use actually relies on it.

**Non-goals.**
- Not indicator selection (that is **UINDM**).
- Not scoring, aggregation, comparison, selection (USCM / ULSAM / CPM / SelectorMechanism).
- Not a data governance system: UNM is a concept-level mechanism with an explicit governing pattern and auditability.

## A.19.UNM:5 - Archetypal Grounding (Tell–Show–Show) {#archetypal-grounding-tell-show-show}

**Tell.** UNM is the conceptual “front gate” that turns “raw coordinate values” into “values comparable under declared invariants”, by:
1) choosing an admissible normalization method instance (with evidence and validity window),
2) applying it to produce NCVs,
3) returning only the inverse, equivalence, class-level operation or query result whose additional conditions hold for the receiving use.

**Show (System).** A team compares alternatives using `normalization-based` comparability:
- CN-Spec declares:
  - `comparability.mode = normalization-based`
  - `normalization.invariants = {unit-alignment, polarity}`
  - a method instance `M_unitScale` with validity window `VW_2026Q1` and evidence pins.
- UNM applies `M_unitScale` to each coordinate value, producing NCVs.
- CPM compares the NCV-profiles (not raw profiles).
- If evidence pins are missing for a slice, UNM returns `GuardDecision = abstain`, preventing “fake comparability”.

**Show (Episteme) — a many-to-one LUT.** Let D be `{0,1,2}` and `n(0)=0`, `n(1)=n(2)=1`. Applying n to 2 returns the transformed value 1. Equality of outputs partitions D into `{0}` and `{1,2}`: it is reflexive, symmetric and transitive. The directed edge `2→1` supplies no edge `1→2`.

The query `x>0` is constant on each class and can be answered from the class. The query `x>1` is false at 1 and true at 2, so no function of their common class can recover it. Retain x, split that class with the needed distinction, or return the unresolved answer set `{false,true}` when that set answers the receiving question. Selecting 1 as a representative would answer a question about the representative, not the lost original input.

Now let a partial operation f be defined at 0 and 1 but not at 2, with `f(1)=0`. Because `1 ≡_UNM 2` while availability differs, f cannot descend to a representative-independent operation on these classes. Matching only the outputs that happen to exist would miss the failure. Preserve the distinguishing input or refine the class before applying f.

**Show — reversible conversion and partial normalization.** For exact temperature values in the declared physical domain, Celsius-to-kelvin conversion `n(c)=c+273.15` has inverse `c=k-273.15` on its image. For example, 20 °C maps to 293.15 K and back to 20 °C. Measurement uncertainty remains governed by its measurement result; the exact coordinate law does not remove it. More generally, a strictly monotone encoding has an inverse on its image, not automatically everywhere in the named target.

Restrict the LUT above to D=`{0,1}`. Input 2 is then undefined, has no NCV and belongs to no kernel class of that partial normalizer. A policy's degraded-evidence allowance does not define n(2). Likewise, an idempotence claim needs composability and `n(n(x))=n(x)` on the named domain; a function's fibers do not prove it.

**Show (P2W and transformation flow).** Missing/stale inputs:
- A selector (or comparator) requires comparability under `normalization-based` mode.
- UNM finds that a required coordinate value is missing/stale for the current slice and the instance validity window.
- UNM returns `GuardDecision = abstain` (fail-closed) and identifies the missing current measurement. The receiver may reuse an adequate existing result, choose a justified acquisition, or leave this comparison unresolved; any acquisition has its own planning and enactment basis.

## A.19.UNM:6 - Bias‑Annotation {#bias-annotation}

Common cognitive traps around normalization:
- **Normalization-as-truth bias:** treating NCVs as “objective” instead of “objective under declared invariants and validity window”.
- **Hidden-steps bias:** assuming normalization “happened somewhere” and skipping explicit routing/pins.
- **Unit-blindness:** treating numeric sameness as semantic sameness.
- **Proxy legitimacy:** assuming a popular method is legitimate without evidence pins or validity region.

Mitigation: enforce explicit `NormalizationMethodInstance` + validity window + evidence pins; and distinguish the directed output, optional classes and any separately justified operation or query on them.

## A.19.UNM:8 - Common Anti‑Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

1) **Hidden normalization inside scoring or selection**
   Avoid by using `CN_Spec.comparability.mode` and explicit UNM use.

2) **“NCV ⇒ indicator” shortcut**
   Avoid by treating indicatorization as UINDM policy, not a byproduct of normalization.

3) **“We normalized” without declaring invariants**
   Avoid by naming the actual domain, transformation, preserved invariants and lost distinctions; supply a class or congruence claim only under its additional conditions.

4) **Reusing a normalized value after its basis changed**
   Avoid by checking the exact bearer, method and CN-Spec editions, scope/window, comparison basis, evidence, and intended use again; cite a Bridge, kind relation, or plane relation only when the new use actually relies on it.

5) **Choosing a representative implicitly**
   Avoid by either keeping quotient objects abstract or declaring `NormalizationFix`.

6) **Treating a generic mapping word as a specialized relation claim**
   State the normalization's operands, rule, invariants and loss. Test any specialized `Map` or F.9 Bridge claim separately under its defining pattern.

7) **Treating UNM outputs as comparable beyond their declared bearer, basis, scope/window, or reference plane**
   Avoid by keeping comparison local to the recorded premises. Where a conclusion depends on another source-local meaning, bearer kind, or plane, cite the exact obtaining relation and its loss; otherwise constitute a new normalization result or fail closed.

8) **Re-authoring method, basis, or evidence anchors downstream**
   Avoid by citing the exact editioned method, basis, and evidence anchors as refs; a downstream pattern neither rewrites them nor replaces them with a generic registry.

## A.19.UNM:10 - Rationale {#rationale}

UNM is designed as a **minimal canonical semantic surface**:
- Enough structure to prevent illegal comparisons and hidden transformations.
- Explicit routing in CN-frame so normalization is governance, not an algorithmic trick.
- Evidence/calibration are delegated to MM‑CHR to avoid redefining measurement meaning.
- Exact bearer, basis, scope/window and intended-use checks prevent accidental global normalization; actual Bridge, kind, and plane relations are cited only when a conclusion relies on them.

This balances evolvability (methods evolve) with didactic usability (one place to read what UNM is).

## A.19.UNM:11 - SoTA-Echoing — preserve the answer needed after normalization {#sota-echoing-preserve-the-answer-needed-after-normalization}

**Practice question.** May a receiver answer its original query from normalized values after the transformation merges inputs? The selected best-known line checks whether that query is constant on each fiber of the declared function. A serious alternative keeps only bounded normalized values and uses a representative or inverse-transform interface for later queries. The latter is convenient when the receiver deliberately accepts the lost distinctions; it is insufficient for recovering an exact original-input answer that differs within a fiber.

The [Lean reference on quotients](https://lean-lang.org/doc/reference/latest/The-Type-System/Quotients/) supplies the mathematical line: lifting a function requires equal results for equivalent representatives. It also describes canonical-representative implementations as a useful alternative representation. **Adopt** the query-constancy criterion in §4.0, UNM-L2 and §4.4. **Reject** the inference that choosing a representative recovers an original-input query: the representative defines a choice, and recovery still needs constancy. These are mathematical conditions; using Lean or constructing a proof-assistant artifact is not required by UNM.

The [scikit-learn 1.9 MinMaxScaler documentation](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.MinMaxScaler.html) supplies a concrete current preprocessing alternative and its declared trade-off. Optional clipping keeps held-out values in the chosen range, while its documentation warns that inverse transformation may not restore the original data and that clipping can distort the test distribution. **Adapt** this explicit loss disclosure as a receiving-use check, rather than banning bounded preprocessing or treating the software interface as evidence of invertibility.

For example, a declared clipped transform n(x)=min(1,max(0,x/100)) sends 120 and 150 to 1. The query “was x above 130?” gives different answers, so it cannot be recovered from that NCV or its class representative. Keep the original value, refine the output with the needed distinction, or return the unresolved answer allowed by the receiving rule. This is the same test used by the finite-domain example in §5 and the Result branch checklist; separately inherited partial operations also retain their availability check.

At comparable effort, both choices use the same declared transform and query. One counterexample within a fiber can settle failure cheaply; a positive exact-recovery claim needs a constancy argument over the admitted domain, not just sampled successes. Keeping additional input information has a storage/handling cost, while clipping can be appropriate for a model that only needs its bounded input. The chosen rule makes that trade-off explicit and leaves ordinary transformed-value use cheap. Reopen when the receiver changes its query, the transformation or domain changes, or a proposed smaller representation retains the required answer with a sound argument. Neither software documentation nor the quotient theorem supplies measurement legitimacy, evidence sufficiency or assurance for a particular application.


## A.19.UNM:End {#end}
