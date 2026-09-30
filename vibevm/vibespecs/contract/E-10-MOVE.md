# E.10.MOVE - Move, Readiness and Trajectory Wording Precision Restoration {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Part E precision-restoration pattern
> **Status:** Stable
> **Normativity:** Normative for move-like, movement-like, readiness-like, route-like, path-like, and trajectory-like wording-use restoration.

**At a glance.** `E.10.MOVE` restores the exact FPF value or relation hidden by move-like, movement-like, readiness-like, route-like, path-like, or trajectory-like wording. Its branches cover demonstrated continuation, prediction, readiness, and trajectory use. Recover the subject, posture, ordering, and representation needed to reach the direct owner; the pattern admits no generic Move or Trajectory head.

**Use this when.** After the normal `F.19` reading and compact `E.10` routing, use this pattern only while move-like, movement-like, readiness-like, route-like, path-like, or trajectory-like wording still hides the governed claim—for example, a demonstrated continuation, a prediction, readiness for a named Work, or an actual, planned, or modelled trajectory.

**Primary EntityOfConcern.** One wording-use restoration over a bounded text span whose move-like, movement-like, readiness-like, route-like, path-like, or trajectory-like wording has an FPF-governed use.

**First output.** Repaired wording, a truthful split, or a blocker. When later replay relies on the repair, use a temporary `MoveAndReadinessWordingRepairNote` that names the governed span, claim, object under repair, wording-use disposition, subject pattern, exact governed value and kind, relation signature when applicable, repaired wording or blocker, and remaining admissible reader use. A grounded non-use boundary is optional under `F.19`; it is not a required repair field.

**Not this pattern when.** Use `A.3.4.P` first when the wording is primarily about a transformation or change situation. Use `E.10.DEV` first when *development* or *evolution* still hides the changed subject, continuity or membership, or direction or value claim; continue here only if an independent trajectory, route, ordering, posture, or representation ambiguity remains. Use `F.19` and the direct subject pattern immediately when the current object is already known. Generic *process*, *workflow*, *loop*, or *flow* wording stays outside unless it independently carries one of the governed move, readiness, route, path, or trajectory claims.

## E.10.MOVE:1 - Problem Frame {#problem-frame}

"Move" is useful in project conversation. It can mean a chess-like next choice, a first FPF use, a TameFlow `MOVE`, an architecture candidate, a language-state transition, a call-planning next action, a work-preparation item, or an ordinary action. "Ready", "full kit", and "work entry" can likewise mean source currentness, work planning, preparation work, gate passage, or performed work.

The defect is not the word. The defect is letting that word choose the ontology. `E.10.MOVE` restores the object under wording repair and the direct FPF relation before any rewrite is accepted.

## E.10.MOVE:2 - Problem {#problem}

Without this restoration:

1. FPF mints a false root `U.Move`.
2. Pattern-use recommendations become performed work or work authorization.
3. TameFlow `MOVE` is imported as if it were an FPF kind.
4. Readiness labels become gate passage or work occurrence by appearance.
5. Route, workflow, process, and path wording is repaired through taste rather than through the governed object.

## E.10.MOVE:3 - Forces {#forces}

| Force | Pressure |
| --- | --- |
| Plain engineering language | Teams naturally ask for a next useful move or readiness result. |
| Kind safety | The same word may point to several different FPF values. |
| Practical payoff | A repair that removes "move" but hides what the user can do next has failed. |
| Neighboring-pattern discipline | Change-situation wording belongs to `A.3.4.P`; work, gates, publications, sources, architecture, and call planning have their own patterns. |
| Short cue set | The trigger list should be memorable and should not become an alias catalog. |

## E.10.MOVE:4 - Solution {#solution}

**Cheap ordinary use.** When the governed value and its direct pattern are already evident, apply `F.19`, name the value, rewrite the phrase without changing the claim, confirm the remaining admissible reader use, and stop. Do not materialize the repair note or traverse the disposition table. Open the fuller procedure only when the wording remains ambiguous, carries several governed values, imports a source term, or must be replayed later.

For a mantra, recover the pattern use before deciding that two phrases mean different moves. A question about a difficulty can refer to the `Problem frame` or `Problem`; a reminder of what to do can refer to the same use through the `Solution`. “Find what the trial establishes” can state the difficulty and the action intended to resolve it. When the subject, intended result and conditions are clear, retain the useful wording. Clarify a missing participant or relation where the reader would otherwise choose a different pattern or action. This wording choice decides neither whether a mantra is local or long nor whether a surrounding presentation is a demonstrative slice of an independently qualified CGUS.

Restore the governed target before choosing replacement wording:

1. Name the exact `GovernedTextSpan`, the `ClaimBeingMade`, and the `ObjectUnderWordingRepair`.
2. Decide whether the wording is ordinary prose, a quotation, or wording relied on for an FPF-governed claim. Ordinary and quotation uses can close without inventing a technical target.
3. When the phrase is `mantra move`, first ask which use is present. In a post-qualification A.22.CGUS demonstrative slice that shows pattern use, recover the exact E.11.PUA `PatternUsePracticeContinuationDescription@Context`: its proposed use, expected result and kind, PatternID and name, current condition, and continuation disposition. Keep `mantra move` only as bounded Plain wording for that shown continuation. A.22.CGUS supplies the structure and slice boundary; it does not create a universal displayed-row kind. For a Plain local mantra, name the bounded result and restore the move-like wording through that result's exact predicate or constraint. For a Plain long mantra, name the intended final result and the particular map location whose answer or stop is current, then state the exact answer or blocker and use the subject pattern only as a locator. Do not invent a demonstrated row, collapse the long map into one pattern's Solution, or treat any branch as Work order.
4. When `move`, `movement`, `direction`, or similar wording predicts a later evaluation result, recover `ExpectedEvaluationResultChange@Context` under `E.23`. That value is a coordinate-and-scale-qualified prediction episteme, not an operation, transition, movement, work occurrence, or proof of improvement.
5. For every other governed use, name the exact recovered value or relation, its kind, and its subject pattern. For a relation claim, name the admitted direct predicate and actual participants. Add a `RelationSignature` reference only when an admitted reusable typed declaration is current and the receiving use needs that declaration. If the governed value is already clear, use its pattern directly.
6. Split the text when one phrase carries more than one governed value. A recommendation, method, transformation, readiness claim or result, gate decision, publication relation, and performed Work do not become one value because the same word was used for them.
7. Preserve `RemainingReaderUse`: the repair is complete only when a practitioner can still tell what can be inspected, selected, evaluated, planned, performed, or returned to next.

### E.10.MOVE:4.1 - MoveAndReadinessWordingRepairNote {#moveandreadinesswordingrepairnote}

```text
MoveAndReadinessWordingRepairNote:
  EncounteredWording:
  GovernedTextSpan:
  ClaimBeingMade:
  ObjectUnderWordingRepair:
  WordingUseDispositionValue: boundedDemonstratedContinuation | evaluationResultChangePrediction | directGovernedUse | importedSourceWording | ordinaryProse | quoteOnly
  SubjectPatternLocator?: PatternID, locating the pattern whose content defines, constrains, or tests the recovered value
  RecoveredGovernedValueRef?: U.EntityRef
  RecoveredGovernedValueKindRef?: U.KindRef
  RecoveredRelationSignatureRef?: U.EntityRef, referencing one RelationSignature
  RetainedPlainWording?:
  BlockedOverread?:
  SplitDisposition?:
  FinalWordingOrBlocker:
  RemainingReaderUse:
  QualificationWindow:
  CurrentnessBasis:
  ReopenCondition:
```

The governed-value ref and kind ref are both present or both absent. `BlockedOverread?` states a rejected reading and appears only when independent local evidence makes the exact rival reading plausible to the intended reader and deleting the boundary would change understanding, selection, safety, reliance, stop, or action. The relation-signature ref is present only when an admitted reusable typed declaration is current and the receiving use needs that declaration. Otherwise a relation claim names the admitted direct predicate and actual participants without a signature ref. A governed use has a non-semantic `SubjectPatternLocator`: an ordinary PatternID that identifies the pattern whose content defines, constrains, or tests the recovered value. Where the receiving claim needs a Method or MethodDescription, use the independent `A.3.1` and `A.3.2` conditions; admit any Method-use relation under its direct relation owner. For ordinary prose or quote-only use, the disposition explains why no FPF object is claimed; the corresponding object positions may remain absent. The `...Ref` fields carry references of the declared RefKinds; they do not carry the referenced values or kinds. A materialized note also states the edition, source, context, or time window in which the repair is relied on, the current pattern or source basis for that interpretation, and the smallest change that reopens it. Use `G.11` only when actual refresh orchestration is current; the note merely records its own currentness boundary. `FinalWordingOrBlocker` gives the wording or blocker for this bounded repair under its qualification and currentness conditions; a later change can reopen it. The note is a temporary wording-restoration aid; substantive results use their direct pattern's admission rules. Ordinary immediate repair need not materialize the note.

### E.10.MOVE:4.2 - Trigger groups {#trigger-groups}

After `E.10` selects this pattern, use these cue groups to find the appropriate recovery branch while an action-changing ambiguity remains:

- `move`, `step`, `action`, `application`, `solution`, and `next action`;
- `readiness`, `ready`, `full kit`, `work entry`, `committed`, and `launch-ready`;
- `movement`, `direction`, or `shift` used for an expected evaluation-result change;
- `route`, `workflow`, `process`, `path`, `trajectory`, `loop`, or `flow` used for an unresolved claim about a path, ordering, or what it represents; use the direct exits below;
- imported source wording such as TameFlow `MOVE`.

The cue group locates a recovery branch. The recovered claim and its direct owner determine the governed-value kind.

#### E.10.MOVE:4.2.1 - Readiness exits {#readiness-exits}

Stay in E.10.MOVE only while `readiness`, `ready`, `full kit`, `work entry`, or a similar cue still hides which governed value is meant. Once that value is recovered, use the direct pattern:

| Recovered claim | Direct pattern |
| --- | --- |
| A patient, system, or other subject has a value in a still-hidden state frame | `A.19.SPR`, then the subject pattern that defines or tests the recovered value. |
| An exact system-role assignment satisfies a by-value assignment-state condition | `A.2.5`; keep its predicate, world-side relation occurrence, and assertion episteme distinct. |
| One intended performance satisfies a work-entry criterion | `A.15.5`; its local readiness result is not a gate decision or performed target Work. |
| A named gate decides whether one bounded action or transition may proceed under an applicable profile | `A.21` combines independently established check results into a `GateDecisionResult`; publication is a separate optional use. A ready label or readiness result alone is not gate passage. |
| A publication use, permission claim, preparation Work, or target Work is meant | `E.17`, the direct permission pattern, or `A.15.1` as applicable. Keep each claim separate. |

If the direct pattern and value were already clear, bypass this table and use that pattern immediately.

### E.10.MOVE:4.2a - No synonym closure {#no-synonym-closure}

Recover the governed value and its subject pattern before closing a synonym replacement. Ordinary-prose or quote-only use closes when no FPF-governed value is claimed.

If responsibility is the remaining claim, name the admitted System, direct domain predicate, actual participants, and applicability, or return the exact A.6.RCD missing governor; an assignment is not a responsibility result. Individuate the responsibility-relation occurrence separately only when a named receiving use needs to distinguish that occurrence.

### E.10.MOVE:4.2b - Trajectory wording recovery {#trajectory-wording-recovery}

Use this branch when *trajectory* or close path wording remains claim-bearing after any primary transformation wording has been recovered. The first result is an ordinary repaired claim or exact gap, not a trajectory record.

Ask only the questions the receiving use needs:

1. What exact bearer or represented subject is positioned or ordered?
2. What identity, continuity, membership, lineage, or edition rule matters?
3. Which declared position, state, configuration or possibility space is relied on, if any? Name a defining episteme edition separately when the use depends on it.
4. What is the ordering or reference domain—time, event, generation, plan order, graph order, or another index?
5. What counts as a position, segment, branch, interval, generation, or edge for this use?
6. What posture does the claim need—for example, actual, observed, reconstructed, predicted, simulated, proposed, recommended, or planned?
7. Which direct pattern owns the resulting claim, what receiving use is allowed, and is any grounded non-use boundary needed under the `F.19` plausible-intended-reader test?

These are recovery questions, not fields of a new `Trajectory`, `TrajectoryAccount`, relation head, Method, or mandatory card.

| Recovered trajectory use | Direct exit and boundary |
| --- | --- |
| Actual or reconstructed history of one identified subject | `A.3.4`, `A.3.4.P`, `B.4`, `C.27.TA`, and A.10 as applicable. A plotted sequence or intervention does not establish actual change or continuity. |
| Predicted or simulated state history | `A.3.3`, `A.19`, `C.27`, and `C.29`; name model edition, state space or position space, transition law, validity boundary, and posture. Model output is not actual history. |
| Proposed, recommended, or planned route | `C.22.2`, `C.11.CRC`, `C.11`, A.15.2, and the domain Method. Recommendation, choice, WorkPlan, performed Work, and effect remain separate. |
| Population or lineage history | `C.36` only for the cultural case; otherwise use an admitted domain owner or return the named non-cultural population or lineage architecture gap. Do not model membership turnover as one-holder continuity. |
| NQD/OEE search history, archive or front succession, or possibility-space projection | `C.17`–`C.19`, `G.5`, `G.11`, and `C.29` as applicable. An archive is not automatically a population. |
| Language-state history needed by a responsibility question | `A.16.0` supplies an ordinary account of the relevant source editions, position claims, moves, lineage and losses. Any actual responsibility change needs its independently governed participants, scope, time and instituting facts under §4.6; language-state movement does not supply that relation. |
| Mathematical trajectory lens | `C.29` for the selected representation and explicit correspondence, with declared losses; keep the represented subject under its direct owner. |
| Ordinary or quote-only wording | Preserve it and stop unless a later FPF use relies on a stronger claim. |

For *development trajectory*, open `E.10.DEV` first when the action-changing doubt is what develops, what remains identifiable, or whether improvement is asserted. Continue here only if trajectory still carries an independent claim about position, ordering, posture, or representation. If the bearer and development claim are already clear and only path posture is unresolved, start here and open `E.10.DEV` afterward only for a remaining separate ambiguity. Do not require two notes or two full passes by spelling alone.

### E.10.MOVE:4.3 - Wording-use dispositions {#wording-use-dispositions}

`WordingUseDispositionValue` is a local finite enumeration for choosing a repair branch. It is not a U-kind, relation kind, state frame, or claim about the project value being repaired.

| `WordingUseDispositionValue` | Selected recovery |
| --- | --- |
| `boundedDemonstratedContinuation` | One E.11.PUA `PatternUsePracticeContinuationDescription@Context` shown inside a post-qualification demonstrative slice. A.22.CGUS supplies the structure and slice boundary, not a wrapper-row kind. Retain the complete bounded use and route any separate FPF-governed claim to its direct pattern. |
| `evaluationResultChangePrediction` | One E.23 `ExpectedEvaluationResultChange@Context` with evaluation pattern, coordinate, scale, current result, one expected value, range, or closed direction, proposal basis, and protected tradeoffs. |
| `directGovernedUse` | The exact governed value or relation, its kind, and its subject pattern. For a relation claim, name the admitted direct predicate and actual participants; include a `RelationSignature` reference only when an admitted reusable typed declaration is current and the receiving use needs it. The wording disposition itself contributes no project ontology. |
| `importedSourceWording` | Preserve the source expression only as source wording; recover every FPF use under its direct pattern. |
| `ordinaryProse` | Keep or lightly rewrite when no FPF-governed value is being asserted. |
| `quoteOnly` | Preserve the quotation and its source-licensed use. State a grounded project-side non-use boundary only when that boundary changes the receiving use. |

### E.10.MOVE:4.4 - Relation to A.3.4.P {#relation-to-a-3-4-p}

Use `A.3.4.P` first when the claim is about a change situation or transformation-flow structure. Use `E.10.MOVE` only for the remaining wording-use question. If the same sentence also recommends a pattern use, claims readiness, or names a demonstrated continuation, split those claims and use its direct pattern for each.

### E.10.MOVE:4.5 - Durable name repair {#durable-name-repair}

A durable name states the recovered subject value or relation; it does not retain an implementation head merely because the fields are typed.

| Misleading durable name | Repair |
| --- | --- |
| `localMoveLocus` | Name the exact local value or relation and its subject pattern. Do not preserve `locus` as a cross-pattern grouping head. |
| `ExpectedEvaluationMovement` | Use `ExpectedEvaluationResultChange@Context` only when the E.23 prediction positions are recoverable. |
| `FirstMoveRecord@Context` | Name the actual first result or relation governed by the direct pattern. |
| `Pattern-Use Sequence` | Use `PatternUseCoordination@Context` for the coordination judgement, `PatternUseOrderingRelation@Context` for one justified pairwise precedence relation inside it, and `PatternUseSequence@Context` only for the bounded total-order specialization under a named receiving use. Keep conversational coordination or ordering unmaterialized when no later reliance needs an addressable object. |

These are repair demonstrations, not a global replacement table.

## E.10.MOVE:7 - Conformance Checklist {#conformance-checklist}

| ID | A conforming repair... | Check |
| --- | --- | --- |
| `CC-E10MOVE-1` | @fact:CC-E10MOVE-1 names the governed text span, claim being made, and object under wording repair before choosing a replacement. @status:spec/done | Resolve the kind from the current claim and its direct pattern. |
| `CC-E10MOVE-2` | @fact:CC-E10MOVE-2 assigns one wording-use disposition and does not treat that local enumeration as project ontology. @status:spec/done | Demonstrated row, evaluation-result prediction, direct governed use, imported source wording, ordinary prose, and quotation cases remain distinct. |
| `CC-E10MOVE-3` | @fact:CC-E10MOVE-3 names the exact recovered governed value, value kind, and non-semantic PatternID locator for the subject pattern whose content defines, constrains, or tests that value. For a relation claim, it names the admitted direct predicate and actual participants; it includes a `RelationSignature` reference only when an admitted reusable typed declaration is current and the receiving use needs it. @status:spec/done | Confirm the recovered project value under its direct pattern. Any relied-on MethodDescription identity needs independent A.3.2 admission, as in §4.1. |
| `CC-E10MOVE-4` | @fact:CC-E10MOVE-4 blocks root `U.Move`. @status:spec/done | No durable move kind is minted by wording pressure. |
| `CC-E10MOVE-5` | @fact:CC-E10MOVE-5 preserves remaining reader use. @status:spec/done | The repaired text still says what the practitioner can do or inspect next. |
| `CC-E10MOVE-6` | @fact:CC-E10MOVE-6 splits change-situation wording from pattern-use or readiness wording. @status:spec/done | `A.3.4.P` and `E.10.MOVE` are both used when both objects are current. |
| `CC-E10MOVE-7` | @fact:CC-E10MOVE-7 avoids synonym tables. @status:spec/done | Closure requires the recovered object and relation. |
| `CC-E10MOVE-8` | @fact:CC-E10MOVE-8 recovers the current trajectory claim, its direct owner or exact gap, and the remaining admissible reader use. It recovers bearer or represented subject, identity rule, ordering or reference domain, and posture only where those distinctions affect that claim or use; a grounded non-use boundary appears only when the `F.19` plausible-intended-reader test requires it. @status:spec/done | Keep the subject, posture, ordering, and representation distinctions needed by the use; apply each direct owner's identity and evidence rules. |

### E.10.MOVE:7.1 - Lowering and Reopen Conditions {#lowering-and-reopen-conditions}

Lower, block, or reopen the repair when the governed text span, claim being made, or object under wording repair is not recoverable, the wording-use disposition is uncertain, the proposed wording changes kind or relation without an accepted subject pattern, the subject pattern is missing, a change-situation claim was not separated from pattern-use or readiness wording, the repaired wording loses the remaining reader use, or changed source wording invalidates the recorded source-licensed use.

## E.10.MOVE:9 - Consequences {#consequences}

Benefits:

- FPF keeps friendly move, readiness, route, path, and trajectory language without letting it mint false kinds.
- A trajectory sentence reaches its direct claim owner or exact gap. Subject, posture, ordering, and representation are recovered separately where the use needs them.
- Pattern-use recommendation, P2W, work readiness, gate decision, performed work, transformation, architecture, and call planning stay separable.
- Corpus cleanup can find move-headed debt without doing mechanical global renames.

Costs:

- Reliance-bearing or still-ambiguous phrases may need the small repair note before they can be rewritten safely; ordinary direct-pattern repair does not.
- Text may need to split one sentence into two governed claims when the original wording carried both change-situation and pattern-use meaning.

## E.10.MOVE:12 - Relations {#relations}

- **Builds on:** `F.19`, `E.10`, `E.10.ARCH`, `A.3.4.P`, `A.22.CGUS`, `E.11.PUA`, `E.11.PUR`, `E.23`, `A.15.5`, and `E.24`.
- **Coordinates with:** `E.11.PUA` for the `PatternUsePracticeContinuationDescription@Context` shown by a qualified practice continuation; `E.11.PUR` for `PatternUseCoordination@Context`, one `PatternUseOrderingRelation@Context`, or the bounded total-order `PatternUseSequence@Context`; `E.10.DEV` when development or evolution wording and trajectory wording carry independent ambiguities; `A.1.STM` for a non-CGUS system-thinking long-mantra map location; `A.3.3`, `A.3.4`, `A.3.4.P`, `B.4`, `C.27.TA`, `C.29`, `C.17`–`C.19`, `C.22.2`, `C.11`, A.15.2, `C.36`, and `A.16.0` for trajectory exits; and `E.18`, `E.18.1`, `A.15`, `A.21`, `C.24`, `C.30`, `E.17`, `F.17`, `F.18`, `G.11`, A.10, and each recovered value's direct subject pattern. `F.18` governs a durable-name decision; `G.11` governs refresh orchestration only when currentness, edition, telemetry, freshness, or decay is the actual claim.
- **Selected by:** E.10 compact routing when move, readiness, route, path, or trajectory wording still has an unresolved FPF-governed use after the `F.19` reading and no direct subject pattern has already resolved it.


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/F-19#root, spec://ai.lev/fpf-spec/contract/E-10#root, spec://ai.lev/fpf-spec/contract/E-10-ARCH#root, spec://ai.lev/fpf-spec/contract/A-3-4-P#root, spec://ai.lev/fpf-spec/contract/A-22-CGUS#root, spec://ai.lev/fpf-spec/contract/E-11-PUA#root, spec://ai.lev/fpf-spec/contract/E-11-PUR#root, spec://ai.lev/fpf-spec/contract/E-23#root, spec://ai.lev/fpf-spec/contract/A-15-5#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/E-10-DEV#root for an independent development or evolution ambiguity, spec://ai.lev/fpf-spec/contract/E-18-1#root, spec://ai.lev/fpf-spec/contract/A-15#root, spec://ai.lev/fpf-spec/contract/A-21#root, spec://ai.lev/fpf-spec/contract/C-24#root, spec://ai.lev/fpf-spec/contract/C-30#root, spec://ai.lev/fpf-spec/contract/F-17#root, spec://ai.lev/fpf-spec/contract/G-11#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-15-4#root, spec://ai.lev/fpf-spec/contract/A-15-5#root, spec://ai.lev/fpf-spec/contract/A-16#root, spec://ai.lev/fpf-spec/contract/A-3-4-P#root, spec://ai.lev/fpf-spec/contract/C-22-2#root, spec://ai.lev/fpf-spec/contract/C-36#root, spec://ai.lev/fpf-spec/contract/C-36-P#root, spec://ai.lev/fpf-spec/contract/E-10#root, spec://ai.lev/fpf-spec/contract/E-10-ARCH#root, spec://ai.lev/fpf-spec/contract/E-10-DEV#root, spec://ai.lev/fpf-spec/contract/E-11-PUR#root, spec://ai.lev/fpf-spec/contract/F-17#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/E-10-MOVE
