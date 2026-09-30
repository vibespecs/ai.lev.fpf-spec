# C.11.CRC - Configuration-Relative Contribution Comparison {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Tech name:** `ConfigurationRelativeContributionComparison`
>
> **Plain name:** compare what this finite change adds to the current configuration
>
> **Type:** C-pattern
>
> **Status:** Stable
>
> **Placement:** a narrow companion used before `C.11` when its comparison basis is not yet available

## C.11.CRC:0 - Use This When {#use-this-when}

Use this pattern when a bounded addition, replacement, removal, intervention, experiment, information/computation acquisition, capability-development element, project, or component is being justified by “what it adds,” but the current configuration, interactions, resources, horizon, uncertainty, and receiving decision are not yet part of the comparison.

**First useful result.** Return one ordinary `C.2.1` episteme that compares a realizable finite changed configuration with the current configuration under a declared basis. State the result coordinates and resource coordinates, interactions, uncertainty, option effects, unsupported overreads, and the `C.11` decision that can consume the claim. The comparison does not choose the option.

**Cheap exit.** If a current `A.19`/`C.11` account already states the same finite baseline, change, horizon, result and resource coordinates, interactions, uncertainty, and reopen condition, use that account directly.

**Not this pattern when.** Do not use it for a source-only comparison with no realizable configuration change; for a purely causal question under `C.28`; for a mathematical-lens question already answered by `C.29` and a field Method; for an archive/front relation under `C.18`; or as a substitute for field-specific finance, optimization, operations, engineering, experimental-design, or capability-development calculation.

## C.11.CRC:1 - Problem Frame {#problem-frame}

Candidates are often described by an isolated score, average benefit, frequency, local gradient, shadow price, or expected information gain. The receiving decision concerns something else: whether a finite change is worthwhile *from this current configuration*, over this horizon, for these affected Systems, under these resource and authority constraints.

The same candidate can contribute differently when prerequisites, complements, substitutes, bottlenecks, thresholds, congestion, implementation capability, uncertainty, reversibility, and future options differ. A good isolated characteristic can therefore coexist with a dominated configuration change, and a weak-looking local result can preserve valuable options or reveal a critical blocker.

## C.11.CRC:2 - Problem {#problem}

Without an explicit configuration-relative comparison, practitioners make at least six transfers:

- a finite change is approximated by a derivative outside its valid region;
- a shadow price for one active constraint is multiplied into the value of an asset that changes several constraints;
- a candidate is compared with an empty system instead of the actual current configuration;
- several result and resource coordinates are hidden inside one scalar;
- interaction and common-cause overlap are counted as independent contribution; and
- information, option value, or reversibility is treated as realized benefit.

`A.19` provides comparison mechanisms and characteristic spaces, `C.29` governs mathematical lenses, and `C.11` governs the choice. The remaining recurring practitioner action is to construct the finite comparison claim that those patterns can consume.

## C.11.CRC:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Local simplicity vs finite reality | Derivatives and local prices can be useful while the realizable change is indivisible, thresholded, or interacting. |
| Multiple results vs decision closure | Several benefits, harms, and resources must stay visible without preventing a bounded choice. |
| Current value vs future options | Waiting, learning, staging, reversibility, and path dependence can change later possibilities. |
| Reuse vs domain authority | FPF can supply the comparison grammar; practitioners must use domain Methods to calculate quantities and judge evidence. |
| Recognition vs assurance | A well-formed comparison can still lack trustworthy inputs, implementation capability, or required assurance. |

## C.11.CRC:4 - Solution {#solution}

Construct the smallest finite counterfactual comparison that can change one named decision.

1. **Name the receiving decision.** State the deciding System, current `DecisionSubject`, decision deadline, current `OptionSet` or the option-set question that this comparison will inform, and which result could change the decision.
2. **Freeze the current configuration.** Name the actual or currently relied-on configuration `S0`, system boundary, affected Systems, the holder or beneficiary and what it holds or benefits from, relevant environment, and what is held fixed only for this comparison. If the affected-System coordinate is missing and could change the comparison, use `A.1.CSD` first; bring back only consequence claims compatible with this `S0`/`Δ`/`S1`, horizon, evidence window, and receiving decision. A historical, empty, or ideal configuration is not the default baseline.
3. **Name the finite change.** State the addition, replacement, removal, intervention, or probe `Δ`, the realizable candidate configuration `S1`, admissibility conditions, implementation capability, planned transition work, reversibility, and excluded variants.
4. **Fix horizon and scenarios.** State the interval, relevant states or scenarios, timing assumptions, and any decision or evidence window. Do not combine results from incompatible horizons without an explicit mapping.
5. **Declare result coordinates.** Name the result vector whose coordinates can change the decision and the protected coordinates that may not be silently scalarized. Include affected-System consequences and distributional differences when current.
6. **Declare resource coordinates.** For the action, transition, information acquisition, and computation, name the attention, capital, time, material, energy, and other resources consumed or expected to be consumed in this field case. State required authority separately as an admissibility condition. Keep costs of evaluating and realizing the change distinct.
7. **Recover constraints and interactions.** State active and potentially activated constraints, complements, substitutes, thresholds, congestion, downstream effects, common causes, overlaps, and double-counting risks.
8. **Recover option effects.** State whether the finite change opens, closes, delays, preserves, or makes irreversible later options. Keep information value and option value as decision inputs, not already realized operating results.
9. **Qualify evidence and uncertainty.** Identify source claims, currentness, uncertainty, sensitivity/robustness results, transfer limits, rival explanations, and `A.10` reliance dispositions where an evidence-bearing claim is used.
10. **Write the comparison claim.** State what `S1` contributes relative to `S0` only under the declared coordinates, horizon, scenarios, constraints, interactions, and evidence. Use dominated, non-dominated, beneficial, harmful, or indeterminate wording only when the stated relation supports it; do not force one scalar winner.
11. **Route mathematical near-misses.** Apply the distinction in `C.11.CRC:4.2`; the finite comparison may consume a derivative, sensitivity, shadow price, variational, or inference result without becoming identical to it.
12. **Return to `C.11`.** Use `C.11` to combine this claim with preferences, belief state, outcome model, probe worth, and other premises and emit one `ChoiceResult`. State the smallest configuration, horizon, evidence, resource, constraint, or option-set change that reopens this comparison.

### C.11.CRC:4.1 - Lightweight comparison form {#lightweight-comparison-form}

`ConfigurationRelativeContributionComparison@Context` is a form name for one ordinary comparison episteme. It is not a root U-kind, universal delta value, selector result, or decision.

```text
receivingDecisionRef:
currentConfigurationRef: S0
candidateFiniteChangeRef: Δ
candidateConfigurationRef: S1
systemBoundaryAndAffectedSystems:
horizonAndScenarios:
resultCoordinateRefs:
protectedCoordinateRefs:
resourceCoordinateRefs:
constraintsAndInteractions:
transitionAndImplementationBasis:
futureOptionEffects:
evidenceAndUncertaintyRefs:
comparisonClaim:
unsupportedOverreads:
reopenCondition:
nextGoverningPattern: C.11
```

Omit a field only when it cannot change this comparison and that omission is apparent from the bounded case. A polished record cannot compensate for a missing current configuration or decision.

### C.11.CRC:4.2 - Mathematical and model-routing distinction {#mathematical-and-model-routing-distinction}

| Expression encountered | Exact question | Required boundary |
| --- | --- | --- |
| Finite difference or counterfactual configuration comparison | What changes between realizable `S0` and `S1` over the declared horizon? | Default here for indivisible, non-smooth, thresholded, path-dependent, or strongly interacting changes. Do not infer additivity. |
| Derivative or gradient | What is the local rate of change with respect to a coordinate under smoothness and small-change assumptions? | It approximates the finite contribution only when the validity region and remainder are adequate for `Δ`. |
| Sensitivity | How does a result vary with a parameter, assumption, input, model, or scenario? | It supplies robustness or assurance information; it need not describe a realizable configuration change. |
| Shadow price or dual variable | What is the local value of relaxing a formulated active constraint under the primal/dual model? | It depends on formulation, active set, regularity, units, and local region; it is not the contribution of an arbitrary asset or intervention. |
| Functional variation / calculus of variations | How does a functional change when the varied object is a function, path, trajectory, field, control, or shape in a declared admissible variation space? | Name the functional, admissible variations, constraints, boundary conditions, stationarity/extremum claim, sufficiency, and validation. An Euler–Lagrange equation is not a generic contribution claim or proof that a physical System optimizes. |
| Variational inference | Which member of an approximation family best approximates a target probability distribution under a declared divergence or bound? | The result is an approximate distribution and uncertainty account, not an extremal physical trajectory, capability acquisition, or general marginal value. |
| Evolutionary variation | How are retained variants generated and selected in an evolutionary or cultural process? | The shared word *variation* does not identify the mathematical object or Method above; route to `C.18`, `C.36`, or the field practice. |

This is why calculus of variations matters without becoming the default interpretation of marginality. When the candidate is a whole trajectory, field, function, control, or shape, pointwise finite-coordinate reasoning can miss the coupled admissible deformation. `C.29` governs the mapping from the world or domain model to that mathematical object, what structure is preserved or lost, and when the lens must stop. Specialist practice governs derivation, discretization, solver choice, optimality and sufficiency checks, and validation.

### C.11.CRC:4.3 - Recognition and assurance split {#recognition-and-assurance-split}

**Recognition.** A user can recognize a conforming comparison when `S0`, finite `Δ`, `S1`, boundary, horizon, result and resource coordinates, interactions, uncertainty, and receiving decision are visible.

**Assurance.** Trust in the numbers and relations remains separate. Field evidence must support the baseline and candidate behavior; implementation capability and the basis for planned transition work must be credible; causal claims use `C.28`; source reliance uses `A.10`; for an assurance claim, use `B.3` with the named target claim and assurance use; authority and permission use their direct patterns. This pattern creates none of those results.

## C.11.CRC:7 - Conformance Checklist {#conformance-checklist}

1. Is one receiving decision named?
2. Are `S0`, finite `Δ`, and realizable `S1` explicit?
3. Are system boundary, affected Systems, horizon, scenarios, and evidence window compatible—and, when a missing bearer could change the comparison, was `A.1.CSD` used before freezing this coordinate?
4. Are result and resource coordinates explicit, with protected coordinates not silently scalarized?
5. Are implementation capability, planned transition work, reversibility, and excluded variants recoverable?
6. Are constraints, interactions, overlap, thresholds, congestion, and downstream effects considered where material?
7. Are future option effects distinguished from realized results?
8. Are evidence, uncertainty, sensitivity/robustness, transfer limits, and unsupported overreads visible?
9. Is each derivative, sensitivity, shadow-price, functional-variation, variational-inference, or evolutionary-variation result used only for its exact question?
10. Does the output remain a comparison claim, with `C.11` retaining the `ChoiceResult`?
11. Is the smallest reopen condition stated?

## C.11.CRC:9 - Consequences and Reopen Condition {#consequences-and-reopen-condition}

**Benefits.** Finite additions, removals, replacements, probes, and investments become comparable without requiring additivity, smoothness, or a universal scalar. Domain calculations can be reused while their validity regions remain visible. The result gives `C.11` a stable comparison input and keeps choice authority there.

**Costs.** Practitioners must name a baseline, vectors, interactions, and uncertainty that an isolated score could hide. Some cases remain indeterminate until field evidence or implementation capability is available.

Reopen this pattern when repeated cases cannot express their finite comparison with this spine; when a current `A.19`/`C.11` composition fully absorbs the same practitioner entry, action, first result, and stop; or when a mathematical branch requires a different transdisciplinary action rather than a field-specific Method.

## C.11.CRC:12 - Relations {#relations}

- **Builds on:** `C.2.1`, `A.10`, `A.19`, `C.16`, `C.27`, `C.28`, and `C.29`.
- **Supplies:** one finite comparison claim to `C.11`; it can also supply an input to a field-specific portfolio, programme, intervention, architecture, or experiment decision.
- **Coordinates with:** `A.1.CSD` when affected-System consequence coordinates are missing; `C.18` when the candidate changes the possibility space; `C.19` for pool governance; `B.3` for assurance; `A.15` for the distinction between transition plans (`A.15.2`) and performed transition Work (`A.15.1`); and the direct field practice for calculation and validation.
- **Keeps outside:** universal marginal value, a new delta kind, domain formulas and thresholds, causal proof, assurance, permission, selected-set declaration, and `ChoiceResult`.


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/C-2-1#root, spec://ai.lev/fpf-spec/contract/A-10#root, spec://ai.lev/fpf-spec/contract/A-19#root, spec://ai.lev/fpf-spec/contract/C-16#root, spec://ai.lev/fpf-spec/contract/C-27#root, spec://ai.lev/fpf-spec/contract/C-28#root, spec://ai.lev/fpf-spec/contract/C-29#root. @status:spec/done
- @fact:SUPPLIES Supplies: one finite comparison claim to spec://ai.lev/fpf-spec/contract/C-11#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/C-18#root, spec://ai.lev/fpf-spec/contract/C-19#root, spec://ai.lev/fpf-spec/contract/B-3#root, spec://ai.lev/fpf-spec/contract/A-15#root, and direct field calculations. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-1-CSD#root, spec://ai.lev/fpf-spec/contract/A-15-11#root, spec://ai.lev/fpf-spec/contract/C-11#root, spec://ai.lev/fpf-spec/contract/C-11-DUA#root, spec://ai.lev/fpf-spec/contract/C-17#root, spec://ai.lev/fpf-spec/contract/C-19#root, spec://ai.lev/fpf-eng-doca/contract/DOCA-1-CHR#root, spec://ai.lev/fpf-eng-doca/contract/DOCA-4#root, spec://ai.lev/fpf-eng-doca/contract/DOCA-5#root, spec://ai.lev/fpf-eng-doca/contract/DOCA-6#root, spec://ai.lev/fpf-eng-exd/contract/EXD-6#root, spec://ai.lev/fpf-eng-hcd/contract/HCD-2#root, spec://ai.lev/fpf-eng-ops/contract/OPS-10#root, spec://ai.lev/fpf-eng-ops/contract/OPS-10-1#root, spec://ai.lev/fpf-eng-ops/contract/OPS-11#root, spec://ai.lev/fpf-eng-ops/contract/OPS-9#root, spec://ai.lev/fpf-eng-psd/contract/PSD-11#root, spec://ai.lev/fpf-eng-str/contract/STR-14#root, spec://ai.lev/fpf-eng-str/contract/STR-9#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/C-11-CRC
