# E.10.ROLE - Recovering What “Role” Means in the Current Claim {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Lexical and ontological precision restoration (E)
>
> **Status:** Stable
>
> **Plain name:** Recover what “role” means here

## E.10.ROLE:0 - Use This When {#use-this-when}

Use this pattern when claim-bearing wording uses *role* and the current sentence does not yet reveal which object or relation it means.

> A **system role** is a context-local kind for an entity already admitted under A.1 as a `U.System`, which may be a person, team, organization, or non-human technical object. The name creates no admission, assignment, agency, capability, or Work.

A **system-role assignment** is one exact occurrence under `U.SystemRoleAssignment`. The bare word *role* identifies neither object.

**First useful result.** Rewrite the ordinary domain sentence so that its recognizable object and action or relation are explicit. Select the pattern for that object or relation. Stop there unless the receiving claim needs a technical designation, exact occurrence, predicate, assertion, or reference.

For example:

- “Alice is reviewer” may remain ordinary recognition prose;
- “Alice holds the review assignment for this manuscript” makes an assignment claim current;
- “the report plays a role in approval” normally needs an evidence-use, source-use, reliance, or other direct relation, not a system-role assignment;
- “the first role in this tuple” normally points to a representation position, not a system-role kind.

**Not this pattern when.** Keep ordinary or quoted wording unchanged when no FPF claim relies on the word. When the object and its direct pattern are already clear, use that pattern directly. Use `A.6.RSIR` when the unresolved question is specifically about participation in a direct relation, a relation declaration, an interface, or a representation position.

`ROLE` remains in this PatternID because it is the ambiguous source word that opens this recovery. It is not a Tech designation for one governed object and is not a naming precedent.

## E.10.ROLE:1 - Problem Frame {#problem-frame}

Readers meet *role* in organizational, engineering, mathematical, software, documentary, and ordinary language. The same spelling may point to a local classification of systems, one assignment occurrence, participation in a relation, a declaration slot, a position in a representation or organization, functioning, capability, Work, authority, responsibility, use of an episteme, or no technical claim at all.

One remote definition cannot make the word safe in every sentence. Replacing every occurrence with `SystemRole` is also wrong: it would turn unrelated participation, slot, representation, evidence, and ordinary-language claims into a new ontology.

## E.10.ROLE:2 - Problem {#problem}

A cold reader needs to answer two questions at the point of use:

1. What exact object or relation does this sentence claim?
2. What useful action or conclusion depends on making that distinction?

If the text answers neither question, a fluent rewrite can preserve the word while changing the claim. A mechanical replacement can be even worse: it can assign a report, schema field, relation participant, or diagram position to a system-role kind that was never intended.

## E.10.ROLE:3 - Forces {#forces}

| Force | Tension |
|---|---|
| Natural wording vs technical identity | Practitioners need short sentences, while a later claim may need one exact kind, assignment, relation, or declaration. |
| Familiar word vs many neighboring objects | The word aids recognition but cannot select one ontology by itself. |
| Direct routing vs duplicate ontology | The entry must find the right pattern without copying that pattern's rules. |
| Precise distinction vs modifier stacking | Add `system`, `kind`, `assignment`, or another qualifier only when it distinguishes a live alternative. |
| One check vs procedural burden | Recover the claim once; do not create a form or ledger for a clean local repair. |

## E.10.ROLE:4 - Solution {#solution}

Use the sentence's intended claim, not the trigger word, to select the result.

1. Quote or locate the bounded phrase only when its source identity matters.
2. Write the ordinary sentence the reader should understand, naming the recognizable object and action or relation.
3. Select one branch below from that recovered claim. The examples are non-exhaustive; they illustrate result families and do not define a new role taxonomy.
4. Apply the selected pattern only as far as the receiving claim needs. Add a Tech designation, occurrence identity, predicate, assertion, reference, evidence, or assurance only when omitting it would change truth, action, reuse, or reliance.
5. For one recovered claim, stop when one exact object or relation and its pattern are selected, or return the exact `missing-governor`, missing-information, quote-only, or ordinary-non-use result.

If recovery shows that the same bounded phrase carries several distinct claims at once, rewrite them as separate ordinary sentences and apply steps 3–5 to each sentence. Ambiguity by itself is not evidence of several claims. Use A.6.C **Contract Unpacking for Boundaries** only when its contract-like boundary-language trigger holds; otherwise apply the direct rule for each recovered claim. Do not create a multi-claim record or an umbrella role object.

| Current claim recovered from the wording | Required result and next action |
|---|---|
| One exact local work-facing system-role kind, or a technical claim that one admitted system counts under it | For kind recovery, use C.3 and A.2 to identify one exact context-local system-role kind; a durable local designation normally ends in `...SystemRole`, for example `ReviewerSystemRole`. For a current classification judgment, use A.2 and C.3.2 and keep the admitted candidate system, exact kind, current `KindSignature` edition, context slice, and `true | false | unknown` result recoverable. Kind admission is not the classification judgment. |
| One obtaining assignment of an admitted system to that kind | Recover one occurrence of an exact direct species under `U.SystemRoleAssignment` through A.2.1. Assignment creates neither system admission, another classification, capability, participation, responsibility, nor Work. |
| “The system as reviewer” or similar readable designation | Keep the readable actor designation when it carries the needed ordinary claim. Recover exact system identity, a separately obtaining classification, or an assignment only when the receiving claim uses that distinction. Create no `SystemInRole` individual. |
| Participant meaning or actual participant of a direct relation | Use `A.6.RSIR` and the pattern for that direct relation. State the participant meaning and actual participant without calling either a system role. |
| One place in a declaration, for example a source-named field, argument, result, endpoint, slot, or port | Use `A.6.RSIR`, followed by A.6.5, A.6.1, or the exact interface pattern. Recover `SlotKind`, `SlotSpec`, an argument or result declaration, or the interface term rather than `SystemRole`. |
| One position in a representation, for example a tuple component, formula argument, graph endpoint, diagram place, schema field, or call position | Use the pattern for the selected representation; use C.29 for a mathematical-lens correspondence when that use is current. The position is neither participant meaning nor system-role kind. |
| Another object or relation, for example participation, functioning, capability, Method, Work, obligation, permission, access, authority, responsibility, position, result, or status | Use the direct pattern and relation for that claim. If exact participants are known but no current direct relation closes the use, return the exact `missing-governor` result through A.6.RCD. |
| A use of an episteme, for example when a report, standard, dataset, description, model, or publication “plays a role” | Recover the exact evidence-use, source-use, description-use, publication-use, reliance, status-use, or other direct relation. The episteme does not become a system-role holder. |
| Ordinary or quoted wording carrying no FPF claim | Retain it as ordinary or source wording. Create no Tech token, kind, assignment, or repair record. |

### E.10.ROLE:4.1 - Boundary with A.6.RSIR {#boundary-with-a-6-rsir}

`E.10.ROLE` starts from the ambiguous word and recovers the sentence's work-facing or use-facing object. Use `A.6.RSIR` for the narrower question of direct-relation participation, reusable declaration, interface, operation declaration or binding, and representation position.

If the recovered claim leaves a direct-participation, reusable-declaration, interface, operation-declaration-or-binding, or representation-position question unanswered, apply `A.6.RSIR` to that question. If it recovers a system-role kind, assignment, capability, Work, deontic relation, evidence use, another direct object, or ordinary non-use, apply that object's direct rule and do not apply RSIR. Neither pattern duplicates the other's subject rules.

### E.10.ROLE:4.2 - Lightweight Result {#lightweight-result}

Ordinary repaired wording is enough. This example assumes that the source establishes the stated evidence use. Include `blocked overread` only when independent local evidence makes that rejected reading plausible and the boundary changes the receiving use:

```text
source sentence: the report played a role in approval
recovered sentence: reviewers used Report-R as evidence for ApprovalClaim-C
applicable rule: A.10 evidence-provenance account
blocked overread: Report-R has no system-role assignment by this claim
stop: ApprovalClaim-C remains the current question
```

No separate repair record is required unless another named use must inspect or reuse the decision.

## E.10.ROLE:7 - Conformance Checklist {#conformance-checklist}

1. Is *role* being used in a claim, rather than only in ordinary or quoted wording?
2. Does the repaired ordinary sentence name the recognizable object and action or relation?
3. Was the result selected from the recovered claim rather than from the word alone?
4. If a system-role kind is current, are its local boundary and stable contribution distinction recoverable through C.3 and A.2? If a technical classification claim is current, are the candidate’s independent A.1 system admission, exact kind, current `KindSignature` edition, context slice, and `true | false | unknown` C.3.2 judgment separately recoverable?
5. If an assignment is current, can you identify both the assignment occurrence and its declared species? Does that species' direct predicate obtain for the actual participants, including the holder, under the stated applicability, and is the occurrence's extent recoverable? Is supporting evidence kept separate from whether the assignment obtains?
6. Are participation, declaration slot, operation binding, interface place, and representation position kept distinct?
7. Are functioning, capability, Work, deontics, access, authority, responsibility, evidence use, and results kept under their direct relations?
8. Does ordinary prose stay ordinary when no technical distinction changes the receiving claim?
9. Does the repair add a qualifier only for a live alternative and avoid a fixed formal expansion?
10. For each recovered claim, does the repair stop after one exact object or relation and its applicable rule are selected?

## E.10.ROLE:9 - Consequences — Reopen Condition {#consequences-reopen-condition}

**Benefits.** Cold readers can recover the intended object at the point of use. Natural practitioner language survives. Technical names become more precise without turning relation slots, evidence uses, or representation positions into system-role kinds.

**Costs.** A claim-bearing ambiguous sentence needs one bounded interpretation before it can be reused. Some old compact Tech names must be retired or made explicitly historical.

Reopen this pattern only when an actual bare-*role* use cannot reach one exact object, relation, ordinary non-use, or missing governor without duplicating `A.6.RSIR`, or when repeated cold readers still infer system admission, assignment, agency, capability, participation, or Work from `SystemRole` morphology.

## E.10.ROLE:12 - Relations {#relations}

| Pattern | Use |
|---|---|
| `E.10` | Detect bare *role* as a trigger with no default Tech reading. |
| `E.10.ARCH` | Place this bounded entry in the wording-use restoration architecture. |
| `A.2`, `C.3`, `C.3.1`, and `C.3.2` | Recover exact local system-role kinds; judge candidate membership through C.3.2 under an exact signature edition and slice; recover subkind order and continuity. |
| `A.2.1`, `A.2.5`, `A.2.7`, and `F.6` | Recover assignments, assignment state, relations among system-role kinds, and performed-Work attribution. |
| `A.6.RSIR`, `A.6.5`, `A.6.1`, and `C.29` | Recover direct-relation participation, declaration places, operation declarations and bindings, interfaces, and representation positions. |
| `A.10`, `B.3`, `F.10`, `E.17`, and `E.24.PUB` | Use A.10 for claim-bound evidence-provenance accounts, B.3 for an actual named assurance claim, F.10 for status-family distinctions, E.17 for reader-facing forms of an accepted account, and E.24.PUB for publication occurrence, form, carrier, or audience availability. |
| `F.18` and `F.19` | Check durable names and the final plain precise sentence after the object is recovered. |


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/E-10#root, spec://ai.lev/fpf-spec/contract/E-10-ARCH#root. @status:spec/done
- @fact:ROUTES-TO Routes to: spec://ai.lev/fpf-spec/contract/A-2#root, spec://ai.lev/fpf-spec/contract/A-2-1#root, spec://ai.lev/fpf-spec/contract/A-6-RSIR#root, spec://ai.lev/fpf-spec/contract/A-6-5#root, and the direct pattern for the recovered object or relation. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/F-18#root, spec://ai.lev/fpf-spec/contract/F-19#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-15#root, spec://ai.lev/fpf-spec/contract/A-2#root, spec://ai.lev/fpf-spec/contract/A-2-4#root, spec://ai.lev/fpf-spec/contract/A-2-7#root, spec://ai.lev/fpf-spec/contract/A-6-P#root, spec://ai.lev/fpf-spec/contract/A-6-RSIR#root, spec://ai.lev/fpf-spec/contract/B-1#root, spec://ai.lev/fpf-spec/contract/B-5-3#root, spec://ai.lev/fpf-spec/contract/C-32-HCS#root, spec://ai.lev/fpf-spec/contract/C-36#root, spec://ai.lev/fpf-spec/contract/D-3#root, spec://ai.lev/fpf-spec/contract/E-24-CD#root, spec://ai.lev/fpf-spec/contract/F-4#root, spec://ai.lev/fpf-spec/contract/F-5#root, spec://ai.lev/fpf-spec/contract/F-6#root, spec://ai.lev/fpf-eng-syse/contract/SYSE-9#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/E-10-ROLE
