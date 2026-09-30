# E.4.PFIP - Principle-Framework Publication Integration and Preservation: depth {#depth}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## E.4.PFIP:5 - Archetypal Grounding {#archetypal-grounding}

**Tell — one-to-one text revision.** A DPF maintainer adds an accepted pattern and updates one existing pattern. The source-to-candidate comparison confirms both changes. A text comparison with the predecessor monolith then finds an unrelated non-use boundary deleted during paragraph cleanup. That boundary has no accepted retirement decision, so the preservation conclusion reports accidental loss even though the build and accepted-source comparison are clean.

**Show — one form split into two.** One predecessor pattern-text form is split into two candidate forms. The accepted split decision names all three expressions. The complete predecessor inventory allocates a shared working-situation claim to both candidates, three predecessor claims to one candidate pattern card, and one obsolete tool instruction to an accepted content-retirement decision. A predecessor non-use warning appears in neither candidate. Retiring the old form does not retire the warning, so the missing line blocks preservation until the warning is restored or its content change or retirement is accepted.

**Show — architecture diagram.** One FPF architecture-diagram form is replaced one-to-one by a candidate diagram for the same orientation use. The diagrams have no useful line diff. The maintainer uses the FPF pattern that defines or constrains that diagram form to select named framework parts, dependency edges, and legend distinctions for the inventory. The maintainer uses `C.33` to record captured and lost structure and `C.34` to record the declared correspondence. One predecessor dependency edge has no candidate correspondent, so similar layout cannot support a positive conclusion.

**Show — local practice framework.** An LPF candidate replaces a repeated general explanation with a reference to a new FPF method. The accepted-source comparison passes. The predecessor comparison still checks the LPF's local recovery cue, concrete work-size limit, and tool-specific stop because the general FPF method does not include those local actions. Removing them would be loss, not successful deduplication.

## E.4.PFIP:6 - Bias-Annotation {#bias-annotation}

**Scope:** Limited to accepted-source integration and predecessor continuity for FPF, DPF, and LPF publication expressions. The complete-traversal rule applies across text, diagrams, cards, retrieval forms, and split or merged publications only when a selectable inventory and feasible semantic inspection exist for the declared use. It is not a universal software-merge, data-migration, or digital-preservation method.

| Lens | Likely drift | Repair |
| --- | --- | --- |
| Gov | Source parity, a green build, or an accepted form change is read as permission to change or retire predecessor content. | Require an accepted content-change or content-retirement decision for that disposition. Keep the preservation conclusion as comparison evidence, not acceptance, release, landing, or assurance authority. |
| Arch | Edition, form, expression relation, carrier, and publication occurrence collapse into one file or bundle, so a surviving carrier is treated as surviving content. | Keep the objects distinct; use eligible expression pairs for one-to-one continuity and allocation comparisons for every split or merge. |
| Epist (Epistemological and Ontological) | A selected inventory is treated as complete knowledge of the publication because filenames, headings, or visible text were covered. | Select the inventory through the applicable FPF pattern or another accepted basis for the declared use. Return `missing form-comparison basis` when no complete inventory can be selected. |
| Prag | Complete traversal grows into a written positive ledger, or cost pressure turns one proxy into preservation proof. | Traverse every inventory entry, reuse shared evidence, and write only losses, accepted changes or retirements that explain a difference, unexpected additions, blockers, and unresolved questions. |
| Did | Retained content without a prose row looks unchecked, so reviewers ask for duplicate status text instead of inspecting the traversal boundary. | State once that the complete inventory is checkable and ordinary retained entries need no prose rows; use the unlike worked cases to teach where a separate result is required. |

The external source traditions below come mainly from software transformation, merge analysis, and digital preservation. They make semantic and form-specific comparison visible, but they do not make a principle framework into software or an archival object. The applicable FPF pattern defines or constrains what matters for each form, and the maintainer selects the inventory for the declared publication use.

## E.4.PFIP:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | What fails | Repair |
| --- | --- | --- |
| Source parity proves preservation | Accepted additions are present, but unrelated predecessor content may be gone. | Run the predecessor-to-candidate comparison independently. |
| Green build proves preservation | Syntax and assembly succeed while meaning or selected structure disappears. | Select the form-appropriate inventory and inspect semantic outcomes. |
| Same use means same form | Two different forms serving orientation are paired as versions. | Require retained form identity or an accepted one-to-one continuity decision. |
| Text diff for every form | Diagram relations, card fields, or retrieval cues have no meaningful shared spans. | Use the FPF pattern that defines or constrains the form, `C.33`, or `C.34` to select content or structure. |
| Retired form, retired content | A split or merge decision silently authorizes every old omission. | Run the allocation comparison over the complete predecessor inventory. |
| Collective-publication shortcut | Several forms or carriers are renamed as one bundle so one comparison seems sufficient. | Keep named expressions separate and use them as inputs to the allocation comparison. |
| Carrier continuity as content continuity | An unchanged file or address is treated as proof that the selected edition and expression still obtain. | Apply `E.24.PUB` and compare the selected expression, not the storage proxy. |
| Positive preservation ledger | Every unchanged sentence or field receives a report row. | Keep completeness checkable and report losses, accepted differences, unexpected additions, blockers, and unresolved correspondences or content-change questions. |
| Fabricated predecessor | A first publication is forced through a predecessor comparison. | Use accepted-source incorporation, complete candidate inventory, and package evaluation only. |

## E.4.PFIP:10 - Rationale {#rationale}

This method belongs in the `E.4` ecosystem because FPF, DPF, and LPF publications share one recurring integration problem. Accepted source carry-through and predecessor preservation answer different questions; when both are claimed, neither implies the other.

`E.24.PUB` distinguishes edition, expression, form, carrier, audience, use, and publication occurrence. `E.17` supplies the method for reader-facing plurality. `C.33` and `C.34` define captured, lost, and corresponding selected structure. Independently redefining those distinctions here would create a second publication ontology. The integration method uses these existing distinctions together.

The one-to-one and allocation branches remain separate because they answer different correspondence questions. A pair compares two expressions. An allocation traverses several named expressions without inventing a collective expression or treating a form decision as a content decision.

## E.4.PFIP:11 - SoTA-Echoing {#sota-echoing}

| Current source branch and reference | Working lesson | Adoption in this pattern | Boundary |
| --- | --- | --- | --- |
| Semantic merge: Da Silva, Borba, Maciel et al. (2024), [“Detecting semantic conflicts with unit tests”](https://doi.org/10.1016/j.jss.2024.112070) | Current empirical semantic-merge work shows that textual and structured merge can succeed while an unwanted semantic change remains; the reported method uses behavior-relevant tests as partial specifications. | **Adapt.** The Solution does not treat build or text-diff success as sufficient evidence of preservation and requires a use-relevant inventory with explicit loss outcomes. | Software tests are not imported as a universal framework-publication check; each publication form supplies its own comparison basis. |
| Transformation traceability and versioned co-evolution: Höppner and Tichy (2024), [“Traceability and reuse mechanisms, the most important properties of model transformation languages”](https://doi.org/10.1007/s10664-023-10428-2), and Homolka, Marchezan, Assunção et al. (2026), [“What really happened to my models?”](https://doi.org/10.1007/s10664-025-10773-4) | The empirical survey identifies traceability and reuse as leading transformation-language capabilities while showing that their effects vary with use and scale. The later evaluated approach retains complete model and metamodel histories, links model changes to the changes that caused them, and permits several versions to coexist. | **Adapt.** Source contributions, predecessor content, and selected structures keep explicit candidate correspondences; source incorporation does not replace predecessor preservation; and pair results may be reused inside a larger allocation without replacing it. | The survey measures transformation-language practice, and the later approach evaluates model co-evolution. Neither establishes complete traceability for a framework publication. This pattern adds no transformation language, operation history, automatic correspondence claim, or generic traceability relation. |
| Reusable model migration: Bettini, Di Salle, Iovino, and Pierantonio (2024), [“Supporting reusable model migration with Edelta”](https://doi.org/10.1016/j.jss.2024.112012) | Changes to a metamodel can invalidate dependent artifacts. The evaluated approach reuses migration patterns across domains while retaining custom or interactive rules for changes that automatic migration cannot settle. | **Adapt.** One reusable comparison method covers FPF, DPF, and LPF; the pattern that defines or constrains a publication form supplies its form-specific inventory, and a changed public interface brings its direct consumers into the candidate. | The Edelta language, metamodel kinds, automatic copier, and model-migration operations are not imported into FPF publication ontology. |
| Digital-preservation planning: the current [NARA Digital Preservation Framework](https://www.archives.gov/preservation/digital-preservation/risk), its [structured-data preservation guidance](https://www.archives.gov/preservation/digital-preservation/linked-data/structureddata), and Becker (2018), [“Metaphors We Work By”](https://archivaria.ca/index.php/archivaria/article/view/13628) | NARA selects significant properties by record type and uses them as transformation-test criteria while stating that its plans are not exhaustive or universal. Becker shows why bits, records, computed performances, and preservation claims cannot be collapsed into one digital-object metaphor. | **Adapt.** The applicable FPF pattern defines or constrains the inventory basis, the maintainer selects the inventory for the declared use, and edition, content, form, carrier, and publication occurrence remain separate. | NARA record categories and archival authenticity terms are not imported as FPF kinds or as one universal significant-property list. |

These traditions support one shared stance: compare the properties and correspondences that matter for the declared use, not the easiest visible proxy. The semantic-merge row disciplines the one-to-one text case; the traceability and migration rows discipline the split-form case and direct-consumer closure; and the preservation row disciplines the diagram case and the separation of edition, form, content, and carrier. The method adapts that stance to principle-framework publications and keeps its scope narrower than general software merge, data migration, or digital preservation.

Reopen this source use when current publication-preservation or structured-transformation practice supplies a cheaper complete semantic comparison, shows that trace reuse can replace rather than only support allocation traversal, or demonstrates a non-framework use that warrants a broader pattern scope.


## E.4.PFIP:End {#end}
