# A.6.REL - Relation Obtaining and Individuation: Distinguish Occurrences When Needed: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## A.6.REL:5 - Archetypal Grounding {#archetypal-grounding}

### A.6.REL:5.1 - Repeated occurrence of one direct system-role-assignment species {#repeated-occurrence-of-one-direct-system-role-assignment-species}

Start with `Robot-7 is assigned as inspector through InspectionAssignment-17` and trace only the objects needed by the current use.

1. **World-side participants and occurrence.** `Robot-7` remains an admitted `U.System`; `InspectorSystemRole` remains one exact local C.3 kind. `InspectionAssignment-17` is an occurrence of directly declared `MaintenanceInspectionAssignment <: U.SystemRoleAssignment`. `Robot-7` participates as the holder system and `InspectorSystemRole` as the assigned local system-role kind. Those two values are the complete participant set of this direct species.
2. **Direct settlement.** A.2.1 supplies the species' participant meanings, direct predicate, applicability, and same-versus-new-occurrence rule. The occurrence continues while that predicate obtains without interruption for the same complete participant set. A demonstrated predicate-false gap ends it; later resumption starts another occurrence. An evidence gap by itself does neither.
3. **Reusable declaration.** For typed reuse, the `MaintenanceInspectionAssignment` `RelationSignature` contains `HolderSystemSlot : U.System / U.EntityRef` and the declaration-local `AssignedSystemRoleKindSlot` with `MaintenanceSystemRoleKindDomain` as ValueKind and `ByValue` as refMode. In `InspectionAssignment-17`, `InspectorSystemRole` is the assigned-kind participant value. A stronger direct species adds only its real identity-bearing participants. `assignmentInterval` remains assertion or occurrence-description content, not another participant SlotSpec.
4. **Assertion and participant designations.** An `InspectionAssignmentAssertion` carries designations corresponding to the species' declared SlotSpecs and states the currently known `assignmentInterval` separately. Its claim may say that `Robot-7` is currently assigned as inspector through `InspectionAssignment-17`. If later use only needs that current report, keep the assertion and stop without adding another occurrence object.
5. **Occurrence identity, designator, and reference.** Suppose two episodes of the same direct species have the same complete participant values but occur in inspection shifts separated by a demonstrated predicate-false period. To prepare a history or Work-attribution claim that must distinguish the episodes, a practitioner applies the A.2.1 continuity rule, distinguishes the second occurrence, and assigns a designator only if stable reference is needed. A roster-row identifier, copied field set, taxonomy edition, reference scheme, or reused source key cannot collapse or split the two episodes.
6. **Representation.** A roster row or diagram edge may represent the assignment assertion or an occurrence-description episteme. A roster row's fields and key retain their representation-side meanings; the source elements of a diagram edge retain their representation-side meanings. An explicit declaration or representation correspondence relates a source field to the exact SlotKind and the carried value or reference to the participant designation; using the same spelling for field and SlotKind is optional and establishes no identity. Representation identity does not replace the A.2.1 occurrence rule.

The practical payoff is visible at each stop. In a current staffing report, keep the readable direct sentence. For typed reuse, consult the existing declaration. When history or Work attribution must distinguish a repeated episode, apply the A.2.1 continuity rule and distinguish that episode; assign a designator only if stable reference is needed.

### A.6.REL:5.2 - Hypothetical installed-part boundary {#hypothetical-installed-part-boundary}

`Bearing_B isPartOf Pump_P` may be a readable source claim, but current A.14 does not supply an `InstalledPart` relation kind, installed-part participant meanings, an installed-part obtaining predicate, or its same-versus-new-occurrence rule. Names such as `InstalledPartRelationSignature`, `InstalledPartSlot`, and `AssemblyWholeSlot` are therefore hypothetical candidates, not current declarations. Do not use them to claim conformance or an individuated installed-part occurrence.

A future accepted subject pattern could make installation work or a continuous installation interval identity-bearing, but A.6.REL does not choose that ontology. Until such a subject pattern exists, keep the physical entities, installation work, proposed part relation, assertion, occurrence description, designator, reference, and database or drawing representation separate, and stop before an occurrence-identity result.

### A.6.REL:5.3 - Formal reduced case {#formal-reduced-case}

The expression `3 < 5` is assertion content written in a mathematical notation. Under the referenced arithmetic structure, the values three and five satisfy the less-than predicate. The expression is not thereby a relation occurrence. No receiving use in this case needs the obtaining less-than relation occurrence explicitly individuated under `U.Relation`, so the engineer stops at the assertion. A graph edge or RDF reifier introduced by tooling remains a representation of the proposition or assertion and is not an occurrence-identity rule in the formal subject domain.

### A.6.REL:5.4 - Relation occurrence as a participant {#relation-occurrence-as-a-participant}

`C.22.PFR` has one actual-condition relation occurrence and one problem-criterion-applicability relation occurrence as world-side participants. Each is individuated under its own direct identity rule. The PFR direct pattern states those two participant meanings, its obtaining condition, and its identity rule; the PFR `RelationSignature` episteme declares the corresponding SlotSpecs. A PFR assertion designates the two occurrences according to those SlotSpecs. PFR is a direct relation, not an episteme whose content merely groups two assertions.

### A.6.REL:5.5 - Description and publication recursion through the relation-object architecture {#description-and-publication-recursion-through-the-relation}

Let `R1` be the already individuated second `MaintenanceInspectionAssignment` occurrence from 5.1.

1. An assignment-occurrence description episteme `E1` has `R1` as its exact EntityOfConcern. In the reusable C.2.1 `EpistemeConstitutionRelationSignature`, the declaration-local SlotKind `EntityOfConcernSlot` names the entity-of-concern participant meaning. In a card representation of `E1`, the source field `entityOfConcernRef` corresponds to that SlotKind only through a declared representation correspondence; its `U.EntityRef` value is the participant designation that resolves to `R1`. Neither spelling nor containment identifies the field, SlotKind, designation, or occurrence.
2. A second episteme `E2` contains the result of evaluation work concerning the adequacy of `E1`. Its exact EntityOfConcern is `E1`, not `R1`. A field in a reusable card or other representation may carry a `U.EntityRef` designating `E1`; it corresponds to `EntityOfConcernSlot` only through a declared representation correspondence. The two epistemes therefore have different EntitiesOfConcern and retain separate C.2.1 identities: `E1` describes `R1`, while `E2` evaluates the adequacy of `E1`.
3. Under a publication-relation occurrence, the current edition of `E1` is available to a declared audience and use. The selected episteme edition is an actual participant of that publication relation under the publication pattern's participant meaning. The publication form and its representation elements retain their own kinds and correspond to the published episteme only through the declared publication and representation relations.

A system performing revision work can establish another edition of `E1` or `E2`; a system performing publication work can establish another publication-relation occurrence for a selected edition. `R1` continues or ceases only as the A.2.1 obtaining predicate and occurrence-identity rule determine from the assignment facts. This recursive case preserves the distinction: a description episteme can itself become the actual participant or EntityOfConcern of another relation without becoming the relation occurrence it describes.

## A.6.REL:6 - Bias-Annotation {#bias-annotation}

This pattern has an individuation bias because it serves receiving uses that need relation identity. The lightweight stop rule prevents that bias from turning every direct relation into an explicit relation-occurrence description episteme.

The admitted system-role-assignment case can over-emphasize participant identities and temporal continuity. Another direct relation may instead use constituting Work or another world-side discriminator, but only when its own accepted pattern states that contribution. The hypothetical installed-part boundary demonstrates why A.6.REL must not invent that rule.

Engineers can easily picture relation instances through data-model examples. When a representation must distinguish an obtaining occurrence, first apply the subject pattern's obtaining test to the relevant case facts or constituting history, then apply its occurrence-identity rule. A system introduces a database row, graph edge, reifier, or other representation for that declared use only after those steps. Representing an assertion or another claim family does not by itself require an obtaining relation occurrence or explicit individuation.

## A.6.REL:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Failure | Repair |
|---|---|---|
| Representation-first relation | A table row, edge, or object identifier is treated as what makes the relation obtain. | State the direct relation, participants, and obtaining condition first; treat the row as a representation unless the direct ontology demonstrates that the corresponding representation-producing work is constitutive. |
| Predicate-as-relation | A semantic predicate or its expression is treated as the world-side occurrence. | State the direct relation and its actual participants; use the predicate only to state the truth-valued obtaining condition. |
| Designation treated as occurrence creation | A relation is said to exist only because another assertion designates it. | Recover the test from the subject pattern and determine whether current-case facts or constituting history satisfy it; let the assertion state the result and let designation justify only later reference, never occurrence creation. |
| Participant-identity collapse | Two assignments or part-relation episodes with the same participants become one occurrence. | Apply the direct identity rule and recover its domain discriminator; use a maximal continuous obtaining interval or constituting work only when that rule includes it in occurrence identity. |
| Observation-window identity | A new measurement or assessment window is treated as a new relation occurrence. | Keep the observation window with its measurement or assessment assertion; recognize another occurrence only when the direct relation ceases and resumes or the direct identity rule supplies another discriminator. |
| Edition-as-world-change | Another edition of an assertion, signature, or description episteme, or another publication occurrence, is called a new version of the world-side relation. | Name the exact changed object and apply its own identity or edition rule. Apply A.10 only when receiving work separately needs a reliance judgment about a claim and evidence; it is neither the trigger nor the source of world-side change. |
| Relator by analogy | A dependent truth-maker is introduced although the direct relation ontology does not identify its dependence relations and occurrence identity. | Introduce a relator only where the direct material ontology identifies the relator, its dependence relations to the participants, and its occurrence-identity rule. |
| Full occurrence description by default | Simple engineering prose becomes a mandatory signature-and-description exercise. | Ask whether later work must tell this occurrence from another occurrence of the same relation; when it only reports the current relation, keep the readable direct sentence and stop. |

## A.6.REL:10 - Rationale {#rationale}

Applying this method lets an engineer use exact occurrence identity without equating ontology with documentation. A direct relation can obtain for its participants before an FPF episteme states a sentence about it. The actual relation participants, considered under their participant meanings, satisfy the semantic predicate within the direct relation pattern's declared applicability and temporal conditions; an assertion is an episteme whose content affirms or denies that predicate under its exact direct claim family; `A.10` or the receiving evaluation separately governs supported, refuted, or unresolved reliance; explicit-individuation work is performed by a system for a named receiving use; and an identifier only enables later reference. Keeping those objects and moves distinct prevents semio-bias in which an episteme is mistaken for the world-side relation.

The identity rule belongs to the direct relation pattern because the direct ontology determines whether participant identities suffice. The same complete participant set can stand in two occurrences of one A.2.1 direct species when a demonstrated predicate-false gap separates them. The same component and whole may belong to distinct part-relation episodes only if their accepted subject pattern declares the relevant discriminator; A.6.REL supplies none. Conversely, an ordinary formal order assertion may need no explicit occurrence object in project work. A universal key would be too weak for repetition and too heavy for ordinary use.

Assertion, description, and signature epistemes can have editions; a system performing publication work can establish another publication-relation occurrence for a selected edition. A relation occurrence instead begins, continues, or ceases under its direct rule; when a system applying that rule distinguishes another occurrence, the other occurrence has its own identity. Keeping episteme edition change, publication occurrence, and relation occurrence continuity separate makes repair local and prevents publication history from masquerading as world history.

## A.6.REL:11 - SoTA-Echoing {#sota-echoing}

### Ontological SoTA and constructional sources {#ontological-sota-and-constructional-sources}

This pattern uses these sources to constrain its account of occurrence existence and identity. They provide ontological comparisons, not notation selection.

| Ontological source | What it contributes | FPF adoption, mutation, and practical effect |
|---|---|---|
| Florio and Linnebo, [Introduction to Constructional Ontology](https://www.utwente.nl/en/eemcs/fois2024/resources/papers/florio-linnebo-introduction-to-constructional-ontology.pdf), 2024 | Separates constructors, constructor inputs, the source account's construction process, and output identity. | **Adopt the construction test and adapt the source process to FPF method and work distinctions.** Section 4.3 asks which system acts as constructor, which method it enacts, which entities are inputs, which work it performs, and how that work occurrence contributes to output or relation identity. Row creation and assertion remain non-constructive unless the direct rule declares the corresponding work constitutive. |
| Borgo and Righetti, [Towards Applied Constructional Ontology](https://doi.org/10.3233/FAIA250480), 2025 | Tests how constructional analysis could reconstruct existing foundational ontologies and exposes conceptual, structural, completeness, and consistency questions; it is an early applied step, not a finished recipe. | **Adapt with that maturity boundary.** Checklist 9 and the physical case require a recoverable construction choice instead of accepting an inherited relation representation or taxonomy. |
| Partridge, [BORO Ontology](https://borosolutions.net/boro-ontology), C-FORS 2025 presentation | Presents a 4D extensional, categorical, and constructional ontology with an ontology-evolution method. | **Adapt as a current ontological comparison under a boundary.** Sections 4.3 and 5.1 use temporal extent and constituting occurrences when the direct identity rule needs them. FPF rejects universal 4D identity, unrestricted composition, and BORO's category architecture for this pattern. |
| Almeida, Guizzardi, Sales, and Fonseca, [gUFO](https://arxiv.org/abs/2603.20948), 2026 preprint | Provides a current foundational-ontology implementation with differentiated relational-aspect and reification patterns. | **Adapt its ontological distinctions as a current comparison; reject its OWL implementation as proof of FPF occurrence existence or identity.** Section 4.4 separates direct relation, assertion, reifier, and optional relator without importing the complete category hierarchy. |
| [OntoUML Relator](https://ontouml.readthedocs.io/en/init-ontouml/classes/sortals/relator/index.html), specification lineage | Models a relator as a dependent truth-maker for a material relation. | **Reject as current competitive SoTA; retain and adapt as a lineage comparison for material relators.** Section 4.4 permits a relator only when the direct material ontology identifies the relator, its dependence relations to the participants, and its occurrence-identity rule. |

### Representation and implementation stress tests {#representation-and-implementation-stress-tests}

This pattern uses these sources to test whether the selected ontological distinctions can be represented and used. They do not determine what relation occurrences exist or how they are identified.

| Representation or implementation line | Distinction tested | Bounded use in A.6.REL |
|---|---|---|
| [TypeDB 3.x `links` statement](https://typedb.com/docs/typeql-reference/statements/links/) and current relation model | A query can expose a relation variable with named source-language *role players*, while shorthand remains available when the represented relation instance need not be referenced. That source term denotes neither an FPF system-role kind nor a system-role assignment. | **Adapt as a representation stress test; reject as an ontology source.** Sections 4.2, 4.5, and 4.6 preserve a readable direct relation before explicit individuation. TypeDB demonstrates one implementable representation; it does not establish the FPF relation kind, obtaining condition, or identity rule. |
| [RDF 1.2 Concepts](https://www.w3.org/TR/rdf12-concepts/), Candidate Recommendation Snapshot, 7 April 2026 | Distinguishes a proposition expressed by a triple term, assertion of a triple, and reifiers used for further statements. | **Adapt as a representation stress test; reject graph syntax and reifier identity as world-side identity sources.** Sections 4.4 and 5.3 apply that distinction to proposition, assertion, and reifier separation. |

The worked cases expose both boundaries outside information-system projects.


## A.6.REL:End {#end}
