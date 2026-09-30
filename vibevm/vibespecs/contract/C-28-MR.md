# C.28.MR - Derive an Intervention Consequence by Mechanism Replacement {#root}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method pattern
> **Status:** Draft
> **Normativity:** Normative

## C.28.MR:1 - Problem frame {#problem-frame}

Use this pattern when a causal model is available and the working question asks what follows if a mechanism is replaced: a controller uses a different rule, a variable is held at a chosen value, or an action occurs at a specified event. The model may be small enough to calculate by hand.

The subject is the intervention query in that model. The Method constructs the modified model and derives the requested value, distribution, contrast or bound under its assumptions. The practitioner needs the subject meaning of the variables and enough mathematical or computational help to solve the relevant equations.

**First useful move.** Point to the equation that represents the proposed change. Replace that equation and re-evaluate the variables needed for the question. If a display merely reports voltage, changing its displayed number leaves the supply equation in place. Changing the supply command instead changes the voltage and the current through the retained load equation.

Use an adequate existing derivation directly. Observational reporting can finish without this transformation. If only an observed joint distribution is available, recover a causal-model assumption or an identification result through C.28 before claiming a particular intervention consequence. Identifying an effect from data is a separate task from deriving it in a supplied model.

## C.28.MR:2 - Problem {#problem}

An observed value tells us something about how the existing mechanisms operated. An intervention changes a mechanism. Conditioning on the observed value can therefore answer a different question from imposing that value.

A second difficulty appears when a mathematical or software operation has an unclear physical interpretation. Assigning a value to an indicator, replacing a controller and forcing a physical quantity can change different mechanisms. Reusing the same variable name hides that difference.

Even a clearly specified replacement can change the solvability of a model or its subsequent dynamics. The useful result requires both the model transformation and a derivation for the question actually asked.

## C.28.MR:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Local change and propagated effects | One equation changes directly; other variables may change through their retained mechanisms. |
| Mathematical construction and physical interpretation | A replacement can be well-defined mathematically while the proposed action affects additional mechanisms. |
| Compact models and time | An equilibrium or one-step account can answer one query while omitting the transient or feedback needed by another. |
| Shared conditions and random variation | A comparison needs its intended population and input dependence, including common causes. |
| Definite answers and affordable work | A requested comparison may be determined before every state or parameter is resolved. |

## C.28.MR:4 - Solution {#solution}

**Choose the intervention and question → recover the mechanisms and input law → replace the selected mechanisms → solve the affected relations → obtain the requested consequence → return its interpretation and useful limit.**

These moves form a derivation. A few equations can carry the complete small result.

### C.28.MR:4.1 - Specify what is changed and what is asked {#specify-what-is-changed-and-what-is-asked}

Name the modeled variable or mechanism, the proposed replacement and the result needed for use. Include the time or horizon when it changes the question. “Set the alarm to zero now” and “keep its output at zero for the next hour” describe different interventions in a model with later feedback.

For a constant intervention, use `do(X=x)` to mean replacing the equation for X by the constant x. For a changed rule, state that rule and the information it may use: for example, a controller's command as a function of the readings available before the command. C.28:4.10 distinguishes the relevant action-policy families when that choice matters.

Specify a comparison only when one is wanted. A value under one intervention, a difference between two interventions and a difference from natural behavior have different required inputs. A question about the same historical case under another action also needs the factual observations and the resulting information about that case's underlying inputs. Infer those inputs using the factual mechanisms and observing procedure before replacing the mechanism. Carry the inferred distribution or compatible possibilities into the alternative calculation, preserving the dependence that makes it the same modeled case. C.28 governs what supports that counterfactual use; a population intervention average can answer a different question.

### C.28.MR:4.2 - Recover the model that gives the replacement meaning {#recover-the-model-that-gives-the-replacement-meaning}

Write or recover each relevant mechanism in a form such as `X_i = f_i(parents, U)`. The function tells how the modeled quantity is determined by other modeled quantities and by U, the inputs left outside these mechanisms. Recover their domains and the joint distribution of U, or their given values for a deterministic calculation.

Keep the subject interpretation with the equations. An equation's left-hand side is selected by the causal account. Algebraically rearranging `I=V/R` to `V=IR` preserves the equality but does not decide which physical component an intervention replaces. In :5.2 the supply controls V and the resistor relates V to I.

Preserve common inputs and their dependence. If two disturbances arise from one shared event, retain that event or their joint law when calculating both effects. A simulation must generate one compatible joint input for a case; independent resampling of its components would change the model.

Recover only the mechanisms needed to determine the queried consequence and their relevant conditions. A missing actuator relation may prevent a physical consequence while still allowing a useful comparison inside an explicitly assumed model. State that assumption where the result uses it.

### C.28.MR:4.3 - Construct the modified model {#construct-the-modified-model}

Replace each targeted mechanism by its stated constant or function. Retain the other mechanism functions and the supplied input law. Then let their output values follow from the new inputs to those functions.

For a randomized replacement, give its randomization law and its dependence on existing inputs. An independent randomizer is one possible specification. If the proposed change also alters the environment or population, include that change in the compared model instead of silently treating it as part of a constant intervention.

Keep a replacement's scope visible in time. In a discrete-time model, identify the affected update steps. In an event-driven model, identify the triggering condition and the state change it initiates. A.3.3.TR helps construct the relevant continuation rule from interactions, events and subject laws when that rule is missing.

At the physical interpretation, ask whether the proposed action also changes another modeled mechanism. Changing a supply command and attaching a device that forces its output can have different consequences for current limits and other connections. Add the relevant effects before using the modified model to answer that physical question.

### C.28.MR:4.4 - Solve what the intervention query requires {#solve-what-the-intervention-query-requires}

For an acyclic model, evaluate the retained and replaced functions in dependency order. For a time-stepped model, propagate from its initial conditions through the selected horizon. For simultaneous equations or continuous dynamics, use the solution method and conditions appropriate to those relations.

Check the transformed relations themselves when a replacement can change existence or select among several solutions. A solver's first returned branch may leave other admitted answers. If all admitted solutions agree on the queried quantity, that agreement can answer the question. If their answers differ, retain the possible answers, derive a useful bound, or expose the condition needed to choose among them. If the model has no relevant solution for inputs the query includes, return that obstruction and repair the model or question.

For probabilistic results, the selected solutions must define the requested random quantity under the input law. Existence of one numerical trace supplies less than a uniquely determined distribution. A general proof is unnecessary when a direct finite calculation settles the present query.

For a dynamically triggered jump, recover the event-order or flow/jump choice if it changes the result. A model's steady-state solution alone does not determine what happens during a transient. The hybrid-system approach discussed in :11 supplies one current treatment with explicit conditions; the subject model still determines which treatment is appropriate.

### C.28.MR:4.5 - Calculate the consequence under the retained conditions {#calculate-the-consequence-under-the-retained-conditions}

Let `Y_g(u)` be the queried output obtained with replacement g and input u. For a finite input population with probabilities `p(u)`, its mean is

`E[Y_g] = sum_u p(u) Y_g(u).`

Use the corresponding integral for a continuous input law when it exists. For a contrast between g and h in the same population, evaluate both under that population's law. A paired simulation can reuse each joint input u for both computations. Preserve the dependence of inputs within each computation.

A symbolic expression, an inequality or a bound can be sufficient. Numerical precision should serve the receiving choice or explanation. If an estimate is required, distinguish its computational or sampling error from uncertainty about the causal model and its parameters.

### C.28.MR:4.6 - Return the result and reopen only what changes it {#return-the-result-and-reopen-only-what-changes-it}

Return the consequence together with the replacement, model assumptions and comparison or horizon needed to interpret it. The equations and answer already produced may suffice. Use C.28's reusable support form only when another use needs a referenced conclusion.

Keep the mathematical result conditional on the supplied causal account. When the receiving question concerns an actual device or organization, connect the proposed action to the modeled replacement and ask which unmodeled interaction could change this result. Obtain further evidence only when that unresolved question can change the use. B.5.MPC connects the physical account, mathematical construction, computation and observation when this passage needs work.

When a parameter, intervention scope or mechanism changes, revisit the dependent derivation. Preserve unaffected relations and calculations. A changed event time can require another continuation; a changed source of disturbance can require another joint input law. Stop when the requested result or a useful supported limit is available.

## C.28.MR:7 - Conformance Checklist {#conformance-checklist}

- The intervention and queried consequence identify the same modeled subject, population and relevant time.
- The replaced equation or rule is recoverable, including any inputs used by a policy or randomizer.
- Other mechanisms remain in force; their values are recomputed where the replacement affects them.
- The joint input law and common causes needed by the query survive the computation.
- The transformed model determines the reported answer, or the result retains the relevant alternatives, bound or obstruction.
- A comparison uses the required baseline and conditions; an intervention outcome alone is not reported as an estimated change.
- The result's physical use connects the actual action to the modeled replacement and any consequential additional effect.
- The amount of calculation, recording and new evidence serves the receiving question.

## C.28.MR:9 - Consequences {#consequences}

The practitioner obtains a reproducible model-based consequence and can locate which proposed change produces it. This supports comparisons of control rules, experimental proposals and organizational mechanisms under their stated assumptions.

The method also exposes useful partial results. A fixed intervention outcome may be available when a baseline contrast is not. A bound may already separate two choices. These results preserve progress without requiring a complete empirical programme.

The main effort lies in recovering the mechanisms and conditions needed to answer the query. More elaborate equations can increase solving cost while leaving a decisive omitted interaction untouched. A small model is preferable when it already resolves the receiving question under adequate assumptions.

## C.28.MR:12 - Relations {#relations}

- **C.28** recovers the causal-use question, distinguishes intervention and counterfactual reliance, and combines the support results needed by a receiving use. This member supplies the derivation inside a given model.
- **C.28:4.10** distinguishes action-policy regimes when the replacement's available information changes the causal question.
- **A.3.3.TR** constructs continuation rules from interactions, operations and subject laws when time or events matter to the replacement.
- **B.5.MPC** connects the physical account, mathematical construction, computation and observation used to interpret the consequence.
- **B.5.RR** revises the affected reasoning when a premise or mechanism changes.
- **C.29.1** checks transfer of a mathematical result into another representation or use; the current member constructs the intervention result that can later be transferred.


## Dependencies {#dependencies}

- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/C-28#root, spec://ai.lev/fpf-spec/contract/A-3-3-TR#root, spec://ai.lev/fpf-spec/contract/B-5-MPC#root, spec://ai.lev/fpf-spec/contract/B-5-RR#root and spec://ai.lev/fpf-spec/contract/C-29-1#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/C-28-CM#root, spec://ai.lev/fpf-think-mmp/contract/MMP-11#root, spec://ai.lev/fpf-think-mmp/contract/MMP-15#root, spec://ai.lev/fpf-think-mmp/contract/MMP-19#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/C-28-MR
