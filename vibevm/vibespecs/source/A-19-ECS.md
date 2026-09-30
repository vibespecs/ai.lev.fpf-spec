# A.19.ECS - Evaluation CharacteristicSpace Construction: Define What Counts as Better: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## A.19.ECS:5 - Archetypal Grounding {#archetypal-grounding}

**Show, FPF pattern quality.** The evaluated object kind is one FPF pattern version. The existing evaluation is `E.21`, so `A.19.ECS` stays closed unless `E.21` itself is being redesigned. `E.23` may improve the pattern version under `E.21`.

**Show, DRR adequacy.** The evaluated object kind is one `DRR` version for a declared campaign-decision use. The existing evaluation is `E.9.DA`. If a campaign needs a different DRR adequacy coordinate, `A.19.ECS` can test whether that coordinate belongs inside `E.9.DA`, another evaluation, or no current FPF pattern.

**Show, FPF Pillar adequacy.** The evaluated object is FPF as a corpus or release candidate. `E.2` gives the Pillars; `E.2.DA` is the evaluation. `A.19.ECS` explains why `E.2.DA` needs evaluated object, use, eligibility, coordinates, evidence loci, stop meanings, and neighbour governing relations rather than a Pillar essay.

**Show, name improvement.** The evaluated object is a durable term candidate. `F.18` already supplies a grouped lexical quality vector: `SemanticFidelity`, `CognitiveErgonomics`, `MorphologicalActionFit`, and `AliasRisk`, plus NQD discipline over candidate names. `A.19.ECS` treats `F.18` as an existing local evaluation for naming, not as a reason to build another one.

**Show, no evaluation yet.** A team says "make this onboarding method better" but cannot say better for whom, by what values, or with what stop. `A.19.ECS` opens before `E.23`: it names evaluated object kind, user, use, contrast cases, candidate characteristics, scales, floors, missingness, protected trade-offs, and neighbour governing relations. Only then can `E.22` frame an improvement-oriented quality evaluation and `E.23` improve the method.

## A.19.ECS:5.1 - Bias-Annotation {#bias-annotation}

A.19.ECS corrects score-first bias. Teams often begin improvement by choosing convenient scores, visible dashboards, or familiar criteria. The pattern starts instead from evaluated object kind, declared use, contrast cases, characteristic slots, scale bindings, value meanings, evidence basis, missingness, protected trade-offs, and stop conditions.

It also corrects evaluation-reuse bias. A reusable evaluation is useful only when it fits the object kind and use. If the existing evaluation already fits, use it; if it does not, construct or repair the evaluation characteristic space before starting an improvement loop.

## A.19.ECS:7 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Symptom | Repair |
|---|---|---|
| **Scale set from air.** | Coordinates appear because they are familiar. | Rebuild from evaluated object kind, use, contrast cases, failure modes, domain tradition, first principles, and current source-use relation. |
| **Wrong-kind object forced through the table.** | Objects outside the declared kind are either scored as weak members of that kind or silently exempted from declared coordinates. | Add an object-kind-fit rule and boundary cases: before opening, return to a suitable evaluation; after invocation, record an explicit object-kind-fit defect/value or repair status. |
| **Checklist masquerading as characteristic space.** | A list of tasks is treated as coordinates. | Convert each task row to an evaluated EntityOfConcern property with a characteristic, scale, value meaning, and evidence rule, or move it to work planning. |
| **One total quality score.** | Several ordinal values are averaged. | Use coordinates, statuses, dominance or comparison rule, and protected trade-offs; do not scalarize unless an neighboring pattern governing the claim explicitly declares the operation. |
| **Improvement without floor.** | A loop continues because more change is possible. | State floor, exceptional meaning, stop condition, and reopen condition. |
| **Hidden value drift.** | The evaluation changes while old evaluations are compared as if nothing changed. | Version the evaluation and state comparability, bridge, or retirement. |
| **Evaluation theft.** | The new evaluation starts asserting evidence, assurance, gate, work, decision, or publication truth without the corresponding predicate and case facts. | State each neighboring subject assertion under its exact predicate or constraint and leave only the value evaluation here. |
| **Result prose as evaluation.** | An evaluator returns a narrative, two-column table, checklist count, or value list without evidence basis and short rationales. | Define the result-row shape, require short rationales and evidence basis, and apply the declared missingness rule to each coordinate whose needed evidence is missing or unchecked. |
| **Evidence basis as evaluated-object method.** | Corpus projection, retrieval, currentness, comparator, monolith-parity, quality-status evidence, or author or reviewer turn correspondence is written in the evaluated object as if it were what the evaluated-object user does. | Move the evidence to the evaluation result, evidence basis, projection carrier, or selected publication carrier; keep only the user action or boundary that the evidence justifies. |
| **Coordinate wording as ontology change.** | A coordinate or repair name sounds cleaner, but changes the evaluated object kind, characteristic kind, relation or claim kind, admissible use, or scope. | Treat it as a changed evaluation decision, recover the pre/post kind relation, and repair or reopen the evaluation rather than accepting lexical cleanup. |

## A.19.ECS:9 - Rationale {#rationale}

Improvement cannot be better than its evaluation. A loop that changes an object version without a declared characteristic space can only produce activity, persuasion, or evaluator preference. An evaluation that lists scales without evaluated-object-kind discrimination, floor, evidence, missingness, trade-offs, and stop meanings cannot guide improvement safely.

Placing this method under `A.19` keeps the ontology clean. `A.19` governs the structure of `CharacteristicSpace`; `A.19.ECS` governs the construction method for evaluations of declared EntityOfConcern kinds and uses. `A.19.ECS` governs the selected characteristics, scales, coordinate construction, and evaluation-use boundaries of the evaluation characteristic space, not its publication or record form. An FPF pattern is only one possible publication form when the evaluation belongs in FPF; a local rubric, standard, table, or project rule is enough when the use is local. `E.23` stays a universal loop method because it does not need to know how every domain chooses its scales. Domain and FPF-specific evaluations such as `E.21`, `E.9.DA`, `E.2.DA`, and `F.18` keep coordinate choices inside those evaluations.

## A.19.ECS:10 - SoTA-Echoing {#sota-echoing}

| Claim | Current practice line | Adoption in A.19.ECS | Boundary |
|---|---|---|---|
| Evaluation artifacts must declare intended use, object, criteria, and missingness before their values are useful. | Current reporting anchors: BenchmarkCards/EvalCards practice for evaluation-card structure, model-card lineage for intended-use and performance-characteristic reporting, and HELM/VHELM/AHELM-style evaluation suites for scenario, metric, raw-result, and modality-extension transparency. | `A.19.ECS` starts from evaluated object kind, use scope, contrast cases, coordinate meanings, evidence rule, and missingness rule. | It is not a benchmark harness, automated judge, or publication format by itself. |
| Multicriteria evaluation needs preserved dimensions and protected trade-offs. | Current QD overview: `A survey on Quality-Diversity optimization: Approaches, applications, and challenges`, Swarm and Evolutionary Computation 100:102240 (2026); retained design lineage: MCDA and value-focused thinking for criterion separation and trade-off visibility. | The pattern requires coordinate values, polarity or no-simple-direction value rule, protected trade-offs, status meanings, and stop or reopen conditions. | Scalarization belongs only to an neighboring pattern governing the claim or explicitly declared local method. |
| Improvement concern can damage the intended value when the evaluation is a weak proxy. | Current proxy-risk anchors: `Goodhart's Law in Reinforcement Learning` (ICLR 2024) and current catastrophic-Goodhart reward-misspecification work (NeurIPS 2024); retained lineage: Goodhart taxonomy. | `A.19.ECS` requires evidence rules, missingness rules, protected trade-offs, and lowering/reopen conditions before a loop can treat a value as improved. | It is not an anti-measurement rule; it makes the measurement or ordinal evaluation explicit enough to be challenged. |
| OEE and NQD work keeps the quality side distinct from novelty, diversity, archive, pool, and selected-set semantics. | Current QD, OEE, and NQD neighbour basis: quality-diversity work evaluates quality together with novelty and diversity, while archive and front are separate relations. Use `C.17` for novelty and diversity retention, `C.18` for archive and front relations, `C.19` for pool treatment, `G.5` for selected-set result declaration, `G.9` for parity, and `G.11` for currentness and refresh. When audience availability is current, use `E.17` for a source-backed publication face and return to source and `E.24.PUB` for the publication occurrence, form, carrier, audience, bounded use, and availability. | An evaluation may supply `Q` values. It does not thereby establish neighboring search, selection, retention, currentness, or publication claims. Examples include novelty, diversity, archive, front, pool, selected-set, parity, refresh, and publication claims; apply the named definitions and tests only when the corresponding claim is current. | `A.19.ECS` constructs an evaluation `U.CharacteristicSpace`; using it neither performs nor establishes OEE or NQD generation, selection, archive, publication, parity, or refresh. |


## A.19.ECS:End {#end}
