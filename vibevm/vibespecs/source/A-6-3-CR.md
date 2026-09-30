# A.6.3.CR - ConservativeRetextualization: EntityOfConcern-Preserving Textual Re-Expression: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## A.6.3.CR:5 - Archetypal Grounding {#archetypal-grounding}

### A.6.3.CR:5.1 - Same-EntityOfConcern report rewrite {#same-entityofconcern-report-rewrite}
**Source note slice.** `Service S exceeded the latency threshold in the evening batch window. Trace T-44 and dashboard pin D-17 show the spike. Two low-confidence hypotheses remain open.`

**Published report slice.** `Evening-batch latency for Service S exceeded the threshold. Source pins: Trace T-44, Dashboard D-17. Low-confidence hypotheses are omitted here and remain in the pinned source note.`

This is an admissible direct `ConservativeRetextualization` because the EntityOfConcern stays fixed, the report remains textual, and the omission is stated rather than hidden. In ordinary internal use, this often needs only source pins plus visible omission notes rather than a full explicit review record.

### A.6.3.CR:5.1.a - Ordinary inherited-pin summary {#ordinary-inherited-pin-summary}
**Pinned source cluster.** `In this example, N-14 is the source note in §5.1; N-14, trace T-44, and dashboard card D-17 are already published together under one incident review bundle.`

**Published stand-up slice.** `Evening-batch latency exceeded the threshold for Service S. See N-14 / T-44 / D-17 for the pinned source cluster.`

This is still an admissible ordinary case even though the short stand-up slice does not restate every pin and qualifier inline. The didactic point is that lightweight use may inherit already-published pins and provenance when the tether stays visible to the reader.

### A.6.3.CR:5.1.b - Benign omission that stays ordinary {#benign-omission-that-stays-ordinary}
**Source note slice.** `Service S exceeded the latency threshold in the evening batch window. Trace T-44 and dashboard pin D-17 show the spike. The note also lists two low-confidence hypotheses for separate investigation.`

**Published stand-up slice.** `Evening-batch latency for Service S exceeded the threshold. Source pins: T-44, D-17. Low-confidence hypotheses are omitted from this stand-up note and remain in the pinned source.`

This stays ordinary `ConservativeRetextualization` because the omission is declared, the same EntityOfConcern remains visible, and no separate narrower admissible use, non-admissible downstream use, or source-bearing return is needed to justify the omission. Ordinary omission alone is not controlled semantic coarsening.

### A.6.3.CR:5.1.c - Functional-description textual summary {#functional-description-textual-summary}

**Source note slice.** `The principle scheme says: choose method family MF-2 for small-batch mixing when material X remains below threshold T; selected method M-2 still requires work plan WP-17 and result measurement RM-4.`

**Published summary slice.** `For small-batch mixing, choose method family MF-2 when material X remains below T. Selected method M-2 still requires work plan WP-17 and result measurement RM-4.`

This remains `ConservativeRetextualization` because it is a textual restatement of the same source-episteme claims and it keeps the work-planning and result-measurement requirements visible. It is admissible for interpretation and source-finding. It does not by itself provide performed `U.Work`, evidence, gate passage, engineering justification, or control architecture. If the summary drops WP-17 or RM-4, or makes the selected method look executable by summary alone, restore those requirements before presenting it as a faithful summary or executable guidance. A deliberately coarsened version needs `A.6.3.CSC Controlled Semantic Coarsening` with narrower admissible use, forbidden stronger use, and source-bearing return. For stronger use, apply the exact governing requirement to the current facts; the CSC label or a reference alone does not satisfy it.

### A.6.3.CR:5.1.d - Generated-summary source-relation variant {#generated-summary-source-relation-variant}

A generated or machine-assisted summary may stay in `ConservativeRetextualization` only when it remains an entityOfConcernRef-preserving textual re-expression and its source relation is visible enough for the intended use. This is the ordinary LLM-generated-summary case: a model-produced paragraph over a pinned inspection note, method-selection note, safety note, incident note, or other source slice is not automatically `ExplanationFaithfulnessProfile` merely because it was generated; it remains `ConservativeRetextualization` only while it restates source claims and leaves omissions, loss, and non-admissible uses visible. Ordinary source-finding use can stay light; use the compact variant below when the summary will be reused, cited, disputed, or relied on.

| Source-relation question | CR-local meaning |
| --- | --- |
| source pointer present | The summary points to the source slice or source bundle it claims to restate. |
| source actually used | The inspectable source relation shows that the generation or rewrite actually used the named source, not merely a similar topic or remembered background. If that relation is unavailable, source use remains unresolved; retain only the justified source-pointer or orientation use until the relation is recovered. |
| claim recoverable from source | Each claim-bearing summary claim can be recovered from the source slice or declared correspondence witness. |
| claim merely plausible | A sentence sounds likely but is not recoverable from the source. Do not present it as source-backed: retain only a justified source-finding or orientation pointer, or explicitly separate the unsupported proposition and repair it or handle it under the pattern for the new claim. |
| omission or loss | Relevant omitted qualifiers, alternatives, caveats, uncertainty, or conditions are visible enough for the admissible use. |
| claim widening | The summary does not turn possibility, hypothesis, bounded scope, or low-confidence wording into a wider commitment. |
| added linkage | New causal, bridge, comparison, work, gate, evidence, or explanation links are not introduced as if they were in the source. |

When the generated-summary case needs shared vocabulary, use only the `E.17:5.1b` source-relation or bounded-use distinction that changes the present use. Keep claim recoverability from the source separate from admissibility for that use, and an unknown relation separate from one known absent. The same source governs independent-verification claims and reopen conditions.

The summary may expose or cite the source slice it restates. It does not become that source slice by fluency, brevity, translation, layout, generated form, or reuse. If the needed source content, governing requirement, or case relation is missing, a repair request or source-gap note is only prospective: it neither establishes earlier source use nor supplies the missing claim support or use condition.

If the generated summary is source-pointer-only, merely plausible, claim-widened, or carrying added linkage, do not treat it as a conservative source-equivalent summary. For source-finding or orientation, retain only the justified pointer and separate any unsupported or new proposition from the source-backed account. Repair the claim against the source, or apply A.6.3.CSC, ExplanationFaithfulnessProfile, RepresentationSchemeTransition, E.17.ID.CR, A.15, A.10, or another pattern that defines, constrains, or tests the actual claim. An orientation or coarsening label alone does not make an unsupported claim source-faithful.

### A.6.3.CR:5.2 - Same-EntityOfConcern rewrite via declared correspondence {#same-entityofconcern-rewrite-via-declared-correspondence}

**Source design slice.** `Cooling loop CL-2 preserves safe temperature margins during standard operating demand.`

**Source safety slice.** `Cooling loop CL-2 maintains the temperature condition required for hazard-control claim HC-7 during standard operating demand.`

**Published joint-review slice.** `For standard operating demand, Cooling loop CL-2 is described in both the design and safety views as maintaining the required temperature condition. This summary relies on CorrespondenceModel CM-12 and does not add claims beyond that declared overlap.`

The synthesis may stay in this pattern only if the source relation remains explicit, every downstream claim remains recoverable to the design slice, the safety slice, or the declared `CorrespondenceModel`, and the text does not silently widen claims beyond the declared entityOfConcernRef-preserving overlap. Because this case requires a correspondence witness, a fuller review record is usually warranted.

### A.6.3.CR:5.2.b - Cross-language re-expression without hidden bridge work {#cross-language-re-expression-without-hidden-bridge-work}
**Source slice.** `The backup controller stays in passive watch mode until the primary loop fails two consecutive heartbeat checks.`

**Published slice.** `Резервный контроллер остаётся в режиме пассивного наблюдения, пока основной контур не провалит две последовательные проверки heartbeat.`

**English reader gloss (comprehension aid only).** `The backup controller remains in passive observation mode until the primary loop fails two consecutive heartbeat checks.`

The gloss helps an English-only reader follow the example and find the claim being re-expressed. It is a comprehension aid, not a second source or verification of the Russian translation. A conservativity claim still requires suitable language competence or other evidence for the same-claim, same-EntityOfConcern, and hidden-bridge tests.

This remains in `ConservativeRetextualization` only if the translation is tethered to the same source claim, preserves the same EntityOfConcern, and adds no claim beyond the source. Apply F.9 only when a semantic Bridge between local senses or a proposed bounded use of that Bridge is claimed.

### A.6.3.CR:5.2.c - Boundary to controlled coarsening {#boundary-to-controlled-coarsening}
**Source slice.** `Vendor bulletin VB-7 requires rollback when pressure drift exceeds 2.5%, and it keeps two equipment-specific exceptions in the pinned annex.`

**Published coarsened slice.** `Pressure drift above 2.5% is a warning condition in the bulletin. Check the pinned bulletin and annex before treating the note as rollback guidance.`

This does **not** remain ordinary `ConservativeRetextualization`. The coarsened slice drops equipment-specific exceptions and remains only an orientation warning: it is not an executable rollback command. It can stay honest only through narrower admissible use, non-admissible downstream use, and source-bearing return to the source-bearing bulletin. Once that narrower-use boundary becomes primary, the case leaves ordinary same-entity rewrite and must use `A.6.3.CSC Controlled Semantic Coarsening` rather than being treated as a harmless summary.

### A.6.3.CR:5.3 - Boundary to explanation-facing renderings {#boundary-to-explanation-facing-renderings}

A text is rewritten not mainly to restate the same source, but to explain why it matters, simplify reasoning for a learner, or narrate a mechanism. That move should leave `ConservativeRetextualization` and be reviewed under `ExplanationFaithfulnessProfile`.

### A.6.3.CR:5.4 - Boundary to representation-scheme transition {#boundary-to-representation-scheme-transition}
A prose note is rewritten as a table, matrix, diagram, latent representation, or distributed representation with a material representation-scheme change. Even if the EntityOfConcern stays fixed, this is not only a textual rewrite; it belongs with `RepresentationSchemeTransition`.

## A.6.3.CR:6 - Bias-Annotation {#bias-annotation}


This pattern intentionally biases toward same-entity conservativity and away from explanation or retargeting inflation. The main mitigation is to repair a preservation defect within CR when possible and apply `ExplanationFaithfulnessProfile`, `RepresentationSchemeTransition`, `A.6.4`, or the pattern that defines, constrains, or tests the actual changed claim or use when it requires leaving same-entity textual restatement.

## A.6.3.CR:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Why it is wrong | How to avoid it |
|---|---|---|
| Treating every summary as automatically conservative | summary demand hides omission and claim shift | publish loss and provenance discipline explicitly |
| Hiding correspondence in plain paraphrase | required correspondence witness disappears into prose | declare `CorrespondenceModelRef` when needed |
| Letting a rewrite become explanation | explanation work quietly becomes a textual "rewrite" | apply explanation governance once didactic or explanatory work dominates |
| Letting the EntityOfConcern shift by topic similarity | same topic is not the same EntityOfConcern | independently resolve the source and receiving `entityOfConcernRef` values; apply `A.6.4` if the resolved entities differ |

## A.6.3.CR:10 - Rationale {#rationale}

This pattern is worth splitting out because same-entity textual re-expression is common and useful. Keeping it under `A.6.3` as a named specialization keeps the boundary with neighboring transform families visible, makes a recurring authoring move easier to review, and preserves E.14’s working-model-first discipline for ordinary cases.

## A.6.3.CR:11 - SoTA Alignment: Adopted Invariants, Adapted Invariants, and Rejected Shortcuts {#sota-alignment-adopted-invariants-adapted-invariants-and}

**SoTA alignment rule.** Read each row here as source idea -> local FPF invariant -> practical local test -> popular shortcut rejected. A source citation governs nothing by reputation; it counts only when the cited idea is translated into the Solution, conformance checks, boundary rules, worked slices, and Relations of this pattern.

**Traditions covered.** This pattern binds itself to architecture-description governance, summarization factuality, translation-quality governance, and plain-language rewrite practice.

| Claim need | Source idea and current source | Current source reference | Local FPF invariant and practical local test | Adopted invariant, adapted invariant, and rejected shortcut |
|---|---|---|---|---|
| Conservative rewrite must stay visibly tied to the same source content rather than shifting through presentation fluency. | Architecture-description practice separates source publication, view, viewpoint, and required correspondence witness instead of letting rendered prose silently change the EntityOfConcern. | ISO/IEC/IEEE 42010:2022; source maturity = mature standard | `A.6.3.CR` keeps entityOfConcernRef-preserving textual restatement under `A.6.3`, applies `A.6.4` when the resolved EntityOfConcern changes, and keeps bridge relation work out of fluent rewrite. | **Adopt.** |
| Summary-like rewriting is not automatically harmless; factuality and faithfulness need source-sensitive checking. | Modern summarization work treats unsupported compression, strengthening, and hallucinated linkage as core failure modes rather than editorial noise. | Maynez et al. (2020), *On Faithfulness and Factuality in Abstractive Summarization*; source maturity = research paper as source for evaluation use | `A.6.3.CR` adopts that stance and adapts it to FPF by making omission, reliability assessment, and same-entity bounds explicit review concerns. | **Adopt and adapt.** |
| Translation quality is governed through declared quality aspects such as accuracy, omission, and addition rather than by fluency alone. | Translation-quality governance separates adequacy from text smoothness and requires explicit treatment of omission and addition error classes. | W3C Multidimensional Quality Metrics (MQM) Community Group and MQM issue-type framework: ongoing framework and community practice, with stable issue-type work and current attention to human, machine, and generative-AI translation quality evaluation. | `A.6.3.CR` adapts this by treating correspondence-mediated and cross-language rewrites as admissible only when loss, provenance, and same-entity bounds stay explicit. | **Adapt; source maturity = ongoing framework and community practice.** |
| Plain-language rewrite may improve readability, but it must not silently change commitments, scope, or force. | Plain-language standards favour reader-oriented rewriting while preserving the original commitments and conditions that matter for use. | ISO 24495-1:2023; source maturity = mature standard | `A.6.3.CR` adopts reader-oriented simplification for ordinary cases and rejects the popular shortcut that “plainer text” alone proves conservativity. | **Adopt and reject the popular shortcut.** |

**Architecture-description governance.** `A.6.3.CR` adopts the discipline that rendered text must stay visibly tied to a declared source publication or `U.View` line. It therefore rejects same-topic textual polish as sufficient evidence of entityOfConcernRef-preserving conservativity.

**Summarization factuality.** `A.6.3.CR` adapts modern factuality concerns into source-sensitive conservativity checking, including independent verification and reopening when those questions are live. Use `E.17:5.1b` for the source-relation and bounded-use distinctions needed by the case, keeping source recoverability separate from use admissibility; use `E.17:5.1c` for the shared use-boundary terms and `E.17:5.1d` to select the primary boundary. This pattern uses them only for entityOfConcernRef-preserving textual restatement.

**Translation and plain-language traditions.** `A.6.3.CR` adopts the reader-oriented value of translation and plain rewrite, but rejects the still-popular habit of treating cross-language or plain-language textual fluency as automatic proof that no new claim has been introduced. The W3C MQM source is used for issue-type and evaluation discipline, not as a brand-level warrant that a translated or rewritten sentence is source-equivalent.

**Local stance.** Best-known current practice motivates a narrow rule: entityOfConcernRef-preserving textual restatement is admissible only when source tether, loss, provenance, and same-entity bounds remain explicit enough that the reader can still tell what was preserved, what was omitted, when the rewrite has become a different claim, and which pattern to use next.


## A.6.3.CR:End {#end}
