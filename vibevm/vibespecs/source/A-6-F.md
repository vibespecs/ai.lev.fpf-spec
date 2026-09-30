# A.6.F - Function and Functional Precision Restoration (RPR-FUNCTION): depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## A.6.F:5 - Archetypal Grounding {#archetypal-grounding}

| Tell-Show-Show row | Grounding |
| --- | --- |
| Tell | A practitioner reads “the function”, “functional architecture”, or “this functionality” and needs to know whether the sentence is about capability, effect, method, Work, a system-role kind or assignment, participation, actual functioning, responsibility, module allocation, mathematical relation, quality, or architecture. A.6.F asks for the exact object or claim and its subject pattern before the phrase carries an FPF claim. |
| Show: `U.System` | A robot, software system, plant, product platform, or AI-agent system may have capabilities, required effects, control functions, module allocations, runtime flows, and user-visible functionality. Those are not one FPF object; A.6.F identifies the exact entity, value, claim, episteme, or direct relation current in each use and requires its subject pattern for it. |
| Show: `U.Episteme` — method-description case | An algorithm file is not automatically a method description. It passes the A.3.2 membership test only when one identified claim-bearing episteme has one admitted exact `U.Method` as its `EntityOfConcern` and says substantively how that method is done. File form, name, author, citation, approval, or executability alone is the near-miss; stop at the direct representation, publication, form, carrier, or other current pattern. |
| Show: `U.Episteme` — other function-like claims | A functional diagram, modeling-language view, architecture view or note, generated-code architecture note, benchmark report, or mathematical model may cue a claim-bearing episteme; a publication form can express its selected edition and a publication occurrence can make that edition available. Read the claim before the form: use C.30 for architecture and view claims, C.30.ASV for structural-view claims, and the pattern that defines any required representation correspondence; keep a benchmark report as an episteme and publication rather than evidence or a method description, and recover its independently established support relation and basis through A.10 before relying on it, using G.6 when an addressable provenance path is needed; use its subject pattern for a mathematical or formal claim and use C.29 when a mathematical-lens use is current. Neither the episteme, publication occurrence, form, carrier, nor correspondence becomes the function, capability, Work, evidence relation, architecture, or mathematical object by its form. |

## A.6.F:6 - Bias-Annotation {#bias-annotation}

Lenses tested: **Arch**, **Ontology and episteme**, **Prag**, **Did**, **Gov**. Scope: function-like wording that carries an FPF claim being made across FPF.

| Bias risk | Mitigation |
| --- | --- |
| Function-root bias | The pattern explicitly does not mint `U.Function`; it requires the subject pattern for the exact object or claim. |
| Functional-architecture exception bias | Functional architecture is normalized as `FunctionalStructure`, not a peer ontology. |
| Module bias | Function-to-module allocation uses correspondence or `A.6.M` module-relation repair; function and module remain distinct. |
| Mathematical bias | Mathematical function wording is assigned to C.29 when used as a lens. |
| Check-only bias | Every conformance item carries a repair action or subject-pattern application. |

This checklist verifies the preceding guidance after the practitioner has chosen the selected repair action; it is not a required project control form and not a substitute for the card, note, view, relation, or repair guidance above.

## A.6.F:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Symptom | Repair |
| --- | --- | --- |
| **Root function kind** | The text treats function as a new universal FPF kind. | Name the exact object or claim and apply its subject pattern; use the optional `FunctionUseRepair` when the receiving use needs that record. |
| **Functional architecture exception** | Functional architecture is treated as a peer architecture ontology. | Expand to `FunctionalStructure` under `ArchitectureOf@Context` and C.30.ASV. |
| **Capability collapse** | What the holon can do is treated as a functional dependency or vice versa. | Split capability claim from functional relation or effect claim. |
| **Work collapse** | Work occurrence or result is described as a function. | Assign occurrence or result claims to A.15 and P2W and keep functional wording design-side unless a work-evidence claim is being made. |
| **Algorithm-form shortcut** | Procedure, code, solver, recipe, protocol, or algorithm form is treated as proof of `U.MethodDescription` membership. | Recover the claim-bearing C.2.1 episteme, one admitted `U.Method` as its exact `EntityOfConcern`, and at least one substantive way-of-doing claim under A.3.2; otherwise keep the source form with its subject pattern. |
| **Mathematical-function import** | A mathematical function, loss, objective, or value functional becomes design ontology. | Use C.29 and state preserved and lost structure plus stop condition. |
| **Module allocation shortcut** | A function is considered implemented because a module is named. | Add correspondence, allocation, module-interface boundary, signature-discipline boundary, or `A.6.M` module-relation repair. |
| **Functionality as quality proxy** | "Functionality" carries adequacy or quality claim without bearer and subject pattern. | Recover bearer and subject pattern through `C.25`, `C.16`, C.16.Q, or an admitted characteristic or measurement subject pattern. |
| **Sterile kind repair** | The wording is typed but no useful move remains. | Restore the direct action on the exact object or claim: use the pattern that defines or tests it, open the selected view, add the needed alignment or correspondence, or stop the stronger reading. |

## A.6.F:10 - Rationale {#rationale}

Function-like wording is too useful to ban and too overloaded to leave unresolved. The smallest useful repair is not a new ontology or a generic record. Name the exact entity, value, claim, or claim-bearing episteme, apply its subject pattern, and state the remaining use. Add an explanatory rejected reading only under the full F.19:4 test.

This design follows A.6.P: recover the direct relation and actual participants when one obtains; add a reusable `RelationSignature` and declaration-local `SlotSpec`s only for typed reuse; keep assertion, specification, or view epistemes separate; and keep representation elements under C.29 with explicit correspondence. It also follows C.30: functional architecture is selected structure for a described holon, not a peer of architecture, not a selected transformation-flow structure by default, and not a mathematical graph description by itself.

The pattern keeps ordinary language usable. A phrase can remain Plain when it carries no FPF claim. When it carries an ontological, evidence, causal, assurance, bridge, gate, work, decision, or admissibility claim, the exact object or claim and subject pattern are recoverable. No generic relation, claim, slot, or view record stands in for that result.

## A.6.F:11 - SoTA-Echoing {#sota-echoing}

| Practice or source line | A.6.F adoption | Action consequence | Boundary |
| --- | --- | --- | --- |
| ISO/IEC/IEEE 42010:2022 architecture-description discipline | Adapt view and concern discipline to functional architecture as a structure-kind view over an architecture claim. | Functional architecture expands through C.30 and C.30.ASV rather than becoming a separate ontology. | ISO terminology does not mint `U.Function` or turn diagrams into architecture. |
| Deliberate exclusion — SysML v2 and its UML-lineage modeling practice | Do not use it as the SoTA basis for this pattern; its popularity and search visibility do not establish present engineering advantage for this problem. | No A.6.F rule or example depends on SysML model elements. More useful domain languages may still supply bounded comparison evidence under their own current source-use record. | This is an explicit non-lineage boundary: SysML terminology and diagram practice do not define FPF kinds, relations, subject patterns, or functional-view adequacy. |
| INCOSE systems-engineering and MBSE functional-analysis practice | Adopt the practical need to separate function, requirement, behavior, physical allocation, and verification claims. | A function-like phrase can guide architecture work only after capability or effect, allocation, evidence, and verification claims are separated. | Functional analysis practice is not evidence sufficiency, assurance, gate passage, or project decision by itself. |
| ISO/IEC 25010 quality-model practice | Treat functionality or functional suitability as quality wording when it evaluates a product or service. | Assign quality-like uses to C.25, C.16, or C.16.Q before they carry adequacy claims. | "Functionality" is not a free adequacy score and not an `ArchitectureOf@Context` claim or selected functional view. |
| C.29 mathematical-lens discipline | Adopt domain, codomain or relation-domain, preserved and lost structure, lens-use admissibility value, and stop condition for mathematical function use. | Mathematical function wording enters a C.29 lens claim only when its fields are recoverable. | Mathematical functions, objectives, and value functionals do not become holon purpose, evidence, causal proof, assurance, or decision claim by themselves. |
| GonzoML neural-network architecture discussions | Adapt practitioner operation language involving blocks, activations, path-selection, memory, cache, loss functions, pruning, ablation, and architecture search as recognition material. | Function-like neural-network wording must resolve to the exact mathematical object, flow relation, module-interface claim, capability or effect, quality characteristic, decision, or evidence claim and its subject pattern. | Neural-network labels and benchmark results do not become FPF ontology, architecture decision, evidence sufficiency, gate passage, or assurance by themselves. |


## A.6.F:End {#end}
