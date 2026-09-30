# A.19.SOURCE-SET-SPACE-SUBSTRATE - Source-Set and Search/Outcome-Space Substrate: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## A.19.SOURCE-SET-SPACE-SUBSTRATE:5 - Archetypal Grounding {#archetypal-grounding}

### A.19.SOURCE-SET-SPACE-SUBSTRATE:5.1 - System {#system}

**Tell.** One QD line keeps saying that one archive is both the search-side role and the evaluation basis. Downstream readers need to see that the same declared `CharacteristicSpace` can still occupy two different role positions without turning the archive or the descriptor layer into the space itself.

**Show.**

```text
SourceSetFamily       = Archive
SearchSpaceRef          = BehaviorCharacteristicSpace@ed=12
OutcomeSpaceRef         = BehaviorCharacteristicSpace@ed=12
SpaceRefRelationKind    = sameDeclaredSpaceAs
SourceToOutcomeRelation = archive-retained candidates are navigated and judged
                          for local coverage gain in the same declared behavior
                          space
DistortionPosture       = metric/model-dependent; descriptor realization and
                          neighborhood metric qualifier are active
DescriptorMapRef        = QDDescriptorMap@ed=9
DistanceDefRef          = ArchiveNeighborhoodDistance@ed=4
SpaceMetricRef          = ArchiveNeighborhoodMetric@ed=4
```

**Cash-out.** This line now says three distinct things cleanly: the active source set is one archive, both role-refs resolve to the same declared `CharacteristicSpace`, and the `DescriptorMapRef` plus `DistanceDefRef` are only interpretive layers over that shared space reference. A downstream selection or archive-maintenance discussion can reuse this line without pretending the archive itself is the space.

### A.19.SOURCE-SET-SPACE-SUBSTRATE:5.2 - Episteme {#episteme}

**Tell.** One synthesis line presents one derived tradition front and then starts speaking as if the visible front were the default meaning of the whole palette.

**Show.**

```text
SourceSetFamily        = Front
DerivedViewKind        = TraditionFront
BasePaletteRef         = SoTAPaletteDescriptionId
SearchSpaceRef         = TraditionComparisonSpace@ed=3
OutcomeSpaceRef        = AdoptionOutcomeSpace@ed=2
SpaceRefRelationKind   = distinctDeclaredSpaceFrom
SourceToOutcomeRelation = for each retained tradition profile, AdoptionEstimate@ed=1
                          uses its integration requirements and the named team's
                          capability and workload facts to estimate adoption cost
                          and expected benefit in AdoptionOutcomeSpace@ed=2
DistortionPosture      = model-dependent; the estimate is conditional on those
                         team and workload facts and omits unmodelled adoption effects
BridgeDistortionNote   = not used; this example asserts no F.9 semantic Bridge
```

**Cash-out.** The visible front stays a derived view over the recoverable palette. `AdoptionEstimate@ed=1` supplies the stated conditional source-to-outcome mapping. A later interpretive or atlas view may reorganize the presentation while preserving that mapping and its model limitations.

### A.19.SOURCE-SET-SPACE-SUBSTRATE:5.3 - Boundary anti-case {#boundary-anti-case}

**Tell.** One note says only that "the shortlist front is the published result for the current selector result" and names no source-to-outcome relation, no search-side space, no outcome-side space, and no posture.

**Show.** This is not a substrate declaration. It is publication metadata over one already-selected set.

**Cash-out.** Apply `G.5` or `G.10` to that note. Do not pad it with pseudo-substrate words just to make it look deeper than it is.

### A.19.SOURCE-SET-SPACE-SUBSTRATE:5.4 - Use-situation spread {#use-situation-spread}

Use the pattern this way across different working situations:

| Working situation | What to do with this pattern | What must stay explicit | Common miss avoided |
| --- | --- | --- | --- |
| Archive-side QD line where navigation and evaluation stay in one declared behavior space | Use the shared-space profile. Fill the six core fields, then add descriptor/metric qualifier only if active. | `Archive` as source set, both role-refs, `sameDeclaredSpaceAs`, and the active posture. | Treating the archive or descriptor layer as if it were the space itself. |
| Derived tradition/front line that is judged against one different outcome space | Use the cross-space profile and keep `DerivedViewKind` plus `BasePaletteRef` visible. | The derived view stays derived, the base palette stays recoverable, and the cross-space relation stays explicit. | Letting the visible front replace the base palette or hiding the bridge-loss posture. |
| Learned, adaptive, or uncertainty-bearing line where the space declaration is real but heavier qualification is still case-bound | Keep the substrate core explicit and choose the honest posture token such as `uncertainty-bearing`, `learned/adaptive`, or `unstable-under-refresh`. | The reader can see that the substrate is real without being promised fake geometric closure. | Pretending every serious case is either fully transparent or fully described by one metric stack. |
| Shortlist or publication note that only says what set result or publication form is shown or shipped | Do not use this pattern. Apply `G.5` or `G.10` directly. | The note stays publication-facing instead of imitating substrate depth. | Padding publication metadata with pseudo-substrate language. |

## A.19.SOURCE-SET-SPACE-SUBSTRATE:6 - Bias-Annotation {#bias-annotation}

- **Gov bias.** The pattern prefers explicit declaration over convenient shorthand.
- **Arch bias.** The pattern keeps substrate, interpretive view, and publication consumers separated even when one merged story would read more smoothly.
- **Prag bias.** The pattern prefers a short explicit substrate declaration that can be reused across search, synthesis, and publication-adjacent lines.
- **SoTA bias.** The pattern assumes current QD and OEE work often uses learned, adaptive, unstructured, or uncertainty-bearing spaces and therefore resists premature geometric closure.

## A.19.SOURCE-SET-SPACE-SUBSTRATE:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Why it fails | Repair |
| --- | --- | --- |
| Treating one archive or front as the search space itself | A source set is not the same kind as one declared `CharacteristicSpace`. | Keep `SourceSetFamily` and `SearchSpaceRef` separate. |
| Leaving `SpaceRefRelationKind` implicit | The reader then has to guess whether search and outcome share one declared space or use two distinct declared spaces. | Declare `sameDeclaredSpaceAs` or `distinctDeclaredSpaceFrom` next to the two refs. |
| Letting `DescriptorMapRef` stand in for the whole substrate | A representation layer is not identical to the position-typed space declaration. | State the docking rule explicitly and keep the space refs visible. |
| Making `SourceSetComposition` or `DerivedViewKind` mandatory in every line | The line fabricates composition or derivation where none exists. | Keep them conditional. |
| Publishing with bare `portfolio` language | `portfolio` blurs retained-set, selected-set, and posture talk. | Use declared source-set and outcome metadata instead. |
| Treating all distortion as one bridge story | Not every qualified relation is bridge-mediated. | State the active posture directly. |
| Letting `G.5` or `G.10` sound like the substrate itself | Publication metadata then silently replaces substrate semantics. | Keep publication as downstream use of the substrate. |

## A.19.SOURCE-SET-SPACE-SUBSTRATE:10 - Rationale {#rationale}

The pattern chooses a narrow but sturdy center of gravity.

`A.19` already declares `CharacteristicSpace`. The missing load is not another free-floating space kind. It is the ref-position and relation stack that tells the reader:

- which declared source set is active;
- which declared space is named in the search-side position;
- which declared space is named in the outcome-side position;
- what `SpaceRefRelationKind` says about those two refs;
- and how much transparency, distortion, uncertainty, or error the line is honestly claiming.

That is why this pattern stops before interpretive views and before publication metadata. If it tried to say less, the load would collapse back into vague `space` or `projection` talk. If it tried to say more, it would start absorbing views, fronts, archives, shortlists, or shipping semantics that belong elsewhere.

## A.19.SOURCE-SET-SPACE-SUBSTRATE:11 - SoTA-Echoing {#sota-echoing}

| SoTA practice | Primary source(s) | Practice demand disciplined here | Practical safeguard bought | Adoption stance |
| --- | --- | --- | --- | --- |
| Modern multilevel evolutionary theory looks for one common substrate across several levels rather than forcing one tradition-local carrier to tell the whole story. | Vanchurin (2026) on generally covariant evolutionary dynamics; Warrell et al. (2024) on unified multilevel evolutionary frameworks. | `SS-0`, `SS-2`, `CC-A19SS-1`, `CC-A19SS-2`. | Keeps one neutral substrate beside `A.19`, so one archive, front, or publication face cannot silently stand in for the whole substrate declaration load. | **Adapt.** Keep one neutral substrate, but bind it to FPF declaration discipline. |
| Contemporary QD practice distinguishes feature/behavior space, quality/objective side, archive/repertoire set results, and local competition rather than treating one vague "space" as enough. | 2026 QD review; IJCAI 2024 stepping-stone results; MOUR-QD (2025). | `SS-1`, `SS-3`, `CC-A19SS-3`, `CC-A19SS-4`, worked slices `5.1` and `5.2`. | Forces search-side ref, outcome-side ref, and source-to-outcome relation to stay explicit, so downstream search/evaluation claims remain auditable. | **Adopt/Adapt.** Adopt the split; adapt it to FPF declared-source-set discipline. |
| Frontier QD and adjacent work increasingly use learned, adaptive, unstructured, and uncertainty-bearing spaces and qualifiers, so one heavy metric or transition stack should not be assumed everywhere. | Uncertain Quality-Diversity (2023); Extract-QD (2025); later adaptive-space and meta-competition lines. | `SS-4`, `SS-5`, `CC-A19SS-5`, `CC-A19SS-6`. | Makes uncertainty posture explicit while keeping declared map ref, metric, transition, and bridge-loss pins optional unless the case truly depends on them. | **Adopt/Adapt.** Adopt uncertainty honesty and optional heavier qualifiers; reject mandatory geometric monoculture. |
| Atlas and manifold-qualifier lines are useful in some cases, but they are not the default meaning of every source-set/space-substrate line. | UMAP 2024 review; 2024-2025 atlas and manifold-optimization lines. | `SS-5`, `SS-6`, boundary anti-case `5.3`, `CC-A19SS-8`. | Preserves substrate semantics so later interpretive or atlas views can help interpretation without quietly becoming the ontology. | **Adapt.** Keep atlas-form interpretation as a later specialization, not the substrate's ordinary center. |


## A.19.SOURCE-SET-SPACE-SUBSTRATE:End {#end}
