# B.5.TC - Compare Theoretical Accounts for a Working Question {#root}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method-description pattern
> **Status:** Draft
> **Normativity:** Normative unless marked informative

## B.5.TC:1 - Problem frame {#problem-frame}

**Use this when** two theoretical accounts appear to give different answers, explanations or instructions for the work you are doing, and you need to decide how to use them. They may employ different objects, preserve different information or obtain a result by different operations. Comparing their vocabulary or final numbers has left the practical difference unclear.

The work here is to compare particular uses of those accounts. A theory supplies objects, relations and ways of reasoning; an application adds a question, an interpretation and the premises needed to obtain an answer. Compare those applications while keeping the underlying accounts understandable on their own terms.

**First useful move.** Ask one concrete question of each account. Supply the same relevant situation, recover how each answer is obtained, and locate the first difference that matters to the use. A route description that says where travel is possible and one that gives minimum travel cost can both be useful. The question determines which information and operations you need.

The result explains what each account contributes, the conditions of agreement or difference, and which use or inquiry should follow. You may select one sufficient account, combine complementary contributions, or retain an unresolved difference together with what remains usable.

Use a familiar comparison directly when its question and conditions already fit. If only one application is unclear, B.5.TU helps construct it. If the disputed object is a numerical implementation of an understood model, begin with C.29.2. This pattern becomes useful when it is still necessary to compare the accounts or locate the source of their apparent disagreement.

## B.5.TC:2 - Problem {#problem}

Two descriptions can use the same word for different quantities, or different words for a shared construction. One can answer a weaker question. They can agree on observations while disagreeing about an intervention. An approximate computation can also obscure agreement between the theories from which the computations were derived.

A useful comparison must recover enough of each application to distinguish these situations. It must also leave room for an account that opens a question the original comparison did not ask. The practical problem is to determine **what the difference permits, prevents or changes for the work**, without requiring a verdict on the theories in every possible use.

## B.5.TC:3 - Forces {#forces}

| Force | Working tension |
|---|---|
| A shared question vs different concepts | Comparison needs a shared use, while translating every term into one vocabulary can erase the difference being investigated. |
| Agreement vs scope | A worked case makes an account usable; an equivalence claim across cases needs the corresponding argument. |
| Explanatory reach vs effort | A richer account can answer further questions while a smaller account supplies the present answer more cheaply. |
| Discrimination vs useful closure | A difference may justify further work, or leave the needed result unchanged. |
| Common operations vs subject knowledge | The comparison method travels across practices; its particular proofs, laws and causal premises come from the accounts being compared. |

## B.5.TC:4 - Solution {#solution}

**Fix the working question → construct each account's application → align the case and the meaning of its answer → locate the consequential difference → use what the comparison establishes, or pursue the difference that matters.**

The sequence is revisable. Reuse an established application or correspondence. Return to the question when the accounts reveal that it combines different needs. Stop when the available result suffices for the intended use.

### B.5.TC:4.1 - State the answer the work needs {#state-the-answer-the-work-needs}

Say what you want to explain, predict, construct or decide, and what would count as an answer. Specify the conditions that can alter that answer: for example, the initial state and time of a prediction, the allowed routes and quantity to minimize, or which intervention is contemplated.

Keep the account and its proposed use separately visible. Comparing a theory's possible reach with a rival's already implemented calculation is a comparison of unequal contributions. Either construct the relevant application of both or state which contribution is still unavailable. An unavailable application can be a reason to use another account now while retaining the first for development.

If the accounts answer different questions, identify their shared question, if any. For the remaining questions, compare their usefulness as complementary contributions. A newly expressible question can itself be a valuable result: explain what inquiry it opens and why that inquiry matters. B.5:4.4 connects this result to problem development.

### B.5.TC:4.2 - Recover an application of each account {#recover-an-application-of-each-account}

For each account, recover the objects and relations used, what is supplied or assumed, the operation that obtains the answer, and how that answer is interpreted. Follow the reasoning far enough to reproduce the step on which the comparison turns. B.5.TU, B.5.RC and B.5.RA supply application, construction and argument recovery when needed.

Preserve the source's distinctions during this work. If two accounts use *state* differently, explain which information each state retains and what continuation it determines. If a symbol has no counterpart, say what the account does with it before proposing a correspondence. Translate the required objects and operations; a word-to-word substitution alone cannot settle their relation.

An account may need information the present work lacks. Separate a supplied premise, a proposed premise and a derived result in the explanation. Continue conditionally when that is useful: “Under this independence assumption the minimum is 3; if continuations depend on the incoming route, we must retain that dependency.”

A collaborator or tool can supply a calculation or proof. Recover the interpretation and conditions needed to compare its contribution. Learn or request the missing operation when you cannot yet follow the decisive step; a broad study of both theories is unnecessary when a smaller contribution settles the use.

### B.5.TC:4.3 - Work the same case and align the answers {#work-the-same-case-and-align-the-answers}

Choose a small case that exercises the disputed operation or distinction. Give each account the corresponding inputs, derive its answer, and express the answers in the terms of the working question. Explain the correspondence when the inputs or outputs have different forms.

For a mathematical application, compare the retained distinctions and operations. C.29.1 supplies the preservation argument when a result is to be transferred. For a physical application, keep the phenomenon, operating conditions and meaning of the predicted quantity aligned. For a computation, separate the mathematical formulation from approximation, numerical tolerance and execution.

Begin with an understood case so a transcription or implementation error can be found. Then use a changed case that exercises the claimed difference: a shared resource, a constraint, an intervention or another relevant variation. Derive a general relation when the intended conclusion ranges beyond the cases. A finite example establishes its own result; a counterexample can refute a general assertion whose premises it satisfies.

Agreement of reported numbers is informative only after their meanings and conditions are aligned. Conversely, different intermediate objects can lead to the same answer through an explained correspondence. Record only the derivation or explanation the receiving use needs; the comparison does not require a standard table or separate report.

### B.5.TC:4.4 - Locate what causes the difference {#locate-what-causes-the-difference}

Follow each answer back to the first step where the applications cease to agree. Use the following distinctions where they resolve that case.

| What differs | Next useful operation |
|---|---|
| The question or output meaning | Restate the common question; keep other answers as complementary contributions. |
| A premise, boundary or retained distinction | Work the accounts under aligned premises, or show which case requires the additional premise or information. |
| A construction or inference | Recover the competing steps. Derive their relation or exhibit where one fails under its stated conditions. |
| An approximation or execution | Compare the mathematical result with the implemented procedure and its error under the relevant conditions. |
| The proposed physical or causal account | Derive the consequence on which they disagree; use the available domain knowledge and evidence for that consequence. |

Several differences can interact. Aligning one premise can remove an apparent conflict; it can also expose a remaining one. Keep the remaining question named. If the answer depends on a missing correspondence or inaccessible operation, return that missing contribution rather than ranking the theories from their summaries.

Additional evidence is useful when it can change the needed conclusion. First use an available derivation, counterexample, observation or established result. If the difference remains consequential, compare the possible gain from a discriminating inquiry with its cost and feasibility under C.11.DUA. A difference that cannot change the present use can remain unresolved. When it does change the use and cannot be settled, retain the conditional answers or obtain a sufficient weaker result.

### B.5.TC:4.5 - Choose the use and preserve the reason {#choose-the-use-and-preserve-the-reason}

Return the comparison in the form the work can use. A short explanation can state the question, the decisive construction, what agrees or differs and the resulting continuation.

Common outcomes are:

- **One sufficient account.** Use the account that answers the question under acceptable conditions and effort. State the limitation that would make another account necessary.
- **Agreement for a stated range.** Reuse either account for that result, choosing by effort, available tools or the further construction it makes easier. Preserve the relation that supports the agreement.
- **Complementary uses.** Give each account its question and contribution. When combining their results, establish the compatibility needed at the connection.
- **A consequential unresolved difference.** Keep the conditional answers and the premise or observation that would discriminate them. Continue with an unaffected result, a sufficient bound or the worthwhile inquiry selected for that difference.

Accuracy, reach, computational effort, learning effort and the ability to change the construction can matter differently across uses. Compare the values that can change this choice. If their trade-off is unresolved, C.11 supplies the decision method; a single “best theory” score would hide it.

Reopen when the question, premises, interpretation, available operation or relevant evidence changes. B.5.RR helps revise the affected reasoning. Reuse the comparison where its dependencies remain intact.

### B.5.TC:4.6 - Separate recognition from assurance {#separate-recognition-from-assurance}

Recognize the need from an unresolved disagreement or a choice between accounts. One worked comparison can already reveal an omitted premise or a useful complementary answer.

Qualify the result for its intended use. A mathematical equivalence needs a derivation over its claimed domain. A physical prediction needs the corresponding model and observation basis. An implemented approximation needs an error account adequate for the question. Use the relevant subject Methods and B.3 for these claims. Broader reliance is a reason to establish the broader claim, while an ordinary local use can stop with its sufficient local result.

## B.5.TC:7 - Conformance Checklist {#conformance-checklist}

- The comparison names a working question and explains what its answer changes.
- Each application has recoverable meanings, inputs, premises, decisive operations and an interpreted answer.
- The shared case corresponds across accounts; a missing correspondence remains visible.
- Agreement or disagreement is traced to the relevant question, premise, operation, inference, implementation or physical account.
- The conclusion has the scope established by its derivation, cases and applicable evidence.
- A sufficient cheaper account, complementary use or useful conditional result remains selectable.
- Further inquiry has a consequence for the intended use that can justify its burden.
- The result states the next use and the change that would reopen the comparison.

## B.5.TC:9 - Consequences {#consequences}

The practitioner gains a reasoned division of use between accounts, or a located disagreement that can guide the next inquiry. That result also supports collaboration: contributors can work on the missing mathematical operation, physical premise or computational approximation instead of repeating the whole dispute.

Reconstruction costs effort. Reuse an applicable comparison and stop at the explanation needed for the work. A comparison remains dependent on its question and premises; a changed use can make previously irrelevant distinctions decisive.

## B.5.TC:12 - Relations {#relations}

- **B.5** coordinates the reasoning cycle and return to a changed question. **B.5.TU**, **B.5.RC** and **B.5.RA** recover an application, construction or argument; **B.5.RR** revises the affected reasoning.
- **C.29** selects mathematical lens use; **C.29.1** constructs the correspondence needed to transfer a result. **C.29.2** and **C.29.3** separate computational formulation from physical execution.
- **B.5.MPC** connects mathematical, physical and computational contributions. **C.28** governs causal and intervention claims.
- **C.38** constructs comparable ways to obtain one result. This pattern supplies a theoretical comparison when such a way depends on an unsettled account. **C.11** and **C.11.DUA** govern a consequential choice and the worth of further inquiry.
- **F.0.2** uses a comparison of accounts when forming a conceptual synthesis across sources. **A.6.3.RT** supports operative expression, and **A.15.9** obtains a missing specialist contribution.


## Dependencies {#dependencies}

- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/B-5-TU#root, spec://ai.lev/fpf-spec/contract/B-5-RA#root and spec://ai.lev/fpf-spec/contract/B-5-RR#root for applications and reasoning; spec://ai.lev/fpf-spec/contract/C-29-1#root, spec://ai.lev/fpf-spec/contract/C-29-2#root and spec://ai.lev/fpf-spec/contract/C-29-3#root for transfer and computation; spec://ai.lev/fpf-spec/contract/C-28#root for causal use; spec://ai.lev/fpf-spec/contract/F-0-2#root for synthesis; spec://ai.lev/fpf-spec/contract/C-11-DUA#root for worthwhile inquiry. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-1-RI#root, spec://ai.lev/fpf-spec/contract/B-5-QD-CF#root, spec://ai.lev/fpf-think-phy/contract/PHY-10#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/B-5-TC
