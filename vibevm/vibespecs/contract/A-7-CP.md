# A.7.CP - Constructive-Premise Compact and Reasoning-Basis Use {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Architectural (A)
> **Status:** Stable
> **Normativity:** Normative

## A.7.CP:0 - Use this when {#use-this-when}

Use this pattern when reasoning, ontology analysis, choice, or reconciliation actually relies on a broad constructive claim and another person must be able to recover which claim, exact receiving claim or result, posture, scope, work occurrence, and interval carried that reliance.

The first useful move is to name the dated reasoning work, each exact claim-bearing result or receiving decision it is forming, the exact `A7CP-*` claim IDs used for that result, and whether each use is an `adoptedPremise` or `conditionalAssumption`. Leave the other compact claims latent.

**Not this pattern when.** Use the relevant subject pattern for citation, publication, shared vocabulary, ordinary `A.7` category-error repair, source currentness, or domain/evidence questions when no compact claim is used in reasoning. No reasoning-basis occurrence obtains in that case.

The primary reader is an author or reviewer who must make one load-bearing constructive premise use recoverable. The governed object is one `ClaimUsedAsReasoningBasisRelation@Context` occurrence and the exact compact claim content it cites.

## A.7.CP:1 - Problem frame {#problem-frame}

Dated work applying an FPF method can rely on broad claims such as “a publication does not create world-side obtaining” or “a MethodDescription episteme does not perform Work”. A `U.MethodDescription` episteme may state or cite one of those claims as a declared premise or branch condition for its described `U.Method`. `ClaimUsedAsReasoningBasisRelation@Context` obtains only when one actual inference, comparison, or choice in dated Work relies on that claim for the exact receiving result. Copying the claim into every method description makes it drift; leaving the dated reliance implicit hides whether a particular result used an adopted premise, a conditional branch, or no common claim at all.

The compact publishes twelve stable claim contents once. A `U.MethodDescription` episteme can declare an intrinsic premise or a branch condition for its described Method; a dated application records only the compact claims actually used in its reasoning. Ordinary Work therefore does not acquire a foundation checklist.

## A.7.CP:2 - Problem {#problem}

Three conflations make premise use unreliable:

1. claim content is confused with the posture in which one work occurrence uses it;
2. citation or co-location is confused with actual reliance in reasoning; and
3. a support pattern is treated as a method that performs or governs the consuming work.

The result is either hidden premises or a copied catalogue that becomes a second ontology authority. Both failures obscure occurrence identity and reopen behavior.

## A.7.CP:3 - Forces {#forces}

| Force | Tension |
|---|---|
| Stable claims vs local use | Claim content should be durable, while posture, work, context, and interval vary per use. |
| Recoverability vs cheap first use | Load-bearing use needs a trace; ordinary method use should not traverse twelve claims. |
| Shared support vs subject patternship | Common claims coordinate patterns without absorbing evidence, currentness, construction, work, or kind admission. |
| Adopted premise vs conditional assumption | Both can support reasoning, but their defeaters and reopen conditions differ. |
| Reuse vs copied variants | one authoritative source prevents drift; consumers still need locally intelligible action guidance. |

## A.7.CP:4 - Solution {#solution}

### A.7.CP:4.1 - Publish the compact once {#publish-the-compact-once}

The compact carries these stable claim contents:

1. **`A7CP-01 Existence and obtaining`.** World-side obtaining is not created by a claim, database row, predicate, or publication merely representing it.
2. **`A7CP-02 Constructive settlement`.** When identity, constitution, dependence, or obtaining changes a consequence, name the construction or direct governing relation that grounds it; a reconstructible trace is not itself the world construction.
3. **`A7CP-03 Constitution and social objects`.** Constituting acts, admitted systems, and the relations they institute remain distinct from descriptions of those acts and relations.
4. **`A7CP-04 Epistemic openness and fallibility`.** Evidence and reliance may remain unresolved without turning unresolved evidence into a third world-side obtaining mode.
5. **`A7CP-05 Representation boundary`.** Descriptions, logical forms, database rows, graphs, and publications represent or carry claims under exact relations; their form does not prove the represented ontic.
6. **`A7CP-06 Agency and work attribution`.** A `U.MethodDescription` episteme describes an admitted `U.Method`; for a precise performed-Work claim, recover each exact actual performer through A.13 and let A.15.1 independently admit the dated `U.Work`. Only when the claim or its receiving use expressly consumes precise assignment-bound attribution does F.6 separately relate that Work to the same obtaining A.13 assignment; F.6 identifies neither the assignment nor the performer, neither the system-role kind nor the assignment acts, and missing or failed F.6 leaves the Work intact. A result follows only through its own separately established relation—for example, a production, operation-result, measurement, evaluation, decision, delivery, or acceptance relation—not from Work in general.
7. **`A7CP-07 Kind discipline`.** Use direct existing kinds and local admission before proposing a universal kind, root relation, or role-like surrogate.
8. **`A7CP-08 Scoped pluralism`.** Different source traditions or apparatuses may be useful for different receiving claims; compatibility is tested by consequences, not achieved through prestige hierarchy.
9. **`A7CP-09 Structure and wholeness`.** A description of structure is not the structure; not every construction is mereology, and `C.13` alone defines constructional mereology.
10. **`A7CP-10 Time, identity, and currentness`.** World-side temporal qualification, occurrence identity, claim/publication currentness, and source supersession are separate questions.
11. **`A7CP-11 Subject-pattern separation`.** Capability, state, architecture, role, method, work, evidence, permission, and relation families retain their subject patterns even when an ontology method diagnoses a conflict among them.
12. **`A7CP-12 Formal projection non-reversal`.** CT2R and formalization may preserve, collapse, or omit structure. Logical validity or representation form does not reverse-infer a unique world construction.

The twelve IDs form a stable closed compact in this pattern. They are not steps, completeness criteria for every ontology use, or twelve intrinsic premise kinds.

### A.7.CP:4.2 - Record actual reasoning-basis use {#record-actual-reasoning-basis-use}

`Premise` and `assumption` name postures of exact claim use, not disjoint claim kinds.

```text
ClaimUsedAsReasoningBasisRelation@Context <: U.Relation

RelationSignature:
  BasisClaimSlot:
    SlotKind: BasisClaimSlot
    ValueKind: U.Episteme
    refMode: U.EpistemeRef
  ReasoningWorkSlot:
    SlotKind: ReasoningWorkSlot
    ValueKind: U.Work
    refMode: WorkRef
  ReceivingReasoningResultSlot:
    SlotKind: ReceivingReasoningResultSlot
    ValueKind: U.Episteme
    refMode: U.EpistemeRef

semanticDirection: BasisClaimSlot -> ReceivingReasoningResultSlot
  through the named ReasoningWorkSlot
ReasoningBasisPostureValue ::= adoptedPremise | conditionalAssumption

RelationOccurrenceQualifiers:
  basisClaimAddress: ClaimAddress
  posture: ReasoningBasisPostureValue
  reasoningUseScope?: U.ClaimScope
  modelUseStructureRef?: U.StructureRef

OccurrenceIdentity:
  <exact basis-claim edition and claim ID,
   exact reasoning-work occurrence,
   exact receiving-result edition,
   posture,
   reasoningUseScope when present,
   maximalContinuousRelianceInterval>
```

`BasisClaimSlot` is the exact claim-bearing episteme used, and `basisClaimAddress` is a `C.2.1 ClaimAddress` selecting the exact claim inside that same edition by its intrinsic ClaimGraph identity. `ReasoningWorkSlot` is the dated reasoning, choice, ontology-analysis, or reconciliation `U.Work` that relies on it. `ReceivingReasoningResultSlot` is the claim, comparison, decision, or other claim-bearing result episteme whose content that Work forms or revises using the basis claim. If the practical result is world-side, use the direct result claim that bears on it; the world-side object retains its subject pattern. Use A.13 to identify the admitted `U.System` that performs the Work and retain the obtaining occurrence of the separately declared `U.SystemRoleAssignment` species used by A.13. Recover the obtaining F.6 attribution for that exact Work-assignment pair only when the claim or its receiving use expressly consumes precise assignment-bound attribution; the assignment holder must be the same System. The assignment's existence, holder, or interval does not establish that attribution; the independently identified System performs the Work. Claim episteme, described Method when one is used, Work occurrence, assignment occurrence, attribution, use posture, receiving result, and any world-side result remain distinct. The words “premise” and “assumption” are not relation participants.

The relation obtains during the maximal continuous interval in which the named work actually relies on the exact basis claim to form or revise the exact receiving result. Access, citation, publication, co-location, or use of the claim elsewhere in the same work is insufficient. `reasoningUseScope` appears only when this premise use is narrower than or otherwise differs from the receiving result's declared claim scope; `modelUseStructureRef` appears only when an independently selected `BoundedModelUseStructure` changes interpretation. Source currentness, evidence, publication, work method, and the receiving result's own governance remain with their subject patterns.

One occurrence is identified by the exact basis-claim edition and ID, reasoning-work occurrence, receiving-result edition, posture, optional narrower use scope, and maximal continuous reliance interval. If one work uses the same basis claim for two independent results, record two relation occurrences that share the work participant but name different receiving results; do not duplicate the work. A change to any identity value ends or splits only the affected result-specific occurrence.

### A.7.CP:4.3 - Keep posture and transition explicit {#keep-posture-and-transition-explicit}

`adoptedPremise` means the named work presently uses the basis claim as accepted support for the exact receiving result. `conditionalAssumption` means the work uses it for that result only in a narrower model, scenario, proof, or branch with an explicit test, defeater, or reopen condition. Every conditional assumption actually used can function as a premise inside that bounded subargument; not every adopted premise is conditional. Neither posture changes the basis-claim episteme's intrinsic kind.

The same claim can have different postures in different work or for different receiving results of one work. A posture transition creates a later occurrence only for the exact receiving result on that relation edge. Reopen that result and its dependents; another result of the same work remains closed when its separate premise-use occurrence and posture did not change.

### A.7.CP:4.4 - Use the cheapest truthful path {#use-the-cheapest-truthful-path}

1. Name the exact reasoning work and each exact receiving claim, decision, comparison, or other claim-bearing result it is forming.
2. For each receiving result, cite only the compact IDs that are load-bearing.
3. Record one relation occurrence per exact basis claim, receiving result, posture, and continuous reliance interval; reuse the same work reference across independent results.
4. Name a narrower `U.ClaimScope` or selected `BoundedModelUseStructure` only when it changes this premise use.
5. Keep evidence, currentness, source use, kind admission, subject construction, work method, and result governance with their subject patterns.
6. Stop when every load-bearing receiving result points to its exact premise-use occurrences. Do not inspect unused compact entries.

## A.7.CP:7 - Conformance Checklist {#conformance-checklist}

| ID | Check |
|---|---|
| `CC-A7CP-1` | @fact:CC-A7CP-1 Every relation occurrence names one exact basis-claim episteme/ID, dated reasoning-work occurrence, exact receiving-result episteme, posture, optional narrower use scope, and maximal continuous reliance interval. @status:spec/done |
| `CC-A7CP-2` | @fact:CC-A7CP-2 The work actually relies on the claim for that exact receiving result; citation, access, publication, or use elsewhere in the work is insufficient. @status:spec/done |
| `CC-A7CP-3` | @fact:CC-A7CP-3 `adoptedPremise` and `conditionalAssumption` are use postures, not intrinsic claim kinds. @status:spec/done |
| `CC-A7CP-4` | @fact:CC-A7CP-4 A posture or identity change splits only the affected result-specific relation occurrence and reopens that receiving result and its dependents. @status:spec/done |
| `CC-A7CP-5` | @fact:CC-A7CP-5 Consumers cite only load-bearing claim IDs and do not copy the compact. @status:spec/done |
| `CC-A7CP-6` | @fact:CC-A7CP-6 The support pattern is not a Method, performer, work plan, result, or mandatory catalogue traversal. A `U.MethodDescription` episteme may declare a premise or branch condition for its described Method, but only an admitted `U.System` performs dated reasoning Work. Any assignment, F.6 attribution, and result relation used by the case must obtain separately. @status:spec/done |
| `CC-A7CP-7` | @fact:CC-A7CP-7 Evidence, currentness, source use, subject construction, kind admission, and work method remain with subject patterns. @status:spec/done |
| `CC-A7CP-8` | @fact:CC-A7CP-8 The twelve compact claims retain their stable IDs and contents as one closed support set. @status:spec/done |

## A.7.CP:9 - Consequences {#consequences}

The compact makes broad constructive reliance recoverable without enlarging current `A.7` or creating copied foundation variants. Ordinary users pay nothing unless a claim is actually load-bearing. The cost is precise claim/work/posture identity in consequential reasoning; the benefit is one stable authoritative content source and bounded reopen.

## A.7.CP:12 - Relations {#relations}

- **Defines:** the twelve `A7CP-*` constructive claim contents and `ClaimUsedAsReasoningBasisRelation@Context`, whose direct result-specific edge states that dated reasoning work used one exact basis claim to form or revise one exact receiving result episteme.
- **Is consumed by:** dated Work applying the Methods described by `A.7.1` or `A.7.2`, which cites exact compact claims and exposes relation occurrences only for load-bearing actual reliance. The A.7.1 and A.7.2 `U.MethodDescription` epistemes may separately declare premises or branch conditions for their described Methods; neither MethodDescription nor Method is a participant of `ClaimUsedAsReasoningBasisRelation@Context`.
- **Coordinates with:** current `A.7` for its existing strict distinctions without broadening its EntityOfConcern, first move, Solution, or cases.
- **Preserves subject patternship in:** `A.10` and `G.11` for evidence/currentness, `E.24`/`E.24.UK` for ontology admission, subject construction patterns for constructive settlement, and `A.7.2` for ontology source-use relations.
- **Does not define:** a premise method, source authority, evidence relation, work plan, performer kind, common realism checklist, or universal foundation ontology.


## Dependencies {#dependencies}

- @fact:SUPPORT-OWNER-CONSUMED-BY Support owner consumed by: spec://ai.lev/fpf-spec/contract/A-7-1#root and spec://ai.lev/fpf-spec/contract/A-7-2#root when one exact compact claim is load-bearing in dated reasoning Work. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-7-1#root, spec://ai.lev/fpf-spec/contract/A-7-2#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/A-7-CP
