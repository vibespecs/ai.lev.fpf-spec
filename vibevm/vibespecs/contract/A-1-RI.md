# A.1.RI - Reidentifying an Object across Observations {#root}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method pattern
> **Status:** Draft
> **Normativity:** Normative

## A.1.RI:1 - Problem frame {#problem-frame}

Use this pattern when the next calculation or action depends on whether observations concern the same continuing object, and the available identification does not yet settle that question. A moving object appears again after an observation gap. Two tracks compete for one detection. A process number appears in reports made before and after a restart.

The subject practice supplies what counts as continuation of that object: permitted motion, a process lifetime, a material continuity rule or another applicable criterion. The Method constructs and compares the connections that the observations and those rules allow.

**First useful move.** Name the object whose continuation matters and the use that depends on it. Then examine one available observation for a feature that distinguishes continuation from a live competing account. For a process run, a changed start time can settle a question that an unchanged process number leaves open.

The result is an identification or exclusion supported by the available premises, or the remaining alternatives relevant to the next use. It can be conditional on a stated motion or observation account. An adequate existing identification can be used directly.

This Method assumes that the object-continuation criterion and the relevant subject rules can be recovered. Constructing a new criterion, motion theory, sensor model or tracking algorithm is further work when one of those contributions is missing. A question about an aggregate quantity may be answerable without deciding which observation belongs to which object.

## A.1.RI:2 - Problem {#problem}

Observations describe what was found at particular occasions and under particular conditions. They can differ while concerning one object, or resemble one another while concerning different objects. A repeated name, location or appearance therefore has the identifying force supplied by the subject rules and observation conditions.

Pairwise plausible connections can also conflict. Under a model in which each object is detected once, assigning the same later detection to two earlier objects fails the joint account. Conversely, several complete associations may all satisfy the available constraints.

The practitioner needs to determine what the observations actually resolve and carry that result into the next calculation or action.

## A.1.RI:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Continuation and change | An object can change while continuing; the relevant criterion determines which changes matter. |
| Local resemblance and joint compatibility | A good pairwise match can prevent a coherent association of the other observations. |
| Observation gaps and available rules | Rules can connect separated observations while leaving more than one connection possible. |
| Ranked choice and resolved identification | A preferred hypothesis may support an action even when the observations have not excluded its rivals. |
| Information and cost | Another observation can distinguish alternatives, but the receiving use may already be possible. |
| General Method and subject construction | The association procedure is reusable; its motion, lifetime and observation rules are subject-specific. |

## A.1.RI:4 - Solution {#solution}

Recover the continuation question, construct the relevant associations under the subject rules, test their joint compatibility and use the distinctions they actually support.

**Name the continuing object → recover observations and rules → construct competing connections → test them together → resolve what the use needs → continue or reopen.**

### A.1.RI:4.1 - Recover the continuation question {#recover-the-continuation-question}

State which object the observations may concern and what would count as its continuation through the interval or change. A continuing software service, one process run and one execution of a requested job have different boundaries. Choose the object required by the question.

Recover the relevant temporal and contextual scope. Coordinates need a frame; a local process number needs the system and naming scope in which it was issued. If the observations use different references, establish their correspondence before comparing values.

State the receiving use. Estimating one object's displacement needs its association across observations. Estimating the mean position of a fixed observed population can leave those associations unresolved.

### A.1.RI:4.2 - Separate observations, rules and assumptions {#separate-observations-rules-and-assumptions}

Recover the observations already available, their occasions and the limitations that matter to this question. Distinguish the observed indication from a position, identity or event inferred through it. C.16.MR and C.16.IR help when the measurement interpretation itself remains unresolved.

Recover the subject rules used to connect those observations: allowed changes, motion bounds, lifecycle events or other continuity conditions. Include the observation conditions needed by the connection. “Each object was observed once” and “the set of objects stayed fixed” are substantive premises when they make the association one-to-one.

Keep an assumed rule available as an assumption. A conclusion derived under it can be useful while a later question requires a different or better-supported account. Use the assurance and information work appropriate to that receiving question.

### A.1.RI:4.3 - Construct the materially different connections {#construct-the-materially-different-connections}

Construct the associations still possible under the available account. A connection states which observations concern the continuing object and how the subject rules permit the intervening change. In a small finite case, listing the alternatives can be enough. Larger cases can use the domain's assignment, constraint or probabilistic Methods.

Include a missed observation, new object, ended object or reused identifier when the observed situation and subject rules make that alternative live. For example, a process can terminate between reports and its number can later be reused. A fixed two-object motion exercise can instead supply persistence and complete detection as premises.

When several objects share observations, construct complete associations for the relevant group. Retain the conditions linking their choices. For independent point motions a pair of admissible paths may suffice; interacting bodies can require a joint evolution satisfying their interactions.

### A.1.RI:4.4 - Test compatibility and the strength of the conclusion {#test-compatibility-and-the-strength-of-the-conclusion}

Apply the subject constraints to each materially different connection. Construct a permitted realization where feasibility matters, or identify a violated condition that excludes it. A numerical solver can help perform this step; its returned result still needs the intended observation and subject interpretation.

Compare the surviving alternatives at the distinction required by the receiving use:

- When the supported premises and considered alternatives determine the association, use that conditional identification.
- When they exclude a proposed association, remove it from the current account.
- When materially different associations remain, retain the unresolved distinction.
- When none fits, inspect the failed observation, rule or assumption before extending the same account.

A best score answers the ranking question defined by that score. If the work uses the top-ranked association provisionally, carry its selection rule and relevant uncertainty into that use. Claiming that the observations uniquely determine it requires the corresponding exclusion of alternatives.

The strength of the identifying judgment changes with its basis.

### A.1.RI:4.5 - Resolve only the distinction the next use needs {#resolve-only-the-distinction-the-next-use-needs}

Try the receiving calculation or decision on the surviving alternatives. If each gives the needed result, continue with that result and leave the unused identity question open. Section :5.1 obtains the same mean position under both surviving associations.

If the difference changes the next action, determine which available fact, observation or subject constraint would distinguish the alternatives. Prefer an already available discriminator. Obtain more information when its likely contribution warrants its cost and delay; C.11.DUA supplies that choice.

Some work permits a provisional action with the unresolved risk. State what that action assumes and what observation would call for correction. Work that requires the identity to be settled must return to the missing identifying contribution. An unresolved identification need not stop other work whose result is unaffected.

### A.1.RI:4.6 - Carry the result into use and revise it locally {#carry-the-result-into-use-and-revise-it-locally}

Use the association to join the relevant observations, calculate the change or address the continuing object. Keep the premises and unresolved alternatives that can change that use.

Reopen the affected connection when a new observation, changed rule or detected observation error invalidates it. Preserve associations and calculations whose basis still holds. B.5.RR helps carry a changed premise through dependent reasoning.

The observations retain their own occasions and claims after their subject is identified. C.2.1 governs observation epistemes and their identities. For a use that needs a separately designated relation occurrence, apply A.6.REL using the direct relation pattern's predicate and occurrence-identity rule.

## A.1.RI:7 - Conformance Checklist {#conformance-checklist}

- @fact:CC-RI-1 **CC-RI-1 - Continuing object.** The subject and its applicable continuation criterion are clear enough for the requested identification. @status:spec/work
- @fact:CC-RI-2 **CC-RI-2 - Observation basis.** Occasions, references and consequential limitations are distinguished from inferred identities. @status:spec/work
- @fact:CC-RI-3 **CC-RI-3 - Subject premises.** Allowed changes and observation conditions support the associations being considered. @status:spec/work
- @fact:CC-RI-4 **CC-RI-4 - Joint construction.** Connections that share observations or subject constraints are tested together. @status:spec/work
- @fact:CC-RI-5 **CC-RI-5 - Supported result.** The conclusion distinguishes a resolved association, exclusion, retained alternatives and an account that fits none. @status:spec/work
- @fact:CC-RI-6 **CC-RI-6 - Affordable continuation.** Additional information is sought when resolving the difference can change the receiving use enough to justify its attainable cost and delay. @status:spec/work
- @fact:CC-RI-7 **CC-RI-7 - Local revision.** Changed observations or premises reopen their dependent connections and results. @status:spec/work

## A.1.RI:9 - Consequences {#consequences}

The practitioner can join observations through an explicit subject construction, distinguish what has been resolved from what remains assumed, and continue calculations that are unaffected by remaining alternatives. A changed premise has a recoverable effect on the identifying result.

The Method depends on the coverage and quality of the available subject account. Constructing and comparing many alternatives can become expensive; domain algorithms and the receiving decision determine how much of that work is worthwhile.

## A.1.RI:12 - Relations {#relations}

- **A.1** supplies general individuation; **A.1.SCR** can consume an identity result when system recognition is the next question.
- **C.2.1** distinguishes observation-episteme identities and the object they concern.
- **C.16.MR and C.16.IR** construct and interpret the measurement relation when indication meanings affect association.
- **A.3.3.TR and A.3.3.PI** construct permitted continuations and retain the information needed to predict them.
- **B.5.TU and B.5.TC** construct a working theory use and compare accounts when the identifying premises need that work.
- **B.5.RR** revises reasoning affected by a changed observation or premise.
- **C.11.DUA** selects worthwhile information work for the receiving decision.
- **A.6.REL** supplies occurrence individuation when a later use specifically needs a designated identifying relation.


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/A-1#root, spec://ai.lev/fpf-spec/contract/C-2-1#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/A-3-3-TR#root, spec://ai.lev/fpf-spec/contract/A-3-3-PI#root, spec://ai.lev/fpf-spec/contract/C-16-MR#root, spec://ai.lev/fpf-spec/contract/C-16-IR#root, spec://ai.lev/fpf-spec/contract/B-5-TU#root, spec://ai.lev/fpf-spec/contract/B-5-TC#root, spec://ai.lev/fpf-spec/contract/B-5-RR#root, spec://ai.lev/fpf-spec/contract/C-11-DUA#root. @status:spec/done

#source spec://ai.lev/fpf-spec/source/A-1-RI
