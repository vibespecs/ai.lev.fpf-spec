# A.6.3.CR - ConservativeRetextualization: EntityOfConcern-Preserving Textual Re-Expression {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Specialization pattern
> **Status:** Stable
> **Normativity:** Normative

## A.6.3.CR:1 - Problem frame {#problem-frame}

Use this pattern when one already available source line about the same EntityOfConcern needs a second textual form: a report rewrite, summary, translation, or declared filtered restatement. The real job is still same-entity textual re-expression, not explanation, representation change, bridge work, retargeting, evidence, gate authority, or work authorization.

**Primary governed case.** One textual re-expression of already available source claims whose resolved EntityOfConcern remains the same. The source and receiving epistemes concern that entity; the textual rendering expresses the receiving claims.

**First useful move.** Separate the source slice, the published slice, the omission or source-loss note, and the admissible use. If preservation is doubtful, name the missing basis or defect; repair it within CR when possible, or name the pattern for the actual changed claim or use.

**What goes wrong if missed.** A summary, translation, or manager-readable rewrite is treated as harmless editing after it has started hiding explanation work, bridge work, changed authority relation, or a narrower admissible use.

**What this buys.** One honest same-entity textual rewrite with visible source-relation tether, visible omission or loss notes, and a clear repair or next-pattern route when conservativity fails.

**Ordinary use.** If the rewrite is admissible only for orientation, source-finding, review, comparison, or planning preparation, one source-slice to published-slice sentence or mini-card with the admissible use and visible omission or source-loss note is enough.

**Reliance-facing use.** Open the fuller rewrite-admissibility record only when the rewritten text will be externally relied on, disputed, cited as a source-relation reason, used across context, or read as release, gate, work-preparation, engineering-justification, approval, or evidence justification.

**Not this pattern when.** Not this pattern when the case is primarily explanatory rendering (`ExplanationFaithfulnessProfile`), representation-scheme change (`RepresentationSchemeTransition`), changed EntityOfConcern (`A.6.4`), comparative review (`E.17.ID.CR`), an F.9 Bridge or bounded-use claim, an optional F.9.1 stance note about such a claim, or a deliberately coarsened rendering whose narrower admissible use, non-admissible downstream use, and source-bearing return have become primary. In that last case, use `A.6.3.CSC Controlled Semantic Coarsening`.

## A.6.3.CR:2 - Problem {#problem}

Without a dedicated pattern for conservative textual re-expression:
1. report, summary, translation, and filtered rewrite cases are handled ad hoc;
2. authors treat textual simplification as if it were automatically conservative;
3. the boundary to explanation-facing renderings stays blurry;
4. correspondence-mediated rewrites are not distinguished from direct rewrites;
5. subsequent users cannot tell whether the result is still a view of the same EntityOfConcern or a new interpretive publication.

## A.6.3.CR:3 - Forces {#forces}

- **Same entity, different wording.** Readers need different textual forms without reopening the EntityOfConcern.
- **Compression vs loss visibility.** Shorter or plainer forms are often useful, but omissions and source-loss modes must stay explicit.
- **Direct vs correspondence-mediated rewrites.** Some rewrites read from one source episteme; others depend on a declared `CorrespondenceModel`.
- **Textual focus vs family creep.** The pattern should cover same-entity textual re-expression, not explanation, not representation-wide shifts, and not retargeting.
- **Publication discipline.** Admissible MVPK faces and publication renderings still matter even when the transform looks like "just a rewrite."

## A.6.3.CR:4 - Solution — entityOfConcernRef-preserving textual re-expression under `A.6.3` {#solution-entityofconcernref-preserving-textual-re-expression}

### A.6.3.CR:4.1 - Informal definition {#informal-definition}

> `ConservativeRetextualization` is a named pattern specialized under `A.6.3 U.EpistemicViewing` for textual re-expression of the same EntityOfConcern.
>
> It preserves the exact EntityOfConcern resolved by each side's `entityOfConcernRef` under that side's effective ReferenceScheme, keeps the transform effect-free, and allows only claim-preserving or explicitly loss-declared rewriting of already available content.
>
> It may change register, ordering, textual density, language, emphasis, or local wording. It may not silently introduce new claims, an F.9 Bridge, bounded-use suitability, current reliance, authorization, actual receiving use, new Work, evidence, gate, release, policy, assurance, adjudication force, or a changed EntityOfConcern.

Here, **entityOfConcernRef-preserving** means that resolved-entity equality, not identical reference spelling. Keep a material reference or scheme change explicit under `A.6.3:4.3`.

### A.6.3.CR:4.1.a - Pattern, case, and publication distinction {#pattern-case-and-publication-distinction}

`ConservativeRetextualization` is a **pattern description** and a named specialization under `A.6.3`. Concrete entityOfConcernRef-preserving rewrites are passive episteme cases or publication texts reviewed under this pattern.

This distinction matters because the pattern defines or constrains **how** a rewrite is recognised, justified, and checked.

### A.6.3.CR:4.1.b - Local working vocabulary {#local-working-vocabulary}

This pattern repeatedly uses a small working vocabulary.
- **Source slice** = the already available pinned or otherwise reviewable textual content being restated.
- **Published slice** = the resulting textual rendering that remains under entityOfConcernRef-preserving discipline.
- **Ordinary case** = a reviewable same-entity rewrite where a short account keeps the source tether, omission notes, and neighboring-pattern conditions readable.
- **Case needing fuller review** = a case where dispute, policy, assurance, required correspondence witness, or cross-context reliance makes a fuller record worth publishing.

`sourceSlice` and `publishedSlice` are local review labels for the source textual slice and resulting textual rendering in one rewrite case. A `publishedSlice` remains a rendering label. When one exact selected `U.Episteme` is made available, E.24.PUB separately requires its bounded-use declaration, publication form, carrier, and obtaining `EpistemePublicationRelation`; no publication kind or second episteme identity follows from the slice label.

These local review labels follow the `E.17:5.1e` local-field rule.

### A.6.3.CR:4.2 - Scope and exclusions {#scope-and-exclusions}

**In scope**
- entityOfConcernRef-preserving report rewrite;
- entityOfConcernRef-preserving summary;
- entityOfConcernRef-preserving translation between natural-language textual forms;
- declared filtering or foregrounding of already-present claims in textual form.
- correspondence-witnessed textual synthesis where every receiving claim remains recoverable to one entityOfConcernRef-preserving source line or declared entityOfConcernRef-preserving correspondence witness.

**Out of scope**
- a difference between the EntityOfConcern values resolved by the source and receiving references, including a hidden change of EntityOfConcern (`A.6.4`);
- explanation-facing renderings whose main purpose is explanatory rendering rather than same-entity rewrite (`ExplanationFaithfulnessProfile`);
- representation-regime changes such as text→table, text→diagram, or text→latent form (`RepresentationSchemeTransition`);
- comparison, abductive-prompt, ranking, recommendation, bridge-mediated, substitution, or action-selection work that introduces new claims rather than restating available ones.

### A.6.3.CR:4.2.a - Reader guidance {#reader-guidance}

Use this pattern when the EntityOfConcern stays fixed and textual restatement remains the primary move.
- If the main change is explanatory, apply ExplanationFaithfulnessProfile.
- If the main change is a representation-scheme shift, apply RepresentationSchemeTransition.
- If the EntityOfConcern changes, apply A.6.4.

### A.6.3.CR:4.2.b - What the user checks first {#what-the-user-checks-first}

The user usually does not begin by filling every field name. The first useful questions are simpler:
1. Is the published result still about the same EntityOfConcern?
2. Does the result remain a textual restatement, or is explanation or a representation-scheme change now primary?
3. Can the reader see what was omitted, softened, or foregrounded?
4. If several source slices or a correspondence witness are doing work, can each receiving claim be traced to one entityOfConcernRef-preserving source line or declared entityOfConcernRef-preserving correspondence witness?
5. Is the source merely pointed at, was it actually used, are the rewritten claims recoverable from it, and is the result admissible for the intended use?
6. If any answer is doubtful, is the problem a missing source or condition, a repairable preservation defect, or an actual changed claim needing another pattern?

If omissions, softening, or filtering are admissible only because the published result is coarsened, tied to narrower admissible use, non-admissible for downstream use, and tied to source-bearing return, the case has crossed out of ordinary conservative retextualization even if the prose still looks like a summary. Use `A.6.3.CSC Controlled Semantic Coarsening` for that source-to-rendering relation.

Here, **source-bearing return** means returning to the source-bearing content. First identify any missing source or condition and repair and recheck a preservation defect within CR when the intended restatement can be restored. A **changed-claim exit** applies when the attempted claim really becomes explanation, representation shift, retargeting, gate, evidence, Work, assurance, or Bridge use: name that claim and use the pattern that defines, constrains, or tests it. Resolve the exact predicate or defining `ClaimGraph` only when the current claim or a named later use depends on that rule edition. A coarsened textual slice may need both source-bearing return and a changed-claim exit.

Only after these questions are answered does a fuller review record usually become worth writing.

### A.6.3.CR:4.3 - Working-model first; explicit review record only when the case needs fuller review {#working-model-first-explicit-review-record-only-when-the-case}

Follow **E.14’s working-model-first discipline**: an ordinary report, summary, or translation states what stayed the same, what was omitted, when the rewrite stops being conservative, and which pattern to use next. Put only the support needed for the current review or reliance question beneath that account.

**Ordinary case (default).** For everyday entityOfConcernRef-preserving rewrites, it is usually enough that the text or its surrounding publication keeps explicit:
- which source `U.Episteme` claims are being re-expressed;
- that the EntityOfConcern resolved by each side's `entityOfConcernRef` remains the same;
- whether the case is direct or correspondence-mediated when that is not obvious;
- what omissions or source-loss modes matter for the reader;
- which pattern to use if the case becomes explanation, representation shift, retargeting, gate, evidence, work, assurance, Bridge use, or another non-retextualization claim.

**Explicit review record (when fuller review is needed).** A fuller record is warranted when the case is assurance-facing, gate-adjacent, cross-context, correspondence-heavy, policy-bearing, or likely to be disputed. Include or inherit the fields needed to inspect the material preservation, correspondence, source-use, or downstream-use question. The record may inherit pattern ids and already-pinned metadata instead of restating them inline. The available field groups are:
- transform relation (`patternSpecializationRef = A.6.3 specialization`, `relationFunctionClaimRef`, `sourcePublicationOrRecordForm`, `targetPublicationOrRecordForm`, `changeTargetRef`);
- preservation context (`entityOfConcernPolicy = preserve`, `boundedContextPolicy`, `viewpointPolicy`, `referenceSchemePolicy`, `representationSchemePolicy`, `groundingPolicy`, `referencePlanePolicy`);
- claim and publication discipline (`claimPolicy`, `claimScopePolicy`, `publicationScopePolicy`, `reliabilityTransportPolicy`, `pinningPolicy`, `provenancePolicy`, `lossProfile`);
- continuity and bridge discipline (`claimContinuityClass`, `microtheoryContinuityClass`, `onticContinuityClass`, `bridgeRequirement`, `conservativityWitness`);
- downstream and admissibility discipline (`worldContactPolicy`, `evidencePolicy`, `gatePolicy`, `workCrossing`, `upstreamPatternLocator`, `downstreamPatternLocator`, `admissibleFaces`, `admissiblePublicationRenderings`, `compositionRule`, `reopenCondition`);
- naming and presentation discipline (`publicNamePolicy`).

The fuller record makes these cases reviewable without hiding meaning in style, topic familiarity, or editor intuition.

### A.6.3.CR:4.3.a - Ordinary admissibility defaults {#ordinary-admissibility-defaults}

Default admissibility for ordinary entityOfConcernRef-preserving textual cases:
- primary admissible faces are `PlainView` and `TechCard`;
- bounded report-only use is admissible when source pins, provenance, loss notes, and entityOfConcernRef-preserving conservativity remain visible;
- `InteropCard` use is admissible only when the governing publication-face source explicitly permits source-pinned, text-preserving export without added semantics;
- `AssuranceLane` or gate-bearing use is not default and requires governing publication-face policy plus source-pinned conservativity without hidden strengthening.

### A.6.3.CR:4.4 - Direct and correspondence-mediated profiles {#direct-and-correspondence-mediated-profiles}

**Direct ConservativeRetextualization**
- source slice and published slice are textual re-expressions of one source episteme;
- no `CorrespondenceModelRef` is needed;
- the main required admissibility record is explicit loss and provenance discipline.

**CorrespondenceConservativeRetextualization**
- the receiving textual rendering is derived from a declared correspondence between epistemes or views of the same EntityOfConcern;
- `CorrespondenceModelRef` is required;
- the result remains under `A.6.3` only if the correspondence witnesses entityOfConcernRef-preserving conservativity and no new claims are imported beyond the declared witness set.

Cross-language translation is not automatically direct. If the translation depends on declared correspondence, reference-scheme mediation, or bounded equivalence notes, it must be treated as correspondence-mediated rather than disguised direct rewriting.

### A.6.3.CR:4.4.a - Recurring same-entity textual moves {#recurring-same-entity-textual-moves}

The pattern covers a small family of recurring textual moves as long as the same EntityOfConcern remains explicit:
- **Register shift** — a technical statement is rewritten into plainer engineer-manager prose without changing what is being said about the same entity.
- **Summary or filtered restatement** — a source note is shortened or focused on one declared slice, with omissions stated rather than hidden.
- **Cross-language restatement** — the same source claim is restated in another natural language while the same source tether and same-entity line remain explicit.
- **Correspondence-witnessed textual synthesis** — one textual rendering is produced from declared same-entity correspondences without importing an extra bridge or substitution admissibility record.

These are recurring move shapes, not separate patterns. The specialization relation remains the same: entityOfConcernRef-preserving textual re-expression under `A.6.3`.

### A.6.3.CR:4.5 - Shared conservative retextualization rule bundle {#shared-conservative-retextualization-rule-bundle}

#### A.6.3.CR:4.5.a. Preservation rule {#a-6-3-cr-4-5-a-preservation-rule}
A case under `ConservativeRetextualization` preserves the same resolved EntityOfConcern, the declared bounded context, and the already available claim-bearing source while changing wording, register, language, ordering, or density. It states what remains preserved about claim scope, publication scope, pins, provenance, grounding, and ontic scaffold, and it says whether the case is `Direct` or `Correspondence`.

#### A.6.3.CR:4.5.b. Loss and reliability rule {#a-6-3-cr-4-5-b-loss-and-reliability-rule}
A reviewed case makes explicit what is omitted, shortened, foregrounded, or carried only through a declared source-loss mode by the rewrite. Reliability transport may remain source-bounded or be explicitly downgraded, but it must never be silently widened by cleaner prose, more forceful rhetoric, or management-facing polish.

#### A.6.3.CR:4.5.c. Authority and changed-claim boundary {#a-6-3-cr-4-5-c-authority-and-changed-claim-boundary}
A case reviewed under this pattern stays about the same entity and remains an episteme-to-episteme textual rewrite. It does not establish explanation faithfulness, an F.9 Bridge or bounded-use suitability, retargeting, current reliance, authorization, or actual receiving use. If the rewrite becomes explanatory, Bridge-bearing, gate-bearing, or world-facing, state the attempted claim and use the pattern that defines, constrains, or tests it. Use F.9 for a semantic Bridge between two exact F.17 local senses or a proposed bounded use of that Bridge. Take a current reliance question to triggered A.10 or B.3 and authorization to the pattern that directly constrains the receiving act. For an asserted occurrence, first recover the actual object or occurrence under its direct obtaining or admission rule, then cite the evidence on which the assertion relies. A precise dated Work claim needs A.13 and independent A.15.1 admission; add F.6 only for precise assignment-bound attribution. Do not create those records when their branches are not live.

#### A.6.3.CR:4.5.d. Composition and reopen rule {#a-6-3-cr-4-5-d-composition-and-reopen-rule}
Repeated direct rewrite over the same source line may be idempotent, but heterogeneous rewrites and correspondence-mediated rewrites are generally order-sensitive. A reviewed case must reopen whenever correspondence witness, source pins, provenance, admissible-face assumptions, or entityOfConcernRef-preserving conservativity stop being explicit. Revalidate the affected claims when a load-bearing source, correspondence witness, provenance, face or use assumption, or preservation condition changes, even if it remains explicit; use `E.17:5.1b–c` for the applicable reopen condition.

#### A.6.3.CR:4.5.e. Non-collapse note for correspondence {#a-6-3-cr-4-5-e-non-collapse-note-for-correspondence}
Correspondence-mediated retextualization does **not** by itself establish an F.9 Bridge, bounded-use suitability, current reliance, authorization, or actual receiving use. Apply F.9 when a cross-local-sense semantic Bridge or a proposed bounded use of that Bridge is claimed. When reliance is current, apply triggered A.10 or B.3. The pattern for the receiving act handles authorization; recover any asserted occurrence under its direct obtaining or admission rule and cite evidence when the assertion relies on it. These are independent questions, not a mandatory record bundle for every rewrite.

#### A.6.3.CR:4.5.f. Local conservativity witness for borderline textual cases {#a-6-3-cr-4-5-f-local-conservativity-witness-for-borderline}
For borderline textual rewrites, the user treats the case as conservative only while each point below remains visibly preserved or its loss is declared and admissible for the stated use. A missing basis or repairable defect follows the repair route in §4.2.b; an actual changed claim or use follows the pattern that defines, constrains, or tests it.
- **Modality and force.** A rewrite may not silently turn possibility, uncertainty, permission, obligation, recommendation, decision status, bounded scope, temporal window, or hypothesis language into a wider commitment.
- **Caveats and qualifications.** A rewrite may not quietly remove conditions, exception notes, uncertainty markers, or temporal qualifiers that still matter for interpreting the same source.
- **Reliability assessment.** Cleaner prose, better ordering, or manager-facing polish may not silently raise confidence, warrant claim, or readiness for action.
- **Bridge and receiving-use boundary.** Same-entity textual fluency may not establish a semantic Bridge between local senses, bounded-use suitability, current reliance, authorization, or a comparative-review occurrence. Open only the F.9, A.10 or B.3, authorization, or occurrence branch that the actual later use needs; recover an asserted occurrence under its direct obtaining or admission rule.
- **Alternative preservation.** A rewrite may not collapse open alternatives, rival hypotheses, or declared plurality into one apparently settled interpretation unless the loss is stated and still admissible under this pattern.

This witness is local to `ConservativeRetextualization`. It does not replace the broader conservativity invariants of `A.6.3`; it makes them inspectable for textual rewrites where fluent prose can otherwise hide strengthening.

## A.6.3.CR:7 - Conformance Checklist {#conformance-checklist}

1. @fact:CC-CR-1 **CC-CR-1 — Same EntityOfConcern remains explicit.** @status:spec/done
   The EntityOfConcern values independently resolved by the source and receiving `entityOfConcernRef` values are equal.
2. @fact:CC-CR-2 **CC-CR-2 — Textual re-expression remains the right family.** @status:spec/done
   Textual restatement remains primary; explanation or a material representation-scheme change is not the primary move.
3. @fact:CC-CR-3 **CC-CR-3 — Loss, provenance, pinning, and reliability are explicit or inherited by pinned reference.** @status:spec/done
   The case states these explicitly or inherits them through already-pinned content that remains visible to review.
4. @fact:CC-CR-4 **CC-CR-4 — Direct vs correspondence split is explicit.** @status:spec/done
   The direct-vs-correspondence split is explicit and justified.
5. @fact:CC-CR-5 **CC-CR-5 — Correspondence witness is named where needed.** @status:spec/done
   If correspondence-mediated, `CorrespondenceModelRef` is declared.
6. @fact:CC-CR-6 **CC-CR-6 — Local conservativity witness remains satisfied.** @status:spec/done
   The reviewed case does not silently widen modality, remove caveats, raise reliability assessment, add an F.9 Bridge or bounded-use suitability claim, establish current reliance or authorization, claim that receiving use occurred, or collapse declared alternatives beyond stated loss notes.
7. @fact:CC-CR-7 **CC-CR-7 — A missing condition, preservation defect, or changed claim is explicit on failure.** @status:spec/done
   If the case fails a check, name the missing source or condition, the repairable preservation defect, or the actual changed claim. Repair and recheck within CR when the intended restatement can be restored. For an actual different claim or use, name the pattern to use next (`ExplanationFaithfulnessProfile`, `RepresentationSchemeTransition`, `A.6.4`, `B.5.2`, or another applicable pattern).
8. @fact:CC-CR-8 **CC-CR-8 — Working-model first remains intact.** @status:spec/done
   Ordinary same-entity rewrites stay lightweight; fuller explicit review records carry the fields needed for cases requiring fuller review.

## A.6.3.CR:9 - Consequences {#consequences}

- Textual same-entity rewrites get an admissible place without inventing a second pattern for the same move.
- Direct and correspondence-mediated variants stay visibly separated.
- Loss, provenance, and reliability transport become explicit instead of implicit editorial judgement.
- Ordinary working-model use stays lightweight, while cases needing fuller review get the additional record content their risk and use warrant.
- The pattern remains bounded by `A.6.3`, `A.6.4`, explanation-facing work, and representation-shift work.

## A.6.3.CR:12 - Relations {#relations}

- **Builds on:** `A.6.3`, `A.6.2`, `A.7`, `E.10.D2`, `E.17.0`, `E.17`, `F.9`, `F.18`, `E.10`
- **Coordinates with:** `ExplanationFaithfulnessProfile`, `RepresentationSchemeTransition`, `E.17.ID.CR ComparativeReviewUnit`, `A.6.4`, `B.5.2`, `A.15`
- **Failed conservativity:** name the missing source or condition, repair and recheck a preservation defect within CR when possible, or apply the pattern for the actual changed claim or use. Retargeting uses `A.6.4`, abductive work uses `B.5.2`, and action or work claims use the applicable `A.15` pattern; explanation, representation change, and other live claims keep their own routes.
- **Boundary notes:** explanation-facing cases apply `ExplanationFaithfulnessProfile`; representation-regime shifts apply `RepresentationSchemeTransition`; bounded comparative review cases apply `E.17.ID.CR ComparativeReviewUnit`; EntityOfConcern changes apply `A.6.4`.


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/A-6-3#root, spec://ai.lev/fpf-spec/contract/A-6-2#root, spec://ai.lev/fpf-spec/contract/A-7#root, spec://ai.lev/fpf-spec/contract/E-10-D2#root, spec://ai.lev/fpf-spec/contract/E-17-0#root, spec://ai.lev/fpf-spec/contract/E-17#root, spec://ai.lev/fpf-spec/contract/F-9#root, spec://ai.lev/fpf-spec/contract/F-18#root, spec://ai.lev/fpf-spec/contract/E-10#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/A-6-3-CSC#root, spec://ai.lev/fpf-spec/contract/A-6-3-RT#root, spec://ai.lev/fpf-spec/contract/E-17-EFP#root, spec://ai.lev/fpf-spec/contract/E-17-ID-CR#root, spec://ai.lev/fpf-spec/contract/A-6-4#root, spec://ai.lev/fpf-spec/contract/B-5-2#root, spec://ai.lev/fpf-spec/contract/A-15#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-6-3#root, spec://ai.lev/fpf-spec/contract/A-6-3-CSC#root, spec://ai.lev/fpf-spec/contract/A-6-3-NAR#root, spec://ai.lev/fpf-spec/contract/A-6-3-RT#root, spec://ai.lev/fpf-spec/contract/E-17-EFP#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/A-6-3-CR
