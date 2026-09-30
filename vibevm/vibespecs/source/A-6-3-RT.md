# A.6.3.RT - Representation-Scheme Transition: Change Representation of the Same EntityOfConcern: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## A.6.3.RT:5 - Archetypal grounding {#archetypal-grounding}

### A.6.3.RT:5.1 - Ordinary same-concern text-to-table move {#ordinary-same-concern-text-to-table-move}

**Source slice.** `Service S showed three recurring latency spikes in the evening batch window. Trace T-44 and dashboard pin D-17 concern the same service and time window.`

**Target table.** These are recurring latency spikes.

| Service | Window | Spike count | Source pins |
| --- | --- | --- | --- |
| Service S | Evening batch | 3 | T-44, D-17 |

The first result needs no endpoint dossier. The note says the service, window, count, recurrence, and pins can be inspected together; those claims survive; prose order is lost; no causal or severity claim is added; use is inspection; and any question about an omitted qualifier or causality returns to the source note and traces.

An independently cited target includes the recurrence caption. If the table is independently cited or disputed, exact source episteme `LatencyFinding-X` and receiving episteme `LatencyTable-Y` concern `Service-S-during-W` under effective schemes `ServiceTelemetryScheme-4` and `TabularTelemetryScheme-2`. `TabulateLatency : LatencyFinding-X -> LatencyTable-Y` is the exact construction; it states claim construction, endpoint-scheme relation, same exact EntityOfConcern, preservation, omission and recoverability, prohibited strengthening, applicability, inspection-only use, and return to the source note and traces. The visible table form and file carrier are not `Y`.

### A.6.3.RT:5.1.a - A diagram used in a geometric construction {#a-diagram-used-in-a-geometric-construction}

A.6.3.RT.OE:5.1 develops the equilateral-triangle construction on a nonzero segment AB in the Euclidean plane. It keeps the same segments available as radii of two constructed circles and as sides of the triangle. The radius equalities can then be combined in the geometric argument.

For the RT use, the source consists of the construction instructions and intermediate geometric relations. The representation note preserves the circle constructions and segment identities, names joint inspection as the gain, and returns to the subject premises if an intersection or equality is disputed. Geometry supplies the construction and justified conclusion; drawing measurements are not proof premises. The construction and drawing can develop together.

### A.6.3.RT:5.1.b - Syllables against a hand-cycle reference {#syllables-against-a-hand-cycle-reference}

A.6.3.RT.OE:5.3 prepares given syllable-duration assignments against a learned three-beat hand cycle with four pulses per beat. Arithmetic and rhythmic composition determine the six-pulse preparation and the phrase's ending at the third cycle boundary.

RT's representation note retains duration assignments, pulse constancy and cycle position, identifies coordination with the hand reference as the gain, and returns to those conditions when the ending no longer aligns. The utterance and gestures can both represent rhythmic content and realize rhythm. Actual fluency or learning requires observation when either is the question.

### A.6.3.RT:5.2 - Positive later-specific table-to-diagram occurrence {#positive-later-specific-table-to-diagram-occurrence}

For this identity-and-obtaining illustration, take the stated endpoint, scheme, model-use, Work and binding facts as hypothetical givens. The source table, receiving diagram and omitted qualifiers are not shown, so this case does not replay their preservation comparison.

Exact source episteme `CoolingLoopRelationTable-X` and exact receiving episteme `CoolingLoopDependencyDiagram-Y` state the same two connection claims about `CoolingLoop-7` under effective schemes `TabularPlantScheme-5` and `DirectedDiagramPlantScheme-3`. `Y` is a candidate episteme, not automatically a `U.View`.

Scheme-description epistemes `TabularPlantSchemeDescription-5` and `DirectedDiagramPlantSchemeDescription-3` concern their respective schemes and state their interpretation rules. Independently selected `CoolingLoopReviewModelUseStructure` satisfies A.1.1 because its model-use organization changes this review. A.13 identifies `PlantModelingTool-2` as the actual performer through the exact covering assignment. A.15.1 independently admits dated `CoolingLoopDiagrammingWork-18`. Because this example states precise assignment-bound attribution, its direct case fact says that the Work was performed under the same exact A.13 assignment, so the F.6 check is positive. If that direct fact were missing or another F.6 condition failed, the Work would remain intact and only the attribution would be unresolved. The Work's A.6.1 bindings use all six participants. `DiagramCoolingLoop : X -> Y` is the exact construction; it states claim construction, endpoint-scheme relation, same exact EntityOfConcern, preserved connection claims, omitted table qualifiers and their recoverability, prohibited strengthening, applicability, topology-inspection use, and return to `X`.

Only then does this occurrence obtain:

```text
RepresentationSchemeTransitionRelation@Context(
  CoolingLoopReviewModelUseStructure,
  CoolingLoop-7,
  CoolingLoopRelationTable-X,
  CoolingLoopDependencyDiagram-Y,
  TabularPlantSchemeDescription-5,
  DirectedDiagramPlantSchemeDescription-3)
```

Its transition-description episteme cites the Work, construction, exact source relations, omitted qualifiers, topology-inspection use, blocked control-timing/work-order inference, and return to `X`. Rows become directed edges; pairwise lookup becomes topology inspection; each edge links back to its source-table relation. Publication, diagram form, and SVG carrier remain separate. `Y` is a `U.View` only if E.17.0 conformance independently obtains.

### A.6.3.RT:5.2.a - Correspondence-mediated text-to-table shift {#correspondence-mediated-text-to-table-shift}

**Source prose.** `In the safety view, CL-2 maintains the required temperature condition during standard operating demand.`

**Target row.**

| Source framing | Subject | Preserved claim | Correspondence reference |
| --- | --- | --- | --- |
| Safety | CL-2 | maintains required temperature condition during standard operating demand | CM-12 |

`CM-12` is an additional illustrative correspondence reference, not content recovered from the source quotation. Until its relation kind, endpoints and obtaining basis are supplied, this row does not establish a correspondence-mediated exact construction.

For reliance-facing use, the case stays RT only when exact `X`, exact `Y`, and `v : X -> Y` are identified, their EntityOfConcern is the same, and every relied-on correspondence is an exact governed occurrence. The visible row and correspondence record are not those governed correspondence occurrences.

### A.6.3.RT:5.2.b - Same-concern diagram-to-structured-notation shift {#same-concern-diagram-to-structured-notation-shift}

**Source diagram.** `CoolingLoop -> Sensor A; CoolingLoop -> Valve B`

**Target notation.** `dependsOn(CoolingLoop, SensorA)` and `dependsOn(CoolingLoop, ValveB)`

This remains RT when the notation carries the same two source connection claims and adds no dependency theory. If `dependsOn` has stronger semantics than the source arrows, that added claim must be removed or separately established.

### A.6.3.RT:5.2.c - Functional-description diagram, table, or screen shift {#functional-description-diagram-table-or-screen-shift}

A source description says that a mixing cell transfers liquid from Tank A through heat exchanger H-2 to reactor R-4, while keeping instrumentation and control claims outside. A target table foregrounds the transfer path. This remains RT only while the same functional slice is represented without adding performed-work order, module structure, evidence, gate passage, or control architecture.

Explanatory diagram order is not physical time or Work order unless the source states that temporal claim. OCR or parsing that merely extracts pixels, text, or layout starts with A.7. If the target becomes honest only by omitting exceptions, confidence bands, or source distinctions under a narrower use, use A.6.3.CSC.

### A.6.3.RT:5.3 - Boundary to textual rewrite {#boundary-to-textual-rewrite}

A prose note is shortened, reordered, or translated but remains in the same textual regime. Use A.6.3.CR rather than inventing RT.

### A.6.3.RT:5.4 - Boundary to explanation-facing rendering {#boundary-to-explanation-facing-rendering}

A representation is changed mainly to teach or explain an existing face. E.17.EFP is primary; RT remains only for a separately material scheme transition.

### A.6.3.RT:5.4.a - Boundary to bridge-bearing comparison {#boundary-to-bridge-bearing-comparison}

A local reliability note about Pump P-2 becomes a comparison claiming operational equivalence with Unit U-7 in another plant. That is not merely representation change. Keep any local representation delta in RT. Under F.9, first resolve the two exact F.17 `SchemeSenseCell` values and test that a Bridge obtains; then state the separate C.2.1 bounded-use claim for this equivalence or substitution use.

### A.6.3.RT:5.4.b - Boundary to carrier work {#boundary-to-carrier-work}

A table is exported as CSV and dashboard PNG after its representation scheme was chosen. The later Work produces the CSV and PNG carriers by formatting, exporting, packaging, or rendering the already chosen representation; it is not another RT merely because the visible form changed.

### A.6.3.RT:5.4.c - Boundary to coarsened dashboard view {#boundary-to-coarsened-dashboard-view}

An incident worksheet carries three causal branches, two confidence bands, and an open ambiguity; a dashboard tile foregrounds only cache-failover evidence. If the tile needs a declared narrower use, non-admissible action, and explicit return to the worksheet, A.6.3.CSC is primary. The tile is not causal proof, service-status verdict, or action cue.

### A.6.3.RT:5.4.d - Boundary to structure-to-narrative rendering {#boundary-to-structure-to-narrative-rendering}

**Source structure.** `Architecture candidate C-2 has module split M, data-custody constraint D, placement constraint P, and unresolved latency versus maintainability trade-off T.`

**Unsupported narrative.** `The team first tried to preserve M, then found that D forced P, so C-2 accepts latency residual T to preserve maintainability.`

This adds an earlier attempt by the team, a discovery with the claim that D forced P, and a decision resolving the source's still-unresolved trade-off.

**Source-faithful reader ordering.** `To examine C-2, first consider module split M, then data-custody constraint D and placement constraint P; finally consider the unresolved latency-versus-maintainability trade-off T.`

The source-faithful alternative orders the selected structures into a reader path; “first”, “then”, and “finally” describe that reading order, not a history of design Work. Apply A.6.3.NAR for ordering, connective account, preservation/loss, use, and source return. Use RT only for a remaining representation-scheme shift that does not depend on that narrative ordering.

### A.6.3.RT:5.5 - Guarded decode-mediated rendering {#guarded-decode-mediated-rendering}

Probe run P-8 is tied to model-state log M-12 and evaluation bundle EV-4. If their source material concerns one independently identified failure episode, a decoded rendering may suggest a cluster corresponding to that same episode. Until the decoding/access relation and recoverability evidence support a named stronger use, keep the result exploratory and report-only. A latent region, feature cluster, probe result, source publication, or readable output fills no episteme endpoint.

## A.6.3.RT:6 - Bias-Annotation {#bias-annotation}

| Bias | Countermove |
| --- | --- |
| Harmless-format bias | Compare source and target for reasoning affordances, loss, and added claims. |
| Formality-first bias | Produce the useful target and compact note before opening exact endpoints or an occurrence. |
| Ontology-by-notation bias | Treat geometry, rows, edges, embeddings, and decoder output as representations until an independent ontology claim is established. |
| Clarity-authority bias | Do not let a cleaner target widen evidence, reliability, assurance, gate, or work authority. |
| Decode-givenness bias | Require explicit decoding access and recoverability evidence for the declared use. |
| Object-collapse bias | Keep exact construction, relation occurrence, performed Work, occurrence-description episteme, publication, form, and carrier distinct. |

## A.6.3.RT:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Why it fails | Repair move |
| --- | --- | --- |
| Endpoint dossier before target | Ordinary work stalls before a useful table, diagram, or notation exists. | Produce the target and source comparison first; open exact identities only at a named receiving-use trigger. |
| Every format shift is harmless | Representation changes alter inspection, salience, and recoverability. | State the practical representation/reasoning delta and compare source with target. |
| Scheme, semiotic mode, and viewpoint collapsed | Users cannot tell what changed or which claim needs review. | Name only the distinction that changes use, and keep viewpoint under E.17.0 when it is current. |
| Notation becomes ontology | Geometry or notation appears to define the world. | Point every target-side relation back to source claims or establish the new ontology claim separately. |
| Occurrence description treated as occurrence | A changed description, publication, layout, or carrier appears to change relation identity. | Keep six-participant identity on the occurrence and identify the description under C.2.1. |
| Retargeting hidden as representation | A changed EntityOfConcern is mislabeled as same-concern conversion. | Use A.6.4 when the concern changes. |
| Latent case first | Decode demands overwhelm the ordinary representation task. | Keep latent use exploratory until decoding access and recovery evidence are explicit. |

## A.6.3.RT:10 - Rationale {#rationale}

Representation changes are neither always cosmetic nor always new ontology. The reusable move is to preserve practical content for a use, expose the changed reasoning medium, and keep loss and return honest. Exact `v : X -> Y` is the stronger claim-level description when needed; the six-participant occurrence is later-specific evidence about actual transition Work, not the entrance fee for changing prose into a table.

An expression can help obtain a result by keeping relevant parts available for joint inspection or manipulation. This benefit depends on its arrangement, the permitted operations and the user's preparation. Comparing the expression with its source protects the givens while the subject Method develops the construction or argument. E.5.2 keeps the meaning portable when another notation is used; portability leaves the effort and available reasoning operations to be compared.

## A.6.3.RT:11 - SoTA-Echoing {#sota-echoing}

**Practice question.** How can a practitioner change a representation so that it supports the next operation while retaining the source distinctions on which that operation depends?

**Selected answer and alternative.** Adopt comparison directed by the receiving use: identify the source and target meanings, make the target, inspect the relations the use needs, and expose loss and return. Adapt operative-expression construction to the same comparison. A serious default is conversion followed by a syntax, format-conformance or readability check. That default is sufficient for a carrier-only change when an established semantic contract already covers the required preservation. It is insufficient when the conversion can change the represented claim.

Compare the answers with the same source, target, reader preparation and requested operation. For example, `A then (B or C)` and `(A then B) or C` use the same labels and can both be well formed. Checking the represented dependency finds that only the first requires A before either continuation. The comparison in §4.1 asks the reader to inspect that dependency; a format or readability check can leave it unexamined. The selected answer spends effort on the distinction that changes the next action. It accepts that additional comparison cost rather than promising a cheaper conversion. Reuse an applicable semantic-preservation result when one already answers the receiving question.

Preparing an operative expression adds a second useful choice. In §5.1.a, keeping the same segments identifiable as radii and triangle sides supports the geometric argument; in §5.1.b, coordinating syllables with the hand cycle supports the rhythmic construction. A polished copy with those relationships hard to recover can preserve individual labels while remaining unsuitable for the operation. The cases justify trying the intended operation when that trial can decide usefulness, with its subject rules and preparation stated. They do not rank one medium above all others.

**How the choice shapes RT.** Section 4.1 combines target construction with source comparison and a conditional trial of the intended operation. Section 4.3 states the source and target semantics for a stronger preservation claim; §4.5 exposes loss and decoding assumptions. CC-RT-1 and CC-RT-13 check these moves, and §5 shows their use. This choice rejects syntax, visual appeal or decoder fluency as sufficient evidence of semantic preservation. Technical translation or causal-intervention claims require the semantics and tests appropriate to those claims; the ordinary comparison in §4.1 remains available when the practitioner needs none of them.

**Reopen this choice** if a target accepted by this procedure loses a dependency, timing relation or uncertainty distinction needed by the declared use; if a changed decoding assumption defeats the claimed recovery; or if an alternative preserves those distinctions and supports the same operation with less preparation or comparison effort. Revisit the affected branch and source comparison.


| Source and role in the comparison | Adopted move | Rejected overread | Practical effect in RT |
| --- | --- | --- | --- |
| Danielle Macbeth, [“Seeing How It Goes: Paper-and-Pencil Reasoning in Mathematical Practice”](https://doi.org/10.1093/philmat/nkr006), 2011, especially pp. 16-18 and 31-42; Catarina Dutilh Novaes, *Formal Languages in Logic: A Philosophical and Cognitive Analysis*, 2012, §§3.2, 5.2 and 6.1. Conceptual basis for the selected operative-expression line. | Prepare expressions, preserve common parts across useful groupings, and connect manipulation with interpretation and learned capabilities. | An expression is only a secondary illustration, or a semantically equivalent notation offers the same reasoning operations and effort to every user. | Grounds target construction and the Euclidean example. These arguments support the operation; they supply no measured learning gain for this pattern. |
| David P. Nelson, *Solkattu Manual: An Introduction to the Rhythmic Language of South Indian Music*, 2008, exercise 7. Constructive case supporting the vocal-gestural application of that line. | Coordinate syllable durations with a learned hand cycle and construct a phrase ending at a cycle boundary. | A symbolic or calculated alignment establishes a particular performer's fluency. | Supplies the duration assignments and six-pulse preparation in §5.1.b; the representation and the performance have separately assessable uses. |
| Stefan Hallerstede and John Hatcliff, “A mechanized semantics for component-based systems in the HAMR AADL runtime” (2025), DOI `10.1016/j.scico.2025.103312`; Jason Belt et al., “Model-driven development for the seL4 microkernel using the HAMR framework” (2023), DOI `10.1016/j.sysarc.2022.102789`, including the applied unmanned-aircraft case. Candidate basis for explicit semantic preservation in technical translations. | Prefer explicit source and target semantics, machine-checkable translation, named preserved properties, and an exercised analysis, verification, or generation path over language or diagram status. | An architecture-language label, visual model, code generator, verified platform, or standard conformance by itself proves lossless same-concern continuity, whole-system validity, or downstream authority. | Grounds technical model-to-analysis and model-to-implementation cases: state the exact source/target meanings, translation, checked property, residual loss, bounded use, and return. |
| Jonatan Reyes, Mina Massoumi, Anil Ufuk Batmaz, and Marta Kersten-Oertel, “Shades of Uncertainty: How AI Uncertainty Visualizations Affect Trust in Alzheimer's Predictions” (2026), current preprint `arXiv:2602.01264`; two bounded studies with 37 general participants and 10 experts. Evidence that uncertainty encoding and audience can change reported confidence and perceived reliability. | Record audience- and encoding-sensitive changes in confidence, perceived reliability, and recognition of limits. | A vivid or continuous display is automatically more truthful, action-ready, or settled cross-domain evidence. | Supports revisiting the comparison when a different encoding or audience changes the interpretation of uncertainty. The two studies do not establish a universal RT rule. |
| Chinh Hoang and Mohammad Rashedul Hasan, “The Abstraction Gap in Vision-Language Causal Reasoning” (2026), current preprint `arXiv:2605.28779`; a CAGE benchmark report used as failure evidence for fluency-only comparison. | Separate fluent target text from faithful causal-chain preservation. | Readability establishes causal fidelity, evidence, ontology, or a settled universal theory of representation change. | Supplies a benchmarked fluency-versus-causal-chain warning for the source-comparison and report-only boundary of generated or decoded explanations. |
| Atticus Geiger et al., “Causal Abstraction: A Theoretical Foundation for Mechanistic Interpretability” (JMLR 26, 2025), together with Denis Sutter, Julian Minder, Thomas Hofmann, and Tiago Pimentel, [“The Non-Linear Representation Dilemma: Is Causal Abstraction Enough for Mechanistic Interpretability?”](https://proceedings.neurips.cc/paper_files/paper/2025/hash/dbb98528c9870377f3f0d133aae6050b-Abstract-Conference.html) (NeurIPS 2025). The first supplies a mapping-and-intervention approach; the second supplies a counterexample to unrestricted alignment. | Adopt explicit mapping and intervention tests, bounded by assumptions about information encoding. Sutter et al. show that sufficiently powerful alignment maps can fit an algorithm even when the model cannot perform its task. Mapping accuracy therefore needs to be judged together with what the map itself computes. | An alignment score alone establishes that the model implements the proposed algorithm. | In §4.5.c, state the decoding relation and the recovery it supports for the intended use. When that use asserts a model's mechanism, reopen the claim if the fitted map supplies the computation attributed to the model. |

The domain studies support the named comparisons within their stated tasks and evidence. RT adopts their source-comparison questions and adapts the burden to the receiving use; it leaves the subject's construction, intervention, learning and reliance claims to their own methods.



## A.6.3.RT:12a - Boundary with quantum-like state-representation shortcuts {#boundary-with-quantum-like-state-representation-shortcuts}

Use RT when the primary move is the same-concern shift from one state representation to another: state vector to typed description, fuller model to quantized record, or one notation to another. Start with the ordinary representation note: content to survive, shortcut representation, loss, use, and return.

Add the following only when the shortcut's claim requires it:

1. source and receiving schemes and the same EntityOfConcern;
2. representation-factor, reasoning-medium, salience, topology, actionability, calibration, or interaction delta that matters;
3. decoding relation and recovery evidence;
4. causal- or approximate-causal-abstraction mapping when action, intervention, manipulation, or cross-abstraction structure is claimed; and
5. the exact C.26 cue and bounded use when a quantum-like state-representation claim is actually current.

| Ordinary shortcut note | Question |
| --- | --- |
| Source and content | Which fuller representation or evidence set carries the distinctions? |
| Shortcut | Which cheaper, typed, quantized, symbolic, or lower-detail representation is used? |
| Loss | Which precision or expressivity is lost, and which compatibility, recovery, or evidence relation is not carried? |
| Admissible use | Which use remains admissible—for decision, explanation, triage, comparison, or action selection? |
| Return | Which dispute, stronger-use demand, evidence gap, or recovery failure sends the user back to the fuller representation? |

For a shortcut with the declared QL cue, apply C.26:12b to the receiving use. A conditional comparison or explanation under the same assumptions can retain its sufficient account. Prediction, model adoption or a comparative-performance claim needs the applicable adequacy account; reuse existing support and obtain only the missing contribution. Reuse or formal notation alone does not require a fuller record. Do not describe ordinary compression, low-bit implementation, diagramming, or representation learning as quantum-like without a claim-bearing formal cue.

## A.6.3.RT:12b - C.29 mathematical-lens use relation {#c-29-mathematical-lens-use-relation}

When RT imports a contested or claim-bearing mathematical lens, RT still carries source/target schemes, same-EntityOfConcern construction, preservation, loss, and return. Cite the applicable C.29 output only for adequacy of that mathematical lens. C.29 neither replaces the RT account nor broadens it into bridge, evidence, or causal authority.


## A.6.3.RT:End {#end}
