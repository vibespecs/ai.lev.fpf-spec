# A.2.8.PER - Granted Permission, Exercise, and Non-Prohibition: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## A.2.8.PER:5 - Archetypal Grounding {#archetypal-grounding}

**Assignment, permission, access, and authority.** `AdminAssignment` is a declared `U.SystemRoleAssignment` species. Occurrence `AdminAssignment-4` has admitted System `ServiceOperator-4` as holder and `AdminSystemRole` as assigned-kind value. That fact alone establishes no grant, access, or decision authority. A policy-valid speech act can separately institute one `GrantedPermissionRelation@Context` for `AdminSystemRole`, `RestartServiceActionSpec`, the declared scope, and the declared window. Matching dated Work exercises that grant only through a separate `PermissionExerciseRelation@Context`. If service access is claimed, cite its domain access predicate and participants; when no such predicate is available, return `A.6.RCD missing-governor[direct service-access relation]`. Permission, exercise, access, authority, assignment, and Work therefore remain separate.

**Strong grant and exercise.** `PlantPermissionGrantorAssignment` is a declared `U.SystemRoleAssignment` species. Occurrence `MaintenanceCoordinator-A@DayShift` has admitted System `MaintenanceCoordinator-A` as holder, and that System performs a policy-valid grant speech act under the assignment. The act institutes `MaintenanceCalibrationGrant-2026-07-19 : GrantedPermissionRelation@Context` for `MaintenanceTechnicianSystemRole` to run `CalibrationProcedure-v3` during one service window. Its beneficiary uses `beneficiarySystemRoleKindRef`.

`PlantCalibrationTechnicianAssignment` is another declared species. Occurrence `Tech-17@Shift-B` has admitted technician System `Tech-17` as holder and `MaintenanceTechnicianSystemRole` as assigned-kind value. `Tech-17` performs dated `CalibrationWork-17B` under that assignment. The Work instantiates `CalibrationProcedure-v3` within the grant's zone, window, and scope, so the action-match predicate holds. The assignment covers the Work and satisfies the policy's eligibility rule for that kind, so the beneficiary predicate holds.

`CalibrationExercise-17B : PermissionExerciseRelation@Context` therefore connects `CalibrationWork-17B` to `MaintenanceCalibrationGrant-2026-07-19`, cites `beneficiarySystemRoleAssignmentRef=Tech-17@Shift-B`, and states the Work interval and scope. The assignments supply holder and assigned-kind facts for the grant and Work attribution; any required authority relation obtains independently. The grant remains current for the rest of the window because the policy is not single-use. Claims about obligation, readiness, capability, gate passage, a safe result, or successful calibration need their own grounds.

**Weak finding.** A policy reviewer checks a named, current, sufficiently complete plant-access frame and finds no prohibition applicable to the exact system-role kind, action specification, zone, and window. The result is `NonProhibitionFinding@Context(result=nonProhibited)`, not an instituted grant. If the emergency-policy register cannot be checked, the result is `unresolved`.

**Actual-Work non-violation.** After `CalibrationWork-17B` is performed, `CalibrationComplianceEvaluation-17B : U.Work` checks that Work against `PlantCalibrationNormativeFrame-2026-07-19-e3`, whose currentness and sufficient completeness for the technician, procedure, zone, and service-window use are named and whose applicable prohibitions are checked. The result is `NonViolationFinding@Context(workRef=CalibrationWork-17B, performerSystemRoleAssignmentRefs={Tech-17@Shift-B}, normativeFrameRef=PlantCalibrationNormativeFrame-2026-07-19-e3, evaluationWorkRef=CalibrationComplianceEvaluation-17B, result=nonViolating)`. The covering assignment already relates the performer system to the beneficiary system-role kind. The separate exercise relation shows which grant the Work exercised; exercise alone does not establish non-violation, and non-exercise alone does not establish it either. If the frame is stale or insufficiently complete for this use, the non-violation result is `unresolved`.

**Conflict and non-use.** The system-role-kind-level calibration grant still obtains under §4.4 while `ContaminatedZoneEntryProhibition-7` forbids the same beneficiary and calibration action in Zone 7 during an overlapping interval. In the direct-rule case, `EmergencyCalibrationPrecedencePolicy-e5` contains applicable claim `CZ7-Prohibition-Overrides-CalGrant`. The rule's conditions match, so the finding is `settledByApplicableRule`, cites that rule, and returns “do not enter Zone 7” for the blocked Work.

In a discretionary Zone 8 case, `PlantSafetyDecisionAssignment` is a declared `U.SystemRoleAssignment` species. Occurrence `SafetyDirector-3@EmergencyShift` has admitted System `SafetyDirector-3` as holder, and that System performs `CalibrationConflictDecisionWork-8` under the assignment. The separately obtaining `PlantEmergencyExceptionAuthority-8` relation authorizes that decision, and current `CalibrationConflictResolutionResult-8` selects the prohibition claim for the stated scope and window. Only then is the finding `settledByDecisionResult`.

A second Zone 8 request that merely names the Safety Director but has no dated decision Work or current result remains `unresolved`. A visible permit and green readiness tile cannot repair either gap. If no calibration Work occurs, the permission is neither exercised nor violated.

## A.2.8.PER:6 - Bias-Annotation {#bias-annotation}


The chief bias is document-and-display authority: a readable permit, badge, policy response, or green gate looks stronger than its recoverable relation. The repair is exact ground, participants, policy/currentness, scope/window, and separate evidence. A second bias is obligation-shaped deontics; the exercise and non-exercise rules preserve permission as latitude.

## A.2.8.PER:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Repair |
|---|---|
| `MAY` stored as a `U.Commitment` modality | Recover whether the claim is a strong grant, weak finding, entry predicate, or ordinary prose; use the applicable subject pattern. |
| No prohibition found, therefore permission | Require currentness and frame completeness; otherwise return `unresolved`. |
| Permit document as permission | Recover the instituting act, current grant occurrence, policy, scope/window, and evidence relation. |
| Gate pass as authorization | Keep `GateDecisionResult` in `A.21`; cite a separate grant/conflict result when the gate actually consumes one. |
| Permission as readiness or capability | Keep readiness in `A.15.5` and capability in `A.2.2`; permission supplies neither. |
| Work “violates permission” | Test exercise coverage and any separately governed prohibition; uncovered work is not a permission violation by default. |
| Unnecessary evaluation records for action match or beneficiary eligibility | Test the Work against the action specification and the performer against the beneficiary branch; cite the already obtaining assignment or on-behalf-of relation and add separate evaluation evidence only when a receiving use needs it. |
| Precedence “owner” as resolution | Apply a policy rule that itself selects the outcome, or name the authorized system's dated decision Work and current conflict-resolution result; a system-role kind, office, assignment, or policy title alone decides nothing. |
| Hidden generic beneficiary kind | Keep the closed reference union and branch-specific eligibility checks. |

## A.2.8.PER:10 - Rationale {#rationale}

Positive permission has different satisfaction and failure behavior from obligation. A grant can obtain while unused; non-use ordinarily violates nothing; matching action can exercise the grant without discharging a duty. Separating weak findings, strong grants, and exercise preserves these practical consequences while using existing episteme, relation, speech-act, policy, work, and evidence-use patterns.

## A.2.8.PER:11 - SoTA-Echoing {#sota-echoing}

| Practice question | Current practice and source | FPF alignment | Disposition |
|---|---|---|---|
| How do weak and strong permission differ? | Moltmann (2024) distinguishes modal objects, strong permission, weak non-violation, and action satisfiers. | Separate frame-relative findings, instituted grants, and actual exercise; retain FPF subject patterns. | **Adapt.** Do not import modal objects, truthmakers, or possible worlds as U-kinds. |
| How should permission, duty, and prohibition remain distinct? | W3C ODRL 2.2 (2018) models permission, prohibition, duty, assignee, action, constraint, and policy separately. | Keep beneficiary, action specification, policy, scope/window, and duty/prohibition predicates and pattern locations explicit. | **Adapt.** FPF uses direct relations and epistemic findings rather than importing the ODRL information model wholesale. |
| What makes a policy decision usable? | NIST SP 800-207 (2020) and current policy-as-code practice separate subject, requested action, resource and operating facts, current policy, and decision evidence. | Exercise eligibility and conflict use are bounded by the exact beneficiary, action, normative-frame and policy editions, ClaimScope, window, and intended use. | **Adapt.** A policy response or gate display is not itself an enduring grant. |
| How should digital permit evidence be relied on? | W3C Verifiable Credentials Data Model 2.0 (2025) separates issuer, holder, verifier, status, proof, and relying context. | Permit publications enter `A.10` evidence/currentness paths and do not replace the grant relation. | **Adapt.** Credential form supplies neither permission nor exercise by itself. |



## A.2.8.PER:End {#end}
