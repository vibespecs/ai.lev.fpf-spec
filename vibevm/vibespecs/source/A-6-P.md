# A.6.P - Relational Precision Restoration - Recovering Direct Relations from Under-Specified Claims: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## A.6.P:5 - Archetypal Grounding {#archetypal-grounding}

### A.6.P:5.1 - Physical assembly and repeated occurrences {#physical-assembly-and-repeated-occurrences}

**Tell.** A maintenance note says `replacement bearing is linked to Pump_P`.

**Show the ordinary repair.** Recover physical bearing `Bearing_B`, pump `Pump_P`, and interval `Interval_T` independently. The readable candidate claim is `Bearing_B is part of Pump_P during Interval_T`. Select the intended direct parthood reading under A.14 and its applicable subject rule. Where that predicate and the case facts already settle the receiving question, state the assertion and stop; an installation history or occurrence identifier is not required merely to report current parthood.

**Show the identity-dependent stop.** A reliability analysis needs to distinguish the installed-part relation before removal from that after reinstallation. Current A.14 does not define an `InstalledPart` relation kind, its participant meanings, obtaining predicate, applicability, or same-versus-new-occurrence rule. Return A.6.RCD `missing-governor` for that proposed relation, naming `Bearing_B`, `Pump_P`, the relevant intervals, and the reliability comparison. Removal and reinstallation alone do not establish two occurrences. A.6.REL explains how to apply a supplied identity rule; it does not supply this missing rule.

**Conditional continuation.** If a direct installed-part definition is accepted, apply its obtaining and same-versus-new-occurrence rules to the case facts. Distinguish two occurrences only when that rule and those facts warrant them; add stable designations or occurrence descriptions only when the receiving use needs them. For repeated typed reuse, an `InstalledPartRelationSignature` may then declare `InstalledPartSlot` and `AssemblyWholeSlot` under A.6.5. Until that definition exists, these names remain hypothetical declaration candidates, as in A.6.REL:5.2 and A.6.5:5.2.

If the adopted construction rule makes installation Work constitutive, identify that independently admitted Work and its declared identity contribution. Database rows, diagram edges, assertions, and declaration components retain their own identities and do not supply the obtaining or recurrence rule. When a mathematical representation is used, state its C.29 correspondence separately. A separate relator is needed only if the direct ontology identifies and justifies it.

### A.6.P:5.2 - Clinical evidence use and negative reliance {#clinical-evidence-use-and-negative-reliance}

**Tell.** A care note says `the measurement supports the dose change`.

**Show.** The repair distinguishes the measurement work occurrence, its measurement-result episteme, the work-plan claim, the measured characteristic, the applicable range, and the exact evidence relation. `C.16` governs measurement construction and applicability; `A.10` governs whether that episteme bears on the named dose-change claim for this use. The broad predicate is not replaced by a universal support relation.

**Show the boundary.** If current evidence refutes the dose-change assertion or leaves reliance unresolved, the receiving evaluation records that posture. It does not create a negative world-side measurement, treatment, or evidence occurrence. A fresh publication of the same measurement-result episteme changes availability, not the measured condition or evidence relation by itself.

### A.6.P:5.3 - Episteme correspondence and representation {#episteme-correspondence-and-representation}

**Tell.** Two teams say `the models are aligned`, and one tool draws an edge between their model nodes.

**Show — models.** Model epistemes `DesignModel_E` and `MaintenanceModel_E` have `EntityOfConcern` `PumpAssembly_P204` and effective reference schemes `CAD-Part-Scheme-v7` and `Asset-Register-Scheme-2026Q2`, respectively. `AlignmentEdge_17` joins nodes labelled `BRG-6204` and `bearing-4471`.

**Structure decision.** No established model-use structure changes either label's reading or whether replacement approval may use the pairing. Add no `BoundedModelUseStructure`; a diagram boundary is not evidence.

**Needed sentence.** `For bearing-replacement planning on PumpAssembly_P204, CAD-Part-Scheme-v7 label BRG-6204 and Asset-Register-Scheme-2026Q2 label bearing-4471 denote the same installed bearing.` This is a candidate claim, not yet a fact.

**Edge boundary.** Under `C.29`, `AlignmentEdge_17` represents that sentence. It does not make the sentence true, prove one referent, or identify a Bridge occurrence.

**Adjacent reading.** Record `ninety-seven percent of endpoint pairs passed the mapping test` with `C.16`. If approval relies on that measurement, `A.10` governs the evidence relation. The percentage does not establish the needed sentence.

**Result.** `A.6.RCD missing-governor`: bearing-replacement approval is blocked; participants are `BRG-6204` and `bearing-4471`; the needed sentence is above; the edge remains a representation. No current direct correspondence or Bridge pattern states when the cross-scheme claim holds. A future direct pattern must state its predicate, conditions, and, if occurrences must be distinguished, identity rule. Until then, do not assert `the models are aligned` or mint a Bridge from the edge or a Card.

**Show the boundary.** The graph edge and its endpoint positions remain representation elements. An explicit `C.29` correspondence states which assertion content, participants, and direct relation the edge represents. The edge does not make the correspondence obtain, prove same EntityOfConcern, or individuate a relation occurrence. Shared labels likewise establish neither same world-side referent nor substitutability.

When the claim is that both model epistemes concern the same world-side holon, recover each episteme's exact EntityOfConcern or grounding designation plus the observations, trajectory, or identity evidence governed for that holon. A Bridge preserves stated correspondences and losses; it does not prove the common world-side referent.

**Show the viewpoint-conformance use.** A review must decide whether model episteme `E` conforms to maintenance viewpoint episteme `P`. Identify `E` from its claim content, EntityOfConcern, and effective reference scheme, and resolve `P` as one claim-bearing viewpoint edition before reading a diagram, field, or reference as ontology. Then apply the direct predicate governed by `E.17.0`: `EpistemeViewpointConformanceRelation(E,P)`. Plainly, `E` conforms to this exact viewpoint.

For unchanged `E` and `P`, the pair `<E,P>` determines one positive occurrence. Selecting `P` for this review is a separate use qualification: selection neither makes conformance obtain nor enters occurrence identity. If another review selects `P2`, test `<E,P2>` instead of retagging `E`. A `viewpointRef` or diagram label does not identify either participant by itself. A query, transformation, or projection may supply construction history for `E`, but neither that history nor an assertion, evaluation, representation, or publication makes conformance obtain.

Add an occurrence designator only if the next decision must distinguish two conformance occurrences. Add an evaluation result or evidence path only if the reader must rely on the conformance verdict. Add construction history only if the task asks how `E` was produced; add a representation or publication only if another reader must inspect or receive it; add associated Work only if the task asks who performed which activity. Otherwise add none of these objects. A.6.P stops after recovering `E`, `P`, and the direct relation; `E.17.0` governs the predicate and, if the use separately asks whether an episteme is a `U.View`, that recognition.

### A.6.P:5.4 - Method, Work, system-role objects, and agency {#method-work-system-role-objects-and-agency}

The sentence `the inspection method checks Pump_P` may remain ordinary metonymy under F.19. For a separate claim about actual inspection history, recover the following exact case. The source basis says that admitted `System_S` has the A.13 core for inspection: it is independently classified under local kind `InspectorSystemRole` and holds obtaining `InspectionAssignment-17` of declared `MaintenanceInspectionAssignment` species for the stated scope and window. A.15.1 then independently admits `InspectionWork_W` and its `enactsMethod(InspectionWork_W, InspectionMethod_M)` relation; the examination relation separately connects the Work to `Pump_P`. Because this worked account expressly states under which assignment the inspection was performed, F.6 then establishes `performedUnderAssignment(InspectionWork_W, InspectionAssignment-17)` and checks the already recovered performer against the holder. If that F.6 relation were unsupported, the Work would remain and only its assignment-bound attribution would be unresolved. Taxonomy episteme and reference scheme may interpret the assertion but are not assignment participants. `System_S` performs `InspectionWork_W`.

### A.6.P:5.5 - Formal reduced case {#formal-reduced-case}

`3 < 5` is assertion content in mathematical notation. The numeral occurrences, comparison sign, and operand places are representation elements under `C.29`. An explicit correspondence can relate them to the values, direct less-than predicate, and any compatible declaration used for typed reuse. No receiving use here distinguishes one obtaining occurrence from another, so the engineer stops at the assertion. A graph edge, tuple, or statement reifier introduced by a tool represents the proposition or assertion; it does not constitute the direct relation.

## A.6.P:6 - Bias-Annotation {#bias-annotation}

This pattern favors ontology-first recovery, direct relation sentences, and the lightest explicit form that serves the named receiving use. That bias counters record-first and vocabulary-first repair.

The counter-risk is under-specification: an engineer may stop before a load-bearing participant, applicability condition, occurrence identity, or reference is exposed. The receiving-use test, hidden-arity check, three-way relation-dependent wording distinction, and explicit conditions for applying neighboring patterns provide the counterweight.

The pattern also favors neutral domain language. Examples span physical assembly, clinical Work, epistemes, ambiguous source *role* wording, system-role kinds and assignments, Methods, and formal relations so that one publication technology or professional tradition does not become the default ontology.

## A.6.P:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Failure mode | Why it fails | Repair |
|---|---|---|
| Replace a broad word with a more technical synonym | The same participants and obtaining condition remain unresolved. | Ground the objects, select the direct relation, and write the readable sentence before naming. |
| Turn every relation phrase into a record-shaped episteme | Representation burden appears before any receiver needs the episteme or occurrence identity. | Use the direct sentence and apply the `A.6.REL` receiving-use test. |
| Let the declaration make the relation obtain | A declaration episteme is confused with the world-side relation. | Keep reusable laws and `SlotSpec`s in `A.6.0` and `A.6.5`; keep obtaining and identity with the pattern that defines the relation. |
| Treat the actual participant as occupying a declaration component | World-side participation is replaced by a schema metaphor. | State participation under the direct participant meaning; use the `SlotSpec` only inside a compatible reusable declaration. |
| Treat relation-dependent wording as an intrinsic kind | A participant described as result, input, or next continuation loses its own kind. | Apply the three-way distinction and use C.3 only for actual typed reasoning. |
| Use one generic relation-change verb | Occurrence change, assertion revision, declaration revision, evidence change, reference retargeting, EntityOfConcern retargeting, and representation change collapse. | Select the changed object and use the operation governed for that object. |
| Infer agency or identity from an active verb | Grammar is treated as ontological evidence. | Recover the exact acting system or direct identity rule independently of grammar. |
| Preserve a hidden union as a long list | The predicate changes meaning across listed participant kinds. | Recover the common predicate or split the relation kind and any compatible declarations. |
| Reverse a sentence for style | Participant meanings and polarity can change silently. | Use the direct inverse law or keep the forward predicate explicit. |
| Use a graph, tuple, function, arrow, or table as ontological proof | Representation is mistaken for what it represents. | State an explicit `C.29` correspondence and keep world-side obtaining and identity with the direct pattern. |

## A.6.P:10 - Rationale {#rationale}

The problem is ontological before it is lexical. A broad expression is dangerous because it can hide different objects, predicates, participant meanings, actual participants, or later claims and operations. Replacing the expression without recovering those objects merely moves the ambiguity.

FPF therefore begins with relation realism: a relation may obtain independently of an assertion about it. Actual participants retain their independently governed kinds while participating under relation-local meanings. An optional `RelationSignature` makes those meanings reusable as typed declaration content; an assertion or description can designate participants or an already recoverable occurrence; a representation corresponds to the selected object or claim content. None of those adjacent objects substitutes for world-side obtaining or identity.

Construction matters only when the direct ontology makes it identity-bearing. In that case, constructor, inputs, construction work or process, and output identity explain how another occurrence begins. Other relations may obtain without such a constructor. A.6.P therefore uses constructional analysis as a discriminating test rather than as a universal ontology.

Progressive elaboration preserves affordability. An engineer can stop at a readable direct fact. Typed declaration, assertion detail, occurrence identity, stable references, descriptions, publications, and representations appear only when a named later claim or operation depends on them. This order also explains why naming comes late: a good name helps designate a recovered distinction but cannot create it.

The changed-object rule prevents a second ontology collapse. Revising an assertion, declaration, evidence relation, designation, reference, publication, Bridge, or representation is not automatically a change in the direct relation being discussed. Naming the changed object makes continuity, evidence, and return conditions intelligible.

Neutral terminology matters because A.6.P is cross-domain. Every claim about an object uses the rule that defines or constrains that claim; A.6.P does not collect unlike objects under one local umbrella. Domain-specialized vocabulary enters only when a direct local pattern defines or constrains the current object.

## A.6.P:11 - SoTA-Echoing {#sota-echoing}

### Ontological SoTA and constructive grounding {#ontological-sota-and-constructive-grounding}

These sources constrain relation occurrence, identity, and construction. They are not interchangeable: FPF takes constructor-and-input discipline from the constructional-ontology line, uses BORO as a distinct 4D comparison, and treats implementation ontologies as stress comparators rather than proof.

| Ontological source and status | What it contributes | FPF adoption, mutation, and practical effect |
|---|---|---|
| Florio and Linnebo, [Introduction to Constructional Ontology](https://www.utwente.nl/en/eemcs/fois2024/resources/papers/florio-linnebo-introduction-to-constructional-ontology.pdf), 2024 | Separates constructors, constructor inputs, and constructional process, and examines functional and relational ways to characterize construction and output identity. | **Adopt the discriminating construction test.** Recover constructor, inputs, process, and identity only when the direct relation ontology makes construction constitutive. A storage operation is not thereby an ontological constructor. |
| Borgo and Righetti, [Towards Applied Constructional Ontology](https://doi.org/10.3233/FAIA250480), 2025 | Tests how constructional analysis can expose conceptual, structural, completeness, and consistency choices while marking unresolved application questions. | **Adopt as improvement pressure, not an imported ontology.** A.6.P exposes the exact construction and identity choice whenever it changes occurrence identity. |
| Partridge, [BORO Ontology](https://borosolutions.net/boro-ontology), C-FORS 2025 presentation | Presents BORO as a 4D extensional, category, and constructional ontology with an evolution method. | **Use as an ontological comparison under an explicit boundary.** A.6.P may use temporal extent when the direct identity rule needs it; FPF does not import universal 4D identity, unrestricted composition, or BORO's category architecture. |
| Almeida, Guizzardi, Sales, and Fonseca, [gUFO](https://arxiv.org/abs/2603.20948), 2026 preprint | Provides a foundational-ontology implementation with differentiated relation and reification patterns. | **Use the distinctions as a comparator; do not treat the implementation as proof.** Direct relation, optional explicit occurrence, assertion, and representation remain separate without importing the source category hierarchy. |
| [OntoUML Relator](https://ontouml.readthedocs.io/en/init-ontouml/classes/sortals/relator/index.html), specification lineage | Models a relator as a dependent truth-maker whose existence connects participants in a material relation. | **Retain as a material-relation comparator, not a universal answer.** The physical case requires the direct parthood ontology to identify and justify such a truth-maker before a relator is introduced; formal and other relations receive none by analogy. |
| Andrei Rodin, [Venus Homotopically](https://philsci-archive.pitt.edu/12116/), 2016 | Shows that identity across presentations is not obtained from a shared label alone; background, observations, and a trajectory can establish the same world-side referent. | **Retain as constructive-grounding lineage.** Candidate referents are separated through observations, identity tests, and direct-pattern conditions; naming does not close ontology. |

### Representation and implementation stress tests {#representation-and-implementation-stress-tests}

These sources do not decide what exists. They test whether a representation can preserve the ontological distinctions selected above without turning a statement, row, graph term, tuple, or reifier into the world-side occurrence.

| Representation or implementation line | Distinction tested | Bounded use in A.6.P |
|---|---|---|
| [TypeDB 3.x `links` statement](https://typedb.com/docs/typeql-reference/statements/links/) and current relation model | A query can select an explicit relation variable with named source-language role players, while shorthand remains available when no reference to the represented item is needed. | **Test progressive explicitness, not ontology.** A.6.P makes explicit occurrence identity conditional on a named receiver. TypeDB demonstrates one implementable representation; it does not establish the FPF relation kind, actual participation, obtaining condition, or identity rule. |
| [RDF 1.2 Concepts](https://www.w3.org/TR/rdf12-concepts/), Candidate Recommendation Snapshot, 7 April 2026 | RDF distinguishes proposition expressed by a triple term, assertion of a triple, and reifiers used for further statements. | **Test proposition, assertion, and reifier separation.** A statement term or graph edge can represent claim content but cannot establish that the direct relation obtains. |

### Service and access separation pressure {#service-and-access-separation-pressure}

These sources constrain the recovery of service or access wording; they do not define a service ontology for FPF.

| Source line | Separation pressure | FPF adoption, adaptation, and rejection |
|---|---|---|
| [S-OPL: Service Ontology Pattern Language, specification v1.7](https://nemo.inf.ufes.br/en/projetos/patterns-and-pattern-languages/) | Offering, agreement, participants, and delivery are related but different modeling problems. | **Adopt** the separation; **adapt** it by using the existing patterns for promise content, commitment, speech acts, direct participation, system-role kinds, direct system-role assignments, Work, evidence, and evaluation. **Reject** the imported process ontology and service ontology, participant taxonomy, and any common service-situation carrier or service bundle. |
| [NIST SP 800-207, Zero Trust Architecture](https://csrc.nist.gov/pubs/sp/800/207/final) | Requester, resource, policy decision, and enforcement functions must remain distinguishable in an access decision. | **Adopt** the demand to name the exact requester, requested use, resource, policy or grant, and enforcement facts; **adapt** grants through A.2.8.PER and performed enforcement through a system, assignment, and dated Work when those facts are current. **Reject** the component diagram as FPF ontology and infer neither `U.Access` nor `AccessRelation`. |
| [The Open Group ArchiMate 3.2 specification](https://pubs.opengroup.org/architecture/archimate32-doc/) | Service, interface or point of access, and realization system are not interchangeable. | **Retain as a comparison only.** Distinguish a service provision, access description or Method, exact access point, and realization bearer; use A.1 only for a separate system-dependent claim. **Reject** imported ArchiMate elements and relations, source-word-induced systemhood, and addressability as a classification rule. |

Earlier public service lineage also cited ITIL 4, ISO 24617-2 speech-act practice, and SRE literature. They remain bounded examples rather than ontological governors: ITIL offer and service-level wording can cue A.2.3 or A.6.C; a communicative act is separated from its content and any enduring binding by A.2.9, A.2.3, and A.2.8; SRE interface, SLO, deployment, telemetry, and incident distinctions can help name separate claims. None licenses an always-unpack word rule, a mandatory facet family, every deontic phrase becoming a commitment, every performative phrase becoming a speech act, or actuals becoming Work and evidence automatically.

Across these sources, FPF adopts separation pressure and adapts it to the subject-and-relation distinctions in 4.11a. It explicitly rejects `U.Access`, `AccessRelation`, a service bundle, word-induced systemhood, and blanket actuals-to-Work.

The first table governs the general ontological moves. The second checks representability only after those moves have been selected. The service-and-access table constrains one recurring recovery branch without importing a service ontology. The physical, clinical, episteme, work, and formal cases test that the resulting method is not specialized to information systems.

**Reopen the smallest affected passage.** Start with the one claim, case, continuation, or source row that uses the changed fact. Reopen it when the exact subject predicate changes who participates, when the relation obtains, or how an occurrence is reidentified; when newer source evidence overturns or narrows the construction or reification distinction used there; or when an actual use can no longer reach the practical result or stopping boundary promised by that passage. Do not reopen the whole pattern unless the same change reaches several passages. If a continuation no longer matches the cited pattern's `Use this when` condition and promised result, stop using that continuation until it is repaired.

## A.6.P:12b - C.29 mathematical-lens account and representation boundary {#c-29-mathematical-lens-account-and-representation-boundary}

Use `C.29` for a declared mathematical-lens-use account or representation only when a mathematical object, tuple, graph, function, arrow, table, or other formalism is used for a stated subject and purpose. It defines the candidate mathematical object designation, mapping mode, explicit correspondence, preserved structure, lost structure, declared use, stop or return condition, and any justified blocked overread. Select that overread through F.19's plausible-reader test. C.29 does not assert world-side participation, make a direct relation obtain, admit its kind, or supply occurrence identity.

When a sentence claims cross-context meaning, export, correspondence, or substitution, first name what each endpoint means locally, then use `F.9` to state and test the direct Bridge predicate. F.9 supplies the obtaining condition and occurrence-identity rule when the two exact local-sense endpoints resolve, their interpretation bases differ, and the declared profile applies. `C.2.1` separately identifies an assertion, occurrence description, or Bridge Card and the bounded-use claim; `A.10` and `B.3` separately govern evidence reliance and assurance, `E.24.PUB` governs publication, and the receiving object's pattern governs any use that actually occurs. A changed claim, Card, evidence item, reliance result, or publication is not a changed Bridge occurrence. Use `C.29` only when the reader relies on a representation or mathematical-lens account; a representation does not establish the Bridge or the represented world-side relation. If the sentence needs no cross-context correspondence or substitution claim, add no Bridge. If it needs another relation for which no current pattern supplies a defining or testing rule after the participants and needed sentence are explicit, record the established A.6.RCD `missing-governor` result.


## A.6.P:End {#end}
