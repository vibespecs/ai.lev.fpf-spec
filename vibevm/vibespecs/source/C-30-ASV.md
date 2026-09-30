# C.30.ASV - Architecture Structural View Adequacy (ASV): depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## C.30.ASV:5 - Archetypal Grounding {#archetypal-grounding}

| Tell-Show-Show row | Grounding |
| --- | --- |
| Tell | A practitioner looks at an architecture "view" and asks whether it is functional, flow, control, module-interface, information or data, placement, scale, work, evidence, or declared logical structure. C.30.ASV turns that question into structure-kind triage or a full description-plus-conformance record. |
| Show: `U.System` | A plant, vehicle, software system, product platform, AI-agent system, or neural-network model can require several structural descriptions over the same exact subject-side architecture. One module view does not exhaust the system architecture, and one flow graph does not prove work, evidence, safety, or release. |
| Show: `U.Episteme` | A diagram, model, generated relation graph, ADR, dashboard, SysML view, or C4 diagram may express or publish a description episteme. That same episteme is an architecture structural view only when exact C.2.1 identity, selected structure, structure kind, exact viewpoint, obtaining E.17.0 conformance relation, hidden and lost structure, correspondence, source or reliance relation, and admissible use are recoverable. |

## C.30.ASV:6 - Bias-Annotation {#bias-annotation}

Bias lenses: **Arch**, **Onto**, **Epist**, **Prag**, **Did**, **Gov**. Scope: architecture structural-view claims over holons.

| Bias risk | Mitigation |
| --- | --- |
| Module-view bias | Make module-interface one structure kind, not the default meaning of architecture. |
| Viewpoint-kind conflation | Keep selected structure kind, exact viewpoint episteme P, catalogue L, local family declaration, exact `U.ViewpointRef`, candidate description E, and conformance relation separate. |
| TEVB mutation bias | Reuse only exact references from a materialized project-local TEVB declaration when their resolved P rules fit; do not treat E.17.2's template or a `VF.TEVB.ENG` spelling as a current family value. |
| Check-only bias | Every failed conformance check gives a repair action or use of an applicable pattern. |
| Didactic-thinning risk | The pattern starts with triage and action, not taxonomy alone. |

This checklist verifies the preceding guidance after the practitioner has chosen the selected repair action; it is not a required project control form and not a substitute for the card, note, description, direct conformance relation, or repair guidance above.

## C.30.ASV:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Symptom | Repair |
| --- | --- | --- |
| **Module diagram as architecture view** | One module-interface diagram is treated as the whole architecture or as a `U.View` by appearance. | Use structure-kind triage; keep module-interface as one structure kind and apply exact E.17.0 conformance only when view membership matters. |
| **Viewpoint as structure kind** | `VP.Functional`, `VP.ModuleInterface`, or another viewpoint is used as if it were the selected structure kind. | Recover `ArchitectureStructureKindRef`; keep its binding to an exact viewpoint episteme separate. |
| **Structure kind as viewpoint** | `FunctionalStructure` or `ControlStructure` is treated as if it were already an admitted viewpoint P. | Keep structure-kind classification separate; when viewpoint reuse is needed, resolve one exact `U.ViewpointRef` from a materialized local catalogue declaration to exact P and test E.17.0 conformance. |
| **Publication-face collapse** | A diagram, model, table, dashboard, generated relation graph, ADR, or C4 view is treated as the view episteme. | Recover description episteme, representation, and E.24.PUB occurrence, form, and carrier separately; use `ArchitectureStructuralView` only if exact conformance obtains and the view changes action. |
| **Single-view decision** | A decision uses one architecture view as if it covered all affected structures. | Name affected structures and view refs, or narrow the decision to the single view's admissible use. |
| **Lost-structure silence** | Extracted, generated, coarsened, or compressed views hide distinctions but still justify action. | Add hidden structure and lost structure and source-return condition, or narrow admissible use. |
| **Proof overread** | The structural view is used as evidence sufficiency, safety proof, causal proof, gate decision, or work record. | Use the applicable evidence, assurance, causal, gate, or work pattern and keep ASV only to view adequacy. |
| **Risk color as security architecture** | A red, yellow, or green risk cell, risk matrix, maturity score, or compliance color stands in for `SecurityTrustBoundaryStructure` or resource-allocation priority. | Recover protected asset or effect, trust boundary, untrusted input, privilege or authority relation, data flow or control flow, abuse or misuse path, and the evidence named by value, assurance, measurement, causal, gate, selection, or allocation claim kind if that claim is being made; do not treat ordinal risk color as security architecture adequacy, resource-allocation priority, or gate passage. |
| **Taxonomy without action** | The text classifies a view but does not say what changes in practice. | Add `admissibleArchitectureMove` or stop at Plain recognition wording. |

## C.30.ASV:10 - Rationale {#rationale}

C.30.ASV exists because architecture descriptions are commonly multi-view, but FPF cannot let "view" absorb every architecture claim. A structure kind and a viewpoint are different. A structure kind says what kind of selected structure is described; a viewpoint is one exact episteme whose fixed rules the candidate description must satisfy. The direct conformance occurrence, not a label or bundle, makes the same episteme a `U.View`.

The pattern keeps first use light by providing `ArchitectureStructureKindTriage@Project`. If triage identifies the structure kind under consideration and the next admissible architecture move, no full view record is needed. The full record is used when exact conformance obtains and a view changes action, correspondence, publication, source return, source or reliance use, or non-view claim kind.

The TEVB decision is conservative. E.17.2 supplies a four-position project-local authoring template, not a current family or importable bundle. Architecture may reuse only exact `U.ViewpointRef` values resolved from a materialized local declaration, with catalogue and member provenance preserved. Architecture-specific structure kinds and candidate-record bindings are defined beside those exact local references rather than mutating their resolved viewpoint epistemes or treating declaration membership as conformance.

## C.30.ASV:11 - SoTA-Echoing {#sota-echoing}

SysML v2 is intentionally excluded from C.30.ASV's SoTA basis. This pattern treats it as a historical dead end rather than a source or lineage and derives no rule from it.

| Practice or source line | C.30.ASV adoption | Action consequence | Boundary |
| --- | --- | --- | --- |
| FPF `C.2.1`, `A.22`, `E.17.0`, `C.30`, and `C.30.AD` | Use exact episteme identity, selected-structure discipline, direct viewpoint conformance, architecture relation, and architecture-description boundaries together. | ASV records require one primary selected structure as EntityOfConcern, effective scheme, structure kind, exact viewpoint, obtaining conformance relation, correspondence when used, and admissible use. | A view remains the same episteme about selected structure; no context field, authoring route, or suffix creates it. |
| [Dyad v3 physical-system modeling and analysis](https://help.juliahub.com/dyad/stable/) | Adopt its current integration of physical models, control analysis, SciML surrogates, calibration, and deployment from one source, with both textual and schematic editing. | A generated or edited description still states `viewConstruction`, selected structure, hidden and lost structure, and a source-return condition when action relies on the description. | Executability, simulation, generation, or tool presentation does not create the source episteme, viewpoint-conformance relation, selected structure, evidence sufficiency, gate passage, or assurance. |
| UAF, ArchiMate, C4, and multi-view architecture practice | Adapt viewpoint-library and lightweight diagram communication pressure. C4 contributes communication and zoom pressure only. | C4-like, UAF-like, and ArchiMate-like diagrams can represent or publish ASV epistemes only when exact description identity, EntityOfConcern, structure refs, structure kind, viewpoint conformance, and publication relations are explicit. | Do not import their layer, viewpoint, enterprise taxonomies, structure-kind adequacy, evidence sufficiency, or architecture decision claim without recoverable FPF objects and relations. |
| Systems security engineering, secure-by-design, SSDF, and CSF-style practice | Adopt security as architecture-side structure when trust boundaries, authority, untrusted input, secure defaults, hardening, update channels, and detection and response boundaries change action. | Use `SecurityTrustBoundaryStructure` before evidence, assurance, gate, risk score, or compliance proof. | A security framework, checklist, risk color, or control catalog is not security architecture adequacy, evidence sufficiency, assurance, or gate passage by itself. |
| Theory of Code Space, arXiv:2603.00601 and related code-agent architecture relation-graph probing | Adopt partial-observability, typed relation discovery, invariant discovery, uncertainty reporting, and externalized architecture relation graphs as ASV practice source. | Treat an externalized code-agent relation graph as a diagnostic description, representation, or ASV publication only with observed, inferred, or unknown observation value, evidence pointers, unexplored regions, and typed relation semantics. Add source-return conditions when the intended use relies on hidden distinctions. | Do not mint `U.CodeSpace`; do not treat probe JSON, cognitive-model publication, dependency-F1 result, or diagnostic relation graph as architecture adequacy, internal belief proof, agent authority, safe-code-change authority, assurance, or release authority. |
| GonzoML neural-network architecture discussions | Adopt practitioner operation language for architecture views: block substitution, relation retargeting, dataflow changes, memory placement or cache placement, path-selection or gating, MoE expert-selection, pruning, distillation, NAS, ablation, and compute, memory, or latency tradeoffs. | Use those phrases as recognition cues for changed structure kind, flow relation, module-interface claim kind, security or trust boundary, data-custody relation, preserved and lost structure, affected characteristic, source relation, and the applicable decision or evidence pattern. | Neural-network labels, benchmarks, ablations, pruning masks, block, layer, router, cache, or state labels, or search outputs do not become FPF ontology, architecture decisions, evidence sufficiency, gate passage, assurance, or architecture adequacy by themselves. |


## C.30.ASV:End {#end}
