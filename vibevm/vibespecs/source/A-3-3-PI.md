# A.3.3.PI - Retain the Information Needed for Prediction: depth {#depth}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## A.3.3.PI:5 - Archetypal Grounding {#archetypal-grounding}

### A.3.3.PI:5.1 - Recover a treatment forecast from component masses or a short history {#recover-a-treatment-forecast-from-component-masses-or-a-short}

Let a_n and b_n be nonnegative masses in kilograms after n treatment cycles. Each cycle leaves half of the first substance and a quarter of the second, with no new material:

    a_(n+1) = a_n/2
    b_(n+1) = b_n/4
    y_n = a_n + b_n

The instrument reports only y_n. States (a_0,b_0) = (1,0) and (0,1) both report y_0 = 1 kg but give next totals 1/2 kg and 1/4 kg. The aggregate has lost the composition needed for a unique next total.

One repair retains the two masses and updates them separately. Another uses two successive readings without measurement error. From y_0 = a_0 + b_0 and y_1 = a_0/2 + b_0/4,

    a_0 = 4*y_1 - y_0
    b_0 = 2*y_0 - 4*y_1
    y_2 = (3/4)*y_1 - (1/8)*y_0

The recovered masses must be nonnegative, requiring y_0/4 <= y_1 <= y_0/2. For y_0 = 1 kg and y_1 = 0.35 kg, the masses are 0.4 kg and 0.6 kg, and y_2 = 0.1375 kg.

The recurrence applies at later cycles under the same law. A rolling pair (previous total, current total) can replace the hidden component values for predicting future totals. On receiving a new total, retain it and the former current total. If no new measurement arrives, the recurrence can propagate the pair as a conditional model prediction.

With only y_0, nonnegativity yields the bound

    y_0/4^n <= y_n <= y_0/2^n, for integer n >= 0.

For y_0 = 1 kg, the next total is at most 0.5 kg. This settles a requirement at most 0.6 kg without learning the composition. A limit of 0.4 kg remains unresolved by that bound.

Now suppose the two readings each have absolute error at most epsilon kilograms while the retention law is fixed. The reconstructed a_0 can err by at most 5*epsilon, and b_0 by at most 6*epsilon. The formula for y_2 has error at most (7/8)*epsilon from those two reading errors: add the absolute contributions (3/4)*epsilon and (1/8)*epsilon. At epsilon = 0.01 kg this gives 0.00875 kg. A marginal threshold decision must account for that interval; a recovered negative mass calls for checking the measurement uncertainty and the model assumptions.

If both substances instead have the same fixed retention factor r, the total obeys y_(n+1) = r*y_n. Composition is then unnecessary for predicting totals under that law. The needed information changes with the operations and the question.

### A.3.3.PI:5.2 - Preserve predictive memory under a coarse readout {#preserve-predictive-memory-under-a-coarse-readout}

A modeled device has hidden states A, B and C, with fixed transition probabilities:

| Present state | Next A | Next B | Next C |
| --- | --- | --- | --- |
| A | 0.7 | 0.2 | 0.1 |
| B | 0.1 | 0.2 | 0.7 |
| C | 0.2 | 0.3 | 0.5 |

The readout is 0 in A or B and 1 in C. A current 0 leaves next-1 probabilities from 0.1 to 0.7, depending on the hidden state. A single value such as their unweighted mean would add an unsupported assumption about which state is present.

For this calculation, take the initial distribution to be the stationary distribution (19/54,13/54,22/54). After observing 1, the current state is C. Its next-state weights are (0.2,0.3,0.5). Observing 0 next removes C and gives current A/B weights (2/5,3/5). The probability of the following 1 is

    (2/5)*0.1 + (3/5)*0.7 = 23/50 = 0.46.

For the history 0,0, the first 0 gives weights (19/32,13/32,0). Apply the matrix, retain A and B after the next 0, and normalize. Their weights become (73/105,32/105), giving

    (73/105)*0.1 + (32/105)*0.7 = 99/350, about 0.283.

A decision that changes when next-1 probability exceeds 0.4 takes different actions after those histories. Keeping only the latest 0 with the stationary A/B mixture would give 11/32, about 0.344, and lose the relevant difference. The distribution conditioned on history is the useful retained information.

The same matrix also gives a long-run fraction of readout 1 equal to 22/54. This finite positive chain has the conditions for that ergodic average. The average answers an aggregate question; the conditional probabilities answer the next-event question.

Initial weights other than the stationary distribution can give different finite-history predictions. If only a current 0 is known and no mixture is justified, the range [0.1,0.7] remains available. A probabilistic estimate requires its initial and transition account.

### A.3.3.PI:5.3 - Distinguish a next output from an updatable state {#distinguish-a-next-output-from-an-updatable-state}

A processor emits and removes the head bit of a pending finite queue once per step. Two possible queues are (0,1) and (0,0). In both cases the next output is 0, so retaining the next bit answers the immediate output question.

After emitting that bit, the next outputs are respectively 1 and 0. The retained next bit cannot update itself without information about the remaining queue. To predict the next two outputs, retain both pending bits. To keep predicting after later steps and arrivals, retain the relevant queue and arrival account, or a summary proved adequate for the selected output question.

The difference is between knowing one output and carrying information that can be updated for further prediction. A description can be economical and sufficient for a short task. Increasing the horizon changes the information it must supply.

## A.3.3.PI:6 - Bias-Annotation {#bias-annotation}

The elementary cases use known change rules and small descriptions. A learned or partially known model can require a separate account of law uncertainty, data coverage and approximation error. A small hidden-state example makes probability updating easy to inspect; larger state spaces can require approximate filtering or bounds.

Observability and useful predictability can also diverge. Identifying every hidden quantity may be difficult while a required output remains tightly bounded. Choose the result from the working question and the information that can economically affect it.

## A.3.3.PI:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Failure | Why it matters | Repair |
| --- | --- | --- |
| Use an aggregate as a predictive state without comparing its merged cases | Components or hidden modes can produce different continuations. | Compare those cases and retain their relevant distinction or output range. |
| Substitute a long-run average for a history-conditioned forecast | A decision about the next event can depend on recent observations. | Condition on the available history or retain its predictive distribution. |
| Turn a recovered value into a measurement without carrying its assumptions | Algebraic reconstruction can amplify errors and depends on the supplied law. | Propagate the reading uncertainty and inspect the admitted domain. |
| Repeat a one-step predictor beyond its supported use | Prediction error can accumulate, or the retained output may lack its own update. | Construct an adequate state update or a predictor for the required horizon. |
| Keep a longer history without the intervening inputs | Similar observations can follow different actions and call for different forecasts. | Retain the actions that enter the transition account. |
| Obtain a full hidden-state estimate after a bound has settled the question | The extra work adds cost without changing the present choice. | Use the bound and reopen the distinction when another question needs it. |

## A.3.3.PI:10 - Architectural Rationale {#architectural-rationale}

The independently useful result is a description or uncertainty account that supports a prediction. Configuration construction determines compatible values; rule construction relates their changes. Prediction-information work asks which distinctions from those accounts must remain available for the future question.

That question is shared by physical measurement, mathematical reduction and computational state design. The common construction compares merged cases and repairs a consequential loss. Subject Methods supply physical laws, observability results, estimation techniques and efficient approximations.

A present model state, an observed value, a history and a distribution conditioned on observations carry different information. Keeping their roles explicit permits a compact predictor without claiming that its retained values identify every physical detail. A short-horizon output and an iteratively updated predictive state are also different useful results.

## A.3.3.PI:11 - SoTA-Echoing {#sota-echoing}

The working question is to obtain a useful future result from the available observations and change law. **Selected approach:** retain the distinctions needed by that result, together with their update or uncertainty. **Serious alternative:** reconstruct and carry the full model state. Full-state recovery supports a broader range of subsequent questions and is convenient when those values are already available. It can require extra measurement, estimation or storage when only an aggregate is observed.

Compare the alternatives for the same law, observations, inputs, horizon and decision, including the preparation needed to use each. In :5.1, a one-total upper bound already settles the 0.6 kg limit; reconstructing composition would require information that cannot improve that decision. For a unique forecast, two available totals support a rolling recurrence. In :5.2, a distribution over hidden states supports the history-dependent forecast without identifying the actual hidden state. That filter costs more than retaining the current readout alone, whose merged histories lose the decision-changing probability. These are chosen information and computation trade-offs, derived in the cases rather than measured as a general efficiency gain.

**Reduction and memory.** Lin and Lu's [Data-driven model reduction, Wiener projections, and the Koopman-Mori-Zwanzig formalism, §§2.1-2.3](https://arxiv.org/html/1908.07725v5) separates forecasting from long-time statistics and exposes memory after projection. **Adapt:** :4.1-:4.3 fix the output and horizon, compare merged states, and choose retained state, history or uncertainty. The projection identity needs a closure construction to become an economical predictor; the elementary mixture and its bounds in :5.1 are authored.

**Filtering a hidden state.** Poole and Mackworth's [Artificial Intelligence: Foundations of Computational Agents, third edition, §§9.6.2-9.6.3](https://artint.info/3e/html/ArtInt3e.Ch9.S6.html) derives filtering under Markov transition and observation assumptions. **Adopt:** :4.4 and :5.2 propagate state weights, incorporate the observation likelihood and normalize. [Section 9.1.1](https://artint.info/3e/html/ArtInt3e.Ch9.S1.html) distinguishes probability masses and densities; :4.4 keeps that distinction for discrete and continuous readouts. The resulting distribution summarizes the history for the supplied model. Learning the model or approximating a larger state space requires further Methods.

**Finite-chain forecasts and averages.** [Cambridge's Markov Chains notes, §§9-10](https://www.statslab.cam.ac.uk/~rrw1/markov/M.pdf) distinguish distribution convergence and ergodic averages. **Adopt:** :4.5 and :5.2 preserve their different questions. The three-state matrix, histories and threshold comparison are authored. Stationary initial weights are used only where stated; the positive finite chain supports the illustrated long-run average.

**Prediction at the intended horizon.** De Jong, Breschi, Schoukens and Lazar's [Koopman Data-Driven Predictive Control with Robust Stability and Recursive Feasibility Guarantees](https://arxiv.org/html/2405.01292v1) constructs multi-step predictors from past inputs and outputs and addresses errors from iterated approximate one-step dynamics. **Adapt:** :4.4-:4.5 compare the predictor at its intended horizon and input policy. The paper's controller guarantees require its specialized construction; the present Method adopts the comparison question, not those guarantees for every predictor.

The common procedure is a conceptual synthesis. Reopen its comparative choice when another description or estimator answers the same question under the same available observations, reader preparation and acceptable error at lower cost, or when a changed law, input policy or consequential prediction failure exposes a distinction it lost. Delay reconstruction, observability, filtering, system identification and model reduction then supply concrete alternative constructions.


## A.3.3.PI:End {#end}
