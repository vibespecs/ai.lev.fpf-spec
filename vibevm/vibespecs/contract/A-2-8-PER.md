# A.2.8.PER - Granted Permission, Exercise, and Non-Prohibition {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Definitional ontic support pattern
> **Status:** Stable
> **Normativity:** Normative unless marked informative

## A.2.8.PER:0 - Use this when {#use-this-when}

Use this pattern when a policy, approval, permit, system-role rule, boundary claim, readiness check, or later work use needs to distinguish five questions:

- whether a sufficiently complete current frame supports a `NonProhibitionFinding@Context`;
- whether a valid grant currently obtains as `GrantedPermissionRelation@Context`;
- whether dated matching work exercises it through `PermissionExerciseRelation@Context`;
- whether checked actual work supports a `NonViolationFinding@Context`; and
- whether an incompatible current grant and norm require `PermissionNormConflictFinding@Context`.

First select the result needed now. Recover the inputs required by its declaration in §§4.2–4.6 and establish that result under its own rule. Do not infer a different result from the selected one.

**Not this pattern when.** Use `A.2.8` for one actual bearer's obligation, recommendation-as-duty, or prohibition; `A.2.9` for the communicative work that institutes or revokes a grant; `A.6.B` for L/A/D/E classification; `A.15.5` for work-entry readiness; `A.21` for gate decisions; and `A.15.1` for the identity and result of performed work.

The primary reader is a policy, boundary, work-planning, assurance, or operations practitioner who must decide exactly what a permission-looking claim can support. The performer of a grant speech act or later Work remains an admitted system under one exact obtaining system-role assignment.

## A.2.8.PER:1 - Problem frame {#problem-frame}

Permission-looking language often compresses unlike values. “No rule forbids it” may be an incomplete search result. “The permit allows it” may refer to a document, an issuing act, or an enduring relation. “We used the permit” may mean only that a badge was visible, while no matching work occurred. A green gate can also look as if it defeated a current prohibition.

The concern is the smallest exact permission result needed for one beneficiary, action specification, normative-frame edition, ClaimScope, intended use, and window. The act, permit episteme, publication carrier, evidence relation, admissibility predicate, readiness relation, gate decision, actual Work, and work result remain distinct and are handled under their respective subject patterns.

## A.2.8.PER:2 - Problem {#problem}

How can FPF represent positive permission without turning it into an obligation modality, absence-of-evidence claim, permit document, gate result, readiness label, capability, or performed action?

A conforming account must make weak and strong permission different, keep grant occurrence identity inspectable, connect only eligible matching work to a current grant, keep both exercise and non-exercise from establishing a frame-relative non-violation finding, and expose same-scope normative conflicts instead of resolving them by display or wording.

## A.2.8.PER:3 - Forces {#forces}

| Force | Tension |
|---|---|
| Latitude vs duty | Permission makes an action allowable; it does not require the action. |
| Weak evidence vs world relation | A complete-frame search can support non-prohibition, while an incomplete search is unresolved. |
| Enduring grant vs instituting act | A speech act can ground a permission without being the continuing relation. |
| Beneficiary variety vs kind discipline | System-role kinds, exact assignment occurrences, and parties all occur in practice, but one generic beneficiary U-kind would erase their different eligibility tests. |
| Current grant vs actual exercise | A grant may obtain without work; work may occur without matching or exercising the grant. |
| Local policy vs visible artifacts | A permit or gate display is easy to see, but scope, window, currentness, revocation, and precedence decide use. |

## A.2.8.PER:4 - Solution {#solution}

### A.2.8.PER:4.1 - Keep the permission objects separate {#keep-the-permission-objects-separate}

Use exactly the object warranted by the current claim:

- `NonProhibitionFinding@Context` is a frame-relative episteme returned before action when a sufficiently complete current normative frame contains no applicable prohibition.
- `GrantedPermissionRelation@Context` is an enduring strong permission instituted under an exact policy.
- `PermissionExerciseRelation@Context` connects actual dated work to one obtaining grant occurrence when action and beneficiary eligibility match.
- `NonViolationFinding@Context` is a frame-relative episteme about actual work that instantiates no applicable prohibition in the checked frame.
- `PermissionNormConflictFinding@Context` is an episteme exposing an incompatible current grant and prohibition or commitment over matching content, scope, and window.

Absence of any one object does not imply another. In particular, no grant is inferred from a weak finding, no exercise is inferred from a grant, and work outside a grant is not called a violation of that grant.

### A.2.8.PER:4.2 - Use the closed beneficiary reference family {#use-the-closed-beneficiary-reference-family}

```text
PermissionBeneficiaryRef ::=
  exactly one branch is present:
    beneficiarySystemRoleKindRef?: U.KindRef resolving to one exact local system-role kind
    beneficiarySystemRoleAssignmentRef?: U.RelationRef constrained to U.SystemRoleAssignment
    beneficiaryPartyRef?: PartyRef
```

The entity designated by the grant is its beneficiary. Apply the exercise-eligibility test for its reference branch:

- `beneficiarySystemRoleAssignmentRef` names one assignment occurrence and its declared species and applies only to that occurrence.
- `beneficiarySystemRoleKindRef` names one exact local system-role kind; the policy states which current assignments to that kind make an actual performer eligible.
- `PartyRef` covers work only when its exact performer or on-behalf-of relation satisfies the policy. Shared naming or organizational membership is insufficient.

This is a closed ref union over admitted `U.Entity` values, not `U.PermissionBeneficiary`, `U.Authorization`, or another new U-kind. A materially different beneficiary meaning requires a separate decision under the applicable subject pattern.

### A.2.8.PER:4.3 - Record weak permission and non-violation as findings {#record-weak-permission-and-non-violation-as-findings}

```text
NonProhibitionFinding@Context <: U.Episteme
  beneficiaryRef: PermissionBeneficiaryRef
  permittedActionSpecificationRef: U.EpistemeRef
  normativeFrameRef: U.EpistemeRef
  frameCurrentnessResultRef: U.EpistemeRef
  frameCompletenessForUseResultRef: U.EpistemeRef
  scope: U.ClaimScope
  intendedUse:
  evaluationWindow: QualificationWindowPolicy
  checkedProhibitionAddresses: set<ClaimAddress>
  result: nonProhibited | unresolved
  evaluationWorkRef: WorkRef

NonViolationFinding@Context <: U.Episteme
  workRef: WorkRef
  performerSystemRoleAssignmentRefs: set<U.RelationRef constrained to U.SystemRoleAssignment>
  onBehalfOfRelationOccurrenceRef?: U.RelationRef constrained to the direct on-behalf-of relation kind
  normativeFrameRef: U.EpistemeRef
  frameCurrentnessResultRef: U.EpistemeRef
  frameCompletenessForUseResultRef: U.EpistemeRef
  scope: U.ClaimScope
  intendedUse:
  evaluationWindow: QualificationWindowPolicy
  checkedProhibitionAddresses: set<ClaimAddress>
  result: nonViolating | unresolved
  evaluationWorkRef: WorkRef
```

`nonProhibited` and `nonViolating` are admissible only when the named frame is current and explicitly sufficiently complete for the intended use. Otherwise the finding is `unresolved`. Neither finding institutes permission or proves absence outside its frame.

Every `ClaimAddress` in this pattern means the reusable `C.2.1 ClaimAddress`: an exact episteme-edition reference plus an intrinsic claim identity declared by that edition's ClaimGraph. A heading, row number, file location, or printed token is insufficient.

For `NonViolationFinding@Context`, recover the performer Systems from the named Work and cite each covering assignment occurrence and its declared `U.SystemRoleAssignment` species. If the checked norm instead turns on Work done for a `PartyRef`, cite the obtaining on-behalf-of relation defined in its pattern. These are case facts used by the evaluation. Omit the on-behalf-of reference when no such branch is used.

### A.2.8.PER:4.4 - Declare the strong granted-permission relation {#declare-the-strong-granted-permission-relation}

```text
GrantedPermissionRelation@Context <: U.Relation

RelationSignature:
  PermissionBeneficiarySlot:
    SlotKind: PermissionBeneficiarySlot
    ValueKind: U.Entity
    refMode: PermissionBeneficiaryRef
  PermittedActionSpecificationSlot:
    SlotKind: PermittedActionSpecificationSlot
    ValueKind: U.Episteme
    refMode: U.EpistemeRef

semanticDirection: PermissionBeneficiarySlot -> PermittedActionSpecificationSlot

RelationOccurrenceGroundAndQualifiers:
  institutingSpeechActRef: SpeechActRef
  grantorSystemRoleAssignmentRef: U.RelationRef constrained to U.SystemRoleAssignment
  grantValidityPolicyRef: U.EpistemeRef
  scope: U.ClaimScope
  validityWindow: QualificationWindowPolicy
  revocationOrSupersessionRef?: SpeechActRef
```

The beneficiary and permitted-action specification are participants. The grantor system-role assignment, instituting act, policy, ClaimScope, validity window, and revocation are constructive grounds or qualifiers.

The relation begins only when an admitted holder `U.System` performs a `U.SpeechAct` under the exact `grantorSystemRoleAssignmentRef`, the act satisfies the current policy's grant-validity predicate, and it institutes permission for the named participants. The assignment's `HolderSystemSlot` resolves to that system: the system performs the act, while the assignment supplies only the holder and assigned-kind fact used by the policy. Any authority claim required by the policy obtains independently. The relation obtains while beneficiary applicability, policy continuation, scope, and window hold and no valid revocation or supersession ends it.

One occurrence is identified by the instituting speech-act occurrence, exact beneficiary ref and ref kind, action-specification edition, policy edition, ClaimScope, and effective interval. Beneficiary change, renewal, materially changed action specification, non-carried policy edition, or revocation ends or splits the occurrence. A policy edition preserves it only through an explicit satisfied carry-forward rule.

### A.2.8.PER:4.5 - Declare actual exercise {#declare-actual-exercise}

```text
PermissionExerciseRelation@Context <: U.Relation

RelationSignature:
  ExercisingWorkSlot:
    SlotKind: ExercisingWorkSlot
    ValueKind: U.Work
    refMode: WorkRef
  GrantedPermissionOccurrenceSlot:
    SlotKind: GrantedPermissionOccurrenceSlot
    ValueKind: U.Relation
    refMode: U.RelationRef constrained to GrantedPermissionRelation@Context
      // resolves to one exact obtaining grant occurrence

semanticDirection: ExercisingWorkSlot -> GrantedPermissionOccurrenceSlot

RelationOccurrenceQualifiers:
  beneficiarySystemRoleAssignmentRef?: U.RelationRef constrained to U.SystemRoleAssignment
  onBehalfOfRelationOccurrenceRef?: U.RelationRef constrained to the direct on-behalf-of relation kind
  exerciseScope: U.ClaimScope
  exerciseInterval: QualificationWindowPolicy
```

Decide exercise from two observable questions about the existing objects: **did this dated Work instantiate the grant's permitted-action specification, and did its actual performer satisfy the grant's beneficiary branch?** For a `beneficiarySystemRoleAssignmentRef` branch, the named assignment must cover the Work and have that performer as holder. For a `beneficiarySystemRoleKindRef` branch, `beneficiarySystemRoleAssignmentRef` names the exact covering assignment whose declaration-local kind slot contains that kind and which satisfies the policy's eligibility rule for that kind. For a `beneficiaryPartyRef` branch, the performer must be that party or `onBehalfOfRelationOccurrenceRef` must cite the already obtaining relation whose predicate is defined by its subject pattern and whose use is licensed by the policy. If either question fails, this exercise relation does not obtain.

The match and eligibility are direct obtaining predicates over the Work, grant, action specification, performer, and cited assignment or on-behalf-of relation. If a receiving assurance or audit use needs a separately recorded evaluation or evidence item, identify that item through the applicable evaluation or evidence-use relation; do not mint a placeholder episteme merely to fill this relation.

The exercise relation obtains only when those two predicates hold, the grant obtains throughout the exercise interval, and the work remains in scope. The work is a satisfier of permitted action content. Judge any obligation-satisfaction or discharge claim under the separate evaluation or compliance rule (A.2.8:4.6). The work consumes the grant only when the named policy explicitly makes it single-use or quota-bound.

Non-exercise leaves an obtaining grant unused and ordinarily still obtaining; it does not establish `NonViolationFinding@Context`. Exercise establishes only the exercise relation and likewise does not establish that finding without the separate checked-frame evaluation. Work outside the action specification, beneficiary eligibility, scope, or window does not exercise the grant; any further consequence is established only by the applicable prohibition, commitment, admissibility, or Work-related predicate. If a decision is required, an admitted system performs the dated decision Work under the relevant Method, covering assignment, and authority relation.

### A.2.8.PER:4.6 - Expose conflict without inventing precedence {#expose-conflict-without-inventing-precedence}

```text
PermissionConflictResolutionResultRef ::= U.EpistemeRef
  // resolves only to PermissionConflictResolutionResult@Context

PermissionConflictResolutionResult@Context <: U.Episteme
  conflictFindingRef: U.EpistemeRef
  governingPrecedencePolicyRef: U.EpistemeRef
  resolutionWorkRef: WorkRef
  deciderSystemRef: U.EntityRef
  deciderSystemRoleAssignmentRef: U.RelationRef constrained to U.SystemRoleAssignment
  decisionAuthorityRelationOccurrenceRef: U.RelationRef constrained to the direct decision-authority relation kind
  selectedGrantOccurrenceRef?: U.RelationRef constrained to GrantedPermissionRelation@Context
  selectedNormClaimAddress?: ClaimAddress
  effectiveScope: U.ClaimScope
  effectiveWindow: QualificationWindowPolicy
  reopenConditionClaimAddress: ClaimAddress

PermissionNormConflictFinding@Context <: U.Episteme
  grantedPermissionOccurrenceRef: U.RelationRef constrained to GrantedPermissionRelation@Context
  conflictingNormClaimAddress: ClaimAddress
  overlapScope: U.ClaimScope
  overlapWindow: QualificationWindowPolicy
  governingPrecedencePolicyRef: U.EpistemeRef
  applicablePrecedenceRuleAddress?: ClaimAddress
  decisionAuthorityRelationOccurrenceRef?: U.RelationRef constrained to the direct decision-authority relation kind
  resolutionWorkRef?: WorkRef
  resolutionResultRef?: PermissionConflictResolutionResultRef
  blockedWorkOrRelianceRef: U.EntityRef
  disposition: unresolved | settledByApplicableRule | settledByDecisionResult
  reopenConditionClaimAddress: ClaimAddress
```

Create the finding only when the grant and current prohibition or commitment concern the same beneficiary/action content, overlapping scope/window, and incompatible practical conclusions. Check that match directly from the two claims and their participants. Permission and an obligation to perform the same action are not automatically in conflict.

Resolve the conflict through exactly one of two branches:

1. **The current policy already decides.** `applicablePrecedenceRuleAddress` cites the policy claim whose stated conditions match this beneficiary, action, scope, and window. Set `settledByApplicableRule` only when that rule itself selects which claim governs the blocked use.
2. **A decision is required.** Name the admitted `U.System` that decides, the covering assignment under which it performs the dated `resolutionWorkRef`, and the independently obtaining authority relation whose predicate is defined by its subject pattern and which authorizes this decision. The direct result relation for that decision must connect the Work to a current `PermissionConflictResolutionResult@Context` selecting either the grant occurrence or the conflicting norm claim for the stated scope/window.

`PermissionConflictResolutionResult@Context` is the exact decision result for this conflict. Exactly one of `selectedGrantOccurrenceRef` or `selectedNormClaimAddress` is filled. Its `deciderSystemRoleAssignmentRef` must cover `resolutionWorkRef` and have `deciderSystemRef` as holder; `decisionAuthorityRelationOccurrenceRef` must independently authorize that decision. If no policy rule decides and no such current result exists, the disposition remains `unresolved`, even when a responsible office or system-role kind is named. Permit text, readiness, or a passing gate does not silently defeat the prohibition.

### A.2.8.PER:4.7 - Keep the handshakes narrow {#keep-the-handshakes-narrow}

| Neighboring object | Exact handshake |
|---|---|
| Grant or revoke act | `A.2.9 U.SpeechAct <: U.Work`; an admitted holder `U.System` performs the act under the exact grantor system-role assignment, and `institutes.permissions` cites the grant occurrence. The assignment supplies the holder and assigned-kind ground; any required authority is established through its own relation. The act and enduring grant retain their separate identities. |
| Permit episteme and carrier | Use `C.2.1` for claims about the permission, `E.17` for a source-backed publication face, `G.11` for source currentness and publication refresh, and `A.10` for evidence used in reliance. Use `E.24.PUB` when the publication occurrence, form, or carrier identity matters. |
| Duty or prohibition | `A.2.8 U.Commitment`; permission remains outside its modality family. |
| Boundary claim or entry predicate | `A.6.B` classifies the claim; an `A-*` predicate may consume a separately established current permission result. |
| Work plan and readiness | `A.15.2` is the pattern for the `U.WorkPlan`; `A.15.5` may cite a separately established permission/conflict result as one readiness input. |
| Gate decision | Use `A.21` for a gate outcome, citing the separate current grant or conflict result whenever its profile requires one. |
| Work and result | identify the dated Work under `A.15.1`. Exercise requires the direct relation above. Claims of capability, readiness, safety, success, or result quality need their own predicates. |

## A.2.8.PER:7 - Conformance Checklist {#conformance-checklist}

| ID | Check |
|---|---|
| `CC-A2.8.PER-1` | @fact:CC-A2-8-PER-1 The current result is exactly `NonProhibitionFinding@Context`, `GrantedPermissionRelation@Context`, `PermissionExerciseRelation@Context`, `NonViolationFinding@Context`, or `PermissionNormConflictFinding@Context`. @status:spec/done |
| `CC-A2.8.PER-2` | @fact:CC-A2-8-PER-2 Beneficiary selects exactly one of `beneficiarySystemRoleKindRef : U.KindRef`, `beneficiarySystemRoleAssignmentRef : U.RelationRef constrained to U.SystemRoleAssignment`, or `beneficiaryPartyRef : PartyRef`, with its branch-specific eligibility test. The branch record is not a new beneficiary U-kind. @status:spec/done |
| `CC-A2.8.PER-3` | @fact:CC-A2-8-PER-3 A strong grant names the admitted `U.System` that performs the instituting act, the exact grantor system-role assignment whose `HolderSystemSlot` resolves to that system, participants, policy edition, ClaimScope and validity window, currentness, and occurrence identity. Any required authority relation obtains independently. @status:spec/done |
| `CC-A2.8.PER-4` | @fact:CC-A2-8-PER-4 Weak findings require a current frame explicitly complete enough for the intended use; incompleteness returns `unresolved`. @status:spec/done |
| `CC-A2.8.PER-5` | @fact:CC-A2-8-PER-5 Exercise names dated work, the admitted `U.System` that performed it, the one current grant occurrence through a `U.RelationRef` constrained to `GrantedPermissionRelation@Context`, scope, and interval; it answers action match and beneficiary eligibility from those objects and the exact covering assignment or on-behalf-of relation. @status:spec/done |
| `CC-A2.8.PER-6` | @fact:CC-A2-8-PER-6 Neither exercise nor non-exercise establishes `NonViolationFinding@Context`; non-exercise is not violation, and exercise is not obligation satisfaction and does not consume a grant without an explicit policy. @status:spec/done |
| `CC-A2.8.PER-7` | @fact:CC-A2-8-PER-7 A same-scope conflict is settled only by an applicable policy rule that selects the outcome or by a current resolution result produced by dated Work of an admitted system under a covering system-role assignment and independently obtaining decision-authority relation. Naming a policy, office, system-role kind, assignment, or “owner” alone leaves only the affected Work or reliance use `unresolved`. @status:spec/done |
| `CC-A2.8.PER-8` | @fact:CC-A2-8-PER-8 Permit episteme, carrier, evidence, admissibility, readiness, gate, capability, Work, and result remain distinct and are handled under their respective subject patterns. @status:spec/done |

## A.2.8.PER:9 - Consequences {#consequences}

Permission becomes inspectable without being inflated into a universal authorization ontology. Practitioners can distinguish a tentative frame-relative result from an enduring grant and from actual exercise, and can stop on unresolved conflict without letting a gate or permit display choose precedence. The cost is recording enough policy, identity, scope, window, and eligibility detail to support the intended use.

## A.2.8.PER:12 - Relations {#relations}

- **Coordinates with:** `A.2.8` for obligations, recommendations-as-duty, and prohibitions; `A.2.9` for instituting or revoking speech acts; and `A.6.B` and `A.6.C` for deontic claim classification and agreement-like boundary-language unpacking.
- **Supplies inputs to:** `A.15.5` readiness and direct mechanism/gate checks only when their own predicates explicitly consume a current grant, finding, or conflict result.
- **Relates to work through:** `A.15.1` for dated `U.Work` identity and `PermissionExerciseRelation@Context` for the separate exercise claim.
- **Uses evidence from:** `A.10` and publication/currentness patterns for claims about the permission relation and its permit carriers.
- **Does not replace:** system-role kind or assignment, capability, plan, gate, admissibility, policy precedence, evidence, performed Work, result, safety, assurance, responsibility, authority, access, or commitment patterns.


## Dependencies {#dependencies}

- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/A-2-8#root, spec://ai.lev/fpf-spec/contract/A-2-9#root, spec://ai.lev/fpf-spec/contract/A-13#root, spec://ai.lev/fpf-spec/contract/F-6#root, spec://ai.lev/fpf-spec/contract/A-6#root, spec://ai.lev/fpf-spec/contract/A-6-B#root, spec://ai.lev/fpf-spec/contract/A-6-C#root, spec://ai.lev/fpf-spec/contract/A-15-1#root, spec://ai.lev/fpf-spec/contract/A-15-5#root, spec://ai.lev/fpf-spec/contract/A-10#root. Does not replace policy, system-role kind or assignment, capability, plan, gate, Work, evidence, or commitment patterns. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-15-4#root, spec://ai.lev/fpf-spec/contract/A-15-5#root, spec://ai.lev/fpf-spec/contract/A-2-8#root, spec://ai.lev/fpf-spec/contract/A-6-B#root, spec://ai.lev/fpf-spec/contract/A-6-C#root, spec://ai.lev/fpf-eng-adm/contract/ADM-8#root, spec://ai.lev/fpf-spec/contract/E-10#root, spec://ai.lev/fpf-eng-fdm/contract/FDM-1#root, spec://ai.lev/fpf-eng-me/contract/ME-10#root, spec://ai.lev/fpf-eng-mnt/contract/MNT-1#root, spec://ai.lev/fpf-eng-mnt/contract/MNT-11#root, spec://ai.lev/fpf-eng-mnt/contract/MNT-8#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/A-2-8-PER
