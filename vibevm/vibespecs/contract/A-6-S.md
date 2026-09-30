# A.6.S - TargetSignature and optional ConstructorSignature - demand-driven signature engineering {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Architectural (A)
> **Status:** Stable
> **Normativity:** Mixed (normative where RFC 2119 keywords appear; quadrant classification is governed by A.6.B)
> **One-liner:** Start from the actual signature assertion, revision, relation, operation application, or Work. Add a separate ConstructorSignature only when a named receiving use needs reusable constructor vocabulary, laws, and applicability. Keep an operation description, any mathematical arrow, its application, performed Work, and publication faces distinct.

**E.24.UK settlement.** A.6.S admits no `U.SignatureEngineeringPair` kind or durable arrangement individual. The spelling is retired. `TargetSignature` and `ConstructorSignature` are use-specific designations for two independently identified `U.Signature` epistemes; neither designation adds another kind, constitution relation, or identity discriminator. Merely pairing two documents or naming both signatures establishes no relation between them.

**Use this pattern when** a project already has, or genuinely needs, a reusable signature that declares how another signature is to be authored or revised, and at least one named receiving use needs that declaration to remain stable across applications, editions, or publishers.

**Do not use this pattern** merely because one signature is edited, one direct relation is stated, one view is prepared, or one work occurrence changes a carrier. Apply that direct rule and stop. A one-off revision needs no ConstructorSignature.

**First useful move.** Say what changes in ordinary language: for example, `The editor added the refund law to PaymentBoundarySignature and issued edition 4.` Identify the changed signature episteme and, when current, the operation application, System, Work, result, or edition relation. Only then ask whether a later receiver needs a reusable declaration of the constructor operations.

**What goes wrong if missed.** At one extreme, the signature, the operation description, and the Work that changes or publishes it collapse into one “contract/editing” story. At the other, every small edit acquires a second signature, a pair object, two operation lexicons, and a full attribution package.

**What this buys.** The light path stays light. Where repeatable constructor language has real users, the ConstructorSignature can preserve that language while the TargetSignature, operation description, A.6.2 arrow, application, Work, assignment, carrier, and publication view keep their own identities and direct relations.

## A.6.S:1 - Problem frame {#problem-frame}

Boundary descriptions often arrive as “half-signatures”: an n-ary relation in ordinary prose, overloaded markers such as *binding*, *anchoring*, or *contract*, and unstated assumptions about participants, applicability, and publication. Teams then revise the boundary through edits, reviews, and partial publications.

A.6.5, A.6.6, A.6.2-A.6.4, and E.17 already govern several different moves that may occur during that work. The missing discipline is not a universal engineering container. It is a proportional choice:

1. state the actual edit, relation, arrow, application, Work, edition, or view and stop when that answers the use; or
2. when a named receiver needs the same constructor vocabulary and laws again, identify a separate ConstructorSignature and state the exact dependency or use that connects it to the work.

Without that choice, four failures recur:

1. the TargetSignature, constructor-operation description, application, and performed Work are conflated;
2. a one-off revision is inflated into a durable two-signature apparatus;
3. semantic changes hide behind generic edit language instead of identifying the receiving episteme and any actual edition, continuity, or reference change; and
4. publication views acquire claims not present in the described signature.

An episteme does not act. When performed Work is claimed, recover each actual performer `U.System` and the complete A.13 core, then independently admit the dated occurrence under A.15.1, as set out in §4.0. A System may separately apply a described operation. Use F.6 afterward only for a receiving claim that consumes precise assignment-bound attribution through the same obtaining A.13 assignment; F.6 identifies neither assignment nor performer, and the assignment itself does not act.

## A.6.S:2 - Problem {#problem}

FPF needs a pattern for **engineering signatures as boundary epistemes**: a disciplined way to construct, revise, and publish a target `U.Signature` from partial input, while maintaining:

* separation between *signature* and *mechanism* (A.6.0 vs A.6.1),
* separation between *laws*, *admissibility*, *deontics*, and *work evidence* (A.6.B),
* explicit multi‑view publication without semantic drift (E.17),
* reproducible evolution across editions without silent mutation.

## A.6.S:3 - Forces {#forces}

* **Stability vs evolution.** TargetSignatures must be stable enough to coordinate, yet change as understanding improves.
* **Explicitness vs overhead.** Unpacking slots/bases/views increases clarity but also increases authoring effort.
* **Arrow law vs enacted work.** An A.6.2 arrow may state the effect-free relation between source and receiving signature epistemes. An application of the described constructor operation has its own predicate, extent, and identity rule under A.6.1. Claims about a created successor or written carrier identify the changed object and effect; any performed Work is admitted separately. For performed Work, recover each actual performer's complete A.13 core and let A.15.1 independently admit the occurrence, as in §4.0. Add F.6 only when a later claim expressly consumes precise assignment-bound attribution through the same obtaining A.13 assignment; F.6 checks that exact Work-assignment link and identifies neither the assignment nor the performer. Missing or failed F.6 leaves the Work intact.

* **Multi‑view richness vs semantic coherence.** Views help stakeholders, but they risk becoming divergent “versions of truth”.
* **Local meaning vs cross-local reuse.** Signature claim content pins its effective ReferenceScheme where interpretation matters. The local kind and any source-local meaning remain separate values. Use F.9 for an actual semantic Bridge between exact local senses whose `<ReferenceScheme, LocalSenseClaim>` interpretation bases differ, and judge its bounded-use claim separately. Distinct F.17 cells or a mapping alone do not establish that relation.
* **Contract talk vs ontology.** “Contract” language invites mixing promises, norms, and invariants; FPF requires quadrant discipline.


## A.6.S:4 - Solution - start with the direct move; add a ConstructorSignature for named reuse {#solution-start-with-the-direct-move-add-a-constructorsignature}

### A.6.S:4.0 - Keep the signature, arrow, application, and Work separate {#keep-the-signature-arrow-application-and-work-separate}

The smallest account names the actual object and move. Describe a signature revision through its source and receiving signature epistemes. A changed C.2.1 discriminator identifies another episteme; an edition or continuity relation requires its own source use, continuation rule, and preserved or deliberately changed features. Republishing unchanged claim content need not identify another episteme. A view, direct relation assertion, operation application, carrier write, and performed Work remain under their own patterns.

A **ConstructorSignature** is optional. When used, it is a `U.Signature` whose reusable declaration content describes a family of constructor operations: its subject and value or result range, vocabulary, laws, and applicability. It does not perform those operations and does not contain the Work that applies them.

If a constructor family also uses an A.6.2 mathematical arrow, identify that arrow separately. The arrow relates exact source and receiving epistemes. Its rule states how their claim content, EntityOfConcern, and effective ReferenceScheme compare. When it reads a neighboring grounding, representation, conformance, edition, or provenance occurrence, name that occurrence and the endpoint facts compared; the arrow neither changes the occurrence nor makes it obtain. A.6.3 and A.6.4 apply only to their exact viewing or EntityOfConcern-retargeting cases.

When dated authoring, deriving, materializing, validating, storing, or publishing Work is claimed, first recover each actual performer as a System under A.1 and its complete A.13 core: the local agential system-role kind and criterion, System classification, obtaining A.2.1 assignment, and the scope, working situation, and window needed by the use, with evidence for those claims. A.15.1 then independently admits the dated occurrence from its performance history, at least one Method actually followed, temporal extent, and at least one obtaining locally declared containing-System relation. Use F.6 afterward only for precise assignment-bound attribution through that same obtaining assignment; missing or failed F.6 leaves the independently admitted Work intact. Additional classifications or assignments, an operation application and its bindings, the resulting episteme, and carrier, evidence, or publication relations enter only when their own claims are current. Add an agency-characteristic profile only when the local criterion, a claimed characteristic, or an assurance use requires it under A.13/A.15.1.

### A.6.S:4.1 - Decide whether a second signature is needed {#decide-whether-a-second-signature-is-needed}

Start with the **TargetSignature**: the `U.Signature` being authored, stabilized, or revised. Its A.6.0 declaration content identifies its subject and value or result range and supplies the reusable vocabulary, laws, and applicability that make it a signature. It contains neither operational gates, deontic duties, evidence claims, nor construction Work merely because those topics occur nearby.

Add a **ConstructorSignature** only when a named receiver needs reusable constructor-operation vocabulary, laws, and applicability. The receiver may be a later editioning process, another authoring System, a publication process, or another repeatable use that would otherwise have to reconstruct the same operation declaration. A one-off edit, direct relation assertion, arrow, operation application, or Work occurrence does not qualify by itself.

The two signatures remain separate C.2.1 epistemes. State only the relation that is actually current:

* when one signature cannot interpret a required term or replay a law without the other, use the exact A.6.0 declaration-dependency claim;
* when a System uses a Method or MethodDescription that cites the ConstructorSignature while revising the TargetSignature, state that method/source use and any actual application or Work under its direct pattern;
* when both signatures are merely relevant to the same local question, name them without inventing a pair relation; and
* if a future use needs a durable relation occurrence between them, first supply that relation kind's participant meanings, predicate, applicability, occurrence identity, and E.24/E.24.UK settlement. A.6.S supplies none by default.

`TargetSignature` and `ConstructorSignature` are Tech designations of each signature's place in this use, not local system-role kinds. A publication may explain TargetSignature as “the signature being engineered”; it need not introduce the abbreviation *SoI*. Do not conflate the TargetSignature with its exact C.2.1 EntityOfConcern. Distinct signature editions remain distinct epistemes when their C.2.1 discriminator triples differ; any empirical-grounding, edition, continuity, dependency, source-use, or publication relation remains separately identified.

**Mint-or-reuse note.** A ConstructorSignature is admitted by the ordinary A.6.0 membership rule, not by being named next to a TargetSignature.

### A.6.S:4.2 - Choose the constructor vocabulary that the receiving use needs {#choose-the-constructor-vocabulary-that-the-receiving-use-needs}

A ConstructorSignature declares only operation families that a named receiver will reuse. It need not contain both A.6.5 slot operations and A.6.6 declaration-change labels, and it need not contain either family when another direct operation declaration is enough.

**Slot operations, when current.** Use A.6.5 when a reusable relation declaration needs stable participant positions, fillers, or references. Its vocabulary distinguishes name binding, first or later by-value filling, reference retargeting, typed substitution, resolution, and parameter passing. Keep `bind` for name binding; do not use generic *edit* to hide a reference retargeting or a referent-internal change. A one-off ordinary edit that needs no reused SlotSpec stays an ordinary edit.

**Assertion or declaration history, when current.** Use A.6.6 first to state the actual dependent, base, and direct relation. Stop when that readable assertion answers the use. If a named receiver needs the history of an optional assertion representation or reusable declaration, its local labels such as `declareBase`, `rebase`, `rescope`, `retime`, or `refreshWitnesses` may describe which represented field changed. They do not establish or change the world-side relation. Producing new evidence is separate Work; changing a witness reference is only a record edit.

**Mathematical arrows, when current.** An operation description may cite an A.6.2, A.6.3, or A.6.4 arrow only when that mathematical relation is useful to the receiver. The ConstructorSignature states the arrow family and the endpoint values or facts it reads or compares. The arrow remains effect-free; an application that produces a receiving episteme and any performed Work remain separate.

**Publication operations, when current.** For E.17 publication, a ConstructorSignature may declare a reusable publication or view-producing operation when its named receiver needs that declaration. Apply A.6.3 only when the operation uses a mathematical source-to-receiving viewing construction; identify those epistemes and the viewing rule. Keep the publication face faithful to its source and apply §4.4 for any separate `U.View` claim. For publishing a face, writing a carrier, committing a file, or issuing a release, distinguish any claimed operation application under A.6.1, any actual changed-object or effect claim, and Work admitted under §4.0. Neither signature performs those actions.

The test is practical: remove the proposed operation family. If the named receiver can still perform or assess its use without reconstructing a shared vocabulary or law, leave that family out.

### A.6.S:4.3 - Change discipline: Viewing vs Retargeting vs editing {#change-discipline-viewing-vs-retargeting-vs-editing}

When more than one distinction is current, classify each move separately rather than forcing all four buckets into every revision:

1. **Publication form and conditional viewing.**
   A *presentation* change (views, stakeholder cards, projections) may be an E.17/E.24.PUB form or carrier change. Use A.6.3 only when a mathematical source-to-receiving viewing construction is current, preserving the exact EntityOfConcern; E.17.0 separately governs any `U.View` membership claim.

2. **Direct edits and conditional declaration history.**
   State a one-off vocabulary, law, applicability, or reference change directly. Use A.6.5 only for reusable relation-participant declarations or reference operations that matter to the receiver. Use A.6.6 declaration history only after the actual base-dependence relation is stated and a named receiver needs that history.
3. **Editioning + reference retargeting (A.6.5).**
   Use when the TargetSignature meaningfully changes and downstream coordination needs a new TargetSignature edition. Do not silently mutate the existing episteme: identify the successor edition and retarget the references whose receiving use now selects it (`Retarget<...>` in the relevant Ref slots).


4. **Epistemic retargeting and structural reinterpretation (A.6.4; rarer).**
   Use only when the source and receiving `EntityOfConcernRef` values resolve to different exact EntitiesOfConcern. A reference-only change that still resolves to the same entity stays with its actual reference operation. A.6.4 identifies the source and receiving epistemes and one exact arrow `r`. A separate C.2.1 bounded-use assertion `q` is about that exact `r`; its ClaimGraph contains the invariant, visible loss, named receiving use, conditions, and affirmative or negative polarity. A separate current-case judgement compares the exact facts with `q` and returns exactly `satisfies`, `fails`, or `cannot decide`; `cannot decide` names the missing fact and reopen condition. This is distinct from an ordinary new edition of the same TargetSignature.

Rule of thumb:

* If only the publication form or carrier changes, use E.17/E.24.PUB and stop; no slot/base declaration is required unless another receiving use needs it.
* If the change is “new TargetSignature edition for consumers”, identify the new edition and explicitly retarget the references whose receiving use now selects it.
* If the change is a different EntityOfConcern, use A.6.4's three-part account: the exact arrow `r`, a separate C.2.1 bounded-use assertion `q`, and a separate current-case judgement. A kind difference alone identifies none of them.

**EFEM discipline.**
When a constructor operation really uses an A.6.2 arrow family, declare its endpoint comparison and `entityOfConcernChangeMode` under A.6.2. An operation description that needs no mathematical arrow introduces none.
**Editioning is orthogonal**: you MAY mint a new edition even under `preserve`; references whose receiving use now selects that edition MUST be retargeted explicitly, with A.6.5 slot discipline where applicable.
For an actual measurement, actuation, validation run, carrier write, or other effect, identify any claimed operation application under A.6.1, changed-object or effect claim under its direct rule, and Work under §4.0 independently. An effect alone establishes neither application nor Work; the A.6.2 arrow performs none of these actions.

### A.6.S:4.4 - Add publication and claim controls only when they are current {#add-publication-and-claim-controls-only-when-they-are-current}

For E.17 publication, choose a faithful publication form for the bounded reader/use and point to the exact source episteme edition. Preserve E.17's no-content-extension rule: informative explanation may expose source meaning without adding boundary commitments. Only when the selected episteme's `U.View` membership is asserted or needed, resolve its exact viewpoint and E.17.0 conformance; add an A.6.3 source-to-receiving construction only when that separate relation is current. The publication occurrence, carrier, viewpoint use, conformance claim, and any publication Work remain separate. When E.17's CC-MVPK-3b boundary claim-set condition applies, keep normative face text traceable to that A.6.B claim set, with informative commentary; a face does not become a second boundary specification. No MVPK package is required merely because a signature changed.

Classify atomic claims under A.6.B, keeping laws, operational admissibility, deontic commitments, and evidence-use claims separate. Correct quadrant classification alone needs no register. Use the applicable claim register when stable identifiers serve reuse, a decision, audit, or cross-face citation; keep a return to the claim's ID or canonical source location for a material dependency. Do not put operational gates, duties, evidence results, or Work into the TargetSignature merely to make one authoring record complete. Without a need for the register, ordinary claim content and the direct patterns are enough.

### A.6.S:4.5 - Signature-construction relation in a transformation-flow structure (informative) {#signature-construction-relation-in-a-transformation-flow}

If a team represents actual signature-construction Work as an E.18 `TransformationFlowStructure`, reference only the A.6.S objects and direct relations that the flow uses; do not convert them into a second graph ontology:

* Declared constructor arrows may appear at transformation-flow loci as independently defined A.6.2 values over signature epistemes. An actual operation application and any performed Work remain separately identified.
* Concrete carrier writes (commits, releases, registry writes, and carrier and source-currentness pinning) may be admitted as Work under §4.0; an E.18 Work locus may bind that already admitted Work. Use F.6 afterward only when the receiving flow account consumes precise attribution through the performer's obtaining A.13 assignment; missing or failed attribution leaves the carrier-write Work intact. Use A.10 for evidence and provenance, E.17 for publication, and the relevant carrier patterns for carriers. The constructor-operation declaration, any identified application that writes a carrier, and the admitted Work remain distinct.
* For validation and admission, E.18 governs any selected gate/check position; each check follows its own subject rule. When an actual gate decision is present, use A.21 and name its exact `GateDecisionResult`, bounded action, applicable `GateProfile` application, complete required `GateCheckApplicationResult` set, decision value, consequence, scope/window, and recheck condition. Use a short `GateCheckRef` only when a selected publication structure needs one, and a `DecisionLog` only when audit or reuse is current.
* When the source and receiving `EntityOfConcernRef` values resolve to different exact EntitiesOfConcern, use A.6.4: identify the exact arrow `r`, separate bounded-use assertion `q`, and any separate current-case judgement, then let E.18 place each only when that transformation-flow use is current. A kind change without that basis supplies no positive claim, and any actual operation application remains separate.

This mapping is optional. A one-off revision needs neither an E.18 flow nor a ConstructorSignature. When a flow is current, use E.18 for its structure and E.18.2 for any mathematical description of that selected structure, including a graph or path description. Use C.29 only for a declared mathematical-lens use. A.6.S identifies the TargetSignature and any independently justified ConstructorSignature and operation declarations.

### A.6.S:4.6 - State during construction (informative) {#state-during-construction-informative}

Do not mint a new kernel “signature state” unless you need it.
In most cases, use:

* **edition** + explicit continuity/withdrawal links for semantic evolution, and
* a coarse **status** (`Draft`/`Review`/`Stable`/`Deprecated`) for process signalling.

If a project needs a reusable state-change policy, place it in the applicable signature's declared content or in a separately identified policy episteme, according to its actual EntityOfConcern and use. A one-off status change is stated directly.
Where state-change policy is normative, express it as a status or state-transition policy for the relevant signature episteme or publication under its effective scheme and ClaimScope, with A.2.4 and F.10 status-use discipline and A.6.5 slot discipline where needed. Do not call the episteme's status a system role or create a system-role assignment for it; use E.10.ROLE to route bare *role* wording to the actual status, state, declaration position, or other direct branch.

## A.6.S:7 - Conformance Checklist {#conformance-checklist}

| ID | Requirement | Purpose |
| ---: | --- | --- |
| **CC-A.6.S-1** | @fact:CC-A-6-S-1 State the actual assertion, revision, relation, arrow, application, or Work first. If it answers the receiving use, no ConstructorSignature or pair object is required. @status:spec/done | Preserves the cheap direct path. |
| **CC-A.6.S-2** | @fact:CC-A-6-S-2 A ConstructorSignature appears only when one named receiving use needs reusable constructor vocabulary, laws, and applicability. It is an independently identified `U.Signature`; `U.SignatureEngineeringPair` is not used. @status:spec/done | Prevents an unsupported object and needless second signature. |
| **CC-A.6.S-3** | @fact:CC-A-6-S-3 When two signatures are both current, state the exact A.6.0 dependency, method/source use, or other direct relation that actually obtains. Co-mentioning them creates no relation. @status:spec/done | Keeps the connection explicit without inventing a universal pair. |
| **CC-A.6.S-4** | @fact:CC-A-6-S-4 The ConstructorSignature declares only operation families its named receiver reuses. A.6.5 slot verbs, A.6.6 declaration-change labels, A.6.2-A.6.4 arrows, E.17 views, assignment identity, and evidence are each conditional on their own current use. @status:spec/done | Prevents the constructor menu from becoming a mandatory package. |
| **CC-A.6.S-5** | @fact:CC-A-6-S-5 A meaning change identifies a new TargetSignature episteme when a C.2.1 discriminator changes. State edition, continuity, and reference-retargeting claims only under their actual predicates; use A.6.4 only when the exact EntityOfConcern-retargeting arrow `r` is current, and identify any bounded-use assertion `q` and current-case judgement separately. @status:spec/done | Separates episteme change, editioning, reference change, and retargeting. |
| **CC-A.6.S-6** | @fact:CC-A-6-S-6 If an A.6.2-A.6.4 arrow is declared, keep the arrow, any separately governed use assertion, any current-case judgement, operation description, application, and Work distinct. Name the endpoint values and neighboring facts read or compared; the arrow changes no neighboring relation occurrence. @status:spec/done | Preserves the accepted arrow/application/Work boundary. |
| **CC-A.6.S-7** | @fact:CC-A-6-S-7 If E.17 publication is used, each face is a faithful publication form over the exact source episteme and adds no new claim. A claimed `U.View` requires E.17.0 conformance; an A.6.3 construction is separate and conditional. Preserve applicable boundary claim-set traceability under §4.4. The publication occurrence, carrier, viewpoint use, conformance, and Work remain separate. @status:spec/done | Prevents publication drift. |
| **CC-A.6.S-8** | @fact:CC-A-6-S-8 A System, not a signature, assignment, or local system-role kind, performs actual Work. Recover each actual performer's complete A.13 core, including its classification and obtaining A.2.1 assignment, and let A.15.1 independently admit the Work as in §4.0; add the separate F.6 Work-assignment relation afterward only when the receiving claim consumes precise attribution through that same assignment. Add application, carrier, provenance, or evidence relations only when their own distinctions are needed. @status:spec/done | Preserves agency without mandatory attribution paperwork. |
| **CC-A.6.S-9** | @fact:CC-A-6-S-9 Laws, operational admissibility, deontic commitments, evidence use, and Work remain under their direct patterns. The TargetSignature and ConstructorSignature do not become all-purpose containers. @status:spec/done | Preserves A.6.B and direct-relation boundaries. |
| **CC-A.6.S-10** | @fact:CC-A-6-S-10 The account begins with an ordinary sentence naming what changed or was reused and what visible result follows. Formal vocabulary is added only where it changes a receiving inference. @status:spec/done | Keeps the pattern usable by a cold reader. |

## A.6.S:9 - Consequences {#consequences}

**Benefits.** One-off work remains readable and cheap. Repeated engineering can still reuse a stable ConstructorSignature. Edition, view, arrow, application, Work, assignment, evidence, and carrier claims remain independently repairable.

**Costs.** A project must decide whether reusable constructor content exists instead of opening a standard package automatically. When it does exist, maintaining another signature costs attention. The mitigation is the named-receiver test and a declaration containing only the vocabulary and laws that receiver reuses.

**Adoption test (informative).** Ask three questions in order: What actual signature claim or change is current? Does that direct account answer the use? Which named receiver, if any, needs reusable constructor vocabulary and laws? A valid adoption result may contain one TargetSignature and one ordinary revision sentence, with no ConstructorSignature.

## A.6.S:12 - Relations {#relations}

* **Depends on:**

  * A.3.1/A.3.2/A.15/A.15.1/A.15.2 — Method, MethodDescription, WorkPlan, Work, and work-result separation
  * A.7 — Strict Distinction (object ≠ description ≠ carrier; Face ≠ Surface)
  * A.6 — Signature Stack: Classify and Place Boundary Claims
  * A.6.0 — `U.Signature`
  * A.6.2 — effect-free episteme-arrow discipline, only when a constructor operation uses a mathematical arrow; endpoint facts are read or compared, not changed by the arrow
  * A.1, A.13, and A.15.1 — System admission, the complete actual-performer core including local-kind classification and an obtaining A.2.1 assignment, and independent dated-Work admission; F.6 follows only for precise attribution through that same assignment
  * C.2.1 — episteme identity through claim content, exact EntityOfConcern, and effective ReferenceScheme, with empirical grounding and edition continuity kept as separate direct relations
  * (optional) E.18 — TransformationFlowStructure, when signature-construction work is represented as a transformation-flow structure
  * E.10 and LEX discipline — if the publication uses Plain twins (“SoI”) or shorthands, keep their exact Tech readings recoverable and keep Plain twins out of normative register
  * A.6.3 — `U.EpistemicViewing`
  * A.6.4 — EntityOfConcern-retargeting arrows, their separate C.2.1 bounded-use assertions, and separate current-case judgements
  * A.6.5 — relation-declaration slot discipline
  * A.6.6 — Base Declaration Discipline
  * A.6.B — Boundary Norm Square & Claim Register discipline
  * E.17 and E.17.0 — MVPK and multi‑view describing

* **Coordinates with:** A.6.5 for reused relation-participant or reference operations and A.6.6 for direct base-dependence assertions and optional declaration history; neither vocabulary is mandatory.

* **Constrains:** a signature-engineering use only where the relevant meaning change, edition, reference retargeting, view, application, or Work claim is current; one distinction does not make the others mandatory.


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/A-3-1#root, spec://ai.lev/fpf-spec/contract/A-3-2#root, spec://ai.lev/fpf-spec/contract/A-15#root, spec://ai.lev/fpf-spec/contract/A-15-1#root, spec://ai.lev/fpf-spec/contract/A-15-2#root, spec://ai.lev/fpf-spec/contract/A-7#root, spec://ai.lev/fpf-spec/contract/A-6#root, spec://ai.lev/fpf-spec/contract/A-6-0#root, A.6.2-A.6.6, spec://ai.lev/fpf-spec/contract/C-2-1#root, spec://ai.lev/fpf-spec/contract/A-2#root, spec://ai.lev/fpf-spec/contract/A-2-1#root, spec://ai.lev/fpf-spec/contract/F-6#root, spec://ai.lev/fpf-spec/contract/A-6-B#root, spec://ai.lev/fpf-spec/contract/E-17#root, and spec://ai.lev/fpf-spec/contract/E-17-0#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/E-18#root only when a TransformationFlowStructure is current, and spec://ai.lev/fpf-spec/contract/E-10#root for wording discipline. @status:spec/done

#source spec://ai.lev/fpf-spec/source/A-6-S
