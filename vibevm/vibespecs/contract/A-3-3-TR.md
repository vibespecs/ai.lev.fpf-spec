# A.3.3.TR - Construct a Rule for State Change {#root}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method pattern
> **Status:** Draft
> **Normativity:** Normative

## A.3.3.TR:1 - Problem frame {#problem-frame}

Use this pattern when you can describe a situation's state but still need to work out how it can change. A connection limits two bodies' positions but leaves their acceleration to be determined. Each participant in a computation has a valid procedure, yet their interleaving can produce an unexpected result. A transformation preserves a mathematical property but can repeat forever.

**First useful move.** Choose one possible change and write which values it reads, which values it changes, what must hold for it to occur and which other values stay fixed during that step. For a participant that has saved a counter value r, its later write sets x' = r + 1. It need not produce x' = x + 1: another participant may have changed x since the read. This small rule exposes the lost-increment case in :5.1.

The Method constructs a rule relating states or describing their continuous evolution under stated inputs. “Allowed” means permitted by that model. The resulting rule can support a conditional calculation, reveal competing continuations or identify a missing interaction, operation or input. A.3.3 supplies the criteria for a U.Dynamics episteme and connects its state space, transition law and observation account.

The finite cases require ordinary arithmetic and conditions. The continuous case additionally uses derivatives and Newton's equation for a stated ideal mechanical model. Subject laws and operation semantics supply the content that the common construction combines.

If a suitable state-change rule already answers the question, apply it directly. When only compatible arrangements are needed, A.3.3.CC can supply that result before a rule of change is available. Use the present Method to construct or revise the rule, not as an extra reporting stage for every calculation.

## A.3.3.TR:2 - Problem {#problem}

A state constraint and a transition rule answer different questions. Two connected carts may have to maintain a fixed separation; that condition permits many common accelerations. Forces and masses are needed to select one. Similarly, saying that a participant reads before it writes constrains local order but leaves several global execution orders possible.

A rule assembled from separately plausible statements can also be inconsistent or too permissive. An omitted unchanged value may become free to vary. Combining alternatives as if they had to occur together can eliminate legitimate behavior. Treating a desired invariant as an automatic filter can hide the very failure the model was meant to investigate.

The practical problem is to construct a connected account from which the needed changes follow, while keeping visible the choices and missing information that still affect the answer.

## A.3.3.TR:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Observable change and hidden steps | A large modeled step is convenient; intermediate reads, interactions or events may change the result. |
| Local rules and joint behavior | Each participant can obey its own rule while their combination violates the intended whole result. |
| Simultaneous relations and execution order | Coupled equations constrain values together; a computation must choose how to obtain a solution. |
| Constraints and interaction laws | A constraint excludes combinations, but additional laws may be needed to determine rates or successors. |
| Possibility, progress and probability | A rule can allow a result without guaranteeing eventual arrival or assigning its likelihood. |
| Detail and useful return | A complete model may be costly; one counterexample, conditional continuation or identified missing rule can already change the decision. |

## A.3.3.TR:4 - Solution {#solution}

Construct the rule around the change that matters to the question. Recover the relevant subject operations or interactions, connect their effects and test the resulting continuation. Revise the state or step when that test reveals an omitted difference.

### A.3.3.TR:4.1 - Choose the state, step and inputs {#choose-the-state-step-and-inputs}

Name what changes and the observation or decision that depends on it. Recover the admitted states, using A.3.3.CC when their compatibility is still unresolved. Separate changing values, parameters held fixed and inputs supplied from outside the model.

Choose what counts as one step. A step can be one instruction, one transaction, an event, an observation interval or an interval of physical evolution. Say which intermediate effects the model retains. Declaring a read-and-write pair atomic is a substantive assumption about interference, as :5.1 shows.

Retain the values needed to apply the rule. A saved read and an instruction position can matter even when neither is visible in the final output. A mechanical law can require velocities as well as positions. If two cases described by the same retained values require different continuations under the same inputs, return to the state choice or retain the unresolved alternatives. A.3.3 supplies the prediction-sufficiency comparison.

For an interval of evolution, specify the inputs over that interval. One initial input value determines a later result only under an assumption such as a held input or a supplied input law. Distinguish that condition from the initial state.

### A.3.3.TR:4.2 - Write each contribution as a relation {#write-each-contribution-as-a-relation}

For a discrete action, write its enabling condition and its relation between the values before and after the action. A prime can mark an after-value: x is the counter before a write, and x' is its value after the write. State what remains unchanged when the action affects only part of the state.

An action may leave several after-values possible. Keep the relation broad enough to represent them. An expression x' = f(x,u) is appropriate when the supplied state and input u determine that after-value; a relation R(x,x',u) can retain several possibilities.

For continuous evolution, recover the subject laws relating quantities, rates and interactions. These may be written as differential equations, algebraic constraints and any event conditions needed by the model. Include the initial and boundary conditions that the selected law requires. With constrained bodies, identify the forces exchanged through their connection and combine the equations, as :5.2 demonstrates.

The form of an equation does not establish its physical applicability. Recover its domain meaning and conditions from the subject account. When that account is missing, name the missing relation and return the conditional result already obtainable.

### A.3.3.TR:4.3 - Combine jointly active relations and alternative actions {#combine-jointly-active-relations-and-alternative-actions}

Relations that must hold during the same modeled change are imposed together. For two coupled carts, both force equations and the fixed-separation condition hold together. The variables shared by those equations must keep the same meanings, reference frames and units.

Actions that provide alternative ways to take the next step are joined as alternatives. In the counter case, the next action can be an enabled read or write by either participant. Requiring every one of those actions in the same step would describe a different computation.

Check how participants interact through shared values. A local action's condition and effect refer to the global state at the selected step. If actions occur together, define their joint effect or derive it from the governing relations; textual order alone supplies neither simultaneity nor a conflict-resolution rule.

For equation-based modeling, keep the coupled relations available while choosing a computation. A solver's evaluation order is part of obtaining a solution. If the actual system has a communication delay, sequential update or other timing effect, represent that effect in the modeled rule. Modelica's instantaneous event semantics is one explicit modeling convention; it requires modeled delays when those delays matter.

A.22.CGUS can help expose alternative continuations and their conditions when that is the working question. The present construction supplies the rules used to judge those alternatives. The jointly applicable equations can also determine a single continuation.

#### A.3.3.TR:4.3.1 - Combine continuous evolution with events {#combine-continuous-evolution-with-events}

When the model mixes continuous evolution and discrete events, state the flow law in each mode, where that flow is permitted, each event's condition and timing, and its reset relation. A reset specifies which values change and which remain continuous.

For a condition that triggers an immediate event, evolve only to its first occurrence. Stop the continuous segment, apply the event relations, and resume from the resulting state under the applicable law. Process an already-enabled immediate event before advancing time. If the reset enables another immediate event, resolve that event according to the model before resuming flow. Incompatible event relations or an unresolved sequence of instantaneous changes are reasons to return a model or computation limitation.

An event that is merely permitted has a different timing rule: retain the allowed waiting and choice. Where simultaneous events can conflict, supply their joint relation or a justified priority. The thermostat in :5.4 uses mandatory immediate switching and a reset that preserves temperature.

### A.3.3.TR:4.4 - Derive a change and test the required property {#derive-a-change-and-test-the-required-property}

Work one case far enough to obtain a successor, a rate, a short behavior or an obstruction. Substitute the resulting values into the jointly required relations. In a finite model, enumerate or explore enabled actions from an admitted start; in a continuous model, derive or compute the behavior needed by the question.

To establish that a property P holds throughout reachable behavior, one sufficient induction argument proves two obligations: P holds at the admitted starts, and every permitted step from any admitted state satisfying P preserves P. For continuous evolution, use the corresponding invariance argument for the selected law and domain.

If preservation fails, seek a reachable path to the failing transition or strengthen the assertion using properties of reachable states. A transition from an unreachable state can defeat this proof without exhibiting a behavior that violates P. A stronger assertion I closes the proof when the admitted starts satisfy I, every permitted step from a state satisfying I preserves I, and I implies P. If neither argument is available, return the unproved obligation. Keep the transition rule being investigated intact while repairing the argument.

For states {0,1,2}, start 0 and transitions 0->0, 1->2 and 2->2, P defined as x<=1 holds throughout reachable behavior. The transition 1->2 defeats direct preservation of P, but 1 is unreachable. The stronger assertion x=0 is preserved and establishes P. A path from an admitted start to a violation would instead be a counterexample to the claimed property.

A small test can find a violation; a claim covering all allowed behavior needs an argument or method covering that behavior.

Keep the intended property separate from the rule being examined. If the model is intended to reveal whether an implementation can overflow a buffer, silently clipping its successors to capacity removes that failure from the model. Derive a control rule that prevents overflow, model what happens at overflow, or narrow the claimed operating conditions with a stated reason.

When no successor is found, determine what that result establishes. A contradictory set of equations, a terminal state, a disabled action, a deadlock and an unsuccessful incomplete search call for different next moves. Return the first missing condition or demonstrated obstruction that matters to the present use; do not invent a successor to fill the gap.

### A.3.3.TR:4.5 - Add selection, progress or probability only when needed {#add-selection-progress-or-probability-only-when-needed}

State what selects among remaining continuations: an input, a scheduler, a control choice, an unresolved environmental condition or a stochastic mechanism. If the current use needs only possibility or a counterexample, the alternative set may be sufficient.

For a progress question, supply the conditions needed to reach the intended result. An invariant can hold throughout an endless repetition. A decreasing nonnegative integer can establish termination for the Euclidean construction in :5.3; a concurrent protocol may instead require a scheduling or fairness condition. Describe what that condition demands of the participating system.

For a likelihood question, use a probability model over the relevant choices or behaviors. Counting alternatives alone gives a count. Different scheduler rules can assign different weights to the same six counter histories.

For a numerical calculation, name the approximation or update method used to obtain the model's consequence. Check the result at the resolution and accuracy the question needs. A numerical step can introduce behavior absent from the subject law; C.29.2 supplies the broader construction and comparison of computations.

### A.3.3.TR:4.6 - Return the usable rule or the missing contribution {#return-the-usable-rule-or-the-missing-contribution}

Return the rule with the state meanings, applicable inputs and conditions needed for its next use. Depending on the question, the first useful result can be a permitted continuation, an impossible transition, a counterexample, a sufficient bound or an identified missing law. Use that result in the calculation, design or explanation for which it was constructed.

If a changed question requires previously hidden steps, forces, state information or observations, reopen those contributions and retain the unaffected ones. B.5.MPC.R coordinates revision across the physical, mathematical and computational accounts. C.11.DUA helps decide whether resolving a remaining uncertainty can improve the choice enough to justify the work.

## A.3.3.TR:7 - Conformance Checklist {#conformance-checklist}

- @fact:CC-A3-3-TR-1 **CC-A3.3.TR-1 - Working change.** The subject, needed result and modeled step are recoverable. @status:spec/work
- @fact:CC-A3-3-TR-2 **CC-A3.3.TR-2 - State and inputs.** The rule retains the values it reads, separates held parameters and states input assumptions over the interval being modeled. @status:spec/work
- @fact:CC-A3-3-TR-3 **CC-A3.3.TR-3 - Connected effects.** Jointly required relations share their variable meanings; alternatives remain alternatives; unchanged values are stated where omission would permit unintended changes. @status:spec/work
- @fact:CC-A3-3-TR-4 **CC-A3.3.TR-4 - Subject contribution.** The physical interactions or operation semantics used by the rule are supplied, or their absence is the returned limitation. @status:spec/work
- @fact:CC-A3-3-TR-5 **CC-A3.3.TR-5 - Worked consequence.** An application obtains a continuation, rate, behavior, obstruction or missing contribution relevant to the question. @status:spec/work
- @fact:CC-A3-3-TR-6 **CC-A3.3.TR-6 - Required property.** A claimed invariant or progress property has the corresponding argument over the claimed cases. A failed induction step is distinguished from a reachable violation; testing and incomplete search retain their actual reach. @status:spec/work
- @fact:CC-A3-3-TR-7 **CC-A3.3.TR-7 - Choice and likelihood.** A selection, progress or probability claim has its own needed conditions. @status:spec/work
- @fact:CC-A3-3-TR-8 **CC-A3.3.TR-8 - Changed use.** A change to granularity, constraints, inputs or subject laws reopens the affected rule and its consequences. @status:spec/work

## A.3.3.TR:9 - Consequences {#consequences}

The reader can obtain a connected rule from local contributions, expose interference or missing interactions, and choose a useful return before constructing a larger model. The same construction makes assumptions about step size, inputs, alternative selection and progress available for revision.

The result's usefulness depends on the supplied subject account and the distinctions retained in the state. Extending the prediction horizon or changing what is observed can require more state information or a different approximation.

## A.3.3.TR:12 - Relations {#relations}

- **A.3.3 - U.Dynamics** identifies a supplied state-and-law account and compares retained information with the prediction being attempted.
- **A.3.3.CC** constructs the compatible configuration description from which state-change work can begin.
- **B.5.FM** constructs a first model for the working question; **B.5.MPC** connects the physical, mathematical and computational contributions.
- **B.5.MPC.R** revises the affected contributions when the question or conditions change.
- **A.22.CGUS** exposes alternatives and case conditions when continuation comparison is needed.
- **C.29.1** compares mathematical representations for the operations they preserve; **C.29.2** constructs the computation that obtains the needed result.
- **C.11.DUA** selects worthwhile additional information and support for the decision being made.


## Dependencies {#dependencies}

- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/A-3-3#root, spec://ai.lev/fpf-spec/contract/A-3-3-CC#root, spec://ai.lev/fpf-spec/contract/B-5-FM#root, spec://ai.lev/fpf-spec/contract/B-5-MPC#root, spec://ai.lev/fpf-spec/contract/B-5-MPC-R#root, spec://ai.lev/fpf-spec/contract/A-22-CGUS#root, spec://ai.lev/fpf-spec/contract/C-29-1#root, spec://ai.lev/fpf-spec/contract/C-29-2#root and spec://ai.lev/fpf-spec/contract/C-11-DUA#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-1-RI#root, spec://ai.lev/fpf-spec/contract/A-3-3-PI#root, spec://ai.lev/fpf-spec/contract/C-28-MR#root, spec://ai.lev/fpf-spec/contract/C-29-BB#root, spec://ai.lev/fpf-think-mmp/contract/MMP-11#root, spec://ai.lev/fpf-think-mmp/contract/MMP-18#root, spec://ai.lev/fpf-think-mmp/contract/MMP-8#root, spec://ai.lev/fpf-think-mmp/contract/MMP-9#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/A-3-3-TR
