# C.11.DUA - Make Advice and Evidence Demands Worth Their Burden {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Tech name:** `DecisionUsefulAdvice`
>
> **Plain name:** make advice and evidence demands useful to the recipient's decision
>
> **Type:** C-pattern
>
> **Status:** Stable

## C.11.DUA:1 - Problem frame {#problem-frame}

**Use this when** a report, expert answer, review comment, rule or checklist asks somebody to act, wait, investigate or supply evidence, but it is unclear how that demand helps their present question or whether they can carry it out.

An engineer reports that a discharge criterion was below the incoming background level. A colleague wants help examining the criterion. A useful answer can attribute the report and distinguish total level from the operation's contribution. Requiring an archive search before making that distinction spends effort without improving that answer. If the colleague later wants to publish who imposed the criterion, the receiving question changes: a contemporary record may now be worth obtaining. The method below reaches a completed answer in both situations.

The broad activity is decision support through advice. This pattern addresses the branch in which advice turns uncertainty or a requirement into consequential work for its recipient. Its subject is the **advice statement or requirement being composed or examined**, including the action or inquiry it demands. An empirical claim, recommendation, method instruction and binding requirement retain their different meanings and force. The method recovers the demand, appraises it and returns a usable continuation.

**First useful result.** Give the supported answer or repaired advice, the continuation available to the recipient, and any limitation that changes its use. The result can be an explanation, recommendation, bounded inquiry, proposed requirement revision or an honest impasse. Ordinary prose is sufficient.

**Ordinary non-use boundary.** If the question, support and feasible answer are already clear, answer directly. Use `A.10` directly for a source-reliance question, `C.11` for an already adequate local choice, or `C.19.2` for economical application under an undisputed declaration. This composition adds value when somebody otherwise has to reconstruct the connection between those questions. Domain inference, experimental design, permission and enactment remain with their own methods and authorities.

## C.11.DUA:2 - Problem {#problem}

A limitation is often followed by a demand that does not follow from it. “This study cannot establish the effect” can be true while “therefore commission the ideal experiment before doing anything” is infeasible or inferior to a bounded action. Conversely, an inexpensive check may distinguish a damaging commitment from a useful alternative. Skipping it merely because the present answer is convenient repeats the same failure to compare consequences.

The difficulty starts before a well-formed option set. Advice such as “validate thoroughly” can hide an investigator, access requirement, delay, claimed guarantee and transfer of cost to somebody else. The recipient has to recover that work before choosing whether it is worthwhile.

A further failure appears at completion. A method may allow work to proceed without more inquiry yet require a probe block, waiver or explanation of every omitted check before accepting the answer. Producing that account is itself work. Sometimes a retained reason protects a later use; sometimes it adds nothing to the completed decision.

## C.11.DUA:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Truthful support and useful continuation | The present evidence may support a narrower answer than the requested one; scarce resources do not strengthen that evidence. |
| Inquiry and commitment | Information or computation can improve a choice, while delay, opportunity cost and investigation risk can worsen it. |
| Requirement merits and present force | A requirement may deserve revision while continuing to constrain what the recipient can presently do. |
| Immediate and later value | Operational action, explanatory progress, better models and future options can all matter at different horizons. |
| Protective contribution and distributed burden | A cheap measure for the issuer can be costly for its recipient or shift risk to another affected party. |
| Useful basis and unnecessary accounting | A decision needs its supporting basis; a record of an inactive check needs an actual receiving use. |

## C.11.DUA:4 - Solution {#solution}

Start from what the recipient is trying to settle. Recover the work hidden in the advice, compare what that work can change with what it costs, and give the best warranted continuation. Follow that continuation through the required result and stopping point.

### C.11.DUA:4.1 - Recover the receiving question and demanded work {#recover-the-receiving-question-and-demanded-work}

Identify the question the recipient needs answered and the horizon at which an improvement matters. Read an existing instruction as something somebody would actually have to perform: what would they believe, do, stop doing, postpone or spend if they followed it?

Recover a missing performer, resource, access, time condition or authority when it can change feasibility or the recommendation. An unavailable data set or a study that finishes after the decision window is a different option from an available timely check. Do not turn a simple answer into a universal plan form.

For a text review, examine the connected passage that creates the demand, including its steps, mandatory fields and completion clauses. “Consider further evidence” and “obtain it before proceeding” impose different work. A final template can impose work that the preceding prose made optional.

Keep three answers distinct:

| Receiving question | Useful answer | Governing contribution when needed |
| --- | --- | --- |
| What does the present basis support? | An attributed claim, supported conclusion and its use limit. | `A.10`; direct domain inference or `C.28` for a causal use. |
| What can the recipient reasonably do with that basis? | A feasible continuation, narrower use, reversible action, deferral or stop. | `C.11` for a local choice; `C.11.CRC` when the finite contribution comparison is missing. |
| What further inquiry could improve that use? | A worthwhile attainable check, or continuation with the present basis. | `C.11` for information or computation value; the direct subject method for the inquiry. |

These are questions to resolve where live, not three mandatory output fields. A source limitation qualifies the attempted claim. It does not by itself choose evidence acquisition.

### C.11.DUA:4.2 - Compare attainable inquiry with its receiving value {#compare-attainable-inquiry-with-its-receiving-value}

When an inquiry is proposed or a consequential uncertainty, anomaly or applicable requirement makes one live, identify a plausible result that would change the conclusion, choice or warranted use. Compare obtaining that result with the feasible alternatives. These may include using present knowledge, a smaller reversible step, a different source, a narrower claim, deferral or stopping.

Include the attainable inquiry's cost, delay, displaced work and downside. Compare what it adds to the present configuration and horizon; `C.11.CRC` supplies that missing comparison when needed. A large uncertainty is not sufficient reason for a large study. Ask how resolving it could improve this use. A cheap probe that can change an irreversible commitment deserves a different answer from an expensive check whose plausible results leave the useful answer unchanged.

Qualitative or ordinal judgement often suffices. A numerical value-of-information or computation model is useful when it improves the choice; do not demand probabilities or a common scalar merely to fill a form. If plausible differences in judgement could reverse an important recommendation, examine those differences at proportionate effort. Keep distinct consequences visible when a scalar would hide the trade-off.

An inquiry can be useful even if the physical action stays the same. It may establish which claim is warranted, meet an applicable evidence condition or make a proposed use admissible. Conversely, inability to obtain evidence does not make the stronger claim true or admissible.

For exploratory research, name the explanatory, model-building, hypothesis-discriminating or option-creating gain at the research horizon. A study can earn its cost through those gains before an operational intervention is selected. The direct research method must still connect its attainable observations to that gain.

### C.11.DUA:4.2.1 - Compare a proposed change with continuing the work {#compare-a-proposed-change-with-continuing-the-work}

For optional advice to change a way of working, include continuing without that change among the serious alternatives. A useful new contribution can be considered while the present work succeeds and its constraints remain unchanged. Recover what the recipient could gain, on which horizon, and what following the advice would require.

When the gain depends on a constituent action, use B.1.5.EW to recover the encompassing work performed through it, the contributions needed below it and the conditions that change its use. Use B.1.5.RS for a proposed replacement in those wholes. Include a second receiving whole or an intermediate connection while it can reverse the advice. Use an already adequate account directly.

Compare the full continuation: understanding and discussing the advice, obtaining support, learning, adaptation, coordination, execution and displaced work. Use C.11.CRC when the finite comparison or interactions are missing. If several changes compete for the same recipient capacity, compare their combined demand with ongoing commitments and changes already selected. Individually useful changes may require a smaller set, deferral or a different combination.

Keep deciding to think further, presenting advice, deciding to change and performing the change separate. Cheap computation can justify frequent consideration while interruption and transition costs justify infrequent advice or intervention. Consider timing and a smaller change when those alternatives matter. A change in performer capability or adaptation cost can justify reconsidering the encompassing way of working.

Use the available basis before asking the recipient for more work. Unclear benefit alone gives the recipient no obligation to prove an optional suggestion useless or fund an expensive evaluation. Obtain more information only when a plausible attainable answer can change a worthwhile continuation. If presenting the advice has no proportionate basis, continue without presenting it; no rejection record is required merely to finish. Preserve a reason or reconsideration condition only for a receiving use that needs it.

An existing obligation still constrains the available continuations. Examine its merits and possible revision through section 4.3 when that question is live.

### C.11.DUA:4.3 - Appraise a disputed requirement and its current force {#appraise-a-disputed-requirement-and-its-current-force}

When the requirement itself is in question, identify the quantity, activity or claim it governs and the problem it is meant to address. Examine its basis and uncertainty, threshold, protective contribution, burden and distribution of error costs. Include delay and displaced risks: reducing one named risk may increase another.

Compare retaining, tightening, relaxing or replacing the requirement only where these are meaningful alternatives. Resolve labels such as “safety” or “security” to the particular hazard, exposure, action or evidence condition. Apply the same proportionality question to the evidence demanded to justify the requirement itself.

A limit below background calls first for distinguishing the incoming background, the activity's attributable increment and the total resulting level. A total-exposure objective can justify reducing background too. Neither “below background” nor “required for safety” settles the merits without that contribution comparison.

Keep the merits judgement separate from the currently available action set. A binding requirement continues to govern until the relevant authority or agreement changes it. Advice can recommend a lawful exception, a revised criterion or another activity and identify the feasible route to that change. A hoped-for revision is not already available. If the current requirement makes the proposed action unavailable and no acceptable alternative or timely revision is feasible, state that impasse.

When applying apparatus under `C.19.2`, compare eligible applications under the current result, guarantee and constraints. A cheaper method that drops a required guarantee is a different proposal. Resume under a revised declaration only when that revision is available through its governing authority or agreement.

### C.11.DUA:4.4 - Return the advice through first useful completion {#return-the-advice-through-first-useful-completion}

Give the supported answer and available continuation in language the recipient can use. Retain uncertainty, attribution, a reason or a return condition when it changes that use. Where a substantive decision record is needed, put this content in the same result.

For an external-text review, return a concrete repair: identify the demanded work, the consequence or burden that makes it defective, and the smallest replacement that reaches a warranted result. Keep a useful evidence demand when the comparison supports it. A finding for another author can be durable without becoming a per-sentence ledger.

Follow the selected method through its completion requirements. Keep the recommendation or decision and its useful basis. An inactive inquiry creates no empty field, no waiver and no requirement to explain why checking was omitted. If a later recipient would otherwise overgeneralize the result, infer fresh evidence or miss a material limitation, retain the minimum explanation in that result. A short useful explanation alone need not instantiate a complete probe account.

Apply the same appraisal to any prescribed record. If it has binding force, distinguish its usefulness from what the current procedure requires and use the available revision route. This pattern does not manufacture permission to disregard it.

Finish when the recipient has the warranted answer and continuation for the present question, including a justified stop when necessary. Reopen when the receiving use, possible consequence, feasible means, source basis or information opportunity changes materially.

### C.11.DUA:4.5 - Keep recognition and assurance about the same advice {#keep-recognition-and-assurance-about-the-same-advice}

The opening and worked situations help the reader recognize a consequential demand and repair it. The checklist below tests that same advice and the work it demands. It does not introduce a separate admission record or require every use to undergo a new review.

Use `A.10` for the evidence boundary, `C.11` for a choice result, `D.4` for ethical mediation and the direct assurance method for a stronger guarantee when that question is live. Advice that a step is sensible supplies neither permission nor evidence that the step was performed.

## C.11.DUA:7 - Conformance Checklist {#conformance-checklist}

The following conditions concern the advice actually given. They require no separately completed checklist.

| ID | Condition |
| --- | --- |
| CC-C11DUA.1 | @fact:CC-C11DUA-1 The receiving question and the action, delay, expenditure or inquiry demanded by the advice are clear enough to judge their contribution. @status:spec/done |
| CC-C11DUA.2 | @fact:CC-C11DUA-2 The answer preserves what present evidence supports and its use boundary. Infeasible acquisition does not strengthen the claim. @status:spec/done |
| CC-C11DUA.3 | @fact:CC-C11DUA-3 A live inquiry is judged by its attainable contribution and relevant cost, delay, opportunity cost and downside. Useful qualitative comparison suffices. @status:spec/done |
| CC-C11DUA.4 | @fact:CC-C11DUA-4 When a requirement's merits are disputed, the appraisal addresses its governed quantity or activity, purpose, contribution and burden while keeping present force separate. @status:spec/done |
| CC-C11DUA.5 | @fact:CC-C11DUA-5 The result reaches the first useful completion for this recipient. Its decision and useful basis remain; inactive inquiry adds no placeholder, waiver or omission account. @status:spec/done |
| CC-C11DUA.6 | @fact:CC-C11DUA-6 Any reason or limitation needed by the decision or a later recipient remains in the same result. Changed use can make previously unnecessary inquiry worthwhile. @status:spec/done |
| CC-C11DUA.7 | @fact:CC-C11DUA-7 The stated continuation is feasible under obtaining conditions, or the answer identifies the actual impasse. Future authorization or evidence is not treated as obtained. @status:spec/done |
| CC-C11DUA.8 | @fact:CC-C11DUA-8 Domain inference, choice, ethical and assurance claims retain their direct methods. Explanatory and future-option gains are judged at their receiving horizon. @status:spec/done |

## C.11.DUA:9 - Consequences {#consequences}

Advice becomes a usable answer to a receiving question. The practitioner can continue with qualified knowledge, select worthwhile inquiry, repair a requirement proposal or recognize an impasse. A reviewer can repair an external report without requiring FPF-formatted input.

The method costs the attention needed to recover hidden work and compare its consequences. That cost is unnecessary for an already clear bounded answer. It also cannot make unavailable means available or settle domain evidence and authority questions by general reasoning alone.

## C.11.DUA:12 - Relations {#relations}

- **Uses:** `A.10` for source-reliance boundaries; `C.11` for local choice and probe-worthiness; `C.11.CRC` when a finite contribution comparison is missing; `C.19.2` for economical application under the current declaration.
- **Coordinates with:** `C.18` when useful options or hypotheses must be generated; `C.28` and direct domain methods when the advice depends on causal inference; `D.4` for ethical mediation; the applicable assurance method for a stronger guarantee.
- **Used by:** `F.19` when clear wording leaves a questionable substantive demand; `E.19` when advice usefulness, feasibility or evidence burden is the live review question; `E.11.PUA` when a pattern's demanded work obstructs its first useful result.
- **Leaves with their owners:** authorization, requirement enactment, domain research design, actual Work and its evidence. The recommendation supplies a reasoned continuation; those contributions determine whether and how it can be carried out.


## Dependencies {#dependencies}

- @fact:USES Uses: spec://ai.lev/fpf-spec/contract/A-10#root, spec://ai.lev/fpf-spec/contract/C-11#root, spec://ai.lev/fpf-spec/contract/C-11-CRC#root, spec://ai.lev/fpf-spec/contract/C-19-2#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/C-18#root, spec://ai.lev/fpf-spec/contract/C-28#root, spec://ai.lev/fpf-spec/contract/D-4#root and domain methods. @status:spec/done
- @fact:USED-BY Used by: spec://ai.lev/fpf-spec/contract/F-19#root, spec://ai.lev/fpf-spec/contract/E-19#root, spec://ai.lev/fpf-spec/contract/E-11-PUA#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-1-CSD#root, spec://ai.lev/fpf-spec/contract/A-1-RI#root, spec://ai.lev/fpf-spec/contract/A-11-OP#root, spec://ai.lev/fpf-spec/contract/A-15-10#root, spec://ai.lev/fpf-spec/contract/A-15-11#root, spec://ai.lev/fpf-spec/contract/A-15-9#root, spec://ai.lev/fpf-spec/contract/A-3-3-PI#root, spec://ai.lev/fpf-spec/contract/A-3-3-TR#root, spec://ai.lev/fpf-spec/contract/B-1-5-RS#root, spec://ai.lev/fpf-spec/contract/B-5-EA#root, spec://ai.lev/fpf-spec/contract/B-5-PI#root, spec://ai.lev/fpf-spec/contract/B-5-QD#root, spec://ai.lev/fpf-spec/contract/B-5-QD-CF#root, spec://ai.lev/fpf-spec/contract/B-5-RR#root, spec://ai.lev/fpf-spec/contract/B-5-TC#root, spec://ai.lev/fpf-spec/contract/C-11#root, spec://ai.lev/fpf-spec/contract/C-16-IR#root, spec://ai.lev/fpf-spec/contract/C-16-MR#root, spec://ai.lev/fpf-spec/contract/C-16-RM#root, spec://ai.lev/fpf-spec/contract/C-28-CM#root, spec://ai.lev/fpf-spec/contract/C-29-BB#root, spec://ai.lev/fpf-spec/contract/C-40-CD#root, spec://ai.lev/fpf-eng-cgov/contract/CGOV-15#root, spec://ai.lev/fpf-think-cmp/contract/CMP-7#root, spec://ai.lev/fpf-spec/contract/D-1#root, spec://ai.lev/fpf-eng-eam/contract/EAM-14#root, spec://ai.lev/fpf-eng-eam/contract/EAM-15#root, spec://ai.lev/fpf-eng-fin/contract/FIN-1#root, spec://ai.lev/fpf-eng-fin/contract/FIN-16#root, spec://ai.lev/fpf-eng-fin/contract/FIN-18#root, spec://ai.lev/fpf-eng-fin/contract/FIN-20#root, spec://ai.lev/fpf-eng-me/contract/ME-25#root, spec://ai.lev/fpf-think-mmp/contract/MMP-14#root, spec://ai.lev/fpf-think-mmp/contract/MMP-16#root, spec://ai.lev/fpf-eng-mnt/contract/MNT-2#root, spec://ai.lev/fpf-eng-mnt/contract/MNT-6#root, spec://ai.lev/fpf-eng-str/contract/STR-10#root, spec://ai.lev/fpf-eng-str/contract/STR-7#root, spec://ai.lev/fpf-eng-syse/contract/SYSE-9#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/C-11-DUA
