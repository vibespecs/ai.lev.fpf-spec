# A.11.OP - Decision-Relevant Least Action and Operational Parsimony: Test a Proposed Requirement {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Part A pragmatic principle pattern
> **Class:** `Prag`
> **Status:** Stable
> **Normativity:** Normative unless marked informative

**Plain name.** Keep only work that changes a substantive choice or result, or protects a condition on which the use relies.

**Primary reader.** A practitioner or designer deciding whether one proposed action or supporting apparatus should be mandatory.

## A.11.OP:1 - Problem frame {#problem-frame}

**Use this when.** Use this pattern when someone proposes making an action or apparatus mandatory and a plausible question remains: does this requirement change the subject work, or does it only make the route look controlled?

The primary `EntityOfConcern` is one proposed mandatory requirement under one declared use and one substantive horizon. The pattern screens the requirement for a substantive contribution. A contribution is necessary, but does not alone make the work obtainable, worthwhile or obligatory; *action*, *apparatus*, *requirement*, and *horizon* keep their ordinary meanings.

**First useful result.** Return one of two short answers:

- retain the requirement for this use and horizon because it has a named substantive contribution and its direct choice, realization, assurance or authority basis justifies requiring the work; or
- remove the requirement or leave it optional because it has no such contribution, or because a contribution does not justify its burden for this use.

For a proposed inquiry whose worth is still open, use `C.11.DUA` to compare what can be gained with feasible effort, delay, opportunity cost and downside; use `C.11` when a current chooser and options need a local choice. Finish with the supported answer and feasible continuation, which may retain the current action, narrow a claim or decline an unsupported use.

Ordinary use needs no score or separate record. Name the receiving decision, result, reliance, or recovery condition in the same sentence as the disposition.

**Three recognition cases.**

- A team has added a second status update before a repair decision. Every possible status leaves the same repair action, and no later user relies on the duplicate update.
- A laboratory considers a bounded probe that leaves today's setup unchanged but can determine which of two methods will be used next week.
- A release route contains both a deterministic build step that creates the selected publication and an assurance check whose evidence is consumed by the release decision.

These are one recurring problem across unlike situations: mandatory effort can be ceremonial, immediately productive, decision-relevant only later, or necessary because another use relies on the assurance or recovery condition it preserves.

**What goes wrong if missed.** Requirements accumulate because each sounds prudent in isolation, while their possible results change no substantive choice and produce no selected result. The opposite error removes exploration, deterministic realization, safety evidence, recovery support, or a small discriminating cue merely because it does not change the next administrative state.

**What this buys.** The practitioner can remove ceremony without treating the fewest steps as the goal. Useful exploration, realization work, assurance, option preservation, and recovery remain when their receiving use is named.

**Not this pattern when.**

- When the question is the force or applicability of an instituted obligation, use its direct authority. Apply A.11.OP only to discretionary apparatus inside the space it leaves. If the present question concerns the obligation's merits, use `C.11.DUA` to examine its protective contribution, burden and feasible amendment; that appraisal does not cancel its current force.
- When several already qualifying alternatives need comparison, use their direct choice, apparatus, architecture, or Method Engineering pattern.
- When the question is whether a new durable ontology value should exist, use `A.11`.
- When the question is how to use an already selected pattern, use `E.11.PUA` or `E.11.PUR`.
- When ongoing Work needs one next action chosen from current facts, use `A.15.7`.
- When an available direct-kind apparatus is already being configured for a declared use, use `C.19.2` for that application question.

## A.11.OP:2 - Problem {#problem}

Methods and their administrative or support arrangements can accumulate apparatus, such as duplicate reads, checks, and handoffs. Each addition can be defended by a possible future benefit. If hypothetical usefulness is enough, every requirement survives. Attention and elapsed time then move from the subject result to the route's own states and receipts.

Simple minimization fails in the other direction. A deterministic assembly step may have no rival outcome yet still create the selected result. A decision maker may use new information to change a later policy while leaving the immediate action unchanged. A safety check may return the expected result while supplying evidence on which release reliance depends. A practitioner may use a recovery cue to avoid continuing from the wrong place. Counting branches, steps, documents, or minutes does not distinguish those cases.

The problem is therefore not how to minimize action in general. It is how to admit one proposed mandatory requirement only when a materially plausible difference reaches a named substantive use, without weakening the direct authority that governs the action.

## A.11.OP:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Economy versus result production | Removing ceremony saves effort, but a deterministic action can be the work that realizes the selected result. |
| Immediate economy versus delayed information value | A probe can leave the next action unchanged while changing a later decision inside the relevant horizon. |
| Light use versus assurance | Ordinary decisions should stay conversational, but a relied-on exposure, release, rollback, or recovery condition may need evidence. |
| Local closure versus open-world reuse | A declared horizon makes action possible; unspecified future reuse cannot justify every precaution. |
| Parsimony versus authority | A burden screen can expose ceremony, but it cannot override law, regulation, Guard-Rails, assurance floors, or direct duties. |
| One general rule versus direct owners | The recurring admission question should be easy to find, while Method, choice, apparatus, evidence, assurance, and Work claims retain their own patterns. |
| Plain guidance versus theory laundering | Use epistemic and counterfactual distinctions without importing a universal engineering objective from free-energy or physical least-action formalisms. |

## A.11.OP:4 - Solution {#solution}

Apply one bounded admission question before making the proposed action or apparatus mandatory.

> **Admission rule.** An author or method designer **MUST NOT** make a proposed action or apparatus mandatory unless at least one materially plausible result can change a named substantive decision or branch within the declared horizon, the action realizes an already selected transformation or required subject result, or removing it changes a named assurance or recoverability condition on which the declared use relies.

Passing one branch establishes only a substantive contribution for this use and horizon. It does not establish that the work can be obtained or is worth requiring. Complete any live worth or choice question through its direct owner before selecting the requirement.

### A.11.OP:4.1 - Name the use and nearest substantive horizon {#name-the-use-and-nearest-substantive-horizon}

1. Name the proposed requirement and the declared use for which mandatory status is being considered.
2. End the horizon at the nearest named substantive decision, receiving use, selected transformation result, assurance use, or recovery use that can justify the requirement.
3. Name the possible result or removal consequence that reaches that horizon. Do not use the requirement's own status, completion flag, receipt, or other administrative transition as its receiver.

The nearest substantive horizon is not necessarily the next event. It may include a later decision when the dependency from the present result to that decision is stated. End it before any further use whose receiver and dependency have not been named.

### A.11.OP:4.2 - Compare keeping and removing through three branches {#compare-keeping-and-removing-through-three-branches}

| Admission branch | Passing condition | Boundary of the result |
| --- | --- | --- |
| **Decision-changing result** | At least one materially plausible result changes a named subject branch or selection among named alternatives inside the horizon. An information-gathering action passes when one of its possible results changes a later policy even if the immediate action stays the same. | The passing basis is the result-to-decision dependency. Obtainability, expected contribution after uncertainty, burden and eventual choice remain open. |
| **Selected realization** | The action performs a required part of an already selected transformation or obtains the required subject result. A deterministic step needs no fabricated rival outcomes. | This branch establishes the action's contribution to the selected result; it presupposes selection and leaves feasibility, authorization, actual Work, and result status to their direct owners. |
| **Assurance or recoverability preservation** | Removing the action changes a named assurance or recoverability condition on which the declared use relies. | This branch preserves that condition; its required level and evidential basis come from the direct assurance or recovery owner. |

Compare the concrete situation with and without the requirement. A passing branch removes the objection that the work contributes nothing. Retain it only as far as its direct basis justifies requiring it. An already selected transformation or established reliance can supply that basis without another comparison.

When a proposed inquiry could matter but its worth remains open, apply `C.11.DUA` to the actual demand and receiving question. Identify the attainable observation, what it could change, and its whole cost within the receiving horizon. Compare available continuations through `C.11` when a local choice is needed. A useful possible result can still arrive too late, require unavailable means, or cost more than its contribution. Keep the presently supported answer or select a feasible alternative under its actual limits. Do not invent an OptionSet or an inquiry merely to certify that none is needed.

If no branch passes, remove the requirement or leave it as an optional convenience. Convenience and prior investment do not supply the missing receiving difference.

### A.11.OP:4.3 - Judge material plausibility through the subject claim {#judge-material-plausibility-through-the-subject-claim}

*Materially plausible* means more than logical possibility and less than certainty. The direct owner of the claimed consequence supplies its standard of evidence. A low-probability result can remain material when its consequence changes exposure or the admissible policy. A large information volume is material only when some possible result changes a named receiving use.

When the branches cannot be distinguished, name the exact claim and missing basis and return them to that claim's direct owner. Keep the qualified answer already supported. A bounded experiment is one possible continuation only when an attainable result and worthwhile contribution justify its whole burden under §4.2. Unresolved usefulness alone does not select an experiment or create permanent mandatory status.

### A.11.OP:4.4 - Return authority and claims to their direct owners {#return-authority-and-claims-to-their-direct-owners}

Apply this screen only inside the space left by every applicable direct authority. The direct owner establishes the obligation or floor and resolves disputes about its basis or applicability.

When the requirement itself is being appraised, use `C.11.DUA` to compare the protected bearer and interest, the threshold and horizon, the causal contribution claimed, and who bears the burden. Identify who can amend the requirement and whether that amendment is feasible in time. Keep its merits and present force distinct: neither a protective label nor a burdensome rule settles the merits, and an unfavorable appraisal supplies no unilateral waiver. The legal, ethical and domain claims remain with their direct owners.

A passing branch establishes only the named contribution. Every downstream claim remains with the direct pattern named in Relations; obtain the required result by value instead of treating this screen as its substitute.

### A.11.OP:4.5 - Keep the result light and reopenable {#keep-the-result-light-and-reopenable}

For ordinary use, say:

> Keep `<requirement>` for `<declared use>` until `<nearest substantive horizon>` because `<named contribution and the basis for requiring this work>`.

or:

> Remove or demote `<requirement>` for `<declared use>` because keeping and removing it produce the same substantive decision and result and change no relied-on assurance or recovery condition.

If a proposed inquiry has a contribution but is unavailable or not worthwhile, finish with the current supported answer and selected continuation. Keep a short reason or limitation in that result when the recipient needs it; add no empty probe fields or separate omission account.

A named later use that must cite, compare, audit, or rely on the disposition records it in the existing record kind appropriate to that use. Otherwise the one-sentence result is complete.

Reopen the disposition when the horizon, plausible results, selected transformation, direct duty, assurance floor, recovery reliance, or burden-bearing alternative changes.

### A.11.OP:4.6 - Keep framework layers distinct {#keep-framework-layers-distinct}

FPF owns this cross-domain admission principle. A Method Engineering DPF may use it when deciding which requirements should be mandatory in a named Method situation; that DPF still owns the Method-specific design. A local practice framework may bind the principle to its own execution and assurance mechanisms. Those mechanisms retain local scope, and the FPF admission condition must still be established for the declared use.

## A.11.OP:7 - Conformance Checklist {#conformance-checklist}

| Check | Passing condition |
| --- | --- |
| `CC-A11.OP-1` Governed requirement | @fact:CC-A11-OP-1 One proposed mandatory requirement, one declared use, and one nearest substantive horizon are recognizable. @status:spec/done |
| `CC-A11.OP-2` Substantive receiver | @fact:CC-A11-OP-2 The justification reaches a named subject decision, receiving use, selected result, assurance use, or recovery use; the requirement's own route state is not its receiver. @status:spec/done |
| `CC-A11.OP-3` Three-branch comparison | @fact:CC-A11-OP-3 Keeping and removing the requirement have been compared through decision-changing result, selected realization, and assurance or recoverability preservation. @status:spec/done |
| `CC-A11.OP-4` Material plausibility | @fact:CC-A11-OP-4 Each claimed difference has the basis appropriate to its subject, evidence, risk, causal, decision, or assurance claim; bare logical possibility and information volume are insufficient. @status:spec/done |
| `CC-A11.OP-5` Deterministic realization | @fact:CC-A11-OP-5 A required deterministic step is retained when it realizes the already selected result without fabricated outcome branches. @status:spec/done |
| `CC-A11.OP-6` Delayed decision value | @fact:CC-A11-OP-6 For an inquiry proposed for a later decision or reliance, at least one materially plausible result reaches that named use inside the horizon. This contribution is not sufficient to require acquisition; a live inquiry decision also establishes obtainability and worthwhile contribution under its direct owner. @status:spec/done |
| `CC-A11.OP-7` Assurance boundary | @fact:CC-A11-OP-7 A retained assurance or recovery action names the relied-on condition and its direct owner; that owner establishes the floor and evidential basis. @status:spec/done |
| `CC-A11.OP-8` Disposition boundary | @fact:CC-A11-OP-8 Passing a branch establishes contribution only. The final disposition uses the applicable choice, realization, assurance or authority basis; appraisal of a requirement's merits remains separate from its current force. @status:spec/done |
| `CC-A11.OP-9` Light result | @fact:CC-A11-OP-9 Ordinary use ends in the direct one-sentence disposition; a durable result uses an existing record kind required by a named later use. @status:spec/done |
| `CC-A11.OP-10` Direct-owner return | @fact:CC-A11-OP-10 Each downstream claim remains with the direct pattern named in Relations and is obtained from that pattern by value. @status:spec/done |
| `CC-A11.OP-11` Reopen condition | @fact:CC-A11-OP-11 The disposition names or makes recoverable which change in horizon, result, transformation, duty, reliance, or alternative can reopen it. @status:spec/done |
| `CC-A11.OP-12` Theory boundary | @fact:CC-A11-OP-12 Epistemic value and a counterfactual horizon may inform the comparison. Expected free energy, variational free energy, and Hamiltonian least action do not supply a universal engineering admission rule. @status:spec/done |

## A.11.OP:9 - Consequences {#consequences}

The pattern changes practice before a requirement is installed. A designer names the receiving horizon and checks what keeping or removing the requirement changes. Duplicate status work becomes removable without making “less paperwork” a universal argument. Deterministic transformations remain because they produce the selected result. Exploration, assurance, recovery, and small cues have a substantive reason to remain when their delayed or relied-on consequence is explicit. Their direct basis determines whether to require them; a relevant but excessive inquiry can give way to a qualified current answer.

| Benefit | Cost or boundary |
| --- | --- |
| Mandatory effort is tied to a decision, result, reliance, or recovery use. | The designer must name that receiving use instead of appealing to generic prudence. |
| Immediate and delayed value are distinguished without a universal calculation. | Material plausibility still depends on the applicable subject, evidence, risk, or assurance basis. |
| Ordinary application stays conversational. | Consequential or disputed use may need an existing claim-bearing episteme for its relying consumer. |
| Direct owners remain intact. | The screen decides only whether the requirement is non-ceremonial for the declared use and horizon. |
| Local closures can remove speculative work and still reopen. | A changed horizon, duty, result, reliance, or alternative can legitimately reverse the earlier disposition. |

## A.11.OP:12 - Relations {#relations}

- **Classified by:** `E.3` as one `Prag` principle. It primarily advances P-1 Cognitive Elegance, P-7 Pragmatic Utility, P-10 Open-Ended Evolution, and P-11 State-of-the-Art Alignment while respecting the other Pillars.
- **Coordinates with:** `A.11`, which governs admission of ontology additions. Namespace adjacency makes the two parsimony questions discoverable; their EntitiesOfConcern remain distinct.
- **Coordinates with:** `E.11.PUA` and `E.11.PUR`, which govern use, recommendation, coordination, and reuse after a pattern has been selected. A.11.OP asks whether an extra mandatory requirement belongs in the first place.
- **Coordinates with:** `C.11.DUA` for the merits and feasible continuation of an advice or evidence demand, including a single requirement with no live OptionSet; `C.11` for a current local choice and probe-worthiness; and `C.19.2`, `A.19`, and Method Engineering for their apparatus, architecture or Method comparisons. A.11.OP supplies the contribution screen. These direct owners complete the applicable demand, selection or configuration question.
- **Coordinates with:** `E.13` for proxy-to-value repair and `E.23` for operations inside repeated evaluated improvement. A.11.OP retains the initial action-admission question.
- **Coordinates with:** `A.3.1` and `A.3.2` for Method and MethodDescription identity, `A.15.1` for dated Work, and `A.15.7` for next-action choice during ongoing Work. A.11.OP governs design-time admission of the requirement.
- **Constrained by:** applicable law and regulation, `E.5` Guard-Rails, `A.10` reliance boundaries, `B.3` assurance floors, and any other direct subject or authority pattern for the use.
- **Consumed by:** Method Engineering and other DPFs when they decide whether domain-specific requirements or support apparatus deserve mandatory status. Those frameworks retain their domain decisions and evidence.
- **May be specialized by:** local practice frameworks for concrete execution and assurance. Their local arrangements remain local rather than FPF authority.


## Dependencies {#dependencies}

- @fact:COMPANION-TO Companion to: spec://ai.lev/fpf-spec/contract/A-11#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/C-11-DUA#root, spec://ai.lev/fpf-spec/contract/C-11#root, spec://ai.lev/fpf-spec/contract/E-11-PUA#root, spec://ai.lev/fpf-spec/contract/E-11-PUR#root, spec://ai.lev/fpf-spec/contract/C-19-2#root, spec://ai.lev/fpf-spec/contract/E-13#root, spec://ai.lev/fpf-spec/contract/E-23#root, and the direct Method, Work, reliance, assurance, and authority owners named in its Relations. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-eng-ops/contract/OPS-12#root, spec://ai.lev/fpf-eng-ops/contract/OPS-14#root, spec://ai.lev/fpf-eng-ops/contract/OPS-15#root, spec://ai.lev/fpf-eng-ops/contract/OPS-17#root, spec://ai.lev/fpf-eng-ops/contract/OPS-18#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/A-11-OP
