# E.8.ECSPF - Author an FPF Pattern from an Accepted Evaluation CharacteristicSpace Specification: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## E.8.ECSPF:5 - Archetypal Grounding {#archetypal-grounding}

**Tell.** Guidance based on an evaluation `CharacteristicSpace` becomes reusable in FPF only when a practitioner can recognize the evaluated object and use before reading the coordinate table. The publication form must teach the evaluation use, not merely list the values. The following slice shows the author's move from an accepted specification to practitioner-facing content.

**Accepted specification.** An author has an accepted `EvaluationCharacteristicSpaceSpec` for one version of a field-service handover instruction.

| Accepted value | Selected content |
|---|---|
| Evaluated object and use | One field-service handover instruction version, judged for readiness for a supervised first use. |
| Working reader and qualification window | A maintenance lead who did not author the instruction; the result remains qualified only while the named equipment configuration and safety-procedure edition remain unchanged. |
| Discriminating cases | A usable handover instruction; an instruction of the same kind that hides its stop condition; and a spare-parts catalogue, which is outside the evaluated object kind. |
| `FirstMoveRecoverability` | `0`: the first move cannot be found; `1`: it can be recovered only with author help or an undeclared source; `2`: the working reader can state and carry out the first move from the instruction. |
| `HazardBoundaryVisibility` | `0`: the hazard or stop boundary is absent; `1`: it is recoverable only by chasing another source; `2`: it appears before the first move and says when to stop or escalate. |
| Evidence and missingness | Observe one cold-reader trial and cite the instruction locus used for each value. An unchecked coordinate is `missing` and cannot be treated as `2`. |
| Result and trade-off | Each row contains coordinate, value, adjacent-value rationale, evidence locus, and missingness. Improving first-move wording must not hide or weaken the hazard boundary. |
| Status and stop | `ready for supervised use` requires `2` on both coordinates with current evidence. Otherwise return `repair`. Reopen after an equipment-configuration or safety-procedure change. |

**Corresponding recognition lines in the authored pattern.**

> Use this pattern when you must decide whether a field-service handover instruction is ready for a supervised first use by a maintenance lead who did not write it. Use it only for the named equipment configuration and safety-procedure edition. First give the current instruction to that reader and ask them to identify the first move and the condition that requires stopping or escalation. A spare-parts catalogue is outside this evaluation.

These lines carry the selected object kind, use, reader, qualification window, first move, and wrong-kind boundary. Merely writing “see `A.19.ECS`” would not.

**Minimal Solution and result form.** The pattern then tells the practitioner to use the current instruction version, observe the cold-reader trial, judge both coordinates from their stated value meanings, and record both rows. For example:

| Coordinate | Value | Adjacent-value rationale | Evidence locus | Missingness |
|---|---:|---|---|---|
| `FirstMoveRecoverability` | `2` | `1` would understate independent recovery; no higher value exists. | Opening instruction and observed first move. | checked |
| `HazardBoundaryVisibility` | `1` | `0` would ignore the recoverable safety reference; `2` would overstate visibility before action. | Safety reference after the first action. | checked |

The returned status is `repair`, because one coordinate remains below its declared ready value. If both checked rows were `2`, the instruction would reach `ready for supervised use`; a spare-parts catalogue would return to evaluation selection before these rows were opened. A simple `A.10` citation is enough to locate the evidence-use discipline for this ordinary case; a particular assertion or `ClaimGraph` is needed only if later interpretation or reuse depends on that identity.

**Near miss, proxy improvement.** An editor shortens the instruction so the first move is easier to find, but deletes the visible stop condition. `FirstMoveRecoverability` rises to `2` while `HazardBoundaryVisibility` falls to `0`. The author must not add or average those ordinal values and call the rewrite better. The protected safety trade-off has been lost, so the pattern returns `repair` and the accepted specification must be reopened if its current status rule would reward that rewrite.

**Show, pattern-quality evaluation.** `E.21` is an evaluation for one FPF pattern version. Its publication form must still open with the working question "is this pattern good enough for the declared use?" before showing coordinates such as first-action recoverability, boundary fit, and SoTA binding.

**Show, local rubric that should not become an FPF pattern.** A project team defines a temporary rubric for choosing a meeting room. The `A.19.ECS` specification may be adequate locally, but no durable FPF pattern is needed because the evaluated object kind and use do not recur across FPF practice.

**Show, object-kind boundary.** A nuclear-plant evaluation can judge nuclear plants and declared comparable power-generation alternatives. A plant inspection report can supply evidence about the plant but is outside that evaluated-object kind: before the evaluation is opened, select a suitable evaluation; after a forced invocation, record an object-kind-fit defect/value rather than treating it as a weak nuclear plant or skipping declared coordinates. The pattern publication form must show that boundary before readers try to use the coordinate table.

## E.8.ECSPF:6 - Bias-Annotation {#bias-annotation}

Evaluation-characteristic-space patterns are vulnerable to domain-example bias: the first examples can silently choose the evaluated object kind, use, and value family for later readers. A conforming publication form names known skew in examples, sources, reader family, domain tradition, measurement preference, benchmark preference, or FPF-internal reuse. When the evaluation claims broad use, the case bank must include heterogeneous evaluated object situations or explicitly narrow the claim.

## E.8.ECSPF:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Symptom | Repair |
|---|---|---|
| **Score-sheet pattern.** | The pattern is mostly a table of values. | Move evaluated object kind, use, first evaluation use, FPF-publication boundary, and practical consequence into recognition text before the table. |
| **Checklist-as-solution.** | Users are told only what must be checked. | Put the actual evaluation method and record shape in `Solution`; let checklist rows verify it. |
| **Publication-form/content collapse.** | The accepted specification, its `CharacteristicSpace`, the pattern, the evaluated object, the later evaluation, and its result are treated as one thing. | State what each is and show that the pattern teaches the accepted specification; none of the other objects becomes the pattern. |
| **Positive-only case bank.** | Every example passes. | Add below-floor and outside-declared-object-kind boundary cases. |
| **Undeclared total.** | Ordinal coordinate values are added, averaged, or collapsed into an “overall score”. | Keep the coordinates visible; if a bounded scalarization is separately admitted, name its method, use, any information loss, applicability, and stop or return condition. |
| **Proxy improvement.** | A visible coordinate rises while a protected value becomes worse, yet the result is called improved. | Compare the changed values and protected trade-offs; stop or reopen when the evaluation rewards the loss. |
| **Related-pattern authority theft.** | The pattern claims authority over evidence, assurance, a gate or release decision, measurement, naming, or improvement. | Cite the applicable pattern and state the concrete contribution used here; keep only the evaluation claim in this pattern. |
| **Rubric promotion.** | A local rubric becomes an FPF pattern because it was useful once. | Keep it local unless durable FPF reuse and evaluated-object scope are established and every outside claim names the applicable pattern and its contribution. |
| **Frozen evaluation publication form.** | The evaluated EntityOfConcern kind, use, use of a cited source, source adoption/adaptation/rejection decision, or coordinate meanings change, but the pattern keeps the old values as if still current. | Reopen A.19.ECS for the changed evaluation specification. Establish whether earlier results remain comparable under the declared basis, need a justified transformation or new evaluation, or no longer support this use. Assert an F.9 Bridge only when its own two-sense relation is needed and obtains. |
| **Report-shaped evaluation pattern.** | The pattern publishes coordinate names but leaves the returned result as a narrative, score list, or two-column table. | Add a result-form block: coordinate, value, short rationale, evidence basis, and coordinate-specific payload where needed. |
| **Pattern-quality report as evaluation pattern.** | `E.21` status, all-`4` or all-`5` posture, corpus projection, retrieval evidence, README, ToC, E.11, and I.2 alignment, monolith parity, landing readiness, or author or reviewer turn correspondence appears anywhere in the pattern as if it were the evaluation method. | Move that evidence to the quality, review, projection, or release carrier and keep the pattern body focused on the evaluation for the declared evaluated object kind. |
| **Apparatus-overwrapped publication form.** | The evaluation relation is written through ambiguous role, carrier, locus, flow, status, or package words that add no evaluated object kind, coordinate meaning, evidence rule, user-facing action, or exact flow position. | Apply `F.19`; if remaining content still hides a word, head, or use, apply `E.10`, `E.10.ARCH`, `F.18`, or the pattern that defines the affected object or relation. |

## E.8.ECSPF:10 - Rationale {#rationale}

The split between `A.19.ECS` and `E.8.ECSPF` preserves the distinction between an evaluation characteristic-space specification, the pattern that teaches its use, a later evaluation, and the resulting record. `A.19.ECS` says what the specification must contain. `E.8.ECSPF` says how to carry that accepted content into an FPF pattern when durable publication is selected. This prevents two symmetric mistakes: stuffing FPF pattern-format requirements into a general characteristic-space construction method, and publishing guidance whose accepted coordinate set is not recoverable by value.

## E.8.ECSPF:11 - SoTA-Echoing {#sota-echoing}

**Source-use convention and qualification.** The current-source decisions below are qualified through 2026-08-15 for the identified editions and this publication-form question. Each source is used only for the content named in its row. Reopen the smallest affected row when a new edition, successor, or materially better competitor changes that adopted content, its scope, or its currentness; a bibliographic change alone does not reopen the pattern.

| Source and stable identity | Adopted content | Change made here | Boundary | Reopen condition |
|---|---|---|---|---|
| [*BenchmarkCards: Large Language Model and Risk Reporting* (arXiv:2410.12974)](https://arxiv.org/abs/2410.12974) | Structured documentation of benchmark properties, including targeted risks and evaluation methodology, to support informed benchmark selection. | When published evaluation guidance relies on a benchmark, its source basis identifies the benchmark properties that affect coordinate or evidence selection. | BenchmarkCards documents benchmark properties. It does not define the whole evaluation process or prescribe how to measure and interpret a result. | Reopen this use if a successor changes which benchmark properties are needed for informed selection. |
| [*Evaluation Cards: An Interpretive Layer for AI Evaluation Reporting* (arXiv:2606.09809)](https://arxiv.org/abs/2606.09809) | Composition of benchmark metadata, evaluation-run data, and model metadata into one interpretable reporting layer, with reader-sensitive interpretation. | The publication form keeps benchmark description, run evidence, evaluated-object metadata, and the evaluation result distinguishable when those values are required. | This is the 2026 *Evaluation Cards* paper. A separate 2025 proposal called *EvalCards* is not a source here unless its content is deliberately selected and identified. | Reopen if the reporting layers or their interpretive use materially change. |
| [*Holistic Evaluation of Language Models* (HELM, arXiv:2211.09110)](https://arxiv.org/abs/2211.09110) | Standardized scenario-and-metric comparison, multi-metric visibility, stated coverage and missingness, and inspectable prompts and completions. | The pattern publishes the declared scenario or use, metric or coordinate meanings, missingness, and evidence needed for comparison instead of a bare aggregate. | HELM is a language-model evaluation suite, not a general FPF publication method. | Reopen if HELM's comparison discipline is superseded for the adopted scenario, metric, or evidence use. |
| [*VHELM: A Holistic Evaluation of Vision Language Models* (arXiv:2410.07112)](https://arxiv.org/abs/2410.07112) | The HELM comparison discipline extended to vision-language models, with modality-relevant aspects and standardized prompting, inference, metrics, and released generations. | A claimed cross-modality evaluation must publish the modality-specific use, procedure, and evidence that actually affect its coordinates. | Only the vision-language extension is adopted; VHELM does not justify claims about every evaluated object or modality. | Reopen if a successor changes the adopted vision-language procedure or exposes a missing modality boundary. |
| [*AHELM: A Holistic Evaluation of Audio-Language Models* (arXiv:2508.21376)](https://arxiv.org/abs/2508.21376) | The HELM comparison discipline extended to audio-language models across audio-relevant aspects, with standardized prompts, inference parameters, metrics, and released outputs. | An audio-language evaluation must publish the audio-specific use, procedure, and evidence that change its coordinates. | AHELM is an audio-language source, not an agent-evaluation source and not evidence for unrelated modalities. | Reopen if a successor changes the adopted audio-language procedure or exposes a missing audio boundary. |
| [*A survey on Quality-Diversity optimization: Approaches, applications, and challenges* (2026, DOI 10.1016/j.swevo.2025.102240)](https://doi.org/10.1016/j.swevo.2025.102240) | Current overview, for this narrow question, of QD feature or descriptor spaces, local quality and objective heads, diversity, containers, comparison or dominance, and evaluation metrics. | The publication form keeps dimensions, comparison rules, and protected trade-offs visible when an aggregate would hide loss. | QD is optimization over a declared feature space, not a universal evaluation architecture. A bounded scalarization remains separately declared with its use, loss, and non-use boundary. | Reopen if a newer synthesis changes the QD comparison used here or if this pattern claims more than the narrow non-scalar lesson. |

Model-card literature and classic pattern-language literature remain historical lineage for intended-use reporting and action-guiding publication. The retained publication lesson is concrete: put recognition and the first evaluation use before coordinate tables. This lineage is not presented as current-best evidence for the question. Current FPF `E.8` supplies the internal authoring rule and is not an external SoTA source.


## E.8.ECSPF:End {#end}
