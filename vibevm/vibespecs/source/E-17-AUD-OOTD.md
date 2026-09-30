# E.17.AUD.OOTD - PublicationUnit Stability Discipline and PublicationUnit Primary-Subject Discipline - publication-unit stability over one primary subject: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## E.17.AUD.OOTD:5 - Archetypal grounding {#archetypal-grounding}

**Worked-slice status.** Read the architecture, operations, episteme-publication-heavy, comparison-return-to, and changed-concern cases as a heterogeneous example bank, not as one recommended progression.

### E.17.AUD.OOTD:5.1 - Architecture note shifting into rollout work {#architecture-note-shifting-into-rollout-work}

A short architecture memo begins with:
`This note is about the proposed service boundary between catalog and checkout.`

Three paragraphs later it says:
`We should therefore assign rollout responsibility to platform and stage migration in two sprints.`

The fix is not only lexical.
The memo's primary subject began as the service boundary, but its carried move changed from describing or assessing that boundary to proposing responsibility assignment and a two-sprint rollout; its apparent downstream use changed from understanding to planning and decision. None of those changes by itself proves that the `C.2.1` `EntityOfConcern` of an exact carried episteme changed.
Repair the memo in one of two ways:
- keep the note about the boundary and push rollout outside;
- or make the changed move and downstream use explicit and use a downstream decision or rollout publication.

**Repaired two-sentence memo.** `This memo assesses the proposed service boundary between catalog and checkout. Rollout sequencing, responsibility assignment, and approval remain outside this memo.`

**Action saved.** The author publishes those two sentences and stops: no six-row artifact, empty transition declaration, neighboring-pattern reference, assurance record, or evidence package is produced. A rollout record opens only if rollout later becomes current work.

### E.17.AUD.OOTD:5.2 - Operations note shifting into approval {#operations-note-shifting-into-approval}

An incident note begins as a comparative review of timing variance and operator context.
It ends as if it already recommends a production action.

The incident episode may remain the primary subject while the foregrounded concern changes and the carried move shifts from comparison to recommendation. Keep the review unit about the episode and the contrast it is surfacing; put action approval in an explicit outside-work or downstream decision text.

Use `C.11` if the new text chooses among already available actions. If an actual approving communication and an instituted permission matter, keep the `A.2.9` communicative Work and the `A.2.8.PER` grant relation separate. Use `A.21` only when a current `OperationalGate(profile)` actually publishes a gate decision.

### E.17.AUD.OOTD:5.3 - Semio-heavy text mixing one local section and wider architecture strategy {#semio-heavy-text-mixing-one-local-section-and-wider}

A semio note starts about one selected pattern section and ends as if it had decided the packaging strategy for the whole overlay.

Here the primary subject broadens from the selected section to the whole overlay, and the carried move broadens from local interpretation to strategy. The unit should state:
- what the note is about now;
- what concern and move it carries over that subject;
- and what wider architecture strategy remains outside the current unit.

### E.17.AUD.OOTD:5.4 - Unit stabilizes and bounded comparison becomes primary {#unit-stabilizes-and-bounded-comparison-becomes-primary}

A review note first shifts between the selected interface boundary, the move it is making over the current evidence, and the rollout implications around that boundary.
After one honest publication-unit repair it now says:
`This review unit is about the interface-boundary options and the contrast they make visible under the current incident evidence; rollout responsibility and approval remain outside this note.`

At that point the same unit already holds one stable primary subject, one carried comparison move, and one outside-work boundary.
`PublicationUnit Primary-Subject Discipline` has done its job.
If the remaining question is now one bounded comparison between the already pinned options over the same evidence, the honest next pattern application is `E.17.ID.CR` rather than keep thickening publication-unit discipline.

### E.17.AUD.OOTD:5.5 - Outside observation changes the live concern or carried claim {#outside-observation-changes-the-live-concern-or-carried-claim}

A release-readiness note is already explicit that it is about one candidate publication or view and the risk state visible from the current evidence.
Mid-review, an external vendor bulletin and a new field observation change the reported failure boundary for that same candidate.

The candidate may remain the primary subject. What changed first is the evidence-facing concern and the claim the note can honestly carry; a later approval or execution question may also change the downstream use. Do not report an `EntityOfConcern` change unless one identified claim-bearing episteme actually has a different exact entity participant under `C.2.1`.
Repair the note in one of three ways:
- stop the current unit at the originally declared evidence boundary and open a new downstream record for the changed question;
- explicitly reopen the same unit with the revised concern, claim or carried move, permitted use, and outside-work boundary;
- or use the downstream decision or work pattern whose instructions now fit once approval, execution, or another downstream decision publication becomes the more honest primary question.

The bulletin and field observation remain sources until a support, evidence, or currentness claim makes `A.10` relevant. Use `C.11` for a later choice, `A.2.9` and `A.2.8.PER` for an approving act and its permission effect, `A.15` for a work claim, and `A.21` only for an actual gate decision.

### E.17.AUD.OOTD:5.6 - Deliberately sectioned multi-subject review packet {#deliberately-sectioned-multi-subject-review-packet}

A release-readiness group needs one packet for one meeting. The packet contains three clearly headed sections:

1. **Interface-boundary options** — compares two architecture alternatives.
2. **Incident evidence** — summarizes the observations that discriminate between those alternatives.
3. **Rollout constraints** — states constraints the later approval decision must respect, without assigning work or granting approval.

The local one-subject heuristic does not force three documents. The packet has one honest umbrella subject—`the evidence and constraints needed to review the interface-boundary choice`—and one bounded use: inform the review, not approve rollout. Keeping the three section-level subjects together avoids navigation and synchronization cost, while the headings prevent their different moves from masquerading as one claim.

An unsectioned version is rejected because readers cannot see the subject and move changes. A short narrative with only one small shift may instead declare that transition. Separate documents become the least-cost choice when the rollout section starts assigning responsibility, serves another audience, needs independent reuse, or becomes an approval input with its own reliance boundary.

## E.17.AUD.OOTD:6 - Bias-Annotation {#bias-annotation}
This section intentionally biases toward explicit publication-unit stability and against quietly letting one unit absorb wider work or decision pressure by habit.
The main mitigation is explicit primary-subject, concern, carried-move, downstream-use, and outside-work surfacing; conditional use of exact `EntityOfConcern` only when `C.2.1` warrants it; early return to `E.17.ID.CR` when publication-unit stability is already solved; and an explicit boundary choice once a downstream claim becomes primary.

## E.17.AUD.OOTD:8 - Common Anti-Patterns {#common-anti-patterns}

- **Local-repair inflation.** Opening publication-unit discipline when one overloaded local lexical head or qualifier is still the real defect.
- **`EntityOfConcern` inflation.** Calling every topic, kind, interpretation, question, or writing transition an `EntityOfConcern` or `EntityOfConcern` change.
- **Work-process smuggling.** Letting a note begin as architecture, incident review, or comparison work and end as rollout, approval, or execution guidance without naming the transition.
- **Admissibility-pattern replacement.** Treating this pattern as if it replaced view, face, or carrier architecture, entityOfConcernRef-preserving transform rules, explanation-face rules, bridge rules, or downstream decision texts.
- **Overgrowth by declaration.** Stacking heavier fields onto a unit that still cannot keep one stable primary subject, one move, and one outside-work boundary in place.

## E.17.AUD.OOTD:10 - Rationale {#rationale}

The point of this pattern is not to create a second architecture of views, faces, carriers, epistemes, or downstream decision texts.
It is narrower: one publication unit can become misleading even when every single sentence looks locally acceptable.

`A.6.P`, `A.7`, `E.10`, and `F.18` already keep kinds, distinctions, and naming precise. `C.2.1` already identifies the exact entity participant of one claim-bearing episteme. This pattern adds only the missing publication-unit discipline: choose the least-cost honest architecture for a bounded readable unit, make its primary subject or section-level subjects and moves visible, and keep downstream use and outside work explicit. It borrows `EntityOfConcern` only through the exact conditional projection in 4.1.b and does not extend that ontology.

The pattern also stays intentionally close to `E.14` and `E.19`.
Recognition comes first through a manager-usable entry block and one ordinary natural-language declaration; the six prompts remain an optional diagnostic.
Heavier declaration comes only after the ordinary declaration already holds and a named receiving use consumes the added fields.

## E.17.AUD.OOTD:11 - SoTA-Echoing {#sota-echoing}

**Source boundary.** These sources support topic focus, scope/non-scope, reader-need organization, and explicit document structure. None establishes a universal ontological rule that every publication unit has one subject, and none supplies a `C.2.1` entity participant. OOTD therefore keeps the one-primary-subject rule as a defeasible local heuristic and compares it with transition, sectioning, and splitting.

| Publication-unit obligation | Exact source and current contribution | Local repair of the source limit | Working implication here |
| --- | --- | --- | --- |
| Keep the current unit focused and expose its scope and non-scope. | [Google Technical Writing One — Documents](https://developers.google.com/tech-writing/one/documents) (updated 2025-07-07) tells authors to state scope and non-scope, then refocus or revise the scope when content veers; [Paragraphs](https://developers.google.com/tech-writing/one/paragraphs) (updated 2025-03-28) treats a paragraph as one independent unit of logic focused on one topic. | Paragraph focus does not imply one subject for every memo, packet, or document. OOTD scales the move by naming the bounded unit and comparing retention, explicit transition, sectioning, and splitting. | `E.17.AUD.OOTD:4.2.a`, `E.17.AUD.OOTD:4.3`, `E.17.AUD.OOTD:5.1`, `E.17.AUD.OOTD:5.6` |
| Organize documentation around the user's need and keep different action/cognition modes visible. | [Diátaxis](https://diataxis.fr/) organizes content, architecture, and form around four distinct user needs; its [compass](https://diataxis.fr/compass/) tests whether material informs action or cognition and supports acquisition or application, at sentence or whole-document scale. | The four modes diagnose a use shift but are not an FPF ontology or a formula for document count. OOTD names the actual carried move and downstream use, then keeps one structured unit only when a shared reader goal makes that cheaper and still clear. | `E.17.AUD.OOTD:4.1.a`, `E.17.AUD.OOTD:4.2.a`, `E.17.AUD.OOTD:5.2`, `E.17.AUD.OOTD:5.6` |
| Use a single-subject reusable topic when modular reuse is the main need. | [OASIS DITA 1.3 `<topic>`](https://docs.oasis-open.org/dita/dita/v1.3/os/part1-base/langRef/base/topic.html) defines the top-level topic as a single-subject topic or article. This is established structured-authoring lineage (2015), not the current source of OOTD's whole-document rule. | A DITA topic is one valid reusable unit architecture, not evidence that a deliberately sectioned review packet is defective. OOTD selects it when independent reuse or retrieval dominates and otherwise permits the coherent multi-section unit. | `E.17.AUD.OOTD:4.2.a`, `E.17.AUD.OOTD:5.6` |
| Keep object words and local designations precise without importing another concept system. | ISO 704:2022 and ISO 1087:2019 terminology practice distinguishes objects, concepts, definitions, designations, and terms. | Terminology discipline repairs overloaded heads but does not choose the publication architecture. OOTD first uses `E.17.AUD.LHR`, then makes subject, concern, carried move, and use explicit only when unit-level instability remains. | `E.17.AUD.OOTD:4.1.a`, `E.17.AUD.OOTD:4.2`, `E.17.AUD.OOTD:5.3` |


## E.17.AUD.OOTD:End {#end}
