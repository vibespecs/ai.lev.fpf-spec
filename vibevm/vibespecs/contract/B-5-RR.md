# B.5.RR - Revise Reasoning After a Premise or Question Changes {#root}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method pattern
> **Status:** Draft
> **Normativity:** Normative unless marked informative

## B.5.RR:1 - Problem frame {#problem-frame}

Use this pattern when reasoning that you could previously use needs to answer a changed question, or when a premise, observation or application condition changes. You need to know what still follows, what must be worked again and what can now be done.

The object of revision is the reasoning used for that question: its premises, intermediate contributions, conclusion and conditions of application. The relevant practice supplies its inference rules and the grounds for using its premises.

**First useful move:** state the change beside the result you now need. Find where the earlier reasoning used the changed condition, or where the new result requires a contribution the earlier argument did not supply.

This work requires enough subject knowledge to follow the argument. Use B.5.RA when that reasoning must first be recovered. If the established result already answers the new question under conditions that still hold, apply it and stop. Rebuilding the entire argument is useful when recovery would cost more, or when a separate obligation requires a full new derivation.

## B.5.RR:2 - Problem {#problem}

A familiar answer often survives in a formula, report or program after the reason for using it has changed. Repeating the earlier steps can produce a convincing answer to the former question. Discarding everything can waste constructions and arguments that remain useful.

Revision requires following the reason for a result. One conclusion may need several premises together; another may have two sufficient arguments. A premise may be shared by apparently different arguments. A change can also make a formerly fixed quantity the unknown, so replacing a number leaves the real task undone.

The result is reasoning that answers the changed question at its supported scope, or a useful partial result and the contribution still needed. It should let the receiver act, obtain that contribution or pursue the newly exposed question.

## B.5.RR:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Reuse and hidden dependence | Retaining an established result saves work, but its application may use the changed premise indirectly. |
| Local repair and a changed question | A small correction can preserve the conclusion; a new objective may require another argument. |
| Several arguments and a shared weakness | An alternative can preserve a conclusion, while a premise common to both can defeat that apparent independence. |
| Useful qualification and continued inquiry | A conditional result or bound may suffice now; another use may need the unresolved premise or a new construction. |

## B.5.RR:4 - Solution {#solution}

Start with the receiving question, follow the affected reasoning and derive the result that can now be used. A useful reminder is:

**Changed question or condition → affected reasoning → retained or replacement contribution → revised conclusion → receiving use.**

### B.5.RR:4.1 - Say what changed and what is needed now {#say-what-changed-and-what-is-needed-now}

Compare the earlier question with the present one. State the result needed and the changed condition in terms that can be used in the reasoning. For a calculation, that may be a new range or an input that is now an unknown. For an empirical conclusion, it may be an observation, a changed population or an operating condition.

Distinguish a change in the situation from a correction to your account of it. A measurement taken yesterday can remain a sound report of yesterday while being insufficient for today's operation. A proposed condition can be explored hypothetically without replacing the account of what has happened.

Keep the meanings of the quantities and claims visible. If the same term now denotes a different quantity, translate the question before substituting its value. If only the spelling or presentation changed and the established application still fits, no reasoning revision is needed.

### B.5.RR:4.2 - Recover the dependence that matters {#recover-the-dependence-that-matters}

Begin at the changed premise and at the desired conclusion. Find which intermediate claims or constructions connect them. At each relevant transition, ask what is needed together, what is produced and why that transition is allowed.

Keep a sufficient alternative separately. For example, recovering a file may require either a readable local copy or an available remote copy. If both are encrypted with one unavailable key, the two storage locations leave the same prerequisite unresolved.

Use an established lemma at the level its receiving use needs. Open its proof when the change reaches a condition of the lemma or the way its result is obtained. Do the same for an established measurement or computation: inspect the part whose application the change calls into question.

A sketch or a few statements can hold these dependencies. Use B.1.1 when a dependency representation needs its relation clarified. A reasoning dependency says which premise or operation supports a conclusion; physical causation and temporal order require their own relations.

If the needed dependence is missing from the account, recover it through B.5.RA or ask for that contribution. Treat a supposedly unaffected part as reusable only when its independence from the change is adequately understood for this use.

### B.5.RR:4.3 - Derive what follows after the change {#derive-what-follows-after-the-change}

Work from available premises through the affected transitions. Reuse a contribution whose conditions and required result still fit. Where they do not, derive the replacement, select an adequate alternative or identify the unresolved step.

Withdrawing a premise removes that premise as a basis for asserting the conclusion. Another sufficient argument may still support it. To assert the opposite conclusion, obtain a reason for that assertion. The conditional argument can remain available for situations in which its premises hold.

Follow the change through each needed use of a shared prerequisite. Keep the premises of an alternative argument together: pieces from two incompatible situations do not form a supported argument for either situation. If conclusions refer back to one another, recover the grounding of that reasoning, such as an initial case and induction step. Mutual repetition alone cannot replace the starting support.

A changed requested result can require working backward as well. Identify what the new conclusion would need, reuse the earlier contributions that supply it, and produce the remaining contribution. Release a former fixed value when the question now asks you to determine it.

Compare the work of recovering and repairing the affected reasoning with the work of obtaining a fresh sufficient answer. A short new calculation can be cheaper and clearer. A maintained dependency account is useful when repeated revisions repay its cost; it is optional for an ordinary one-off question.

### B.5.RR:4.4 - Choose the result the present reasoning supports {#choose-the-result-the-present-reasoning-supports}

Relate the revised conclusion to the result requested in §4.1. It may supply the requested answer, a conditional answer, a bound or an obstruction. Say what the receiver can do with that result.

For a mathematical argument, carry the domain and assumptions into its conclusion. For an empirical application, examine the changed observation or applicability premise using the relevant subject method. Recomputing a model can establish its new consequence while leaving its correspondence with the physical situation unresolved.

If the original target is unattainable under the retained conditions, use the obstruction to propose a changed condition or a different question. Keep that proposal visible as a choice. A weaker result can be useful without silently replacing the requested result.

Obtain further evidence or checking when its possible outcomes can change this use. C.11.DUA helps compare that contribution with its cost. The method can finish with an explicitly conditional result when conditional use is sufficient.

### B.5.RR:4.5 - Apply the result and carry the change to its users {#apply-the-result-and-carry-the-change-to-its-users}

Perform the receiving use, or give its next contributor the revised conclusion and the condition that governs it. When others rely on the earlier result, tell the affected users what changed and which application must change with it. Their unchanged uses need no new argument merely because a nearby result was revised.

Check the changed transition by the method appropriate to its claim. A small instance can reveal a substitution error; a proof establishes its stated general conclusion; an observation can test a physical consequence. Choose the check for the result actually being relied on.

Stop when the receiving question is answered at the required level, or when the remaining contribution has been located well enough to obtain it. A useful new question can begin another inquiry under B.5.

## B.5.RR:7 - Conformance Checklist {#conformance-checklist}

- The present question and the consequential change are stated.
- The reasoning used by the receiving conclusion is recoverable at the needed depth.
- Joint prerequisites, shared premises and sufficient alternatives are preserved.
- Affected transitions are reworked under their applicable inference or construction rules.
- The revised conclusion retains its domain, conditions and any unresolved premise.
- The receiver can identify the next action, useful stop or contribution still required.

## B.5.RR:9 - Consequences {#consequences}

The practitioner can change an application while retaining useful reasoning, or explain why a larger change is required. A failure can expose a missing condition, a different construction or a worthwhile next question.

Recovery costs attention and sometimes specialist help. Its value increases when the same reasoning must be adapted repeatedly or divided among contributors. A short independent solution may remain the better choice for one small question.

## B.5.RR:12 - Relations {#relations}

- **B.5** coordinates inquiry and the next useful question. **B.5.RA** recovers the argument; **B.5.RC** recovers a needed construction.
- **B.1.1** clarifies the represented dependency relation. **A.6.3.RT** helps when the expression prevents the revision operation.
- **B.5.MPC** connects physical, mathematical and computational contributions. **B.5.MPC.R** uses this reasoning revision to repair a failed connection.
- **B.3, B.3.3 and A.10** supply the claim-specific assurance and evidence conditions. **C.11.DUA** helps choose worthwhile additional checking or information.
- **C.39** develops a missing way of obtaining a result. Revision may supply the construction from which that work begins.


## Dependencies {#dependencies}

- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/B-5#root, spec://ai.lev/fpf-spec/contract/B-5-RA#root and spec://ai.lev/fpf-spec/contract/B-5-RC#root for reasoning, spec://ai.lev/fpf-spec/contract/B-5-MPC-R#root for joint physical reasoning, and spec://ai.lev/fpf-spec/contract/C-11-DUA#root for further effort. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-1-RI#root, spec://ai.lev/fpf-spec/contract/A-15-10#root, spec://ai.lev/fpf-spec/contract/A-6-3-RT-OE#root, spec://ai.lev/fpf-spec/contract/B-5-EA#root, spec://ai.lev/fpf-spec/contract/B-5-FM#root, spec://ai.lev/fpf-spec/contract/B-5-MPC-R#root, spec://ai.lev/fpf-spec/contract/B-5-QD#root, spec://ai.lev/fpf-spec/contract/B-5-TC#root, spec://ai.lev/fpf-spec/contract/B-5-TU#root, spec://ai.lev/fpf-spec/contract/C-16-RM#root, spec://ai.lev/fpf-spec/contract/C-28-MR#root, spec://ai.lev/fpf-spec/contract/C-39-RO#root, spec://ai.lev/fpf-think-mmp/contract/MMP-14#root, spec://ai.lev/fpf-think-mmp/contract/MMP-9#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/B-5-RR
