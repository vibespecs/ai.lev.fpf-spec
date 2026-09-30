# A.19.CN - CN-frame: Specify and Maintain Comparability and Normalization {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Scope.** Use a CN-frame to state which values may be compared for one bearer and intended use. Declare the characteristic space, chart, normalization and comparison basis in CN-Spec; maintain its editions and apply the conditions for each proposed reuse.
>
> **Governing-pattern boundary (cite, don’t duplicate).** A.19.CN governs the **CN-frame governance card, registry, bridges, and checklist/harness** (`CN-Spec`, registry, bridges, checklist/harness). It does **not** govern any CHR-mechanism **intensions**, term cards, or method taxonomies. Those are governed by the corresponding mechanism-governing patterns: **A.19.UNM**, **A.19.UINDM**, **A.19.USCM**, **A.19.ULSAM**, **A.19.CPM**, and **A.19.SelectorMechanism**. Evidence/backing is governed by **C.16**; admissibility gates are governed by **G.0**. Therefore A.19.CN specifies *where the references live*, *what must be citeable for audit*, and *how governance changes trigger regression* — not mechanism semantics.
>
> **Reader guide (fast navigation).**
> - “What does `NormalizationMethodId/…InstanceId/≡_UNM/NormalizationFix` mean?” → **A.19.UNM**.
> - “What is an Indicator / `IndicatorChoicePolicy` and why NCV ≠ Indicator?” → **A.19.UINDM**.
> - “Why can we trust a normalization / where does calibration or evidence live?” → **C.16 (MM‑CHR)**.
> - “What is admissible to compare or aggregate, and what is `MinimalEvidence`?” -> **G.0 (CG-Spec)**.

## A.19.CN:1 - Context {#context}

A.19 established a substrate‑neutral picture:

* a **CN‑frame** = a selected **CharacteristicSpace (CS)** + **chart** (coordinate patch and value basis, with Units where applicable) + a referenced **Normalization mechanism (UNM)** for one named bearer, comparison basis, scope/window, and intended use. A.19.UNM defines directed normalization, its preservation/loss basis and any separately justified `≡_UNM` class use;
* **operators** (subspace, product, pullback/pushforward) and **comparability** (coordinatewise vs **normalization‑based (normalize‑then‑compare)**);
* **RSG touch‑points**: role readiness (**RSG** states) are **certified** against CS via **checklists** over observable characteristics;
* **entity/relational mixtures** across CN‑frames via minimal schemas and bridges.

**Terminology guard.** *CN‑frame* is the **lens** (I); *CN‑Spec* is the specification (S) that fixes the bearer, characteristic and scale editions, chart, comparison basis, scope/window, normalization references, comparability rule, aggregation choice, and intended use; *CN‑Description* is the didactic surface (D) with worked examples and anti-patterns. Mechanism-level term cards such as `NormalizationMethod`, `NormalizationMethodInstance`, `NCV`, `≡_UNM`, and `IndicatorChoicePolicy` remain defined by the corresponding **A.19.<MechId>** patterns and are only cited here.

**Normalization names.** Use A.19.UNM’s method and instance identifiers to identify the selected normalization. Ordinary mathematical “mapping” describes its function; it does not assert a specialized FPF `Map` kind or an F.9 Bridge. Resolve a legacy identifier through F.18 alias docking when needed.

A.19.CN makes this *operational and auditable*.

## A.19.CN:2 - Problem {#problem}

Absent a governance layer, four failure modes recur:

1. **Chartless numbers.** Measures move between teams without units, reference states, or declared normalization → **illusory comparability**.
2. **Hidden normalization flips.** Re‑parameterisations (e.g., normalising by batch size) silently alter meaning; trend lines lie.
3. **CN‑frame sprawl.** Every initiative mints a new “dashboard dimension”; semantics diverge; assurance collapses.
4. **Un‑bridgeable reports.** Cross‑team roll‑ups average **incongruent** CN‑frames, without a justified common comparison/aggregation model under B.3.

## A.19.CN:3 - Forces {#forces}

| Force                         | Tension we must balance                                                              |
| ----------------------------- | ------------------------------------------------------------------------------------ |
| **Universality vs nuance**    | One Standard for robotics, safety, and finance, while each named source scheme retains its own exact meanings. |
| **Speed vs audit**            | Light ceremony for on‑ramp; hard guarantees for assurance and SoD.                   |
| **Local truth vs federation** | Keep meanings tied to their exact schemes and claims; still allow explicit relations and bounded receiving uses. |
| **Minimalism vs safety**      | Few mandatory slots; enough structure to forbid silent normalization drift.                  |

## A.19.CN:4 - Solution — **The CN‑Spec** (CN‑Spec) + **Registry** + **Bridges** {#solution-the-cn-spec-cn-spec-registry-bridges}

### A.19.CN:4.1 - The **CN‑Spec** (comparability and normalization specification) {#the-cn-spec-comparability-and-normalization-specification}

A **CN‑frame** is described by a compact, notation-free specification. The specification names the bearer and the exact boundary within which its readings may be compared:

```
CN‑Spec {
  name              : CN‑frameName
  edition           : <edition>
  bearer_ref        : <evaluated bearer or bearer kind>
  characteristic_space_ref : <CharacteristicSpaceRef>
  scope_ref?        : <ClaimScopeRef>
  window?           : <qualification interval>
  reference_or_comparison_basis : <corpus, baseline, reference state, or declared comparison set>
  cs_basis          : [{
    slot_id         : <tech-token>,
    characteristic  : <U.Characteristic>,
    scale           : { type: nominal|ordinal|interval|ratio, unit?: <U.Unit>, bounds?: <…> },
    polarity        : up|down|target-range|none,
    // if needed: missingness?, admissible_domain? (MM‑CHR-consistent metadata)
  }]
  chart             : { reference_state, coordinate_patch, measurement_protocol_ref?, value_ascription_basis? }
  normalization     : {
    UNM_id?,
    methods: [NormalizationMethodId],
    instances?: [NormalizationMethodInstanceId],
    method_descriptions: [NormalizationMethodDescriptionRef],
    admissible_reparameterizations,
    invariants,
    fix?: <NormalizationFixSpec>
  }
  comparability     : { mode ∈ {coordinatewise, normalization-based}, minimal_evidence }
  intended_use      : <claim, comparison, admission, or aggregation use>
  indicator_policy? : { IndicatorChoicePolicyRef, scope, edition }
  acceptance        : { checklist_for_admission, window, evidence_anchors }
  aggregation?      : { Γ_fold, selected WLNK/COMM/LOC/MONO claims, time_policy }
  alignment?        : [{ bridge_ref, direction, correspondence_rule, tolerated_loss, reliance_ref? }]
  maintenance       : { source_maintenance_assignment, DRR_links, deprecation_plan }
}
```

**Reading:** the CN-frame is the selected characteristic space and chart for one named bearer and use. `CN‑Spec` pins the editions, comparison basis, scope and window, normalization references, aggregation choice, and admission evidence that make that use auditable. A.19.UNM still defines normalization semantics, A.19.UINDM defines indicatorization, C.16 supplies measurement and evidence backing, and G.0 supplies admissibility gates. CN‑Spec records the values used; it does not make a source, scope, or Bridge into a universal container. An actual `Γ_fold` cites its law and applicability basis. Its property codes express only the claims needed by this use; A.9 supplies an unresolved law choice or property check, while ULSAM retains the actual CHR fold and admissibility rules.

**Mechanism-reference note.** `UNM_id` identifies the admitted normalization mechanism. `NormalizationMethodId` and `NormalizationMethodInstanceId` retain the meanings declared by A.19.UNM, and evidence for a relied-on instance remains with C.16. CN‑Spec neither redefines those terms nor implies transport or a cross-local relation.

**L‑CN‑Spec‑NORM‑IDs (by reference).** Cite the normalization identifiers defined by A.19.UNM. Reference fields follow A.6.5: `*Ref` names a reference field and `*Slot` names a SlotKind.

### A.19.CN:4.2 - CN-frame registry and conditional independent certification {#cn-frame-registry-and-conditional-independent-certification}

First identify whether the receiving claim or applicable control requires independent certification of this exact CN-Spec edition or admission basis. When it does, the holder certifying it must not have authored or materially selected that basis. Include relevant earlier authoring whose content the certified basis retains. Renaming an assignment or waiting until an authoring assignment ends does not satisfy this condition.

Recover the actual holders, their relevant Work, the exact edition or basis and the applicable history under A.2.1 and A.2.7. Distinct assignments do not establish distinct holders. Missing history leaves independence unresolved. Different holders can satisfy this non-self-certification condition while their assignment windows overlap; any stronger organizational-independence or commissioning control still applies. The certifier's authority and adequacy of examination require their own grounds.

When no independent-certification claim or control applies, an adequately grounded one-person comparison can remain explicitly uncertified. Its measurement, comparison and reliance requirements still apply.

One named registry edition may publish the CN-frame's names, exact editions, characteristic-space and bearer references, the maintenance assignment, and the deprecation relation. When certification affects the receiving use, it also makes the applicable control, relied-on edition, certification result and supporting references recoverable. Distinguish:

* an adequate comparison for the named use with independent certification not required and no such claim made;
* a certification condition satisfied for the exact edition, with the participation, authority and examination grounds;
* a required condition that is unmet or unresolved, with its consequence for the dependent use under the applicable control.

These are different conclusions, not interchangeable registry labels. The registry helps discovery and currentness; it supplies no missing comparison, independence or certification evidence. A changed comparison basis reopens only the certification and receiving conclusions that rely on that change. A display-only registry change does not reopen them.

### A.19.CN:4.3 - **Bridges between exact local meanings** {#bridges-between-exact-local-meanings}

When two CN-frame uses rely on different exact F.17 local senses, cite an obtaining F.9 Bridge between those cells. A compact record can expose the information needed by the receiving use:

```
Bridge <source F.17 cell> → <target F.17 cell>
  direction: <source-to-target use>
  correspondence_rule: <how the local claims correspond>
  applicable_use: <the receiving comparison or aggregation>
  kept_characteristics: [… ]
  lost_characteristics: [… ]
  tolerated_loss: <declared limit>
  transform: {pullback | pushforward | re-scaling | re-binning | … }
  plane_relation_ref?: <only when a separately defined plane relation obtains>
  extra_guards: {additional evidence, review assignment, or waiver speech act}
```

The Bridge establishes only the exact sense relation. A claim that uses it for comparison, admission, or aggregation remains a separate C.2.1 use claim with its direction, rule, and tolerated loss, together with the A.10 provenance account and any B.3 assurance result required for that use. No Bridge follows from matching names, and no reverse direction follows automatically. B.3 supplies any current loss effect on assurance; CN‑Spec may add operational guards but does not redefine that calculus.

## A.19.CN:5 - Conformance Checklist (normative) {#conformance-checklist-normative}

> **Pass these and your CN‑frames are fit for assurance and cross‑team composition.**

**CC‑A19.D1‑1 (Local identity and scope).** Every CN-frame **MUST** identify its name and edition, bearer, characteristic space, reference or comparison basis, intended use, and any scope/window that qualifies the readings. The same label under another scheme or edition is not evidence of the same frame.

**CC‑A19.D1‑2 (Scales, units and preferred direction).** Each characteristic slot in `cs_basis` **MUST** declare its Scale and value meanings, its Unit when that Scale has one, and the polarity or target rule used by the comparison. State when no simple preferred direction applies.

**CC‑A19.D1‑3 (Chart).** `chart` **MUST** name its reference state and coordinate patch. For measured values, cite the applicable measurement method and protocol under C.16; for evaluated or otherwise ascribed values, cite the rule and basis that establish those values.

**CC‑A19.D1‑4 (Normalization references, not redefinition).** `normalization` **MUST** (i) cite the UNM mechanism (`UNM_id?`) and (ii) provide the normalization references required by the A.19.UNM governing pattern (methods / invariants / fix, and instances when used) so that any normalization‑based comparison is auditable. This pattern does not define what a “NormalizationMethod” is — it requires that CN‑Spec can point to the governing pattern that does.

**CC‑A19.D1‑5 (Comparability mode).** `comparability.mode` **MUST** be either **coordinatewise** (same chart & units) or **normalization‑based** (“normalize‑then‑compare” via the declared **UNM**). Mixed/implicit modes are prohibited. A.19.UNM governs the directed result and any optional classes. The receiving comparison must retain its required distinctions; equality of normalized outputs alone establishes no operational congruence. CN-Spec pins the chosen result branch and its basis.

**CC‑A19.D1‑6 (Admission checklist).** `acceptance.checklist_for_admission` **MUST** be observable and time‑bounded; each datum admitted to the CN‑frame **SHALL** cite a **StateAssertion** or equivalent `U.Evaluation`.

**CC‑A19.D1‑7 (Aggregation discipline).** When aggregation is used, `aggregation.Γ_fold` **MUST** identify the declared scale-lawful fold, its applicable algebraic properties and any required time policy. G.0 and A.19.ULSAM govern admissibility and the fold; B.3 applies when the fold serves an assurance claim. Keep the values separate when no fold is needed.

**CC‑A19.D1‑8 (Relation and use discipline).** When reuse depends on different exact F.17 local senses, the receiving claim **MUST** cite an obtaining F.9 Bridge with exact endpoints, direction, correspondence rule, applicable use, and tolerated loss. The comparison or aggregation remains a separate C.2.1 use claim, with the A.10 provenance account and any B.3 assurance result required by that use. Coordinate-by-name without that relation and use account fails.

**CC‑A19.D1‑9 (Conditional non-self-certification).** When the receiving claim or control requires independent certification, the certifying holder **MUST NOT** have authored or materially selected the exact CN-Spec edition or admission basis being certified, including relevant retained earlier content. Apply §4.2 to holder/Work/history, required authority and examination. Unknown history is unresolved. An adequate use with no such requirement may remain explicitly uncertified.

**CC‑A19.D1‑10 (Maintenance, deprecation, and DRR).** Every CN-Spec **MUST** carry a **source-maintenance role assignment**, a **deprecation plan**, and links to **DRR** entries for rationale and changes (Part E.9).

**CC‑A19.D1‑11 (Evidence for the receiving use).** An admission later used for comparison or aggregation **SHALL** retain the independently established measurement or evaluation results and support relations that the receiving use needs, including applicable currentness and validity windows. Use A.10 to recover their provenance and bounded use. Add B.3 assurance lanes and an assurance result only when the receiving use makes that assurance claim. Missing required inputs have the disposition declared by the comparison or aggregation rule.

**CC‑A19.D1‑12 (Notation independence).** CN‑Spec content **MUST NOT** depend on a tool or file format; semantics precede notation (E.5.2 Notational Independence).

**CC‑A19.D1‑13 (Lexical guard‑rails).** characteristic names and role labels **MUST** follow the Part E lexical discipline (registers, twin labels; no overloaded “process/service/function”).

## A.19.CN:6 - Consequences (informative) {#consequences-informative}

| Benefit                           | Why it matters                                                                                                        |
| --------------------------------- | --------------------------------------------------------------------------------------------------------------------- |
| **Auditable comparability**       | Chart + declared normalization (UNM + NormalizationMethods) make “same number” meaningful; silent re‑basings become explicit, reviewable choices.                   |
| **Safe roll‑ups**                 | Γ-folds preserve only the properties justified by the named quantity, operation and dependency model.                                    |
| **Pluralism without incoherence** | Bridges with CL and loss notes allow federation without pretending to global sameness.                                |
| **RSG‑ready**                     | Admission checklists let **RSG** states reference **CN‑frame‑backed** facts (e.g., *Ready* requires characteristics within bounds). |


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/A-19#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/A-6-1#root (mechanism intension cards), spec://ai.lev/fpf-spec/contract/C-16#root (evidence/backing), spec://ai.lev/fpf-spec/contract/F-9#root (Bridges & CL), spec://ai.lev/fpf-spec/contract/G-0#root (CG-Spec admissibility gate). @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-18#root, spec://ai.lev/fpf-spec/contract/A-19-CPM#root, spec://ai.lev/fpf-spec/contract/A-19-SelectorMechanism#root, spec://ai.lev/fpf-spec/contract/A-19-UINDM#root, spec://ai.lev/fpf-spec/contract/A-19-ULSAM#root, spec://ai.lev/fpf-spec/contract/A-19-UNM#root, spec://ai.lev/fpf-spec/contract/A-19-USCM#root, spec://ai.lev/fpf-spec/contract/A-9#root, spec://ai.lev/fpf-spec/contract/G-0#root, spec://ai.lev/fpf-spec/contract/G-1#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/A-19-CN
