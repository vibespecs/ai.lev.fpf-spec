# A.6.RSIR - Relation, Signature, Interface, Role, and Slot Precision Restoration {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** FPF precision-restoration pattern
> **Status:** Stable
> **Normativity:** Normative unless marked informative

## A.6.RSIR:0 - Use This When {#use-this-when}

**Plain name.** Relation-signature-interface-role-slot recovery.

Use this pattern when relation, signature, interface, assignment, enactment, slot, field, parameter, argument, endpoint, port, API, protocol, connector, capability, affordance, method, function, concern, interest, Markov-blanket, computational-boundary, or active-inference-boundary wording hides which FPF object or claim kind is current. For bare claim-bearing *role*, apply `E.10.ROLE` once. Do not apply RSIR when that step recovers a system-role kind, assignment, capability, Work, deontic relation, evidence use, another direct object, or ordinary non-use. Apply RSIR only when the still-unanswered question concerns direct participation, a reusable declaration, an interface, an operation declaration or binding, or a representation position.

**Primary EntityOfConcern.** The EntityOfConcern is one encountered use of an ambiguous engineering phrase together with the claim that this use is intended to carry. RSIR recovers the direct governed object, direct relation and participant meaning, actual participant, declaration-local `SlotSpec` or operation declaration, exact operation application and binding, assertion- or description-side designation, representation position and correspondence, or claim before selecting its subject pattern. The phrase remains wording in an episteme or in speech; it is not the world-side object, occurrence, value, or relation named by the recovered claim.

**Primary working reader.** The first reader is an FPF pattern author, reviewer, or practitioner repairing a phrase before selecting the subject pattern. The downstream reader is the engineer, manager, analyst, or steward who needs the repaired phrase to preserve useful project language without minting a shadow ontology.

**First useful move.** Recover the project concern first, then recover the current governed EntityOfConcern or claim kind. As soon as the applicable definition, constraint, or test is clear, apply that rule and stop the RSIR repair. Keep a reduced-use source label only when no governed value is being asserted.

**What goes wrong if missed.** The same word is used for differently defined objects without saying which claim is current. For example, `interface` may denote an API description, reusable signature, functional port, compatibility claim, or module-boundary relation. Bare *role* may point to a system-role kind, one assignment, direct-relation participation, a declaration-local `SlotKind`, a representation position, use of an episteme, another object, or ordinary wording. A later reader then cannot recover which relation obtains, which participant is meant, which declaration is current, whether an exact operation application binds an actual value, or which representation correspondence is intended.

**What this buys.** The reader gets one small recovery move before the direct pattern is applied. The repair preserves useful engineering words while preventing a lexical cue from minting a new root kind or collapsing direct participation, reusable declaration, assertion or description, exact operation application and binding, and representation correspondence.

**Not this pattern when.** Do not use `A.6.RSIR` after the subject pattern is already clear. Do not use it for general relation repair after `A.6.P` is selected, for slot discipline after `A.6.5` is selected, for function-like repair after `A.6.F` is selected, for module-interface repair after `A.6.M` is selected, for transformation wording after `A.3.4.P` is selected, or for publication and description repair after `E.17`, `C.2.1`, or `C.2.P.DR` is selected.

## A.6.RSIR:1 - Problem frame {#problem-frame}

The RSIR cluster sits at a common failure point in FPF texts. A project team sees one word and treats it as if it already selected the ontology:

- bare “role” whose E.10.ROLE branch may be a system-role kind, assignment, direct relation-participant meaning, declaration-local `SlotKind`, representation position, evidence use, another exact object, or ordinary wording;
- "interface" in a module relation, functional port, API description, protocol, signature, or publication view;
- "slot", "field", "parameter", or "argument" in wording about an actual relation participant, a `RelationSignature` declaration, an A.6.1 argument or result declaration, one actual operation application and bound value, a data, formula, or method-call representation, or ordinary prose;
- "signature" in a law-governed declaration, API shape, interface specification, or plain sign-off phrase;
- "function" in architecture, capability, method, work, mathematical modeling, or quality wording.

`A.6.RSIR` is the first-level recovery pattern for this bounded cluster. It does not decide every neighboring subject ontology. It helps the practitioner recover which object or claim is current, identify the rule that defines or tests it, and then stop the RSIR repair.

## A.6.RSIR:2 - Problem {#problem}

Without this pattern:

1. **Lexical cues create shadow kinds.** Interface, role, slot, endpoint, and function words become local root kinds because they sound technical.
2. **Participant, declaration, and representation uses become system roles.** A direct relation-participant meaning, declaration-local `SlotKind`, argument, field, endpoint, or representation position is renamed as a system-role kind. Evidence-use, transformation, and interface claims then lose their direct relations and patterns.
3. **System-role kinds become declaration or representation labels.** A real context-local system-role kind is demoted into a declaration-local `SlotKind` or source-schema field, so its `KindSignature`, exact assignment occurrence and window, `SystemRoleAssignmentStateRelation`, and Work consequences can no longer be recovered.
4. **Signatures absorb implementations.** A law-governed `U.Signature` is used as if it were a mechanism, method, work-start gate decision, interface conformance proof, or publication.
5. **Participant, declaration, application, and representation boundaries are skipped.** A field or parameter is edited without deciding whether it denotes a direct relation-participant meaning or actual participant, a declaration-local `SlotSpec`, an A.6.1 argument or result declaration, one exact operation application and actual binding, or a position in a selected representation.
6. **Evidence and status uses keep old role grammar.** An episteme, standard, report, publication, or badge is said to have a role instead of being used in an evidence-use, source-use, status-use, publication-use, assurance-use, or gate relation.
7. **Neighboring patterns are copied locally.** A pattern repeats negative catalogues such as "not proof, not permission, not gate" instead of recovering the current object and applying the pattern that defines or constrains the claim.

## A.6.RSIR:3 - Forces {#forces}

| Force | Tension |
|---|---|
| Recognition vs ontology | Engineering words are useful entry cues, but FPF use needs the governed object or claim kind. |
| First-level repair vs overreach | The pattern must recover enough to choose the direct pattern without becoming a second ontology for relation, role, interface, capability, method, function, evidence, or status. |
| Declaration and binding precision vs system-role ontology | One exact direct participant or bound value may itself be a system-role kind, assignment, system, or another entity. A compatible `SlotSpec` or A.6.1 declaration may type the reusable use, but participant, declaration content, exact application, binding occurrence, designation, and representation position remain distinct. |
| Interface usefulness vs interface-as-kind collapse | Interface words are often useful, but they may point to several different subject patterns. |
| Minimal rewrite vs precision | Ordinary prose can remain ordinary; claim-bearing prose must name the governed object, direct relation use, declaration, or representation correspondence on which it relies. |
| Source label preservation vs misuse | A source label can remain quote-only or reduced-use, but it cannot silently make work, evidence, assurance, gate, publication, or architecture claims admissible. |

## A.6.RSIR:4 - Solution {#solution}

Use `A.6.RSIR` as a first-level recovery move. `RSIRRepairNote` is optional working support, not a required record, schema, or publication layout. Omit every branch that is not current. The ordinary path may stop after `projectConcern`, `recoveredEntityOfConcernOrClaimKind`, `selectedSubjectPatternLocator`, and one result stated as `retainedSourceLabelUse`, `blockedOverread`, or `nextAdmissibleUse`. The PatternID is only a locator for applicable defining, constraining, or testing content.

```text
RSIRRepairNote (optional working support; keep only current lines):
  projectConcern:
  recoveredEntityOfConcernOrClaimKind:
  selectedSubjectPatternLocator?: PatternID used only as a locator
  retainedSourceLabelUse?:
  blockedOverread?:
  nextAdmissibleUse?:
  encounteredWording?:
  currentUse?:
  directParticipantMeaningAndActualParticipant?:
  relationDeclaration?:
  assertionOrDescriptionDesignation?:
  operationDeclaration?:
  exactOperationApplicationAndBinding?:
  representationUseAndCorrespondence?:
  neighboringCandidateValues?:
  stopCondition?:
```

When the optional note is used, it is complete when the current object or claim kind is clear enough to apply the subject pattern, keep ordinary prose, keep quote-only wording, or stop the stronger claim. No unused branch is filled for completeness.

### A.6.RSIR:4.1 - Recovery order {#recovery-order}

1. **Recover the project concern.** Say what the project is trying to do: assign work responsibility, declare a signature, check an interface, compare functions, name a port, use evidence, assert status, describe a method, or make another claim.
2. **Recover the current object or claim kind.** Decide whether the wording points to a direct relation or participant meaning, an actual participant, a reusable `RelationSignature` or `SlotSpec`, an assertion- or description-side participant designation, an A.6.1 argument or result declaration, one exact operation application and actual binding, a representation position and correspondence, a signature, interface claim, system-role kind, system-role assignment, system-role-kind description, port, boundary claim bundle, capability, affordance, Method, function, concern, interest, publication, source label, or ordinary prose.
3. **Name the applicable rule.** Use the table in `A.6.RSIR:4.2` only until the definition, constraint, or test needed by the current question is clear. Record its PatternID only as a locator.
4. **Separate direct participation, reusable declaration, and assertion or description.** Use `A.6.5` only when one complete `SlotSpec` in one exact `RelationSignature` is current. The direct relation pattern defines or constrains participant meaning, actual participants, obtaining, and occurrence identity. If an assertion or description episteme designates a participant, `C.2.1` governs that episteme's identity and content, while the direct assertion, evaluation, evidence-use, or description family governs the exact predicate, polarity, or use relation. When a compatible `SlotSpec` is current, `A.6.5` governs the designation's `ValueKind` and `refMode` discipline; an ordinary assertion may instead name actual participants directly without opening a reusable `RelationSignature`.
5. **Separate operation declaration, actual application and binding, and representation.** Use `A.6.1` for declaration-local `ArgumentDeclaration` and `ResultDeclaration` content. Open an actual operation-application binding only after one exact application has been independently identified and its actual bound value matters to a receiving claim. Keep a method-call, formula, tuple, edge, or schema place under `C.29` or its exact representation pattern and state correspondence separately.
6. **Keep the source label reduced-use when no governed claim is current.** A word can remain a cue, quotation, title, or local shorthand without being admitted as FPF-governed vocabulary.

Use Tech `position` only for a place in a selected representation, such as a tuple component, formula or method-call argument, graph-edge endpoint, or schema field. Until an explicit correspondence is stated, that position is neither a relation-participant meaning, actual participant, `SlotKind`, `SlotSpec`, nor evidence that the direct relation obtains.

### A.6.RSIR:4.2 - Subject pattern selection {#subject-pattern-selection}

| Recovered object or claim kind | Apply this rule or pattern family | RSIR boundary |
|---|---|---|
| direct relation wording | `A.6.P` for recovery, then the rule that defines or tests the direct relation; use `A.6.REL` only when a receiving claim needs explicit occurrence identity or reference | RSIR stops when that direct rule is selected. An ordinary readable assertion may stop before explicit occurrence individuation or identifier assignment. |
| direct relation-participant meaning or actual participant | the direct relation pattern; add `A.6.5` only if a receiving use needs a reusable typed declaration | State the participant meaning and actual participant directly. Neither one is a `SlotKind`, `SlotSpec`, designation, operation binding, or representation position. |
| reusable relation-declaration slot, field, parameter, argument, or endpoint | `A.6.5` for one complete `SlotSpec` inside one exact `RelationSignature`, with `A.6.0` for the containing signature | The `SlotKind` is declaration-local and corresponds to one already recovered participant meaning; the declaration does not make the relation obtain. |
| assertion- or description-side participant designation | `C.2.1` for episteme identity and content; the direct assertion, evaluation, evidence-use, or description family for predicate, polarity, and use; `A.6.5` only when a compatible current `SlotSpec` types the designation | An ordinary assertion may name actual participants directly. A typed designation remains episteme content: it is neither the actual participant nor evidence that the direct predicate obtains. |
| operation argument or result declaration | `A.6.1` and the exact mechanism edition and operation declaration | `ArgumentDeclaration` and `ResultDeclaration` are declaration content. Do not reuse relation `SlotSpec` vocabulary for them. |
| exact operation application or declaration-local argument or result binding | `A.6.1` and the exact mechanism edition and operation declaration | Identify the application occurrence independently; assert a binding only for the exact application and actual bound value under the declared predicate. Do not admit public `OperationApplication`, a universal input/output/result relation, or infer production, a produced entity, result episteme, evidence, or work from a result binding. |
| tuple component, formula or method-call argument, graph-edge endpoint, schema field, or other representation position | `C.29` or the exact representation or publication pattern | Keep the position inside that representation and state explicit correspondence when an FPF claim consumes it; do not turn it into a relation participant, declaration, or actual binding by form. |
| signature or law-governed declaration | `A.6.0`; use `A.6.5` only for `SlotSpec` declarations inside a `RelationSignature`, and `A.6.1` for operation argument and result declarations | Do not put mechanisms, methods, work, evidence, actual participants, operation applications or bindings, or representation positions into signature identity-bearing content. |
| bare *role* already recovered as an exact local system-role kind — RSIR non-use | Apply `E.10.ROLE` once, then `A.2`, `C.3`, and the description or naming rules when their use is current | Do not apply RSIR. A system-role kind classifies entities already admitted as systems. It is not a `SlotKind`, assignment, capability, Method, status, or representation position. |
| bare *role* already recovered as a system-role assignment — RSIR non-use | Apply `E.10.ROLE` once, then `A.2.1`; when precise performed Work is claimed, recover each exact actual performer through A.13 and let A.15.1 independently admit the dated Work, adding F.6 only when the claim expressly consumes precise assignment-bound attribution through the same obtaining A.13 assignment; apply `A.6.5` only for a reusable species declaration | Do not apply RSIR. Recover the assignment occurrence and its declared `U.SystemRoleAssignment` species. The species defines the participant meanings; the occurrence supplies the holder System, assigned local kind, and any other participants. Taxonomy and scheme epistemes are not generic participants. Assignment extent follows uninterrupted predicate truth; a receiving assertion or use names any interpretation edition it depends on. |
| state of an assignment to a system role, or structure of relations among system-role kinds | `A.2.5`, `A.2.7` | Recover `SystemRoleAssignmentStateRelation` or `SystemRoleKindRelationStructure`; infer neither from ordinary label chains. |
| system-role-kind description or durable system-role-kind name | `F.4`, `F.5`, `F.18`, and `F.17` when public or cross-context reuse is current | Name the exact local kind or its description episteme. Do not hide assignment, capability, Method, or Work inside the name. |
| independently encountered system-role enactment or assignment wording | When precise performed Work is current, apply A.13 first and let A.15.1 independently admit the dated Work; apply A.2.1 and F.6 afterward only when the claim expressly consumes precise assignment-bound attribution through the same obtaining A.13 assignment. If the starting cue was bare *role*, apply `E.10.ROLE` once and do not apply RSIR after it selects this branch | Recover the exact actual performer `S : U.System` and dated `W : U.Work`. For an attribution-bearing claim, also recover the exact obtaining `RA : U.SystemRoleAssignment` and use `performedUnderAssignment(W, RA)` or the Plain sentence `S performed W under RA`; F.6 identifies neither S nor RA, and missing or failed F.6 leaves W intact. Create no second enactment object beside Work and assignment. |
| module interface or architecture interface | `A.6.M` for module-interface claims; `C.30`, `C.30.ASV`, `C.30.AD`, or `C.30.TFS-REL` for architecture-of, structural-view, architecture-description, or transformation-flow-structure claims; `A.6.0` plus `A.6.5` only for a reusable `RelationSignature` and its complete `SlotSpec`s; `C.29` or the exact representation pattern for interface diagrams or schema positions and their correspondence | Do not create generic `U.Interface`. |
| Markov blanket, Markov border, computational boundary, boundary leak, or active-inference boundary | Recover the current claim before choosing a pattern: accepted local Markov dynamics (`A.3.3`), mathematical or probabilistic lens (`C.29`, sometimes `C.26`), viability or measure-model-act envelope (`C.26.3`), holon delimitation or boundary crossing (`A.1` plus the direct governing relation pattern), relation precision (`A.6.P` after a relation-bearing case is recovered), reusable `RelationSignature` and `SlotSpec` declaration (`A.6.0`, `A.6.5`) or representation position and correspondence (`C.29` or the exact representation pattern), module-interface or interface-specification claim (`A.6.M`), functional port or functional element (`A.6.F`), physical component (`A.14`, `C.13`, `B.3.5`), boundary description or publication (`C.2.1` for claim-bearing description content, `C.30.AD` for architecture descriptions, `E.17` for reader-facing publication of an already accepted account), agency-threshold claim (`A.13` for the agency criterion, `C.16` when a value must be made interpretable as a measurement, `A.19` when a declared `CharacteristicSpace` or reusable by-value `CharacteristicSpacePredicate` over it is the current object), or boundary-package statement classification (`A.6.B`) only when L, A, D, or E classification is the recovered object. | Do not create `U.MarkovBlanket`, generic `U.Boundary`, generic `U.Interface`, or binary `U.Agent`; do not treat a statistical separation, interface, interface module, physical component, description, and boundary-package classification as the same object. |
| functional port or functional structure | `A.6.F`, `A.3.4`, `E.18`, `C.30.TFS-REL` | Do not equate port, function, module interface, and signature by vocabulary alone. |
| API, protocol, connector, service-access wording | Recover the governed object first: `E.17` for API or interface-description publication; `A.6.0` and `A.6.5` for a reusable `RelationSignature` and its `SlotSpec`s; `C.29` or the pattern that defines the exact API-description claim for schema or representation positions and explicit correspondence; `A.6.M` for module-interface claims; `A.6.C` only when recovered protocol, service-term, SLA, or agreement-like wording bundles promise, utterance or publication, governance, Work or consequence, or evidence claims; `A.6.P:4.11a` when service or service-access wording still hides its exact referent or direct relation; `A.6.B` only for L, A, D, or E statement classification inside a boundary package. | API may be description, protocol episteme, exact service or access referent or direct relation, signature, publication, module interface, representation, or boundary-package statement classification. |
| capability | `A.2.2`; method, work, evaluation, or gate patterns only when they use an explicit capability criterion | Role labels and interface labels do not establish or demonstrate capability. |
| affordance or action invitation | `A.6.A` | Do not rename affordance as role, interface, or capability until its exact predicate and current subject assertion establish that value. |
| method, method description, work plan, or dated work | `A.3.1`, `A.3.2`, `A.15`, `A.15.1`, `A.15.2` | Method, description, plan, and work are distinct even when source wording says process. |
| function or functional wording | `A.6.F` | Function-like wording can point to several patterns; `A.6.F` governs that recovery. |
| concern, interest, viewpoint, problem, or characteristic-space selection | `A.7` for EntityOfConcern and description distinction; `C.22` or `C.22.2` for problem-card claims; `E.17.0` or `E.17.2` for viewpoint or view claims; `F.4` or `F.18` for system-role-kind-description or naming cases; `A.19` or `E.21` for characteristic-space cases | Do not mint generic `U.Concern` or `U.Interest` by wording alone. |
| publication, description, declarative representation, source wording | `C.2.1`, `E.17`, `C.2.P.DR`, `E.10`, `E.10.ARCH` | Do not let description or publication use displace the EntityOfConcern selected by the project concern. |

### A.6.RSIR:4.2.1 - Relation-defined wording dispatch {#relation-defined-wording-dispatch}

When wording derives a qualification, status, or category from participation in a relation, recover the object needed by the next use before naming it:

1. If the claim concerns an actual entity participating under one named relation-participant meaning, state the direct relation, that meaning, and the actual participant. The participant retains its direct kind.
2. If reusable typed declaration is current, use `A.6.5` for the corresponding `SlotSpec` inside one exact `RelationSignature`. Its `SlotKind` is declaration-local and neither is the participant nor makes the relation obtain.
3. If an episteme asserts, evaluates, or describes the participation, `C.2.1` governs the episteme's identity and content, while the direct assertion, evaluation, evidence-use, or description family governs the exact predicate, polarity, or use relation. When a compatible `SlotSpec` is current, `A.6.5` governs the participant designation's `ValueKind` and `refMode` discipline; without reusable declaration, the assertion may designate the actual participants directly.
4. If repeated local quantification over such actual participants is current, use `C.3` and `C.3.1` for the local `U.Kind`, membership rule, and extent rule. Neither the participant-meaning label nor the declaration-local `SlotKind` admits that kind.
5. If the source exposes a tuple component, argument, edge endpoint, schema field, or other representation position, keep it under `C.29` or the exact representation pattern and state an explicit correspondence before an FPF claim consumes it. A value shown at that position establishes neither actual participation nor relation obtaining.

For parameter, argument, or result wording, separately recover the A.6.1 declaration content, one independently identified exact operation application and any obtaining declaration-local binding, and the selected representation position. Open the binding only when the actual bound value matters to a receiving claim. Neither the declaration nor representation syntax establishes the binding; a result binding is distinct from production, a produced entity, a result episteme, evidence, and work.

When a receiving use compares or constrains a whole organization of relation occurrences, `A.22` may govern a selected `U.Structure`. One actual participant, corresponding `SlotSpec` or designation, operation binding, or representation position does not by itself establish such a structure.

### A.6.RSIR:4.3 - Replacement candidate rule {#replacement-candidate-rule}

Do not replace one umbrella with another. The minimum admissible repair candidate names:

- the current object or claim kind;
- the subject pattern;
- one result current for the receiving use: a retained reduced-use source label, a blocked stronger reading, or the next admissible use.

Name a direct relation, claim-bearing episteme, declaration-local `SlotSpec`, A.6.1 operation declaration or actual application binding, or representation correspondence only when that exact object is current for the receiving use. Do not fill an unused branch or require both a retained source-label use and a blocked overread. If the minimum cannot be named, leave the phrase in quote-only or reduced-use form and record the blocker.

### A.6.RSIR:4.4 - Reduced-use source labels {#reduced-use-source-labels}

Reduced-use labels are allowed. They are not failures. A source label remains reduced-use when it helps readers find or recognize the case but does not carry FPF-governed content.

Examples:

- “API role” can remain a quoted source phrase while the branch is selected with `E.10.ROLE`. The repaired claim may be an API description, an exact provider system-role assignment, a declaration or representation position, a promise-content episteme under A.2.3, an independently obtaining commitment under A.2.8, `PromiseContentUse`, a delivery or acceptance relation, another named direct relation, or an interface specification.
- "parameter" can remain ordinary prose while a complete `SlotSpec` is named only for a current reusable relation declaration, an operation `ArgumentDeclaration` or `ResultDeclaration` and any exact application binding stay under `A.6.1`, and a method-call, formula, or other representation position stays under `C.29` or its exact representation pattern.
- "function" can remain ordinary engineering language when no architecture, capability, method, work, mathematical, quality, or module claim depends on it.

### A.6.RSIR:4.5 - Shortcut Cost and Reopen Condition {#shortcut-cost-and-reopen-condition}

`A.6.RSIR` is a deliberately weak first-level recovery move. The baseline is full use of the subject pattern: `A.6.P` for relation repair, `A.6.5` only for reusable `RelationSignature` `SlotSpec` discipline and compatible participant-designation typing, `C.2.1` plus the direct claim family for assertion or description content, `A.6.1` for operation declarations and any exact application binding, `C.29` or the pattern that defines the exact representation claim for positions and correspondence, `A.2`, `C.3`, and `A.2.1` for system-role kinds and system-role assignments after that branch is selected with `E.10.ROLE`, `A.6.M` for module-interface, `A.6.F` for function-like repair, or the evidence, status, publication, architecture, method, work, gate, or problem pattern named by value.

The saved effort is that a practitioner does not run several full patterns before knowing which one is current. The loss budget is narrow: RSIR may select a direct pattern, preserve a reduced-use source label, or record a blocker. It may not decide the system-role kind, system-role assignment, signature, operation application or binding, evidence-use relation, status assertion, exact service or access relation, architecture description, or Method relation that belongs to the selected pattern.

Reopen RSIR when the selected pattern shows that the source phrase carried more than one governed object, the object kind was selected too early, a needed slot distinction was missed, or evidence, status, publication, gate, method, work, architecture, capability, or concern claims were folded into one label. The reopened repair splits the phrase into multiple governed values or keeps the excess wording reduced-use.

## A.6.RSIR:7 - Conformance Checklist {#conformance-checklist}

1. The repair starts with project concern, not with a replacement word.
2. The current EntityOfConcern or claim kind is named before a subject pattern is applied.
3. The repair stops once the applicable rule and concrete next action are clear.
4. When reusable relation declaration is current, slot discipline uses `A.6.5` and states one complete `SlotSpec = <SlotKind, ValueKind, refMode>` inside one exact `RelationSignature`; actual participants and representation positions remain outside it.
5. A system-role-assignment claim names one occurrence and its declared `U.SystemRoleAssignment` species. The species defines the participant meanings and rule; the occurrence supplies its holder, assigned local kind, and any other participant that distinguishes it. Apply the direct rule for a system-role-kind description, `SystemRoleAssignmentStateRelation`, selected structure among system-role kinds, capability, Method, planned Work, or performed Work; do not apply RSIR merely to repeat that result.
6. Evidence-use and status-use cases are not represented through `U.SystemRoleAssignment` for epistemes. Apply `E.10.ROLE` once to bare *role*; if it recovers evidence use, status use, or another direct object, apply that object's rule and leave RSIR closed.
7. Interface wording is kept as a recognition cue but is not admitted as generic `U.Interface`.
8. Every neighboring object family selected in the dispatch table uses its defining or testing rule rather than being redescribed inside RSIR.
9. Relation-defined wording dispatches separately to the direct participant meaning and actual participant; a declaration-local `SlotSpec` when reusable typing is current; an assertion- or description-side designation whose episteme identity and content stay with `C.2.1`, whose predicate, polarity, and use stay with the direct claim family, and whose typing stays with `A.6.5` only when a compatible `SlotSpec` is current; a C.3 local kind when repeated quantification is current; or a representation position plus explicit correspondence. It does not create one umbrella qualification object.
10. Operation wording keeps A.6.1 `ArgumentDeclaration` or `ResultDeclaration` content, one independently identified exact application and obtaining argument or result binding, and any call or formula representation position distinct; it infers neither a public application kind nor production, a produced entity, a result episteme, evidence, or work from the binding.
11. Quote-only or reduced-use labels carry no action-facing claim beyond the claim admitted by the selected rule.

## A.6.RSIR:9 - Consequences {#consequences}

`A.6.RSIR` adds a bounded recovery step when the engineering object or claim remains unclear after the F.19 reading with E.10 cues. The selected subject pattern then handles the substantive claim; neighboring patterns can refer to this recovery instead of repeating it.

The pattern also keeps useful source vocabulary alive. Engineers can still say interface, API, role, parameter, function, and endpoint. FPF simply refuses to let those words select ontology by themselves.

The cost is one explicit stop: after the direct pattern is clear, RSIR must stop. Otherwise it becomes the giant repair pattern it was created to avoid.

## A.6.RSIR:12 - Relations {#relations}

Use `F.19` for the whole-span reading with the compact cues in `E.10:0.2`. Apply `E.10.ROLE` once to bare claim-bearing *role*. Apply RSIR afterward only if one concrete direct-relation, declaration, interface, operation, or representation question remains; all other recovered branches use their direct rules and leave RSIR closed. `E.10.ARCH` describes both entries in the shared restoration architecture.

`A.6.5` defines complete declaration-local `SlotSpec = <SlotKind, ValueKind, refMode>` content inside one exact `RelationSignature` and, only when a compatible `SlotSpec` is current, participant-designation typing. `C.2.1` supplies the assertion or description episteme's identity rule, while the direct claim rule supplies predicate, polarity, and use. An ordinary assertion may designate actual participants directly without reusable declaration.

Apply `A.6.P` for relation precision restoration after the recovered object is a relation or relation-bearing claim.

`A.6.0` defines `U.Signature`; `A.6.1` defines operation argument and result declaration content plus the rules for any independently identified exact application and declaration-local binding; `E.20` supplies mechanism-introduction rules. A.6.1 admits no public `OperationApplication` U-kind or universal input/output/result relation, and its result binding alone establishes none of production, a produced entity, a result episteme, evidence, or work.

`A.2`, `A.2.1`, `A.2.2`, `A.2.5`, `A.2.7`, `A.15`, and Part F system-role-description and naming patterns define or constrain local system-role kinds, direct system-role assignments, capability, `SystemRoleAssignmentStateRelation`, `SystemRoleKindRelationStructure`, system-role–Method–Work alignment, and durable system-role-kind names.

Apply `A.6.M`, `A.6.F`, `A.6.A`, `A.3.4.P`, `E.18`, `C.30`, `C.30.ASV`, `C.30.AD`, or `C.30.TFS-REL` for the corresponding module-interface, functional, affordance, transformation, transformation-flow, architecture-of, structural-view, or architecture-description question.

Apply `C.2.1`, `E.17`, `C.2.P.DR`, `A.10`, `B.3`, `G.6`, `F.10`, or `C.28` for the corresponding episteme identity and content, publication, declarative representation, evidence, assurance, provenance, status, or causal-use question; the exact direct claim rule still supplies the predicate, polarity, or use asserted through that content.


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/E-10#root, spec://ai.lev/fpf-spec/contract/E-10-ARCH#root, spec://ai.lev/fpf-spec/contract/E-10-ROLE#root, spec://ai.lev/fpf-spec/contract/A-6-P#root, spec://ai.lev/fpf-spec/contract/A-6-REL#root, spec://ai.lev/fpf-spec/contract/A-6-0#root, spec://ai.lev/fpf-spec/contract/A-6-1#root, spec://ai.lev/fpf-spec/contract/A-6-5#root, spec://ai.lev/fpf-spec/contract/C-2-1#root, spec://ai.lev/fpf-spec/contract/A-2#root, spec://ai.lev/fpf-spec/contract/A-2-1#root, spec://ai.lev/fpf-spec/contract/A-15#root, spec://ai.lev/fpf-spec/contract/C-29#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/A-6-M#root, spec://ai.lev/fpf-spec/contract/A-6-F#root, spec://ai.lev/fpf-spec/contract/A-6-A#root, spec://ai.lev/fpf-spec/contract/A-3-4-P#root, spec://ai.lev/fpf-spec/contract/C-2-P#root, spec://ai.lev/fpf-spec/contract/C-2-P-DR#root, spec://ai.lev/fpf-spec/contract/E-17#root, spec://ai.lev/fpf-spec/contract/A-10#root, spec://ai.lev/fpf-spec/contract/F-10#root, spec://ai.lev/fpf-spec/contract/G-6#root, spec://ai.lev/fpf-spec/contract/F-18#root, spec://ai.lev/fpf-spec/contract/F-19#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-2#root, spec://ai.lev/fpf-spec/contract/A-2-4#root, spec://ai.lev/fpf-spec/contract/A-6-5#root, spec://ai.lev/fpf-spec/contract/A-6-P#root, spec://ai.lev/fpf-spec/contract/E-10-ROLE#root, spec://ai.lev/fpf-spec/contract/E-24-CD#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/A-6-RSIR
