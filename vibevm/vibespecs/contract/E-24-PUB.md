# E.24.PUB - Episteme Publication: Availability, Form and Carrier {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Part E FPF authoring discipline pattern
> **Status:** Stable
> **Normativity:** Normative unless a section is explicitly informative

## E.24.PUB:0 - Use This When {#use-this-when}

Use this pattern when an ontic or another entity is encountered through a card, table, diagram, file, pattern host, dashboard, or similar published expression and the current work depends on knowing what was described, what was made available, and what merely carries the expression.

**Primary working reader.** A practitioner or FPF author deciding whether a visible thing is a claim-bearing episteme, a `U.View`, a publication form, a C.29 representation, a `U.PresentationCarrier`, or evidence of one publication occurrence.

**First useful move.** Put the intended receiving use in the bounded-use declaration itself. Then say, in one sentence, which episteme edition is available, to which declared audience, for which bounded use, in which publication form, and on which presentation carrier. Cite a separate plan, decision question, or `U.WorkPlan` only when it independently exists and changes the publication claim; it is not a second required statement of intended use. Availability establishes none of actual access, reliance, use, Work, or result. When a precise performed-Work claim is independently current, recover each exact actual performer through A.13 and let A.15.1 independently admit the dated Work; add F.6 only when that claim or its receiving use expressly consumes precise assignment-bound attribution through the same obtaining A.13 assignment. F.6 identifies neither assignment nor performer, and missing or failed F.6 leaves the Work intact. Follow A.6.1 for an operation binding, C.11 for a `ChoiceResult`, or the exact access, reliance, or use relation without reproducing its test here. Open the heavier publication-relation declarations only when the receiving use depends on availability, its declared boundary, or publication-occurrence identity.

**What goes wrong if missed.** A visible layout is treated as the described subject, a file is treated as the claims it carries, a diagram is treated as a view merely because it is graphical, or a currently available episteme is turned into a durable `U.EpistemePublication` kind. The receiving work then cannot tell which object changed when claims, layout, carrier, audience, or use changes.

**What this buys.** The user can change a claim, view, form, carrier, audience, or declared bounded use without silently changing all the others. A publication can be inspected and repaired while the subject pattern remains centered on its subject.

**Not this pattern when.**

- Use `C.2.1` when the question is the identity or content of the episteme itself.
- Use `E.17.0` when the question is whether an exact episteme conforms to an exact viewpoint episteme and therefore has `U.View` membership. Use `A.6.3` separately when source-to-receiving viewing construction is current.
- Use `C.29` when representation elements and the operations admitted by a representation are current.
- Use `E.24.CD`, then `E.24`, when a durable ontic is still being considered.
- Use `E.24.UK` when a public `U.*` kind or dependent-kind disposition is unsettled.
- Use the subject pattern directly when publication does not affect the receiving use.

## E.24.PUB:1 - Problem Frame {#problem-frame}

Ontics and other entities are usually encountered through epistemes and physical or digital carriers. One completed inspection card can carry claims and therefore be a `U.Episteme`; its reusable arrangement can be used as a publication form; selected graphical elements can participate in a C.29 representation; a file, screen, sheet, or volume can be a `U.PresentationCarrier`; and one publication occurrence can make the selected card-episteme edition available to a declared audience for a bounded use.

Those are connected uses, not one presentation-side kind. E.24.PUB governs the publication relation and the two supporting relations needed to inspect that use. It keeps the described subject, description episteme, `U.View`, representation, publication form, carrier, and publication occurrence distinct without requiring every ordinary sentence to repeat the full stack.

Plain `published episteme` names an episteme while it participates as the selected edition in a current publication occurrence. It is a contingent qualification, not a durable U-kind and not a second identity beside `U.Episteme`.

Here a publication occurrence is an occurrence of `EpistemePublicationRelation`: an availability relation that can endure. It is not the instantaneous rendering, printing, uploading, or access-control work that may establish or restore that availability.

## E.24.PUB:2 - Problem {#problem}

The practical problem is change localization. When a reader sees only “the diagram was updated” or “the model was published”, five materially different changes are hidden:

1. the selected episteme edition may have changed because its claim content, EntityOfConcern, or effective reference scheme changed;
2. another episteme edition may have been constructed, or the exact episteme may conform to a different viewpoint edition;
3. the publication form or C.29 representation may have changed while the claims stayed the same;
4. the presentation carrier or its availability may have changed;
5. the declared audience or bounded use may have changed while the same edition, form, and carrier remained.

Without the distinction, the receiving use cannot identify the smallest object or relation to inspect, revise, republish, or stop relying on.

## E.24.PUB:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Readable first use vs exact relation identity | Most users need one sentence; contested availability needs exact participants, obtaining, and occurrence identity. |
| One encountered thing vs several governed uses | A card or diagram can participate in several relations, but visible shape decides none of their kinds. |
| Stable episteme vs changing publication | The same episteme edition may be republished through another form or carrier, while a changed claim discriminator identifies another episteme. |
| Audience reach vs actual use | Making an edition available does not prove that any system read it, relied on it, or performed work from it. |
| Subject-first explanation vs semio-bias | Publication distinctions protect reasoning about the subject; they should not displace the subject from its subject pattern. |

## E.24.PUB:4 - Solution {#solution}

Start with this readable publication statement:

> Publication occurrence `<P>` makes episteme edition `<E>` available to the audience identified by `<A>` for the use bounded by `<U>`, through publication form `<F>` borne by presentation carrier `<C>`.

The sentence names the five participant meanings without asking the user to fill a record. If it supplies the publication distinction needed by the receiving use, stop. If availability, identity, or a change is disputed, recover the three direct relations below.

### E.24.PUB:4.1 - Identify the publication occurrence {#identify-the-publication-occurrence}

`EpistemePublicationRelation` is the direct relation kind whose occurrence makes one selected episteme edition available to a declared audience for a declared bounded use.

Its actual participants are:

| Participant meaning | Admitted value | What the value supplies |
| --- | --- | --- |
| selected episteme edition | one exact `U.Episteme` identified under `C.2.1` | the claims made available |
| audience declaration | one `U.Episteme` whose claims identify the intended receiving entities or a C.3-governed local kind and its membership criterion | who is included; a reader label alone is insufficient when the boundary matters |
| bounded-use declaration | one `U.Episteme` whose claims state the operations or decisions supported, the conditions of that use, and the excluded stronger use | what availability is for; actual reliance remains another relation |
| publication form | one exact `U.Entity` used as the selected arrangement, notation, or rendering convention that expresses the edition for the bounded use | how the edition is expressed; visible shape alone does not establish this use |
| presentation carrier | one exact `U.PresentationCarrier` | what physically or digitally bears the selected form |

The use of common `U.Entity` for the publication-form participant does not admit a universal publication-form U-kind. `Publication form` is a relation-defined participant meaning here: the exact entity keeps the more specific kind and identity supplied by its direct pattern, and it fills `PublicationFormSlot` only while `PublicationFormExpressionRelation` obtains for the selected edition and bounded use. This is one predicate over a real common kind, not a prose union of cards, tables, diagrams, and files. E.8 governs FPF pattern form; E.17 governs multi-view publication forms and faces; a domain publication pattern may govern another form.

The reusable declaration is:

```text
EpistemePublicationRelationSignature:
  RelationKind: EpistemePublicationRelation
  SlotSpecs:
    SelectedEpistemeEditionSlot: ValueKind=U.Episteme, refMode=U.EpistemeRef, Required
    AudienceDeclarationSlot: ValueKind=U.Episteme, refMode=U.EpistemeRef, Required
    BoundedUseDeclarationSlot: ValueKind=U.Episteme, refMode=U.EpistemeRef, Required
    PublicationFormSlot: ValueKind=U.Entity, refMode=U.EntityRef, Required
    PresentationCarrierSlot: ValueKind=U.PresentationCarrier, refMode=U.EntityRef, Required
```

These SlotKinds name participant meanings only inside this `RelationSignature`. They do not create five new U-kinds, and a card field with a similar label does not become one of these SlotSpecs.

The audience-declaration episteme identifies the audience criterion; it is not the audience and does not prove access by any particular system. A concrete system's access, reading, reliance, or later work is another direct relation or work occurrence. This lets one publication be available to every entity satisfying a stable criterion without inventing `U.Audience` or treating a changing set of readers as changing participants of the same publication occurrence.

`EpistemePublicationRelation` obtains while all of the following are true:

1. `PublicationFormExpressionRelation` relates the selected edition, publication form, and bounded-use declaration;
2. `PublicationFormBearingRelation` relates the exact carrier and publication form;
3. entities admitted by the audience declaration can obtain the expressed edition from that carrier under the conditions stated by the bounded-use declaration;
4. the selected edition, declarations, form, and carrier remain the identified participants of this occurrence.

One occurrence is reidentified by those five fixed participants and their maximal continuous interval of availability. Changing any participant yields another publication occurrence. Demonstrated loss of availability followed by restoration yields a later occurrence. Missing or stale evidence leaves current obtaining unresolved; it does not prove a gap.

Rendering, printing, uploading, indexing, or granting access are activities separate from the publication occurrence. If one is independently claimed as dated Work, apply its direct Work and attribution patterns; E.24.PUB does not restate their admission, assignment, or compact-reporting rules. The activity and any result remain separate from the publication-relation participants.

### E.24.PUB:4.2 - Recover expression and bearing only when needed {#recover-expression-and-bearing-only-when-needed}

`PublicationFormExpressionRelation` relates one selected episteme edition, one exact publication form, and one bounded-use declaration. It obtains when the form expresses enough of that edition, under its effective reference scheme, for the declared use. One occurrence is reidentified by those three fixed participants and their maximal continuous interval of predicate truth. Omission, coarsening, changed notation, or changed admitted operations can end this relation even while the carrier remains unchanged. `A.6.3`, `C.29`, or `E.17` governs the more specific preservation, loss, view, or representation claim when that claim is current.

`PublicationFormBearingRelation` relates one exact `U.PresentationCarrier` and one exact publication form. It obtains while that carrier bears or renders that form as the same recoverable form. One occurrence is reidentified by the two fixed participants and their maximal continuous interval of bearing. Changing a filename or storage address does not by itself settle carrier identity; apply the carrier's direct identity and currentness pattern.

Their reusable declarations are:

```text
PublicationFormExpressionRelationSignature:
  RelationKind: PublicationFormExpressionRelation
  SlotSpecs:
    ExpressedEpistemeEditionSlot: ValueKind=U.Episteme, refMode=U.EpistemeRef, Required
    PublicationFormSlot: ValueKind=U.Entity, refMode=U.EntityRef, Required
    BoundedUseDeclarationSlot: ValueKind=U.Episteme, refMode=U.EpistemeRef, Required

PublicationFormBearingRelationSignature:
  RelationKind: PublicationFormBearingRelation
  SlotSpecs:
    PresentationCarrierSlot: ValueKind=U.PresentationCarrier, refMode=U.EntityRef, Required
    BornePublicationFormSlot: ValueKind=U.Entity, refMode=U.EntityRef, Required
```

These supporting relations prevent two shortcuts. A form does not make itself available, and a carrier does not express claims merely by storing bytes, ink, or another physical state. The publication occurrence depends on both relations but remains a distinct availability occurrence.

### E.24.PUB:4.3 - Use progressive explicitness {#use-progressive-explicitness}

Use the smallest statement that supports the current work:

1. **Ordinary use:** name the selected episteme edition, audience, bounded use, form, and carrier in one sentence.
2. **Changed-object use:** say which one of those objects changed and which relation must be re-evaluated.
3. **Contested availability:** state the `EpistemePublicationRelation` participants, obtaining evidence, and occurrence identity.
4. **Contested expression:** open `PublicationFormExpressionRelation` and the exact view, representation, preservation, or loss pattern.
5. **Contested carrier availability:** open `PublicationFormBearingRelation` plus the direct carrier-currentness or access pattern.

Do not materialize all five levels as a standing publication card. Stop as soon as the receiving use can distinguish the operative object and relation.

### E.24.PUB:4.4 - Classify the encountered form by current use {#classify-the-encountered-form-by-current-use}

Ask one question at a time:

| Current question | Governed object or relation |
| --- | --- |
| Does the filled card, diagram, or record carry identifiable claims about an EntityOfConcern under an effective reference scheme? | a `U.Episteme` under `C.2.1` |
| Does `EpistemeViewpointConformanceRelation(E,P)` obtain for that episteme E and at least one exact viewpoint episteme P? | the same E has dependent-kind membership as `U.View` under `E.17.0`; any A.6.3 construction remains a separate optional relation |
| Is an arrangement, notation, or rendering convention selected to express the edition for this bounded use? | the publication-form participant of `PublicationFormExpressionRelation` |
| Do selected elements correspond to independently recovered objects and change the admitted modeling or reasoning operations? | a C.29 representation and its correspondence |
| Does a physical or digital entity bear the form? | a `U.PresentationCarrier` in `PublicationFormBearingRelation` |
| Is the selected edition available to the declared audience for the declared use through that form and carrier? | one `EpistemePublicationRelation` occurrence |

The answers can be jointly positive because they concern different objects or relations. They do not follow from the words `card`, `record`, `table`, `schema`, `diagram`, `view`, `file`, or `publication` alone.

### E.24.PUB:4.5 - Keep direct verbs with their relations {#keep-direct-verbs-with-their-relations}

- an episteme carries claims and designations;
- a `U.View` is the same episteme individual for which E.17.0 conformance to at least one exact viewpoint episteme obtains;
- a publication form expresses a selected episteme edition for a bounded use;
- a C.29 representation stands in a declared correspondence to independently recovered objects;
- a presentation carrier bears a publication form;
- a publication occurrence makes one selected episteme edition available;
- a system may perform publication activity and may later access or rely on the published episteme, but those are separate claims under their direct patterns; publication availability establishes none of them;

A designator designates and a governed reference resolves to a referent. Neither operation publishes, bears, represents, or makes the subject-side predicate obtain.

### E.24.PUB:4.6 - Keep subject patterns subject-first {#keep-subject-patterns-subject-first}

In a pattern about an ontic, structure, architecture, characteristic space, method, or another subject, explain the subject's identity, relations, practical problem, and solution before publication details. Add E.24.PUB only when the receiving use depends on distinguishing the description, selected edition, form, carrier, audience, or bounded use.

When the EntityOfConcern is itself a description episteme, the same rule applies one level up. The description stays the subject; publication of that description is a neighboring relation.

## E.24.PUB:7 - Conformance Checklist {#conformance-checklist}

| Check | Observable conformance condition |
| --- | --- |
| `CC-E24PUB-1` | @fact:CC-E24PUB-1 The bounded-use declaration itself names the intended receiving use. A separate plan, decision question, or `U.WorkPlan` is cited only when it independently exists and changes the publication claim. The publication statement names the selected edition, audience, bounded use, form, and carrier; it establishes no actual access, reliance, use, Work, or result. Any independently current stronger claim is routed to its direct pattern without reproducing that pattern's test here. @status:spec/done |
| `CC-E24PUB-2` | @fact:CC-E24PUB-2 The selected episteme edition, audience declaration, bounded-use declaration, publication form, and presentation carrier are distinguishable. @status:spec/done |
| `CC-E24PUB-3` | @fact:CC-E24PUB-3 `EpistemePublicationRelation` has the five exact participant meanings, the availability predicate, and the maximal-continuous-occurrence identity rule stated in section 4.1. @status:spec/done |
| `CC-E24PUB-4` | @fact:CC-E24PUB-4 `PublicationFormExpressionRelation` and `PublicationFormBearingRelation` are recoverable when expression or carrier availability is load-bearing. @status:spec/done |
| `CC-E24PUB-5` | @fact:CC-E24PUB-5 Plain `published episteme` is used only for contingent participation; `U.EpistemePublication` is not used as a durable kind. @status:spec/done |
| `CC-E24PUB-6` | @fact:CC-E24PUB-6 A `U.View` remains a same-individual dependent specialization of `U.Episteme` under an obtaining E.17.0 conformance relation; graphical appearance and A.6.3 construction alone supply no membership. @status:spec/done |
| `CC-E24PUB-7` | @fact:CC-E24PUB-7 C.29 representation elements and correspondence remain distinct from the publication form and direct subject-side objects. @status:spec/done |
| `CC-E24PUB-8` | @fact:CC-E24PUB-8 Publication activity, actual access, reliance, evidence, decision, performed Work, operation binding, and result remain under their direct patterns. E.24.PUB checks only that publication availability is not used as proof of those stronger claims. @status:spec/done |
| `CC-E24PUB-9` | @fact:CC-E24PUB-9 A changed edition, form, carrier, audience, or bounded use leads to the smallest affected object or relation rather than a whole-stack rewrite. @status:spec/done |
| `CC-E24PUB-10` | @fact:CC-E24PUB-10 Ordinary use stops at the readable sentence when the receiving use needs no fuller relation detail. @status:spec/done |

## E.24.PUB:9 - Consequences {#consequences}

The main gain is local repair. A stale carrier can be replaced without pretending that the claims changed. A revised claim can create another episteme edition without pretending that the audience or form changed. A narrower audience or use can create another publication occurrence while preserving the edition.

The cost is that load-bearing publication claims need five identified participants and two supporting relations. Progressive explicitness contains that cost: ordinary users state one sentence; only disputed availability, expression, or bearing opens the complete relation detail.

## E.24.PUB:12 - Relations {#relations}

- **Builds on:** `A.6.REL` for direct obtaining and occurrence identity, `C.2.1` for the selected edition and declaration epistemes, and `E.24` for ontic-description boundaries.
- **Coordinates with:** `E.17.0` for `U.View` membership and `E.17` for multi-view publication; `A.6.3` for optional viewing construction; `C.29` for representation and admitted operations; `E.8` for FPF pattern publication form; and the direct carrier-currentness or access pattern when carrier availability is current.
- **Coordinates with:** `E.24.CD` for candidate detection and `E.24.UK` for public U-kind and dependent-kind settlement. `U.EpistemePublication` is rejected there; this pattern uses Plain `published episteme` for contingent participation.
- **Used by:** subject patterns only when a receiving use depends on distinguishing the subject, description episteme, selected edition, view, representation, publication form, carrier, audience, bounded use, or publication occurrence.


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/E-24#root, spec://ai.lev/fpf-spec/contract/C-2-1#root, spec://ai.lev/fpf-spec/contract/E-17#root, spec://ai.lev/fpf-spec/contract/E-8#root, spec://ai.lev/fpf-spec/contract/E-10#root, spec://ai.lev/fpf-spec/contract/F-19#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/E-24-CD#root, spec://ai.lev/fpf-spec/contract/C-30-AD#root, spec://ai.lev/fpf-spec/contract/E-21#root, spec://ai.lev/fpf-spec/contract/E-9-DA#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-1-1#root, spec://ai.lev/fpf-spec/contract/A-12#root, spec://ai.lev/fpf-spec/contract/A-15-3#root, spec://ai.lev/fpf-spec/contract/A-15-6#root, spec://ai.lev/fpf-spec/contract/A-15-PROD#root, spec://ai.lev/fpf-spec/contract/A-16-0#root, spec://ai.lev/fpf-spec/contract/A-3-2#root, spec://ai.lev/fpf-spec/contract/A-6-0#root, spec://ai.lev/fpf-spec/contract/A-6-3#root, spec://ai.lev/fpf-spec/contract/A-6-3-CSC#root, spec://ai.lev/fpf-spec/contract/A-6-3-NAR#root, spec://ai.lev/fpf-spec/contract/A-6-3-RT#root, spec://ai.lev/fpf-spec/contract/A-6-4#root, spec://ai.lev/fpf-spec/contract/A-6-F#root, spec://ai.lev/fpf-spec/contract/A-6-P#root, spec://ai.lev/fpf-spec/contract/B-3#root, spec://ai.lev/fpf-spec/contract/C-19#root, spec://ai.lev/fpf-spec/contract/C-2-1#root, spec://ai.lev/fpf-spec/contract/C-30-ASV#root, spec://ai.lev/fpf-spec/contract/C-32-ADA#root, spec://ai.lev/fpf-spec/contract/C-32-ADR#root, spec://ai.lev/fpf-spec/contract/C-32-FAIL#root, spec://ai.lev/fpf-spec/contract/C-32-P2S#root, spec://ai.lev/fpf-spec/contract/C-32-PAD#root, spec://ai.lev/fpf-spec/contract/C-37#root, spec://ai.lev/fpf-spec/contract/E-10#root, spec://ai.lev/fpf-spec/contract/E-10-ARCH#root, spec://ai.lev/fpf-spec/contract/E-11-DSG#root, spec://ai.lev/fpf-spec/contract/E-11-PFP#root, spec://ai.lev/fpf-spec/contract/E-15#root, spec://ai.lev/fpf-spec/contract/E-17#root, spec://ai.lev/fpf-spec/contract/E-17-0#root, spec://ai.lev/fpf-spec/contract/E-17-1#root, spec://ai.lev/fpf-spec/contract/E-17-2#root, spec://ai.lev/fpf-spec/contract/E-24#root, spec://ai.lev/fpf-spec/contract/E-24-CD#root, spec://ai.lev/fpf-spec/contract/E-24-UK#root, spec://ai.lev/fpf-spec/contract/E-4-PFAD#root, spec://ai.lev/fpf-spec/contract/E-4-PFIP#root, spec://ai.lev/fpf-spec/contract/F-17#root, spec://ai.lev/fpf-spec/contract/F-18#root, spec://ai.lev/fpf-spec/contract/F-9-1#root, spec://ai.lev/fpf-spec/contract/G-6#root, spec://ai.lev/fpf-eng-mdpe/contract/MDPE-5#root, spec://ai.lev/fpf-eng-me/contract/ME-9#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/E-24-PUB
