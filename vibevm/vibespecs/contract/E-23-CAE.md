# E.23.CAE - Capability Access and Expression Differential Probe {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Tech-name:** `CapabilityAccessAndExpressionDifferentialProbeMethod`
> **Plain-name:** test whether a capability is unavailable, unrecognized, unexpressed, unadapted, unenacted, or changed
> **Type:** Method-description pattern for an observation-first differential probe; coordinated with `E.23` and `E.23.CDI`
> **Status:** Stable
> **Normativity:** Normative unless marked informative

## E.23.CAE:1 - Problem frame {#problem-frame}

**Use this when.** Use this pattern when one exact holder previously produced a result, passed a qualified reference test, or has a current capability claim for a named Work family, but performance now fails, transfers poorly, or changes with conditions. Use it only when the next question depends on distinguishing at least two of these possibilities:

- the demand lies outside the claimed capability envelope;
- a performer, tool, record, interface, authority, state, or other support is unavailable;
- an available response is not selected as applicable;
- a response cannot be accessed or activated;
- context or interference changes expression;
- an available response cannot be adapted to the changed demand;
- the response cannot be enacted in the current performer arrangement; or
- the holder's capability has actually changed.

**First useful move.** State the case in ordinary language:

> This holder previously obtained this result for this Work family under these conditions. The holder now fails to obtain that result under the changed demand. Before more training, redesign, rehearsal, or parameter updating, return once to a qualified reference condition without further development, vary the smallest decision-bearing condition, and record which observable distinction changes first.

**First useful result.** Return the controlled observations, one or more qualified differential dispositions, the strongest surviving rival, the limits of the result, and candidate routes to the patterns or domain Methods that could receive it. The result is not a choice, authorization, selected next Work, or performed Work; it does not establish hidden memory or a causal mechanism.

**What changes in practice.** A practitioner no longer treats one failed performance as proof that the capability or memory disappeared. They first ask whether the claimed demand, configuration, cue or routing, applicability selection, response access, adaptation, and enactment can be separated by a safe contrast. Development or redesign begins only after a separate steering or choice result uses that evidence.

**What this buys.** The probe can recover a still-available response, avoid unnecessary redevelopment, identify the earliest observable failure position, and return a smaller next question to the right owner. It works across unlike holders because the common part is the contrast and disposition, not one theory of memory, organization, learning, or model internals.

**Not this pattern when.**

- Use `A.2.2` when only the holder, Work family, envelope, measures, evidence, or currentness of a qualified holder-ability claim must be stated.
- Use `A.15.8` when one exact Work or WorkPlan configuration and its recovery relation already bound the whole question.
- Use `E.23.CDI` when capability development has already been selected and the live question is the intervention and representative transfer check.
- Use `A.15.7` when ongoing Work merely needs one next action; use `C.11` only when a current chooser and `OptionSet` already exist and comparison can change the choice.
- Use the direct domain Method when a human memory mechanism, organization routine, continual-learning algorithm, robotic controller, medical condition, safety rule, threshold, or intervention is the live subject.
- Do not use one successful occurrence to infer a capability, and do not run a risky live probe when replay, simulation, staged testing, or another protected evidence route is required.

## E.23.CAE:2 - Problem {#problem}

Apparent capability loss compresses different failures into one sentence: “they knew it yesterday,” “the organization forgot the routine,” “the model catastrophically forgot,” or “the robot cannot do it anymore.” Each sentence can trigger expensive or harmful Work before anyone checks whether the old response still appears under a qualified condition.

The opposite error is to explain every recovery with one theory. Human sensorimotor memories can be expressed according to contextual inference; conceptual knowledge can remain inert until relational retrieval; organizational performance can depend on roles, rules, records, artefacts, and authority; an AI function can remain represented while its activation is biased; a robot can retain a policy while sensing, state estimation, actuation, or configuration prevents enactment. These structures are not one memory system.

The reusable problem-solving move is narrower: bind one capability claim, control further change long enough to compare conditions, recover a reference response where possible, separate observable positions, retain rivals, and return an evidence-bounded disposition. The method must admit both genuine capability change and an unresolved result.

## E.23.CAE:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Exact claim versus familiar story | “Forgot” is recognizable, while the probe needs one holder, Work family, envelope, prior basis, current demand, and window. |
| Recovery versus transfer | Reappearance under an old condition can reject simple global loss, while it does not establish capability in the changed condition. |
| Controlled contrast versus ecological realism | One changed factor helps discriminate rivals, while actual contexts can be coupled, sequential, and partly hidden. |
| Observation versus mechanism | A shared contrast can guide unlike holders, while human memory, organizational routine, AI routing, and robotic control need different explanations. |
| Probe versus intervention | A clean contrast should avoid new learning or updating, while repeated trials can themselves train, prime, fatigue, adapt, or reorganize the holder. |
| Useful disposition versus premature choice | The result should change the next question, while it must not become a `ChoiceResult`, authorization, or selected Work. |
| Information versus safety and cost | Another contrast can reduce uncertainty, while live probing can be unsafe, disruptive, slow, or too expensive. |

## E.23.CAE:4 - Solution {#solution}

### E.23.CAE:4.1 - Bind the claim before probing {#bind-the-claim-before-probing}

Name only the values that can change the probe or its later use:

1. the exact holder System;
2. the named Work family or exact current demand;
3. the capability envelope, measures, evidence, and qualification window currently relied upon;
4. the prior qualified result or reference condition;
5. the present failure or unstable expression;
6. the relevant performer and support configuration;
7. any development, rehearsal, procedure change, parameter update, model update, calibration, or other change that must be held fixed where safe;
8. protected conditions and probe limits; and
9. the receiving question that a differential observation could change.

If the holder or Work family is unclear, return to `A.2.2`. If the current demand is already outside the claimed envelope, return `outsideClaimedEnvelope` and stop the loss diagnosis. If a known configuration failure fully explains the case, use `A.15.8` and stop here.

For a compact retained account, use this local shape only when another use needs it:

```text
CapabilityAccessExpressionProbe@Use:
  holderRef:
  workFamilyOrDemand:
  claimedEnvelopeAndWindow:
  priorReferenceCondition:
  presentObservation:
  controlledChangeCondition:
  protectedConditions:
  disposition:
  strongestSurvivingRival:
  unsupportedUse:
  candidateRoutes:
```

This card is a local Method result, not a new FPF kind.

### E.23.CAE:4.2 - Run the differential probe {#run-the-differential-probe}

1. **Check the demand against the claim.** Confirm that the current task belongs to the Work family and capability envelope being relied upon. Compare measures and qualification windows before calling a difference loss or transfer failure.
2. **Recover the relevant configuration.** Name actual or intended performers, roles, tools, records, interfaces, authority, environmental conditions, state, and other supports only where their direct rules apply. Use `A.15.8` when one exact Work or WorkPlan configuration is current.
3. **Hold development and updating fixed.** During the contrast, avoid new teaching, rehearsal, procedure rewrite, fine-tuning, parameter update, recalibration, or other development where safe and feasible. If the probe necessarily changes the holder, mark the affected distinction unresolved or narrow the claim.
4. **Return to a qualified reference condition.** Recreate a previously successful or separately qualified condition without further development. Prefer an `A → B → A` or equivalent return when order, recency, or transition history can matter. Reappearance rejects simple global loss under those tested conditions; it does not establish general transfer.
5. **Vary a decision-bearing condition.** Change the smallest condition that can distinguish live rivals: an overt cue, cue reliability, preceding decision state or uncertainty, role, record, authority, tool, task or context identifier, state feedback, blocked versus interleaved order, transition frequency, or another domain-relevant condition. A label or visible setting is not assumed to be the effective context.
6. **Observe applicability separately.** Ask whether the relevant Method, response, routine, policy, or prior case is selected as applicable before judging execution. For a person this may involve recognition or choice; for an organization it may involve routing, role, record, or authorization; for AI or robotics it may involve task/context identification, policy routing, or function activation. These are different mechanisms occupying one observational position.
7. **Separate availability, adaptation, enactment, and result.** Where the case permits, observe whether the response can be accessed or activated, whether it can be transformed for the changed demand, whether the actual performer arrangement can enact it, and whether the required result obtains. A later failure does not by itself establish an earlier one.
8. **Compare live rivals.** Retain every explanation still compatible with the observations. Ordinary cue effects, interference, envelope mismatch, configuration loss, applicability failure, access or activation failure, adaptation failure, enactment failure, and actual holder change are not synonyms.
9. **Return a disposition and candidate routes.** State the earliest supported distinction, evidence and conditions, strongest surviving rival, unsupported overread, and patterns or domain Methods that could receive the result. Do not select a route merely because the probe produced a disposition.

These steps organize observations, not a universal cognitive pipeline. A holder may implement them through simultaneous, recurrent, distributed, or structurally different processes.

### E.23.CAE:4.3 - Qualify the disposition {#qualify-the-disposition}

| Differential disposition | Minimum useful observation | Candidate route | What the observation does not establish |
| --- | --- | --- | --- |
| `outsideClaimedEnvelope` | The current demand differs on an envelope coordinate excluded from or unsupported by the current capability claim. | Reframe the claim through `A.2.2`, or open development only through a separate next-action or choice result. | Loss or forgetting inside the old envelope. |
| `configurationOrSupportUnavailable` | Performance changes with a controlled performer, role, record, tool, interface, authority, state, or environment contrast. | `A.15.8` and the direct owner of the failed relation. | Changed holder capability or a human-like memory in a collective. |
| `responseAvailableUnderReferenceCondition` | The prior response or result reappears in a qualified reference condition without new development or update. | Probe applicability, transfer, adaptation, or enactment; then use the applicable steering or choice pattern. | Whole-envelope capability, a particular retrieval mechanism, or sufficient transfer. |
| `applicabilitySelectionFailureSupported` | The response can be produced when selected or prompted, but is not identified, routed, or authorized as applicable under the target demand. | Holder-specific HCD, organization, AI/robotics, or domain inquiry; `A.15.7` or `C.11` only under their own entry conditions. | One common recognition mechanism or the intervention to choose. |
| `accessOrActivationFailureSupported` | Applicability is established, yet access or activation changes under a controlled cue, task/context, or routing contrast before adaptation and enactment. | Holder-specific access, retrieval, activation, or routing inquiry. | Erased content, a universal latent context, or a sufficient repair. |
| `contextDependentExpressionOrInterferenceSupported` | Expression changes systematically with a qualified context, cue-reliability, or transition-statistics contrast and can reappear without development. | Holder-specific explanation and development Method when separately selected. | The hidden context representation or memory architecture that caused the observation. |
| `adaptationFailureSupported` | The response is selected and available, but cannot be transformed to the changed demand while enactment supports are adequate. | Direct adaptation or domain Method inquiry. | Loss of the original response or the correct adaptation Method. |
| `enactmentFailureSupported` | The response or adapted Method is selected and available, but performer assignment, coordination, authority, body, actuator, interface, tool, or another condition prevents actual Work or its result. | `A.15.8`, performer/authority owners, and the direct domain Method. | Capability change when the necessary performer arrangement did not obtain. |
| `capabilityClaimRevisionWarranted` | Qualified reference and target probes fail across relevant conditions, envelope and configuration rivals have been addressed, and holder-specific evidence supports changed ability in the stated window. | Reassess the `A.2.2` capability claim; use a separate steering or choice result before development. | A specific human, organizational, model, or controller memory mechanism. |
| `unresolvedDifferential` | Safety, missing reference evidence, concurrent updating, coupled changes, insufficient measures, or surviving rivals block a responsible distinction. | Obtain the missing evidence, use a protected test, narrow the claim, or stop. | Permission to choose the most familiar explanation. |

One case may support several ordered dispositions. Keep each observation and its limits visible. No disposition is a `ChoiceResult`, authorization, selected next Work, or performed Work.

### E.23.CAE:4.4 - Keep recognition and assurance separate {#keep-recognition-and-assurance-separate}

**Recognition.** A quick return probe is warranted when the practitioner hears “it worked before,” “the model forgot,” “the team knows the routine,” “the dancer can do it only in class,” or another apparent-loss phrase and at least two live explanations would lead to different next Work.

**Assurance.** Stronger reliance needs proportionate evidence:

- a qualified reference basis rather than a nostalgic recollection or one cherry-picked success;
- commensurable measures, envelopes, configurations, and windows;
- protection against probe-induced learning, fatigue, priming, adaptation, or update;
- enough order, cue-reliability, and transition variation to address the live rival;
- replay, simulation, staged testing, or specialist assurance when live probing would be unsafe; and
- holder-specific evidence before claiming a memory mechanism, causal explanation, or actual capability change.

A cheap reversible probe can support a narrow disposition. A high-stakes capability-loss, safety, medical, employment, deployment, or public-performance decision may require a direct domain evaluation and assurance account before anyone relies on the result.

### E.23.CAE:4.5 - Route without choosing {#route-without-choosing}

The first result should fit in six lines:

> **Claim tested:** [holder, Work family, envelope, window].
> **Controlled contrast:** [reference, changed condition, and what was held fixed].
> **Observation:** [what reappeared, disappeared, or changed first].
> **Disposition:** [qualified differential result].
> **Surviving rival and limit:** [what remains plausible and what is not established].
> **Candidate routes:** [patterns or domain Methods that could receive the result].

During ongoing Work, `A.15.7` can use the disposition as current information while recovering a next action. Use `C.11` only when a current chooser and `OptionSet` already exist and comparison or another probe can change the choice. `E.23.CAE` supplies neither pattern's result. Use `E.23.CDI` only after a separate applicable steering or choice result selects capability development.

## E.23.CAE:7 - Conformance Checklist {#conformance-checklist}

| Check | Passing condition |
| --- | --- |
| `CC-E23CAE-1` | @fact:CC-E23CAE-1 One exact holder, Work family or demand, claimed envelope, evidence basis, and qualification window are explicit. @status:spec/done |
| `CC-E23CAE-2` | @fact:CC-E23CAE-2 A prior qualified result or reference condition exists; one anecdote or familiar label is not substituted. @status:spec/done |
| `CC-E23CAE-3` | @fact:CC-E23CAE-3 The current demand is checked against the claimed envelope before loss, forgetting, or transfer failure is asserted. @status:spec/done |
| `CC-E23CAE-4` | @fact:CC-E23CAE-4 Relevant performer and support configuration is stated, with `A.15.8` used when that exact configuration question is live. @status:spec/done |
| `CC-E23CAE-5` | @fact:CC-E23CAE-5 Development, rehearsal, procedure change, parameter update, calibration, or another holder-changing operation is controlled where safe; contamination narrows or blocks the disposition. @status:spec/done |
| `CC-E23CAE-6` | @fact:CC-E23CAE-6 A qualified reference return and at least one decision-bearing condition distinguish live rivals; cue reliability, order, and transition history are included when they can change the observation. @status:spec/done |
| `CC-E23CAE-7` | @fact:CC-E23CAE-7 Applicability selection, response access or activation, adaptation, enactment, and obtained result are not inferred from one undifferentiated success or failure. @status:spec/done |
| `CC-E23CAE-8` | @fact:CC-E23CAE-8 The disposition names its observation, conditions, strongest surviving rival, unsupported overread, and claim limit. @status:spec/done |
| `CC-E23CAE-9` | @fact:CC-E23CAE-9 Human, organizational, AI, robotic, collective, or hybrid explanations and interventions remain with their direct owners; no common hidden mechanism is asserted. @status:spec/done |
| `CC-E23CAE-10` | @fact:CC-E23CAE-10 The result remains a premise and candidate-route set, not a `ChoiceResult`, authorization, selected next Work, or performed Work. @status:spec/done |
| `CC-E23CAE-11` | @fact:CC-E23CAE-11 Unsafe, overly costly, coupled, or change-inducing probes return a protected alternative, narrower claim, or `unresolvedDifferential`. @status:spec/done |
| `CC-E23CAE-12` | @fact:CC-E23CAE-12 Reopen conditions include changed holder, Work family, envelope, configuration, source, cue structure, update state, measure, evidence, window, or direct-consumer contradiction. @status:spec/done |

## E.23.CAE:9 - Consequences {#consequences}

The pattern reduces premature retraining, redesign, procedure rewrite, and parameter updating by making still-available responses observable before a capability claim is revised. It also returns smaller questions: configuration recovery, applicability selection, access or activation, adaptation, enactment, development, claim revision, or honest uncertainty.

The cost is a qualified reference basis, controlled contrast, explicit claim boundary, and possible protected replay or simulation. Context dimensions can be coupled, reference evidence can be stale, and the probe can change the holder. A narrow unresolved result is therefore a successful outcome when the available evidence cannot support a stronger distinction.

What changes in practice is not the adoption of one memory theory. It is the refusal to move directly from failed expression to capability loss or development Work without first asking which observable contrast could change that conclusion.

### Reopen condition {#reopen-condition}

Revisit this pattern when a current FPF neighbor supplies the whole differential with less burden; actual human, organizational, and AI or robotic uses cannot share the observation-only action; a direct source correction removes a load-bearing contrast; a new direct consumer requires a different disposition; or repeated uses show that one observation position is an independent Method with its own result and boundary.

## E.23.CAE:12 - Relations {#relations}

| Pattern or practice | Relation |
| --- | --- |
| `A.2.2` | Supplies the holder and its qualified ability claim, work conditions, attained bounds, evidence, qualification and fit. The differential probe does not create or update that capability claim automatically. |
| `A.13`, `A.15.1`, `A.2.1`, `F.6` | Govern actual performer recovery, dated Work admission, assignment, and precise assignment-bound attribution independently when those claims are current. A probe result establishes none of them by itself. |
| `A.15.8` | Governs an exact Work or WorkPlan performance configuration and recovery. Its observation may support a configuration disposition here; this pattern does not absorb its relation tests. |
| `E.23.CDI` | Receives the result only after a separate applicable steering or choice result selects capability development. It retains limiting-contribution diagnosis, intervention, protected conditions, and representative transfer. |
| `E.23` | Uses this pattern first only when the proposed object under improvement remains ambiguous because a capability may be available but inaccessible, unexpressed, unadapted, or unenacted. It retains the repeated object-improvement loop. |
| `A.15.7` | May use the disposition as current information for a light next action during ongoing Work. It retains chooser, performer, authority, action, and feedback. |
| `C.11` | May use the disposition as a premise when a current chooser and `OptionSet` exist and comparison or another probe can change the choice. It alone emits the `ChoiceResult`. |
| `E.22`, `A.10`, `B.3` | Govern an explicit evaluation frame, evidence reliance, and assurance when a receiving use needs them. The probe record is not evidence or assurance by form. |
| `E.10.LRN` | Repairs ambiguous learning wording; it supplies no substantive differential probe or holder-specific learning Method. |
| `C.36` | Governs cultural generation, transmission, reconstruction, recognition, selection, retention, and loss across a population. Cultural continuation is not one holder's capability or response availability. |
| HCD, OCE, AI and robotics, MDPE, health, and exact domain practices | Retain holder-specific mechanisms, development Methods, interventions, thresholds, safety rules, and evidence. They consume only the observation and disposition their use requires. |


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/A-2-2#root, spec://ai.lev/fpf-spec/contract/A-15-8#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/E-23#root, spec://ai.lev/fpf-spec/contract/E-23-CDI#root, spec://ai.lev/fpf-spec/contract/A-15-7#root, spec://ai.lev/fpf-spec/contract/C-11#root, spec://ai.lev/fpf-spec/contract/E-10-LRN#root, spec://ai.lev/fpf-spec/contract/C-36#root, and holder-specific practices. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-15-10#root, spec://ai.lev/fpf-spec/contract/A-15-11#root, spec://ai.lev/fpf-spec/contract/C-36-RP#root, spec://ai.lev/fpf-spec/contract/E-10-DEV#root, spec://ai.lev/fpf-spec/contract/E-23-CDI#root, spec://ai.lev/fpf-eng-hcd/contract/HCD-10#root, spec://ai.lev/fpf-eng-hcd/contract/HCD-12#root, spec://ai.lev/fpf-eng-hcd/contract/HCD-13#root, spec://ai.lev/fpf-eng-hcd/contract/HCD-3#root, spec://ai.lev/fpf-eng-syse/contract/SYSE-46#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/E-23-CAE
