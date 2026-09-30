# C.2.LS - `U.LanguageStateFacetProfile` - Thin profile bundle for language-state facets: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## C.2.LS:5 - Archetypal Grounding {#archetypal-grounding}
**Tell.** A team may say a draft is "still forming" for different reasons. `U.LanguageStateFacetProfile` forces the team to say whether the issue is low articulation, low candidate-space closure, an anchoring mismatch, or an unresolved representation-factor bundle.

**Show (System).** An operator alert note can be `AM.OperatorLoop` anchored and low-closure without being low-formality in every respect.

**Show (Episteme).** An inquiry note can be low articulation yet already tightly anchored to exemplars and traces.

## C.2.LS:6 - Bias-Annotation {#bias-annotation}
The pattern biases authors toward keeping facets explicit and away from master-scale stories. That cost is intentional: the goal is to prevent surrogate progressions from entering the Core.

## C.2.LS:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}
- **Shadow progression.** Treating `early/late` as a master scale. Split the judgement into the named facets.
- **Formality capture.** Letting `F` stand in for closure or articulation. Publish those facets explicitly.
- **Bundle inflation.** Turning `U.LanguageStateFacetProfile` into a second `A.19`. Keep it thin and referential.
- **Opaque readiness.** Using words such as `ready` or `mature` without naming which facet justifies the claim.
- **Route-note capture.** Letting an informative route note act as a move rule, gate state, or endpoint rule. Keep route notes informative. Use `A.16` for admissible moves, the applicable pattern for a downstream definition or test, the applicable gate or Work pattern for those claims, and an `authoritySourceRef` only when an external authority actually supplies the rule.

## C.2.LS:10 - Rationale {#rationale}
The pattern gives the declared language-state chart over `U.CharacteristicSpace` one stable record through which its facet bundle can be published together, without taking over definitions and tests supplied elsewhere in FPF.

## C.2.LS:11 - SoTA-Echoing {#sota-echoing}

**SoTA note.** This section does not mint a second rule source. It is a load-bearing alignment statement: the Solution, Conformance Checklist, and boundary discipline of this pattern must match the stance stated here or explicitly justify divergence.

**Source boundary.** The exact facet meanings and profile rules come from `A.18/A.19` and the neighboring FPF patterns. External sources are used only when they change a rule or case.

| Claim need | Bounded comparison | Exact source | Use in `C.2.LS` | Disposition |
|---|---|---|---|---|
| Readiness claims should stay scoped instead of collapsing into one global adjective. | A profile can state scoped conditions and local thresholds rather than one blanket readiness label. | NIST AI RMF 1.0 (2023) | Require explicit facet-level thresholds and reject a polished profile label as a substitute for the facet values. | **Adopt/Adapt.** |
| A publication can keep several named description elements visible without making their container identical to those elements. | Architecture-description vocabulary distinguishes named elements and their correspondence in a published description. | ISO/IEC/IEEE 42010:2022 | Use this only as a narrow publication comparator; it does not establish the language-state facet ontology. | **Narrow comparator only.** |

SysML v2 is deliberately excluded from the positive SoTA basis and from useful lineage for this question. Search prominence and official status do not show that it solves the facet-profile problem, and no demonstrated use here changes a rule or worked case. Treat it as a historical dead end for this comparison. Do not add a replacement citation merely to fill the removed row.

**Local stance.** The useful bounded result is a small explicit facet profile with local thresholds and decomposable readings, not one maturity adjective or one route-coloured bundle label.

## C.2.LS:13 - Worked Examples and Composition Notes {#worked-examples-and-composition-notes}

### C.2.LS:13.1 - Operator-facing early alert {#operator-facing-early-alert}
A console alert note may be published with a language-state facet profile such as:

- `F = F2/F3` because the note is structurally controlled but still lightweight;
- `AE = AE2` because candidate anchors are visible but not yet fully relation-shaped;
- `CD = CD1` because several routes remain live;
- `LanguageStateAnchoringMode = AM.OperatorLoop` because the note is directly anchored to operator intervention/work;
- `RepresentationFactorBundle = {local, sparse, mixed-symbolic}` because alert text and compact codes coexist.

This example shows why no one facet can replace the others. The note is not `simply early`; it is early in a specific, decomposable way.

### C.2.LS:13.2 - Research cue before lexical repair {#research-cue-before-lexical-repair}
A felt or trace-anchored mismatch cue in an inquiry note may be:

- low `AE`,
- very low `CD`,
- `AM.EmbodiedFelt`,
- and representation-wise mixed because the cue is partly verbal, partly kinesthetic, partly exemplar-based.

That profile explains why the cue should remain in `A.16.1` rather than being forced into `A.6.P` or `B.5.2` immediately.

### C.2.LS:13.3 - Architecture-description case {#architecture-description-case}
A viewpoint-bound note about the adequacy of an architecture description may be moderately high in `F`, moderately high in `AE`, still mid-level in `CD`, document-mediated in `AM`, and symbolic in its representation-factor bundle. The profile keeps description-side adequacy distinct from system-side engineering quality.

### C.2.LS:13.4 - Same `F`, different profile {#same-f-different-profile}
Two notes may share the same rough `F` band and still differ sharply in articulation, closure, anchoring, and representation factors. One may be operator-loop anchored and low-closure; another may be document-mediated and comparatively closed. The profile bundle keeps that difference visible instead of letting `F` behave like a master factor.

## C.2.LS:14 - Authoring and Review Guidance {#authoring-and-review-guidance}

### C.2.LS:14.1 - For authors {#for-authors}
When publishing a language-state facet profile:

1. start from the local authoring problem rather than from a memorized progression;
2. name the facet refs explicitly;
3. add threshold refs only when a threshold changes routing, repair, or another operative decision;
4. avoid global labels such as "mature", "raw", or "ready" unless the profile decomposition is already visible.

### C.2.LS:14.2 - For assurance readers {#for-assurance-readers}
An assurance reader should ask:

- is any facet silently replaced by `F`?
- is a threshold published on an explicit facet rather than on a poetic surrogate?
- do route or reopen claims actually match the published facet bundle?
- are profile notes genuinely informative, or are they smuggling definitions or tests from elsewhere?

### C.2.LS:14.3 - For integrators {#for-integrators}
Integrators should preserve profile references rather than rephrasing them into local slang. A local alias is acceptable only if the underlying facet docking remains explicit and stable.

## C.2.LS:15 - Extension and Migration Notes {#extension-and-migration-notes}

### C.2.LS:15.1 - Local extension rule {#local-extension-rule}
Contexts may extend the profile with local threshold refs, route notes, or additional descriptive aids, but they shall not add a new master facet that collapses the named facet set into one summary factor.

### C.2.LS:15.2 - Migration from surrogate prose {#migration-from-surrogate-prose}
Older prose often says:

- "the episteme is still early",
- "the issue is not mature enough",
- "the note is ready",
- "the cue is still raw".

A conforming migration rewrites such statements into explicit facet talk: which facet is low, which is high, which threshold is or is not met, and which move that fact justifies.

### C.2.LS:15.3 - Boundary reminder {#boundary-reminder}
`U.LanguageStateFacetProfile` is a coordination record. If authors put move rules, bridge rules, scale rules, or bundle semantics into the profile itself, that content belongs with the pattern that defines the move, Bridge, scale, or bundle.
## C.2.LS:16 - Profile Publication Package Discipline {#profile-publication-package-discipline}

### C.2.LS:16.1 - Minimal publishable profile package {#minimal-publishable-profile-package}
A publishable `U.LanguageStateFacetProfile` should normally carry:

- the declared facet refs for `AE`, `CD`, `LanguageStateAnchoringMode`, and `LanguageStateRepresentationFactorBundle`;
- any threshold refs that substantively affect routing, repair, bridge interpretation, or review load;
- the local relation to `F` when readers might otherwise treat `F` as a surrogate;
- any omission note when a facet is intentionally unpublished, unknown, or locally irrelevant.

One-line publication is admissible only if the facet definitions and tests remain legible.

### C.2.LS:16.2 - Partial-profile rule {#partial-profile-rule}
A partial profile is admissible only when omission is explicit. Publishing `AE` and `CD` while deferring `LanguageStateAnchoringMode` is acceptable; silently omitting it and then speaking in scalar prose such as "early" or "ready" is not.

If only one facet is published, either explain why the others are not included in the current note or point to the note where they are already published.

### C.2.LS:16.3 - Overlay discipline {#overlay-discipline}
Local overlays such as "explicit-but-open", "trace-heavy", or "operator-tight" are admissible only when they dock to explicit facet refs. Overlays remain secondary to the declared profile and must not replace the facet bundle.

## C.2.LS:17 - Cross-Facet Reading Rule {#cross-facet-reading-rule}

### C.2.LS:17.1 - No master-facet reading {#no-master-facet-reading}
Do not infer the whole language-state profile from one facet. High `AE` does not entail high `CD`; strong `AM.OperatorLoop` does not fix `AE` or `CD`; symbolic representation does not entail high `F`; low `CD` does not imply low operational consequence.

### C.2.LS:17.2 - Threshold interaction rule {#threshold-interaction-rule}
When a threshold is expressed over one facet, say whether the other facets are merely informative or also constraining. A Context may allow entry into `B.5.2.0` once `AE` suffices for an explicit open question while still capping `CD` so rival answers remain live; it may allow entry into `A.6.P` at `AE3+` while still capping `CD` so the move remains exploratory rather than endpoint-binding.

### C.2.LS:17.3 - Transition reading rule {#transition-reading-rule}
Read profile transitions facetwise. A note may become more explicit without becoming more closed, more document-mediated without changing closure, or more symbolic without becoming more formal. `A.16`, `A.16.1`, `A.16.2`, `B.4.1`, and `B.5.2.0` should therefore cite the facet transition that actually justifies the move.

## C.2.LS:18 - Review Matrix and Migration Tests {#review-matrix-and-migration-tests}

### C.2.LS:18.1 - Review matrix {#review-matrix}
An assurance reader should ask:

- does each published facet keep the definition and test supplied by its own pattern rather than by surrogate prose;
- does any overlay smuggle a hidden scalar or gate decision;
- are threshold claims tied to the facet that really bears them;
- do cited moves in `A.16`, `A.16.1`, `A.16.2`, `B.4.1`, or `B.5.2.0` actually match the facet bundle;
- if the profile crosses a Bridge or viewpoint boundary, did the author use `F.9` for the Bridge, bounded-use claim, and loss account, and keep any optional F.9.1 stance note separate rather than importing it as a fake facet?

### C.2.LS:18.2 - Migration test for source prose {#migration-test-for-source-prose}
Source phrases such as "still immature", "not ready yet", or "already stable enough" should be unpacked into: which facet is claimed, which anchor or bundle member justifies it, which threshold or route consequence follows, and which cited rule or external `authoritySourceRef` justifies that consequence.

### C.2.LS:18.3 - Comparative profile use {#comparative-profile-use}
Compare profiles facetwise unless a Context has published an explicit local aggregation for reporting. Such an aggregation remains secondary and must not replace the profile in norms, thresholds, or bridge claims.


## C.2.LS:End {#end}
