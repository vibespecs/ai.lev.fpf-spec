# C.16.IR - Determine What a Measurement Indication Can Resolve: depth {#depth}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## C.16.IR:5 - Archetypal Grounding {#archetypal-grounding}

### C.16.IR:5.1 - One source, two loads and an unidentified influence {#one-source-two-loads-and-an-unidentified-influence}

Suppose a source has unknown open-circuit voltage E ≥ 0 and finite internal resistance Rs ≥ 0. An ideal meter of known input resistance Rm > 0 reads the connected voltage:

`V = E*Rm/(Rs + Rm).`

The relation and passive-source assumptions are supplied. The question is whether E is at most 8 V.

A reading of 5 V with Rm = 1 MΩ gives:

`E = 5 V*(1 + Rs/(1 MΩ)).`

Rs = 0 and E = 5 V fit the reading; Rs = 1 MΩ and E = 10 V also fit it. The threshold question is unresolved. The reading does establish E ≥ 5 V under the stated domain.

Now a meter with Rm = 3 MΩ reads 7.5 V. Assume E and Rs stayed unchanged between the readings and both meters obey the given model. The two equations share those two unknowns. Express E from each equation and equate:

`V1*(1 + Rs/R1) = V2*(1 + Rs/R2).`

Hence, when the denominator is nonzero,

`Rs = (V2 - V1)/(V1/R1 - V2/R2).`

The supplied readings give Rs = 1 MΩ and E = 10 V. Substitution recovers both 5 V and 7.5 V. The answer to E ≤ 8 V is now no.

The shared-source condition does work here. If E changes between readings, replacing it with E1 and E2 leaves the original inference unsupported. A second number is useful through the relation connecting its measurement to the first.

For two zero readings under the same model, E = 0 follows while Rs can be any finite nonnegative value. A zero denominator in the derived formula is a reason to return to the original equations. Full recovery of Rs is unnecessary for this voltage result.

### C.16.IR:5.2 - A saturated reading can settle one threshold {#a-saturated-reading-can-settle-one-threshold}

An ideal instrument reports r = min(y,10), where y ≥ 0 is a quantity expressed on the instrument's stated scale. For r = 10, every y ≥ 10 is compatible.

If the working question is y ≥ 8, the reading settles it. If the question is y ≥ 12, y = 10 and y = 13 are compatible cases with different answers. Reporting y = 10 as the determined quantity would lose that distinction.

Now suppose the reported reading follows `r = min(y,10) + e`, with -0.2 ≤ e ≤ 0.2. This error is applied after the clipping operation. For the same r = 10, the ideal clipped value can lie from 9.8 to 10. The compatible set becomes y ≥ 9.8: y = 9.8 with e = 0.2 is a feasible endpoint, and every y ≥ 10 fits with e = 0.

The reading still settles y ≥ 8. It no longer settles y ≥ 10, since y = 9.8 and y = 10 are both compatible. This is a bound-based result; no probability was assigned to the error. Repeated readings do not narrow that bound merely by being repeated. A narrower result needs a relation that supports the reduction, such as a justified stochastic error model or a smaller error bound.

### C.16.IR:5.3 - Combining counter remainders {#combining-counter-remainders}

A device starts at zero, increments once per event and stores N modulo 16. No reset or missed event occurs. A supplied count bound is 0 ≤ N < 100. The stored value 5 permits:

`N in {5,21,37,53,69,85}.`

These six values come from `N = 5 + 16*k` with an integer k in the range allowed by the bound. They all satisfy the original operation. The reading settles N < 90, while N < 30 remains unresolved; 21 and 37 are witnesses.

Suppose a second counter starts at the same event boundary, sees every same event, and stores N modulo 17. It reports 4. Test the six candidates against this second relation: only N = 21 remains. The physical event correspondence and initialization make the mathematical intersection appropriate.

If the supplied bound is relaxed to N < 300, both 21 and 293 satisfy the two remainders. The earlier uniqueness conclusion therefore depended on the bound. If the counters cover different event intervals, use separate counts and recover the relation between them before combining their readings.

## C.16.IR:6 - Bias-Annotation {#bias-annotation}

Under the five Principle-Taxonomy lenses of E.3 (Gov, Arch, Epist, Prag and Did), this pattern is scoped to interpreting indications through available relations. The cases use supplied, simple relations. Real inverse problems may be high-dimensional, unstable or sensitive to uncertain model structure. Establishing complete bounds can then require considerably more work than exhibiting one ambiguity.

The set-based branch treats uncertainty as admitted possibilities. Statistical inference and decisions under risk can distinguish those possibilities by likelihood, loss or preference when their own assumptions are supplied. Use the result form appropriate to the question; a demand for uniqueness can make an already useful measurement appear inadequate.

## C.16.IR:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Failure in the worked situation | Consequence | Repair |
| --- | --- | --- |
| Use the displayed number as the sought value | Loading or clipping changes the answer. | Interpret the reading through the available relation and target conditions. |
| Select one root and discard the rest | A sign or other consequential branch disappears. | Test the admitted domain and retain every branch relevant to the conclusion. |
| Demand every parameter's unique value | Work continues after the requested quantity is determined. | Test agreement on the sought value, as in the zero-voltage case. |
| Treat a wide computational enclosure as realized ambiguity | Approximation slack is mistaken for attainable alternatives. | Construct feasible witnesses or report the unresolved computation. |
| Combine readings without their shared-subject condition | An apparent extra equation relates different unknowns. | Recover the time, initialization and subject correspondence before intersection. |
| Convert repeated readings into a narrower bound by counting them | A common bias or unrestricted bounded error survives repetition. | Supply the error relation that justifies the proposed reduction. |

## C.16.IR:10 - Architectural Rationale {#architectural-rationale}

Indication production and interpretation have different directions. A procedure can map many subject conditions to the same output. Interpreting that output therefore asks which of those conditions remain possible and which distinctions the receiving question needs.

This explains the separate contribution from C.16.MR. A measurement relation can already be available while its inverse use is unresolved. Constructing compatible cases makes that relation usable without requiring a new model or an estimate for every parameter.

The same reasoning connects physical measurement, mathematical inverse relations and computational information loss. Their subject premises differ. A source's loading law, an instrument's clipping order and a counter's event semantics supply the cases to which the common reasoning applies.

## C.16.IR:11 - SoTA-Echoing {#sota-echoing}

**Practice question.** What does an indication determine when an available relation has influential unknowns, lost distinctions or consequential input uncertainty?

**Selected answer and serious alternative.** Adopt a question-relative compatible-set calculation or sufficient bound when those features can change the answer. The serious alternative is direct use of a suitable calibrated analysis function, or a justified estimate with its uncertainty. Keep that cheaper route when it settles the same question. In :5.1, using one loaded reading as E returns the wrong target; two elementary compatible cases expose the loss at comparable effort. In :5.2, a threshold result needs less work than a point estimate. The selected method trades a convenient single output for the alternatives needed by the decision.

**Measurement-model contribution.** [JCGM GUM-6:2020, §11.4 and §§13.5–13.6](https://www.bipm.org/documents/20126/2071204/JCGM_GUM_6_2020.pdf) distinguishes calibration and analysis functions, permits directly estimating an analysis function, and retains implicit measurement models under a stated local-uniqueness assumption. **Adapt** that direction distinction in :4.1–4.3. When uniqueness is unavailable, :4.4 returns the alternatives needed by the question. The document supplies quantitative measurement-model practice; it does not establish that every inverse problem has a unique solution.

**Computational contribution.** [IBEX 2.9, Contractors, Introduction and Forward-Backward](https://ibex-team.github.io/ibex-lib/contractor.html) describes filtering a domain while preserving its feasible solutions. **Adopt** that preservation requirement for the bounded numerical branch in :4.3. A surviving outer domain can still contain infeasible points, which motivates the feasible-witness distinction. Symbolic elimination and finite enumeration suffice for the worked cases.

The common question, target projection, sufficient-result return and diverse cases are conceptual synthesis. Specialized inverse, statistical and decision methods contribute where the question needs their further operations or guarantees. Reopen the comparison when a cheaper analysis settles the same use with equivalent uncertainty, when a proposed bound misses a compatible branch, or when a changed measurement relation invalidates the result.


## C.16.IR:End {#end}
