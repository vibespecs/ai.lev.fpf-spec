# A.19.CN - CN-frame: Specify and Maintain Comparability and Normalization: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## A.19.CN:7 - Rationale (informative) {#rationale-informative}

A comparison depends on the meaning and basis of its values. Keeping that basis with the CN-Spec makes a changed chart, normalization or intended use visible to the receiver. A claimed aggregation also needs its justified model; a required assurance claim retains its applicable loss policy under B.3.

## A.19.CN:8 - Archetypal Grounding *(Tell‑Show‑Show)* {#archetypal-grounding-tell-show-show}

> **Same slots, three arenas; no tooling implied.** The examples below use plain-language normalization descriptions as placeholders; any normative use must cite A.19.UNM-governed ids/refs (A.19.UNM) and evidence pins (C.16), not invent new terminology here.

### A.19.CN:8.1 - **Industrial line** — *Weld‑quality CN‑frame* (`AssemblyLine_2026`) {#industrial-line-weld-quality-cn-frame-assemblyline-2026}

* `cs_basis`: *BeadWidth\[mm] (target 6.0±0.2)*, *Porosity\[ppm] (↓)*, *SeamRate\[1/min] (↑ until limit)*
* `chart`: reference jig, fixture ID, torch type; `MethodDescription#Weld_MIG_v3`
* `normalization`: affine rescale on gray‑level calibration → invariant = physical porosity
* `comparability`: **normalization‑based (UNM)** (calibration tables applied)
* `aggregation`: a minimum bound only for a declared bottleneck quality model; commutative count addition only for disjoint contributions; time = per-shift histograms
* **RSG hook**: `WelderRole.Ready` requires *Porosity ≤ 500 ppm* & *BeadWidth within ±0.2 mm* admitted by this CN‑frame.

### A.19.CN:8.2 - **Software/SRE line** — *Latency CN‑frame* (`SRE_Prod_Cluster_EU_2026`) {#software-sre-line-latency-cn-frame-sre-prod-cluster-eu-2026}

* `cs_basis`: *P50Latency\[ms] (↓)*, *P99Latency\[ms] (↓)*, *Load\[req/s]*
* `chart`: client vantage, trace sampler v4; `MethodDescription#HTTP_probe_v4`
* Before comparing a client end-to-end reading with a server processing reading, resolve their actual Characteristic and observation basis. Both may use ms yet answer different questions. Keep separate coordinates or obtain readings for the same declared characteristic and basis; a unit conversion alone cannot supply that match.
* `normalization`: monotone time‑warp compensation for collector skew; invariant = percentile order
* `comparability`: **normalization‑based (UNM)** with declared normalization
* `aggregation`: use a max-of-mins latency fold only when the declared service model justifies it; a WLNK bound needs its own bottleneck model. Neither follows from latency percentiles alone.
* **RSG hook**: `DeployerRole.Active` gated if **P99** < declared SLO over the admission window.

### A.19.CN:8.3 - **Clinical/episteme line** — *Trial‑outcome CN‑frame* (`Cardio_2026`) {#clinical-episteme-line-trial-outcome-cn-frame-cardio-2026}

* cs_basis:
  - slot_id: ΔBP
    characteristic: BloodPressureChange
    scale: { type: ratio, unit: mmHg }
    polarity: down
  - slot_id: AdverseRate
    characteristic: AdverseEventRate
    scale: { type: ratio, unit: "%" }
    polarity: down
  - slot_id: Age
    characteristic: Age
    scale: { type: ratio, unit: years }
    polarity: neutral
* `chart`: cohort definition; `MethodDescription#TrialProtocol_v5`
* `normalization`: case‑mix adjustment (propensity score); invariant = adjusted ΔBP
* `comparability`: **normalization‑based (UNM)** (post‑adjustment)
* `aggregation`: recombine subcohorts only under the declared population and weighting model; select the law or supported bound for each named safety outcome under its own justified dependency model.
* **RSG hook**: evidence-use validation of an admission requires CN‑frame acceptance; **Assurance** pulls CL from any Bridge used.

### A.19.CN:8.4 - Worked mini-schemas (entity and relation mixtures across CN-frames, informative) {#worked-mini-schemas-entity-and-relation-mixtures-across-cn}

The three small schemas below show an operations use, an assurance use, and an alignment use. They are explanatory representations, not storage requirements. Each keeps the bearer, system-role kind and assignment, measurement or evaluation result, source-local relation, and evidence use distinct.

#### A.19.CN:8.4.1 - Operations CN‑frame — runtime gating and enactment {#operations-cn-frame-runtime-gating-and-enactment}

_Entity graph view:_

```
System ── classifiedAs ──> SystemRoleKind
System + SystemRoleKind + scope/window ── assignment ──> SystemRoleAssignment
Role-state graph ── lists ──> State
Checklist ── tested by evaluation Work ──> StateAssertion
Work ── performedBy ──> assigned System
Work ── enacts ──> Method
```

The System is classified under one exact local system-role kind and participates in an obtaining assignment for the stated scope and window. A role-state graph lists states such as Ready, Waiting, or Degraded. Evaluation Work applies the state checklist and supports a StateAssertion. Operational Work may proceed only when the relied-on assertion says that an enactable state obtains; the Work, Method, assignment, and result remain different objects.

_Relational stub:_

| Table | Key columns (essential) |
|---|---|
| **ROLE_ASSIGNMENT** | `RA_ID`; `HOLDER_SYSTEM_ID`; `SYSTEM_ROLE_KIND_ID`; `REFERENCE_SCHEME_ID`; `SCOPE_REF?`; `WINDOW_FROM`; `WINDOW_TO` |
| **RCS_SNAPSHOT** | `SNAP_ID`; `RA_ID`; `WINDOW_FROM`; `WINDOW_TO`; `CHAR_ID`; `VALUE`; `UNIT`; `SCALE_TYPE`; `RESULT_REF` |
| **RSG_STATE** | `STATE_ID`; `SYSTEM_ROLE_KIND_ID`; `NAME`; `ENACTABLE` |
| **CHECKLIST** | `CHK_ID`; `STATE_ID`; `PREDICATE_TYPE`; `PREDICATE_SPEC` |
| **STATE_ASSERTION** | `SA_ID`; `RA_ID`; `STATE_ID`; `CHK_ID`; `WINDOW_FROM`; `WINDOW_TO`; `VERDICT`; `NORMALIZATION_INSTANCE_ID?`; `BRIDGE_USE_CLAIM_REF?` |
| **WORK** | `WORK_ID`; `PERFORMER_SYSTEM_ID`; `METHOD_ID`; `WINDOW_FROM`; `WINDOW_TO`; result and evidence refs as needed |

The RCS snapshot keeps the characteristic, value, unit, scale, window, and result identity visible. A StateAssertion separately identifies any normalization instance and any claim that uses a Bridge. An enactment query can therefore ask whether the latest admissible assertion for this assignment has an enactable state and a passing verdict without treating a role label, CN-frame, or Bridge as the acting System.

#### A.19.CN:8.4.2 - Assurance CN‑frame — evidence freshness and related local meanings {#assurance-cn-frame-evidence-freshness-and-related-local-meanings}

_Entity graph view:_

```
NormalizationMethodInstance ── used for ──> characteristic re-expression
F.9 Bridge ── relates ──> exact source and target F.17 cells
ComparisonClaim ── cites ──> normalization instance and/or Bridge-use claim
RelianceClaim ── cites ──> evidence status and assurance limits
```

The normalization instance identifies the declared re-expression and its validity window. The Bridge identifies only an obtaining relation between two exact local senses. A comparison that relies on either one says so in its own use claim; its evidence and assurance limits remain explicit.

_Relational stub:_

| Table | Key columns (essential) |
|---|---|
| **NORMALIZATION_METHOD** | `NORMALIZATION_METHOD_ID`; `KIND`; `DESCRIPTION_REF` |
| **NORMALIZATION_INSTANCE** | `NORMALIZATION_INSTANCE_ID`; `NORMALIZATION_METHOD_ID`; `SRC_CHAR_ID`; `TGT_CHAR_ID`; `FORMULA_SPEC_OR_LUT_REF`; `VALIDITY_WINDOW`; `EVIDENCE_REF` |
| **BRIDGE** | `BRIDGE_ID`; `SOURCE_CELL_REF`; `TARGET_CELL_REF`; `DIRECTION`; `CORRESPONDENCE_RULE`; `APPLICABLE_USE`; `TOLERATED_LOSS` |
| **COMPARISON_USE** | `USE_CLAIM_ID`; `RESULT_REF`; `NORMALIZATION_INSTANCE_ID?`; `BRIDGE_ID?`; `EVIDENCE_USE_REF`; `ASSURANCE_REF?` |
| **ASSURANCE_EVENT** | `AE_ID`; `USE_CLAIM_ID`; `EFFECT`; `DETAILS`; `WINDOW` |

The tables make an audit path possible without assigning meaning to the table itself. A low-assurance relation, stale normalization instance, or refreshed evidence can be recorded as a distinct event and can reopen only the comparisons that rely on it.

#### A.19.CN:8.4.3 - Alignment CN‑frame — design-time reuse across local schemes {#alignment-cn-frame-design-time-reuse-across-local-schemes}

_Entity graph view:_

```
Checklist for target state ← re-expressed by N ─ Checklist for source state
source F.17 cell ── Bridge with direction and loss ──> target F.17 cell
SystemRoleKind' ── stated refinement relation ──> SystemRoleKind
```

A checklist from one source scheme may be re-expressed for another only through the named normalization instance and, when its local meaning changes, an obtaining F.9 Bridge plus a separate use claim. A stated refinement between system-role kinds records how their state distinctions correspond; it must preserve the entailment needed for enactability rather than relying on similar role names.

_Relational stub:_

| Table | Key columns (essential) |
|---|---|
| **RSG_REFINEMENT** | `REFINEMENT_ID`; `SOURCE_SYSTEM_ROLE_KIND_ID`; `TARGET_SYSTEM_ROLE_KIND_ID`; `SOURCE_STATE_ID`; `TARGET_STATE_ID`; `ENTAILMENT_RULE`; `EVIDENCE_REF` |
| **CHECKLIST_REEXPRESSION** | `REEXPRESSION_ID`; `SRC_STATE_ID`; `TGT_STATE_ID`; `NORMALIZATION_INSTANCE_ID`; `BRIDGE_USE_CLAIM_REF?`; `SOURCE_EDITION`; `TARGET_EDITION`; `VALIDITY_WINDOW` |

At least one enactable source state must correspond under the stated rule to an enactable target state when that is the promised refinement. The re-expression record fixes the two editions and validity window so later changes can reopen the affected alignment rather than silently changing an old checklist.

### A.19.CN:8.5 - Same basis, different holder and timing cases {#same-basis-different-holder-and-timing-cases}

For this worked case, the receiving comparison cites `CN-Spec E7`, and its commissioning control requires independent certification of E7's comparison basis. Alice authored that basis. After her stewardship assignment ends, she receives a certifier assignment and examines E7. The holder condition fails: the later assignment still certifies her own basis.

Bob's certifier assignment instead overlaps Alice's stewardship assignment. When Bob neither authored nor materially selected E7's basis, this local holder condition is satisfied despite the overlap. The receiver must still establish Bob's authority for E7, the required examination and any stronger organizational-independence condition from the commissioning control. Missing evidence for one of these conditions leaves that dependent certification conclusion open; different names alone do not establish it.

In an ordinary comparison with no independent-certification requirement or claim, Alice may use a sufficiently supported E7 basis and publish the comparison as uncertified. If E8 later changes the compared population or normalization basis, reopen only uses and certification claims depending on that changed basis. Correcting E7's registry display while its content and evidence stay fixed does not have that effect.

## A.19.CN:9 - Anti‑patterns (and the fix) {#anti-patterns-and-the-fix}

| Anti‑pattern            | Symptom                                   | Why it hurts                 | Fix (CN‑Spec slot)                           |
| ----------------------- | ----------------------------------------- | ---------------------------- | --------------------------------------- |
| **Chartless number**    | “Latency = 120”                           | No unit/vantage → untestable | Fill `cs_basis` + `chart`                          |
| **Normalization smuggling**     | Quiet “per‑unit” normalisation mid‑stream | Trend reversal               | Declare UNM normalization references (`NormalizationMethodId` / `NormalizationMethodInstanceId`) + named invariants (see A.19.UNM)        |
| **Bridge-by-name**      | Reusing equal labels under different schemes | False comparability | Establish the exact F.9 relation and state the separate receiving use and tolerated loss |
| **Free-hand averaging** | An arithmetic mean is used without a model for the intended risk result | The number can answer the wrong question | Use A.9 to select a justified law, bound or separate-input result; declare an actual `Γ_fold` only for the selected fold |
| **CN‑frame sprawl**        | Ten nearly‑identical CN‑frames               | Cognitive debt               | Use Registry + DRR; prefer reuse        |
| **Self-certification hidden by assignments** | A holder authors the basis and later certifies it under a new role | A required independent check still examines that holder's own basis | Apply §4.2 to actual participation in the exact edition; separate authority and examination, and keep uncertified use explicit when certification is not required |

## A.19.CN:10 - Didactic quick cards (one‑liners teams reuse) {#didactic-quick-cards-one-liners-teams-reuse}

1. **Numbers travel with their basis.** Cite the characteristic and scale editions, bearer, reference or comparison basis, scope/window, and result.
2. **If the normalization is not declared, the trend is fiction.**
3. **The intended result selects the law.** Use a weakest-part bound only when its declared dependency model justifies it; a safety label alone selects no fold.
4. **Admit → Assert → Act.** (CN‑frame admission → RSG StateAssertion → Method step).
5. **Relate before reuse.** When local meanings differ, establish the exact Bridge, then state the separate receiving use, direction, rule, and tolerated loss.
6. **When independence is required, check who made the basis.** A later role assignment does not remove self-certification; a sufficient uncertified comparison remains possible when no independent certification is required.
7. **Ground each chart value.** Name the reference state and coordinate patch. For measured values, cite the applicable measurement method and protocol; for evaluated or otherwise ascribed values, cite their rule and basis.
8. **Deprecate in the open.** CN‑frame cards carry DRR & retirement plans.
9. **Keep characteristics few, meanings sharp.** Prefer ≤ 7 characteristics per CN‑frame.
10. **Identify the normalization used.** Cite its method and instance under A.19.UNM; ordinary mathematical mapping language alone identifies neither.

## A.19.CN:11 - SCR / RSCR Harness (acceptance & regression) {#scr-rscr-harness-acceptance-regression}

> **These are concept‑level checks; notation‑agnostic.**

### A.19.CN:11.1 - **SCR — Acceptance (first introduction)** {#scr-acceptance-first-introduction}

* **SCR‑A19.4‑S01 (Completeness).** CN-Spec has every applicable mandatory value. Each cs_basis position declares its Scale and value meanings, Unit when that Scale has one, and the comparison's polarity or target rule, including no preferred direction when appropriate. The chart names its reference state and coordinate patch; measured values cite their C.16 measurement method/protocol, while evaluated or otherwise ascribed values cite the rule and basis that establish them, as required by CC-A19.D1-2 and CC-A19.D1-3.
* **SCR‑A19.4‑S02 (Normalization clarity).** `normalization` cites the UNM mechanism (`UNM_id?`) and provides the normalization references required by the A.19.UNM governing pattern (methods / invariants / fix, and instances when used). If instances are referenced in assurance logs, their evidence/backing and validity constraints are handled by the governing evidence pattern (C.16), not by A.19.CN.
* **SCR‑A19.4‑S03 (Comparability test).** Provide one worked example showing **coordinatewise** or **normalization‑based** comparison end‑to‑end (with Evidence Graph Ref).
* **SCR‑A19.4‑S04 (Γ‑fold audit).** The aggregation rule states the intended result, law and applicability basis, with only the required property claims; the reviewer reconstructs the result on a toy set under that model.
* **SCR‑A19.4‑S05 (Required certification).** Identify the exact receiving claim/control and relied-on CN-Spec edition or admission basis. If independent certification is required, check the actual certifier against authoring/material-selection history, then the independently applicable authority and examination conditions. Replay both successive same-holder assignments and overlapping different-holder assignments. If certification is not required, keep the adequate comparison explicitly uncertified.
* **SCR‑A19.4‑S06 (bearer and anchors surfaced).** For each CN-Spec characteristic used in the worked example, cite its bearer, Characteristic and Scale editions, reference/comparison basis, scope/window, and the A.10 evidence anchors that support the reading.

### A.19.CN:11.2 - **RSCR — Regression (on change)** {#rscr-regression-on-change}

* **RSCR‑A19.4‑R01 (UNM edit).** When `normalization` changes, flag every comparison and Bridge-use claim that cites that normalization for affected-only reassessment, then rerun the corresponding worked comparisons.
* **RSCR‑A19.4‑R02 (Slot surgery/Basis surgery).** Adding/removing/renaming slot/basis requires a **new edition**; old data remain valid **for their edition**.
* **RSCR‑A19.4‑R03 (Chart drift).** Updating measurement protocol bumps edition; **historic Work** keeps old edition link.
* **RSCR‑A19.4‑R04 (Fold change).** Any change to `Γ_fold` invalidates cached roll‑ups; re‑compute or mark as superseded.
* **RSCR‑A19.4‑R05 (Bridge health).** After either endpoint's scheme, claim, or edition changes, revalidate the Bridge direction, correspondence, and loss before relying on it again; reopen only the claims that use it.
* **RSCR‑A19.4‑R06 (Deprecation rule).** On deprecating a CN‑frame, Registry lists its successor; bridges re‑targeted or retired.
* **RSCR‑A19.4‑R07 (Certification basis).** A change to the relied-on basis, relevant participation history or applicable control reopens only the certification and receiving conclusions it can change. A registry display change alone does not.

## A.19.CN:12 - Interaction summary (wiring to the rest of the kernel) {#interaction-summary-wiring-to-the-rest-of-the-kernel}

* **A.2 / A.2.5 (Roles / RSG).** RSG **checklists** quote **CN‑Spec.acceptance**; enactment gates rely on **admitted** CN‑frame data.
* **B.1 and A.9.** B.1 supplies any claimed whole/part construction; A.9 supplies an unresolved aggregation-law choice or property check. CN-Spec records the justified `Γ_fold`, including its model and time policy.
* **B.3 (Assurance).** Bridge CL enters the **R** term; a safety roll-up requires the law or bound justified for its named outcome and dependency model.
* **Current proof/inference support and the C.16/A.19 characterization stack.** Units, scales, and measurement templates come from C.16, A.17, A.18, and A.19. Claims about folds currently use C.2.1 for claim/episteme identity, A.10 for evidence and provenance, B.3 for assurance, and C.23 when method-family evidence or maturity is at issue. Planned C.6 LOG‑CAL may later consolidate proof-use semantics, but supplies no current governing force.

## A.19.CN:13 - Minimal CN‑Spec template (copy/paste, informational) {#minimal-cn-spec-template-copy-paste-informational}

**Template note (refs-only).** This template shows *slot placement* for governance. Token semantics for normalization belong to the A.19.UNM governing pattern (A.19.UNM); indicatorization semantics belong to the indicatorization governing pattern (e.g., A.19.UINDM); evidence/backing semantics belong to C.16; admissibility/evidence gates belong to G.0.

```
CN‑frame: <Name>      Edition: <edition>      Bearer: <bearer ref>
ComparisonBasis: <corpus, baseline, reference state, or declared comparison set>
ScopeAndWindow: <scope ref and qualification interval, when used>
IntendedUse: <claim, comparison, admission, or aggregation use>
characteristics:
  - <CharacteristicName> : <Scale; Unit when applicable>  [Polarity: up|down|target-range|none]
Chart:
  reference_state: <text>
  coordinate_patch: <domain/subset>
  measurement_protocol_ref?: <applicable measurement MethodDescriptionId>
  value_ascription_basis?: <applicable evaluation rule and evidence>
Normalization:
  UNM: <UNMId?>
  methods: [<NormalizationMethodId>… ]
  method_descriptions: [<NormalizationMethodDescriptionRef>… ]
  invariants: [<property>… ]           # what the selected transformation preserves; name losses too (A.19.UNM)
  fix?: <NormalizationFixSpec>          # only for an established class whose receiving use needs a representative (A.19.UNM)
Indicators (optional):
  policy_ref: <IndicatorChoicePolicyRef>
  resulting_indicators: [<IndicatorId>… ] // selection is policy‑defined; NCVs alone do not make an Indicator (see A.19.UINDM)
Comparability:
  mode: coordinatewise | normalization-based
  minimal_evidence: <what must be observed to compare>  # admissibility/evidence gate surface (see G.0 and C.16)
Aggregation:
  fold: <Γ_fold expr>   time_policy: <window, statistic>
  WLNK/COMM/LOC/MONO: <only selected property claims, with their model and applicability basis>
Acceptance:
  checklist: [<observable criterion>… ]
  window: <ISO 8601 interval>
  evidence_anchors: [<Observation/Evaluation ids>… ]
Alignment (optional):
  bridges: [<BridgeId, CL, kept/lost characteristics, extra guards>… ]
MaintenanceAndDeprecation:
  source_maintenance_role_assignment: <RoleAssignmentRef>
  DRR_links: [<DRR ids>… ]
  deprecation_plan: <short note>
```

**Implementation note (non‑normative): conceptual audit fields.** (For implementation completeness only; not part of the CN‑Spec normative surface.) The goal is *auditability*: any implementation should be able to cite the relevant refs (CN‑Spec edition, evidence anchors, UNM instance refs, Bridge ids) when producing a `StateAssertion`. The normative semantics of normalization and evidence/backing are governed by the corresponding mechanism and evidence patterns (e.g., A.19.UNM and C.16). A.19.CN does not prescribe storage formats.

## A.19.CN:14 - SoTA-Echoing — enough basis to compare coordinate values {#sota-echoing-enough-basis-to-compare-coordinate-values}

**Practice question.** What must accompany two chart values before a practitioner treats them as comparable? The selected best-known line identifies the bearer/property, value-producing procedure or evaluation rule, relevant time and result basis alongside Scale/Unit meanings. A serious smaller alternative is to carry only the quantity kind, value and unit, converting units before comparison.

The [QUDT quantity model](https://www.qudt.org/pages/QUDToverviewPage.html) is the useful comparator: it separates Quantity, QuantityKind, QuantityValue and Unit and supports precise quantity descriptions. **Adopt** that discipline where a Unit applies. Using only that portion is cheaper and sufficient when the same property, procedure and observation basis are already fixed outside the record. **Reject** treating it alone as evidence that two independently obtained readings answer the same question; this is a limit of that reduced use, not a claim that QUDT forbids richer descriptions.

The [SOSA/SSN 2023-edition working draft of 24 September 2026](https://www.w3.org/TR/2026/WD-vocab-ssn-2023-20260924/) supplies the compared observation/procedure line: it distinguishes the feature, observed property, procedure, result and temporal qualifications. **Adapt** that separation in CN-Spec's bearer, cs_basis and chart, CC-A19.D1-1/-3/-11, and SCR-S01. The source is work in progress and does not establish FPF admission, Scale lawfulness, certification independence or a Bridge; those retain their direct rules. An evaluated coordinate keeps its actual rule and basis rather than acquiring a fictive measurement or Unit.

At comparable effort, both alternatives start from the same pair of readings and existing method records. The selected line adds the references that can change this comparison, reusing common frame-level values rather than repeating a full observation history for every cell. The SRE case in §8.2 shows the gain: equal millisecond units cannot make client end-to-end latency and server processing latency the same Characteristic. Keep them separate or obtain values for the same declared characteristic and observation basis. The added references cost more than a bare numeric pair; that cost is accepted when the basis is not already common and recoverable.

Reopen when a proposed comparison changes the property, value-producing rule, reference state or relevant window, or when a smaller representation demonstrably retains all the distinctions needed by that use. These sources support the compared representational choices; they do not validate every CN-frame or make its registry self-certifying.

## A.19.CN:Close {#a-19-cn-close}

A.19.CN makes comparability operational: a one-page *CN-Spec*, a registry for edition, status, supersession, and deprecation records, explicit relations and receiving-use claims for cross-local reuse, and a checklist plus harness for audit. It remains tool-agnostic and keeps every reading tied to its characteristic and scale editions, bearer, comparison basis, scope/window, evidence, and intended use.


## A.19.CN:End {#end}
