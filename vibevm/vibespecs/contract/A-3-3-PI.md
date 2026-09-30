# A.3.3.PI - Retain the Information Needed for Prediction {#root}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method pattern
> **Status:** Draft
> **Normativity:** Normative

## A.3.3.PI:1 - Problem frame {#problem-frame}

Use this pattern when a description of the present leaves a future result unresolved, or when you want to simplify a predictive account without losing an answer that matters. A total can hide components that change at different rates. A current readout can merge situations whose next outcomes have different probabilities. A summary adequate for the next output can lose information needed two steps later.

**First useful move.** Find two admitted situations that the proposed description treats as the same. Apply the supplied change rule under the same inputs and compare the future result needed by the question. If one kilogram of substance A becomes half a kilogram after treatment, while one kilogram of substance B becomes a quarter, the description “one kilogram remains” cannot determine the next total. It can still supply the range from a quarter to half a kilogram.

The Method constructs information sufficient for a stated prediction: additional state values, a usable history, a distribution over possible states or a bound that settles the question. Its result can also identify which missing distinction would change the answer. It connects the state, transition and observation contributions recognized by A.3.3.

The elementary cases require arithmetic, equations and conditional probabilities. More demanding models need their subject-specific estimation, reduction or computational Methods. The common task is to choose and use the retained information with the prediction it supports.

When an available prediction or bound already settles the working question, use it. When the missing contribution is a rule of change, A.3.3.TR helps construct that rule. The present Method applies when the retained information and the desired prediction need to be reconciled.

## A.3.3.PI:2 - Problem {#problem}

A description can correctly report the present while omitting what determines its continuation. Recovering every underlying detail is often impractical, and a useful future distinction may require only a small part of that detail.

Adding observations does not automatically solve the problem. Their timing, the actions taken between them, measurement error and the assumed law determine what can be inferred. A fitted predictor can also work for one interval and accumulate consequential error when repeatedly applied.

The practical problem is to retain enough information for the future question, and to know what result remains obtainable when the available information supports only a range, a conditional probability or a shorter horizon.

## A.3.3.PI:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Compact description and predictive distinctions | Aggregation simplifies a model but can merge states that evolve differently. |
| Observation and model state | A reading reports some aspect of the situation; a prediction may need an unobserved quantity or a distribution over possible values. |
| Present values and history | A past observation can recover a missing distinction, while a long history can make computation expensive. |
| One result and repeated prediction | Information can determine one requested output without supplying a state that can be updated indefinitely. |
| Ideal recovery and measurement error | Algebra can reconstruct hidden values while amplifying errors in the readings used. |
| Additional information and usable uncertainty | A bound can settle a decision before identifying the actual underlying state. |

## A.3.3.PI:4 - Solution {#solution}

Begin with the future distinction needed in the work. Compare the situations merged by the proposed description, construct a description or uncertainty account that retains the consequential differences, and use it at the required horizon.

### A.3.3.PI:4.1 - Specify the future question and the available account {#specify-the-future-question-and-the-available-account}

Name the quantity, event or choice being predicted, the horizon and the inputs over that horizon. Specify the accuracy or decision boundary when it changes what information is needed. Predicting a total after one treatment cycle, determining whether it will be below a limit, and estimating a long-run average can require different information.

Recover the rule of change, observation meanings, sampling times and available initial information. Separate uncertainty about the state from uncertainty about the rule or future input. A longer observation history cannot replace an unspecified intervention.

State what the proposed description retains: present readings, model coordinates, past inputs and outputs, derived features or weights over possible states. Where future actions are chosen by a controller, retain the action assumptions needed by the comparison.

### A.3.3.PI:4.2 - Compare situations merged by the description {#compare-situations-merged-by-the-description}

Construct two admitted states or histories with the same retained description. Keep the rule, input conditions and future question fixed. Derive their relevant continuations. A difference in the requested result identifies information lost by that description.

For a deterministic discrete model, let x be its state, u its input, F(x,u) the next state and z = r(x) the retained description. An update z' = G(z,u) is well-defined when r(F(x,u)) has the same value for every admitted x having the same z, for each input covered by the claim. This condition says how to construct G: choose any compatible x, apply F and retain r of the result. All compatible choices must give the same answer. C.29.1 supplies the general comparison of operations under a representation change.

A prediction of one selected output at a fixed horizon may need less information than an update of the entire retained state. Compare the output that the question asks for. If the result will be used repeatedly, also determine how to update the information from which the next prediction is made.

For a probabilistic model, compare the distributions of the relevant future result under the merged states or histories. The current readout can conceal different next-event probabilities even when the full model is Markov, as :5.2 shows.

One divergent pair refutes sufficiency for a claim covering both cases. Matching a few pairs supports only those comparisons. A general sufficiency claim needs an argument or subject Method covering its stated class; a local counterexample or conditional forecast may already be enough for the present work.

### A.3.3.PI:4.3 - Choose the least costly useful repair {#choose-the-least-costly-useful-repair}

Use the missing distinction to choose a repair.

- **Retain additional state values.** Keep component amounts, velocity, operating mode, pending input or another variable whose difference changes the result. Include a way to obtain or estimate it in the intended use.
- **Retain relevant history.** Use observations and intervening actions to infer the missing state or construct a direct recurrence. Derive the needed history length from the rule and observation account where possible.
- **Retain an uncertainty account.** Carry the admitted state set or a distribution over possible states and propagate it through the rule. Use probability weights when a probability model is supplied.
- **Answer a weaker question that still serves the work.** A range, threshold decision or shorter-horizon result can be sufficient even when a unique future value remains unresolved.

Compare the available repairs by what they change in the decision and by their cost. C.11.DUA helps decide whether another measurement or calculation is worth obtaining. Use an already adequate bound directly.

A finite history can close some models, including the two-substance example. Other projections need a longer history, an approximate memory account or retained uncertainty. Choose the repair from the dynamics and the intended error, rather than assuming a fixed number of observations always reconstructs the state.

### A.3.3.PI:4.4 - Construct the prediction and its update {#construct-the-prediction-and-its-update}

For an algebraic reconstruction, solve the observation and change equations for the hidden values. Check the admitted domain and substitute the result back. Derive a recurrence if the next prediction will use a rolling history. Include how to discard old information and incorporate the next reading.

For a set of possible states, apply the change rule to that set under the admitted inputs, then use the observation relation to obtain possible outputs. A simpler enclosing interval can be enough for a threshold question. Keep the direction of the bound that makes the decision valid.

For a finite hidden-state probability model, let Pij be the probability of transition from state i to state j, and let pi be the current probability of state i given the observations and actions already used. First predict the next-state weights:

    predicted_pj = sum_i(pi * Pij)

When a new observation y arrives, multiply each predicted weight by the observation likelihood Lj(y), then divide by the sum of those products. For a discrete readout, Lj(y) is the probability of y in state j. For a continuous readout with a modeled density, use that density at y. Under the Markov and observation assumptions, the normalized weights summarize the history for the next prediction. Use the transition probabilities for the action actually taken when actions affect the model.

Supply the initial weights and observation likelihoods from the selected model. If the normalizing sum is zero, this update cannot supply posterior weights. Check the observation account, initial possibilities and numerical calculation before proceeding. The weights describe the current uncertainty about the modeled state.

For example, two equally weighted hidden states have Gaussian observation densities with means 0 and 1 and variance 1. An observation y=0 gives likelihoods proportional to 1 and exp(-1/2), so the first state's updated probability is 1/(1+exp(-1/2)), about 0.622. Using the probability of a single value would give zero for both continuous distributions and prevent this valid update.
A learned predictor offers another construction. Train or select it for the output, horizon, inputs and error that matter. A direct prediction several steps ahead and repeated application of an approximate one-step model can behave differently. Evaluate the intended use, including how the predictor receives the information available at each step.

### A.3.3.PI:4.5 - Test the horizon, error and changing conditions {#test-the-horizon-error-and-changing-conditions}

Work a case through to the requested future result. Include a pair merged by the simpler description when one motivated the repair. Identify which retained information now changes the calculation.

When readings are imperfect, propagate their stated uncertainty far enough to determine whether it changes the result. A reconstruction can amplify observation error even when the underlying equations have a unique solution. Parameter and input uncertainty require their own treatment; changing a sampling interval can change the update rule.

Check repeated use at its claimed horizon. A universally valid closed update can be iterated while its domain and input assumptions hold. A good fit over one observed step does not provide that result for an approximate predictor. Check the errors or bounds relevant to its use and shorten the horizon or change the account when needed.

Keep forecast performance and aggregate statistics tied to their questions. A model can reproduce a long-run average yet lose the history that changes the next-event probability. Conversely, a useful short-horizon predictor may not reproduce long-run behavior.

### A.3.3.PI:4.6 - Return the prediction with the information needed to reuse it {#return-the-prediction-with-the-information-needed-to-reuse-it}

Return the prediction, bound or unresolved distinction in the work where it is needed. Keep its observation meanings, inputs, horizon and consequential assumptions available in the calculation or explanation.

If additional information is worthwhile, identify the measurement, state distinction or model contribution that would change the answer. A result can be useful while the actual hidden state remains unknown. Reopen the affected comparison when the input policy, law, observation scheme or question changes, using B.5.MPC.R where several accounts must change together.

## A.3.3.PI:7 - Conformance Checklist {#conformance-checklist}

- @fact:CC-A3-3-PI-1 **CC-A3.3.PI-1 - Future question.** The output, event or decision, horizon and consequential input assumptions are recoverable. @status:spec/work
- @fact:CC-A3-3-PI-2 **CC-A3.3.PI-2 - Retained information.** The description identifies the state values, observations, history, features or weights used in the prediction. @status:spec/work
- @fact:CC-A3-3-PI-3 **CC-A3.3.PI-3 - Lost distinction.** The comparison keeps the rule and inputs fixed and identifies whether merged situations can change the requested result. @status:spec/work
- @fact:CC-A3-3-PI-4 **CC-A3.3.PI-4 - Usable construction.** The additional state, recurrence, uncertainty propagation or weaker answer supplies the claimed prediction or identifies what remains unresolved. @status:spec/work
- @fact:CC-A3-3-PI-5 **CC-A3.3.PI-5 - Probabilistic account.** A probability claim supplies the initial, transition and observation assumptions it uses. @status:spec/work
- @fact:CC-A3-3-PI-6 **CC-A3.3.PI-6 - Scope and error.** A sufficiency or performance claim is supported over its stated cases and horizon, with consequential observation and approximation error accounted for. @status:spec/work
- @fact:CC-A3-3-PI-7 **CC-A3.3.PI-7 - Repeated use.** Repeated prediction supplies an update of the retained information or a predictor covering the intended horizon. @status:spec/work
- @fact:CC-A3-3-PI-8 **CC-A3.3.PI-8 - Worthwhile return.** The result changes the calculation or decision; further information is sought when its expected contribution warrants the work. @status:spec/work

## A.3.3.PI:9 - Consequences {#consequences}

The reader can simplify a predictive account while preserving the relevant future distinction, recover missing information from history, or act using a useful bound. The construction also makes visible why a changed horizon, law or observation scheme can require a different description.

The result is relative to its supplied model, observations and use. More retained information can increase storage, estimation and computational cost, and reconstructed quantities can be sensitive to measurement error.

## A.3.3.PI:12 - Relations {#relations}

- **A.3.3 - U.Dynamics** distinguishes the state, transition and observation contributions used in this prediction.
- **A.3.3.CC** constructs compatible configurations; **A.3.3.TR** constructs the rule of change used to compare their continuations.
- **C.29.1** compares operations across mathematical representations; **C.29.2** constructs and judges computations at their intended use.
- **C.16** supplies the observation relation and consequential measurement uncertainty.
- **B.5.MPC** connects physical, mathematical and computational contributions; **B.5.MPC.R** revises them when the question changes.
- **C.11.DUA** selects additional information by what it can improve in the working decision.


## Dependencies {#dependencies}

- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/A-3-3#root, spec://ai.lev/fpf-spec/contract/A-3-3-CC#root, spec://ai.lev/fpf-spec/contract/A-3-3-TR#root, spec://ai.lev/fpf-spec/contract/C-16#root, spec://ai.lev/fpf-spec/contract/C-29-1#root, spec://ai.lev/fpf-spec/contract/B-5-FM#root, spec://ai.lev/fpf-spec/contract/B-5-MPC-R#root and spec://ai.lev/fpf-spec/contract/C-11-DUA#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-1-RI#root, spec://ai.lev/fpf-spec/contract/C-16-IR#root, spec://ai.lev/fpf-think-mmp/contract/MMP-8-SD#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/A-3-3-PI
