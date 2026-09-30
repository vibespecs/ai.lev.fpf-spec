# C.30.TFS-REL - Use Transformation-Flow Structures and Networks in Architecture: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## C.30.TFS-REL:5 - Archetypal Grounding {#archetypal-grounding}

| Tell-Show-Show row | Grounding |
| --- | --- |
| Tell | A practitioner sees one TFS or several connected TFSs and wants to use that flow structure in an architecture question. C.30.TFS-REL makes them name the exact TFS or network and exact architecture locus; for a network, they choose one containing holon/relation or the exact participating holons and relations/claims. The result is one usable trace or an exact stop, not an architecture relation inferred from the diagram. |
| Show: `U.System` | A software system, plant, AI agent, neural network, vehicle, or supply chain may have transformation-flow structure. A diagram or mathematical description can inform architecture reasoning about that structure without carrying the required-effect, actual-transformation, or other non-flow claims named in `C.30.TFS-REL:4.3`. |
| Show: `U.Episteme` | For a mathematical graph description, generated relation graph, code-agent probe output, neural-network diagram, dashboard, or architecture note, distinguish the description episteme from its representation or publication; E.17.0 governs whether that episteme is a view. The episteme can support the transformation-flow use only when exact E.18 TFS or E.18.NET network, the selected network architecture branch when applicable, edition/plane/context pins, correspondence, any relied-on row locator, hidden relation-structure return condition, and admissible use are recoverable. |

## C.30.TFS-REL:6 - Bias-Annotation {#bias-annotation}

Bias lenses: **Arch**, **Onto**, **Epist**, **Prag**, **Did**, **Gov**. Scope: architecture-to-transformation-flow uses of E.18 TFS or E.18.NET network objects.

| Bias risk | Mitigation |
| --- | --- |
| Structure-or-description-as-architecture bias | Direct architecture relations and bounded claims stay with C.30, descriptions with C.30.AD, mathematical representations with C.29, mathematical descriptions with E.18.2, math-lens uses with C.29, and structural views with C.30.ASV/E.17.0. |
| Function-flow/change collapse | Required functional content, selected transformation-flow structure, and actual A.3.4 transformation remain separate. Functional and flow structures are related, not identical by default. |
| Non-flow claim overread | The relation table assigns non-flow claim kinds to their governing patterns. |
| Mathematical overread | Mathematical-lens use of a graph or valuation is governed by C.29. |
| Check-only bias | Conformance checks include repair actions and stop conditions. |

This checklist verifies the preceding guidance after the practitioner has chosen the selected repair action; it is not a required project control form and not a substitute for the card, note, use record, direct relations, or repair guidance above.

## C.30.TFS-REL:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Symptom | Repair |
| --- | --- | --- |
| **Structure-as-architecture** | The E.18 selected transformation-flow structure is called the whole architecture. | Use C.30 for the actual architecture relation, selected structure, or bounded claim; C.30.AD for description; keep this record only for the transformation-flow use. |
| **Unnamed network as architecture bearer** | A connected network or its graph is assigned maintainability, capability, responsibility, agency, production, required effect, or actual transformation without one containing holon/relation or explicit participating holons. | Select the named-containing-holon or explicit inter-holon branch, restore every characteristic to a named bearer, and keep graph/record outside architecture identity. |
| **Graph-description-as-functional-architecture** | A graph-shaped mathematical description or diagram is treated as functional architecture, functional element, or actual change. | Split functional claim, selected TFS, actual transformation, mathematical description, representation, and publication; add correspondence when needed. |
| **Flow-as-work-log** | Path or slice wording is treated as Work occurrence. | Use A.15.1 for the occurrence and the governing work-result or P2W relation for those claims; keep E.18 to selected structure, path, slice, or valuation. |
| **Crossing-as-gate-result** | A crossing relation is treated as gate passage. | Assign gate-decision claims to A.21 and keep crossing relation under E.18. |
| **Valuation-as-score** | A flow valuation is used as a generic architecture score. | State E.18 valuation and set-return discipline; assign measurement, characterization, selection, or candidate-set claims to `C.16` or an admitted governing pattern. |
| **Generated relation-graph proof** | A code-agent relation graph or probe output is used as proof of architecture understanding or safety. | Recover source publication/codebase edition, extraction/probe locus, observation class from {observed, inferred, unknown}, unexplored regions, hidden structure, and direct evidence or assurance application. |
| **Prompt-data-tool flow as authority proof** | A prompt, data, or tool-flow diagram is treated as permission for tool action or proof that authority is safe. | Keep it as a transformation-flow use or E.18.2 mathematical description. Route a selected `SecurityTrustBoundaryStructure` view through C.30.ASV; for agentic tool use, route call planning to `C.24` after the action or option is fixed and autonomy-budget enforcement to `E.16`. Use `A.20` for an internal-constraint result, `A.21` for a named gate decision, or the direct domain pattern for the particular release, admissibility, or approval claim when that claim is current. |

## C.30.TFS-REL:10 - Rationale {#rationale}

E.18 governs one selected TFS, its paths, crossings, valuations, and pins; E.18.NET governs one selected network and its exact cross-member relations. Architecture needs to use either object without taking over its ontology or inventing an unnamed architecture bearer. The smallest stable result is therefore one C.30-side use record pointing to exact objects and stating the named-containing-holon or explicit inter-holon branch when a network is selected.

This pattern also protects functional architecture and actual-change semantics. A functional structure may correspond to a transformation-flow structure, and in some cases both views may designate the same selected `U.Structure`; that identity is not automatic. Required or desired effect remains claim content, while an actual `U.Transformation` requires the independent A.3.4 basis.

## C.30.TFS-REL:11 - SoTA-Echoing {#sota-echoing}

| Practice or reference line | C.30.TFS-REL adoption | Action consequence | Boundary |
| --- | --- | --- | --- |
| E.18 one-TFS discipline and E.18.NET network discipline | Adopt E.18 as owner of one TFS, paths, crossings, and valuations; E.18.NET as owner of one selected network, member-local references, and exact cross-member relations. | Name the exact TFS or network, then add only the exact C.30 architecture locus and selected network branch. | Neither flow-structure owner becomes generic architecture or architecture-description ontology. |
| ISO/IEC/IEEE 42010:2022 and multi-view architecture practice | Adapt view and correspondence discipline to architecture-to-transformation-flow reliance. | Transformation-flow views relate to actual architecture relations, selected structures, exact structural views, or conditional descriptions through C.30, C.30.AD, C.30.ASV, and correspondence claims/relations. | Architecture views do not become proof, evidence, gates, decisions, required-effect realization, or actual transformation by view status alone. |
| MBSE and SysML v2 view and relation practice | Adapt model-derived flow views and path views as descriptions derived from a model publication or edition. | A model-derived flow description states model edition, selected structure, hidden/lost structure, and admissible use. | Tool models or query results do not establish FPF E.18, C.30, A.3.4, or E.17.0 relations without their defining predicates and case facts. |
| Neural-network dataflow and GonzoML architecture-operation corpus | Adopt practitioner recognition for block replacement, path selection, memory/cache placement, MoE expert selection, pruning, distillation, ablation, and compute/memory/latency tradeoffs. | Keep source labels with `C.30.STRAT` until exact values are recovered; C.30.TFS-REL applies only when recovered flow structure changes the architecture move. | Benchmarks, ablations, pruning masks, or search outputs do not become evidence, assurance, gate passage, actual transformation, or architecture decision by themselves. |
| Theory of Code Space (arXiv:2603.00601) code-agent relation graph probing | Adapt component-belief statuses from {observed, inferred, unknown} and partial-observability warnings to relation-graph use. | Generated code relation graphs can be used only with typed relation semantics, source/codebase edition, extraction/probe locus, unexplored regions, and hidden-relation return condition. | Do not mint `U.CodeSpace`; probe output alone does not prove internal belief or establish architecture adequacy, assurance, or a release-evidence claim. |

**Currentness boundary.** Inputs are E.18 TFS semantics and pins; E.18.NET network identity, cross-member relations, and row-locator resolution when selected; the chosen network architecture branch and exact containing or participating holons/relations/claims; C.30/C.30.AD/C.30.ASV architecture-side rules; observation class; required-versus-actual status; and non-flow governors named in `C.30.TFS-REL:4.3`. When one changes, the record changes only at the affected reference, branch, row locator, correspondence, hidden relation-structure return condition, admissible-use boundary, or governing-pattern assignment.


## C.30.TFS-REL:End {#end}
