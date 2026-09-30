# E.17.ID.CR - Compare Sources Within a Shared Review Frame (ComparativeReviewUnit) {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Status:** Stable

**Plain-name.** Bounded source comparison under a shared review frame.

**Use this when.** Use this pattern when a team needs one small comparison note, comparison sheet, or guided review aid over already available source epistemes or source publications. The unit should make one bounded contrast or a small set of contrast rows inspectable while the shared review frame stays visible and downstream claim or effect remains outside.

**First-minute working moment.** A team has two or more source-pinned notes, sheets, views, or review aids on the table. They need one honest comparison unit: two design options for one release, two methods for one task family, two vendor bulletins for one control scope, two research syntheses for one uncertainty question, or two programme strategies for one initiative. The job is not yet action selection, approval, ontology repair, or wider work-process control. It is to compare without pretending that the comparison note already became a decision.

**First output.** Use the ordinary seven-row card:

```text
ComparativeReviewUnit:
  ReviewedSources:
  SharedReviewFrame:
  ComparedAlternatives:
  ComparisonCriterionOrRows:
  BoundedLift:
  BlockedDownstreamClaimOrEffect:
  BoundaryTrigger:
```

**What goes wrong if missed.** A comparison unit is either dismissed as harmless prose or overread as equivalence, action selection, gate pressure, release approval, work or reliance guidance, or adjudication authority. The team then argues about hidden authority instead of inspecting the bounded contrast.

**What this buys in practice.** The team can compare already available sources, inspect one bounded contrast or a small comparison sheet, and use the boundary trigger to name any crossed claim and the pattern that governs that claim.

**Not this pattern when.** If the primary question is no longer the bounded comparison unit or its shared review frame, name the crossed claim and apply the governing pattern for that claim: source transformation, bridge, explanation face, prompt or action selection, ontology or `EntityOfConcern` change, decision, work or reliance, gate, assurance, adjudication, or reduced-use source rendering.

**Quick working-fit check.**
1. Am I working over the comparative review unit itself?
2. Does the shared review frame stay preserved, with compared alternatives still distinct when they are distinct?
3. Is one bounded contrast or small row set being made visible?
4. Is the downstream claim or effect still outside?

If yes, stay here and use the ordinary card. If no, use the neighboring-work boundary in `E.17.ID.CR:4.5`.

## E.17.ID.CR:1 - Problem frame {#problem-frame}
Engineer-managers, programme leads, and research or cultural reviewers repeatedly need to prepare or share a small comparative review unit that helps a team read two already available source epistemes or source publications together without overstating what downstream claim or effect that unit now carries.
Typical moments include:
- a design-review note that says one already available option write-up foregrounds coupling risk more than another;
- a release or compliance comparison that says an internal control sheet and a vendor bulletin are not yet equivalent even though they speak to the same review task;
- an operations comparison that says a dashboard view and a maintenance note foreground different operational pressures in the same service episode;
- a research-review note that says one available synthesis foregrounds measurement uncertainty more than another without yet declaring a better method;
- a program or cultural review note that says one available brief foregrounds participation continuity more than another without yet deciding funding, curation, or program direction.

These review units are useful precisely because they make the next review discussion more precise.
They become dangerous when a reader starts treating them as if they already established equivalence, root cause, redesign priority, action selection, program choice, or approval.

## E.17.ID.CR:2 - Problem {#problem}

Without a named comparative-review-unit discipline:
1. a useful comparative review unit is dismissed as if it were only harmless prose;
2. a cautious review aid is overread as if it already licensed substitution, interoperability, or equivalence;
3. a comparative review unit quietly becomes action-selection pressure or hidden hypothesis work while still sounding calm;
4. same-entity viewing, explanation rendering, and bounded comparison collapse into one fuzzy review bucket;
5. ontology-facing target shift or changed EntityOfConcern hides inside comparative wording;
6. a review unit written to serve review is mistaken for work or reliance guidance, assurance shorthand, or release authority.

## E.17.ID.CR:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| **Engineer-manager usability vs governance precision** | The pattern starts from a recognisable review situation without hiding its neighboring patterns. |
| **Middle-band reality** | Some bounded comparisons add more interpretive lift than a short F.9.1 stance note about an existing bounded-use claim but still stop below full action selection. |
| **Source tether vs interpretive lift** | The case adds a bounded interpretive lift without pretending to create a new free-floating semantics. |
| **Comparison unit vs surrounding work** | The pattern keeps the comparative review unit, the bounded comparison, and the larger review process distinct rather than sliding between them by style. |
| **Viewing restraint** | Interpretation does not absorb same-entity viewing, conservative rewriting, or representation-scheme transition whose main question is not bounded comparison. |
| **Bridge restraint** | Interpretation does not become a second bridge taxonomy. |
| **Explanation restraint** | Interpretation does not become a shadow face-use discipline system next to `E.17.EFP`. |
| **Abductive restraint** | Interpretation stops before an abductive-prompt or action-selection claim governs the next action. |
| **Ontology restraint** | Interpretation does not hide same-referent pressure, retargeted-EntityOfConcernRef pressure, or changed `EntityOfConcernRef`. |
| **Interpretant-side boundedness** | Reader-fit can matter, but it remains explicit and bounded rather than silently rewriting authority. |

## E.17.ID.CR:4 - Solution - comparative review units with bounded comparison, escalation, and boundary rules {#solution-comparative-review-units-with-bounded-comparison}

### E.17.ID.CR:4.1 - Ordinary comparative review-unit move {#ordinary-comparative-review-unit-move}

Make one bounded comparison unit over already available source epistemes or source publications. Pin the reviewed sources, state the shared review frame, keep the compared alternatives visible, write the bounded comparative lift, name the downstream claim or effect that remains blocked, and give the boundary trigger that would move the case to another governing pattern.

In plain working terms, this pattern is for a review unit that says something like:
- `this option write-up foregrounds integration pressure more than that one`;
- `these two available source epistemes or source publications are useful together, but they are not yet equivalent`;
- `this dashboard view helps triage one contrastive question, but it is not yet a release decision or a root-cause claim`;
- `this research synthesis foregrounds uncertainty more than that one, but it is not yet a method choice`;
- `this program brief foregrounds continuity risk more than that one, but it is not yet a funding decision`.

If that sounds like the review unit you need, keep the comparison unit bounded by the seven-row card. If the first move is no longer bounded comparison over pinned sources, name the crossed claim and let its governing pattern carry that claim before this unit is used.

### E.17.ID.CR:4.1.b - Compact placement {#compact-placement}

`ComparativeReviewUnit` is the governing pattern selected inside the wider `InterpretationDiscipline` naming family for this bounded use. The family name helps readers find the interpretation area; it does not govern the local claim. The local object is one comparative review unit carrying one bounded comparison, or a small set of bounded contrast rows, over already available source epistemes or source publications.

> `ComparativeReviewUnit` governs one comparative review unit over already available, source-pinned epistemes or source-pinned publications. It stays bounded only while the shared review frame and source references remain visible, distinct alternatives stay distinct, the added lift remains comparative, and any crossed bridge, prompt, ontology, work, gate, authority, or downstream-use claim is named and governed by the pattern for that claim.

Use `E.17.ID.CR`, `ID.CR`, or `ComparativeReviewUnit` when this bounded comparison unit is the current object. Use the neighboring pattern when the crossed claim becomes primary.

### E.17.ID.CR:4.1.c - Why the comparative-review-unit specialization needs its own discipline {#why-the-comparative-review-unit-specialization-needs-its-own}

Teams already produce small comparative review units, often as comparison notes, comparison sheets, or guided review aids, that add more interpretive lift than a short F.9.1 stance note about an existing bounded-use claim but still stop below action selection, ontology reframing, retargeting, or approval guidance.
Leaving that middle band unnamed creates two opposite failures: one reader dismisses the review unit as harmless prose, while another over-reads it as if it already carried substitution, action-selection pressure, or action authority.

This pattern gives teams a narrow way to prepare, share, and inspect that comparative review unit without smuggling a downstream claim or effect beyond what the source, bridge stance, and bounded use can honestly carry.

### E.17.ID.CR:4.1.d - Local working vocabulary {#local-working-vocabulary}

This pattern uses a small local vocabulary for review.
- **Comparative review unit** = a lightweight review unit such as a short comparison note, small comparison sheet, guided review aid, or guided comparative UI whose explicit job is one bounded comparison or a small set of bounded contrast rows under one shared review frame.
- **Base governing case** = the primary source relation, pattern-governing case, or project work question that already governs the review use before bounded comparison is added.
- **Reviewed source episteme or source publication** = the already pinned or otherwise reviewable source episteme or source publication being comparatively read; in plain terms, the already available source episteme or source publication under review.
- **Source references** = `sourceAnchorSet` or `sourceRefs` that make the interpreted source episteme or source publication inspectable.
- **Shared review frame** = the review target, described situation, decision situation, release candidate, method family, control scope, problem frame, or source-set reference that remains preserved while the comparison is made.
- **Compared alternative** = one distinct option, method, bulletin, strategy, note, view, source episteme, source publication, or project-side FPF kind and reference named by value kept separate under the shared review frame.
- **Same `EntityOfConcernRef` case** = the special case where the compared sources describe the same entity. This is common, but it is not required when distinct alternatives remain under one shared review frame.
- **Interpretive lift** = the bounded comparative or asymmetry-bearing comparison added on top of already available source epistemes or source publications; in a small comparison sheet, each row has its own declared comparison criterion while the unit keeps one shared blocked downstream claim or effect and boundary trigger.
- **Bridge references** = required `bridgeOccurrenceRef` and `boundedUseClaimRef` when the case depends on bridge-mediated correspondence rather than ordinary source interpretation alone. The use-claim reference resolves a claim whose `EntityOfConcern` is that Bridge occurrence and whose proposed use, direction, correspondence rule, tolerated loss, and polarity match this comparative unit. Optional `bridgeCardRef` cites reusable packaging, and optional `bridgeStanceRef` cites a separate F.9.1 episteme whose `EntityOfConcern` is that exact use claim.
- **Bounded comparative use** = what this review unit can be used for while it remains only a bounded comparative review unit.
- **Overread risk** = how the review unit is most likely to be overread into a bridge, action-selection, ontology, or authority claim that it does not carry.
- **Prompt boundary** = the explicit `U.AbductivePrompt` publication that becomes the governing publication when an abductive-prompt or action-selection claim governs the next action.
- **Ordinary minimum block** = the smallest ordinary record that keeps the review unit honest for working use.
- **Load-bearing extension** = the fuller declaration record used when the case sits close to bridge, explanation, abductive, ontology, or authority boundaries.

These terms are local review fields for completing the comparative review unit. They keep source references, shared review frame, compared alternatives, bounded lift, blocked downstream claim or effect, and boundary trigger readable in the card.
When one of those fields starts carrying a bridge, evidence, gate, speech-act, commitment, work, authority, publication-face, or project-side FPF claim, name that crossed claim and use the governing pattern for it.

### E.17.ID.CR:4.2 - Scope and exclusions {#scope-and-exclusions}

**In scope**
- bounded comparative asymmetry over already declared reviewed source epistemes or source publications;
- reader-facing interpretive caution that stays source-tethered and preserves the shared review frame;
- comparison of distinct alternatives under one shared review target, described situation, release candidate, method family, control scope, problem frame, or source-set reference;
- comparative review units that answer one explicit contrastive question without creating a rival action-selection search;
- bounded user-fit when that fit only limits use rather than widening authority.

**Out of scope**
- same-entity restatement, conservative rewrite, or representation shift whose main question stays with `A.6.3`, `A.6.3.CR`, or `A.6.3.RT`;
- a separate F.9.1 stance note that only clarifies an already constituted F.9 bounded-use claim;
- explanation-face use discipline, bounded-use boundary, or added-link review on existing faces (`E.17.EFP`);
- abductive-prompt or action-selection cases (`B.5.2.0` or `B.5.2`);
- ontology-facing reframing or changed EntityOfConcern (`OntologicalReframing` or `A.6.4`);
- policy, gate, adjudication, assurance, or work-facing use (name the actual claim and use its governing pattern; see `E.17.ID.CR:4.5`).

### E.17.ID.CR:4.2.a - Working-fit test {#working-fit-test}

Use this discipline only when all of the following hold:
1. the reviewed source episteme or source publication is already pinned or otherwise reviewable;
2. the review unit adds one bounded comparative or interpretive lift, or a small set of bounded contrast rows with row-level comparison criteria;
3. the case is still answering a bounded contrastive question rather than selecting an action;
4. the shared review frame stays preserved, and compared alternatives remain distinct unless an explicit bridge or substitution source supplies equivalence, substitution, or another named relation between them;
5. the main question is not already better described as same-entity viewing, an F.9.1 stance note about an existing bounded-use claim, or explanation-face use discipline.

If any of those fail, handle the current work under the neighboring FPF pattern and project-side FPF kind and reference named by value that actually govern it.

### E.17.ID.CR:4.2.b - Nearest neighboring work {#nearest-neighboring-work}

Name the base source relation or work question before adding bounded comparison. If the current question is already source transformation, bridge, explanation-face use, prompt or action selection, ontology or changed `EntityOfConcern`, decision, work or reliance, gate, assurance, adjudication, or reduced-use source rendering, do not stretch `ComparativeReviewUnit` to carry it. Use the compact boundary map in `E.17.ID.CR:4.5` and the governing pattern for the crossed claim.

### E.17.ID.CR:4.3 - Working-model first; plain questions first, ordinary minimum second, full declaration third {#working-model-first-plain-questions-first-ordinary-minimum}

Most working users do not have to start with a long declaration block.
This pattern therefore follows `E.14`'s working-model-first discipline: the first usable block is a small set of plain questions that helps an engineer-manager keep the review unit bounded to the work it can honestly carry.
The ordinary minimum block comes next for ordinary use: it lets the reader turn the working comparison into the seven-row card before touching the fuller declaration block.
The fuller declaration block remains available as a reviewable declaration extension that carries source, boundary, and downstream-claim fields by value. If a real assurance or B.3 threshold is current, cite the separately constituted B.3 claim or record; do not turn this declaration extension into that assurance record.

### E.17.ID.CR:4.3.a - Five plain working questions {#five-plain-working-questions}

The near-top quick working-fit check is the canonical first working block for this pattern.
A working user can usually answer the following five questions before touching the fuller blocks:
1. What already available source epistemes or source publications am I comparing?
2. What single contrast or small set of contrast rows am I trying to make visible?
3. Am I still inside the same shared review frame, with compared alternatives kept distinct when they are distinct, or has the review target already shifted?
4. What blocked downstream interpretation does the team avoid taking from this review unit?
5. What would make another governing pattern govern the explanation, bridge work, prompt work, ontology work, or decision-authority claim?

If these five answers are not visible, the case is not ready to stay here as a bounded comparative review unit.

### E.17.ID.CR:4.3.b - Ordinary minimum block {#ordinary-minimum-block}

For ordinary bounded comparative review units, it is usually enough that the unit or its surrounding review context keeps explicit:
- what reviewed source episteme or source publication is being interpreted;
- which source references carry the local claim;
- that the shared review frame remains preserved and that distinct alternatives remain distinct unless another source supplies bridge or substitution relation;
- what declared bounded comparative lift is being added, or which bounded contrast rows are included and what comparison criterion each row uses;
- what downstream claim or effect remains blocked;
- that the default `worldContactPolicy` here is review-only and non-executive;
- and what neighboring FPF pattern becomes mandatory if the case crosses that neighboring boundary.

If those minimum answers cannot stay stable across the same note, sheet, or review aid without sliding between reviewed source episteme or source publication, bounded comparative review unit, bounded lift, and outside work, stop here. Repair local lexical-head kind pressure through `E.17.AUD.LHR` (`Local Head Restoration`); if the whole review unit still has unstable primary-subject identification (including the carried EntityOfConcern when applicable) or carried-move identification after that repair, apply `E.17.AUD.OOTD` (`PublicationUnit Primary-Subject Discipline`) before adding more declaration weight.

#### E.17.ID.CR:4.3.b.a - Ordinary working card {#ordinary-working-card}

An ordinary comparative review unit normally lets a reader recover these seven rows without using the heavier fuller declaration:

| Row | Plain question | Minimum answer |
| --- | --- | --- |
| **Reviewed source** | What already available source epistemes or source publications are being compared? | one pinned source slice, one explicit source pair, or one explicit source set |
| **Source references** | Where can a reviewer inspect that source episteme or source publication? | visible `sourceAnchorSet` or nearby `sourceRefs` |
| **Shared review frame and alternative identities** | What review target, described situation, or source-set reference is preserved, and what alternatives remain distinct under it? | preserved shared review frame; distinct alternatives are not treated as equivalent or substitutable without bridge relation |
| **Bounded lift row(s)** | What single contrast or small row set is this unit making visible? | one declared `comparisonBasis` or a small set of row-level `comparisonBasis` statements under one shared blocked downstream claim or effect and boundary trigger |
| **Blocked downstream claim or effect** | What is this unit not yet claiming? | no equivalence, abductive-prompt creation, ontology change, or decision authority |
| **World-contact limit** | What can the unit not be used to do? | `review-only and non-executive` |
| **Boundary trigger** | What would end this pattern and require another governing pattern? | one explicit bridge, explanation, prompt, ontology, or authority trigger |

This working card can appear inline in the comparative review unit or in its immediate review context.
Use it as the ordinary recovery reference for the near-top working-fit check:
- if rows 1-4 are still unstable because one pressured local lexical head or qualifier is doing too much work, stop and repair that local lexical-head pressure through `E.17.AUD.LHR` (`Local Head Restoration`) before you keep building the comparative review unit here;
- if rows 3-7 cannot stay stable because the same review unit still has unstable reviewed-source, comparative-move identification, or outside-work boundary after one honest local repair, apply `E.17.AUD.OOTD` (`PublicationUnit Primary-Subject Discipline`);
- if rows 1-7 stay recoverable over one pinned source slice or source pair, one preserved shared review frame, distinct alternatives where present, and one bounded contrast or small row set, `ComparativeReviewUnit` remains the honest primary governing pattern.

The nearest stay-here worked slices for this pattern are `E.17.ID.CR:5.4.5` through `E.17.ID.CR:5.4.6.b`.
The nearest stop-and-reopen worked slice is `E.17.ID.CR:5.4.6.c`.

Use the fuller declaration extension only when one of the boundary, reader-fit, or misuse conditions in `E.17.ID.CR:4.3.c` becomes true.
`ComparativeReviewUnit` remains primary only while those seven rows stay recoverable and the same review unit is still mainly about one bounded comparison, or a small set of bounded contrast rows, over already pinned source epistemes or source publications. If the first question is what the review unit is about, what move it carries, and what wider work remains outside, use `E.17.AUD.OOTD` (`PublicationUnit Primary-Subject Discipline`) to stabilize that `PublicationUnit` question before adding more declaration weight here.

### E.17.ID.CR:4.3.c - Fuller Declaration Extension Guidance {#fuller-declaration-extension-guidance}

A fuller declaration record becomes warranted only when a local condition changes the actual first move: reader-fit is doing real work, overread risk is high, a mixed case depends on `A.6.3.*` or `E.17.EFP`, bridge-mediated relation is live, or the same review unit still has unstable reviewed-source, comparative-move identification, or outside-work boundary after local repair.

The fuller declaration extension can inherit already-declared case ids, source pins, and provenance references instead of restating them inline. When recorded as a claim-bearing review unit, that extension normally captures the ordinary minimum block plus only the neighboring-pattern fields that govern the mixed case.

Do not answer `PublicationUnit` instability by stacking more local fields onto the fuller declaration extension. If `E.17.AUD.LHR` (`Local Head Restoration`) has already repaired the local lexical-head pressure and the same review unit still has unstable reviewed-source, publication-unit, comparative-move identification, or outside-work boundary, stabilize that `PublicationUnit` question with `E.17.AUD.OOTD` (`PublicationUnit Primary-Subject Discipline`) before deciding how much declaration weight stays here.

### E.17.ID.CR:4.3.d - Fuller Declaration Block {#fuller-declaration-block}
When the heavier declaration weight really stays here, the unit still makes at least these fields recoverable:
- `sourceRelationClass` using the shared `E.17:5.1b` vocabulary when the comparison depends on source pointer, source availability or retrieval, source use, source faithfulness, claim recoverability, contradiction, omission, claim widening, added linkage, independent verification, bounded use, forbidden downstream use, or reopen trigger;
- `sourceAnchorSet` or `sourceRefs`;
- `comparativeRelationClass = sameEntityComparisonClass | sharedFrameDistinctAlternativeClass | readerFitComparativeClass`;
- `comparisonBasis`;
- `addedClaimPolicy`;
- required `bridgeOccurrenceRef` and `boundedUseClaimRef` when the case depends on bridge-mediated comparative relation; the use-claim reference resolves an exact claim whose `EntityOfConcern` is that Bridge occurrence and whose proposed use, direction, correspondence rule, tolerated loss, and polarity match the current comparative unit;
- optional `bridgeCardRef` when a reusable Card exists;
- optional `bridgeStanceRef` when it resolves the separate F.9.1 episteme whose `EntityOfConcern` is that exact use claim;
- `targetUserModel` when reader-fit is materially shaping the comparison unit;
- `interactionMode` when the review unit is not just one static comparative sentence;
- `contrastiveQuestion` when the case is answering a specific contrast;
- `boundedComparativeUse`;
- `overreadRisk`;
- `promptWorthinessThreshold`;
- `ontologyBoundaryTrigger`;
- `worldContactPolicy`;
- `downstreamAuthorityLimit`;
- `baseCasePattern` when the review unit is a mixed case layered over `A.6.3.*` or `E.17.EFP`.

`sourceRelationClass` is only the source-relation or bounded-claim class for the local claim or use. `comparativeRelationClass` is only the comparative-relation class of this review unit. Neither field is a neighboring object or claim such as a relation kind, Bridge occurrence, bounded-use claim, Card, stance note, semantic identity, evidence relation, gate, assurance, work relation, speech act, commitment, authority reference, or decision record. The `sameEntityComparisonClass` value is a special case for comparisons where the compared sources really describe the same entity; it does not assert semantic identity. When the unit compares distinct alternatives, use `sharedFrameDistinctAlternativeClass` plus distinct alternative refs, and do not treat the alternatives as equivalent or substitutable without an obtaining Bridge and the required bounded-use claim.
`readerFitComparativeClass` by itself does not create an interpretation claim. When bounded correspondence wording implies a cross-context Bridge, first apply F.9. The `boundedUseClaimRef` must resolve a claim whose `EntityOfConcern` is the exact `bridgeOccurrenceRef`, and its proposed use, direction, correspondence rule, tolerated loss, and polarity must match this comparative unit. A positive proposed use requires affirmative polarity; when A.10 or B.3 is triggered, current reliance must support that exact use. A degraded reliance result narrows the use. Negative, abstaining, reopened, evidence-needed, blocked, or mismatched results stop this bridge-mediated use. The pattern that directly constrains the proposed comparison decides authorization, and evidence of the comparative-review Work says whether it occurred. A `bridgeCardRef` remains optional packaging. A `bridgeStanceRef` is also optional and is admissible only when it resolves a separate F.9.1 episteme whose `EntityOfConcern` is that same bounded-use claim. None of these references can substitute for another.
The main comparison question plus the neighboring pattern boundaries still decide the selected FPF pattern or project-side FPF kind and reference named by value.

### E.17.ID.CR:4.3.e - Interpretant-side block {#interpretant-side-block}

The interpretant-side fields above do not turn this zone into a full interactive explanation system or a dialog-management system.
Their current role is narrower:
- keep bounded comparison from pretending it is audience-neutral when it is not;
- make the contrastive question, guided review mode, and bounded use visible;
- and stop interpretation prose from quietly becoming prompt-bearing guidance, assurance shorthand, or policy pressure.

### E.17.ID.CR:4.3.f - Static note versus interactive aid {#static-note-versus-interactive-aid}

Use two comparison-relation forms.

1. **Static comparative review note.** A static note, sheet, or short review unit normally needs only the reviewed source episteme or source publication set, source references, `E.17:5.1b` source-relation class when source relation is disputed, comparison criterion, bounded lift, blocked downstream claim or effect, world-contact limit, and boundary trigger. Do not import interactive-explanation vocabulary into this ordinary case.
2. **Interactive comparative aid.** Add `targetUserModel`, `interactionMode`, state or history needed for the comparison claim, `overreadRisk`, and bounded-use boundary only when the aid is actually interactive, stateful, adaptive, or user-model-bearing. These fields keep the interactive comparative aid from being mistaken for audience-neutral static prose; they do not carry a crossed claim.

A comparative review unit can expose or cite the source epistemes, source publications, or project-side FPF references being compared, but layout, fluent contrast, side-by-side placement, or guided-review reuse does not change the kind of the unit or create a stronger source relation. If the required source relation is missing, the repair request or source-gap note is prospective only; it does not backdate a source relation into the earlier comparison.

**Comparative-review-unit identity over revision.** A revised comparison table, regenerated comparison note, or updated guided review aid is not the same bounded comparison merely because the layout, title, or compared-source family stayed familiar. If new source input, revised source references, changed comparison criterion, changed shared review frame, or changed blocked downstream claim or effect changes the comparison identity or downstream use, publish the preserved comparative frame and the changed claims, or treat the result as a new comparative review unit before using it for a stronger crossed claim.

### E.17.ID.CR:4.3.g - Representation ontology and modeling lens (informative) {#representation-ontology-and-modeling-lens-informative}

The early canonical lens for this pattern is already stated near the top: one comparative review unit over already available, source-pinned epistemes or source-pinned publications, with the shared review frame preserved, one bounded contrast or small row set made visible, and blocked downstream claim or effect kept outside.

This pattern does not model interpretation in general.
It models one comparative review unit governed by `ComparativeReviewUnit` within the broader `InterpretationDiscipline` family.
In plain terms, the pattern works over the review unit itself.
That unit can appear as a comparison note, comparison sheet, or guided review aid, but it is not the whole review process or the source system.
The bounded comparison is the interpretive lift carried by that review unit.

The minimum typed lens is a compact record of:
- source references and source relation;
- one declared source-relation class;
- one declared comparison criterion and added-claim policy;
- one bounded-use boundary, one overread-risk line, and one `worldContactPolicy` that remains subordinate to the pattern governing a gate or adjudication claim; `A.21` governs a named gate decision under its applicable profile, while `A.20` applies only to a named internal-constraint check in a transformation-flow case;
- the relevant prompt, ontology, and authority boundary triggers;
- and which neighboring pattern still governs the base case when this remains a mixed overlay.

The lens keeps the main read tied to the review unit and the problem-owning review domain, while leaving source, continuity, and boundary discipline under whichever neighboring pattern still governs the base case.

### E.17.ID.CR:4.3.h - Working read-out {#working-read-out}

A working reader can usually say, in one short paragraph:
- what reviewed source episteme or source publication is being comparatively read;
- what bounded interpretive lift is being added;
- what shared review frame remains preserved, and, in the special same-EntityOfConcern case, why the same `EntityOfConcernRef` remains preserved;
- which crossed claim is still outside this pattern and which neighboring pattern would govern that claim if it became primary;
- and which boundary condition shows that the primary claim is no longer a bounded `ComparativeReviewUnit` claim.

If that read-out becomes fuzzy, the review unit is no longer bounded enough to stay here; narrow it, clarify it, or make the governing neighboring pattern primary for the crossed claim.

### E.17.ID.CR:4.4 - Branch-discipline summary {#branch-discipline-summary}

This section is the compact governing-rule summary for `ComparativeReviewUnit` inside the Core. Use the fuller solution, boundary table, worked slices, and relations section here only when specific clause wording, full field set, or full reopen conditions matter.

1. **Preserve the shared review frame.**
   Keep the reviewed source episteme or source publication set, source references, declared comparison criterion, and distinct alternative identities visible. If `contrastiveQuestion` is doing real review work, state it.
2. **Keep the lift bounded and comparative.**
   The review unit can add one bounded comparative or asymmetry-bearing lift. It stops when that lift starts carrying a stronger crossed claim.
3. **Name the crossed claim instead of repeating exclusions.**
   When the case stops being bounded comparison, name the claim that crossed the boundary and apply the pattern that governs it; use `E.17.ID.CR:4.5` to identify the relevant boundary.
4. **Keep neighboring-pattern authority explicit.**
   Bridge-mediated comparison requires an exact `bridgeOccurrenceRef` and a tuple-matched `boundedUseClaimRef` whose `EntityOfConcern` is that Bridge. Positive use requires affirmative polarity and, when A.10 or B.3 is triggered, current reliance for that exact use. Degraded reliance narrows the use; a negative, abstaining, reopened, evidence-needed, blocked, or mismatched result stops it. A Card and F.9.1 stance note remain optional and separate. Authorization and evidence that comparative-review Work occurred remain with their own patterns and records.
5. **Keep reader-fit bounded.**
   `targetUserModel`, `interactionMode`, `contrastiveQuestion`, `boundedComparativeUse`, and `overreadRisk` can be stated when they change actual review use, but they do not create authority that the unit does not carry.

### E.17.ID.CR:4.5 - Neighboring-work boundary glance {#neighboring-work-boundary-glance}

This table is a compact boundary aid for separating the comparative review unit from neighboring project work and source requirements.
For a fuller mixed-case read, read this table together with the neighboring pattern discipline.

| If the case is really doing this... | Governing pattern or bounded disposition |
| --- | --- |
| one local lexical head or qualifier is still doing too much work, but one honest repair would stabilize the same unit | `E.17.AUD.LHR` (`Local Head Restoration`) |
| the same note is mostly rewriting, reframing, or re-rendering the same EntityOfConcern with no bounded comparative lift | `A.6.3`, `A.6.3.CR`, or `A.6.3.RT` |
| the real job is only to add a short reading note about an already constituted F.9 bounded-use claim | `F.9.1`; a Card is optional packaging |
| the comparison wording is now making a relation-precision claim between compared items | `A.6.P` |
| the comparison wording is now making sameness, equivalence, alignment, mapping, substitution, or a cross-context Bridge claim | Part F with `A.6.9` for wording and F.9 for the Bridge and bounded-use claim; use F.9.1 only for an optional stance note about that claim |
| the note is primarily a reduced-use source-pinned rendering with narrower-use, blocked downstream use, and source-bearing reopen discipline | `A.6.3.CSC Controlled Semantic Coarsening` |
| one review unit already keeps the same primary entity of concern, one bounded comparison, and one outside-work boundary stable | `ComparativeReviewUnit` within `InterpretationDiscipline` |
| the same unit still has unstable reviewed-source, comparative-move identification, or outside-work boundary after local repair | `E.17.AUD.OOTD` (`PublicationUnit Primary-Subject Discipline`) |
| the real job is explanation-face governance on existing faces | `E.17.EFP` |
| the comparison now creates an abductive-prompt claim or action-selection question | `B.5.2.0` or `B.5.2` |
| the target or ontology is changing and now needs continuity witnesses | `OntologicalReframing` or `A.6.4` |
| the unit is now being used as a decision-making claim or decision record | `C.11` |
| the unit is now being used for execution, gate, or adjudication consequence | `A.15` for System-Role–Method–Work alignment, `A.15.1` for dated `U.Work`, and `A.21` for a named gate decision under its applicable profile; `A.20` only for a named internal-constraint check in a transformation-flow case; adjudication stays with its defining policy or pattern |

For first-minute use, read the four boundary rows around the comparative-review-unit case itself as a compact mirror of the near-top working-fit check and the ordinary working card:
- pressured local lexical head -> `E.17.AUD.LHR` (`Local Head Restoration`);
- stable same-object comparative review unit -> stay with `ComparativeReviewUnit`;
- same unit still unstable after local repair -> `E.17.AUD.OOTD` (`PublicationUnit Primary-Subject Discipline`);
- any stronger crossed claim already primary -> the governing pattern for that claim is primary.
If the comparison unit is already carrying neighboring work, use the boundary rows first and then read `E.17.ID.CR:5.4.7` through `E.17.ID.CR:5.4.10` as the nearest worked boundary examples.

### E.17.ID.CR:4.5.a - Ordinary working order for the card {#ordinary-working-order-for-the-card}

The shortest ordinary working order is:
1. name the base source relation or work question if the case is mixed;
2. pin the reviewed source episteme or source publication and make the shared review frame plus any distinct alternatives visible;
3. state the bounded comparative lift, or the small set of contrast rows and their row-level comparison criteria, in compact form;
4. declare the blocked downstream claim or effect and the review-only and non-executive world-contact limit;
5. name the boundary trigger that would end interpretation.

Use this order only to recover the seven-row ordinary working card in `E.17.ID.CR:4.3.b.a`; publish the resulting card in compact form whenever boundary pressure still stays low.

If the seven-row working card still cannot be completed plainly through that order, the review unit is not yet ready to stay here.
If the first question is what the note, sheet, or review aid is about, what move it carries, and what wider work remains outside, stabilize that `PublicationUnit` question with `E.17.AUD.OOTD` (`PublicationUnit Primary-Subject Discipline`) before continuing comparative-review-unit work.

## E.17.ID.CR:7 - Conformance Checklist {#conformance-checklist}

A conformance check is retained only if it changes the next bounded use of the comparative review unit, blocks a concrete overclaim, or preserves a source reference or reopen condition needed for the declared bounded use.

Use ID.CR-Core for ordinary comparison notes. Conditional rows apply only when the note touches neighboring-pattern relation, bridge declaration, or reader-fit fields. For fuller mixed-case read, read this checklist together with the neighboring pattern discipline and the boundary conditions gathered in this section.

**Assurance recovery note.** Use this checklist as a heavier check of the already-declared ComparativeReviewUnit governing rule, not as a second rule list. If a row cannot be recovered through the ordinary seven-row card, the nearest worked slices, or the practical safeguards already named in the pattern, the case is not yet stable enough to rely on checklist prose alone.

### E.17.ID.CR:7.1 - ID.CR-Core ordinary checks {#id-cr-core-ordinary-checks}

1. @fact:CC-ID-1 **CC-ID-1 - Bounded comparative review unit is explicit.** @status:spec/done
   The pattern distinguishes the bounded comparative review unit from the surrounding review or decision work.
2. @fact:CC-ID-2 **CC-ID-2 - Source references and comparison criterion are explicit.** @status:spec/done
   A reviewer can see what already-fixed source episteme or source publication is being interpreted and what declared comparison criterion or contrast is carrying the lift.
3. @fact:CC-ID-3 **CC-ID-3 - The lift stays bounded.** @status:spec/done
   The ordinary card keeps bounded lift, blocked downstream claim or effect, world-contact limit, and boundary trigger visible before any neighboring claim can be read from the unit.
4. @fact:CC-ID-6 **CC-ID-6 - Neighboring-pattern boundaries stay visible.** @status:spec/done
   When the boundary trigger fires, the neighboring FPF pattern carries that prompt, ontology, action, gate, authority, or downstream claim instead of leaving it hidden inside comparative prose.
5. @fact:CC-ID-8 **CC-ID-8 - The review unit does not over-claim authority.** @status:spec/done
   The unit remains review-only and non-executive; stronger authority use is carried only by the named governing pattern and project-side FPF kind and reference.

### E.17.ID.CR:7.2 - ID.CR-Conditional checks {#id-cr-conditional-checks}

1. @fact:CC-ID-4 **CC-ID-4 - Base-case governing-pattern relation is explicit.** @status:spec/done
   A reviewer can tell why the case does not really belong to `A.6.3.*`, an F.9 Bridge or bounded-use branch, an F.9.1 stance-note branch, `E.17.EFP`, `B.5.2(.0)`, `OntologicalReframing`, or `A.6.4`.
2. @fact:CC-ID-5 **CC-ID-5 - Bridge declaration does not hide.** @status:spec/done
   If the case depends on bridge-mediated comparison, `bridgeOccurrenceRef` and `boundedUseClaimRef` are required. The latter resolves a claim whose `EntityOfConcern` is that Bridge and whose use/direction/rule/loss/polarity tuple matches the comparative unit. Positive use requires affirmative polarity and, when A.10 or B.3 is triggered, current reliance for that exact use; degraded reliance narrows it, while a negative, abstaining, reopened, evidence-needed, blocked, or mismatched result stops it. Authorization and actual comparative-review Work remain separate. Optional `bridgeCardRef` remains packaging; optional `bridgeStanceRef` resolves a separate F.9.1 episteme whose `EntityOfConcern` is that claim.
3. @fact:CC-ID-7 **CC-ID-7 - Reader-fit stays bounded.** @status:spec/done
   `targetUserModel`, `interactionMode`, `contrastiveQuestion`, `boundedComparativeUse`, and `overreadRisk` are visible when needed, but they do not create an authority claim that the unit does not carry.

**Checklist recovery map.** If an assurance-side reader wants to recover one checklist row by value, use the nearest ordinary card row and worked recovery below before treating the checklist as self-sufficient:

| Checklist row | Recover through first | Nearest worked or practical recovery |
| --- | --- | --- |
| `CC-ID-1` | `E.17.ID.CR:4.3.b.a` rows **Reviewed source** and **Shared review frame and alternative identities** | `E.17.ID.CR:5.4.5`, `E.17.ID.CR:5.4.6`, `E.17.ID.CR:5.4.6.a` |
| `CC-ID-2` | `E.17.ID.CR:4.3.b.a` rows **Reviewed source**, **Source references**, and **Bounded lift** | `E.17.ID.CR:5.4.5`, `E.17.ID.CR:5.4.6`, `E.17.ID.CR:5.4.6.a` |
| `CC-ID-3` | `E.17.ID.CR:4.3.b.a` rows **Bounded lift**, **Blocked downstream claim or effect**, and **World-contact limit** | `E.17.ID.CR:5.4.6`, `E.17.ID.CR:5.4.10`, `E.17.ID.CR:5.4.11` |
| `CC-ID-4` | near-top **Neighboring-work boundary**, **Quick working-fit check**, and `E.17.ID.CR:4.5 - Neighboring-work boundary glance` | `E.17.ID.CR:5.4.7` through `E.17.ID.CR:5.4.10` |
| `CC-ID-5` | `E.17.ID.CR:4.3.d` bridge-declaration fields plus `E.17.ID.CR:4.2` neighboring patterns | `E.17.ID.CR:5.4.1`, `E.17.ID.CR:5.4.2`, `E.17.ID.CR:5.4.3` |
| `CC-ID-6` | `E.17.ID.CR:4.3.b.a` row **Boundary trigger** plus the near-top boundary corridor | `E.17.ID.CR:5.4.7` through `E.17.ID.CR:5.4.10` |
| `CC-ID-7` | `E.17.ID.CR:4.3.d` interpretant-side fields, kept subordinate to the ordinary card and blocked downstream claim or effect | `E.17.ID.CR:5.4.4`, `E.17.ID.CR:5.4.6`, `E.17.ID.CR:5.4.6.b` |
| `CC-ID-8` | `E.17.ID.CR:4.3.b.a` rows **Blocked downstream claim or effect** and **World-contact limit** | `E.17.ID.CR:5.4.6`, `E.17.ID.CR:5.4.10`, `E.17.ID.CR:5.4.11` |

## E.17.ID.CR:9 - Consequences {#consequences}

- The middle band between a short F.9.1 stance note about an existing bounded-use claim and prompt-bearing abduction becomes reviewable rather than rhetorical.
- Reviewers get a cleaner way to distinguish comparative interpretation from the first crossed claim that would make another governing pattern primary.
- Authors pay a small extra declaration weight, but the gain is fewer hidden neighboring-pattern boundary mistakes and less comparison-unit instability.
- Guided comparative review units become easier to prepare honestly because bounded use, overread risk, and world-contact limits can be declared without pretending that the unit already carries a broader guidance claim than it really does.
- Users get a bounded way to keep comparative review units modest while the boundary trigger remains below the first crossed claim.

## E.17.ID.CR:12 - Relations {#relations}
- **Citation.** Cite this pattern as `E.17.ID.CR`, `ID.CR`, or `ComparativeReviewUnit` when the current object is one bounded comparative review unit. Use `A.6.3.CR` when the intended pattern is `ConservativeRetextualization`.
- **Placement.** `ComparativeReviewUnit` sits inside the wider `InterpretationDiscipline` naming family, but the local governing object is the comparative review unit and its bounded comparison. The wider review or decision work remains outside until a crossed claim becomes primary.
- **Builds on:** `C.2.2a`, `A.16.0`, `F.9`, `F.9.1`, Part F, `A.6.9`, and `E.14`.
- **Coordinates with:** `A.6.P`, `A.6.3`, `A.6.3.CR`, `A.6.3.RT`, `A.6.3.CSC`, `F.9`, `F.9.1`, Part F, `A.6.9`, `E.17.EFP`, `B.5.2.0`, `B.5.2`, `OntologicalReframing`, `A.6.4`, `C.11`, `A.15`, `A.15.2`, `A.15.4`, `A.20`, `A.21`.
- **Boundary map.** Use `E.17.ID.CR:4.5` when the comparison starts carrying relation precision, bridge or sameness, prompt or action selection, ontology or changed target, decision, work or reliance, gate, assurance, adjudication, or reduced-source-use claims. The neighboring pattern governs only the crossed claim it names.
- **Local repair neighbors.** Use `E.17.AUD.LHR` only when a local lexical head or qualifier still destabilizes the same unit; use `E.17.AUD.OOTD` only when the reviewed-source, publication-unit, comparative-move, or outside-work boundary is still unstable after local repair.


## Dependencies {#dependencies}

- @fact:DEPENDS-ON Dependencies (as published): `spec://ai.lev/fpf-spec/contract/C-2-2a#root`, `spec://ai.lev/fpf-spec/contract/A-16-0#root`, `spec://ai.lev/fpf-spec/contract/F-9#root`, `spec://ai.lev/fpf-spec/contract/E-14#root`; coordinates with `spec://ai.lev/fpf-spec/contract/E-17-EFP#root`, `spec://ai.lev/fpf-spec/contract/E-17-AUD-LHR#root`, `spec://ai.lev/fpf-spec/contract/E-17-AUD-OOTD#root`, `spec://ai.lev/fpf-spec/contract/A-6-3#root.*`, `spec://ai.lev/fpf-spec/contract/A-15#root`, `spec://ai.lev/fpf-spec/contract/A-20#root`, `spec://ai.lev/fpf-spec/contract/A-21#root` @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-6-3-CR#root, spec://ai.lev/fpf-spec/contract/A-6-3-CSC#root, spec://ai.lev/fpf-spec/contract/A-6-3-RT#root, spec://ai.lev/fpf-spec/contract/C-2-P#root, spec://ai.lev/fpf-spec/contract/C-22-2#root, spec://ai.lev/fpf-spec/contract/C-29#root, spec://ai.lev/fpf-spec/contract/E-17#root, spec://ai.lev/fpf-spec/contract/E-17-AUD#root, spec://ai.lev/fpf-spec/contract/E-17-AUD-LHR#root, spec://ai.lev/fpf-spec/contract/E-17-AUD-OOTD#root, spec://ai.lev/fpf-spec/contract/E-17-EFP#root, spec://ai.lev/fpf-spec/contract/F-9#root, spec://ai.lev/fpf-spec/contract/F-9-1#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/E-17-ID-CR
