# C.2.LS - `U.LanguageStateFacetProfile` - Thin profile bundle for language-state facets {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Definitional (D)
> **Status:** Stable
> **Normativity:** Normative unless marked informative

**Plain-name.** Language-state facet profile.

**Use this pattern when.** Use C.2.LS when a `U.Episteme` publication needs one explicit profile that keeps formality, articulation, closure, anchoring, representation factors, and local thresholds visible together.

**What goes wrong if missed.** Teams replace the facet profile with a maturity adjective such as `ready`, `raw`, or `stable`, then use that label to choose routes, decide whether to reopen, interpret Bridges, or make publication decisions. The label hides the actual facet values.

**What this buys.** A thin, decomposable profile bundle: each facet keeps the definition and tests supplied by its own pattern, while the profile gives authors, assurance readers, and integrators one place to publish a threshold-relevant language-state position.

## C.2.LS:1 - Problem frame {#problem-frame}
Once position claims in the declared language-state chart over `U.CharacteristicSpace` must be published and compared, teams need one thin profile bundle that keeps the relevant facets visible as one explicit facet profile without turning that profile into a second characteristic calculus or a surrogate maturity progression.

## C.2.LS:2 - Problem {#problem}
Without a dedicated profile bundle, authors blur articulation, closure, anchoring, and representation into one vague maturity story, or they silently reuse `F` as a surrogate. That blocks admissible threshold publication, undercuts `A.16` move guards, and makes school-to-school bridge work harder than it needs to be.

## C.2.LS:3 - Forces {#forces}
| Force | Tension |
|---|---|
| **Thin profile bundle vs practical coordination** | Keep the bundle small, but still give one stable place where the language-state facets are named together. |
| **Reuse vs duplication** | Reuse A.18/A.19 characteristic machinery and A.16 moves; use E.18 only for an independently selected TransformationFlowStructure. |
| **Local thresholds vs cross-context comparability** | Contexts need local thresholds, but the facet names must stay stable enough for bridge work and viewpoint bundles. |

## C.2.LS:4 - Solution {#solution}
`U.LanguageStateFacetProfile` is a typed profile bundle that names the facets by which position claims in the declared language-state chart over `U.CharacteristicSpace` are published and interpreted:

- `formalityRef` -> `U.Formality` from `C.2.3`
- `articulationExplicitnessRef` -> `U.ArticulationExplicitness` from `C.2.4`
- `languageStateClosureDegreeRef` -> `U.LanguageStateClosureDegree` from `C.2.5`
- `languageStateAnchoringModeRef` -> `U.LanguageStateAnchoringMode` from `C.2.6`
- `languageStateRepresentationFactorBundleRef` -> `U.LanguageStateRepresentationFactorBundle` from `C.2.7`
- `thresholdRefs?` -> context-local threshold declarations over the named facets
- `routeNotes?` -> informative notes that help interpret routing or reopening decisions

`C.2.LS` therefore defines only the **profile bundle**; it defines neither an individual characteristic nor a trajectory. `A.18/A.19` supply characteristic semantics, `A.16` defines admissible moves, and `E.18` governs an independently selected TransformationFlowStructure.

### C.2.LS:4.0a - Kind and profile-bundle boundary {#kind-and-profile-bundle-boundary}

`U.LanguageStateFacetProfile` is a dependent durable profile-bundle value under the declared `U.LanguageStateSpace` and `U.CharacteristicSpace` boundary, not a root U-kind. Its identity is the explicit bundle of language-state facet refs used for position reading and threshold publication. A local dashboard, table, route note, or maturity label is a publication or interpretation over the bundle, not the bundle itself.

### C.2.LS:4.1 - Contribution boundary {#contribution-boundary}
`C.2.LS` defines only profile composition and requires the language-state facets to remain explicit and non-collapsed. It does **not**:

- redefine `F`;
- invent a second formality progression;
- redefine the scale semantics of `AE`, `CD`, `LanguageStateAnchoringMode`, or `U.LanguageStateRepresentationFactorBundle`;
- define reopen/backoff moves;
- define endpoint classification or bridge kinds.

### C.2.LS:4.2 - Threshold publication discipline {#threshold-publication-discipline}
Any threshold used to choose a next question, constrain an admissible move, or begin `A.6.P` recovery shall be published on explicit named facets in the profile. Do not describe hidden sub-levels of `F` when the real issue is articulation, closure, anchoring, or the representation-factor bundle.

### C.2.LS:4.2.a - Local profile-reading witness {#local-profile-reading-witness}
For this pattern, a published facet profile is reviewable when:

- the facet refs are explicit or explicitly inherited from an already pinned upstream publication;
- any threshold-bearing use names the facet whose threshold is being invoked;
- route notes or local overlays remain informative and visibly docked to the explicit facet bundle;
- and the profile does not smuggle move rules, bridge rules, gate state, or downstream definitions and tests into the bundle record.

A polished label, one strong facet, or one memorable route note does not by itself yield an admissible profile reading. The profile remains conformant only when the named facets stay explicit and decomposable.

### C.2.LS:4.3 - Composite readings {#composite-readings}
A language-state judgement may be composite, but the composite shall be decomposable. For example, a cue may be:

- low `AE`,
- medium `CD`,
- `AM.TraceAnchored`,
- and representation-wise mixed rather than purely symbolic.

A conforming profile makes this decomposition visible rather than hiding it under one poetic label such as "early" or "raw".

### C.2.LS:4.4 - Corridor map note {#corridor-map-note}
`C.2.LS` participates in the current `Language-State & Semantic Routing Corridor`, but contributes only the thin facet-profile bundle. Readers who need one map of the full language-state pattern set should read the corridor note in `C.2.2a`.

That map does not change this boundary: `C.2.LS` still does not define cue preservation, route-bearing publication, prompt entry, or downstream endpoint use.

## C.2.LS:7 - Conformance Checklist {#conformance-checklist}
- @fact:CC-C-2-LS-1 `CC-C.2.LS-1` A language-state facet profile **SHALL** reference the patterns that define its facets rather than invent local unnamed factors. @status:spec/done
- @fact:CC-C-2-LS-2 `CC-C.2.LS-2` `C.2.LS` **MUST NOT** redefine `F` or create a second formality progression. @status:spec/done
- @fact:CC-C-2-LS-3 `CC-C.2.LS-3` Thresholds that matter for routing, reopening, or lexical repair **SHALL** be published on explicit facets. @status:spec/done
- @fact:CC-C-2-LS-4 `CC-C.2.LS-4` Trajectory accounts that rely on facet profiles **SHOULD** reuse A.16 move kinds. Apply E.18 only to an independently selected TransformationFlowStructure; use E.18.2 when its mathematical description is needed. @status:spec/done
- @fact:CC-C-2-LS-5 `CC-C.2.LS-5` Composite labels such as `early`, `settled`, or `ready` **SHALL NOT** stand in for the explicit facet bundle when those states matter operationally. @status:spec/done
- @fact:CC-C-2-LS-6 `CC-C.2.LS-6` Composite readings, overlays, and route notes **SHALL** remain decomposable into named facets and **MUST NOT** behave as hidden master factors. @status:spec/done
- @fact:CC-C-2-LS-7 `CC-C.2.LS-7` A profile bundle **MUST NOT** smuggle move rules, bridge rules, gate state, or downstream definitions and tests into what should remain a thin facet-profile record. @status:spec/done

## C.2.LS:9 - Consequences {#consequences}
The benefit is clearer source and rule references: early cue work, bridge annotations, and reopen moves can all refer to one explicit facet profile. The trade-off is more explicit profile authoring and threshold publication.

## C.2.LS:12 - Relations {#relations}
- Builds on: `A.18`, `A.19`, `C.2.2a`, `C.2.3`.
- Coordinates with: `C.2.4`, `C.2.5`, `C.2.6`, `C.2.7`, `A.16.0`, `A.16`, `A.16.1`, `A.16.2`, `B.4.1`, `B.5.2.0`, `E.18`, `F.9` for any Bridge and bounded-use claim, and `F.9.1` only for an optional stance note about that claim.
- Constrains: language-state threshold publication and profile composition.

## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/C-2-2a#root, C.2.4-C.2.7. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/A-16#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-16#root, spec://ai.lev/fpf-spec/contract/A-16-1#root, spec://ai.lev/fpf-spec/contract/C-2-2a#root, spec://ai.lev/fpf-spec/contract/C-2-4#root, spec://ai.lev/fpf-spec/contract/C-2-5#root, spec://ai.lev/fpf-spec/contract/C-2-6#root, spec://ai.lev/fpf-spec/contract/C-2-7#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/C-2-LS
