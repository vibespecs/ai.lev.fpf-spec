# B.5.QD.CF - Reformulate a Problem by Examining Its Conflicting Assumptions {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method pattern
> **Status:** Stable
> **Normativity:** Normative

## B.5.QD.CF:1 - Problem frame {#problem-frame}

**Use this when** an account makes needed outcomes appear incompatible and you need to find what could change without losing the purpose of the work. Two requirements may concern different operating conditions, yet the model gives them one setting. A familiar means of obtaining one result may obstruct another result, although that means has never been shown necessary.

**First useful move.** Put the two demands beside the statement that makes them conflict. Ask what requires that statement. For example, “the setting must be at least 6 during work and at most 2 during quiet operation” conflicts with a fixed-setting design. It leaves open a question about changing the setting between those conditions.

The result is a reformulated question or candidate construction whose retained requirements, changed premise and remaining obstacle are understood. Sometimes the useful result is an impossibility under the retained conditions, followed by a decision about which requirement can change.

The reader needs enough knowledge to interpret the requirements and the inference connecting them, or access to someone who can supply that interpretation. Start with ordinary statements and a small case. Use an adequate existing solution directly. If the only unresolved question is choosing an accepted trade-off, compare the options; recovering premises is useful when it could reveal another option or change the grounds for that choice.

## B.5.QD.CF:2 - Problem {#problem}

An incompatibility identifies a limit of the statements used together. It does not yet identify the repair. A requirement may have been mistaken for a particular means, two situations may have been collapsed into one, or the desired result may be impossible under conditions that must remain.

Two shortcuts lose the useful question. Continuing with the same proposed means can make an avoidable conflict look inevitable. Relaxing a condition until the account has a solution can make a different task look like a solution of the original one.

The work is to reconstruct why the conflict follows, find a consequential premise worth examining, and develop another construction or an honest limit while keeping the original need recoverable.

## B.5.QD.CF:3 - Forces {#forces}

| Force | Working tension |
| --- | --- |
| Needed outcome and familiar means | A proven way is valuable, but familiarity can conceal an unsupported necessity claim. |
| Clear conflict and hidden conditions | A small conflicting set is easier to inspect; other requirements can still defeat its proposed repair. |
| Exploration and commitment | A temporary relaxation can reveal a possibility before anyone has the means or authority to realize it. |
| Precision and effort | A formal construction can settle a consequential inference; ordinary reasoning may already locate the question. |
| Continuity and change | A narrower question may produce useful work while leaving the original need partly unanswered. |

## B.5.QD.CF:4 - Solution {#solution}

**Recover the need and the conflict → expose the premises producing it → examine an assumed necessity or shared condition → construct another question or way → return to the retained requirements.**

Enter at the unresolved step. A short explanation beside the working model can carry the result; no separate conflict form is required.

### B.5.QD.CF:4.1 - State what must be obtained and where the conflict arises {#state-what-must-be-obtained-and-where-the-conflict-arises}

Say what result is needed, for whom or for what later operation, and under which conditions. Separate that result from the proposed means of obtaining it. Keep a requirement that the work cannot change visible throughout the attempt.

Recover the incompatibility in its stated scope. Two propositions may contradict each other under one interpretation. Two physical operations may compete for the same resource at the same time. Two people may disagree about a premise or about which outcome matters. A trade-off may permit both outcomes to some degree. These situations require different reasoning; use this method where examining the asserted incompatibility can change the construction question.

Identify the participants and conditions shared by the conflicting statements. Does “the setting” mean the same setting in the same operating condition? Does “available” refer to immediate access or access after a permitted delay? B.5.FM helps construct a missing distinction; B.5.TC compares different accounts when their questions or output meanings are unsettled.

### B.5.QD.CF:4.2 - Recover the inference and the status of its premises {#recover-the-inference-and-the-status-of-its-premises}

Work backward from the conflict to the statements that produce it. Use B.5.RA if the argument needs reconstruction. Keep their different roles understandable: what the work requests, what was observed, what the model assumes, and which proposed operation is supposed to supply a result.

Pay attention to necessity. “To obtain A, D is necessary” means A implies D. “Doing D under conditions K obtains A” is a sufficiency claim. Success with D alone supplies no argument that every way of obtaining A requires D. The question may be whether another operation E obtains A while avoiding the condition that obstructs the other requirement.

A small set of jointly conflicting statements is often sufficient. For a finite constraint account, one can hold the requirements fixed and examine what happens when one assumption is omitted. A remaining solution identifies a candidate assumption to examine; it does not establish that the assumption is false or dispensable in the intended work.

Find a minimal conflicting set only when the smaller explanation changes the task. “Subset-minimal” means that removing any member of that set removes its inconsistency. It does not mean that the set is the smallest possible, that repairing it is cheapest, or that no other conflict remains outside it.

### B.5.QD.CF:4.3 - Turn the consequential premise into a constructive question {#turn-the-consequential-premise-into-a-constructive-question}

Choose a premise whose change could matter and whose status is open to examination. Work the corresponding question:

- **An assumed necessary means creates the conflict.** What operation could obtain the needed outcome without that means? Follow the result that the means supplied; use C.39 to find or develop a replacement operation.
- **One value is imposed across different conditions.** Do the requirements concern distinguishable participants, times or situations? If so, what construction permits the required values in those conditions? If they concern the same participant and condition, a second name supplies no new possibility.
- **A restriction belongs to the present representation or construction.** What relation must a different representation or construction preserve, and how could it satisfy the retained requirements? B.5.FM constructs the relation; B.5.RR carries its change through the affected reasoning.

These are common entries, not an exhaustive set of creative moves. State what would answer the selected question: an alternative operation, a condition-dependent construction, a counterexample to necessity, or a derivation of impossibility.

A tentative assumption change lets you explore that question. Keep the conclusion conditional until the replacement premise or operation has the support its use needs. Reconsider a requirement explicitly when that is the selected change; a convenient answer to the changed requirement leaves the original one open.

### B.5.QD.CF:4.4 - Construct a small answer and return it to the whole need {#construct-a-small-answer-and-return-it-to-the-whole-need}

Perform the relevant reasoning or operation on a case that includes the changed condition. Show how the candidate obtains the needed result, or locate the contribution still unavailable. A formal witness answers a question about its model. A physical or organizational proposal also needs the means to produce the corresponding result in its intended setting.

Reapply every retained requirement that the proposed change can affect, including those outside the small set used to locate the conflict. A separate operating setting may require a transition that is too slow. An archived input may reproduce a calculation while violating a retained deletion requirement. Either consequence changes what the candidate can answer.

Keep three facts distinguishable: the revised statements are compatible; an operation is proposed that would supply their values; that operation has produced or otherwise established the result required for this use. Use the strongest available fact the current question needs. An inquiry about what to design next may be answered by a conditional construction; deploying it can require further work.

If the conditions remain incompatible, state that result under the premises that support it. The next question can ask which requirement may change, whether another model is warranted, or whether the work should stop. A proof of impossibility can settle a construction request without finding a replacement.

### B.5.QD.CF:4.5 - Continue at the missing contribution, or use the answer {#continue-at-the-missing-contribution-or-use-the-answer}

Use a sufficient answer. Otherwise say which part of the original need remains and what the next attainable result would change. B.5.QD develops that question; C.40.CD connects it with development of a way to answer it. A theoretical result can be worth pursuing because it makes further constructions or explanations possible, even before a particular application is known.

Compare the likely contribution of further work with its burden, including obtaining a capability or resource and the work displaced. Start with available arguments, results and specialist contributions. C.11.DUA applies when the worth of another information-gathering step is unsettled. The pattern requires no experiment merely to acknowledge that a proposal remains conditional.

Several contributors can divide this work by the result needed next: one recovers the disputed necessity, another constructs a replacement, and another interprets its consequences for the original work. They need the retained requirements and the meaning of each returned result. When this reasoning is a constituent of design or research, its local success must support the encompassing method's result; compatibility alone may be insufficient for that result. Constituent and encompassing methods can be enacted during the same work under B.1.5.

### B.5.QD.CF:4.6 - Separate recognition from assurance {#separate-recognition-from-assurance}

An asserted conflict and a premise worth examining can be enough to start. Recognition does not require an exhaustive diagnosis or a proof that a repair exists.

Judge each resulting claim by what it says. An implication needs valid reasoning under its premises. A replacement operation needs the mathematical, physical or professional basis appropriate to its intended use. A requirement change needs the decision that permits it. The method supplies a way to find and formulate these questions; their answers come from the corresponding subject methods.

Reopen the result when a retained requirement, affected premise, available operation or intended use changes. Preserve independently usable parts while revising the affected inference.

## B.5.QD.CF:7 - Conformance Checklist {#conformance-checklist}

- The needed result and the scope of the incompatibility are recoverable.
- The inference distinguishes requirements, observations, modeling assumptions and proposed means where their different roles change the answer.
- A claimed necessity has its direction and basis; a proposed replacement supplies the result previously attributed to that means.
- A changed participant or condition corresponds to the intended situation, rather than merely changing a name.
- The candidate returns to the retained requirements, including affected conditions outside the diagnosed conflict.
- A compatible account, conditional construction, obtained result and authorized requirement change retain their different meanings.
- The next question serves the unresolved need or states how that need was changed; a sufficient answer or impossibility can stop the work.

## B.5.QD.CF:9 - Consequences {#consequences}

The method can turn a conflict into a more useful construction question while preserving the purpose of the work. It also makes an impossibility usable: contributors can stop an unproductive search or decide which demand is open to change.

Recovering premises and returning a proposal to the full need costs effort. Concentrating on the inference that changes the next action keeps this effort bounded. Some conflicts remain unresolved because the replacement operation, relevant knowledge or authority is unavailable.

## B.5.QD.CF:12 - Relations {#relations}

- **B.5.QD** develops a useful question from a result or construction; this pattern specializes the conflict-to-question contribution.
- **B.5.RA** recovers the argument; **B.5.RR** revises the reasoning affected by a premise change. **B.5.TC** compares accounts whose meanings or conditions may differ.
- **B.5.FM** constructs a distinction and its relations. **C.39** develops a way to obtain the needed result; **C.40.CD** develops that way and the problem together.
- **B.1.5** supplies the Method-parthood relation when this reasoning contributes to an encompassing method while its constituent operations are enacted.
- **C.11.DUA** helps decide whether further information work can change a useful continuation enough to warrant its burden. **A.15.9** helps obtain a needed contribution from another practice.


## Dependencies {#dependencies}

- @fact:SPECIALIZES Specializes: spec://ai.lev/fpf-spec/contract/B-5-QD#root. @status:spec/done
- @fact:USES Uses: spec://ai.lev/fpf-spec/contract/B-5-FM#root, spec://ai.lev/fpf-spec/contract/B-5-RA#root and spec://ai.lev/fpf-spec/contract/B-5-TC#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/C-40-CD#root, spec://ai.lev/fpf-spec/contract/C-11-DUA#root and spec://ai.lev/fpf-spec/contract/B-1-5-EW#root. @status:spec/done

#source spec://ai.lev/fpf-spec/source/B-5-QD-CF
