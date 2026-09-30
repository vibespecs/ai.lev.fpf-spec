# A.19.SPR - Repair State and Status Wording {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** State-family precision-restoration pattern
> **Status:** Stable
> **Normativity:** Normative unless explicitly marked informative

**Plain-name.** State-wording repair.

## A.19.SPR:0 - Use this when {#use-this-when}

Use this pattern when a phrase such as “the system is ready”, “the source is current”, or “the evidence status is incomplete” matters to an FPF claim but does not yet say which item the sentence is about, what is true of it, or which rule makes that statement meaningful.

**What goes wrong if missed.** A short status word starts carrying several claims at once. A source label becomes evidence, a readiness label becomes gate passage, or a project-side status leaks into pattern guidance.

**First question.** Ask:

> What exact item is this sentence about, what does it say about that item, and which rule or criterion gives the statement its meaning?

**Cheap direct repair.** Write the answer as one ordinary technical sentence. Name the item, the actual value, relation, result, or claim, and the rule or criterion only when the reader needs it to understand or act. If that sentence is clear and safe for the intended use, stop. Do not create a repair note or list every claim the sentence does not make.

**What this buys.** A reader can understand the statement and its next practical use without learning a hidden status vocabulary.

Typical triggers include `state`, `status`, `posture`, `stance`, `currentness`, `validity`, `stable`, `accepted`, `blocked`, `candidate`, `degraded`, `readiness`, `ready`, and similar compounds. A precise-looking field such as `LensUseBoundaryValue` or `dynClaimPosture` is also a trigger when its object, possible values, or rule cannot be recovered.

**Not this pattern when.**

- If the exact item, claim or value, and applicable rule are already clear, use that rule directly.
- If `readiness` or `ready` still hides whether the sentence concerns a subject state, assignment condition, work entry, gate decision, publication use, permission, or performed Work, use `E.10.MOVE` first.
- If the wording is ordinary prose and carries no FPF-governed claim, keep it ordinary.
- If one `Characteristic`, Scale, Coordinate, score, or measurement construction is hidden, use `C.16.P` first.
- If a source expression, publication, carrier, or source-use relation is hidden, use `C.2.P` first and return here only if a state-wording problem remains.
- For relation, architecture, quality, function, or naming problems, use `A.6.P`, `C.30.P`, `C.16.Q`, `A.6.F`, or `F.18` as selected by `E.10`.

## A.19.SPR:1 - Problem frame {#problem-frame}

FPF needs compact state words. Engineers reasonably say that a pump is stable, a source is current, an evidence path is incomplete, an assurance claim has expired, or an intended performance is ready for work entry.

The words work when the reader can recover the item, the actual claim or value, and the rule behind it. Trouble begins when the word replaces those facts. “Ready” may mean a patient condition, an assignment satisfying a condition, an A.15.5 work-entry result, an A.21 gate decision, or merely a green display. Those are different claims.

A repaired sentence may therefore name an ordinary domain condition, an obtaining relation, an assertion episteme, an evaluation result, a decision result, or a project-side record field. It introduces a predicate only when the rule for that claim defines or needs one.

## A.19.SPR:2 - Problem {#problem}

How can FPF keep useful words such as `state`, `status`, and `ready` without:

- creating one general `Posture` or readiness kind;
- replacing one broad status word with another;
- treating every state statement as a `CharacteristicSpace` position or predicate;
- merging source use, evidence, assurance, publication, assignment state, work entry, gate decisions, performed Work, and project records;
- copying the same wording-repair procedure into every pattern; or
- deleting a useful local finite field whose object, values, rule, and practical use are already clear?

## A.19.SPR:3 - Forces {#forces}

| Need | Tension |
| --- | --- |
| Short working language | Practitioners need compact sentences, but a consequential claim must still identify what is being judged. |
| Local fields | A finite field can be useful; a vague status field can hide several unrelated claims. |
| Direct patterns | A.19 covers characteristic spaces, while evidence, assurance, publication, assignment state, readiness, gates, and project records keep their own rules. |
| Small repair | Most cases need one rewritten sentence, while replayed or high-consequence cases may need a few additional fields. |

## A.19.SPR:4 - Solution {#solution}

Start with the direct sentence:

1. name the exact item;
2. say what value, relation, result, or claim is current; and
3. name the rule or criterion when the sentence is not understandable or usable without it.

Stop there when the intended reader can act safely. Add evidence, time, allowed-use, or blocked-inference detail only when that detail changes the receiving action or prevents a likely harmful conclusion.

Use a `StateFamilyPrecisionRepair` note only when another person or tool must replay the repair, or when the claim has enough consequence that its extra basis must remain inspectable:

```text
StateFamilyPrecisionRepair:
  triggerSpan:
  finalSentence:
  recoveredObjectRef?:
  recoveredClaimValueRelationOrResult?:
  definingOrTestingPatternLocator?:
  predicateRef?:
  criteriaOrEvidenceRef?:
  allowedUse?:
  blockedInference?:
  checkAgainWhen?:
```

The optional fields are triggered separately:

| Add this field | Only when... |
| --- | --- |
| `predicateRef` | the direct pattern defines or needs a reusable predicate. |
| `criteriaOrEvidenceRef` | a receiving decision relies on the criterion or evidence identity. |
| `allowedUse` | the same value could drive materially different actions. |
| `blockedInference` | a likely adjacent inference would be harmful, such as treating readiness as gate passage. |
| `checkAgainWhen` | the value can expire or change during the intended use. |
| exact references and machine fields | automation, audit, comparison, or later replay needs those identities. |

A direct relation, classification, assertion episteme, evaluation result, decision result, or record field keeps its own form. The repair note does not turn it into a new state predicate or result kind.

### A.19.SPR:4.1 - Direct repair {#direct-repair}

For ordinary prose, inspect only the current sentence:

1. **Find the item.** For system-role wording, distinguish an exact local system-role kind, an obtaining assignment, its state condition, the world-side assignment-state relation, and an assertion about either. Do not stop at bare `role`.
2. **Write the claim.** Say that the item has a value, that a relation obtains, that an assertion or result says something, or that a project record has a field value.
3. **Use the direct rule.** Cite the applicable pattern when its criterion or distinction matters. If the direct rule already settles the sentence, A.19.SPR has finished its job.

Add a time boundary, evidence basis, allowed use, or blocked inference only under the triggers above. If the item or claim still cannot be recovered, keep the wording as a quotation or navigation cue, narrow its use, or state the exact blocker.

#### A.19.SPR:4.1.1 - Assignment-state exits {#assignment-state-exits}

| Recovered claim | Direct exit |
| --- | --- |
| One exact system-role assignment or its holder, with no state condition claimed | `A.2.1`; the assignment itself is not readiness. |
| A reusable condition for assignments to one exact local system-role kind | A.2.5 `SystemRoleAssignmentStatePredicate`, by value. |
| One exact assignment satisfies that condition during the relevant interval | The world-side A.2.5 `SystemRoleAssignmentStateRelation` occurrence. |
| An affirmative or negative claim about the assignment or an established relation occurrence | A.2.5 `SystemRoleAssignmentStateAssertion : U.Episteme`; the assertion is not its EntityOfConcern. |
| Evidence, currentness, reliance, or an evaluation concerning that assertion episteme | `A.2.4`, `A.10`, or the direct evaluation pattern. Keep the assertion episteme distinct from the assignment and world-side relation. |
| Whether intended Work may enter now | `A.15.5` or the direct receiving pattern. A.2.5 may supply an assignment-state input; it does not publish the admission result, gate decision, or Work occurrence. |

#### A.19.SPR:4.1.2 - Readiness exits {#readiness-exits}

When `readiness` or `ready` still hides which governed value is meant, use `E.10.MOVE` first. Once the claim is recovered, leave the wording repair through exactly one direct exit:

| Recovered readiness-like claim | Direct exit |
| --- | --- |
| A subject such as a patient or system has a value in a still-hidden state frame | `A.19.SPR`, followed by the subject pattern that defines or tests that value. |
| An assignment satisfies an assignment-state condition | `A.2.5`. |
| One intended performance satisfies a work-entry criterion | `A.15.5` work-entry readiness result. |
| A distinct `OperationalGate(profile)` consumes declared checks and publishes a decision | `A.21`; a ready label alone is not gate passage. |
| A publication use, permission claim, or dated performed Work is meant | `E.17`, the direct permission pattern, or `A.15.1`, respectively. Readiness wording establishes none of them. |

### A.19.SPR:4.2 - Where the repaired claim belongs {#where-the-repaired-claim-belongs}

| What the sentence means | Use this pattern or record |
| --- | --- |
| position in a declared `CharacteristicSpace` | `A.19`, with `A.17`, `A.18`, `C.16`, and `C.16.P` when construction is hidden |
| reusable transition law, trajectory, or dynamics model | `A.3.3` |
| exact system-role assignment with no state condition claimed | `A.2.1`; do not treat assignment as readiness |
| by-value assignment-state condition, obtaining assignment-state relation, or assertion episteme about either | `A.2.5`, keeping `SystemRoleAssignmentStatePredicate`, `SystemRoleAssignmentStateRelation`, and `SystemRoleAssignmentStateAssertion` distinct |
| evidence, currentness, reliance, or evaluation concerning an assignment-state assertion | `A.2.4`, `A.10`, or the direct evaluation pattern; the assertion episteme does not become its subject |
| work-entry use of an assignment-state claim | `A.15.5` or the direct receiving pattern; A.2.5 supplies only the exact assignment-state input |
| language-state position for episteme or publication wording | `C.2.2a` and `A.16.*` after `C.2.P` when source-publication recovery is needed |
| source use, source currentness, source publication, or source-use disposition | `C.2.P`, `E.17`, `E.9.DA`, or source-use field named by value |
| evidence path state, evidence relation, or reliance disposition | Use `A.10` to recover the exact source, independently established support relations, currentness and bounded use; use the direct defining pattern for the particular support relation or reliance decision. |
| assurance result, assurance claim, assurance input, or engineering-justification use | `B.3` |
| constraint or local CV | `A.20` or the direct constraint pattern |
| ambiguous `readiness` or `ready` wording | `E.10.MOVE` until the governed value is recovered |
| work-entry readiness | `A.15.5` |
| distinct gate decision | `A.21` only when an `OperationalGate(profile)` consumes declared checks and publishes that decision |
| release or permission claim | the direct release or permission pattern; a readiness value establishes neither |
| publication use, publication face, form, or unit value, source-finding use | `E.17`, `E.17.0`, `E.17.AUD`, or publication pattern governing the claim |
| Description episteme admitted for specification use or specification refinement | `A.7`, plus the specification-granting neighbouring pattern named by value: `A.6.2`, `C.2.3`, `A.21`, `C.16`, `E.17`, `E.10`, or another named pattern |
| temporal claim status or temporal-use classification | `C.27`, retaining `dynClaimPosture` only as a declared C.27 field |
| mathematical-lens use admissibility | `C.29`, retaining `LensUseBoundaryValue` only as a declared C.29 field |
| `DRR` decision-adequacy result or source-use classification | `E.9.DA` |
| pattern-quality result or pattern-quality review status | `E.21`, with `E.19` only as review or admission profile |
| administrative, review, dispatch, release or admission, or source-control state | the project-side administrative, review, dispatch, release or admission, or source-control record; not pattern prose unless the pattern's own `EntityOfConcern` is that record |

### A.19.SPR:4.3 - Keeping a technical state field {#keeping-a-technical-state-field}

A technical field such as `...Status`, `...Readiness`, or `...State` may stay when the text makes three things clear: what item the field describes, which values it can take, and which rule or criterion gives those values meaning.

Add an allowed-use boundary only when the field changes a receiving action. Add a blocked inference only when a likely misreading would be harmful. Add a validity window or recheck condition only when the value can change during the intended use. Machine-readable identifiers belong only to automation, audit, comparison, or replay that consumes them.

If the three basic facts are missing, complete them or replace the field with the ordinary sentence the reader actually needs. A narrowing adjective alone does not recover the claim.

## A.19.SPR:6 - Conformance checks {#conformance-checks}

| Check | Requirement |
| --- | --- |
| `CC-A19SPR-1` | @fact:CC-A19SPR-1 The final sentence names the exact item and what is claimed or valued, or explicitly keeps the wording ordinary, quoted, navigation-only, narrowed, or blocked. @status:spec/done |
| `CC-A19SPR-2` | @fact:CC-A19SPR-2 The direct rule or criterion is recoverable whenever the claim is not understandable or usable without it. @status:spec/done |
| `CC-A19SPR-3` | @fact:CC-A19SPR-3 A predicate appears only when the direct pattern defines or needs one; relations, assertions, results, decisions, and record fields keep their own forms. @status:spec/done |
| `CC-A19SPR-4` | @fact:CC-A19SPR-4 An allowed-use or blocked-inference clause appears only when it changes the receiving action or prevents a likely harmful conclusion. @status:spec/done |
| `CC-A19SPR-5` | @fact:CC-A19SPR-5 A time window, expiry rule, or recheck condition appears when the value can change during the intended use. @status:spec/done |
| `CC-A19SPR-6` | @fact:CC-A19SPR-6 Source, evidence, assurance, publication, assignment state, work entry, gates, decisions, release or admission, and project records use the patterns or records that define or test those exact claims. @status:spec/done |
| `CC-A19SPR-7` | @fact:CC-A19SPR-7 Source and publication patterns are not used as a general home for evidence, assurance, gate, Work, temporal, mathematical-lens, or project status. @status:spec/done |
| `CC-A19SPR-8` | @fact:CC-A19SPR-8 A retained technical field names its item, possible values, and rule; it adds use, time, evidence, and blocked-inference fields only under their triggers. @status:spec/done |
| `CC-A19SPR-9` | @fact:CC-A19SPR-9 A cold reader can say what the sentence is about, what it claims, and what to do or check next. Type-correct but opaque wording fails. @status:spec/done |
| `CC-A19SPR-10` | @fact:CC-A19SPR-10 Corpus repair classifies each use; it never performs a blind global replacement of `posture`, `state`, `status`, or `readiness`. @status:spec/done |

## A.19.SPR:8 - Relations {#relations}

The dependency and distribution detail belongs here, after the working method. A.19.SPR builds on `E.10`, `E.10.ARCH`, `E.10.MOVE`, `A.19`, `A.3.3`, `A.2.5`, `A.15.5`, `C.2.2a`, `A.10`, `B.3`, `A.20`, `A.21`, `C.27`, `C.29`, `E.17`, `E.9.DA`, `E.21`, and `F.18`. It coordinates with `A.17`, `A.18`, `C.16`, `C.16.P`, `C.16.Q`, `A.6.P`, `C.2.P`, `C.30.P`, `E.8`, `E.19`, and `E.11` when those patterns define or test the recovered claim.

| Pattern | Contribution |
| --- | --- |
| `E.10`, `E.10.ARCH` | Recognize the wording problem and keep one shared restoration architecture. |
| `E.10.MOVE` | Resolves ambiguous readiness-like wording before it exits to A.19.SPR or a direct pattern. |
| `A.2.5`, `A.15.5` | Distinguish assignment-state predicate, world-side relation, assertion episteme, and the separate work-entry readiness result. |
| `A.19`, `A.3.3`, `C.16.P` | Define characteristic-space, dynamics, and characteristic or scale claims when those are the actual subject. |
| `C.2.P`, `C.2.2a`, `A.16.*`, `E.17` | Define source, publication, and language-state claims. |
| `A.10`, `B.3` | `A.10` recovers provenance and bounded reliance; `B.3` governs assurance claims. Each support relation retains its direct defining pattern. |
| `A.20`, `A.21` | Define constraint or adjudication results and distinct gate decisions. |
| `C.27`, `C.29` | Define temporal-claim and mathematical-lens uses, including their local fields. |
| `E.9.DA`, `E.21`, `E.19` | Define DRR adequacy, pattern-quality results, and review or admission profiles. |
| `F.18`, `F.19` | Settle durable names after the claim is known and rewrite the final practitioner path in plain technical language. |
| `E.11` | Places first-use cues without creating a second routing table. |


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/E-10#root, spec://ai.lev/fpf-spec/contract/E-10-ARCH#root, spec://ai.lev/fpf-spec/contract/A-19#root, spec://ai.lev/fpf-spec/contract/A-3-3#root, spec://ai.lev/fpf-spec/contract/C-2-2a#root, `spec://ai.lev/fpf-spec/contract/A-16#root.*`, spec://ai.lev/fpf-spec/contract/A-10#root, spec://ai.lev/fpf-spec/contract/B-3#root, spec://ai.lev/fpf-spec/contract/A-20#root, spec://ai.lev/fpf-spec/contract/A-21#root, spec://ai.lev/fpf-spec/contract/C-27#root, spec://ai.lev/fpf-spec/contract/C-29#root, spec://ai.lev/fpf-spec/contract/E-17#root, spec://ai.lev/fpf-spec/contract/E-9-DA#root, spec://ai.lev/fpf-spec/contract/E-21#root, spec://ai.lev/fpf-spec/contract/F-18#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/A-17#root, spec://ai.lev/fpf-spec/contract/A-18#root, spec://ai.lev/fpf-spec/contract/C-16#root, spec://ai.lev/fpf-spec/contract/C-16-P#root, spec://ai.lev/fpf-spec/contract/C-16-Q#root, spec://ai.lev/fpf-spec/contract/A-6-P#root, spec://ai.lev/fpf-spec/contract/C-2-P#root, spec://ai.lev/fpf-spec/contract/C-30-P#root, spec://ai.lev/fpf-spec/contract/E-8#root, spec://ai.lev/fpf-spec/contract/E-19#root, spec://ai.lev/fpf-spec/contract/E-11#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/C-30-STRAT#root, spec://ai.lev/fpf-spec/contract/E-10#root, spec://ai.lev/fpf-spec/contract/E-10-ARCH#root, spec://ai.lev/fpf-spec/contract/F-19#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/A-19-SPR
