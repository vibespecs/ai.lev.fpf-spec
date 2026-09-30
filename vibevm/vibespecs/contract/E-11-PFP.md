# E.11.PFP - Framework Publication Form Profile for Markdown {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Specialization of E.11
> **Status:** Stable
> **Normativity:** Normative unless marked informative.

## E.11.PFP:1 - Problem frame {#problem-frame}

Use this pattern when one FPF, DPF, or LPF edition needs a public Markdown form that a cold reader can enter and a small deterministic checker can recognize. The framework's pattern set, product boundary, and edition values must already be selected for the publication being assembled or checked.

The first useful result is a publication arrangement in which readers can find both the whole-framework explanation and each directly useful pattern. Name the edition source and public units; locate the twelve substantive answers under section 4.7 and each missing, reordered, duplicated, unresolved, or mismatched form element. A passing form check does not accept the edition, prove framework adequacy, identify a carrier, or establish a publication occurrence.

Do not use this pattern to decide whether one pattern set is a framework, whether a catalogue or guide is another product, or whether an edition is current or available. Use the E.4 family for the product and framework boundary, E.24.PUB for publication occurrence and carrier relations, and the applicable decision, quality, and currentness patterns for those claims.

## E.11.PFP:2 - Problem {#problem}

FPF-family publications can expose the same useful material through different headings, edition labels, index layouts, and Readme cards. A familiar reader can compensate. A cold reader or parser cannot reliably tell which edition is present, which index is authoritative, whether several Part tables form one index, or whether a support table is a rival front door.

Even a navigable collection can leave readers unable to explain what its Methods accomplish together, why they are arranged that way, which assumptions and sources support several patterns, or how a narrower profile changes use. Those answers can be scattered through development notes and disappear when the pattern bodies are published.

The opposite repair is also harmful. A rigid carrier template can put authorship, credits, dates, status, dependencies, build details, and maintainer records ahead of the reader's question whether or not those facts change the reader's choice. It can also force a catalogue, inquiry programme, guide, or other adjacent product to pretend that it is a framework edition. The common form must therefore be exact where shared recognition matters, practitioner-first in its opening, and explicitly limited to framework editions.

## E.11.PFP:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Cold-reader entry | Stable labels and order reduce search cost, but edition administration must not displace practical entry or the pattern bodies. |
| Exact edition return | Readers need a stable public designation and locator, while dates, filenames, statuses, and build digests must not become edition identity. |
| One logical index | FPF-family editions need one authoritative pattern index, while visible Part or placement groups remain useful. |
| Product variation | FPF, DPF, and LPF editions share a front form, but their body, reference tail, and choice-relevant public cues differ. |
| Whole and direct use | Readers need the language's shared problem, organization, reasons, and limits, while a direct question may be answered by one pattern. |
| Product boundary | Support units may belong to one framework product; independently useful adjacent products need a truthful boundary and public return. |
| Deterministic checking | Syntax checks should be reproducible, but they must not infer table purpose, product truth, or reader value from prose. |
| Form and carrier separation | One form may be borne by several carriers, and one outer carrier may expose several products, without merging their identities. |
| Accessibility and translation | Predictable headings and navigation aid many readers and tools, while one English label set cannot silently stand in for every language or access need. |

## E.11.PFP:4 - Solution {#solution}

Apply one common reader-facing publication form to one FPF, DPF, or LPF edition. The profile is the reusable rule for that form. It is not the form itself, the presentation carrier that bears the form, the edition expressed by it, or the publication occurrence that makes the edition available.

### E.11.PFP:4.1 - Preserve the compact product opening {#preserve-the-compact-product-opening}

For an all-in-one Markdown publication, preserve the product-declared compact opening and use this H1 route:

1. `# <product-declared publication title>`;
2. `# Table of Contents`;
3. the exact product-declared Readme H1;
4. the exact product-declared Preface H1;
5. the pattern bodies or pattern collection in the order selected by that edition; and
6. reference and maintenance material under headings declared by the product pattern.

The title and Readme H1 are separate product declarations. A checker receives both exact strings; it does not derive the Readme H1 by concatenating `Readme` to a longer carrier title. The common profile does not insert a metadata block, edition record, warning, or other lines into a compact predecessor opening merely to make products look alike. A product-specific builder may pin a compact front shape, including the line at which the ToC begins, when that shape protects an established reader entry.

Between the title and ToC, retain only the shortest public cues already justified by product use. An exact edition designation or locator belongs there only when its possible values change the reader's next use, reliance, return, language, dependency, or access choice. When such a cue is present, project it from one product-owned edition or relation record; do not maintain a second editable copy. Add authorship, credit, date, dependency, language, access, or a product-declared maintenance status, support window, or currentness window only under the same next-working-move test. A date is a cue, not edition identity, and a visible status or window is not evidence of acceptance, currentness, maintenance, availability, access, or authorization.

When readers copy, adapt, translate or redistribute a framework publication, its copyright-license notice tells them what permission the rights holder grants. Identify the covered material, rights holder and chosen license, and make the license text reachable from a standalone copy. Project a compact notice from the product's chosen licensing terms; retain applicable attribution and mark any third-party or differently licensed material. The author of an independently created DPF or LPF chooses its license. Where copyright permission is needed, reuse of another framework's protected expression is governed by that material's terms; applicable copyright exceptions remain available. Adopting its methods or publication form does not impose that framework's license on the new work.

Reader front matter extends from the opening title through the Readme and Preface up to the first pattern-body collection H1. It must not contain campaign keys; candidate, review, or result identifiers; local disk or repository paths; source or candidate digests; Git commits or blobs; generated comments; build commands; machine warnings; or "do not edit" instructions. Detailed edition, provenance, rebuildability, and maintenance records remain adjacent maintainer evidence or product-declared reference-tail material unless a separately selected public use justifies a reader-facing projection.

### E.11.PFP:4.2 - Put public units into the established Table of Contents {#put-public-units-into-the-established-table-of-contents}

Immediately after the single `# Table of Contents` H1, continue the product's established ToC grammar. Represent the exact Readme and Preface before the logical pattern index using the same kind of labelled segment and rows already used for non-pattern units in that product. When an established ToC already represents Preface and pattern groups, add Readme there; do not invent a generic `Publication route`, a second mini-menu, or a new table shape. A non-pattern publication unit receives no fabricated PatternID. Its product-declared entry remains mechanically recognizable and, when the carrier supports links, resolves to the exact unit.

Place the one authoritative logical pattern index after those public-unit entries. It may be one table or several ordered, uniquely labelled Part or placement segments. Every authoritative segment uses:

```text
| § | ID & Title | Status | Keywords & Search Queries | Dependencies |
```

Across all segments, every pattern body has exactly one row, every row resolves to exactly one body, and no PatternID appears twice. A Part label groups rows for navigation; it is not a pattern row, a semantic parent, or another index.

PatternID, title, Part, and `§` position remain separate even when one row displays them together. PatternID supplies the stable public address within the named framework; the title explains the pattern; Part and `§` show where the current edition places it. Within each Part, the ToC rows and pattern bodies follow the same order. That order need not ascend by PatternID, and moving or retitling a pattern does not by itself change its PatternID.

When the surrounding text does not already identify the framework, name the framework together with the PatternID. To select the body published in one edition, also name that framework edition. For a DPF, `E.4.DPF` supplies the choice of reference code and local locator, and the continuity decision; this profile only makes the selected distinctions visible in the publication.

Reserve `Support index — <lookup job>` for a secondary pattern lookup. Its exact header is:

```text
| PatternID | Pattern title | Lookup use |
```

Ordinary relation, source-return, maintenance, and reference tables may cite PatternIDs under truthful headings and other complete headers. Do not infer that they are indexes from their cell values. Reject a second `# Table of Contents`, a `Pattern Index` heading for the same job, an authoritative header outside the authoritative ToC region, or a support heading and header that do not occur together. Public-unit entries are navigation inside the one ToC, not another pattern catalogue.

### E.11.PFP:4.3 - Keep one practical-entry set and two visible forms {#keep-one-practical-entry-set-and-two-visible-forms}

Start the Readme body with `## Practical entries`. The product maintains one declaration for every selectable example and assigns each key exactly one public form: ordinary practical entry or Practical-Use Card. Each declared key occurs once, at H3 for an ordinary entry or at H4 for a card. A compact locator may precede or follow these examples, but it is a finding aid rather than another editable entry set.

The Readme says plainly that its entries are selected examples, not a catalogue or coverage boundary. It tells the reader to bring the actual question and to use the product's index, direct patterns, or another finding aid when no example fits. Tell readers that they can ask an assisting agent for explanations and comments in ordinary language, without the framework's specialist vocabulary. For example: “Explain this and give me your comments in ordinary language, without framework jargon.” Clear wording is the default under `F.19`; the request helps the assistant adapt its wording to the reader.

The selected examples should make two uses visible without implying that every question belongs to either displayed case:

- an ordinary entry shows how one direct pattern or one bounded direct route can answer a comparatively simple difficulty without a mantra; and
- a Practical-Use Card shows a recurring complex difficulty whose useful answer spans several direct pattern contributions and whose long dependency is easier to retain with a mantra.

The `First useful result or blocker` value gives the result of the action the entry supports, or a condition preventing that action. When several actions could be meant, name the relevant action in the value.

Use this ordinary-entry form:

```text
### <ordinary-entry key> — <plain title>

- **Situation:** <recognizable working situation>
- **Question:** <practical question>
- **First useful result or blocker:** <smallest useful result of the named action, or the condition preventing that action>
- **Start with:** <direct PatternID or bounded plausible set>
- **Stop or return:** <ordinary stop, wrong-turn return, or reopen condition>
```

When the product selects at least one card, place all selected cards under one group:

```text
### Practical-Use Cards

<plain statement that these are selected examples of extended cross-pattern use, not a catalogue or prescribed workflow>

#### <card key> — <plain title>

- **Situation:** <recognizable recurring difficulty>
- **Question:** <practical question>
- **First useful result or blocker:** <smallest useful result of the named action, or the condition preventing that action>
- **Mantra:** <plain repeatable wording that retains the cross-pattern dependency>
- **Start with:** <direct PatternIDs or bounded route>
- **Stop or return:** <ordinary stop, wrong-turn return, or reopen condition>

##### Expansion for <card key>

<optional explanation only>
```

`### Practical-Use Cards` is a group inside the one `Practical entries` set, not another front door or selectable key. Omit the group when the product selects no cards. The card's canonical structural field is `Mantra`; its value begins directly with the repeatable wording and needs no `Local`/`Long` prefix. A local reminder for one direct pattern or bounded result may remain in that pattern, an ordinary entry, or other teaching material, but it does not by itself select the richer card form. `E.11` owns this content decision.

Every selectable ordinary entry and card shares one product-wide semantic-key namespace. The product declaration assigns each key one form, so a key cannot occur as both H3 and H4. An H5 expansion repeats its enclosing card key only to attach optional explanation; it is not another selectable occurrence. A card has zero or one expansion. Its compact portion ends after `Stop or return`; the expansion ends at the next H4-or-higher heading or the end of the group. The expansion may explain branch choices, examples, or exact result support, but cannot contain another H4 card or H5 expansion.

The product-language application declares one deterministic reading-burden measure and two maxima: one for the mantra and one for the complete compact card. The measure must suit the publication language; whitespace counting is suitable only where it meaningfully measures reading burden. The maxima protect scanability and recall. They are not targets, proof of reader value, a fixed card count, or authority to delete a choice-changing distinction. Content that a compact card cannot carry truthfully returns to the direct patterns or, only when first choice needs it, the same-key expansion.

Applying this grammar does not select a card, prove that the examples cover the product, or show that every cited pattern is needed in a particular case. `E.11` defines the direct-entry/card comparison, cross-pattern mnemonic-gain test, and non-exhaustive discoverability purpose. The product-specific E.4 pattern declares its selected example keys, forms, reading-burden measure, and two limits. A validator consumes those values and checks structure; it does not decide content value.

Use `First useful result or blocker` for this field in new entries. In existing publications, `First useful result or honest blocker` identifies the same field, with the same value and position; including both labels in one entry repeats the field.

This profile keeps structural field keys in canonical English. A translation may translate surrounding prose and values and may add a human-readable gloss, but it does not silently replace or reorder the field keys. A translated structural-key profile needs a separately selected recovery and checking rule. Test translated and low-tool publications with actual readers and navigation tools rather than treating English parser success as accessibility evidence.

### E.11.PFP:4.4 - Keep support units and adjacent products distinct {#keep-support-units-and-adjacent-products-distinct}

A Readme, Preface, ToC, pattern-body collection, whole-framework account, relation or edition note, and refresh route may be publication units of one framework product when they serve its declared use and edition boundary. Place each unit where its readers can find and use it. A separate file is a carrier choice.

Use `E.4:4.1` to decide an adjacent product boundary from the useful result and its intended use. People may need to use, cite, or change a result as an identified whole, whether it appears inside a collection or through a separate carrier. State its identity, edition or current state, users, use, content boundary, and access route to the extent needed for that use. An established maintainer or maintenance commitment is not a prerequisite; record maintenance and refresh conditions when they are established and change reliance or use.

Examples include a source registry, MethodDescription collection, decision-support publication, inquiry evidence package, practitioner guide, pedagogical companion, catalogue, tool reference, access service, or inquiry programme. Their labels do not decide the boundary. Where an independent boundary is useful, point to the exact product edition or state. An annex may carry a declared snapshot or projection with a return to that product. Where ordinary framework use needs the material within the same boundary, include it as a named support publication unit.

One outer presentation carrier may expose several products. Each keeps its own identity, edition or state, form, access, and any separately established status or maintenance relation. Apply this profile to the FPF, DPF, or LPF constituents. A catalogue, evidence package, guide, service, programme, or other non-framework product uses the form selected for its own kind.

DRRs, build manifests, quality runs, digests, logs, and campaign state are process or maintainer evidence by default. A selected public use can justify a separate reader product or a public explanation drawn from that evidence. Publish durable use-changing reasons in the whole account or the relevant pattern; keep the dated decision, review, and release history in their records.


### E.11.PFP:4.5 - Check syntax and product truth at the right boundary {#check-syntax-and-product-truth-at-the-right-boundary}

The deterministic part of the form check handles recoverable syntax and projection agreement:

- the product-declared title and Readme H1, the compact opening, and absence of prohibited development or machine material from reader front matter;
- the required H1 sequence plus the product-declared body and reference tail;
- product-declared Readme and Preface entries in the established ToC grammar, before the logical pattern index, with no generic rival mini-menu;
- one correctly addressed, content-free Preface end heading at the boundary of that unit;
- authoritative index segments, aggregate row/body bijection, duplicates, and reserved support-index grammar;
- the Readme's one practical-entry set; its explicit examples-not-coverage statement; the product's declaration of example keys and forms; exactly one H3 ordinary entry or H4 card per declared key; five ordered ordinary-entry fields; a non-empty card-group explanation; six ordered card fields; the shared reading-burden measure and mantra/card limits; and zero or one same-key H5 expansion with the declared boundary; and
- equality and source agreement of every optional public cue that is actually projected.

Check Markdown grouping with a focused source-hazard scan and a parser-backed render of the same candidate. Inspect the rendered heading outline and the block, list, table, code and link structure together. Reuse matching unchanged results. A clean mechanical result supports but does not replace the reader-visible judgement.

The product-specific check compares every visible cue with the exact edition or relation record from which it was projected and checks the product-specific body, reference tail, and any pinned compact-front shape. A syntax-valid but unresolved value fails there. A field absent from the public opening is not a form defect unless a selected reader use and product-specific rule require it.

A reader also follows the twelve content questions in section 4.7 to their public answers. A link or heading proves only that a target exists; reading establishes whether it answers the question at the claimed scale and preserves direct use. Reuse unchanged answers and current matching results. This content reading belongs to the selected authoring or publication question; the common form adds no separate release procedure.

Neither check decides framework scale from pattern count. Report `pattern_count = 1` as a diagnostic. Use E.4, E.4.PFAD, E.4.DPF.DA, E.11, E.21, and the applicable subject patterns to judge whether the result is a usable pattern language for its declared field and first use.

### E.11.PFP:4.6 - Return the form result without overclaiming {#return-the-form-result-without-overclaiming}

Return the exact framework edition, edition-record source, carriers checked, form units found, public-cue agreement, logical-index result, practical-entry declaration and form result, product-specific tail checked, the public answers or unresolved content questions under section 4.7, and every mismatch or unresolved ref. Say separately whether the edition, carrier, publication occurrence, availability, currentness, or framework adequacy has an applicable result. Do not infer those claims or the truthfulness of card selection from form conformance.

### E.11.PFP:4.7 - Explain the Methods at each selected scale {#explain-the-methods-at-each-selected-scale}

Use all twelve substantive E.8 functions as authoring questions for the whole framework and each substantive profile selected by its architecture. Answer them at the scope the publication promises. A framework may describe one composite Method through many patterns, several related Methods, or a repertoire used in different combinations. Where an exact MethodDescription claim matters, use `A.3.1` to identify the admitted Method and `A.3.2` to test the description episteme's MethodDescription membership. The number of patterns, mantras, files, or description media does not settle that identity.

The whole account connects the answers that individual pattern bodies supply. Write the shared answer once and give exact returns to inherited content. At a narrower scope, state what changes in the situation, contribution, combination, evidence, result, or boundary. When an answer is missing, say which question remains open, which promised use it limits, and what remains usable.

Develop a missing instruction in the underlying account through E.8:4.2.1.1 before choosing how to present it. Then follow the promised use through the resulting publication, including any return to a supplying explanation. The reader must still obtain the input meanings, necessary operation, intermediate result and action-changing conditions that make the continuation possible. A short entry may rely on its reachable developed destination; it must keep any condition needed before taking its first action. A full explanation elsewhere does not close a gap if the reader cannot find or use it under the declared access conditions. Restore missing content at its source or repair its presentation and return, then revalidate the affected connected reading under F.19. A sound file structure or resolved link alone does not establish that the instruction survived.

| E.8 function | Question the whole or profile account answers |
| --- | --- |
| Problem frame | Who is doing what kind of work, under which conditions, and when would this language help? |
| Problem | Which inquiry, intended transformation, opportunity, or recurring difficulty needs an answer? What remains unresolved with the available approach? |
| Forces | Which competing requirements, resource limits, evidence conditions, or values shape the choice of Methods? |
| Solution | Which Methods and pattern contributions answer the problem? How do their results connect, which choices change the route, and where can the reader enter directly? |
| Archetypal Grounding | What actual or minimally viable worked case shows the language or profile producing a useful result, including a consequential branch or limit? |
| Bias-Annotation | Which assumptions, perspectives, exclusions, or access conditions affect whose work the language serves and where its claims travel? |
| Conformance Checklist | Which substantive questions establish correct use at this scope? Which answers can be inherited, and which changed conditions need their own judgement? |
| Common Anti-Patterns and How to Avoid Them | Which documented failures, text-invited misreadings, or consequential neighbouring cases need a practical correction? Apply the grounded-guard rule in E.8 and F.19. |
| Consequences | What practical gains, costs, residual limits, and subsequent moves follow from using this arrangement? |
| Architectural Rationale | Why does this organization of Methods serve the declared use? Which serious alternatives and trade-offs explain its boundaries, profiles, composition, and reuse, and when should a different choice be made? |
| SoTA-Echoing | Which current answers and source contributions shaped the Methods and their shared architecture? What was adopted, adapted, or rejected against a serious alternative, and what would reopen that choice? |
| Relations | Which specialization, bounded-use projection, composition, reuse, dependence, or publication-grouping relations actually hold, and where does each named contribution become useful? |

When a condition governs a whole combination of Methods, give it one public statement at the scope where that combination is used. State the quantities, assumptions, or other conditions needed to apply it, and return to that statement from affected profiles and patterns. Pairwise relations remain useful, but a condition on the whole set may require a different decision. A change to that condition reopens the combinations that rely on it; unchanged local contributions remain available.

Also explain the relevant vertical of Method composition and ongoing performance. A selected action can constitute part of a larger work that is being performed at that same moment. Give a representative example in which a condition of the whole changes the constituent action; show where a missing intermediate capability or incompatible resource demand prevents the combination. B.1.5.EW recovers that connection and B.1.5.RS examines a constituent replacement. A DPF can describe only part of the needed vertical: state the preparation, support and coordinating performance needed beyond its own descriptions. Reuse clear existing explanations and stop decomposition when further detail cannot change the use. Genuine earlier-result dependencies remain part of the account.

Place the connected account in the product's existing Preface and declared reference or support units. Readme explains how to enter and use it. A large language may use a public Reference for explanations shared across many bodies; a small language may carry them in its Preface. Preserve enough rationale, source synthesis, alternatives, and worked detail for the intended reader to understand and adapt the language without its development intake or DRR. An exact inherited answer can satisfy a question; merely naming a pattern or listing source titles cannot supply missing explanation.

These are twelve content functions, not twelve compulsory new H1 sections. Each full pattern body retains its address and E.8 form. The outer Solution explains how to use the contributions together and returns to the bodies in the existing collection. It does not nest them under a new parent heading or require reading the whole account before a direct pattern use. If the public account uses the canonical function labels, prefer `Architectural Rationale`; `Rationale` remains the accepted alias defined by E.8.

There is no fixed number of generality scales. For example, a reader can move from FPF's general treatment of Methods to a Method Engineering DPF, a pattern-language construction profile, a narrower literature-based extension profile, and a pattern that recovers one candidate Method from source and Work evidence. Further useful scales can be introduced. Explain the relation at each move: a profile is a bounded-use projection; specialization carries inherited content plus a delta; composition connects Method contributions; reuse makes one contribution available in several settings; a chapter or Part groups publication text. A substantive narrowing must pass `E.8:4.1.3`'s same-situation usefulness comparison.

A pattern can participate in several profiles, and a profile can draw on several contributions. Describe this structure through the relations that hold. If a mathematical view is useful, apply `C.29`: select the elements and relation being modeled. A partial order needs its order properties; a lattice additionally needs the required bounds for every relevant pair. Multiple parentage or overlapping membership alone establishes neither. Keep that mathematical representation distinct from the Methods and their subject-side relations.

#### E.11.PFP:4.7.1 - Make a Preface section recognizable on its own {#make-a-preface-section-recognizable-on-its-own}

A reader entering through search, a quotation, a link or a retrieved excerpt may see a heading without its parents. Every heading that introduces Preface content therefore carries the framework's public reference code, the publication-unit key `Preface`, and its complete ordinal section path:

```text
## <FrameworkCode>.Preface:<n> - <Title>
### <FrameworkCode>.Preface:<n>.<m> - <Title>
```

For example, `## STR.Preface:1 - Problem frame - Direction and commitment under changing conditions` identifies the first section of the Strategy Preface. `### ME.Preface:7.3 - Production MethodDescription` identifies a nested section in the Method Engineering Preface. Use the framework's declared public code; name the framework as well when quoting outside a context that identifies it. The enclosing Preface H1 retains its product-declared title and established ToC entry.

Close the complete Preface with one content-free H2 heading, `## <FrameworkCode>.Preface:End`, after its last paragraph, list or other content and before the next publication unit. For example, the Strategy Preface ends with `## STR.Preface:End`. This visible boundary shows where the Preface ends when it is copied or retrieved separately. It closes the whole Preface, not each numbered subsection; it adds neither a content section nor a pattern-index entry. A heading shown inside a fenced example does not close the unit.

Number sibling sections in reading order, starting at 1, and carry the complete parent path into nested headings. Each nesting level adds one heading level and one ordinal. These ordinals locate sections in this Preface; their titles state the content functions. An account can combine several E.8 functions in one section or explain one function across several sections. Keep that useful arrangement instead of adding twelve empty sections to match numbers. The rule introduces no limit on useful conceptual scales; physical Markdown heading depth remains a carrier constraint.

`STR.Preface` names a publication unit. Its section addresses are `SectionRef` uses under E.8, not declarations of additional patterns: the pattern index continues to contain the individually declared pattern bodies. Apply the same self-identifying construction to a profile account or other support unit when it needs its own section addresses, using its product-declared unit key. A profile explained inside the Preface retains its Preface section path; that text position does not decide the profile's semantic relations.

The prefix lets a reader distinguish a whole-language Problem frame from the Problem frame of one pattern before choosing what to read or cite. Visible names and numbers also survive copying and printing, where a hidden anchor cannot help.

The visible address and title use the ASCII ` - ` separator. Build each clickable fragment from the complete rendered heading according to the target Markdown carrier's rules, including punctuation removal and duplicate handling. When a heading changes, update its direct links in the publication, source templates and public consumers together. Check that the link resolves to the intended heading, then read that target for the answer the link promises. Keep the visible address usable for search and non-clickable copies. HTML anchors are optional carrier facilities, not a substitute for a self-identifying visible heading.

## E.11.PFP:7 - Conformance Checklist {#conformance-checklist}

| Check | Passing condition |
| --- | --- |
| CC-PFP.1 Scope truthful | @fact:CC-PFP-1 The form expresses one named FPF, DPF, or LPF edition; no carrier or adjacent product is relabelled as that edition. @status:spec/done |
| CC-PFP.2 Practitioner-first opening | @fact:CC-PFP-2 The compact product-declared opening leads directly to the ToC; the common profile has not inserted a record or completeness block ahead of the reader's question. @status:spec/done |
| CC-PFP.3 Edition return works when needed | @fact:CC-PFP-3 When exact edition return changes use or reliance, the shortest public designation and locator resolve without repository knowledge; otherwise no unused return field is mandatory. @status:spec/done |
| CC-PFP.4 Extra cues earn their place | @fact:CC-PFP-4 Every cue before the ToC is projected from its exact record and changes a named reader decision or action; no common optional field is required merely for completeness. @status:spec/done |
| CC-PFP.5 Development state excluded | @fact:CC-PFP-5 Reader front matter contains no campaign or candidate identifier, local path, digest, Git identity, generated comment, build command, machine warning, or maintainer instruction. @status:spec/done |
| CC-PFP.6 Entries and order recognizable | @fact:CC-PFP-6 The title, compact cues, ToC, Readme and Preface entries in the product's established ToC grammar, Readme, Preface, pattern collection, and product-declared reference tail occur in the selected order; every declared target resolves where links are used. @status:spec/done |
| CC-PFP.7 Logical index and order truthful | @fact:CC-PFP-7 One logical index may use several labelled segments, but every pattern row resolves to one body, every body has one row, and PatternIDs are unique within the named framework. PatternID is separate from title, Part, and `§` position; ToC and body order agree within each Part even when PatternIDs are non-ascending. When the surrounding text does not identify the framework, a citation names the framework together with the PatternID; a citation selecting the body published in one edition also names that edition. @status:spec/done |
| CC-PFP.8 Other tables remain truthful | @fact:CC-PFP-8 Only the closed authoritative and support-index grammars are treated as indexes; relation and reference tables are not reclassified from cell values. @status:spec/done |
| CC-PFP.9 One entry set and declaration | @fact:CC-PFP-9 One `Practical entries` set contains every selectable ordinary entry and selected card. One declaration for the product assigns every key exactly one form; each key has exactly one selectable H3 ordinary-entry or H4 card occurrence, and no rival key list or entry set exists. @status:spec/done |
| CC-PFP.9a Ordinary entry usable | @fact:CC-PFP-9a Every ordinary entry gives the five fields in order and retains any richer content needed for the first useful result and stop boundary. No mantra is forced onto a locator or ordinary entry. @status:spec/done |
| CC-PFP.9b Selected card usable | @fact:CC-PFP-9b Every selected card gives the six fields in order, begins its `Mantra` value directly with repeatable plain wording, preserves a real path through several direct pattern contributions, returns to those patterns, and has zero or one same-key H5 expansion outside the compact card. Applying the form is not evidence that the card should have been selected. @status:spec/done |
| CC-PFP.9c Product-language guard shared | @fact:CC-PFP-9c The product declares one measurable language-appropriate reading-burden rule plus mantra and compact-card maxima, and authoring and validation consume the same values. Canonical English field keys do not make whitespace limits universal. The limits check compactness; they neither select cards nor prove example coverage. @status:spec/done |
| CC-PFP.10 Readme projection restrained | @fact:CC-PFP-10 A standalone Readme repeats a short edition cue only when circulating without it would change use or return; it does not duplicate the edition or rebuildability record. @status:spec/done |
| CC-PFP.11 Product boundary preserved | @fact:CC-PFP-11 Framework support units share the declared framework boundary; independently useful adjacent products retain the boundary selected through E.4:4.1, their own identity and form, and the access or separately established maintenance conditions that change use. @status:spec/done |
| CC-PFP.12 Combined carrier neutral | @fact:CC-PFP-12 Every constituent product keeps its own form and identity; E.11.PFP applies only to framework constituents. @status:spec/done |
| CC-PFP.13 Claims remain separate | @fact:CC-PFP-13 Form conformance is not reported as acceptance, adequacy, carrier identity, publication, availability, access, maintenance, or currentness. @status:spec/done |
| CC-PFP.14 Scope examples survive | @fact:CC-PFP-14 The rule remains usable for FPF, DPF, and LPF editions and for a low-tool or non-clickable carrier without introducing a second edition identity. @status:spec/done |
| CC-PFP.15 Navigation remains usable | @fact:CC-PFP-15 The ToC represents Readme and Preface in its established product-native grammar before the singular pattern index; headings and labels describe their purpose, and the integrated rendered-structure summary plus intended-reader inspection exposes grouping defects without a second full read. @status:spec/done |
| CC-PFP.16 Whole account usable | @fact:CC-PFP-16 Every substantive E.8 question has a public answer, an exact inherited answer, or an explicit use-changing gap at each selected scope. The account connects Methods and their results, retains their Architectural Rationale and shared source synthesis, and leaves direct pattern entry available. Headings or locators alone do not establish this content. @status:spec/done |
| CC-PFP.17 Scales and relations truthful | @fact:CC-PFP-17 Further useful scales remain possible; the actual specialization, profile, composition, reuse, and publication-grouping relations are distinguished. A claimed mathematical order or lattice has the conditions required by C.29. @status:spec/done |
| CC-PFP.18 Whole-account sections addressable | @fact:CC-PFP-18 Every Preface subsection exposes its framework code, Preface unit and complete ordinal path; nested paths and heading levels agree. The whole Preface ends with one correctly addressed, content-free H2 `:End` heading before the next unit. Addressed profile or support units identify their declared unit. Links resolve to the intended rendered headings, while the target content supplies the promised answer. Publication-unit addresses do not create pattern-index entries. @status:spec/done |

## E.11.PFP:9 - Consequences {#consequences}

Readers retain each product's compact familiar opening and find Readme and Preface in the ToC grammar already used by that product, before the one authoritative pattern index. Inside the Readme they see one explicitly non-exhaustive practical-entry set: ordinary examples show cheap direct use, while only honestly selected cross-pattern cards add a visible mantra and an optional bounded expansion. Optional public cues remain recoverable from one source when they change use, while development and rebuildability records stay out of reader front matter. Builders gain checks that fail on missing public-unit entries, duplicate or cross-form keys, card grammar, structural, projection, and development-state drift without guessing table meaning, deciding card value or coverage, or inventing a rival navigation block.

The whole account also makes shared choices and source synthesis accessible beyond individual bodies. Authors can refine one profile without copying the entire language, and readers can see which answers remain inherited. Keeping those returns current costs work; concentrating the shared explanation reduces the number of independently editable copies.

## E.11.PFP:12 - Relations {#relations}

- **Specializes:** `E.11` for the common reader-facing form of one FPF, DPF, or LPF edition; `E.11` retains practical-use discoverability and first-result routing.
- **Uses:** `E.8` for the twelve substantive content functions, preferred Architectural Rationale title, intended-reader boundary, and usefulness of narrowing; `A.3.2` for an exact MethodDescription claim and `C.29` for any mathematical view of the relations.
- **Coordinates with:** `E.4`, `E.4.FPF`, and `E.4.DPF` for framework/product boundary, product-specific publication units, optional reader cues, body order, and carrier assembly.
- **Coordinates with:** `E.24.PUB` for publication occurrence, selected edition, form expression, carrier bearing, audience, bounded use, availability, and access; and `E.17` for bounded publication projections and source return.
- **Coordinates with:** `E.4.PFR` for exact dependency and edition relations, `G.11` for currentness and refresh, `E.4.DPF.DA` and `E.2.DA` for applicable package or whole-FPF adequacy, and `E.21` for pattern quality.
- **Does not replace:** product-specific builders or validators, the edition record, `FPFEditionRebuildabilityRecord`, `FrameworkPackageManifest`, an architecture decision, or a public product boundary.


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/E-11#root, spec://ai.lev/fpf-spec/contract/E-17#root, spec://ai.lev/fpf-spec/contract/E-24-PUB#root. @status:spec/done
- @fact:USED-BY Used by: spec://ai.lev/fpf-spec/contract/E-4-FPF#root, spec://ai.lev/fpf-spec/contract/E-4-DPF#root and bounded LPF/DPF publication-form applications. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/E-11#root, spec://ai.lev/fpf-spec/contract/E-4-CM#root, spec://ai.lev/fpf-eng-me/contract/ME-23#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/E-11-PFP
