# E.11.DSG - DPF Suite Reference {#root}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Specialization of E.11 (E)
> **Status:** Candidate
> **Normativity:** Normative for a DPF Suite Reference product series, its editions, and public entries.

## E.11.DSG:1 - Problem frame {#problem-frame}

### E.11.DSG:1.1 - Use this when {#use-this-when}

Use this pattern when a practitioner may need results from several DPFs, cannot yet tell which DPF applies, needs a Suite-wide commonality or relation, or needs a truthful stop because the ecosystem lacks part of the answer. The DPF Suite Reference is the editioned non-framework publication for that situation. It gives a short useful answer or honest blocker, says what each returned result or source contributes, and returns the reader to the Suite collection and the product series or states that change the answer. It is not an instructional Guide, and co-listing proves neither Suite belonging nor dependency or compatibility.

**First useful result.** Give one short answer that names the situation and returns each needed item in its real use: an available result, a MethodDescription, direct-source evidence, or a named unavailable result. Say what each contributes and end with an ordinary stop or return. State maintenance only when it changes the use. Do not fill a missing result with another title.

**Primary `EntityOfConcern`.** One DPF Suite Reference edition: a non-framework `U.Episteme` in a separately constituted Reference product series. The edition, its continuity with another edition, and its belonging to that series are separate claims.

**What this buys.** A reader can act on a small answer and still return to the Suite collection, the product series that belong to it, relevant editions or states, source facts, warnings, and stronger relations when those details change the action.

**Not this pattern when.** Use `E.4:4.2` and `E.4.PFAD` to decide product-series or Suite constitution, which editions belong to which product series, which product series belong to the Suite, maintenance, and exposure. Use one DPF directly when its result is already clear. The Reference is the problem-led entry only when selection, cross-DPF use, Suite-wide commonality or relations, or an ecosystem gap is current. An absent, unavailable, stale, or unneeded Reference neither erases the Suite nor prohibits direct DPF use, but it cannot supply a current cross-DPF route. Use `E.11.PFP` only for an FPF, DPF, or LPF edition; a Suite Reference is not a framework edition. A publication that compares several Suites has its own product boundary. Use the direct patterns for lookup Work, publication, availability, dependency, compatibility, evidence, authority, or currentness claims.

## E.11.DSG:2 - Problem {#problem}

A bare list of DPFs does not tell a practitioner which combination answers one working question. A Reference written as a tutorial or metadata catalogue fails in the opposite direction: explanation and repeated fields hide the first useful answer.

Both failures invite stronger false claims. Readers may infer that listed DPFs form one framework, depend on each other, are compatible, current, or available. They may also treat the Reference as lookup Work, evidence, or the decision that makes a product series belong to a Suite. A changed DPF edition can then make an answer stale while the Suite, product series, and Reference edition remain unclear.

## E.11.DSG:3 - Forces {#forces}

| Force | Pressure on the solution |
| --- | --- |
| Fast first use | A reader needs an answer before a catalogue of internal distinctions. |
| Exact return | The answer must still lead to the Suite collection, the product series or edition that changes the action, the Reference edition, and the direct source. |
| Separate managed boundaries | The Suite collection, Reference product series, DPF product series that belong to the Suite, adjacent evidence products, and carriers have distinct identity, edition or state, and maintenance claims. |
| Honest combination | Several resources may be necessary, alternatives, or merely plausible; the Reference must state the actual relation or uncertainty. |
| Current action | Date, status, warning, availability, and source return matter only when they change what the reader should do. |
| Low record burden | Ordinary lookup may remain conversation; addressable answers are justified only by later review, reuse, publication, or reliance. |
| Language reach | Translation and language-specific maintenance may change the episteme or the product boundary. |

## E.11.DSG:4 - Solution {#solution}

Write the practical answer first. State the recognizable situation and question, then say what each returned item actually is and what it contributes: an available result of its own kind and supplying product, a MethodDescription used to select or perform its Method, direct-source evidence for a named claim or decision, or a named unavailable result with its blocker and retry. State maintenance only when it changes the answer. End with the ordinary stop or return. Add identity, relation, evidence, warning, or reliance detail only when it changes the answer's truth, the reader's choice, or a named later use.

### E.11.DSG:4.1 - Keep the Reference product series, each edition, and Suite belonging distinct {#keep-the-reference-product-series-each-edition-and-suite}

A **DPF Suite Reference product series** is a continuing collection of Reference edition epistemes under its reader-use, content-selection, admission, reidentification, later-review, and retirement rules. It begins when a product-constitution decision under `E.4:4.2` admits the first Reference edition. A separate publication occurrence may make that edition available. A maintaining System, maintenance commitment, revision duty, another edition, or continued availability requires a separate claim. A title, date, language tag, file, carrier, or publication alone does not create the series.

A later Reference edition belongs to that series only after its source-edition relation and the Reference admission rule pass and an admission decision takes effect. Supersession, unavailability, non-currentness, or edition retirement does not end that occurrence while the same Reference product series continues. If the series ends, current belonging ends with it. If its identity rule identifies another series, belonging to the old series ends when that reidentification takes effect. The past fact remains, and another Reference product series needs its own admission and occurrence. A fork, translation, retargeting, or reconstruction is not admitted by title or provenance alone. A changed-scheme derivative may remain in the same Reference product series only when it also qualifies as an edition and the shared reader, access, warning, later-review, and retirement conditions still hold.

The Reference product series belongs to its DPF Suite only after a separate Suite-inclusion decision takes effect. Belonging remains current only while the same Reference product series and Suite continue and no removal decision has taken effect. If either collection ends, current belonging ends with it. If its identity rule identifies another collection, belonging to the old collection ends when that reidentification takes effect. Neither case requires a prior removal decision, and the new Reference product series or Suite needs a new inclusion. The Reference product series, its Suite belonging, Reference availability, and Reference use are different claims. The Suite may exist before the Reference series is included, and a Reference may be temporarily unusable without ending the Suite or other belonging occurrences. This claim establishes no parthood or holonhood; any such claim needs the complete A.1 test and its own part relation.

One exact **DPF Suite Reference edition** is identified under `C.2.1` as:

```text
<claim content = J_g, EntityOfConcern = G, effective ReferenceScheme = R_g>
```

`G` is that Reference edition. `J_g` states its intended readers and use, the Suite collection, selected problem-led entries, the resource and blocker claims those entries make, and only the product-series or edition state, source, warning, availability, and currentness claims that change those entries. `R_g` resolves the Reference edition, Suite collection, cited product series and editions, results, adjacent products, direct sources, and relation words used in the entries.

The Reference product has its own intended readers and use, edition-admission and reidentification rule, access, later-review, and retirement conditions. A publication occurrence may make an edition available. A maintaining System, maintenance relation, commitment, or future maintenance Work exists only when its direct evidence establishes it; authorship, constitution, publication, a locator, or the word *maintained* establishes none of them. Suite maintenance does not supply Reference maintenance, and Reference maintenance does not supply maintenance of the DPF product series that belong to the Suite.

### E.11.DSG:4.2 - Make the public minimum immediately useful {#make-the-public-minimum-immediately-useful}

Show these Reference-level facts where a reader can see them before choosing an entry:

- title and exact Reference-edition locator;
- fixed edition date, intended readers, and practical use;
- actionable status or an honest non-current, superseded, or retired warning, together with its as-of basis;
- Suite-collection locator, working return to its identity and inclusion/removal account, and any product-series state that changes the answer; and
- a table of contents that locates Reference sections and DPFs whose product series belong to the Suite without implying order or stronger relations.

The edition date says when this edition was constituted. It is not a changing currentness claim or the date of every publication occurrence. Show the author when attribution, trust, contact, reliance, or source return changes what the reader should do. A byline does not identify the Reference maintainer, suite maintainer, publisher, or authority.

Every problem-led entry keeps this small visible core:

```text
recognizable situation and practical question
first useful answer or honest blocker
available result, MethodDescription, direct-source evidence, or named unavailable result needed now, and what each contributes
ordinary stop or return
```

Add a DPF product series' or edition's state, field promise, detailed locator, applicability, evidence, availability, dependency, compatibility, warning, author, or claim-local reopen condition only when it changes the choice, truth, stop, return, or named reliance. Put a genuinely shared boundary once at Reference or section level. Do not repeat empty fields, and do not copy `E.11.PFP`'s framework pattern-index grammar into this non-framework Reference.

Frame each entry around a real working question and the decision or action the reader needs next. Let the answer branch, overlap, or offer several honest stops when the situation does; do not force a false linear procedure. Keep the action-changing answer in the entry and link to detailed sources or explanation instead of repeating them. At Reference level, state whose information need is served, how the publication is presented and made available, how readers return to its sources, and where later review or retirement is decided. Future revision or continued availability requires a separate commitment.

### E.11.DSG:4.3 - Keep lookup Work and the answer separate {#keep-lookup-work-and-the-answer-separate}

A person, team, or assisting System may use one Reference edition while doing lookup Work. Ordinary use alone does not establish a Method, assignment, operation application, evidence, or authority. Identify those objects only when the current claim actually needs their direct rules.

An ordinary answer may remain readable conversation. Persist one only when review, reuse, publication, or later reliance needs an addressable result. First identify the exact practical-question episteme `Q`. Then identify the answer episteme `A` under `C.2.1` as `<claim content = J_a, EntityOfConcern = Q, effective ReferenceScheme = R_a>`. `J_a` states the answer, exact Reference edition used, every returned resource or blocker, and what each does in this answer. `R_a` resolves those values and the use-specific relation words. This is an ordinary episteme, not a new lookup-result kind.

Say directly what each returned item does. For an available result, name the result's actual kind, supplying product and edition or current state, receiving use, and any currentness or availability condition that can change that use. State maintenance only when it changes the answer. For a MethodDescription, name the described Method and how the reader uses the description; do not present its expected result as already obtained. For direct-source evidence, name the supported claim or decision and the source limits. For an unavailable result, name the blocker and retry condition. Recommendation, alternative, dependency, compatibility, and co-listing remain separate claims and create none of these stronger relations.

### E.11.DSG:4.4 - Test sufficiency and each item's necessity {#test-sufficiency-and-each-item-s-necessity}

Call an answer a **sufficient combination with every returned item necessary** only when the Reference entry gives a recoverable candidate boundary, required result, and sufficiency rule, the combination satisfies that rule, and removing any returned item makes the result insufficient. The boundary is the resources actually inspected through the entry and its direct source returns, not every publication that might exist. This item-necessity test does not establish the smallest combination. A “smallest” claim also needs a declared size criterion and a comparison or argument showing that no smaller in-scope combination is sufficient.

When that test cannot be completed, return a bounded plausible combination and name the uncertainty or missing item. Do not disguise a convenient shortlist as a `JointUseSet`. Use `G.5` only when every named returned resource is required for one named use and the current inclusion basis supports that all-items-needed claim.

### E.11.DSG:4.5 - Return to the Suite collection and exact sources when products change {#return-to-the-suite-collection-and-exact-sources-when-products}

The Reference identifies the Suite collection; it does not decide or copy which product series belong. Its public return names:

- the Suite collection and a working route to its identity, inclusion, and removal decisions;
- each product series that belongs to the Suite, and each edition, result, state, or direct source that changes the answer;
- when reproducibility needs one, the exact optional configuration description, its as-of scope, and its source return.

A Reference projection states which belongs-to claims it captures, omits, or coarsens and the time or scope for which that account applies. It does not become the authoritative collection account. A combined carrier identifies each constituent and keeps identities, editions, access, currentness, and any separately established maintenance claims distinct. A copied product table or locator without a working source return is orientation only.

When a DPF publishes a new edition, test separately whether that edition belongs to its product series. Then refresh only the Reference advice, availability, compatibility, warning, or source return that changed. A superseded or unavailable edition still belonged to its product series while that series continued. If a product series in the Suite no longer qualifies under the inclusion rule, show the warning and return to `E.4:4.2` and `E.4.PFAD` for repair, removal, Suite change, or retirement. Until that decision, do not present the product as qualifying, current for the defeated common use, or recommended on that basis. Belonging continues until an effective removal only while the same product series and Suite continue; restoration before removal preserves the occurrence, while removal followed by inclusion creates another. If the product series ends or its identity rule identifies another series, belonging to the old Suite ends without a prior removal. The new product series needs a new inclusion.

An absent, unavailable, stale, or unneeded Reference does not erase the Suite, end current belongs-to occurrences, or prohibit direct use of a known DPF result. It does prohibit a claim that the Reference currently supplies the cross-DPF route. If the Reference loses source return, becomes unavailable, or no longer supports its claimed use, present its historical editions, warn readers, and use a direct DPF where the result is already known. Edition identity, publication, availability, and currentness continue to follow their own facts when a maintenance commitment is absent or ends; only the maintained claim then lacks support. If the Suite temporarily contains one product series or none under an explicit preservation decision, present no current cross-DPF answer; return to restoration, review, or retirement. When a Suite end or retirement decision takes effect, every current belongs-to occurrence ends without separate removals. Keep the past fact that each product belonged to that Suite, but require another constitution decision and new inclusions for any later active ecosystem.

### E.11.DSG:4.6 - Distinguish expression, derivative, edition, and product {#distinguish-expression-derivative-edition-and-product}

Another layout, carrier, rendering, or faithful expression of the same exact claims under the same scheme presents the same Reference episteme. A translation or other derivative that changes claims or effective scheme is a distinct episteme with an exact source-to-use path under `C.2.P`; when meanings cross schemes, test the `F.9` Bridge and bounded use separately. Title or provenance alone establishes no `EpistemeEditionRelation`.

A language-specific derivative stays within the same Reference product only while it uses the same intended readers and use, access rule, warning rule, later-review rule, and retirement rule. A separately established maintenance relation changes product identity only when the identity rule says so. If a language community needs a different current state or any of those rules, select another Reference product. A multi-suite comparison publication also has another product identity.

## E.11.DSG:7 - Conformance Checklist {#conformance-checklist}

| ID | Passing condition |
| --- | --- |
| `CC-DSG.1` Situation first | @fact:CC-DSG-1 A cold reader sees the working situation, practical question, useful answer or blocker, exact contributions, and stop or return before internal apparatus. @status:spec/work |
| `CC-DSG.2` Reference and Suite return | @fact:CC-DSG-2 The Reference identifies its edition and returns to the Suite collection, the decisions that establish which product series belong, and each product, edition, result, state, or source that changes the answer. An optional configuration description is named only when the use needs it. @status:spec/work |
| `CC-DSG.3` Separate product and use boundaries | @fact:CC-DSG-3 Reference product series, Reference edition, Suite collection, DPF product series and editions, lookup Work, answer, publication, carrier, belongs-to occurrences, availability, and Reference use remain distinct. @status:spec/work |
| `CC-DSG.4` Progressive detail | @fact:CC-DSG-4 Date and actionable status are visible; author, evidence, relation, product-series state, warning, and reopen detail appears only when it changes reader action, truth, or named reliance. @status:spec/work |
| `CC-DSG.5` Answer discipline | @fact:CC-DSG-5 Each returned item is classified and stated separately as an available result of its actual kind and supplying product, a `MethodDescription` reference, direct-source evidence, or a named unavailable result. Its readable contribution or blocker is explicit; maintenance appears only when it changes use, and recommendation, alternative, dependency, compatibility, and co-listing create none of those relations. @status:spec/work |
| `CC-DSG.6` Sufficiency and necessity tested | @fact:CC-DSG-6 The combination satisfies the declared sufficiency rule and removing any returned item makes the required result insufficient within the stated candidate boundary. A “smallest” claim additionally states a size criterion and establishes that no smaller in-scope combination is sufficient; otherwise retain the narrower necessity claim or call the answer bounded and plausible. @status:spec/work |
| `CC-DSG.7` Change and return honesty | @fact:CC-DSG-7 Edition admission to a product series, product-series inclusion in a Suite, qualification warning, removal, product or Suite ending and reidentification, past belonging, availability, Reference route, temporary empty state, and retirement follow their separate rules. A known DPF result remains directly usable without a Reference detour. @status:spec/work |
| `CC-DSG.8` Derivative boundary | @fact:CC-DSG-8 Expression, translation or other derivative, an established edition-continuity relation, language-specific product, and carrier are distinguished by their actual identity, source, scheme, reader-use, and maintenance facts. @status:spec/work |
| `CC-DSG.9` Plain-language whole passage | @fact:CC-DSG-9 The complete changed passage can be read by an engineer or manager without reconstructing ontology notation; exact triples and relation terms appear only where they change identification or a stronger claim. @status:spec/work |
| `CC-DSG.10` Current problem-led entry fit | @fact:CC-DSG-10 Each entry starts from a real working question, supports necessary branches or honest stops, links out distracting detail, and reflects the intended readers' information need, presentation, availability, and any separately established maintenance fact that changes use. The Reference records what was adopted, adapted, and rejected from current task-guide practice and when to recheck it. @status:spec/work |

## E.11.DSG:9 - Consequences {#consequences}

**Benefits.** Readers can start with a short cross-DPF answer, distinguish an available result from a MethodDescription, source evidence, or a missing result, recover the products behind the answer, and see an honest product gap. A later maintainer can refresh advice without silently changing which editions belong to product series, which product series belong to the Suite, edition continuity, dependency, or compatibility.

**Costs.** The Reference and Suite need separate identity, source-return, publication, availability, and currentness facts. A maintenance arrangement adds its own evidence and coordination cost only when it is actually claimed; neither constitution nor first publication requires it. High-consequence answers may require more detail than ordinary lookups. Those costs appear only where the reader's action or later reliance needs them.

## E.11.DSG:12 - Relations {#relations}

- **Specializes:** `E.11` for one editioned cross-DPF Reference product; it does not specialize `E.11.PFP`.
- **Uses:** `E.4:4.2` and `E.4.PFAD` for product-series and Suite constitution, edition-to-product belonging, Suite inclusion and removal, and their decisions; `A.14` for the distinction between collection belonging and constructive parthood; `C.2.1` for Reference and DPF editions and their continuity; and `G.5` only for an actual `JointUseSet`.
- **Coordinates with:** `E.4.PFR` for exact edition dependency and compatibility; `C.2.P` and `F.9` for derivatives and cross-scheme use; `E.17`, `E.24.PUB`, and `G.11` for source return, publication, availability, and currentness; `E.11.PUA` and `E.11.PUR` for actual selected-pattern use and pattern-use coordination.
- **Constrains:** public DPF Suite Reference entries, Reference-level metadata and warnings, source-return projections, persisted lookup answers, and returns after inclusion, availability, identity, or retirement changes.


## Dependencies {#dependencies}

- @fact:SPECIALIZES Specializes: spec://ai.lev/fpf-spec/contract/E-11#root. @status:spec/done
- @fact:USES Uses: spec://ai.lev/fpf-spec/contract/E-4#root:4.2 and spec://ai.lev/fpf-spec/contract/E-4-PFAD#root for Suite architecture, spec://ai.lev/fpf-spec/contract/C-2-1#root for Reference and DPF editions, and spec://ai.lev/fpf-spec/contract/G-5#root only for an actual JointUseSet. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/E-4-PFR#root, spec://ai.lev/fpf-spec/contract/C-2-P#root, spec://ai.lev/fpf-spec/contract/F-9#root, spec://ai.lev/fpf-spec/contract/E-17#root, spec://ai.lev/fpf-spec/contract/E-24-PUB#root, spec://ai.lev/fpf-spec/contract/G-11#root, spec://ai.lev/fpf-spec/contract/E-11-PUA#root, and spec://ai.lev/fpf-spec/contract/E-11-PUR#root. @status:spec/done

#source spec://ai.lev/fpf-spec/source/E-11-DSG
