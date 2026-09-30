# A.6.A - Affordance and Action-Invitation Precision Restoration (ACT-INV): depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## A.6.A:5 - Archetypal Grounding {#archetypal-grounding}

### A.6.A:5.1 - Tell {#tell}

Read an affordance-like sentence as a question about its intended meaning. The result can be an ordinary supported claim, a proposed action, an inquiry question, or an exact gap. Keep the subject conditions that make that result usable. An optional record can express the result but does not give different subjects one obtaining predicate.

### A.6.A:5.2 - Show (System case) {#show-system-case}

**Draft:** “The alarm calls for rollback.”

**Repair A — control and incident line**

Recover the proposed use: OpsTeam_Phoenix is considering RollbackMethod_R41 on Release_R41 in ProdCluster_EU_1 during RunWindow_RW. RollbackRunbook_R41 describes that Method. AlarmBundle_AB9 exposes the cue about ServiceState_S7; AnomalyPolicy_AP7 detected it. AlertTrace_91 and ErrorBudgetSeries_4 are candidate evidence for applying IncidentPolicy_IP2 over Horizon_H15m.

The first useful statement is: “Check whether the current incident-policy guard and authority permit this team to use RollbackMethod_R41 on Release_R41 in this window; the alarm alone does not settle that question.” If the rule and facts establish a required rollback, state that independently grounded duty or gate result. Otherwise retain the proposed action or the precise missing condition. Nothing in these supplied names asserts a performed rollback.

If the receiving operational review uses `VP.OperationsControl`, resolve its `U.ViewpointRef` under `OperationsControlScheme_2026`. `OperationsRollbackView_9` remains an independently identified C.2.1 episteme and a `U.View` only if its exact E.17.0 conformance obtains. These are optional, separately established references, not additional requirements to understand the alarm sentence.

**Recognizable near misses.** A runbook reference alone does not identify the Method selected for enactment. A viewpoint field does not make a dashboard a `U.View`. The alarm, a recovery note or a `PolicyHook` does not prove duty, gate passage or performed Work.

**Repair B — ecological and robot line**

**Draft:** “This handle affords pulling.”

Recover the proposed physical claim: ServiceRobot_R2 can pull DoorHandle_17 along Axis_A1 in Window_W1 while the door is closed, under the actual reach, grip and clearance conditions described by ReachEnvelope_RE2, GripClass_G1 and ClearanceProfile_CP3. The reach description is not the physical reach condition itself. PerceptionStack_PS4 is the detector; DepthFrame_883 and ContactModelRun_17 are candidate evidence.

**Result with the supplied information.** These names identify the question but provide neither the physical obtaining predicate nor its required readings. Return: “Can R2 pull this handle along A1 in W1 under the specified grip, clearance and reach conditions? The applicable physical rule and its supported inputs are still needed.” A rule that requires sufficient contact force or a collision-free path must say so and be supported by the relevant measurements or model result. Naming G1, CP3 or a model run does not establish those conditions.

When that subject rule and the evidence support the claim, return the qualified physical statement directly. If the receiving task instead needs an executable manipulation plan and already has a suitable domain method, use its required observations and constraint representation. Reuse any adequate existing interpretation; producing another recovery note adds nothing by itself. With the same robot, grip, clearance, reach and door facts, changing PS4 can change detection without changing the physical opportunity. Changing an operator cue can likewise change what the operator notices. Withdrawing the description changes its availability; it does not close the door or remove the opportunity. A different, information-constituted relation must be assessed under its own predicate rather than inferred from this physical case.

### A.6.A:5.3 - Show (Episteme case) {#show-episteme-case}

**Draft:** “This problem asks for a better question.”

**Repair A — epistemic probe line**

`ProblemFramingEpisode_PF3` is the framing account, `ResearchTeam_A` the intended inquirer and `Reviewer_A1` the detector of the problem. Keep `ExemplarPack_EP3`, `OpenIssueSet_O2`, `EpisodeNotes_3` and `CounterexampleCard_2` as its named source context.

For this worked case, take EP3 to compare detected and missed handle opportunities with the robot, grip and clearance facts fixed. O2 asks whether a changed physical opportunity or a changed detector explains the discrepancy. CounterexampleCard_2 records the same physical configuration with a different detection result. The recovered question is: “With the physical conditions held fixed, does changing PS4's detection configuration change which pulling opportunities are detected?” The counterexample motivates that inquiry; it does not already establish its answer or a general detector effect.

This question is the first useful result. If further question construction is needed, the team can select the already admitted `ContrastiveQuestioningMethod_Q2`; `ContrastiveQuestioning_Q2` is its separate MethodDescription. An explanatory prompt follows B.5.2.0 when its conditions hold. Choosing the inquiry, scheduling it and actually performing it remain separate claims. No invitation occurrence or compulsory `OptionSet` precedes the question.

**Repair B — closure-advance line**

**Draft:** “The draft is ready for formalization.”

Recover the proposed clarification: `AuthorCollective_C1` would express `DraftHypothesis_H7` using `TypedInvariantSet_V1` within `ClaimScope_G1`. `ReviewPanel_R4` points to `AmbiguityMemo_8` and `ReviewCommentSet_5` as grounds for that move.

Return the actual question: “Which unresolved claims in H7 can V1 express under G1, and which ambiguities would remain?” If the receiving rule establishes readiness, state its qualified result and the proposed action. The named memo and comments alone establish neither readiness, Formality F, acceptance nor performed formalization. A sufficient question can remain open without becoming a generic invitation record.

## A.6.A:6 - Bias-Annotation {#bias-annotation}

* **Gov bias:** this pattern may tempt authors to smuggle decisions into invitation language.
  *Mitigation:* explicit A.6.B claim classification and obligation barrier.
* **Arch bias:** an interpretation menu can be mistaken for one ontology of all action-oriented claims.
  *Mitigation:* recover each subject and its rule; make the menu and recovery record optional.
* **Ontology and episteme bias:** this pattern insists on separating invitation from evaluation, capability, commitment, and work.
  *Mitigation:* first separate a direct contrast from a cross-context semantic-correspondence claim; test F.9 only for the latter, and keep any bounded-use claim and optional F.9.1 reading note separate.
* **Prag bias:** it favors enactor, site, and action explicitness, which raises authoring cost.
  *Mitigation:* stop at a sufficient sentence; recover only details that change the receiving result.
* **Did bias:** repeated rewrites make the pattern teachable, but may over-formalize early cues.
  *Mitigation:* preserve an early cue or open question without requiring a sense token, record or closed answer.

## A.6.A:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern                   | Symptom                                                                                     | Why it fails                                           | How to avoid or repair                                           |
| ------------------------------ | ------------------------------------------------------------------------------------------- | ------------------------------------------------------ | --------------------------------------------------------------- |
| **Site-participant-property affordance** | "The site participant is actionable" with no enactor or coupling frame | collapses relationality into monadic property language | publish site, enactor, action, and coupling frame |
| **Invitation-as-obligation**   | "This calls for rollback" is treated as if rollback is already required                     | hides A-classified or D-classified claim status and accountability | recover the actual claim and apply its duty or gate rule through A.6.B |
| **Invitation-as-work**         | “The system reacted” is used where only a cue or option exists                              | confuses offer with execution                          | keep invitation separate from A.15 and `U.Work`                   |
| **MethodDescription as invited Method** | `Enact(methodDescriptionRef=Runbook)` supplies no exact Method | makes a C.2.1 episteme the world-side way of doing | select exact `methodRef -> U.Method`; keep the description auxiliary |
| **Viewpoint or view by record inclusion** | a field name or bundle row is treated as proof of `U.Viewpoint` or `U.View` | bypasses reference resolution and E.17.0 dependent-kind rules | resolve `viewpointRef` under the effective scheme and establish any view's conformance independently |
| **Capability-as-invitation**   | “The robot can do X” stands in for a situated affordance                                    | destroys local enactor and site conditions             | separate capability description from action invitation          |
| **Latent cue as explanation**  | a model tendency is narrated as if it were already an explicit rationale                    | overstates articulation and evidence                   | state the supported model tendency; use a cue pack or option set only when that form helps the receiving use     |
| **Premature automation**       | a cue without required witness records is wired directly into gates or controllers with no explicit hook `authoritySourceRef` named source or guard | creates unsafe action-to-automation coupling                         | apply the existing controller or gate rule, recover authority and evidence, and use an explicit hook when its interface requires one                |
| **ArticulationHint as F proxy**| `hook-explicit` is treated as "more formal"                                                | recreates a forbidden second formality characteristic          | keep F in C.2.3; reserve articulation and closure semantics for `A.16` |

## A.6.A:10 - Rationale {#rationale}

Physical opportunities, their detection, operator prompts and inquiry questions can share an action-oriented sentence shape while having different obtaining and identity conditions. Recovering their meaning is a reusable method; their common grammar does not supply a common relation kind.

A universal invitation record would add an intermediate object whose truth conditions the menu cannot establish. A complete sum of independently specified relation kinds could serve a particular receiver, but it would require those actual predicates, identity rules and a receiving use. Wording recovery can usually stop earlier, at the supported subject claim or question. This reduces representation work while preserving consequential distinctions.

Use `C.16.Q` for an evaluative repair, `A.6.B` for the actual boundary-bearing claim, `A.15` for Method/Work distinctions and `A.16` for a needed account transition. `C.2.3` remains the direct governor of Formality F. A physical-opportunity statement, an open inquiry and a policy decision need not pass through the same intermediate relation.

## A.6.A:11 - SoTA-Echoing — choose wording recovery or a domain form by the receiving task {#sota-echoing-choose-wording-recovery-or-a-domain-form-by-the}

**Practice question.** For §5.2's “This handle affords pulling,” should the receiver first recover the supported claim or directly produce a domain-specific action representation? The selected answer for ambiguous documentation is §4.0a's six-step recovery, stopping at the useful statement, inquiry or missing basis. The serious alternative is to apply the source's established interpretation and manipulation method directly. **Adopt** that shorter route when the intended meaning and receiving interface are already settled. **Reject** choosing an operational form merely because the sentence contains “affords.”

[ReKep, PMLR 270 (2025)](https://proceedings.mlr.press/v270/huang25g.html) supplies a concrete form-and-method alternative: language instructions and RGB-D observations can be converted into constraints over 3D keypoints, then used in optimization for robot actions. It is a serious alternative for an actual manipulation task, not a proposed general theory of wording. **Adapt** its explicit interface demand to the last branch in §5.2: use the representation when the receiver needs that plan and has the required inputs. Its manipulation results do not establish the truth of this pattern's handle claim or validate the six-step recovery.

Compare one author pass over the same supplied handle case and receiving question; do not compare that pass with a robot experiment or count absent observations as free inputs:

| Receiving task and available basis | Direct source-specific method or form | Recovery-first choice and accepted cost |
| --- | --- | --- |
| Explain whether the supplied R2/G1/CP3 names support pulling; the physical rule and readings are absent. | A domain expert can immediately name the missing physical grounds. Attempting a manipulation representation requires additional observations and still leaves that evidential question to its domain rule. | §5.2 returns the bounded question and missing grounds. The six steps add interpretation work for a reader who has not yet distinguished opportunity, detection and command; no speed advantage over the informed expert is claimed. |
| Produce actions from an already understood instruction, with the domain method and required observations available. | Apply the method's representation and planning procedure directly. | Reuse the established interpretation and continue to that method. Another recovery note has no required role. The ordinary sentence alone does not deliver the executable plan. |
| Explain differing detections with physical handle facts held fixed, as in §5.3. | A manipulation-command form serves a different output; a source-specific inquiry method is suitable if it preserves that question. | Return the detector question first, then use an inquiry method only if further construction is needed. This avoids silently replacing inquiry with a movement target. |

This is a **local inference** about the stated tasks, supplied information and required outputs. It motivates §4.0a steps 1/5/6, the optional forms in §4.5, and the explicit domain-method continuation in §5.2. It establishes neither a robot effect nor a measured reduction in author effort. The deliberate trade-off is some interpretive work before committing to a form, with that work omitted when an adequate interpretation already exists.

The supporting sources constrain different claims:

* **Hansen (2024), §2**, distinguishes action possibilities from obligations and allows possibilities to escape immediate perception. **Adopt** those distinctions for the physical case; his account of perception supplies no universal ontology for metaphorical invitations. ([Frontiers][1])
* **Vauclin and colleagues (2023)** review attunement and action calibration in human person-plus-object systems. **Adapt** the distinction to the question about changed detection versus changed capabilities or physical conditions. The human findings do not establish the robot case; its physical rule and evidence remain necessary. ([Springer][2])
* **Pezzulo and colleagues**, in *Neural representation in active inference*, distinguish roles of generative models in action-perception, planning and imagination. **Adapt** that distinction when recovering a model-side claim from “the model wants”; the model tendency establishes no duty, explicit rationale or performed Work. ([UCL Discovery][3])
* **MOKA (2024)** supplies a compact point-based interface between image predictions and robot manipulation. **Adopt** the principle of an intermediate form with an actual receiver. Its robot-interface use neither makes such a form compulsory for an inquiry nor provides one obtaining predicate for every invitation. ([Robotics: Science and Systems][4])

Reopen the affected recovery when a source-specific meaning or physical criterion changes the supported interpretation, when new observations answer the named gap, or when the receiver now needs an executable interface. Recompare the method if a serious alternative preserves these distinctions with less required work. A new source's date, another field in a record, or shared terminology alone changes none of those conditions.


## A.6.A:End {#end}
