# E.4.FPF - FPF Edition Assembly: Publication Forms, Carriers and Access Routes: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## E.4.FPF:5 - Archetypal Grounding {#archetypal-grounding}

Tell: A later FPF edition updates its public front, Readme, Preface, ToC, and several pattern bodies. The FPF edition rebuildability record names one scoped edition, lists its Core pattern set, publication units and forms, exact presentation carriers, and access routes, records which entry text is only a projection, and points to `E.2.DA` for whole-FPF adequacy. It records Readme and Preface as publication units and names a presentation carrier only under an exact `PublicationFormBearingRelation`.

Show: A domain principle framework for any one practice depends on FPF Core and may cite architecture, representation, precision, and improvement patterns from FPF. Its publication units, forms, exact presentation carriers, and access routes belong to that DPF edition. Its package adequacy uses `E.4.DPF.DA`; FPF Core retains its transdisciplinary scope and its own amendment route.

Show: An FPF skill pack exposes pattern lookup, first-entry guidance, and short-use prompts. A versioned skill-pack bundle can be an access-facing `U.PresentationCarrier`; the service, endpoint, or assistant integration that returns it is an access route. Their descriptions name the FPF edition they expose and its refresh condition. Authority claims return to the named subject pattern and edition.

### E.4.FPF:5.1 - Rebuild an edition and catch a boundary error {#rebuild-an-edition-and-catch-a-boundary-error}

A steward is preparing **Cedar 2**, a fictional FPF edition for engineers who start from a working question. **Cedar 1** is its frozen predecessor. The example follows three changed bodies inside the full edition; all other bodies must carry forward unchanged.

The accepted complete sources are **DUA-2** for `C.11.DUA`, **PUR-2** for `E.11.PUR`, and **Ways-1** for `C.39`. DUA-2 replaces DUA-1 and includes continuing without optional advice; PUR-2 replaces PUR-1 and distinguishes applicability from recommendation. Ways-1 adds the method-development contribution between the existing `C.38` and `C.40` bodies. **Readme R2** adds their practical entry. **Preface P1** remains unchanged.

The first useful result is rebuildability record **RC2**, which gives the assembler these particular inputs and boundaries:

| Record content | Filled value |
|---|---|
| Edition and scope | Cedar 2; transdisciplinary FPF Core for the same reader and use as Cedar 1 |
| Predecessor | The complete Cedar 1 text, including Readme R1, Preface P1, index I1 and body collection K1 |
| Selected complete sources | DUA-2 replaces the whole C.11.DUA body; PUR-2 replaces the whole E.11.PUR body; Ways-1 inserts the whole C.39 body after C.38 and before C.40 |
| Publication units | Opening O2, Readme R2, unchanged Preface P1, derived index I2 and body collection K2 |
| Publication forms | A book arrangement: compact opening, contents and index, Readme, Preface, then bodies; a standalone Readme arrangement using R2 |
| Particular carriers | Cedar-2-book-a, one assembled Markdown file; Cedar-2-readme-a, one rendered HTML file |
| Access carrier and route | None selected for this assembly |
| Reader-facing scope account | O2 names engineers and their working questions; R2 offers starting examples and returns to the bodies; P1 explains the wider reasoning practice |
| Source and adequacy results | Q-DUA-2, Q-PUR-2 and Q-Ways-1 cover the three accepted source editions. Cedar 1's whole-edition assessment A1 does not assess Cedar 2 |
| Reconsideration condition | A selected source, predecessor span, declared form or receiving use changes |

Each carrier bears a form of the named units; neither file is the edition itself. The standalone HTML carries R2 without becoming another independently authored Readme. No access service has been selected.

Assembly replaces the two bounded bodies, inserts Ways-1, and derives I2 from that same membership. I2 must contain one row each for C.11.DUA, E.11.PUR and C.39, with no duplicate C.39 row. The full body inventory gains exactly C.39; all other membership and order stay as in Cedar 1.

A first candidate has exact copies of DUA-2, PUR-2 and Ways-1 and the expected index. It still fails. The Readme replacement ended two sentences inside P1 instead of at its boundary. The lost predecessor text was: “Start from your working question. Stop when the answer is sufficient; the entry list is not a required sequence.” The candidate has lost useful stopping guidance although every selected body matches its source.

The complete predecessor comparison exposes that unselected deletion. Stop the assembly at this failed preservation condition. Correct the Readme boundary and restore both sentences from frozen P1; do not rewrite the accepted pattern bodies. Rebuild and repeat source correspondence, the full inventory and the complete publication comparison.

In the repaired candidate, DUA-2, PUR-2 and Ways-1 still match their selected sources, I2 and K2 agree, R2 appears in both selected carriers, and P1 and every other unselected predecessor span are unchanged. The remaining differences are the two declared body replacements, one insertion and index row, R2 and its opening references. That is a completed construction with a stated preservation result under `E.4.PFIP`. Acceptance, publication and whole-FPF adequacy still require their own conclusions.

## E.4.FPF:6 - Bias-Annotation {#bias-annotation}

**Scope:** Limited to the publication units and forms, assembly, exact presentation carriers, access routes, and whole-framework evaluation route of an FPF edition. Repository layout, assembly tool, carrier split, and publication service remain implementation choices. A one-sentence repair that leaves these FPF-level values unchanged uses its direct wording and source route.

| Lens | Likely drift | Repair |
|---|---|---|
| Gov | A successful assembly or form check is read as acceptance, publication, availability, currentness, or adequacy. | Keep construction results separate from the decisions and relations that establish those claims. |
| Arch | The current all-in-one layout, source tree, or helper is treated as the only possible FPF architecture. | Preserve edition, selected Core, publication-unit/form, presentation-carrier, access-route, index/body, and unchanged-content invariants while allowing another repository, tool, carrier split, or publication service. |
| Onto-Epist | The edition, one publication unit, its form, the presentation carrier bearing it, an access route, the rebuildability record, the assembly Method, and performed assembly Work collapse into one object. | Name them separately where the distinction changes the claim. The record describes reconstruction inputs and routes; the assembly Work is the construction occurrence; the edition contains the coordinated framework content; and an exact `U.PresentationCarrier` bears the selected form. |
| Prag | Every small source edit is forced through FPF-level assembly paperwork, or exact source return is omitted to save effort. | Use this pattern only when FPF publication units, form, carriers, access routes, edition assembly, or whole-FPF evaluation are live; keep the record minimal but retain complete selected sources and unchanged-predecessor protection. |
| Did | Build apparatus meets the reader before a working question, or a smooth front hides where authoritative pattern content resumes. | Apply `E.11.PFP` to the reader-facing opening and keep paths, commands, digests, and diagnostics in maintainer evidence or tool help. |

## E.4.FPF:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | What fails | Repair |
|---|---|---|
| FPF as one DPF | FPF is treated as a domain package, so its first-principles and transdisciplinary burden disappears. | Use `E.4.FPF` for FPF form and `E.4.DPF` only for domain or local dependents. |
| Unit, form, route, or carrier as FPF | A Readme, Preface, ToC, logical index, publication form, all-in-one file or site, split-file bundle, skill-pack bundle, or MCP route is treated as the framework edition itself—or a publication unit or access route is called a carrier without an exact `U.PresentationCarrier` and bearing relation. | Record units, forms, exact presentation carriers, and access routes in their separate `FPFEditionRebuildabilityRecord` fields; keep authoritative claims in the Core patterns and their edition relations. |
| Rival FPF manifest | A DPF or LPF `FrameworkPackageManifest` or a duplicate unit, form, carrier, or route field is copied into FPF even though the rebuildability record already names the needed sources, publication units and forms, presentation carriers, access routes, projections, relations, and refresh route. | Use the `FPFEditionRebuildabilityRecord` fields and the assembly result; reopen this record decision only when a genuinely missing FPF value is shown. |
| Rival practical-entry declaration | Readme authoring, assembly, and validation keep separate ordinary-entry, card, scope, or limit lists, so the same key can change form or disappear without one reviewable change. | Consume the single current FPF declaration in `E.4.FPF`; change it only after the `E.11` reader-use comparison and propagate that one change to its true consumers. |
| Directly patched all-in-one carrier | Selected sources are correct, but the assembled carrier is edited outside the declared source assembly, so a mismatch or lost predecessor span can be hidden. | Assemble from the exact predecessor and complete selected sources with explicit replacement or insertion boundaries; stop on any source, index/body, boundary, or preservation mismatch. |
| Repository recipe as framework law | One helper, path layout, template set, insertion syntax, or campaign identifier becomes part of the public FPF Method. | State the semantic assembly invariants here; keep the current implementation recipe and examples in maintainer documentation or tool help. |
| Invisible FPF entry route | Readme or Preface helps adoption but never says what first-principles structures it foregrounds, what it leaves to the pattern bodies, or who it is written for. | Add a publication-unit structure account while preserving its thin projection status and keeping form and carrier claims separate. |
| Build apparatus as FPF front door | Generated-source comments, candidate records, digests, source paths, or machine identity fields appear before the reader can find a working question, or a new profile shifts an established compact ToC merely to display them. | Preserve the compact reader opening and direct Readme-first route; keep reproducibility and exact edition evidence in maintainer or package records, and project another cue only when its possible values change a named reader action. |
| Whole-FPF quality by local score | Good `E.21` values or successful landing are treated as whole-FPF adequacy. | Run `E.2.DA` for the scoped FPF object and declared use; use local results only as evidence loci. |
| DPF reverse dependency | A good DPF discovery is treated as a hidden Core dependency. | Propose a Core amendment that establishes the transdisciplinary contribution in Core, and update the affected Core patterns and edition relations while preserving dependency direction. |
| Access route as authority | A skill, MCP endpoint, retrieval index, or assistant integration is read as source, decision, work, or currentness authority, or the route is silently treated as the carrier it returns. | Record an exact skill-pack, index, or response carrier only when one exists; keep the service or route separate and route generated text, tool work, evidence, assurance, and refresh claims to their subject patterns. |

## E.4.FPF:10 - Rationale {#rationale}

FPF carries transdisciplinary first-principles distinctions that can seed and discipline many domain and local frameworks. Those frameworks supply their own domain or local subjects and practices.

That makes FPF form a real architecture concern. Separate publication units, forms, exact presentation carriers, access routes, and the framework edition so adoption work returns authority to the subject patterns. `E.4.DPF.DA` answers the DPF package question; `E.21` evaluates individual patterns; and `E.2.DA` evaluates whole-FPF adequacy.

## E.4.FPF:11 - SoTA-Echoing {#sota-echoing}

| Practice question | Best-known line | Serious alternative or default | Defect overcome and E.4.FPF mutation | Source roles and limits | Reopen condition |
| --- | --- | --- | --- | --- | --- |
| How can one authoritative framework-edition source produce several publication versions and access forms without identity drift or tool-specific framework law? | [RFC 9720, *RFC Formats and Versions*](https://www.rfc-editor.org/rfc/rfc9720.html) (2025), is the best-known-line candidate for this narrow publication-version question because one operating publication series distinguishes a definitive semantic version from rendered publication versions, seeks to preserve semantic content as fully as practicable while managing risk, and keeps controlled reissues and archives recoverable. | Independently editing split and all-in-one publications, or treating [Antora component-version](https://docs.antora.org/antora/latest/component-version/) and [Sphinx toctree](https://www.sphinx-doc.org/en/master/usage/restructuredtext/directives.html#table-of-contents) configuration as the framework's identity and law, are the serious defaults. | Separate editing drifts content and order; tool-defined identity hides the edition, publication unit, form, carrier, and route distinctions. **Adapt:** `FPFEditionRebuildabilityRecord`, the ordinary assembly method, Grounding, and `CC-FPF.9–12` require exact source membership, one logical order, several forms, semantic-preservation checks, duplicate or mismatch stops, and recoverable prior versions. **Reject:** RFCXML, Antora component ontology, Sphinx `toctree`, repository conventions, and any production tool as universal FPF machinery. | RFC 9720 supplies the best-known-line candidate because of its explicit definitive/rendered-version distinction and risk-managed preservation aim, not because it is an RFC. The linked Antora and Sphinx documentation are popular tool comparators only; their release or maintenance status supplies no SoTA rank. The selected transfer does not prove unchanged content or whole-FPF adequacy. | Reopen if a stronger current publication practice preserves exact source membership, index/body correspondence, semantic equivalence, and prior versions at lower reader or maintainer effort, or if an actual rebuild defeats this boundary. |

The current practical-entry declaration and the internal FPF quality, dependency, carrier, and access-route rules remain governed in `Solution`, checks, and Relations. They are not external SoTA evidence about this pattern. Official architecture-description references, current tool pages, fresh surveys, and lineage rows are omitted unless a future comparison shows the exact action-changing defect they are needed to expose.


## E.4.FPF:End {#end}
