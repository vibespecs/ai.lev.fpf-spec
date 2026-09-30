# B.5.TU - Construct a Working Use of an Unfamiliar Theory {#root}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method-description pattern
> **Status:** Draft
> **Normativity:** Normative unless marked informative

## B.5.TU:1 - Problem frame {#problem-frame}

Use this pattern when a theory offers a promising way to answer a question, but you cannot yet connect its objects and reasoning to an answer you can use. You may recognize the notation or reproduce a calculation while still being unable to say what to supply, which operation matters, or what the result would let you do.

The work here is to construct one application of the theory. Begin with the question and the available account; obtain and interpret the contribution that question needs. The result can be a construction, prediction, explanation, bound or identified missing operation. A mathematical question about what can be constructed is a possible receiving use, as is an engineering decision.

**First useful move.** Choose one question the theory might settle. Find a source case or rule that could supply its answer. Say what plays each required part in your case, work the decisive operation, and explain what its result changes. If you cannot make that connection, locate the first missing premise, interpretation or operation.

For example, a theory of composition lets you combine two operations. Does it let both consume one input, or does the combination require two separately supplied inputs? Recovering that distinction can change the proposed implementation before any code is written.

Use an adequate, understood application directly. A specialist or tool may supply a result you can already interpret and use under its conditions. Reconstruct more of the theory when the needed application, criticism, adaptation or explanation remains unresolved.

## B.5.TU:2 - Problem {#problem}

A theory's descriptions usually distribute its usefulness across definitions, examples, constructions and arguments. A reader may know each familiar word yet be unable to assemble these contributions for a new question. Conversely, a familiar calculation can conceal a change of question: the calculation solves the stated equations, while the receiving work needs a condition those equations omitted.

The difficulty has two connected parts. First, discover what the account makes possible and how to obtain that result. Then apply it to the question that justified the work. An answer can also reveal a new question or a useful limitation of the theory.

## B.5.TU:3 - Forces {#forces}

| Force | Consequence for the method |
| --- | --- |
| A question focuses learning, while an unfamiliar account can change the question. | Begin with one intended use and revise it when a construction reveals a consequential distinction. |
| A worked source case saves effort, while a new application changes some of its premises. | Reuse the case and identify the changed contribution before carrying over its answer. |
| Operational fluency and understanding of derivations serve different work. | Recover the depth needed to apply, criticize or alter the contribution. |
| A small case exposes connections, while a general claim reaches beyond that case. | Keep the demonstrated use and the argument for greater reach distinguishable. |
| Available assistance can supply difficult operations, while the receiving use still needs interpretation. | Divide work at the missing contribution and retain the meaning of the returned result. |

## B.5.TU:4 - Solution {#solution}

Connect the working question, the theory's constructive or inferential resources, and the use of the resulting answer. Enter where the unresolved connection begins; reuse contributions already available. The following unfolding can be revisited when its own result changes an earlier choice.

### B.5.TU:4.1 - Choose an application worth constructing {#choose-an-application-worth-constructing}

State what an answer would help someone understand, obtain, predict, rule out or change. Select one case small enough to work with the available means while retaining the difficulty. For example, “Can these two operations use the same input?” gives composition rules a purpose; “understand category theory” leaves that first use unselected.

Locate a source application serving that question, or the nearest account whose objects and rules could be adapted. State which part is supplied and which you are proposing. A theory can also be explored to discover a useful question: try one of its characteristic operations and inspect what its result makes distinguishable or obtainable.

Determine the contribution you need to learn or obtain. Applying a supported formula can need its inputs and use conditions; changing the formula can need its construction and argument. Explain the needed difference in work before selecting further study.

### B.5.TU:4.2 - Recover what the theory lets you work with {#recover-what-the-theory-lets-you-work-with}

For this application, identify the objects, relations, given information, permitted constructions and inferential rules. Read a definition together with an operation that uses it. Ask what can be supplied as an input, what can be produced, and which property or conclusion the rule establishes.

Follow the needed result backward to its prerequisites. Keep shared prerequisites and jointly required inputs visible. When a description names a construction without showing how to perform it, B.5.RC recovers its producing operations. When an inference remains unclear, B.5.RA recovers the reason and transitions needed by the receiving use.

Make an unfamiliar expression operative at the point of difficulty. Determine the arguments of a function, the objects related by a diagram, or the conditions under which a rule applies. A.6.3.RT helps construct a usable expression under the available notation. Understanding a symbol's name is useful only as far as it helps perform or interpret the operation.

### B.5.TU:4.3 - Construct the application {#construct-the-application}

Connect each consequential object and condition to the selected case. Some are supplied by observation or design; some are assumptions of the model; others belong to the theory's mathematical construction. Keep their roles clear where they affect the conclusion.

Choose the values, boundary conditions, allowed operations and sought output. For a theoretical question, this may be entirely a construction within the theory. For a physical use, explain which system, quantity or interaction the mathematical object represents. C.29 supplies the mathematical correspondence and the comparison of what it preserves, omits or introduces.

Compose the required operations. Check the connection between successive contributions: an operation's output must supply the next operation's required input. An integration procedure, for example, needs a function of its integration variable; a formula with unfilled path or parameter arguments has yet to supply that function.

If a source case cannot be adapted by the available rules, identify the particular missing contribution. Another formulation, a specialist result or a developed operation may supply it. A.15.9 supports obtaining and using bounded help; C.39 supports developing a way when none is known.

### B.5.TU:4.4 - Obtain and inspect a consequence {#obtain-and-inspect-a-consequence}

Work the selected case far enough to answer the question or expose the gap. Use direct reasoning, a construction, a small computation or an available tool according to the work. Recover the step that makes the consequence follow and the premises it uses.

When computation is involved, interpret its inputs, operations and output. C.29.2 supplies a missing computational formulation; C.29.3 supplies the connection to the system performing it. A successful execution can help locate expression or implementation errors. The argument for what the computation establishes remains tied to the chosen formulation.

Compare with a simple consequence you can inspect when that comparison can reveal an error: a limiting case, a preserved quantity, an input count, a dimensional relation or a small enumeration. Select the relevant comparison; its purpose is to expose a possible failure in this application.

### B.5.TU:4.5 - Apply the answer to the working question {#apply-the-answer-to-the-working-question}

Read the answer back in the terms of the intended use. If it gives a construction, determine whether the required inputs and operations are available. If it gives a bound, use the exclusion or allowance that bound supports. If it gives a physical prediction, identify the model and operating conditions under which that prediction concerns the system.

Examine the correspondence at the point where it could change the action. Does a feasible mathematical answer violate a receiving condition? Could two cases treated alike by the formulation require different actions? If so, restore the distinction, change the formulation, or keep a weaker answer that remains useful.

For a new physical reliance, address the model assumptions whose failure could change that use. Reuse adequate knowledge and observations. Choose further checking or acquisition under C.11.DUA when their benefit and burden are the live decision; an unresolved stronger claim need not displace a sufficient conditional answer.

### B.5.TU:4.6 - Return the result and choose the continuation {#return-the-result-and-choose-the-continuation}

Return the interpreted answer and the conditions its receiver needs. An ordinary explanation, calculation or demonstration can carry it. Preserve a separate account when another participant or later use needs to reconstruct the application.

Stop when the contribution suffices. Otherwise identify what remains: a source explanation, missing operation, changed model, competing theoretical account or newly worthwhile question. B.5.RR follows the effect of a changed premise; B.5 coordinates a changed inquiry.

Use this result to choose the next learning or work contribution. When the work requires one participant to apply or alter the method independently, that capability needs its own performed use under the relevant conditions. A supplied answer can still serve work that does not require that independence.

## B.5.TU:7 - Conformance Checklist {#conformance-checklist}

- The application has a working question and a useful result to obtain or interpret.
- The theory's objects, operations and premises needed for that application are recoverable.
- The construction connects supplied inputs to required outputs; a missing operation remains a specific gap.
- A source-supported application and a newly proposed adaptation retain their respective grounds.
- The worked consequence states what its construction, argument or computation establishes.
- The receiving use preserves consequential conditions, including any difference between an attainable result and a bound.
- Further study, evidence or specialist work serves a remaining useful contribution at an appropriate cost.
- The return supports an action, understanding, construction or next question; sufficient use can stop.

## B.5.TU:9 - Consequences {#consequences}

The practitioner can move from a promising theory to a worked use, or state the contribution that prevents it. The result also makes division of work easier: one participant can supply a model, another a construction or calculation, and another the receiving interpretation.

The cost is recovering enough of the account to assemble and use the application. Reuse supplied explanations and operations where adequate. Detailed derivations, broader source comparison or empirical inquiry are worthwhile when their answers affect the intended work.

## B.5.TU:12 - Relations {#relations}

- **B.5** coordinates the inquiry and a changed question. **B.5.FM** constructs a first model when consequential participants or relations remain unclear.
- **B.5.RC**, **B.5.RA** and **B.5.RR** supply construction recovery, argument recovery and reasoning revision.
- **B.5.4** constructs a situational interpretation of an available concept. **C.29** and **C.29.1** supply mathematical correspondence and result transfer.
- **C.29.2**, **C.29.3** and **B.5.MPC** connect computation, realization and the physical question.
- **A.6.3.RT** prepares an operative expression; **C.2.8** helps characterize what a recipient can extract from an explanation under stated preparation and access.
- **A.15.9** supplies bounded professional help; **C.11.DUA** selects useful further effort; **C.39** develops a missing way.
- **C.40** develops questions and ways together when the application opens that further work.


## Dependencies {#dependencies}

- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/B-5#root, spec://ai.lev/fpf-spec/contract/B-5-RC#root, spec://ai.lev/fpf-spec/contract/B-5-RA#root and spec://ai.lev/fpf-spec/contract/B-5-RR#root for reasoning; spec://ai.lev/fpf-spec/contract/C-29#root and spec://ai.lev/fpf-spec/contract/A-6-3-RT#root for mathematical correspondence and expression; spec://ai.lev/fpf-spec/contract/A-15-9#root for bounded help. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-1-RI#root, spec://ai.lev/fpf-spec/contract/B-5-TC#root, spec://ai.lev/fpf-spec/contract/C-39-RO#root, spec://ai.lev/fpf-spec/contract/C-40-CD#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/B-5-TU
