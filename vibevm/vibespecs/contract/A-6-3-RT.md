# A.6.3.RT - Representation-Scheme Transition: Change Representation of the Same EntityOfConcern {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Specialization pattern
> **Status:** Stable
> **Normativity:** Normative

## A.6.3.RT:1 - Problem frame {#problem-frame}

Use this pattern when practical content must survive a change of representation scheme or reasoning medium: prose to table, table to diagram, diagram to structured notation, a model to a different inspectable rendering, or another declared representation change. In plain language: **change the representation while preserving what matters for this use**.

Start with the content that must survive and the action the new representation should support. The source can be givens, constraints and a partial construction while the answer is still unknown. Under an available scheme, make the target, compare it with the source, and state what was preserved, foregrounded, rearranged, lost or newly suggested. Exact episteme identities are not prerequisites for this ordinary first result.

Plain starting vocabulary:

| Term | Plain meaning |
| --- | --- |
| `source material` | The source claims, table, prose, diagram, model, record, publication, or other material being re-represented. In an exact case, distinguish the source episteme from its form, carrier, world-side concern, and additional inputs. |
| `content to survive` | The claims, relations, commitments, uncertainty, source pins, or distinctions the target representation must still support for the declared use. |
| `target representation` | The table, diagram, symbolic expression, sequence of signs or other representation made for the receiving task. Its visible form or carrier does not by itself identify a receiving episteme. |
| `representation scheme` | The conventions for forming and interpreting expressions in this use. Different expressions can use the same scheme. |
| `reasoning medium` | What the representation lets a user inspect, compare, infer, traverse, or replay more or less easily. |
| `representation delta` | What changed in shape, notation, salience, topology, ordering, interaction, or another representation factor. |
| `loss and recoverability` | What becomes harder to see or is omitted, and how the user can recover it when it matters. |
| `use and return` | What the target supports, what it does not support, and when and where to return to source material. |
| `representation worker` | The person, team, or system doing the conversion. Recover the exact system-role assignment, method, and dated Work only when production history matters; doing the work grants no authority over the represented claims. |

**First useful move.** Name the content that must survive and the target representation; make the target; then attach a compact representation note: source material, intended user action, target representation and why, preserved content, representation/reasoning-medium delta, loss or unsupported additions, admissible and non-admissible use, and return trigger.

**What goes wrong if missed.** A cleaner table, diagram, notation, or decoded rendering is treated as harmless formatting after it has hidden uncertainty, changed the concern, imported a new relation, weakened recoverability, or invited a stronger action than the source supports.

**What this buys.** Users gain a representation suited to their task while preservation, reasoning affordances, loss, unsupported strengthening, and source return stay visible.

**Ordinary use.** For inspection, comparison, source-finding, technical discussion, or reversible planning preparation, the target representation and compact note are normally enough.

**Reliance-facing use.** Open the exact episteme-construction branch when the target must travel independently, be cited or disputed, cross a scheme boundary for consequential use, be considered for admission as receiving episteme `Y` in a generated or decode-mediated case, or meet an exact-identity requirement from a named public, evidence, or assurance receiver. Then recover exact source episteme `X`, receiving episteme `Y`, and viewing construction `v : X -> Y`, together with the source claims and relations on which `v` depends, and the scheme relation, loss/recoverability, evidence, or assurance actually needed for that use.

**Later-specific occurrence.** Open `RepresentationSchemeTransitionRelation@Context` only when actual representation-transformation Work and the exact six participants defined in §4.1.b are themselves material. An exact `v : X -> Y` does not imply that occurrence.

**Not this pattern when.** Use A.6.3.CR for same-regime wording, A.6.3.NAR when reader-useful narrative ordering is primary, E.17.EFP when explanation adequacy is primary, A.6.4 when the EntityOfConcern changes, A.7 for carrier work or extraction that has not yet constituted a receiving episteme, and A.6.3.CSC when a narrower-use coarsened receiving episteme is primary.

## A.6.3.RT:2 - Problem {#problem}

Without a dedicated representation-scheme-transition pattern:

1. teams treat text-to-table, table-to-diagram, and notation shifts as harmless formatting;
2. changes in reasoning medium and recoverability remain implicit;
3. a visible edge, row, geometry, or decoder output silently imports claims that the source did not make;
4. latent or distributed representations tempt users to treat feature geometry as ontology-by-default;
5. users cannot tell when the case has become retargeting, explanation, narrative ordering, carrier work, bridge use, or controlled coarsening; and
6. exact endpoint, occurrence, Work, publication, and assurance records are demanded before an ordinary useful target representation exists.

## A.6.3.RT:3 - Forces {#forces}

- **Same concern, different reasoning medium.** Teams need representations suited to different tasks without silently changing what the claims concern.
- **Legibility vs recoverability.** A clearer target helps only if users can recover the source content and distinctions needed by the declared use.
- **Useful foregrounding vs unsupported strengthening.** Tables, diagrams, notation, and interactive views can expose structure while also making added links look source-given.
- **Representation change vs ontology change.** New notation or geometry can make structure visible; visibility does not establish world-side structure or a new EntityOfConcern.
- **Progressive exactness.** Ordinary conversions should stay easy, while externally relied-on or decode-mediated cases retain exact identity, source dependencies, loss, and evidence discipline.
- **Recoverability before decode ambition.** Directly inspectable cases establish the normal entry; latent cases need explicit decoding access and evidence for their use.

## A.6.3.RT:4 - Solution — preserve practical content across a representation change {#solution-preserve-practical-content-across-a-representation}

### A.6.3.RT:4.1 - Ordinary representation move {#ordinary-representation-move}

Produce the useful target first:

1. Name the user action the new representation should help: compare, inspect, traverse, calculate, communicate or replay. Identify the user's familiarity with the notation when that changes what they can do with it.
2. Point to the source material. Recover the givens, constraints and partial construction, including the claims, commitments, uncertainty and source references that must survive. Keep unknowns identifiable as unknowns.
3. Choose an available scheme and a target representation suited to that action. Identify the formation and interpretation rules needed for this use; a familiar notation can be named without reproducing its grammar.
4. Make the smallest target that supports the action. Arrange its parts so they can be used together: for example, keep a shared element recognizable in two groupings, or align a sequence of signs with a temporal reference. Explain any meaning-bearing mark, position or timing whose interpretation is not already clear from the selected conventions. A.6.3.RT.OE develops this construction when the expression's parts must be prepared for the intended operation.
5. Compare target and source. Mark what is preserved and foregrounded; what is rearranged, omitted or harder to recover; and which visible links or interpretations were added by the representation.
6. Try the intended operation when a short trial can decide whether the expression is useful. Apply the relevant mathematical, physical or other subject Method. Use the result to judge or repair the expression.
7. State the representation and reasoning-medium delta only as far as it changes use or blocks a likely overread.
8. Close with admissible use, non-admissible use, and a concrete return trigger and destination.

The first result is the expression and its representation note. If working with the expression establishes a new claim, its construction or argument supplies the source for representing that claim. Do not describe the new conclusion as content preserved from the original givens; sharing an EntityOfConcern does not establish that preservation.

Choose another available scheme when the current one cannot express a needed distinction. If new signs or rules are needed, develop the scheme through notation-design work. The scheme's description can use A.6.0 for a reusable vocabulary, laws and applicability, and A.6.1 for declared operations when those are needed. Those declarations describe the designed rules. RT uses the selected rules to construct particular expressions.

Use this compact note for ordinary work:

| Representation note entry | Practical question |
| --- | --- |
| User action | What should the target make easier? |
| Source material | What will the user return to? |
| Content to survive | Which claims, relations, commitments, uncertainty, or pins matter? |
| Target and reason | Which representation is chosen, and why does it help? |
| Preserved/foregrounded | What remains recoverable, and what becomes easier to see? |
| Rearranged/lost/added | What is omitted or weakened, and which apparent relation is not source-given? |
| Use boundary | What may and may not be done with the target? |
| Return | Which condition sends the user back to the source or to a stronger claim's direct pattern? |

### A.6.3.RT:4.1.a - Exact episteme-construction branch {#exact-episteme-construction-branch}

Open this branch only when the receiving use makes exact claim identity material: the target must travel independently, be cited or disputed, cross a scheme boundary for consequential use, be considered for admission as receiving episteme `Y` in a generated or decode-mediated case, or meet an exact-identity requirement from a named public, evidence, or assurance receiver.

Then establish exact A.6.3 construction `v : X -> Y`:

1. identify source episteme `X` and receiving episteme `Y` independently under C.2.1 by claim content, exact EntityOfConcern, and effective `U.ReferenceScheme`;
2. require the same exact EntityOfConcern; a changed concern requires A.6.4;
3. state how claims in `X` and any named additional source epistemes construct the claims in `Y`;
4. state the relation between endpoint schemes, preserved and foregrounded content, admitted loss or recoverability, prohibited strengthening, applicability, use, and return; and
5. cite every exact correspondence relation on which `v` actually depends. Scheme difference, similar content, adjacency, or a visible edge proves none.

A source model, graph, publication occurrence, form, carrier, table, or display does not substitute for `X`; a target table, diagram, notation, page, or file does not substitute for `Y`. If the target has no recoverable claim content, exact EntityOfConcern, or effective reference scheme, keep it as a useful rendering or candidate carrier and do not assert exact RT yet.

An exact `v` performs no Work and is not a relation occurrence. A system may perform representation-transformation Work under A.15.1; methods, source-use relations, A.6.1 bindings, and any A.15.PROD inception claim remain separate. E.17.0 independently decides viewpoint conformance and dependent `U.View` membership. E.24.PUB independently identifies publication occurrence, form, carrier, audience, and bounded use. Completing the exact construction does not itself authorize reliance.

### A.6.3.RT:4.1.b - Later-specific six-participant occurrence {#later-specific-six-participant-occurrence}

Use `RepresentationSchemeTransitionRelation@Context` only when the actual transition occurrence is itself needed and all six exact participants plus actual Work are present. The suffix `@Context` retrieves one independently selected A.1.1 `BoundedModelUseStructure : U.Structure`; it introduces no generic context kind or description-context field.

```text
RepresentationSchemeTransitionRelation@Context <: U.Relation:
  TransitionModelUseStructureSlot = <TransitionModelUseStructureSlot, U.Structure, U.StructureRef constrained to one exact BoundedModelUseStructure>
  PreservedEntityOfConcernSlot = <PreservedEntityOfConcernSlot, U.Entity, U.EntityRef>
  SourceRepresentationEpistemeSlot = <SourceRepresentationEpistemeSlot, U.Episteme, U.EpistemeRef>
  ReceivingRepresentationEpistemeSlot = <ReceivingRepresentationEpistemeSlot, U.Episteme, U.EpistemeRef>
  SourceRepresentationSchemeDescriptionSlot = <SourceRepresentationSchemeDescriptionSlot, U.Episteme, U.EpistemeRef>
  ReceivingRepresentationSchemeDescriptionSlot = <ReceivingRepresentationSchemeDescriptionSlot, U.Episteme, U.EpistemeRef>
  direction = SourceRepresentationEpistemeSlot -> ReceivingRepresentationEpistemeSlot
```

The six SlotSpecs and direction are the exact `RelationSignature`. `X` and `Y` have the same exact EntityOfConcern and their own effective schemes. Each scheme-description episteme is independently constituted: its claims describe one exact endpoint scheme, its EntityOfConcern is that scheme, and its own effective reference scheme makes the description interpretable. A scheme label or visible notation fills no scheme-description slot.

A positive occurrence obtains only when all of the following hold together:

1. all six participants resolve exactly, and the `BoundedModelUseStructure` was independently selected because its model-use organization changes this transition use;
2. A.13 identifies the actual performer, and A.15.1 independently admits the dated representation-transformation Work. If the current use also needs to say exactly which assignment covered that Work, F.6 checks that separate relation against the same A.13 assignment; F.6 identifies neither performer nor assignment, and a missing or failed attribution leaves the Work intact. The Work uses all six participant values collectively through its governed inputs, result, references, A.6.1 bindings, or a combination of these;
3. exact `v : X -> Y` states claim construction, endpoint-scheme relation, same EntityOfConcern, preservation, loss or recoverability, prohibited strengthening, applicability, use, and return; and
4. every depended-on correspondence is an exact separately governed relation or claim.

Work, performer, assignment, method, operation application, source-use relations, and any inception claim are not seventh participants or identity discriminators. Work alone proves neither `v` nor the occurrence. Conversely, an inspectable `v` without the selected model-use structure and exact Work remains an ordinary exact construction.

The occurrence is participant-determined by the complete six-participant tuple. Changing any participant identifies another occurrence. A repeat Work episode, evidence change, publication, form, carrier, layout, transition-description edition, or C.29 output does not reidentify an unchanged tuple. A changed C.2.1 discriminator of `X` or `Y` first identifies another episteme and therefore another tuple.

### A.6.3.RT:4.1.c - Transition description and source-relation epistemes {#transition-description-and-source-relation-epistemes}

Describe the occurrence durably only after it obtains and a receiving use needs that description. The transition-description episteme is identified under C.2.1 by claim content about the exact six-participant occurrence, that occurrence as EntityOfConcern, and its own effective `U.ReferenceScheme`. Editing its claim graph creates another description episteme without changing the occurrence.

Its claim content may make these values recoverable; they are not extra participants or identity fields:

| Description content | Meaning |
| --- | --- |
| `transitionRelationRef` | The exact six-participant occurrence. |
| `viewingConstructionRefOrStatement` | Exact `v : X -> Y`, including claim construction, endpoint-scheme relation, same exact EntityOfConcern, preservation, loss/recoverability, prohibited strengthening, applicability, use, and return. |
| `representationTransformationWorkRef` | Exact A.15.1 Work already used in the obtaining test; actual performer, assignment, Method, A.6.1 bindings, and any A.15.PROD inception claim remain separate. |
| `sourceRelationReferenceEpistemeRefs[]` | C.2.1 epistemes about exact source relations actually used; each relation still needs its own obtaining basis. |
| `preservedClaimRefs[]` | Exact source claims carried into `Y` for this use. |
| `preservedCommitmentRefs[]?` | Exact commitments preserved when a commitment is current. |
| `representationSchemeDeltaDescriptionRef` | What differs between the source and receiving schemes described by the participating scheme-description epistemes. |
| `reasoningMediumDeltaDescriptionRef?` | Changed inspection, comparison, inference, or replay affordance when material. |
| `representationLossDescriptionRef?` | Lost, narrowed, foregrounded, or rearranged distinctions. |
| `recoverabilityDescriptionRef?` | How omitted content is recovered from exact `X` or source relations. |
| `admissibleUseDescriptionRef` | What `Y` supports now. |
| `nonAdmissibleDownstreamUseDescriptionRef` | Which stronger use has not been established. |
| `returnConditionDescriptionRef` | When the user returns to exact `X` or its source relations. |

At least one of loss and recoverability is explicit; both are explicit when distinctions are lost and a recovery route is claimed.

When `v` cites a claim about one exact source relation, identify any reference-bearing episteme independently by its own C.2.1 triple: claims designating that relation and stating its exact kind, signature, defining pattern, and use in `v`; the source relation as EntityOfConcern; and its effective scheme. The episteme is not the relation, and citation does not make the relation obtain.

Publication may expose `X`, `Y`, the occurrence, or its description; forms, carriers, C.29 representations, and publication occurrences substitute for none of them.

### A.6.3.RT:4.2 - Progressive use and local vocabulary {#progressive-use-and-local-vocabulary}

Use three levels, without copying one level's burden into another:

- **Ordinary target:** target representation plus compact note.
- **Exact construction:** add `X`, `Y`, `v`, endpoint schemes, exact source dependencies, and claim-level loss/return when the receiving use triggers them.
- **Actual transition occurrence:** add the six-participant relation, Work, and optional occurrence-description episteme only when that historical relation is itself material.

Use detailed vocabulary only when it changes the next representation decision or blocks a concrete overclaim:

- **semiotic mode** — the meaning-bearing relation doing the main work, such as structural likeness, trace, conventional code, model-mediated correspondence, or decode-mediated recovery;
- **factor delta** — the representation-factor change material to review;
- **source dependencies of `v`** — the identified source claims and relations on which the construction depends, including which are needed jointly for each part of it and any required precedence between those parts. This dependency structure can branch or join;
- **source-return references** — links or other locators used to reopen source material for omitted detail or a changed question;
- **decode-mediated case** — a case whose receiving interpretation depends on a declared decoding or access relation;
- **actionability shift** — an apparent change in what users think they can do, which is not work authority, gate status, or permission; and
- **recoverability evidence** — evidence that omitted content can be recovered well enough for the declared use.

State the actual use, loss, evidence, and return once. Use A.10 or B.3 only when a specific evidence or assurance claim is current.

### A.6.3.RT:4.3 - Direct and correspondence-mediated constructions {#direct-and-correspondence-mediated-constructions}

In a **direct** exact construction, `Y` is constructed from `X` and fixed declared configuration. State the claim construction, endpoint-scheme relation, same exact EntityOfConcern, preservation, loss/recoverability, prohibited strengthening, applicability, use, and return; no generic correspondence object is required.

In a **correspondence-mediated** exact construction, `Y` depends on additional source epistemes or governed relations among their claim-bearing contents. Recover each needed direct relation and, when `v` cites a claim about it, the exact C.2.1 assertion episteme. A correspondence table, model, graph edge, or scheme difference is neither the relation nor proof that it obtains.

Both profiles retain the same exact EntityOfConcern. A correspondence by itself establishes neither an F.9 Bridge nor any substitution, comparative-review, evidence, or publication claim. Add C.29 only for a current mathematical modeling or reasoning use.

### A.6.3.RT:4.4 - Recurring moves and useful deltas {#recurring-moves-and-useful-deltas}

Recurring move shapes include tabulation, diagramming, structured-notation shift, and a same-EntityOfConcern correspondence-mediated representation shift.

In ordinary language, say what changed and why it helps: “the table foregrounds row comparison”, “the diagram foregrounds dependency shape”, or “the notation foregrounds explicit argument positions”. Add salience, topology, actionability, calibration, interactivity, or semiotic-mode detail only when it materially changes use or misuse risk.

### A.6.3.RT:4.5 - Preservation, loss, decode, and composition {#preservation-loss-decode-and-composition}

#### A.6.3.RT:4.5.a - Preservation and conservativity {#preservation-and-conservativity}

The ordinary move preserves the practical content named for the use. The exact branch preserves the same exact EntityOfConcern across independently constituted `X` and `Y` while changing scheme and often reasoning medium.

Check for unsupported strengthening when a target:

- upgrades a source-visible relation into dependency theory or another relation not present in the source;
- turns geometry, notation, embedding proximity, or decoder output into ontology-by-default;
- adds a Bridge, substitution, comparative, mechanism, temporal, or control claim that the source does not state and that has not been independently established under its governing pattern;
- collapses source alternatives, uncertainty, or bounded scope into one wider commitment; or
- treats decode-mediated recovery as direct givenness.

Check each target-side connective against the source or exact same-EntityOfConcern correspondence. A clearer, more structured, or more formal target does not establish a broader reliability claim.

#### A.6.3.RT:4.5.b - Loss and recoverability {#loss-and-recoverability}

State which distinctions, inspection possibilities, uncertainty cues, or local qualifiers are lost, foregrounded, rearranged, or harder to recover. The target may remain useful under a reliability claim bounded by the source or with an explicitly narrowed admissible use. If it remains honest only through a declared narrower use and source return, A.6.3.CSC is primary.

#### A.6.3.RT:4.5.c - Decode-mediated entry {#decode-mediated-entry}

A latent or decode-mediated case stays bounded until it has source material for the same concern, a decoding or access relation, recoverability evidence for the intended use, admissible and non-admissible use, remaining user action, and source return. When exact reliance is claimed, recover exact source episteme `X`, receiving episteme `Y`, construction `v`, and the source dependencies of `v` defined in §4.2.

A latent region, activation pattern, embedding, probe result, decoded rendering, publication form, or carrier may help locate the case but fills no episteme endpoint. Missing recovery evidence keeps the result exploratory, report-only, or blocked.

#### A.6.3.RT:4.5.d - Composition and reopen rule {#composition-and-reopen-rule}

Repeated same-regime normalization may be idempotent; heterogeneous representation shifts are generally order-sensitive. For an ordered sequence of representation shifts, compare the source and target of each shift and carry forward the loss from earlier shifts. Keep the source and target, content under test, scheme delta, preserved and withdrawn commitments, loss/recovery, and remaining action recoverable at every step.

Reopen the affected account when source content, endpoint identity, recovery assumptions, pins or provenance, correspondence or counter-witness disposition, primary semiotic mode, intended publication or receiving use, or accumulated loss changes. A changed EntityOfConcern requires A.6.4; a changed target-side claim uses the pattern that defines that exact claim.

### A.6.3.RT:4.6 - Boundary triggers {#boundary-triggers}

| What became primary | Required move |
| --- | --- |
| Same-regime wording only | Use A.6.3.CR. |
| Reader-useful ordering into a narrative path | Use A.6.3.NAR; keep RT only for a remaining material scheme shift. |
| Explanation adequacy of an existing face | Use E.17.EFP. |
| Receiving episteme has an independently identified different exact EntityOfConcern | Use A.6.4 for the retargeting arrow, its separate C.2.1 bounded-use assertion, and the current-case judgement `satisfies`, `fails`, or `cannot decide`. |
| Changed kind, ontology frame, predicate set, mathematical domain, or notation without an established EntityOfConcern change | Repeat the C.2.1 identity test and use the exact ontology pattern for any changed claim. Stay in RT when the same EntityOfConcern remains current and representation is the primary change. |
| Same-signal time/frequency or another mathematical representation change | Stay in RT when the same EntityOfConcern remains current and representation is the primary change. Add C.29 only when the use depends on a contested or claim-bearing mathematical lens. A.6.4 opens only after C.2.1 independently identifies a different receiving entity. |
| Carrier rendering, export or serialization of a chosen representation; OCR or parsing that extracts carrier content without yet constituting a receiving episteme | Use A.7 or the corresponding carrier/extraction pattern. |
| A narrower-use coarsened receiving episteme | Use A.6.3.CSC with explicit loss and source return. |
| Cross-context equivalence, substitution, or Bridge use | Keep RT for the representation delta. Use F.9 to test a Bridge between two exact F.17 `SchemeSenseCell` values from different semantic contexts; cite the Bridge only if it obtains, and keep any C.2.1 bounded-use claim separate. |
| Bounded comparison over already available source epistemes | Use E.17.ID.CR; keep RT only for a remaining material representation change. |
| Problem formulation or abductive prompt, candidate, or selection | Use B.5.2.0 for the prompt and B.5.2 for the abductive loop. |
| Performed Work, a work plan, or authority to act | Use the applicable A.15 pattern for performed Work or a work plan. For an authority-looking claim, select the matching A.6 `A6-AW-*` row and its direct subject pattern. An RT note or construction supplies neither the Work nor the plan and grants no authority to act. |
| Evidence or assurance force | Keep RT for preservation/loss and use A.10 or B.3 for that exact claim. |
| Temporal or dynamics claim | Use C.27 or A.3.3 for the claim actually made. |
| Transformation-flow graph/path, step-validity, or gate-decision claim | Use E.18, A.20, or A.21 respectively. |
| A contested mathematical lens | Keep RT for the representation transition and use C.29 only for adequacy of that lens. |

## A.6.3.RT:7 - Conformance and counterexample replay {#conformance-and-counterexample-replay}

### A.6.3.RT:7.1 - Ordinary and exact checks {#ordinary-and-exact-checks}

1. @fact:CC-RT-1 **CC-RT-1 — Useful ordinary entry.** A user can recover the source content, choose an available scheme, make a target suited to the next action, and compare it with the source before supplying exact endpoint identities. Givens, unknowns and a partial construction can support this first result. @status:spec/done
2. @fact:CC-RT-2 **CC-RT-2 — Same concern and right family.** The target still concerns the same thing; representation scheme or reasoning medium is the primary change rather than wording, narrative, explanation, carrier work, retargeting, bridge use, or controlled coarsening. @status:spec/done
3. @fact:CC-RT-3 **CC-RT-3 — Delta and source comparison.** Preserved and foregrounded content, rearrangement, loss, recoverability, and apparent links not licensed by the source are visible. @status:spec/done
4. @fact:CC-RT-4 **CC-RT-4 — Use and return.** Admissible and non-admissible use plus a practical source-return trigger are clear. @status:spec/done
5. @fact:CC-RT-5 **CC-RT-5 — Progressive burden.** Detailed factors, semiotic mode, decode evidence, exact identities, Work, publication, evidence, and assurance appear only when each changes use or blocks a likely error. @status:spec/done
6. @fact:CC-RT-6 **CC-RT-6 — Exact endpoints when triggered.** `X` and `Y` are independently constituted C.2.1 epistemes with the same exact EntityOfConcern and recoverable effective schemes; forms, carriers, models, displays, and readable output substitute for neither. @status:spec/done
7. @fact:CC-RT-7 **CC-RT-7 — Exact construction.** `v : X -> Y` states claim construction, endpoint-scheme relation, same exact EntityOfConcern, preservation, loss/recovery, prohibited strengthening, applicability, use, and return. @status:spec/done
8. @fact:CC-RT-8 **CC-RT-8 — Exact dependencies and neighbors.** Correspondence dependencies obtain independently; C.29 representation, E.17.0 View membership, grounding, publication, evidence, assurance, bridge, gate, and receiving Work remain separate. @status:spec/done
9. @fact:CC-RT-9 **CC-RT-9 — Later-specific occurrence only at its trigger.** A positive `RepresentationSchemeTransitionRelation@Context` has the exact A.1.1 model-use structure, preserved concern, `X`, `Y`, two exact scheme-description epistemes, and actual Work satisfying §4.1.b. @status:spec/done
10. @fact:CC-RT-10 **CC-RT-10 — Occurrence, Work, and description stay distinct.** The participant tuple identifies the occurrence; Work and production claims remain separate; the transition-description episteme has the occurrence as EntityOfConcern and its own C.2.1 identity. @status:spec/done
11. @fact:CC-RT-11 **CC-RT-11 — Occurrence identity.** Only a changed participant reidentifies the occurrence; repeat Work, evidence, publication, layout, carrier, description edition, or C.29 output does not. @status:spec/done
12. @fact:CC-RT-12 **CC-RT-12 — Reuse is local.** When the source or target, delta, dependency, loss, use, evidence, or return changes, reopen only the affected part of the account. @status:spec/done
13. @fact:CC-RT-13 **CC-RT-13 — Construction and subject result.** The expression uses identified rules and supports the named operation. A trial is required only when it can decide usefulness. A new subject conclusion keeps its construction or argument as its source; notation-scheme design and the subject Method remain distinct from making the expression. @status:spec/done

### A.6.3.RT:7.2 - Counterexample replay {#counterexample-replay}

| Case | Required result |
| --- | --- |
| Ordinary entry | A service note can become a useful comparison table and loss note without first inventing `X`, `Y`, `v`, Work, publication, or assurance records. |
| Constructive use | Givens and an intermediate geometric construction can become a diagram used in an argument. RT compares the diagram with those inputs; geometry establishes any new conclusion. |
| Scheme limit | If the selected conventions cannot express a required distinction, choose another scheme or design the missing rules before claiming a usable expression under them. |
| Preserve vs retarget | Exact RT requires equal EntityOfConcern; a changed concern requires A.6.4 even when labels overlap. |
| Same scheme | If scheme and reasoning medium are unchanged and only wording changes, use A.6.3.CR. |
| Different scheme | Scheme difference alone establishes neither `v`, correspondence, Work, Bridge, nor the six-participant occurrence. |
| Candidate vs `U.View` | A valid receiving episteme and RT construction may fail E.17.0 conformance and remain a non-View candidate. |
| Publication/form/carrier | Availability, form change, or carrier replacement substitutes for no endpoint and reidentifies no unchanged construction or occurrence. |
| Work without conservativity | A system may produce `Y`, yet unsupported strengthening or hidden loss blocks the exact construction and occurrence. |
| Grounded source, ungrounded receiver | Grounding of `X` does not transfer through `v`; `Y` has an `EpistemeEmpiricalGroundingRelation` only when its own covered claims and conditions make one obtain. |
| Readable decode without recovery basis | Keep a fluent decoded output exploratory, report-only, or blocked until the same-concern source, a declared decoding or access relation, recoverability evidence for the intended use, admissible and non-admissible use, remaining user action, and return are present. Readability, probe score, feature geometry, or publication form fills no episteme endpoint. |
| Selected structure overread | The exact `BoundedModelUseStructure` is one participant only in the triggered occurrence; it is not transformer, viewpoint, `U.View`, representation, publication, or EntityOfConcern. |
| Cross-scheme dependency | Scheme difference, similar content, a description, or C.29 output cannot replace an exact transition. When the dependency crosses semantic contexts, none of those cues can replace the obtaining F.9 Bridge and separate bounded-use claim. |
| Description or C.29 output | Editing the transition description or mathematical output does not change the occurrence unless an exact participant changes. |

## A.6.3.RT:9 - Consequences {#consequences}

- Ordinary users can obtain a useful target representation without a six-participant record.
- Representation and reasoning-medium changes become explicit rather than rhetorical.
- Exact same-EntityOfConcern, scheme, source dependencies, loss, and occurrence identity remain available for consequential use.
- Recoverability and decode dependence become reviewable instead of hiding behind cleaner output.
- Work, View membership, publication, evidence, assurance, bridge, and ontology claims remain separate.

Costs and trade-offs:

- Authors must compare source and target instead of judging only appearance.
- Reliance-facing use adds exact identity and evidence work proportionate to the receiver.
- Some attractive targets remain orientation-only or exploratory because source return or recovery is weak.

## A.6.3.RT:12 - Relations {#relations}

- **Builds on:** `A.6.3` and `A.6.2` for effect-free source-to-receiving construction; C.2.1 for exact endpoint and description identity; A.1.1 for the later-specific model-use structure; A.13 for actual-performer identification; A.15.1 for independent dated-Work admission; F.6 only for current precise assignment-bound attribution; C.2.7 and E.10.D2 when representation factors or semiotic mode are material.
- **Operative-expression construction:** A.6.3.RT.OE prepares an expression under available conventions so the next operation can be performed. Use its result in the ordinary representation move of :4.1.
- **Coordinates with:** A.6.3.CR, A.6.3.NAR, A.6.3.CSC, E.17.EFP, E.17.ID.CR, A.6.4, A.7, F.9, B.5.2.0, B.5.2, A.15, E.18, A.20, A.21, A.10, B.3, C.27, A.3.3, C.26, and C.29 at the specific boundaries named above.
- **Keeps separate:** actual Work and method; E.17.0 View membership; E.24.PUB publication occurrence, form, carrier, audience, and use; grounding; bridge; evidence; assurance; gate; temporal, dynamics, and transformation-flow claims.
- **Boundary:** RT contributes preservation, representation/reasoning delta, loss/recovery, use, and return. It does not let a table, diagram, notation, model display, decoded output, publication, form, or carrier substitute for an exact episteme or authorize a stronger claim.


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/A-6-3#root, spec://ai.lev/fpf-spec/contract/A-6-2#root, spec://ai.lev/fpf-spec/contract/C-2-1#root; later occurrence uses spec://ai.lev/fpf-spec/contract/A-1-1#root and spec://ai.lev/fpf-spec/contract/A-15-1#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/A-6-3-CR#root, spec://ai.lev/fpf-spec/contract/A-6-3-NAR#root, spec://ai.lev/fpf-spec/contract/A-6-3-CSC#root, spec://ai.lev/fpf-spec/contract/E-17-EFP#root, spec://ai.lev/fpf-spec/contract/E-17-ID-CR#root, spec://ai.lev/fpf-spec/contract/A-6-4#root, spec://ai.lev/fpf-spec/contract/A-7#root, spec://ai.lev/fpf-spec/contract/F-9#root, spec://ai.lev/fpf-spec/contract/A-15#root, spec://ai.lev/fpf-spec/contract/E-17-0#root, spec://ai.lev/fpf-spec/contract/E-24-PUB#root, spec://ai.lev/fpf-spec/contract/A-10#root, spec://ai.lev/fpf-spec/contract/B-3#root, spec://ai.lev/fpf-spec/contract/C-26#root, spec://ai.lev/fpf-spec/contract/C-29#root, spec://ai.lev/fpf-spec/contract/E-18#root, spec://ai.lev/fpf-spec/contract/A-20#root, spec://ai.lev/fpf-spec/contract/A-21#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-3-3-CC#root, spec://ai.lev/fpf-spec/contract/A-6-3#root, spec://ai.lev/fpf-spec/contract/A-6-3-CR#root, spec://ai.lev/fpf-spec/contract/A-6-3-CSC#root, spec://ai.lev/fpf-spec/contract/A-6-3-NAR#root, spec://ai.lev/fpf-spec/contract/A-6-3-RT-OE#root, spec://ai.lev/fpf-spec/contract/A-6-4#root, spec://ai.lev/fpf-spec/contract/A-6-9#root, spec://ai.lev/fpf-spec/contract/A-6-P-RI#root, spec://ai.lev/fpf-spec/contract/B-5-FM#root, spec://ai.lev/fpf-spec/contract/B-5-MPC#root, spec://ai.lev/fpf-spec/contract/B-5-MPC-R#root, spec://ai.lev/fpf-spec/contract/B-5-RC#root, spec://ai.lev/fpf-spec/contract/B-5-TU#root, spec://ai.lev/fpf-spec/contract/C-22-2#root, spec://ai.lev/fpf-spec/contract/C-26#root, spec://ai.lev/fpf-spec/contract/C-29#root, spec://ai.lev/fpf-spec/contract/C-29-1#root, spec://ai.lev/fpf-spec/contract/C-29-2#root, spec://ai.lev/fpf-spec/contract/C-37#root, spec://ai.lev/fpf-spec/contract/E-17-EFP#root, spec://ai.lev/fpf-eng-me/contract/ME-22#root, spec://ai.lev/fpf-think-not/contract/NOT-2#root, spec://ai.lev/fpf-eng-sie/contract/SIE-7#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/A-6-3-RT
