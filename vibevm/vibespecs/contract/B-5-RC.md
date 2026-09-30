# B.5.RC - Recover a Construction from Its Description {#root}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method pattern
> **Status:** Draft
> **Normativity:** Normative unless marked informative

## B.5.RC:1 - Problem frame {#problem-frame}

Use this pattern when a description points to a result you need, but you cannot yet recover how to obtain it from what is available. You may be reading a mathematical construction, an assembly method or a way to transform data. The difficulty is in the connection between starting material, allowed operations and the required result.

Here, a **construction** is a way of obtaining an object by applying operations to given objects. In a mathematical construction, those operations form mathematical objects. In an assembly method, they may produce a design or a physical assembly; identify which result the description promises. The relevant practice supplies the operations and their application conditions.

**First useful move:** name the result needed for the next use, then find the operation that could produce it and what that operation requires. Follow those requirements back to available starting material. Work a small instance forward to recover the missing connection.

This method needs access to the description and enough subject knowledge to interpret its objects and rules. Use an adequate known construction directly. If the task is to invent a method where no usable account is available, use C.39 for that development; a missing operation discovered here can become its input.

## B.5.RC:2 - Problem {#problem}

A reader can recognize the name of a result and repeat its desired properties while remaining unable to construct it. The source may compress several operations into one verb, leave a prerequisite implicit or describe a property without giving a procedure that produces an instance.

Execution then fails at the first unprovided intermediate result. Guessing a plausible step can make the example work while changing the method being recovered. Repeating the requirement leaves the difficulty in place.

The useful result is a recovered construction that can be performed for the intended case, or a localized missing contribution that makes the next source return, specialist request or method-development move possible.

## B.5.RC:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Required result and available means | Working backward keeps the desired result in view; working forward reveals what the available operations can actually produce. |
| Source fidelity and useful invention | Filling a gap may solve the task, but the added operation then needs its own justification and must remain distinguishable from what the source supplied. |
| Properties and ways of obtaining an object | A property can guide construction or follow from it. The next use determines whether an existence result suffices or an instance must be obtained. |
| Shared prerequisites and execution order | Several steps may use the same object, and one step may need several results together. A simple list can hide either relation. |
| Small case and reusable method | A small case exposes missing operations cheaply; broader use depends on which conditions and operations survive the change of case. |

## B.5.RC:4 - Solution {#solution}

Recover the construction in two connected directions: from the required result toward its prerequisites, then from the available inputs toward a result. Keep the needed property in view throughout. The following actions form a useful working order; return to an earlier action when a missing condition changes the construction.

### B.5.RC:4.1 - Fix the result and starting situation {#fix-the-result-and-starting-situation}

Say what the next user needs to obtain and what they will do with it. Recover the conditions that distinguish a usable result: for example, a triangle on a supplied side, a display design that uses the supplied fittings, or data in the format required by a calculation.

Identify the starting objects and information already available. Distinguish an object supplied by the task from one the construction must produce. If a property alone answers the question, keep that smaller task. When an instance is needed, locate the operation that could obtain one.

Choose a small case that retains the troublesome dependency. A case that omits the unfamiliar operation cannot resolve how that operation works.

### B.5.RC:4.2 - Recover the operations {#recover-the-operations}

Read the description for ways of forming, transforming or combining the objects. For each operation needed by the case, recover:

- what it takes as input;
- the conditions under which it can be used;
- what it produces.

This information can appear in a definition, diagram, earlier construction or convention used by the source. A verb such as “combine” is enough only when its operation is already recoverable. Otherwise ask which parts are combined and how.

In a mathematical account, include the formation and equality rules that the construction uses. A rule for forming an object and a claim about its properties do different work: the first supplies an object for a later operation, while the second may justify applying that operation. Both can be needed.

Use the rules of the account being recovered. For a physical assembly, a joining operation may require compatible fittings and available components. For a mathematical expression, using one value at two places depends on the rules of that expression. Recover the relevant condition where the construction actually relies on it.

### B.5.RC:4.3 - Follow prerequisites backward {#follow-prerequisites-backward}

Start with an operation that produces the required result. Ask what must be available just before it can be applied. Repeat for any prerequisite not yet supplied.

Keep **joint prerequisites** together: drawing a segment between two points requires both points. Keep **alternative constructions** separate: either one complete construction or another may produce an acceptable result. Where several later steps use an intermediate object, retain that shared dependency instead of silently creating several unrelated objects.

Stop tracing a branch when it reaches an available input or an understood subconstruction whose starting inputs are available. The resulting dependency structure may have shared parts and alternatives. Draw it when that helps retain them; the structure does not have to be expressed as a graph.

If tracing returns to a result that it already requires, examine the source. It may describe an iterative construction with a starting value and stopping rule, a simultaneous problem with a separate solving method, or an omitted prerequisite. Recover that method or prerequisite before treating the circular description as executable steps.

A missing operation gives a focused question: “How is this intermediate object obtained under these conditions?” Return to the relevant source passage or specialist with that question. When you propose an operation yourself, treat it as a contribution to the construction and establish the conditions for using it.

### B.5.RC:4.4 - Work the small case forward {#work-the-small-case-forward}

Begin with the available inputs. Apply an operation when its prerequisites and conditions hold, retaining the output needed by later operations. At an unfamiliar transition, write, draw or perform enough of it to see what changes.

If the construction uses a notation you can read but cannot operate with, use A.6.3.RT to prepare a usable expression under its rules. If interpreting the notation itself remains the difficulty, obtain that missing preparation. A more legible expression helps only when it preserves the relation required by the operation.

Where an operation admits several outputs, select one that permits the intended continuation. If the source only guarantees that some suitable object exists, determine whether its account also provides a way to obtain the instance your next use needs.

Retain the difference between the construction being described and the particular trial. One successful trial can reveal the method and expose a gap. A claim about a whole class of inputs additionally needs the argument or other subject support appropriate to that claim.

### B.5.RC:4.5 - Establish the useful property and continue {#establish-the-useful-property-and-continue}

Recover why the constructed object has the property the next use requires. An auxiliary construction can make the argument possible; an established property can permit the next construction step. Use B.5.RA when the argument is present but its reasoning remains unclear.

The useful stopping point can be:

- the required object and a sufficient account of the property being used;
- a conditional construction whose unresolved condition matters to the next decision;
- an identified missing input or operation, with enough context to obtain it.

Select the support needed for that next use under C.11.DUA and the relevant subject method. A design calculation, mathematical proof and trial assembly answer different questions. If an existing result already supplies the needed support, use it.

An explanation to a collaborator should let them continue from the recovered result or address the localized gap. Use the working drawing, expression or conversation when it already carries that information.

## B.5.RC:7 - Conformance Checklist {#conformance-checklist}

For the construction being recovered:

1. The needed result and its next use are clear enough to select a useful small case.
2. Starting objects are distinguished from the intermediate objects to be produced.
3. Each operation needed by the case has recoverable inputs, application conditions and output.
4. Joint prerequisites, shared objects and alternative constructions retain their different effects.
5. The forward construction reaches a useful result or locates the input or operation that prevents it.
6. The property claimed of that result has the support its use requires; a broader claim retains its broader support question.
7. An invented addition is identifiable as an addition, and the next collaborator can use the result or act on the gap.

Apply these questions to the work already done. Write a separate account only when its recipient needs one.

## B.5.RC:9 - Consequences {#consequences}

The practitioner can turn a compressed account into an obtainable result and a meaningful division of further work. A specialist request can name the missing operation and its inputs rather than ask for a second explanation of the entire source.

Recovery may expose a gap in the source or in the reader's preparation. It also costs more than directly using a construction already understood. The stopping rule preserves that cheaper route and allows a useful conditional result.

## B.5.RC:12 - Relations {#relations}

- **B.5:** selects construction recovery as one contribution to inquiry and connects its result with further reasoning.
- **B.5.RA:** recovers the argument for a property that construction or later use needs.
- **B.5.MPC:** uses recovered constructions while connecting physical, mathematical and computational reasoning.
- **A.6.3.RT:** prepares a usable expression under a notation scheme when the representation obstructs an operation.
- **C.29.1 and C.29.2:** supply mathematical result transfer and computational formulation when those are the missing constructions.
- **C.39:** develops a missing way of working from the localized problem.
- **C.11.DUA:** selects the additional checking or information worth obtaining for the intended use.


## Dependencies {#dependencies}

- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/B-5#root and spec://ai.lev/fpf-spec/contract/B-5-RA#root for reasoning, spec://ai.lev/fpf-spec/contract/A-6-3-RT#root for expression, spec://ai.lev/fpf-spec/contract/C-29-1#root/spec://ai.lev/fpf-spec/contract/C-29-2#root for mathematical transfer and computational formulation, and spec://ai.lev/fpf-spec/contract/C-39#root for a missing method. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-15-10#root, spec://ai.lev/fpf-spec/contract/A-6-3-RT-OE#root, spec://ai.lev/fpf-spec/contract/B-5-RA#root, spec://ai.lev/fpf-spec/contract/B-5-RR#root, spec://ai.lev/fpf-spec/contract/B-5-TU#root, spec://ai.lev/fpf-spec/contract/C-16-MR#root, spec://ai.lev/fpf-spec/contract/C-36-RP#root, spec://ai.lev/fpf-spec/contract/C-39-RO#root, spec://ai.lev/fpf-spec/contract/C-40-CD#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/B-5-RC
