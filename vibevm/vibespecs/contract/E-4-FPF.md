# E.4.FPF - FPF Edition Assembly: Publication Forms, Carriers and Access Routes {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Architectural (A)
> **Status:** Stable
> **Normativity:** Normative unless marked informative.

## E.4.FPF:1 - Problem frame {#problem-frame}

Use this pattern when an FPF steward, framework author, reviewer, or AI agent must assemble, expose, or evaluate FPF itself as one framework edition and distinguish it from its publication units, forms, presentation carriers, access routes, and domain or local dependents.

Primary `EntityOfConcern`: the scoped FPF edition (`FirstPrinciplesFrameworkEdition`) being assembled, exposed, or evaluated. The first useful output is a record for rebuilding that edition. It names the first-principles scope, selected Core patterns, recurring cross-domain problems and reusable solution moves, selected publication units and forms, exact publication- or access-facing `U.PresentationCarrier` values, access routes, edition relations, and the applicable whole-FPF quality result from `E.2.DA`. Add an exact competing-reading reference only under the full F.19:4 test: independent local ground, plausibility for the intended reader, a change in truth, understanding, or use, and the smallest clear correction.

Use this when the work changes FPF publication units or forms—such as the public opening, Readme, Preface, ToC, first-entry view, cards, or split pattern collection—or assembles the exact physical or digital carrier that bears them, such as an all-in-one file, site snapshot, volume, or bundle. Use it also when a skill-pack carrier or an MCP, retrieval, search, or assistant access route exposes the edition. When a public presentation carrier is in scope, use `E.11.PFP` for its common reader-facing form and this pattern for FPF-specific source selection and assembly. Use `E.4.DPF` instead when the framework is a domain or local framework grounded in FPF. Use `E.4` when the live question is only family placement and routing among framework members.

The practical payoff is direct. A reader can identify the FPF edition, the reader-facing units and forms that expose it, and the exact presentation carriers that bear them. The same account names its access routes and whole-FPF adequacy route. A DPF or local framework may depend on FPF Core while remaining its own framework edition.

## E.4.FPF:2 - Problem {#problem}

After DPF and local-framework publication forms become explicit, FPF itself can fall into the opposite omission: DPF packages get careful publication-unit, form, carrier, relation, naming, quality, and refresh rules, while FPF is treated as if its form were self-evident because it is "the main spec".

That creates several failures:

- an all-in-one file or site, one of its Readme, Preface, ToC, pattern-body, card, or first-entry units, a skill-pack bundle, or an MCP route is mistaken for the FPF edition itself;
- FPF is described as one more DPF, losing the first-principles and transdisciplinary burden that makes DPFs possible;
- whole-FPF quality is checked by local pattern scores, landing status, or DPF package scales instead of `E.2.DA`;
- adoption units, forms, or access surfaces grow user-facing explanations that quietly become shadow authority beside subject patterns;
- skill or MCP access makes FPF look like a callable service, tool permission layer, or runtime dependency rather than a framework edition reached through an access route or borne by an exact access-facing presentation carrier.

Use an FPF-specific form rule. FPF must keep first-principles distinctions usable across domains while allowing domain and local frameworks to grow from it; `E.4.DPF` governs those dependent frameworks.

## E.4.FPF:3 - Forces {#forces}

| Force | Tension |
|---|---|
| First principles vs domain knowledge | FPF must carry transdisciplinary ontology, epistemology, evidence, architecture, decision, work, publication, and improvement distinctions without becoming a doctrine of one domain. |
| Public adoption vs subject-pattern authority | Readme, Preface, examples, cards, skills, and MCP access must help new users without becoming a second spec. |
| Core stability vs evolution | FPF needs stable dependability for downstream DPFs, while the framework remains open to new patterns, better terminology, and source-front movement. |
| Pattern-set quality vs whole-framework quality | Individual `E.21` results matter, but they do not equal whole-FPF Pillar adequacy. |
| Carrier plurality vs identity | The same FPF edition can use several publication units and forms, several exact presentation carriers, and several access routes; those different objects must not create competing FPFs or collapse into one another. |
| Access convenience vs architecture clarity | A callable access route can make FPF easier to use while hiding edition, currentness, source, and authority boundaries. |

## E.4.FPF:4 - Solution {#solution}

Treat FPF as a `FirstPrinciplesFrameworkEdition`: one transdisciplinary edition with a selected Core pattern set and a stated first-principles scope. Record its recurring cross-domain problems, reusable solution moves, edition relations, publication units and forms, exact presentation carriers, and access routes under their direct subjects and relations, and coordinate them within that edition. Units and forms expose selected content; presentation carriers bear the selected forms; access routes help an audience or system reach them.

Use these local names:

| Local name | Kind and use |
|---|---|
| `FirstPrinciplesFrameworkEdition` | One scoped FPF edition carrying transdisciplinary first-principles distinctions and the Core pattern set that downstream frameworks depend on. |
| `FPFCorePatternSet` | The selected subject pattern set for the edition. Readme, Preface, ToC, publication form, presentation carrier, skill-pack bundle, and access route use the direct local names below. |
| `FPFPublicationUnit` | Local reference for one selected content unit of the FPF edition, such as its public opening, Readme, Preface, ToC, first-entry view, card set, or pattern-body collection. The unit keeps the kind and identity supplied by its direct source; an exact carrier that bears its form is named separately as an `FPFPublicationCarrier`. |
| `FPFPublicationCarrier` | Local designation for one exact physical or digital `U.PresentationCarrier` that actually bears a selected FPF publication form. `PublicationFormBearingRelation` relates that carrier to the form it bears. A versioned all-in-one file, PDF volume, website snapshot, or bundle may qualify. Readme, Preface, ToC, logical index, and pattern collection name publication units or forms; name an independently identified carrier when one bears them. |
| `FPFAccessCarrier` | Local designation for one exact `U.PresentationCarrier` that bears an access-facing FPF form, such as a versioned skill-pack bundle, retrieval-index file, or response document. Services, endpoints, retrieval routes, search functions, and assistant integrations use `FPFAccessRoute`; name a returned carrier separately. |
| `FPFAccessRoute` | One identified service, endpoint, retrieval, search, or assistant route through which a declared audience or system may obtain the selected edition or reach a named carrier. Actual access, availability, reliance, authority, and Work use their own direct predicates and evidence. |
| `FPFEditionRebuildabilityRecord` | Claim-bearing record for one FPF edition. It names the exact sources, publication units and forms, presentation carriers, access routes, edition relations, projections, quality and currentness results, and refresh routes needed to reconstruct that edition's public form. A blocked-overread reference is optional and must pass `F.19`'s grounded-contribution test. |
| `FPFLevelAdequacyAssertionRef` | Exact whole-FPF adequacy assertion under the predicate defined in `E.2.DA`; individual pattern-quality assertions still use `E.21`, and DRR-quality assertions still use `E.9.DA`. |

The progressive-minimum F.18 NameCard `NC-FPF-EDITION-REBUILDABILITY-RECORD` names the family of claim-bearing records defined by the `FPFEditionRebuildabilityRecord` row and declaration in `E.4.FPF:4`; that section is also its subject-pattern locator. This is an ordinary record family. Keep a particular record, its Markdown carrier, the assembly Method, the performed assembly Work, and an actual E.10 `Map` under their direct kinds.

The NameCard uses `FPFCoreReferenceScheme` by value. In that scheme, `FPFEditionRebuildabilityRecord` designates only the record family whose instances concern one FPF edition and name the exact sources, publication units and forms, presentation carriers, access routes, relations, projections, quality and currentness results, and refresh routes needed to reconstruct its public form. No Bridge is claimed. Use the Tech designation in edition and rebuildability records, maintainer diagnostics, and direct consumers; use the Plain designation “record for rebuilding one FPF edition” in ordinary practitioner explanation.

The name comparison covers `FPFEditionRebuildabilityRecord`, `FPFEditionAssemblyRecord`, `FPFEditionSourceAndCarrierIndex`, and the predecessor `FPFFormMap`: rebuildability-record, assembly-record, index, and mapping-Method readings. `AssemblyRecord` is too narrow because the record also names relations, projections, quality, currentness, and refresh inputs; assembly itself is the subsequent operation. `SourceAndCarrierIndex` is too narrow because the record must also keep publication units, forms, and access routes distinct. `FormMap` is retired rather than kept as an alias because E.10 reserves `Map` for a mapping `U.Method`. Reopen this settlement if the named family becomes such a Method, ceases to concern one edition's reconstruction inputs and routes, `FPFCoreReferenceScheme` or the local-sense claim changes, a direct consumer needs another distinction, or a narrower admitted record kind covers every current field and use.

**Current FPF practical-entry declaration.** Apply `E.11`'s content test to every proposed example. The current English FPF Readme declaration is:

| Semantic key | Selected public form |
| --- | --- |
| `NAMING` | Ordinary practical entry |
| `SYSTEM-RECOGNITION` | Ordinary practical entry |
| `TIME` | Ordinary practical entry |
| `CAUSAL-USE` | Ordinary practical entry |
| `MEASUREMENT` | Ordinary practical entry |
| `MATHEMATICAL-MODELING` | Ordinary practical entry |
| `LIVE-WORK-STEERING` | Ordinary practical entry |
| `METHOD-RECOVERY` | Ordinary practical entry |
| `WORK-OPPORTUNITY` | Ordinary practical entry |
| `PROFESSIONAL-RESULT` | Ordinary practical entry |
| `UNFAMILIAR-THEORY` | Practical-Use Card |
| `PHYSICAL-RESULT` | Practical-Use Card |
| `ARCHITECTURE` | Practical-Use Card |
| `PRACTICE-ARCHITECTURE` | Practical-Use Card |
| `WORKING-DOCUMENTS` | Practical-Use Card |
| `COMMUNICATION-FOR-USE` | Ordinary practical entry |
| `OPTION-COMPARISON` | Practical-Use Card |
| `RESULT-TO-NEXT-MOVE` | Ordinary practical entry |
| `ACTUAL-TEMPORAL-STRUCTURE` | Ordinary practical entry |
| `CONSEQUENCE-BEARERS` | Ordinary practical entry |
| `PROBLEM-SHAPING` | Practical-Use Card |
| `IMPROVEMENT` | Practical-Use Card |
| `WORDING` | Practical-Use Card |
| `SOTA-PORTFOLIO` | Practical-Use Card |
| `SYSTEM-DELIMITATION` | Practical-Use Card |

This is the one FPF declaration consumed by Readme authoring, assembly, and validation; do not maintain another ordinary-entry or card list. The Readme must say that FPF and the applicable DPF or LPF can answer a much wider range of questions and must return a reader whose question fits no example to the Table of Contents, another finding aid, or the direct patterns.

Related questions remain recoverable without a separate selectable entry for each topic: `CAPABILITY-DEVELOPMENT` is carried by `PRACTICE-ARCHITECTURE` and `IMPROVEMENT`; `COSTLY-ACTION` is carried by `OPTION-COMPARISON`; `DESCRIPTION-USE` is carried by `WORKING-DOCUMENTS`; and `DPF-AUTHORING` is carried by `SOTA-PORTFOLIO`.

`UNFAMILIAR-THEORY` connects recovering a construction and argument with transfer to the project's representation. `PHYSICAL-RESULT` connects physical modeling, mathematics, computation and realization, including returns when one contribution changes. Their mantras retain those dependencies while the direct patterns supply the operations.

`WORK-OPPORTUNITY` starts at the first missing contribution and can end at a local result, an exact gap or continued work without advice. Its conditional returns do not prescribe a traversal through every linked pattern; its Readme explanation uses the ordinary-entry form.

`TIME`, `CAUSAL-USE`, `MEASUREMENT`, and `MATHEMATICAL-MODELING` are ordinary examples because each starts with one direct pattern and can stop at its first useful result without a cross-pattern mantra; no `MODELING-FOR-ACTION` card joins them. `LIVE-WORK-STEERING` and `METHOD-RECOVERY` are ordinary examples for the same reason: each begins at one direct pattern and may stop at its first useful result or blocker. `PROFESSIONAL-RESULT` is also ordinary: it starts with `A.15.9`, tests an already-available result before any new request, and can stop at bounded reuse, the smallest missing-result request, or a blocker without a cross-pattern mantra.

`COMMUNICATION-FOR-USE` starts with the communication and its intended use. Its ordinary explanation distinguishes interpretation, response, later action and effect, then opens a wording, representation, evidence, causal or repair question only when that question is needed. The reader can stop at a supported use or an explicit blocker.

`RESULT-TO-NEXT-MOVE` starts with the obtained result and its direct pattern. Its ordinary explanation preserves the conditions for a later interpretation, reliance, characterization, comparison or live-choice question and stops before a question that is not current.

`CONSEQUENCE-BEARERS` starts with the bounded consequence account under `A.1.CSD`. Its ordinary explanation retains the boundary challenge, conditional systemhood check, separate obtaining and modal paths, each bearer's changes and uncertainty, and the return when the receiving use changes.

`ACTUAL-TEMPORAL-STRUCTURE` starts with what the temporal claim concerns. Its ordinary explanation distinguishes actual subjects and obtaining relations, a selected structure and its account, and future specifications or representations. A coordination trial follows only when it can change the decision and warrants its burden; otherwise the reader stops at the supported answer or missing basis.

`PUBLICATION-FORM` and `DPF-SUITE-REFERENCE` remain direct locators to `E.11.PFP` and `E.11.DSG`, not selected examples. Exact content stays in those direct patterns; the Readme carries only the recognition, cross-pattern dependency, and return needed for discoverability.

For every card row, keep the card and its practical-use guidance findable by the same key. The current English FPF counts whitespace-separated tokens and requires at most 80 for a card mantra and 220 for a complete compact card. These are maxima with no minimum length. They are calibrated publication envelopes for this English FPF, not psychometric thresholds or universal DPF, LPF, or translated-publication limits. Reopen the smallest affected declaration row and consumer when a cold-reader replay loses a choice-changing distinction, a useful card cannot fit without copying direct-pattern apparatus, or either ceiling can be lowered without losing use value. The optional `@FPFReadme` support records may carry FPF links but do not define shared conformance.
Create the FPF edition rebuildability record with this shape when FPF itself is being assembled, republished, exposed, or evaluated:

```text
FPFEditionRebuildabilityRecord:
  recordRef: <exact rebuildability-record identifier>
  firstPrinciplesFrameworkEditionRef: <FPF edition named by value>
  firstPrinciplesScopeRef: <transdisciplinary scope and non-domain boundary>
  selectedCorePatternSetRefs: <exact selected complete pattern-source refs or declared sections of an accepted source edition>
  selectedFirstPrinciplesProblemSituationRefs: <recurring cross-domain problem situations and forces rendered by the edition>
  selectedFirstPrinciplesSolutionMoveRefs: <reusable solution moves, consequences, and repair routes rendered by the edition>
  selectedPublicationUnitRefs: <selected FPF content-unit refs, for example: public opening | standalone Readme | Preface | ToC | pattern-body collection | card set>
  selectedPublicationFormRefs: <exact arrangements or rendering conventions selected to express those units for named uses>
  selectedPublicationCarrierRefs: <exact U.PresentationCarrier refs that bear selected public forms, for example: all-in-one Markdown file | PDF volume | website snapshot | split-file bundle>
  selectedAccessCarrierRefs: <exact U.PresentationCarrier refs that bear access-facing forms, for example: skill-pack bundle | retrieval-index file | response document>
  selectedAccessRouteRefs: <identified services or routes, for example: MCP service | retrieval route | search function | assistant integration>
  relationAndEditionRefs: <direct relation and edition assertions, including edition pins and dependency boundaries; E.4.PFR rows only for a named maintenance consumer>
  firstEntryAndProjectionRefs: <E.11.PFP, E.11, E.17, I.2, Readme, Preface, ToC, and other contribution or projection loci>
  publicationSelfRenderingRefs: <statements in selected publication units of reader, selected first-principles structures, deliberate coarsening, abstraction, omission or deferral, and return to subject patterns, for example: Readme | Preface | ToC>
  qualityAndImprovementRefs: <E.2.DA for FPF-level adequacy; E.21, E.23, and E.9.DA as evidence or local routes>
  currentnessAndRefreshRefs: <G.11 plus exact source-use and currentness records>
  blockedOverreadRefs: <optional exact refs to explanatory guards admitted by F.19:4's plausible-reader and grounded-contribution test>
```

These fields preserve the existing rebuildability content while making unit, form, presentation-carrier, and access-route references explicit. `firstPrinciplesFrameworkEditionRef` resolves to the edition record for the selected FPF edition; `relationAndEditionRefs` resolves that edition's status and dependency assertions. Keep DPF or LPF package records separate instead of copying them into this record. The rebuildability record supplies reconstruction inputs; downstream assembly and use claims come from their direct results and relations.

The ordinary method is:

1. Name the FPF edition or edition candidate being assembled by its stable designation and exact edition record.
2. State the first-principles scope: FPF supplies transdisciplinary distinctions that can be reused across domains. Domain doctrines remain with their DPFs; the declared scope sets the useful coverage boundary.
3. Identify the selected Core pattern set and any companion or projection loci that expose it.
4. When a public presentation carrier is being assembled or checked, use `E.11.PFP` for the common publication form. Keep a product-declared compact opening and separate exact title and Readme H1 values. Represent Readme and Preface in the product's established ToC grammar before one logical pattern index. Keep one explicitly non-exhaustive practical-entry set, five-field ordinary examples, six-field selected cards, and one integrated source-hazard plus rendered-structure check. Apply `E.11`'s use test before assigning card form, and use the current FPF declaration above for every selected key and form plus the English reading-burden measure and two limits. Add another public cue only when a named reader decision or action needs it. For the established all-in-one FPF carrier, add Readme through the same non-pattern table grammar already used for Preface, preserve the compact pre-ToC shape, and keep the exact line-position and native-ToC assertions in the builder regression. Keep FPF-specific source selection, body order, and assembly here; the carrier and form remain separate from the FPF edition.
5. Separate the objects before recording them. Readme, Preface, ToC, the public opening, cards, and the pattern collection are publication units; their selected arrangement is the publication form. Name the exact `U.PresentationCarrier`—for example, a versioned Markdown file, site snapshot, PDF volume, split-file bundle, skill-pack bundle, index file, or response document—only when it actually bears that form. Record an MCP service, retrieval route, search function, or assistant integration as an access route; name any returned carrier separately. Record these units, forms, carriers, and routes as distinct subjects and relations for the `FirstPrinciplesFrameworkEdition`.
6. State relation, dependency, edition, deprecation, supersession, publication, and access claims directly. Open an `E.4.PFR` row only for a named maintenance consumer.
7. Keep downstream direction clear: DPFs and local practice frameworks may depend on FPF Core. Incorporate an accepted transdisciplinary contribution through a deliberate Core amendment before Core uses it; the amended Core supplies that contribution without depending on the DPF or local framework.
8. Fill the existing `FPFEditionRebuildabilityRecord` with exact selected source, publication-unit, publication-form, presentation-carrier, access-route, relation, practical-entry declaration, currentness, and refresh references. Make the Readme assembly and its checks consume the same declaration rather than another key or card list. Do not create a rival manifest or duplicate rebuildability account.
9. Assemble the all-in-one edition candidate from the exact predecessor, the selected edition record, the matching `FPFEditionRebuildabilityRecord`, and every selected complete pattern source. Give each replacement or insertion an explicit boundary. Derive the logical index and pattern bodies from the same selection, verify one index row per selected PatternID, report which source supplied each assembled unit, and verify that every unselected predecessor span is unchanged. A missing or duplicate record, unresolved ref, index/body mismatch, ambiguous boundary, source mismatch, or changed unselected span stops construction. The construction result reports the assembled candidate and source correspondence; acceptance and publication require their separate decisions and relations. Keep repository paths, commands, helper options, template names, and insertion syntax in maintainer documentation or the selected tool's help.
10. When the assembled publication claims accepted-source integration or continuity with its predecessor, use `E.4.PFIP` for that comparison. For whole-FPF adequacy, use `E.2.DA` over the scoped FPF object and declared use. Use `E.21` for individual pattern bodies, `E.9.DA` for a DRR, and `E.4.DPF.DA` only for DPF or local-framework packages.
11. For first-entry and reader-facing exposure, use `E.11` and `E.17`; keep their projection text thin enough that subject pattern authority remains in the patterns.
12. Make the FPF Readme, Preface, and ToC publication units structure-account-aware: state the reader and use they serve, which first-principles structures they foreground, what they deliberately coarsen, abstract, omit, or defer, and where the reader returns for subject-pattern detail. Use `E.11.PFP` for the common publication-form structure. Preserve the product-declared compact opening, put the direct Readme/Preface route before the logical pattern index, and keep source paths, digests, machine identity blocks, candidate records, and build instructions outside reader front matter.
13. For source-front, currentness, and refresh claims, use the direct `G.2` and `G.11` assertions. Publication units, forms, presentation carriers, and access routes contribute only their stated publication or access facts.
14. For skill packs or MCP-backed access, expose edition identity, dependency boundary, and currentness or refusal conditions. Distinguish the exact skill-pack, index, or response carrier from the service or route that returns it. Generated candidate text intended for architecture use goes to `C.35`; keep tool capability and Work claims separate, using the applicable tool pattern for the former and `A.15` plus the pattern for the exact Work for the latter; use the applicable patterns for assurance, evidence, and decision-authority claims.

Use this quick routing test:

| Live question | Use |
|---|---|
| "What is the form of FPF itself, and how are publication units, forms, presentation carriers, and access routes separated from the framework edition?" | `E.4.FPF` |
| "Which public title and edition cue, unit order, logical index, and practical Readme entry form should this FPF publication use?" | `E.11.PFP` |
| "How is this all-in-one FPF edition candidate rebuilt from its selected sources without changing unselected predecessor content?" | `E.4.FPF`; use `E.4.PFIP` when accepted-source integration or predecessor continuity is claimed |
| "Does this whole-FPF object realize the Pillars for a declared use?" | `E.2.DA` |
| "How do FPF, a DPF, and a local framework depend on one another?" | `E.4`; state the dependency directly and use `E.4.PFR` only for a named maintenance consumer |
| "How do we author a domain or local framework grounded in FPF?" | `E.4.DPF` |
| "Is this DPF package good enough for one declared domain or local use?" | `E.4.DPF.DA` |
| "Is this individual pattern body good enough?" | `E.21` |
| "How do new users find and read FPF?" | `E.11` and `E.17` |

## E.4.FPF:7 - Conformance checklist {#conformance-checklist}

| Check | Passing condition |
|---|---|
| CC-FPF.1 Edition named | @fact:CC-FPF-1 The scoped FPF edition or selected FPF object is named by value. @status:spec/done |
| CC-FPF.2 First-principles scope explicit | @fact:CC-FPF-2 The text states that FPF is transdisciplinary first-principles material, including cross-domain problem-situation and solution-move architecture; domain and local framework subjects use their own editions. @status:spec/done |
| CC-FPF.3 Core, units, forms, carriers, and routes separated | @fact:CC-FPF-3 Core pattern set, publication units, publication forms, exact `U.PresentationCarrier` values, access routes, relation records, source and currentness records, and quality records remain distinct. @status:spec/done |
| CC-FPF.4 Dependency direction protected | @fact:CC-FPF-4 DPFs and local frameworks may depend on FPF Core. A transdisciplinary contribution enters through a deliberate Core amendment whose content no longer depends on the DPF or local framework. @status:spec/done |
| CC-FPF.5 Quality route correct | @fact:CC-FPF-5 Whole-FPF adequacy uses `E.2.DA`; individual patterns use `E.21`; DPF packages use `E.4.DPF.DA`; DRR uses `E.9.DA`. @status:spec/done |
| CC-FPF.6 Publication thinness preserved | @fact:CC-FPF-6 Readme, Preface, ToC, cards, and other projection units help entry and return semantic authority to subject patterns; an exact `U.PresentationCarrier` and bearing relation support each carrier claim. @status:spec/done |
| CC-FPF.7 Access carrier and route bounded | @fact:CC-FPF-7 Each named access carrier is an exact `U.PresentationCarrier` that bears an access-facing form. MCP services, retrieval and search routes, and assistant integrations are recorded separately and expose edition identity, currentness, and refusal conditions. Framework authority, runtime dependency, work permission, and actual access claims use their own direct predicates and evidence. @status:spec/done |
| CC-FPF.8 Refresh relation visible | @fact:CC-FPF-8 Source-front, edition, entry-use, currentness, and evaluation changes identify the affected assertion and exact subject pattern, such as `G.2`, `G.11`, `E.2.DA`, or `E.21`. @status:spec/done |
| CC-FPF.9 Unit, form, and carrier boundary visible | @fact:CC-FPF-9 Each Readme, Preface, ToC, or equivalent FPF publication unit states the reader and use, the first-principles route it foregrounds, what it coarsens or leaves out, and where subject-pattern detail resumes. The selected publication form arranges those units; an exact all-in-one Markdown or other `U.PresentationCarrier` bears that form without exposing build metadata as reader front matter. @status:spec/done |
| CC-FPF.10 Common form reused | @fact:CC-FPF-10 The selected public form satisfies `E.11.PFP` for the compact product-declared opening, distinct exact title and Readme H1, Readme and Preface entries in the established ToC grammar, one logical index, practical entries, and any choice-relevant cue. This pattern retains FPF-specific sources, units, body order, carrier and route selection, and builder regressions for the established compact-front line shape and native ToC grammar. @status:spec/done |
| CC-FPF.11 Existing rebuildability record sufficient | @fact:CC-FPF-11 One `FPFEditionRebuildabilityRecord` carries the exact selected source, publication-unit, publication-form, presentation-carrier, access-route, relation, projection, and refresh references. Add another manifest, field, or record only after showing a genuinely missing FPF value. @status:spec/done |
| CC-FPF.12 Deterministic source assembly | @fact:CC-FPF-12 The all-in-one edition candidate uses the exact predecessor, selected edition record, matching `FPFEditionRebuildabilityRecord`, selected complete pattern sources, and explicit replacement or insertion boundaries. One selection drives both index and bodies; source correspondence is reported; every unselected predecessor span is unchanged; any identity, source, index/body, boundary, or preservation mismatch stops construction before an acceptance or publication claim. Repository filenames, commands, helper options, and template syntax remain in maintainer documentation or tool help rather than this reusable rule. @status:spec/done |
| CC-FPF.13 One practical-entry declaration | @fact:CC-FPF-13 One current FPF declaration covers all selectable Readme examples, assigns each exactly one ordinary-entry or card form, and supplies the same calibrated 80-token mantra and 220-token compact-card whitespace guard to authoring, assembly, and validation. The Readme states that the ordinary entries and cross-pattern cards selected by the declaration in §4 are non-exhaustive. Every card passes `E.11`'s mnemonic-gain test, remains linked by key to its guidance and optional expansion, and returns to its direct patterns. Authoring, assembly, and validation consume this declaration as the sole source for key, card, and coverage assignments. @status:spec/done |

## E.4.FPF:9 - Consequences {#consequences}

FPF adoption becomes easier to reproduce because authors can build Readme, Preface, ToC, and pattern-body publication units; arrange them in all-in-one or split forms; bear those forms on exact files, sites, volumes, or bundles; and provide skill, MCP, search, or retrieval access without changing what FPF is. The same declaration keeps FPF's few direct and cross-pattern examples, their forms, and the two reading-burden limits aligned across authoring, assembly, and validation. Explicit non-exhaustive wording lets the examples promote pattern-language use without turning the Readme into a catalogue or forcing a card onto every entry.

The cost is one extra distinction for stewards: whole-FPF form is not the same problem as DPF authoring, package adequacy, individual pattern quality, or first-entry publication. That cost is acceptable because those problems have different evidence and failure modes.

## E.4.FPF:12 - Relations {#relations}

- **Specializes:** `E.4` for the case where the framework family member under form work is FPF itself.
- **Builds on:** `E.2` Pillars through `E.2.DA` for whole-FPF adequacy.
- **Coordinates with:** `E.4.PFR` when a named maintenance consumer needs a reusable relation, edition, dependency, publication, access, deprecation, or supersession record; otherwise state the direct relation assertion.
- **Coordinates with:** `E.4.DPF` and `E.4.DPF.DA` as sibling patterns for domain and local frameworks, not as FPF-level substitutes.
- **Coordinates with:** `E.11.PFP` for the common framework publication form and with `E.11`, `E.17`, and `I.2` for first entry, projection, and publication or access use.
- **Coordinates with:** `G.2`, `G.11`, `C.33`, `C.34`, and `C.35` for source, currentness, structural preservation, and admission of generated or discovered results for architecture use.
- **Coordinates with:** `E.21`, `E.22`, `E.23`, and `E.9.DA` when individual pattern quality, evaluation framing, improvement loops, or DRR adequacy provide evidence for FPF-level changes.


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/E-4#root, spec://ai.lev/fpf-spec/contract/E-2-DA#root, spec://ai.lev/fpf-spec/contract/E-11#root, spec://ai.lev/fpf-spec/contract/E-17#root, spec://ai.lev/fpf-spec/contract/E-21#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/E-4-PFAD#root, spec://ai.lev/fpf-spec/contract/E-4-PFR#root, spec://ai.lev/fpf-spec/contract/E-4-DPF#root, spec://ai.lev/fpf-spec/contract/E-4-DPF-DA#root, spec://ai.lev/fpf-spec/contract/G-11#root, spec://ai.lev/fpf-spec/contract/F-18#root, spec://ai.lev/fpf-spec/contract/F-19#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/E-11-PFP#root, spec://ai.lev/fpf-spec/contract/E-4#root, spec://ai.lev/fpf-spec/contract/E-4-PFIP#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/E-4-FPF
