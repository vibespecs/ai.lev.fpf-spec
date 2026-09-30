# A.3.3.CC - Construct a Configuration Description under Constraints {#root}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method pattern
> **Status:** Draft
> **Normativity:** Normative

## A.3.3.CC:1 - Problem frame {#problem-frame}

Use this pattern when you need to describe how participants can be arranged, but choosing values for them separately admits combinations that the modeled situation excludes. A linkage joins its endpoints at a fixed distance; buffers share a fixed stock; a body must fit inside a container. The next calculation needs a description that preserves those connections.

**First useful move.** Name the participants, the question and one condition joining their values. For two buffers containing three jobs altogether, begin with “q1 and q2 are nonnegative integer job counts, and q1 + q2 = 3.” You can now recover the second count from the first and reject a proposed pair whose sum differs from three. Add buffer capacities when the question concerns which distributions fit.

The Method constructs an interpretable description of configurations: the retained arrangement or combination of participant values, expressed through variables and constraints. It can return an equation, a parametrization, a finite set or another usable representation. The arrangement being modeled and its description remain distinct. The examples assume elementary algebra and, for the linkage, the ordinary meaning of sine and cosine; the Solution explains the representation choices.

The practical gain is a basis for finding, comparing or rejecting configurations and for constructing a later model of change. If an available description already supplies the combinations and distinctions the question needs, use it directly. A prediction additionally needs the state information and law addressed by A.3.3.

## A.3.3.CC:2 - Problem {#problem}

Separate value ranges leave relations unstated. Each endpoint of a rigid link can have a position in a plane, yet most pairs of positions violate the link length. A software representation that permits every pair will include arrangements the intended physical model excludes.

A reduced description can fail in the opposite direction. One buffer count determines the other while total stock is fixed. After external arrivals become possible, keeping that same formula excludes distributions the new situation permits. Counts can also lose job order when the question changes from occupancy to which job is served next.

The construction must therefore retain the differences relevant to the question, express the constraints between them and provide a way to interpret the represented combinations. The choice of variables and the choice of constraints have to be made together.

## A.3.3.CC:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Few coordinates and visible relations | Eliminating a dependent coordinate can simplify calculation; retaining it can make a physical connection or consistency condition easier to understand. |
| Convenient notation and coverage | One parametrization may work locally while missing configurations or becoming singular elsewhere. |
| Compactness and retained distinctions | Counts or aggregate quantities are economical when they answer the question; identity, order or orientation can become consequential in another use. |
| Constraint fidelity and computational cost | Explicitly listing admissible combinations works for a small finite set; larger sets often need equations, predicates or a solver. |
| Present arrangement and possible change | A configuration can satisfy every positional constraint while a proposed motion violates the system's operation or velocity rules. |
| Model usefulness and subject knowledge | A coherent constraint account can support a conditional calculation; deciding whether it describes the actual system may require additional subject knowledge or measurement. |

## A.3.3.CC:4 - Solution {#solution}

Construct the description from the working question, then choose a representation in which the needed combinations can be expressed and used. If the calculation becomes inconvenient, reconsider the representation. If a premise changes, revisit the variables and constraints it affects.

### A.3.3.CC:4.1 - Select the participants and retained differences {#select-the-participants-and-retained-differences}

State what the reader must find: a fitting arrangement, a compatible assignment, a range of positions or the configurations to which a law will later apply. Identify the participants and the differences that can change this answer.

Give each variable a meaning and a value range. For a physical position, include the reference frame and unit needed to interpret it. For a relation, identify its participants: a distance needs the two endpoints; a job count needs the particular buffer. A.17 and A.18 supply the Characteristic and Scale vocabulary when the variables are declared as FPF characteristics.

Separate quantities held fixed in the present model from variables to be found. A link length may be a parameter in a rigid-body model and a changing quantity in an elastic model. The distinction follows the modeled use, so a later revision can change it.

Ask whether two arrangements described by the same values can require different answers to the current question. If they can, retain the missing distinction. For example, a pair of queue lengths suffices for occupancy but loses the order of differently treated jobs. State the needed order before attempting the receiving calculation.

### A.3.3.CC:4.2 - Express compatible combinations {#express-compatible-combinations}

Start with the product of the separate value sets. Write the conditions selecting the combinations admitted by the model. In a finite problem this may be a table of allowed tuples. In an algebraic description it may use equalities, inequalities or other predicates.

In A.19 terms, `CS = product_i ValueSet(Scale_i)` is the CharacteristicSpace. A constraint predicate `P` selects a subset `Q = {q in CS : P(q)}` used as the represented configuration set. A point in CS supplies a value for every selected slot; membership in Q additionally satisfies the constraints. The same method can be used in ordinary mathematical notation without creating a separate FPF record.

Explain what each condition represents. Fixed distance, conserved stock, nonpenetration and an imposed operating limit can all constrain the calculation, but changing each condition changes a different premise. Keep a condition imposed by the intended use recognizable so that revising a preference does not appear to alter a physical law.

When time or an external parameter changes which combinations are admitted, make that dependence recoverable, for example `Q(t; p)`. A moving wall changes a position constraint even before its interaction law is known.

Place restrictions on rates, operations or transitions with those relations. The car constraint in :5.4 limits instantaneous velocity; it leaves the corresponding configuration variables available. A.3.3 uses both kinds of restriction when constructing allowed continuations.

### A.3.3.CC:4.3 - Choose a representation that supports the operation {#choose-a-representation-that-supports-the-operation}

Compare the following forms using the operation the reader actually needs.

| Form | How to construct and use it | When it becomes inconvenient |
| --- | --- | --- |
| Variables with implicit constraints | Keep the participant values and equations or predicates between them. Test a proposed tuple by substitution. | Finding a satisfying tuple can require solving coupled conditions. |
| Parametrization | Choose parameters u and a reconstruction q = f(u) that satisfies the constraints. Perform the calculation in u and reconstruct the required participant values. | The chosen parameters may cover only part of the admitted set, repeat a configuration or become singular. |
| Explicit finite set | Generate candidate tuples, retain those satisfying the conditions and inspect or compare the resulting set. | The product of value sets can become too large to enumerate. |

For a parametrization, establish the coverage its use needs. If the task claims to represent every admitted configuration, explain how each can be obtained, possibly using several charts or cases. State when two parameter values represent the same configuration. A full turn of an angle repeats an orientation; treating its endpoints as unrelated can break a continuity calculation.

Keep redundant coordinates when they preserve useful structure or avoid a difficult elimination. If the task instead uses a local count of freely variable coordinates, establish independence and regularity of the active equality constraints before subtracting their number. A count alone supplies neither a parametrization nor its global coverage.

When replacing one representation with another, reconstruct the participant values and compare the receiving result. C.29.1 supplies a fuller transfer comparison when the replacement can change an operation or lose information. Group configurations as equivalent only when every member gives the same required answer and the required operations preserve that grouping. This mathematical construction is called a quotient. For an operation on the groups, check that choosing another member of the same group gives an equivalent result. Keep differently labeled endpoints distinct when exchanging them changes the answer.

### A.3.3.CC:4.4 - Obtain the configuration result the question needs {#obtain-the-configuration-result-the-question-needs}

Apply the description to the receiving question. If one fitting arrangement is enough, finding a satisfying tuple can finish the search. If the question asks for all arrangements, a range or impossibility, supply the corresponding enumeration, argument or solver result.

For a small finite product, generate a tuple, evaluate the conditions and retain it when they hold. A partial assignment can already be rejected when it violates a constraint whose participating values are known. Otherwise it may still have no satisfying completion: local checks leave the remaining constraints to be solved. For a large search, use a suitable constraint-solving Method; the explicit variables, domains and conditions provide its input.

For equations or inequalities, solve them to the extent needed and substitute the result into the retained relations. If numerical computation is used, interpret its tolerance against the modeled condition. A small residual has a different use from a proof of equality or an established margin from a collision boundary.

A configuration rejected by one condition identifies a concrete premise to inspect. An empty admissible set under the chosen premises is also useful: it can return the task to a size, capacity, connection or requirement decision. Failure of an incomplete search to find a tuple leaves the existence question open.

### A.3.3.CC:4.5 - Carry the result into use and revise it when needed {#carry-the-result-into-use-and-revise-it-when-needed}

Return the participant meanings, chosen variables, constraints and interpretation needed to use the result. Keep the representation as small as the receiving operation allows. The equations beside a design or the meanings attached to solver input may already carry everything needed; no additional report is required.

For a later prediction, recover the extra state information and transition rules under A.3.3. A linkage configuration may need velocities; an occupied-buffer configuration may need service or arrival information. An arrangement that fits now gives a starting point for planning, while reaching it from another arrangement needs an allowed-transition account.

When the question or premises change, revisit the affected part. A variable length replaces the fixed-length constraint; arrivals change a stock constraint; a job-order question needs more than counts. B.5.MPC.R coordinates a revision when that change also affects the physical interpretation, calculation or actual execution.

Recognition of the Method's result concerns whether the description expresses the selected configurations and supports the receiving operation. Reliance on its physical accuracy uses the subject premises and whatever calibration or uncertainty account that decision needs. C.11.DUA helps decide whether obtaining further information can change the action enough to justify its cost.

## A.3.3.CC:7 - Conformance Checklist {#conformance-checklist}

- Does the description name the arrangement question, participants and differences that can change its answer?
- Can the reader interpret each variable, its value range and any quantity held fixed?
- Do the constraints state which combinations are admitted and why those conditions apply to this model or use?
- If a parametrization or reduced description is used, does it cover the required cases and preserve the distinctions used in the answer?
- Can the receiving operation obtain its required tuple, set, range or conditional impossibility from the description? Is an unfinished search reported as unfinished?
- Are restrictions on configurations distinguished from any rate or transition conditions actually used?
- When the question changes, are newly relevant quantities, identities or order retained?
- Is support for physical reliance supplied to the extent that the particular decision needs, with further inquiry chosen by its possible effect on that decision?

## A.3.3.CC:9 - Consequences {#consequences}

The description makes compatibility usable: a solver can seek a fitting arrangement, a practitioner can locate the condition excluding one, and another participant can reconstruct the represented values. A later law of change starts from interpretable configurations.

Construction takes effort, particularly when constraints interact or a compact representation loses necessary detail. An implicit description may save modeling effort while making each computation harder; a parametrization reverses that trade-off. Reuse an adequate description until a changed operation, premise or required distinction defeats it.

## A.3.3.CC:12 - Relations {#relations}

- **A.3.3** connects configurations to state, transition rules, observation and the information required for prediction.
- **A.17, A.18 and A.19** supply characteristic meanings, value scales, the product space and predicates selecting admitted combinations.
- **B.5.FM** constructs a first model for a working question; this Method supplies its configuration construction when compatibility is the difficulty.
- **C.29 and C.29.1** connect the subject with a mathematical representation and compare transfer to another account.
- **C.29.2** constructs a computational formulation when obtaining the configuration result requires a nontrivial computation.
- **A.6.3.RT** makes the chosen notation usable under its interpretation scheme.
- **B.5.MPC and B.5.MPC.R** coordinate the joint physical, mathematical and computational answer and its revision.
- **C.16 and C.11.DUA** support a needed measurement relation and the decision whether additional information is worth obtaining.


## Dependencies {#dependencies}

- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/A-3-3#root, spec://ai.lev/fpf-spec/contract/A-17#root, spec://ai.lev/fpf-spec/contract/A-18#root, spec://ai.lev/fpf-spec/contract/A-19#root, spec://ai.lev/fpf-spec/contract/B-5-FM#root, spec://ai.lev/fpf-spec/contract/C-29-1#root, spec://ai.lev/fpf-spec/contract/C-29-2#root, spec://ai.lev/fpf-spec/contract/A-6-3-RT#root and spec://ai.lev/fpf-spec/contract/B-5-MPC#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-3-3-PI#root, spec://ai.lev/fpf-spec/contract/A-3-3-TR#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/A-3-3-CC
