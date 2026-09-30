# C.27.TA - Temporal Aspect: Time Windows, Rhythm, Cadence, and Currentness {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Definitional pattern
> **Status:** Stable
> **Normativity:** Normative except where a section is explicitly informative

## C.27.TA:0 - Use This When {#use-this-when}

Use this pattern when a project needs to state a positive temporal-aspect claim about one exact object or exact claim—for example, its time window, cadence, freshness, recovery timing, or currentness.

Use it when the working question is:

- which time window, interval, duration, latency, cadence, rhythm, synchronization, currentness, freshness, validity window, recovery timing, stabilization timing, trajectory, effort over time, inertia, or refresh condition matters;
- which bearer has that temporal property: system, episteme, work plan, work occurrence, claim, source, benchmark, architecture-selected structure, method description, publication, or project-world object;
- which temporal reference makes the statement reviewable: calendar time, clock time, event order, cycle, sprint, epoch, release train, sampling interval, follow-up interval, or domain-local timing reference; and
- whether the property is merely stated, measured, used in a temporal claim, used in a transformation claim, or used in a work, evidence, or decision relation.

**Primary EntityOfConcern.** The `EntityOfConcern` is the independently identified bearer or exact claim being qualified. A temporal label such as *cadence*, *freshness*, or *recovery timing* is a predicate or qualifier in the ClaimGraph; it is not a second entity.

**C.2.1 and publication boundary.** A materialized temporal-aspect statement is record-shaped ClaimGraph content in one `C.2.1` episteme whose effective ReferenceScheme makes the temporal terms interpretable. Changing that claim content identifies another episteme. A changed layout, publication occurrence, form, or carrier can leave the episteme unchanged; those publication objects remain separate under `E.24.PUB` when availability matters. When the claim depends on another direct relation, cite that relation's exact declaration or independently established occurrence. A PatternID remains an ordinary rule citation and is never a relation reference.

**First useful move.** State four things in one readable sentence: the exact bearer or claim, the temporal predicate, the temporal reference, and the interval or window.

**First result.** `CheckoutSystem-1 had a weekly release cadence during release train R14.` This is enough when the receiving action needs no further distinction. Stop there.

Open the fuller statement only when the receiving use also depends on measurement, an exact scheme or scope, a selected Structure, a source or use boundary, currentness, reopen conditions, coupling, another direct relation, or an explicit rule citation or blocked overread.

**What goes wrong if missed.** Temporal words become vibe labels. A cadence is named without bearer, a freshness claim has no validity window, a rhythm has no timing reference, a recovery claim has no interval, an architecture trajectory has no changed structure, and a transformation claim smuggles timing into method, mechanism, or evidence.

**What this buys.** A practitioner can state one positive temporal-aspect claim before selecting `C.27`, `A.3.4`, `A.3.3`, `A.15.2`, `A.15.1`, `C.16`, `C.28`, `G.9`, or the relevant evidence, source, gate, or assurance pattern for the receiving use.

**Not this pattern when.**

- If the question is adequacy or supported use of an authored temporal claim, use `C.27`.
- If the question is bounded transformation under conditions, use `A.3.4`.
- If the question is a state-space and transition-law episteme, use `A.3.3`.
- If the question is work planning or dated work, use `A.15.2` or `A.15.1`.
- If the question is measurement construction, rate construction, scale, score, or metric comparability, use `C.16` and related characterization patterns.
- If the question is causal use of an intervention or policy, use `C.28`.
- If the temporal phrase is ordinary prose and no practical use changes, do not introduce a C.27.TA statement.

## C.27.TA:1 - Problem Frame {#problem-frame}

Distinguish two concerns. One concern is temporal-claim adequacy: whether an authored claim about speed, rhythm, rate-change, recovery, or stabilization can carry a named use. The other concern is positive temporal subject matter: windows, duration, cadence, synchronization, freshness, currentness, inertia, effort over time, recovery, stabilization, and trajectory as aspects of objects or claims.

C.27.TA addresses the second concern. It lets a practitioner state what temporal aspect is in play without immediately opening an adequacy card, a dynamics model, a work plan, a causal-use record, or a transformation statement.

## C.27.TA:2 - Problem {#problem}

Without C.27.TA:

1. **Cadence and rhythm become decorative words.** A text says "release cadence" or "team rhythm" without naming bearer, interval, timing reference, or use.
2. **Freshness becomes a vague virtue.** A source, benchmark, dashboard, or claim is called current without a validity window or refresh relation.
3. **Recovery and stabilization hide their interval.** A claim says "recover faster" or "stabilize" without saying over which window, after which disturbance, and for which bearer.
4. **Effort and inertia float free.** A text speaks about momentum, residue, stored work, adaptation cost, or resistance without linking it to a temporal window and exact object.
5. **Transformation absorbs time silently.** A transformation statement names a change but leaves timing and ordering implicit, so method, mechanism, work, evidence, and temporal claims get tangled.

## C.27.TA:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Positive temporal subject vs claim adequacy | Some temporal aspects merely need to be named; others become authored temporal claims whose adequacy must be judged by C.27. |
| Bearer and interval | A rhythm, latency, recovery time, or validity window means little without a bearer and temporal reference. |
| Local timing vs durable use | A local work note may need one interval; a public claim, benchmark, source use, or assurance relation may need currentness and refresh discipline elsewhere. |
| Transformation and dynamics pressure | A temporal aspect can time a transformation or dynamics model without becoming the transformation or the dynamics episteme. |
| Measurement pressure | Some temporal aspects require measurement construction; others only need a named temporal reference. |

## C.27.TA:4 - Solution {#solution}

### C.27.TA:4.1 - Definition {#definition}

A temporal-aspect claim says that one exact object or exact claim has a time-bearing or order-bearing property under a stated temporal reference and interval. The statement is claim content, not automatically a temporal claim-adequacy result, dynamics law, work trace, method, mechanism, gate, evidence relation, or permission.

Typical temporal predicates and qualifiers include:

- `timeWindow`;
- `duration`;
- `latency`;
- `freshness`;
- `currentness`;
- `validityWindow`;
- `cadence`;
- `rhythm`;
- `synchronization`;
- `trajectory`;
- `recoveryTiming`;
- `stabilizationTiming`;
- `effortOverTime`;
- `inertiaOrResidue`;
- `refreshOrReopenCondition`.

These names are predicates or qualifiers inside claim content, not new `U.*` kinds or locally identified aspect objects.

### C.27.TA:4.2 - Temporal Aspect Statement {#temporal-aspect-statement}

Use this fuller statement only when the four-part first result is not enough for the receiving use:

```text
TemporalAspectStatementClaimContent:
  entityOfConcernRef:
  aspectPredicate:
  temporalReference:
  windowOrInterval:
  entityRulePatternCitation?:
  effectiveReferenceSchemeRef?:
  claimOrWorkScopeRef?:
  selectedStructureRef?:
  sourceOrUseBoundaryRef?:
  localUseCondition?:
  measuredReadingRef?:
  directRelationDeclarationRef?:
  obtainingRelationOccurrenceRef?:
  receivingUseRulePatternCitation?:
  validityOrCurrentnessCondition?:
  refreshOrReopenCondition?:
  blockedLocalOverread?:
```

When this statement is materialized, the record is ClaimGraph content in one `C.2.1` episteme. `entityOfConcernRef` resolves the exact bearer or exact claim being qualified. `aspectPredicate` says what is asserted of it; the label does not identify a temporal-aspect object. The first four fields are the normal minimum.

Every remaining field is conditional. Add it only when changing that value could change the claim or the receiving action. PatternID citations tell the reader which rule to apply and assert no relation. If the claim relies on another direct relation, cite its exact declaration and cite an obtaining occurrence only after its predicate passes. There is no generic context field; each optional scheme, scope, Structure, source or use boundary, or local-use condition keeps the identity and test supplied by its direct pattern.

### C.27.TA:4.3 - Direct Use and Rule Citation {#direct-use-and-rule-citation}

| Temporal use | Direct pattern or rule citation |
| --- | --- |
| positive temporal-aspect claim about an object or claim | `C.27.TA` |
| adequacy or supported use of an authored temporal claim | `C.27` |
| bounded transformation under conditions with temporal reference | `A.3.4` plus `C.27.TA` |
| state-space or transition-law model | `A.3.3` |
| planned work timing | `A.15.2` |
| dated work occurrence or trace | `A.15.1` for the occurrence; `A.10` for evidence and provenance when a claim relies on the trace |
| measurement construction for rate, duration, latency, or freshness | `C.16` and related characterization patterns |
| causal-use timing, intervention window, comparator, or follow-up interval | `C.28` |
| benchmark freshness, baseline window, comparator edition, or parity window | `G.9` |
| source currentness, evidence decay, provenance, or assurance refresh | evidence, source, provenance, assurance, and refresh patterns |

This table supplies rule citations, not relation occurrences. When another relation is part of the temporal claim, use the fields above to cite its declaration; cite an obtaining occurrence only after its predicate passes.

### C.27.TA:4.4 - Rhythm, Cadence, And Synchronization {#rhythm-cadence-and-synchronization}

A minimal rhythm or cadence claim still needs only the exact EntityOfConcern, temporal predicate, temporal reference, and window. Coupling, phase, synchronization, entrainment, dependency, or coordination wording appears only when the claim depends on a cross-bearer temporal relation.

Escalation form:

```text
RhythmAspectClaimContent:
  entityOfConcernRef:
  aspectPredicate: rhythm | cadence | synchronization
  timingReference:
  rhythmWindowRef:
  intervalStructure?:
  rulePatternCitation?:
  directCouplingRelationDeclarationRef?:
  obtainingCouplingOccurrenceRef?:
  validityWindowRef?:
```

The optional fields appear only when the receiving use relies on them. A PatternID citation identifies the rule used to judge a claim; it is not the coupling relation.

A plain "release cadence" or "workshop rhythm" may remain ordinary prose. It needs C.27.TA when cadence or rhythm changes transformation, work planning, benchmark, source, assurance, coordination, or claim-use decisions.

### C.27.TA:4.5 - Currentness, Freshness, And Validity Window {#currentness-freshness-and-validity-window}

A currentness or freshness claim uses the same four-part minimum: exact EntityOfConcern, *current* or *fresh* predicate, reference time or edition, and validity interval or window. A source, benchmark, model, dashboard, or claim may be fresh enough for one use and stale for another.

Add a source-use boundary, currentness condition, refresh condition, or reopen condition only when the receiving use changes when that value changes. Use the direct source, evidence, benchmark, assurance, or refresh pattern for the separate provenance, parity, assurance, or refresh-work claim.

### C.27.TA:4.6 - Recovery, Stabilization, Inertia, And Effort Over Time {#recovery-stabilization-inertia-and-effort-over-time}

A recovery, stabilization, inertia, or effort-over-time claim first names the exact EntityOfConcern, temporal predicate, temporal reference, and interval. It becomes a C.27 adequacy question only when an authored claim uses that result for a practical action.

Add the disturbance or starting condition, measured reading, effort, resistance, residue, inertia relation, rule-pattern citation, or direct-relation reference only when the receiving use relies on that distinction. These values do not turn the temporal predicate into a transformation, Work, evidence, value, or assurance relation.

## C.27.TA:7 - Conformance Checklist {#conformance-checklist}

| Check | Requirement |
| --- | --- |
| `CC-C27TA-1` | @fact:CC-C27TA-1 The first result names one exact EntityOfConcern, temporal predicate, temporal reference, and interval or window. A materialized result is ClaimGraph content in one `C.2.1` episteme. @status:spec/done |
| `CC-C27TA-1a` | @fact:CC-C27TA-1a No generic context value is required. Measurement, effective scheme or scope, selected Structure, source or use boundary, local-use condition, currentness, reopen, coupling, direct relation, PatternID citation, and blocked overread appear only when changing that value could change the claim or receiving action. @status:spec/done |
| `CC-C27TA-2` | @fact:CC-C27TA-2 The aspect label is a predicate or qualifier in claim content, not an identified temporal-aspect object, and the statement distinguishes the positive claim from C.27 adequacy. @status:spec/done |
| `CC-C27TA-3` | @fact:CC-C27TA-3 When present, PatternID citations are ordinary rule locators. Any direct relation uses a separate exact declaration reference and cites an obtaining occurrence only after its own predicate passes. @status:spec/done |
| `CC-C27TA-4` | @fact:CC-C27TA-4 Rhythm or cadence claims use the four-part minimum; cross-bearer fields appear only when an independently established relation changes the receiving use. @status:spec/done |
| `CC-C27TA-5` | @fact:CC-C27TA-5 Currentness or freshness claims add a source-use boundary, currentness, refresh, or reopen condition only when it changes the receiving use. @status:spec/done |
| `CC-C27TA-6` | @fact:CC-C27TA-6 Recovery, stabilization, inertia, and effort-over-time claims begin with the four-part minimum; disturbance, measurement, effort, relation, and rule fields are conditional. @status:spec/done |
| `CC-C27TA-7` | @fact:CC-C27TA-7 The claim does not infer evidence, permission, value, gate passage, work completion, causal use, or a relation occurrence from a temporal predicate. @status:spec/done |
| `CC-C27TA-8` | @fact:CC-C27TA-8 Measurement construction, dynamics laws, transformations, work, benchmark parity, and source or evidence use stay with their direct patterns; publication occurrence, form, and carrier do not reidentify unchanged claim content. @status:spec/done |

## C.27.TA:10 - Consequences {#consequences}

- C.27 addresses adequacy and supported use of authored temporal claims.
- A.3.4 identifies the actual transformation; C.27.TA states its temporal aspect.
- A.3.3 stays the dynamics episteme pattern.
- Use the direct patterns for work planning, actual work, source currentness, benchmark parity, and evidence use.
- Users gain one positive temporal-aspect claim before heavier adequacy, dynamics, causal, benchmark, or assurance patterns are needed.

## C.27.TA:11 - Relations {#relations}

- **Builds on:** `E.24`, `A.6.5`, `A.7`, `C.2.1`.
- **Coordinates with:** `C.27`, `A.3.4`, `A.3.3`, `A.15.2`, `A.15.1`, `C.16`, `C.28`, `G.9`, evidence, source, assurance, refresh, and publication patterns.
- **C.27 consumer boundary:** `C.27` consumes this exact temporal-aspect episteme or one exact `C.2.1 ClaimAddress` to its intrinsically identified claim; it adds only the adequacy-for-use claim and does not redefine the bearer, predicate, window, coupling, or currentness fields.
- **Used by:** patterns that need a positive temporal-aspect claim without making a temporal-claim adequacy judgement.


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/A-3-4#root, spec://ai.lev/fpf-spec/contract/A-3-3#root, spec://ai.lev/fpf-spec/contract/C-27#root, spec://ai.lev/fpf-spec/contract/E-24#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/A-10#root, spec://ai.lev/fpf-spec/contract/B-3#root, spec://ai.lev/fpf-spec/contract/A-15-1#root, spec://ai.lev/fpf-spec/contract/A-15-2#root, spec://ai.lev/fpf-spec/contract/A-20#root, spec://ai.lev/fpf-spec/contract/A-21#root, spec://ai.lev/fpf-spec/contract/C-16#root, spec://ai.lev/fpf-spec/contract/C-29#root, spec://ai.lev/fpf-spec/contract/E-18#root, spec://ai.lev/fpf-spec/contract/G-11#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-14#root, spec://ai.lev/fpf-spec/contract/A-3-3#root, spec://ai.lev/fpf-spec/contract/A-3-4#root, spec://ai.lev/fpf-spec/contract/A-3-4-P#root, spec://ai.lev/fpf-spec/contract/B-1-4#root, spec://ai.lev/fpf-spec/contract/B-3-4#root, spec://ai.lev/fpf-spec/contract/C-27#root, spec://ai.lev/fpf-spec/contract/E-10-ARCH#root, spec://ai.lev/fpf-spec/contract/E-10-DEV#root, spec://ai.lev/fpf-eng-ops/contract/OPS-10#root, spec://ai.lev/fpf-eng-ops/contract/OPS-2#root, spec://ai.lev/fpf-eng-ops/contract/OPS-7#root, spec://ai.lev/fpf-eng-syse/contract/SYSE-13#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/C-27-TA
