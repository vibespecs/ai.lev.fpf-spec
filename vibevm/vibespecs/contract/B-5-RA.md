# B.5.RA - Recover an Argument for Its Next Use {#root}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method pattern
> **Status:** Draft
> **Normativity:** Normative unless marked informative

## B.5.RA:1 - Problem frame {#problem-frame}

Use this pattern when you have an argument or a reported result but cannot yet understand why it supports the conclusion you want to use. You may need to apply the result, criticize it, explain its decisive step or decide which part survives a proposed change.

The **argument** is the reasoning that connects premises to a conclusion. It may use a mathematical construction, a calculation or a subject inference from observations. The relevant practice supplies the permitted inference and the grounds for its premises.

**First useful move:** state what you want to do with the conclusion, then recover the main reason offered for it. Follow the needed intermediate claims until you can explain the decisive transition and its conditions.

The reader needs the subject preparation assumed by the source, or access to the missing explanation. Use an adequately understood result directly when its conditions already fit the task. A request to understand the argument can stop before re-proving every established result it uses. A separate obligation to validate the entire proof or underlying observations selects the corresponding checking work.

## B.5.RA:2 - Problem {#problem}

An argument can be present without being usable by its reader. A reader may recognize each term yet miss why a lemma was introduced, where two premises must be used together, or how a local calculation establishes the general conclusion.

Reading each sentence fluently or checking isolated inferences leaves the overall method uncertain. Reading only the overview can hide a decisive unsupported transition. Either failure prevents useful transfer: the practitioner cannot tell what to use, which condition matters or where to ask for help.

The useful result is enough recovered reasoning to perform the intended use, or a localized gap whose resolution would make that use possible. This may be a conditional conclusion when a needed premise remains open.

## B.5.RA:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Local inference and overall method | Individual transitions can be understood while the purpose of a construction or the route to the conclusion remains obscure. |
| Understanding and checking | Understanding may reuse established results; validating a whole argument can require additional work under a different question. |
| Useful compression and hidden dependence | A lemma can make a long argument manageable, but the reader must know what it supplies and which conditions it uses. |
| Conditional result and unresolved premise | Useful consequences may follow before every premise is established, provided the next use preserves the condition. |
| Source recovery and new reasoning | Repairing a gap can open a valid use, while attribution must distinguish the supplied argument from the reader's addition. |

## B.5.RA:4 - Solution {#solution}

Recover the reasoning at both the level of its main contributions and the transitions needed for the next use. Move between these levels when a local step changes your understanding of the whole argument.

### B.5.RA:4.1 - State the use and read the claim {#state-the-use-and-read-the-claim}

Name what the result would let you do: calculate a quantity, choose between alternatives, criticize a conclusion, adapt an argument or explain it to someone else. This determines how far recovery needs to go.

Read the conclusion with its objects, domain and conditions. In a mathematical statement, recover the quantifiers: which objects are arbitrary, which may be chosen, and on what a chosen object may depend. In an empirical argument, recover what observations and inference support which population, conditions or phenomenon.

Locate the source's definitions when a word or symbol admits different readings that would change this use. If a formal statement accompanies an informal one, compare the part of their meanings on which the intended application depends. For example, whether zero is allowed among “natural numbers” can change the statement.

### B.5.RA:4.2 - Recover the main reason {#recover-the-main-reason}

Read for the difficulty the argument overcomes and the contribution that overcomes it. Ask why a construction, lemma, decomposition or comparison appears where it does.

Express the main reason in a short explanation: what is established first, what that makes possible, and how the remaining step reaches the conclusion. This may involve a reduction to an easier problem, an invariant, an exhaustive case distinction or another subject method. Use the method actually present in the source.

The first explanation is a working interpretation. Check it against the decisive steps. If it cannot explain why those steps are needed, revise it rather than retaining an attractive summary unrelated to the argument.

### B.5.RA:4.3 - Recover the dependencies of the conclusion {#recover-the-dependencies-of-the-conclusion}

Work backward from the conclusion through the claims or constructions it uses. At each needed transition, identify its premises, the inference or operation, and the result.

Keep jointly needed premises together. Preserve an independently sufficient alternative as a separate way to reach the conclusion. Track a shared premise wherever a later step uses it; repeated uses of one assumption do not provide independent support for that assumption.

Distinguish a premise supplied for the argument, a result established earlier and a temporary assumption used inside a subargument. Recover the point at which a temporary assumption is discharged and what then follows. If this logical form is unfamiliar, obtain the relevant explanation before treating the subargument's assumption as an established fact.

Use established results at the level needed for the task. If the question concerns what a lemma permits, its statement and conditions may suffice. If the question concerns how to alter the lemma's proof, recover its internal reasoning.

### B.5.RA:4.4 - Explain the transition that is still missing {#explain-the-transition-that-is-still-missing}

For a transition you cannot follow, recover the relevant definition, rule, earlier result or construction. Apply it to the participants at that transition. Say why these premises license this result and which condition is doing the work.

A useful self-explanation supplies this relation. “I understand this line” reports confidence; a paraphrase repeats the claim. Neither supplies the omitted inference when that is the difficulty.

Work a small instance when it helps reveal the operation or dependence. Then return to the stated scope: the instance may illustrate a general step, while the general conclusion still depends on the argument for all cases in its domain.

If the source's resources do not close the gap, ask for the missing step with its premises and desired result. A proposed repair is new reasoning until it is justified. Keep the consequence conditional when a premise remains unresolved and conditional use is sufficient.

Where the missing step constructs an auxiliary object, use B.5.RC. Where it makes a statistical, causal or other subject inference, use that subject's method and conditions.

### B.5.RA:4.5 - Use the recovered reasoning and stop at a useful result {#use-the-recovered-reasoning-and-stop-at-a-useful-result}

Perform the use named in :4.1. Apply the result under its conditions, explain the decisive step, identify a consequential criticism, or name what must be recovered before the use is possible.

Make the conclusion no stronger than the recovered reasoning supports. If recovering the argument reveals an open premise, state its effect on the intended use. When several sufficient arguments are available, an unresolved branch may be bypassed through a branch whose premises and reasoning are adequate.

If a premise or requested conclusion changes, use B.5.RR to follow the affected reasoning and derive what still follows. The recovered dependencies supply the starting point for that work. An unchanged, adequately supported part can be reused.

C.11.DUA governs whether more checking or information is worth obtaining for this decision. Understanding an argument, verifying its correctness and establishing its real-world premises can require different work. Select further work from the unresolved question. When the work is divided among agents, give the next contributor the premises at the missing transition, the result needed there and the intended use. On return, connect the supplied reasoning to the argument's main reason. Use the explanation or working notation that makes the continuation possible.

## B.5.RA:7 - Conformance Checklist {#conformance-checklist}

For the argument and use being recovered:

1. The intended use and the conclusion's domain and conditions are recoverable.
2. The explanation states the main reason for the result and connects it to the decisive steps.
3. The needed transitions identify their premises, inference or operation and result.
4. Joint premises, sufficient alternatives, shared assumptions and temporary assumptions retain their different roles.
5. The reader can perform the intended use or identify the missing transition or premise that prevents it.
6. A small instance supports the explanation at its stated scope; a general conclusion has its corresponding reasoning.
7. Further checking is selected for an unresolved question, and adequately supported parts remain reusable.

These are questions about the recovered reasoning. Their answers may already be evident in the working explanation or application.

## B.5.RA:9 - Consequences {#consequences}

A recovered argument can support application, explanation, criticism and later revision. Work can be divided around meaningful intermediate results, and a request for help can name the transition that remains obscure.

The method can reveal that the source's conclusion exceeds its support or that the reader lacks a prerequisite. It cannot supply every missing subject method. Its economical stopping points are a sufficient argument for the use, a useful conditional conclusion or a localized gap.

## B.5.RA:12 - Relations {#relations}

- **B.5:** coordinates inquiry and the revision that can follow recovery of an argument.
- **B.5.RC:** obtains an auxiliary construction that a decisive transition requires.
- **B.5.MPC:** connects arguments and constructions across physical, mathematical and computational contributions.
- **B.3 and B.3.3:** govern confidence and assurance questions when the intended reliance requires them.
- **C.11.DUA:** selects additional checking and information for the decision at hand.
- **C.2.8 and C.37:** characterize recipient-accessible structure and support selection of representations.



## Dependencies {#dependencies}

- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/B-5#root and spec://ai.lev/fpf-spec/contract/B-5-RC#root for inquiry and construction, spec://ai.lev/fpf-spec/contract/B-5-MPC#root for joint reasoning, and spec://ai.lev/fpf-spec/contract/C-2-8#root/spec://ai.lev/fpf-spec/contract/C-37#root for recipient understanding and representation choice. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-15-10#root, spec://ai.lev/fpf-spec/contract/A-6-3-RT-OE#root, spec://ai.lev/fpf-spec/contract/B-5-QD#root, spec://ai.lev/fpf-spec/contract/B-5-QD-CF#root, spec://ai.lev/fpf-spec/contract/B-5-RC#root, spec://ai.lev/fpf-spec/contract/B-5-RR#root, spec://ai.lev/fpf-spec/contract/B-5-TC#root, spec://ai.lev/fpf-spec/contract/B-5-TU#root, spec://ai.lev/fpf-spec/contract/C-36-RP#root, spec://ai.lev/fpf-think-math/contract/MATH-10#root, spec://ai.lev/fpf-think-math/contract/MATH-12#root, spec://ai.lev/fpf-think-math/contract/MATH-19#root, spec://ai.lev/fpf-think-math/contract/MATH-6#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/B-5-RA
