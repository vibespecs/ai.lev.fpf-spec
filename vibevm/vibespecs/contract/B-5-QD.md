# B.5.QD - Develop a New Question from a Result or Construction {#root}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method-description pattern
> **Status:** Draft
> **Normativity:** Normative unless marked informative

## B.5.QD:1 - Problem frame {#problem-frame}

**Use this when** a result, counterexample or newly available construction changes what you could usefully investigate, but the next question is still unclear. A failed conjecture may reveal a missing condition. A successful calculation may supply an operation that makes a previously impractical question approachable. The work is to turn that change into a question you can begin to answer.

**First useful move.** Recover the step at which the earlier reasoning failed, or the operation that has become available. Ask what it now lets you distinguish, construct, explain or change. For example, a triangle refutes the claim that every connected graph can be divided into two groups with every edge crossing between groups. It also suggests asking for a construction that returns either the division or an obstruction.

The result is a question with an understood answer form, a useful first attempt and a reason to pursue or retain it. The answer may support further theory, a different investigation or an action in the world. Developing a concept or a reusable operation can be that contribution even before its eventual applications are known.

Use an already adequate question directly. If the question is clear and the missing contribution is a way to answer it, C.39 supplies that search. This pattern is useful when the result sought or the question's conditions themselves need to be developed.

## B.5.QD:2 - Problem {#problem}

“Find the next interesting problem” leaves the crucial work undone. Many variations merely change a number or a name. Others repeat a failed claim with a convenient exception, ask for information the available description cannot determine, or generate questions whose answers would add nothing to the inquiry.

A useful next question grows from a consequential change: an exposed dependency, a new object or operation, a newly distinguished case, or a result that can be used elsewhere. The difficulty is to construct that question while preserving what the earlier work established and keeping a feasible point of entry.

## B.5.QD:3 - Forces {#forces}

| Force | Working tension |
|---|---|
| Continuity and novelty | Earlier reasoning supplies operations worth retaining; its original question can also hide the next useful distinction. |
| Refutation and recovery | A counterexample can invalidate a broad claim while leaving much of its construction available. |
| Reach and tractability | A question can open a valuable field while its first attack must fit the contributors and means available. |
| Exploration and present use | Some contributions have an immediate application; others make new questions or operations possible. |
| Variety and attention | Several alternatives can reveal a better question, while indiscriminate generation consumes the effort needed to work one. |

## B.5.QD:4 - Solution {#solution}

**Recover what changed → locate the dependency or new operation → construct a consequential question → work a revealing case → choose the next inquiry and keep what remains useful.**

Enter with the result that actually changed the inquiry. Reuse a known formulation or derivation when it already supplies the needed step. Return to an earlier step if an attempted answer reveals that the question is ambiguous, underdetermined or more expensive than its use warrants.

### B.5.QD:4.1 - Recover the contribution of the earlier work {#recover-the-contribution-of-the-earlier-work}

State the earlier question and what the work actually obtained. Identify the part that matters now: a counterexample, an unresolved inference, a constructed object, a computational operation or a distinction the earlier description omitted.

For a failure, locate its scope. A counterexample to a lemma can expose a defect in one argument while leaving the main conjecture undecided. A counterexample satisfying the main conjecture's premises refutes that conjecture. A program's failure on a case may instead concern its implementation. Recover the relevant reasoning under B.5.RA or B.5.RR when this difference is unclear.

For a success, recover what can now be done with the result. Explain its inputs, output and application conditions. A computation that produces cumulative totals, for example, may provide a way to answer many interval questions. Its reusable contribution is the relation between those totals and the intervals.

Keep independently supported results available. They can supply the construction, limiting case or partial answer for the next question.

### B.5.QD:4.2 - Find the relation that can change the question {#find-the-relation-that-can-change-the-question}

Follow the earlier result back to a consequential dependency, or forward to an operation it enables.

If a description gives the same information for cases that need different answers, construct two such cases. Their difference identifies information a stronger question may need. If an inference depends on an unproved step, state the missing step as a possible question. If an operation succeeds, ask which other inputs, outputs or combinations preserve its useful relation.

Use variations that have a reason in the work. The following are common ways to construct them.

| What the work reveals | How to form the next question |
|---|---|
| A counterexample identifies a failed condition. | Ask which condition would support the needed conclusion, or which construction identifies the cases where it fails. |
| A successful construction produces more information than the first answer used. | Ask what further result can be obtained from that information and by which operation. |
| Different cases collapse to one description. | Ask what additional distinction determines the answer, or what bound remains possible without it. |
| An argument needs an unavailable intermediate result. | Ask for a lemma, witness or construction that supplies that step; state how it would be used. |
| A familiar operation becomes available in another setting. | Ask whether its required relations hold there and what receiving task it can now serve. |

A variation can change the original task. Preserve that change explicitly: restricting a claim to trees may give a valid result while leaving the original request about all graphs unanswered. If the broader request still matters, keep it as an unresolved question.

These variations can be combined or repeated. Their purpose is to expose a useful answer, not to fill a catalogue of question types.

When requirements appear incompatible, B.5.QD.CF recovers the premises producing the conflict and asks what other construction could satisfy the retained need. It distinguishes changing an assumed means or representation from changing a requirement, and can return a useful impossibility when the conditions must remain.

### B.5.QD:4.3 - Give the new question an answer form {#give-the-new-question-an-answer-form}

Say what would answer the question: for example, a construction, an explanatory relation, a bound, a counterexample or a condition under which an operation works. State the objects, allowed changes and premises that can alter the answer.

Connect that answer to its possible use. “Find a partition” and “return a partition or an odd-cycle witness” make different contributions: the second also explains failure. “Predict the position” and “bound the reachable positions” may serve the same present decision at different effort.

Separate a proposed answer from the question. “Does this procedure always terminate on finite inputs?” remains a useful question when the proposed positive answer is false. The failing case can open the question of a termination condition or another procedure.

If a question combines several missing contributions, make the dependency visible. For a physical calculation, you may first need a model that determines a quantity, then a computation of that model, then an interpretation for action. B.5.MPC coordinates those contributions. Name the first unresolved connection so a person, AI agent or group can work on it using the available subject knowledge and tools.

### B.5.QD:4.4 - Work a case that reveals the difficulty {#work-a-case-that-reveals-the-difficulty}

Choose a small case that exercises the changed condition or new operation. Attempt the requested construction or inference and explain where it succeeds or stops.

Use the result to improve the question. A successful case can expose a reusable relation. A failed case can identify a missing premise, an incompatible demand or an operation still to be developed. If two admissible cases give different answers from the same supplied information, ask for the missing distinction or a result valid for both.

A case establishes its own result. A broader mathematical claim needs its derivation, and applying a physical model needs the relevant physical basis. The question can already be useful before those answers are established: the first attempt should make the next contribution more identifiable.

Begin with available reasoning and information. Obtain further evidence only when its possible answers can change the useful inquiry enough to justify the effort under C.11.DUA. An existing bound or conditional answer may settle the current use.

### B.5.QD:4.5 - Choose an attainable inquiry {#choose-an-attainable-inquiry}

Compare the few questions that remain serious candidates. Ask what each answer would enable and where work could begin with the available capabilities, collaborators and resources. Include the cost of learning or obtaining a missing operation when it affects the choice.

A worthwhile first question may be narrower than the eventual aim: establish a limiting case, find one witness, recover a missing lemma or test a proposed connection. Explain how that result would contribute to the larger question. If the contribution is already available, use it and select the next unresolved step.

E.10.INT helps distinguish useful interest from novelty, surprise or a local scoring heuristic. A question can be worth pursuing because it opens further constructions, changes what can be explained or makes another question approachable. Its eventual practical destination may remain unknown. When problems and ways of solving them must develop together, use C.40; retain a promising alternative when its prospective use justifies doing so.

Continue with the chosen question, its first attempt and the dependency that attempt is meant to resolve. A short explanation in the work can carry this result. Stop when the current need is answered, or when another inquiry is the better use of the available effort.

### B.5.QD:4.6 - Separate question recognition from answer assurance {#separate-question-recognition-from-answer-assurance}

Recognize the opening from a changed possibility of inquiry. One worked counterexample or a useful new operation can be sufficient to begin developing the question.

Judge the question by whether it has a recoverable meaning, a possible contribution and a workable point of entry. Judge its proposed answer by the claim it makes. A conjecture, a proven relation, a simulated result and an observed physical effect support different uses. Apply their subject Methods and B.3 when the receiving use needs that assurance.

Reuse the question while its purpose and conditions remain applicable. Reopen it when a result changes its premises, available operations, attainable scope or intended use. A solved question can open another valuable one; an adequate answer can also end the present work.

## B.5.QD:7 - Conformance Checklist {#conformance-checklist}

- The earlier work and its consequential result are recoverable.
- A failure is located at the claim, premise, inference or implementation it affects; a success exposes its reusable operation or relation.
- The new question states an answer form and the conditions needed to understand it.
- A changed formulation preserves the still-unanswered part of the earlier task when that part remains useful.
- A worked attempt reveals a consequence, a missing distinction or the operation to obtain next.
- The question's possible contribution and its attainable first step justify pursuing or retaining it.
- The proposed answer is used with the scope and support appropriate to its claim.
- Further work can stop when an available answer suffices; explanations and records are only as extensive as their receiving use requires.

## B.5.QD:9 - Consequences {#consequences}

Question development turns both failure and success into possible further work. It can preserve a useful construction, make a missing premise investigable or reveal a result that serves another practice. Contributors can divide the work around those identified dependencies.

There is a cost to opening alternatives. A few consequential variations and a revealing attempt often suffice. Some questions remain worth keeping until a needed operation, collaborator or use becomes available; others can be set aside after their first attempt shows little prospective contribution.

## B.5.QD:12 - Relations {#relations}

- **B.5** coordinates the reasoning cycle. **B.5.RA** recovers an argument; **B.5.RR** revises reasoning after a premise or question changes. This pattern constructs a question that can start that revision.
- **B.5.TC** can reveal a newly expressible question when comparing accounts. **B.5.2** generates candidate explanations once that is the needed contribution.
- **B.5.MPC** connects the physical, mathematical and computational contributions a question needs. **A.3.3**, **C.16** and **C.29.2** supply state, measurement and computational-formulation work where applicable.
- **C.39** obtains a missing way to produce a distinguished result. **C.40** develops problems and ways together; this pattern contributes the question-construction step.
- **C.22.2** describes a problem claim when that description is needed. **E.10.INT**, **C.11** and **C.11.DUA** help choose a worthwhile inquiry and the effort to spend.
- **C.36.RP** supports continuing a shared practice by recovering and changing its ways of inquiry. **A.15.9** helps obtain and use a bounded contribution from another practice when needed.


## Dependencies {#dependencies}

- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/B-5-RA#root and spec://ai.lev/fpf-spec/contract/B-5-RR#root for reasoning; spec://ai.lev/fpf-spec/contract/B-5-MPC#root for joint contributions; spec://ai.lev/fpf-spec/contract/C-39#root and spec://ai.lev/fpf-spec/contract/C-40#root for methods and coupled development; spec://ai.lev/fpf-spec/contract/E-10-INT#root and spec://ai.lev/fpf-spec/contract/C-11-DUA#root for worthwhile inquiry. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/B-5-PI#root, spec://ai.lev/fpf-spec/contract/B-5-QD-CF#root, spec://ai.lev/fpf-spec/contract/C-39-RO#root, spec://ai.lev/fpf-spec/contract/C-40-CD#root, spec://ai.lev/fpf-think-math/contract/MATH-23#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/B-5-QD
