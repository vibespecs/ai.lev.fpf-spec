# C.16.IR - Determine What a Measurement Indication Can Resolve {#root}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method pattern
> **Status:** Draft
> **Normativity:** Normative

## C.16.IR:1 - Problem frame {#problem-frame}

Use this pattern when an available measurement relation leaves open what can be inferred from an indication. A loaded voltmeter reading can fit several source voltages. A saturated sensor can establish that a quantity exceeds one threshold while leaving a higher threshold unresolved. A stored counter remainder can correspond to several event counts.

**First useful move.** Try to construct two cases that fit the same indication and stated conditions but give different answers to the receiving question. If an ideal instrument reports the square of a signed displacement, a reading of 9 square metres fits both +3 and -3 metres. It determines the magnitude but leaves the direction unresolved. Restricting displacement to nonnegative values would resolve that difference only when the subject conditions support the restriction.

The Method determines what the indication resolves under the available relation, domain and uncertainty assumptions. Its result can be a value, a compatible range, a settled comparison, two remaining alternatives or an incompatibility among the premises. C.16 supplies the subject, Characteristic, Scale, performed measurement and result meanings. C.16.MR constructs a missing measurement relation.

The examples require elementary equations, inequalities and integer remainders. More difficult relations can require subject-specific inverse methods, probability models or validated numerical computation.

Apply an already suitable conversion or analysis function directly when it supplies the answer with adequate uncertainty. Use this construction when ambiguity, omitted influences or the meaning of a computed range can change that answer.

## C.16.IR:2 - Problem {#problem}

A measurement relation can predict the indication without allowing the sought value to be uniquely recovered. Several quantities may jointly affect the same reading; a conversion can erase distinctions through clipping, averaging, squaring or wrapping. An algorithm can return one solution while other compatible solutions remain.

The receiving question also matters. An interval may settle an operating threshold even when a point value is unavailable. Conversely, precise arithmetic on one arbitrarily selected solution can hide a decision-changing ambiguity.

The problem is to recover the alternatives allowed by the indication and its conditions, then determine which differences matter to the intended use. This requires keeping the observation, model assumptions, computed approximations and supported conclusion distinguishable throughout the calculation.

## C.16.IR:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Convenient answer and remaining alternatives | One number is easy to use; several values may fit the same reading. |
| Target and influential quantities | Full parameter recovery can be costly; the sought quantity may already be determined. |
| Exact data and uncertain data | An ideal relation may have one solution while the actual error range permits many. |
| Complete computation and sufficient conclusion | Describing the entire compatible set can be expensive; a bound can answer the working question. |
| Additional observation and changed subject | A second reading can distinguish alternatives only under the relations that connect the two measurement situations. |
| Calculation and model revision | Inconsistent premises require diagnosis; forcing a numerical answer can conceal the conflict. |

## C.16.IR:4 - Solution {#solution}

Construct the cases compatible with the indication and relevant conditions. Obtain the sought values represented by those cases, retaining the distinction between feasible examples and bounds that contain all solutions. Use that result to answer the current question.

### C.16.IR:4.1 - Fix the sought distinction and available relation {#fix-the-sought-distinction-and-available-relation}

State the quantity or property being sought, its subject and conditions, and the question that depends on it. Distinguish the state before measurement, the state during interaction and the reported indication when they differ. For the voltmeter case in :5.1, the target is open-circuit source voltage, while the reading is the voltage with the instrument connected.

Recover the relation used to interpret the indication, including the domain of each unknown, relevant calibration, influences and error assumptions. Keep a known input as known and an unknown influence as a variable. Derive a missing contribution with C.16.MR before treating it as part of the available relation.

A domain restriction needs its subject meaning. Positive length, a known rotation range and a passive resistance bound can exclude mathematical solutions when those conditions hold. An inconvenient branch is a reason to inspect the model, not a reason to drop that branch.

State whether the receiving question needs a point value, an interval, a threshold decision or a comparison. This selects which remaining differences matter.

### C.16.IR:4.2 - Construct the jointly compatible cases {#construct-the-jointly-compatible-cases}

Substitute the obtained indication into the relation. Combine that condition with the admitted domains and available information about influences. For repeated or multiple readings, state which subject values and parameters are shared and which may change between them.

With bounded error, include the unknown error in its stated range. If a relation gives an ideal indication f(x,z), x is the sought value, z contains influential unknowns and r is the reported reading, a common model is:

`r = f(x,z) + e, with e in the supplied error range.`

Use that equation only when additive error describes the actual indication convention. An error before clipping, an error after clipping and a missed event can require different relations.

A compact mathematical expression for the compatible sought values is:

`S(r) = {x : there exist admitted z and e for which r = f(x,z) + e}.`

An implicit relation can be used in the same way without converting it to a single-valued function. Retain dependencies among unknowns: independently combining their separate ranges can introduce cases excluded by their joint relation.

A probability model supplies a different additional contribution. Values inside a bounded-error range have no assigned likelihood merely from membership in that range. A confidence interval or posterior distribution requires its corresponding statistical method and assumptions.

### C.16.IR:4.3 - Obtain values or bounds without losing alternatives {#obtain-values-or-bounds-without-losing-alternatives}

Choose the lightest adequate computation. Solve a small equation, eliminate an influential variable, enumerate a finite domain, or obtain a bound. A numerical formulation can use C.29.2 when its construction is nontrivial.

During elimination, preserve the conditions of each operation. Dividing by an unknown expression can discard its zero case. Squaring an equation can admit additional roots. Test the retained cases in the original relation and domains. Finding one root establishes a possible case; uniqueness requires an argument covering the admitted domain or a sufficient justified restriction.

For several unknowns, obtain the sought value from each compatible joint case. The other unknowns can remain unresolved when every compatible case gives the same sought answer. Section :5.1 gives a source voltage determined while its internal resistance remains unknown.

When a complete solution is costly, distinguish two useful computational results:

- A **feasible example** is one case that satisfies the original relations and conditions. Two such cases can establish a consequential ambiguity.
- An **outer bound** contains every compatible sought value but can also contain values that no case realizes. If the whole bound satisfies an inequality, that inequality holds for every compatible value. A bound spanning both sides of a threshold alone does not establish that both outcomes are possible.

For example, let an ideal indication obey r = x² with x ≥ 0, and let r = 9. A computation that has retained only the outer bound 0 ≤ x ≤ 4 leaves values on both sides of the threshold x = 2. The original relation, however, admits only x = 3. Thus x > 2 is resolved, and no feasible witness with x ≤ 2 exists. The coarse bound left the calculation unfinished; it did not establish ambiguity in the indication.

Use a validated enclosure method when the conclusion depends on retaining every solution through numerical calculation. Ordinary sampling can discover a counterexample but can miss another branch. When computation has not established existence, completeness or a needed bound, retain that limitation in the answer instead of interpreting solver termination as the missing result.

### C.16.IR:4.4 - Test what is resolved for the receiving question {#test-what-is-resolved-for-the-receiving-question}

For a point-value question, test whether all compatible cases agree on that value. For a threshold or other condition, test whether it holds throughout the compatible set or a sufficient outer bound. Establish that the premises admit a case before using such a bound as the interpretation of a measurement; substitution of an available feasible case may suffice.

If the question remains unresolved, construct two compatible cases with different answers. Check both against all readings, shared parameters and domain conditions. These witnesses identify what an additional relation or observation would have to distinguish.

Separate a proved empty compatible set from a search that has not found a case. An empty set shows that the combined readings, model and conditions are inconsistent. Locate a consequential conflict; the cause may be a recording error, a changed subject, an unsuitable error bound or an inadequate measurement relation. A failed search instead limits the computational result.

A point result under ideal data can broaden when input uncertainty is restored. Recompute the relevant range when a reading, calibration coefficient or domain changes. Numerical sensitivity and branch ambiguity can require different remedies.

### C.16.IR:4.5 - Choose the useful return {#choose-the-useful-return}

Return the value, range or comparison with the conditions that support it. Stop when it is sufficient for the intended use. A lower bound can be more useful than an unnecessarily precise estimate.

For an unresolved decision, use the differing cases to choose a potentially useful next contribution: an available second reading, a different operating range, a better bound, a changed instrument or a narrower conclusion. Examine what that contribution could distinguish before obtaining it. In :5.3, another counter using a different modulus distinguishes alternatives that repeating the same remainder preserves.

Use C.11.DUA when the value and effort of reducing the ambiguity need comparison. It can be reasonable to act with the remaining uncertainty or leave the question unresolved. B.5.MPC.R coordinates a needed revision across the physical, mathematical and computational contributions.

## C.16.IR:7 - Conformance Checklist {#conformance-checklist}

- @fact:CC-C16-IR-1 **CC-C16.IR-1 - Receiving distinction.** The target property, subject conditions and required conclusion are stated. @status:spec/work
- @fact:CC-C16-IR-2 **CC-C16.IR-2 - Joint premises.** Readings, domains, influences, errors and shared-value assumptions enter the available relation with their meanings preserved. @status:spec/work
- @fact:CC-C16-IR-3 **CC-C16.IR-3 - Inverse operations.** Elimination or numerical calculation retains the needed branches and tests candidates in the original relations. @status:spec/work
- @fact:CC-C16-IR-4 **CC-C16.IR-4 - Result strength.** Feasible cases, outer bounds, proved emptiness and incomplete computation have distinct interpretations. @status:spec/work
- @fact:CC-C16-IR-5 **CC-C16.IR-5 - Supported answer.** Uniqueness or a threshold answer follows across the compatible cases; claimed ambiguity has feasible witnesses with different answers. @status:spec/work
- @fact:CC-C16-IR-6 **CC-C16.IR-6 - Uncertainty meaning.** A range, confidence statement or probability distribution keeps the assumptions that justify that form. @status:spec/work
- @fact:CC-C16-IR-7 **CC-C16.IR-7 - Useful return.** Work stops with a sufficient result or identifies a contribution capable of changing the unresolved answer. @status:spec/work

## C.16.IR:9 - Consequences {#consequences}

The practitioner can identify what information the measurement actually supplies for a question. A useful bound can end inquiry; an explicit pair of alternatives can direct a better observation or a model repair.

The cost grows with the relation and the conclusion claimed. A single ambiguity witness can be cheap, while excluding every alternative may require a global argument or specialized computation. The Method retains that difference so the amount of work follows the receiving use.

## C.16.IR:12 - Relations {#relations}

- **C.16** supplies measurement subject, Characteristic, Scale, model, actual work, uncertainty and obtained-result meanings.
- **C.16.MR** constructs a missing or unsuitable measurement relation.
- **C.29.1** examines the correspondence and preserved distinctions when mathematical representation itself is in question.
- **C.29.2** constructs a needed computational formulation and its accuracy conditions.
- **A.3.3.PI** retains information for a future question under a dynamics account; the present Method interprets an available indication.
- **B.5.MPC.R** coordinates a needed revision across physical, mathematical and computational contributions.
- **C.11.DUA** compares the useful effect and effort of obtaining additional information.


## Dependencies {#dependencies}

- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/C-16#root, spec://ai.lev/fpf-spec/contract/C-16-MR#root, spec://ai.lev/fpf-spec/contract/C-29-1#root, spec://ai.lev/fpf-spec/contract/C-29-2#root, spec://ai.lev/fpf-spec/contract/A-3-3-PI#root, spec://ai.lev/fpf-spec/contract/B-5-MPC-R#root and spec://ai.lev/fpf-spec/contract/C-11-DUA#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-1-RI#root, spec://ai.lev/fpf-spec/contract/C-16-RM#root, spec://ai.lev/fpf-think-mmp/contract/MMP-11#root, spec://ai.lev/fpf-think-mmp/contract/MMP-12#root, spec://ai.lev/fpf-think-mmp/contract/MMP-13#root, spec://ai.lev/fpf-think-mmp/contract/MMP-15#root, spec://ai.lev/fpf-think-mmp/contract/MMP-7#root, spec://ai.lev/fpf-think-phy/contract/PHY-9#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/C-16-IR
