# E.10.INT - Recovering What Interest or Curiosity Means Here: depth {#depth}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## E.10.INT:5 - Archetypal Grounding {#archetypal-grounding}

### E.10.INT:5.1 - An informative controller query {#an-informative-controller-query}

A controller must choose an input that gives output 5. It has two equally plausible candidate relations, `y=x` and `y=-x`, and can first query input 0 or input 1. “Choose the more surprising query” leaves the criterion unclear.

At input 0 both candidates return 0. At input 1 they return 1 and -1 respectively. The second query distinguishes the candidates: after observing 1, command 5; after observing -1, command -5. The recovered instruction is “query input 1 to distinguish the relations, then choose the command.”

A separate fair coin produces an outcome with one bit of surprisal, but its outcome is independent of which relation holds. Querying input 1 yields one bit of information about that relation under the stated equal prior. Tossing the coin yields none. If the controller is already given the relation, it can select the command immediately.

The example constructs an information-seeking policy. Whether a particular controller can execute it is a further capability question.

### E.10.INT:5.2 - Progress and a stepping stone {#progress-and-a-stepping-stone}

In a constructed example, a compressor learns a dictionary entry for a repeated substring in a fixed data block. Its total lossless description of that block, counting the dictionary and encoded data under the same convention, falls from 100 bits before the update to 80 afterwards. “The second version is more interesting” can now be recovered as “this dictionary update reduced the total description by 20 bits for this block.” If the team is choosing more training, it considers the likely further improvement and the work required.

Another construction may deserve attention even though that measure has not improved. In Stanley and Lehman's Picbreeder example, a participant retained and developed an image resembling an alien face; a car-like image appeared through later changes. The first participant could act on the available image and its variation possibilities before knowing that destination. The practical result of this recovery is to retain the construction and its means of variation for exploration. C.18 governs an archive used for that purpose.

These cases permit different choices: improving a known performance measure and preserving a possible starting point for new work.

### E.10.INT:5.3 - Choosing an interesting rhythm {#choosing-an-interesting-rhythm}

A workshop needs music for listeners who are familiar with 4/4 and are beginning to work with 7/8. “Choose moderately complex rhythms; they are the most interesting” hides both the response sought and the listeners' preparation.

Recover the request as “choose material that helps these listeners maintain the beat and want to move while encountering 7/8.” The facilitator can start from simpler 7/8 material and adjust from the listeners' response. If the purpose is instead to exercise a skilled drummer's coordination, that practice question needs its own choice of material.

This distinction is supported by Spiech and colleagues' study: Western listeners' groove ratings peaked at moderate complexity in 4/4, while simpler rhythms received the highest ratings in the less common meters tested. Here *groove* means the pleasurable urge to move. The study supports adapting the comparison to listener and meter; the workshop's teaching method supplies the exercise.

## E.10.INT:6 - Bias-Annotation {#bias-annotation}

The source traditions model different aspects of agency. A person's felt curiosity, an AI policy's objective and a collective's exploration practice call for different accounts of how the effect occurs. Use the shared recovery procedure to keep those subjects visible while comparing their contributions.

Rhythm examples also depend on musical experience. A result for Western listeners and selected meters provides a qualified starting point for that use; another musical practice may support another comparison.

## E.10.INT:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Misuse | Why it changes the work | Repair |
|---|---|---|
| Rewarding unpredictable observations as if they resolved uncertainty | A random source can consume the query budget while leaving the relevant hypotheses unchanged. | Identify which observation updates beliefs about the question being investigated. |
| Requiring a stepping stone to justify a distant objective | The eventual use may become visible only after the construction is varied or combined with another. | Judge the available exploration or retention opportunity from its present basis. |
| Applying “moderate complexity” across agents and tasks | The learner's available methods or the listener's familiar structure can change which material is usable. | Recover the varying characteristic and the agent-relative comparison. |
| Treating one participant's interest as the project's entire choice rule | Other participants can bear different consequences. | State the affected stakes before the applicable decision method compares options. |

## E.10.INT:10 - Architectural Rationale {#architectural-rationale}

The common operation is to recover the relation hidden by a familiar expression. A single engagement score would lose the distinction between a participant's response, a model's progress and a construction's further uses. Conversely, treating these meanings in isolation would miss how one project coordinates them.

The procedure therefore identifies the participant and contribution first, and adds models or measurements only for the question that needs them. This also lets a promising new method be pursued from available clues while later uses are still being discovered.

## E.10.INT:11 - SoTA-Echoing {#sota-echoing}

**Learning progress.** Schmidhuber's historical [formal theory of creativity and intrinsic motivation](https://people.idsia.ch/~juergen/ieeecreative.pdf) distinguishes improvement of a predictor or compressor from the unpredictability of its input. Adopt that comparison for progress claims in §4.2. The competing shortcut, fixed-model surprise, can reward an unlearnable signal; §5.1 makes the related information-seeking error actionable.

**Information-seeking policies.** [Paprika](https://arxiv.org/html/2502.17543v3) describes strategic information gathering for task completion without an intrinsic-motivation reward. Its training curriculum uses a coefficient-of-variation heuristic for sampling tasks. Adapt the policy distinction in §4.1; keep that sampling heuristic separate from a measurement of acquired capability.

**Active inference.** [Friston et al. (2017), §2](https://activeinference.github.io/papers/process_theory.pdf), supplies the historical coupling of epistemic and pragmatic value. Their [2025 technical note](https://arxiv.org/abs/2512.21129) extends information-seeking to distinctions among model structures. Adapt those contributions in §4.2: recover the model, expected information and preferences behind the action. This supplies a richer continuation than explaining all exploration as aversion to an unexpected observation; the selected formal account still determines its assumptions.

**Open-ended search.** Stanley and Lehman's [Why Greatness Cannot Be Planned](https://doi.org/10.1007/978-3-319-15524-1), Chapters 5 and 9, gives the historical argument for judging available stepping stones without requiring their final destination. [Enhanced POET](https://proceedings.mlr.press/v119/wang20l.html), §§2-3, combines a population-relative difficulty screen with novelty and transfer. Adopt the distinction between an attainable learning opportunity and retained possibilities in §§4.1-4.3. A progress-only selector can lose the latter; the particular search method must supply its generation, retention and resource rules.

**Agent-relative challenge.** [Oudeyer's 2026 preprint review](https://pyoudeyer.com/Curiosity-Review-OudeyerMarch26.pdf) compares curiosity processes across timescales and examines conditions for an intermediate-knowledge preference. Adapt this conditional treatment of the Goldilocks region. It improves on an agent-independent midpoint rule by retaining the learner, environment and changing knowledge.

**Rhythmic interest.** Toussaint's *The Geometry of Musical Rhythm*, second edition, Chapter 41 and Epilogue, develops an account using several rhythmic properties and their combinations. [Spiech et al. (2025)](https://www.nature.com/articles/s44271-025-00360-0) compare groove ratings across complexity and meter in three behavioral experiments. Adapt their listener-and-meter distinction in §5.3. It provides a more useful selection basis than a universal complexity optimum, while leaving rhythm construction and teaching to their field methods.

Reconsider these comparisons when a source provides a better account of the particular contribution, changes the conditions under which a signal works, or enables the same action with less inference or measurement.


## E.10.INT:End {#end}
