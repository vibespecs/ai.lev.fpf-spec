# E.17.EFP - ExplanationFaithfulnessProfile — explanation-use discipline over existing MVPK faces {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Architectural (A)
> **Status:** Stable
> **Normativity:** Normative unless marked informative

**One-line summary.** `ExplanationFaithfulnessProfile` classifies the bounded explanation use of a publication form or representation of one exact claim-bearing episteme. It does not decide which episteme the text expresses and cannot turn changed claims into another form of the source.

**Explanation-facing text in plain terms.** One published text on an existing MVPK face. It may express only the part of an exact source edition needed for a declared explanation use. Identify that edition by its ClaimGraph, exact EntityOfConcern and effective ReferenceScheme; then test whether the form expresses enough for that use. Omitting other source content neither claims whole-source coverage nor by itself constitutes another episteme. A changed assertion, concern or effective scheme needs its own identity decision.

**Ontic first screen.** Before assigning an explanation class, identify the source and the intended reader use.

1. Recover the exact source edition's ClaimGraph, EntityOfConcern and effective ReferenceScheme under C.2.1. Equal displayed words alone do not establish this identity.
2. Test whether the text expresses enough of that edition for the declared use under E.24.PUB §4.2. Preserve every qualification that changes the answer for that use, keep the source return, and disclose use-relevant omissions. A partial expression may qualify; a missing required condition leaves source sufficiency unresolved or fails it, even when each displayed sentence is individually true. Omission alone does not create a target episteme. Apply A.6.3.RT as well when a representation-change claim is current.
3. If the text asserts changed content or concerns another entity or effective scheme, identify the exact target under C.2.1 and the source-to-target relation actually claimed under A.6.3.CR, A.6.3.CSC, A.6.4 or another applicable pattern. Establish that relation independently before EFP classifies the target form; the class creates neither participant nor relation.
4. A new causal or counterfactual proposition belongs to a separate hypothesis episteme under B.5.2, or stays outside EFP. Blocking reliance on it does not make it a rendering of the source.

**Explanation-use relation in plain terms.** State which exact episteme the published text expresses, how that episteme relates to the named source when it is a different target, which explanation-use class applies, and what downstream claim or effect still stays outside the profile. Name the exact E.24.PUB publication occurrence, pins, traces, or provenance only when they are material to the present use.

**Use this when.** Use EFP when a real source-pinned, reconstructive, didactic, or speculative ambiguity changes how a published explanation form may be reviewed or used—especially for generated, retrieval-facing, model-facing, derivative, or interactive explanation. Authorship alone does not trigger the profile.

**Start here when.** Identify the source edition through claim content, concern and effective scheme. Then test whether the text preserves enough for the declared explanation use, or asserts a separately identified target. Choose the explanation-use class only after source sufficiency and any required target relation are established.

**What goes wrong if missed.** A publication form, a rewritten episteme, and a new hypothesis are all called a rendering of one source. Helpful wording then hides a changed claim-bearing object or an unsupported source relation.

**What this buys.** One honest identity branch followed by one bounded explanation-use class: the reader can tell which episteme is being published, how a changed target was obtained, and which stronger use remains blocked.

**Not this pattern when.** For an ordinary human-authored note, if a source locator plus one natural-language bounded/blocked-use sentence already preserves meaning and prevents the credible overread, use that simpler publication note and stop. Also do not use EFP to establish rewrite, representation change, coarsening, comparison, retargeting, hypothesis production, evidence, work, assurance, or gate claims; apply their exact patterns first.

**First output.** One compact explanation-use note naming the exact source or related target episteme, explanation class, source reference, bounded explanation-reader use, blocked downstream use, and reopen or boundary condition. The note names a source-to-target relation when the text expresses a separately identified target, including a changed concern or effective scheme. MVPK face, pins, provenance, and other source fields are inherited by reference unless ambiguity or a load-bearing use makes them relevant.

**Ordinary-output claim inventory.** After `ExplanationFaithfulnessProfile`, the author has claimed only that a publication form or representation of this already identified episteme has this explanation class and bounded use. EFP has not constituted an episteme, made a source-to-target relation obtain, or established model truth, evidence, assurance, safe reliance, gate passage, work occurrence, release reliance, or source replacement.

**Working explanation move.** Perform the ontic first screen, identify the exact episteme expressed by the text and any already obtaining source-to-target relation, then classify the publication form's explanation use and state its bounded reader use. If identity, sufficiency for the declared use or a required relation cannot be established, do not repair that gap with an explanation class; return to C.2.1 and the exact rewrite, coarsening, representation, hypothesis, comparison, evidence, work, assurance, or gate pattern.
**Lower-burden ordinary branch.** First try a source locator plus one sentence naming the allowed reader help and blocked stronger use. If that resolves an ordinary human-authored case, do not instantiate EFP. When class ambiguity still changes the next action, use the compact EFP result and no fuller field block.

**Load-bearing use.** Open the fuller explanation review only when the rendering will guide work or reliance, be externally relied on, be disputed, cross context, affect person or team status, or be cited as evidence, approval, engineering justification, gate, or release reliance.

**Stop condition.** Stop before EFP when the simpler source-linked boundary sentence performs the task. After EFP is triggered, stop when the class, bounded/blocked use, and reopen condition settle the next action; add no field or check that does not change it.

**Bounded explanation-use examples.**

| Bounded explanation use | Source-finding check with no downstream claim or effect | Blocked explanation use |
| --- | --- | --- |
| A `SourcePinnedExplanation` or `SourceLinkedExplanationReconstruction` helps navigation, bounded restatement, or source inspection with pins and trace visible. | A didactic explanation helps onboarding or source-finding, while any operative claim returns to the exact source or target episteme and its obtaining source-to-target relation; an `A.10` evidence path opens only when the receiving use actually needs evidence. | A fluent explanation is used as assurance, evidence, approval, gate passage, release permission, or work-occurrence evidence. |

**Neighboring patterns and project records.** `E.17.ID.CR` supplies the bounded-comparison discipline for a comparative review unit; `A.6.3.CR` and `A.6.3.RT` define same-entity rewrite and representation change; `A.6.3.CSC` defines the narrower-use result, blocked downstream use, and source-bearing reopen needed after deliberate coarsening; `A.6.4` and `OntologicalReframing` address a changed EntityOfConcern; `A.15` governs System-Role–Method–Work alignment; `A.15.1` independently admits dated Work; `A.15.4` repairs an appearance-based work or reliance use only while its prerequisite remains unclear; `B.3` supplies assurance and engineering-justification tests; `A.20` tests a named internal constraint for a stated case under that pattern's subject and applicability conditions; and `A.21` governs a named gate decision under its applicable profile. For permission-looking or policy-bearing prose, use `A.2.8.PER` for strong grants, exercises, weak non-prohibition/non-violation findings, and permission conflicts; use `A.2.8` for obligation, recommendation-as-duty, and prohibition commitments; and use `A.2.9` for the communicative Work that institutes or revokes an effect.

**Common wrong escalations and boundary transfers.** Do not use this profile to hide new claims, bridge-comparison load, action-selection pressure, or gate-bearing guidance inside helpful prose. If the rendering is really a bounded comparison, apply `E.17.ID.CR`; if it is only same-entity rewriting or representation shift, apply `A.6.3.CR` or `A.6.3.RT`; if a deliberately coarsened rendering's narrower bounded claim or effect, blocked downstream use, and source-bearing reopen are the actual problem, apply `A.6.3.CSC`; if it is already making world, work or reliance, assurance, or gate-bearing claims, leave `E.17.EFP` for the more exact downstream FPF pattern or project-side record.

**Generated-explanation repaired case.** Identify the exact source by its claims, concern and effective scheme, then test the generated text for the declared use. A sufficient partial expression may remain a form of that source; missing use-relevant content requires source return or repair, not automatic target creation. Changed assertions require an exact target and an independently obtaining source-to-target relation. An identity, sufficiency or relation gap leaves classification for that use open. After identity and bounded sufficiency are settled, use beyond reader help additionally requires an `A.10` path for each operative claim and, for any assurance, gate, work, permission, approval, or release claim, its applicable pattern and exact project record when one is required; missing evidence keeps the classified form at reader help or source-finding.

**Common wrong first interpretation.** A fluent, confident, source-linked, or reliable-looking explanation is treated as evidence. First honest entry: identify the exact episteme expressed by the text and any required source-to-target relation, then classify its publication form for reader help or source-finding; only an operative claim with an A.10 evidence path or another source relation that carries, supports, or exposes the source basis for the operative claim can carry downstream reliance.

Negative result: if a generated explanation says "reliable" but no operative claim maps to a source relation, the E.17.EFP result is source-finding only or reader help only. If an attempted downstream reliance is still raised, the receiving `A.10`, `B.3`, `A.21`, or other relation named by value can return evidence-needed or no-bounded-current-use for that attempted reliance. It is not weak evidence by style, confidence, fluency, or citation-like wording.

**Generated-retelling survival.** Compression or omission may preserve a source edition's inspectable reader-help use, source-finding cue and quoted pins when the partial form remains sufficient under the ontic first screen. State the limited use and material omissions. If the text strengthens or otherwise changes an assertion, or changes the concern or effective scheme, identify the target and establish its claimed source-to-target relation before classifying the target form. Fluency and links establish neither identity nor sufficiency, evidence, assurance, permission, gate passage or work authority.

**Derivative text and adaptation source-link rule.** A fork, adaptation, abridged guide, translation, generated explanation, tutorial or access-format conversion first undergoes the same identity-and-bounded-sufficiency test. A sufficient partial expression may remain a source form. Insufficient expression returns the exact missing source content or condition; a changed claim-bearing target requires its own identity and an obtaining direct relation. EFP then qualifies explanation use only if needed. If the result will guide work or reliance, `A.10` maps each operative claim to its exact source basis; a missing map permits only reader help, a source-gap note, or prospective evidence work.

**Published-form and episteme identity over revision and regeneration.** Reidentify the source or target through ClaimGraph, exact EntityOfConcern and effective ReferenceScheme, then retest expression sufficiency for the declared use. A different selection of source content may remain another sufficient form of the same edition; equal words about another concern or under another effective scheme do not establish the same episteme. A changed target requires its direct source-to-target relation. Face, prompt, template, carrier or title alone settles none of these questions. When use beyond ordinary reader help depends on how the text was produced, identify the exact generation or production relation and the source references it actually used; neither relation changes episteme identity by itself. EFP records only the bounded explanation use of the resulting published form.

**Pattern basis.** E.17 supplies face discipline; E.17.0 supplies viewpoint/view conformance only when `U.View` membership is material.
**Builds on.** `E.17.0 U.MultiViewDescribing`; `E.17` MVPK; `A.7`; `E.10.D2`; `A.6.B`; `F.9`; `F.18`.
**Coordinates with.** `ConservativeRetextualization`; `RepresentationSchemeTransition`; `E.17.ID.CR ComparativeReviewUnit`; `A.6.4`; `A.10`; `A.15`; `A.15.4`; `B.3`; `A.20`; `A.21`; `A.2.8`; `A.2.8.PER`; `A.2.9`.

## E.17.EFP:1 - Problem frame {#problem-frame}

The exact source ClaimGraph may need more than one publication form or representation. Explanation work may also produce a different target ClaimGraph, but that target is another episteme and must not be hidden inside the word `rendering`. Recurrent cases include:

- a manager-readable form of the same technical ClaimGraph;
- connective explanation that remains entailed by the source, or else belongs to an exactly related target episteme;
- didactic use of a sufficient source form, including a partial expression, or of a separately identified target with an obtaining rewrite or coarsening relation;
- exploratory use of a publication form of a separately constituted hypothesis episteme.
FPF already has C.2.1 for episteme identity, A.6.3 and neighboring patterns for source-to-target relations, `E.17.0` for viewpoints and views, `E.17` for publication faces, and E.24.PUB for publication occurrence, form, and carrier. EFP supplies only the remaining bounded explanation-use classification of one form of the already identified source or target episteme.

## E.17.EFP:2 - Problem {#problem}

Without a dedicated profile:
1. a form of the source, a rewritten target episteme, and a new hypothesis blur together;
2. explanation prose starts behaving like a second semantic rule track;
3. publication-side reviewers cannot tell which faces remain bounded-use for a given explanation class;
4. source and evidence details are either demanded for every explanation or omitted when a named claim, dispute, derivative, or reliance actually needs them;
5. an EFP class quietly substitutes for C.2.1 identity, an obtaining source-to-target relation, bridge work, or a gate decision.

## E.17.EFP:3 - Forces {#forces}

- **Clarity vs semantic restraint.** Explanation can help readers, but it does not mint new semantic commitments on publication faces.
- **Face discipline vs reader fit.** The same episteme can need different forms, while changed claims identify another episteme even when reader fit motivated the change.
- **Traceability vs accessibility.** Simpler renderings are useful only if readers can still recover how they relate to the source.
- **Didactic usefulness vs policy misuse.** A didactic or speculative retelling can help humans, but it does not masquerade as assurance or gate-bearing content.
- **Explanation vs interpretation.** Some moves still belong to explanation rendering; other uses require interpretation, retargeting, or the FPF rule or project record that actually defines the world-side or gate claim.

## E.17.EFP:4 - Solution — review profile for explanation renderings on existing MVPK faces {#solution-review-profile-for-explanation-renderings-on-existing}

### E.17.EFP:4.1 - Informal definition {#informal-definition}

> `ExplanationFaithfulnessProfile` is a review profile for the explanation use of publication forms or representations of exact claim-bearing epistemes on existing MVPK faces. E.17 supplies face discipline; E.17.0 supplies viewpoint/view conformance only when `U.View` membership is material.
>
> It does not create a new face family, episteme, or source relation. C.2.1 first identifies the exact episteme expressed by the text; E.24.PUB or A.6.3.RT identifies its form or representation; and, when the ClaimGraph changes, the applicable source-to-target pattern defines the relation and its obtaining test. EFP then states the bounded explanation use of that already identified object.

### E.17.EFP:4.1.a - Profile, episteme, and published-form distinction {#profile-episteme-and-published-form-distinction}

`ExplanationFaithfulnessProfile` is a **review profile**. Its cases concern passive publication forms or representations of an exact `U.Episteme`.

The distinction is executable: identify the episteme through its claim content, exact concern and effective scheme; test the form's sufficiency for the declared use; then classify that explanation use. Partial expression can preserve the source identity. Missing needed content blocks that use, while an actual changed target needs a C.2.1 identity and an independently obtaining source-to-target relation. An EFP class supplies none of these prerequisites.

### E.17.EFP:4.1.b - How to read this profile {#how-to-read-this-profile}

This profile does not decide whether a claim is true or which claim-bearing object exists. It starts after C.2.1 identity and any required source-to-target relation are recoverable, then qualifies the explanation use of one publication form or representation.

- `Faithfulness` names the review question for that explanation use, not a pass verdict or an episteme-identity rule.
- Class names are bounded-use labels for a form or representation, not merit labels and not source-to-target relations.
- Use E.17 for face discipline and E.24.PUB for publication occurrence and form.
- A changed assertion, concern or effective scheme reopens episteme identity even when the prose remains explanatory, didactic, reconstructive or speculative. Selecting only enough source content for a bounded use does not itself assert a changed ClaimGraph.
- A causal or counterfactual addition requires a separate hypothesis episteme under B.5.2 before any publication form can receive an EFP use label.

### E.17.EFP:4.1.c - Local working vocabulary {#local-working-vocabulary}

This profile uses a small local vocabulary for review.

- **Source episteme and publication occurrence** = the exact source `U.Episteme` edition and, when material, the exact E.24.PUB `EpistemePublicationRelation` occurrence through which it is available. Neither is an MVPK face, form, carrier, or arbitrary physical item.
- **Current claim-bearing episteme** = the exact source or target edition identified by ClaimGraph, EntityOfConcern and effective ReferenceScheme. The published form may express a sufficient part of that edition for the declared use. A target's claimed source-to-target relation must obtain under its direct pattern.
- **Published explanation form** = one publication form or representation of that current claim-bearing episteme on one existing face.
- **Class assignment** = the explanation-use class assigned to that published form on that face.
- **Bundle-local class difference** = a case where two forms in one bundle carry different bounded explanation uses.

These are review aids, not new kinds or relation types. EFP neither creates the current episteme nor substitutes for C.2.1, E.24.PUB, A.6.3, B.5.2, or another direct source-to-target pattern.

### E.17.EFP:4.2 - Core profile fields {#core-profile-fields}

The ontic first screen is performed once, not copied into a metadata record for every note. Most published forms whose identity branch is already recoverable need only the compact explanation-use note:

| Core field | Question |
| --- | --- |
| `explanationClass` | Which local profile value is assigned to this one rendering? |
| source reference | Which exact source or related target edition, identified by claims, concern and effective scheme, does the text express sufficiently for this use? Which locator reopens that decision and any material omissions? Which E.24.PUB occurrence matters only when availability is load-bearing? |
| bounded explanation-reader use | What can the explanation reader do with this explanation now: understand, navigate, inspect, teach, or prepare review? |
| blocked downstream use | What wider claim or effect is not carried by the explanation? |
| reopen or boundary condition | What source change, dispute, use escalation, missing source relation, or neighboring-pattern boundary condition ends this profile use? |

The fuller field vocabulary below opens only when ambiguity or load-bearing use is present: different classes across faces, source linkage dispute, connective reconstruction, reader-fit dispute, interaction or statefulness, derivative rendering, cross-context reuse, cited reliance, work or reliance, evidence, gate, engineering justification, bridge, or coarsening boundary.

- `faceRuleRef = E.17` and `viewpointConformanceRuleRef = E.17.0`;
- `sourcePublicationOrRecordForm`;
- `targetPublicationOrRecordForm`;
- `changeTargetRef`;
- `entityOfConcernPolicy = preserve` for explanation renderings over the same underlying source `U.Episteme` edition;
- `boundedContextPolicy`;
- `viewpointPolicy`;
- `referenceSchemePolicy`;
- `representationSchemePolicy`;
- `groundingPolicy`;
- `referencePlanePolicy`;
- `claimPolicy`;
- `claimScopePolicy`;
- `publicationScopePolicy`;
- `reliabilityTransportPolicy`;
- `pinningPolicy`;
- `provenancePolicy`;
- `lossProfile`;
- `claimContinuityClass`;
- `microtheoryContinuityClass`;
- `onticContinuityClass`;
- `bridgeRequirement`;
- `worldContactPolicy`;
- `evidencePolicy`;
- `gatePolicy`;
- `workCrossing`;
- `sourceRelationRuleRef?`, `upstreamAuthoritySourceRef?`, `downstreamUseRuleRef?`, and `downstreamAuthoritySourceRef?`;
- `boundedFaces`;
- `publication-face kind value` when `publication face/form` or `interop publication form` discipline is present;
- `publicNamePolicy`;
- `explanationSourceRelationClass` using the shared `E.17:5.1b` vocabulary when source pointer, source availability or retrieval, source use, source faithfulness, claim-source relation, contradiction, omission, claim widening, added linkage, independent verification, bounded use, forbidden downstream use, or reopen trigger could diverge;
- no generic source-relation field; source relation is recorded through `explanationSourceRelationClass`;
- `augmentationRelation`;
- `addedLinkPolicy` when a non-obvious `SourceLinkedExplanationReconstruction` connective points to an actual derivation from the source claims or to an exact relation occurrence that those source claims already report and whose obtaining is independently established;
- `targetUserModel?` when reader-fit materially shapes the rendering;
- `interactionMode?` when the explanation is more than one static explanatory paragraph;
- `contrastiveQuestion?` when the rendering is answering a specific user-facing contrast or why-question;
- `boundedReaderUse?` when downstream use is bounded by intended reader and task;
- `overreadRisk?` when overinterpretation pressure is part of the review load;
- `evidenceRelation?` only when a named operative claim or receiving reliance actually consumes an A.10 evidence/provenance path;
- `noNewBoundaryClaims = true` on explanation faces;
- `compositionRule`;
- `reopenCondition`.

These fields inherit the `E.17:5.1e` local-field rule. They classify one explanation-facing rendering for review; they do not create `U.Kind`, `publication-face kind`, `RelationKind`, `KindBridge`, `EvidenceKind`, `GateDecision`, `SpeechAct`, `Commitment`, `U.Work`, authority reference, publication face, or project-side FPF kind and reference named by value unless another FPF pattern explicitly defines or instantiates that object. The `explanationClass` value is a local source-relation and bounded-use profile value, not `ExplanationKind`, not `U.Kind`, not `EvidenceKind`, not `FaceKind`, and not a truth certificate.

When claim content changes, pause EFP until the practitioner uses C.2.1 to identify the target episteme and the applicable source-to-target pattern to identify and test the relation. EFP may then qualify a publication form of that target only when explanation use remains a distinct question; it never substitutes for that relation or its obtaining test.

### E.17.EFP:4.2.a - Working-model first {#working-model-first}

Ordinary published forms do not restate every field or replay the ontic decision. When their exact claim-bearing episteme, MVPK face, any material E.24.PUB occurrence, and already published source references make the branch recoverable, the compact note inherits those conditions by reference.

A source-bearing review record becomes necessary when:
- explanation class differs across faces in the same publication bundle;
- the rendering relies on bounded connective prose that is not obvious from the source wording alone;
- didactic or speculative wording creates a real risk of policy, assurance, or gate misuse;
- source linkage, provenance, or reliability transport would otherwise become unclear;
- the rendering is a fork, adaptation, translation, generated explanation, tutorial, access-format conversion, or another derivative publication that can be mistaken for the source publication, source relation, or source episteme itself.

When one rendering needs its own narrower bounded claim or effect line, blocked downstream claim or effect line, or source-bearing reopen rule because distinctions were deliberately coarsened for reader fit, the issue is no longer only explanation class. Do not keep that case here as if it were merely one more helpful rendering style; apply `A.6.3.CSC Controlled Semantic Coarsening`.

### E.17.EFP:4.2.b - What a publication-side reviewer checks first {#what-a-publication-side-reviewer-checks-first}

A publication-side reviewer starts with five questions:

1. Which exact source edition is intended: what ClaimGraph, EntityOfConcern and effective ReferenceScheme identify it?
2. Does the text express enough for the declared use, retaining action-changing qualifications, source return and use-relevant omission disclosure? Whole-source coverage is not required; an omitted answer-changing condition blocks this use even if the displayed sentences are true.
3. Does the text assert changed content or concern another entity or effective scheme? If so, which exact target and independently obtaining source-to-target relation support its form?
4. Which E.24.PUB form or applicable A.6.3.RT representation expresses the identified episteme, and which explanation class changes the reader's next action?
5. Has the form begun carrying another unsupported claim, relation, reliance or deliberately coarsened use that must return to its direct pattern?

If a prerequisite is missing, return the exact source-identity, source-sufficiency, target-identity or relation gap. Do not manufacture a target from an omission or repair a gap with a class. Once these prerequisites and the action-changing class distinction are recoverable, the compact note is complete. Open a fuller face-by-face record only when a section 4.2 trigger consumes additional fields.

### E.17.EFP:4.2.c - Interpretant-side block {#interpretant-side-block}

This profile classifies explanation use on existing faces; it does not describe full interactive explanation systems.

When reader fit materially changes the explanation class, bounded use, blocked use, or reopen condition, make only the distinction needed for that change. A familiar audience and static note may need no separate reader-model field. A contrastive or interactive case may need one or more of `targetUserModel`, `interactionMode`, `contrastiveQuestion`, `boundedReaderUse`, or `overreadRisk`.

These names are optional prompts, not a five-field publication block. They only expose the reader-fit difference that changes the present use.

When the bounded use depends on how much selected structure the reader can recover, use `C.2.8` with the relevant preparation, access and budget. Compare recovered structure separately from explanation faithfulness. Keep the exact episteme identified by the first screen: a content change requires its own target, even if the revised explanation is easier to use. The ordinary source-linked note remains sufficient whenever it meets EFP's non-use condition.

### E.17.EFP:4.3 - Explanation class set {#explanation-class-set}

The explanation-class set used in this profile is:

- `SourcePinnedExplanation`
- `SourceLinkedExplanationReconstruction`
- `DidacticRetelling`
- `SpeculativeRetelling`

In field form, the local assignment is `explanationClass = SourcePinnedExplanation | SourceLinkedExplanationReconstruction | DidacticRetelling | SpeculativeRetelling`.

Class assignment follows, and never replaces, the ontic first screen.

- `SourcePinnedExplanation` qualifies a form or representation that expresses enough of the exact source edition for the declared use, with action-changing qualifications, source return and use-relevant omissions recoverable. It claims no whole-source coverage.
- `SourceLinkedExplanationReconstruction` qualifies a non-obvious connective only when it remains in the same source ClaimGraph because a stated derivation from exact source claims recovers it, or because the source ClaimGraph already reports an exact relation occurrence whose obtaining is independently established under its defining pattern. An independently true relation that the source does not claim belongs to another target ClaimGraph.
- `DidacticRetelling` qualifies teaching or onboarding use of a sufficient source form, including a partial expression, or of an exact target connected under `A.6.3.CR`, `A.6.3.CSC` or another applicable pattern when pedagogy changes claims, concern or effective scheme.
- `SpeculativeRetelling` qualifies only the bounded exploratory use of a form of a separately constituted hypothesis episteme, normally produced under `B.5.2`. It is not a speculative form of the original source ClaimGraph.

These values are not `U.Kind` values, MVPK faces, semantic merit grades, source-to-target relations, or episteme identities. They state how the published form may be used after those objects and relations have been recovered.

Class assignment is per published form on a face, not one blanket label for a whole multi-face bundle. If a `PlainView` form stays source-pinned while a `TechCard` form expresses a separately related target episteme, the bundle names both exact epistemes and the class difference.

### E.17.EFP:4.3.a - Ordinary class-selection guidance {#ordinary-class-selection-guidance}

A practical order is:

1. identify the source's ClaimGraph, exact concern and effective scheme;
2. test sufficiency of the text for the declared use, including qualifications and omissions;
3. identify any actual changed target and independently obtaining source-to-target relation;
4. identify the form or representation and assign an EFP class only if that explanation-use distinction changes the reader's next action.

Use `SourcePinnedExplanation` for sufficient source expression; `SourceLinkedExplanationReconstruction` for an already justified connective explanation; `DidacticRetelling` for bounded teaching use of the identified source or target; and `SpeculativeRetelling` only for a separately constituted hypothesis episteme. A missing prerequisite returns its exact gap. Any narrower reader-help use must itself satisfy the source-expression test.

Do not keep one narrower-use target with declared source-loss mode inside explanation merely because the prose is reader-friendly. When its narrower bounded claim or effect, blocked downstream use, and source-bearing return are primary, use `A.6.3.CSC Controlled Semantic Coarsening`; EFP may qualify a later publication form only if explanation use remains a separate live question.

### E.17.EFP:4.3.b - Entailed connective and `addedLinkPolicy` {#entailed-connective-and-addedlinkpolicy}

Harmless connective wording adds no proposition: conjunction markers, pronoun recovery, and sentence order can simply make an already explicit source statement readable. No `addedLinkPolicy` is needed for that case.

`SourceLinkedExplanationReconstruction` applies to a less obvious connective only when one of two bases is recoverable:

1. the exact source claims plus their effective reference scheme make the connective a consequence under a stated derivation; or
2. the exact source claims already report the relation occurrence, and that occurrence independently obtains under its defining pattern.

When that basis is material but not visible in the prose, a compact `addedLinkPolicy` points to it:

- `addedLinkKind` — the connective being exposed;
- `sourceReferenceSet` — the exact source claims used;
- `effectiveSchemeOrRuleRefs` — the designation, interpretation, ordering, or inference rules used by the derivation;
- `derivationOrRelationRef` — the inspectable derivation or the exact relation occurrence already reported by the source claims and independently shown to obtain;
- `claimContentResult = source-recoverable` — confirmation that the connective introduces no unsupported target claim;
- `reopenTrigger` — a source, scheme, rule, context, or relation change that invalidates the basis.

The policy is an index to the basis, not evidence that the basis exists. `boundednessReason`, a forbidden-link note, or author intent may help delimit use, but none substitutes for `derivationOrRelationRef`.

If neither a derivation from the exact source claims nor an exact source-reported relation occurrence that independently obtains can be recovered, the connective is another claim. Constitute its exact target episteme under C.2.1 and apply the direct relation, bridge, comparison, or B.5.2 hypothesis pattern that fits the new claim. If that result is unavailable, remove the connective or leave EFP; a downgrade label cannot make it source-linked.

### E.17.EFP:4.4 - Working bounded-use matrix {#working-bounded-use-matrix}

| Class | Claim/source relation | Augmentation boundary | Usually bounded faces | Usually bounded publication-form use | Usually forbidden uses |
|---|---|---|---|---|---|
| `SourcePinnedExplanation` | sufficient expression of the exact source edition for the declared use; whole-source coverage is not claimed | no claim-level augmentation | `PlainView`, `TechCard` | source inspection, navigation, or bounded restatement | an assurance, gate, evidence, or work claim not separately established |
| `SourceLinkedExplanationReconstruction` | same source ClaimGraph with a connective recovered by a stated derivation from source claims, or by an exact relation occurrence already reported there and independently shown to obtain | no new relation by class label | `PlainView`, `TechCard` | bounded explanation while the exact derivation or source-reported relation remains recoverable | use for which the source, scheme, derivation, source relation claim, or obtaining basis is unavailable |
| `DidacticRetelling` | sufficient source form, or form of a separately identified target connected under A.6.3 or another applicable pattern | pedagogy does not hide target identity or relation | `PlainView` | didactic or onboarding use | policy, assurance, gate, or source-replacement use |
| `SpeculativeRetelling` | form of a separately constituted B.5.2 hypothesis episteme | causal or counterfactual claim belongs to the hypothesis ClaimGraph | `PlainView` | clearly marked exploratory use | evidence, assurance, gate, release, or policy use |

This matrix assigns no evidence relation. An ordinary EFP result needs no A.10 path. Exact evidence, trace, pin, or provenance details open only when a named claim, dispute, derivative transformation, or receiving reliance consumes them and its applicable pattern or project record requires them.

`ExplanationFaithfulnessProfile` ordinarily stays on `publication face/form`. Any appearance on `interop publication form` remains source-pinned and structure-preserving, and does not smuggle explanation-specific semantics into interop publication. Didactic or speculative restrictions are use-profile restrictions over existing faces, not new face kinds.

Source-pinned explanation on `AssuranceLane`-facing publication is exceptional rather than ordinary. Unless the exact face or source policy permits that use with visible evidence carriers, source pins, and no added semantics, reviewers treat `AssuranceLane`-facing explanation rendering as blocked.

`DidacticRetelling` may carry analogy, scaffolding, or reader orientation without asserting a domain fact. Every domain claim it does express belongs either to the exact source ClaimGraph or to an identified target episteme with an obtaining source-to-target relation. Marking prose non-canonical or trace-free does not erase claim content, create its episteme, or establish that relation. When such analogy or scaffolding sits beside technical content, box or otherwise visibly separate it so readers do not merge it into the technical source; that cue limits likely use but does not establish episteme identity or a source relation.

The compact ordinary result needs only a source locator sufficient to reopen the exact source or target decision. Publish exact claim IDs, pins, trace paths, provenance details, or an A.10 evidence relation only when a named claim, dispute, derivative transformation, or receiving reliance consumes them. A reopenable locator is not automatically an evidence path.

When a reader-fit difference changes the bounded or blocked use, state only the relevant audience, interaction, question, use, or overread distinction. Do not publish or inherit all five reader-model fields for ordinary reader help.

### E.17.EFP:4.5 - Shared explanation rule set {#shared-explanation-rule-set}

#### E.17.EFP:4.5.a. Preservation rule {#e-17-efp-4-5-a-preservation-rule}
Every published explanation form under this profile expresses enough of one exact episteme edition for the declared use. Source identity rests on ClaimGraph, exact EntityOfConcern and effective ReferenceScheme; sufficiency rests on retained action-changing qualifications, source return and disclosure of use-relevant omissions. A partial expression may satisfy both. Insufficiency does not constitute a target; actual changed content, concern or effective scheme requires its own identity decision and any claimed source-to-target relation. E.24.PUB publication occurrence remains separate, and the EFP class changes neither identity nor relation.

#### E.17.EFP:4.5.b. Loss and reliability rule {#e-17-efp-4-5-b-loss-and-reliability-rule}
A published form states material omission, reordering, simplification or connection. An omission that removes information required by the declared use blocks that use even when the remaining text is true. When the form instead asserts changed content, identify its exact target and establish the claimed source-to-target relation under A.6.3 or another applicable pattern. An EFP label supplies neither missing content nor that relation. Reliability is never silently widened by more persuasive prose.

When a concrete reader-fit difference is load-bearing, expose only enough of its bounded use or overread risk to prevent the actual didactic or contrastive form from being mistaken for assurance, policy, or gate guidance.

#### E.17.EFP:4.5.c. Downstream-use and boundary rule {#e-17-efp-4-5-c-downstream-use-and-boundary-rule}
This profile stays explanation-facing and episteme-facing. It does not decide bridge stance, retargeting, action selection, executable docking, gate-bearing claims or effects, assurance, engineering justification, or work enactment. If a case starts carrying one bounded comparative review case, rival interpretations, bridge-mediated comparison load, world consequences, work or reliance consequences, gate consequences, assurance, or engineering justification, apply the neighboring FPF pattern, then name the project-side object or record that carries the claim or effect and its FPF kind. Relevant patterns include `E.17.ID.CR`, `F.9` for an obtaining Bridge and its bounded-use claim, `F.9.1` for an optional stance note, `B.5.2`, `A.6.4`, `A.15`, `A.15.1`, `A.15.4` only while an appearance hides the needed work or reliance prerequisite, `B.3`, `A.20`, and `A.21`.

Interpretant-side fields do not weaken that boundary rule. They only bound reader use; they do not authorize unsupported downstream guidance.

If a coarsened explanation-like rendering needs a narrower bounded claim or effect, blocked downstream use, and source-bearing reopen to remain honest, apply `A.6.3.CSC Controlled Semantic Coarsening` rather than keeping the case in ordinary explanation-use discipline.

#### E.17.EFP:4.5.d. Composition and reopen rule {#e-17-efp-4-5-d-composition-and-reopen-rule}
Repeated `SourcePinnedExplanation` over forms of the same exact source edition can be idempotent for the same bounded use. A changed selection of content reopens sufficiency for that use; changed assertions, concern or effective scheme reopen C.2.1 identity and any source-to-target relation. Didactic target forms reopen when their target edition, relation or use changes; speculative forms reopen when their B.5.2 hypothesis edition, prompt relation or exploratory use changes.

### E.17.EFP:4.6 - Hard boundary rules {#hard-boundary-rules}

A rendering reviewed under this profile keeps the following explicit:
- it does **not** create a second face family;
- it does **not** turn faces into a second semantic rule track;
- it does **not** license new A.6.B boundary claims on explanation faces: law claims, use-boundary claims, deontic or commitment claims, and effect or evidence claims;
- it does **not** replace bridge discipline, retargeting discipline, or world or gate boundary discipline;
- it does **not** let `publication face/form` and `interop publication form` collapse into one undifferentiated explanation channel.

If explanation text carries a changed ClaimGraph, stop class review, identify the exact target episteme and establish that the direct source-to-target relation obtains. Resume EFP only for a publication form of that target when bounded explanation use remains separately material.

## E.17.EFP:7 - Conformance Checklist {#conformance-checklist}

These checks apply only after EFP's use condition survives the simpler-note comparison. Retain a check only if it changes the next bounded use, blocks a concrete overclaim, or preserves the source or reopen condition needed for that action.

Use core ordinary checks first. Conditional rows open only when reader-fit, bundle-local class difference, bounded explanation class, connective reconstruction, derivative rendering, or downstream reliance use is present.

### E.17.EFP:7.1 - EFP-Core ordinary checks {#efp-core-ordinary-checks}

0. @fact:CC-EF-0 **CC-EF-0 — Exact episteme and sufficient expression are recoverable.** @status:spec/done
   Identify the source through ClaimGraph, exact EntityOfConcern and effective ReferenceScheme. Its form expresses enough for the declared use, preserves answer-changing qualifications, returns to the source and discloses use-relevant omissions; whole-source coverage is not required. Insufficiency returns the exact gap, not an invented target. An actual changed target needs its own identity and an independently obtaining source-to-target relation; a speculative causal or counterfactual claim belongs to a separate B.5.2 hypothesis episteme.
1. @fact:CC-EF-1 **CC-EF-1 — Explanation class follows identity.** @status:spec/done
   The class is explicitly named for the publication form after CC-EF-0; it is not used as episteme identity or source-to-target evidence.
2. @fact:CC-EF-3 **CC-EF-3 — Source reference and blocked downstream use are explicit.** @status:spec/done
   The compact note states source reference, bounded explanation-reader use, blocked downstream use, and reopen or boundary condition.
4. @fact:CC-EF-5 **CC-EF-5 — No new A.6.B boundary claims on explanation faces.** @status:spec/done
   The no-new-boundary-claims rule is explicit on explanation faces; the blocked claims are law claims tested under A.6.B, use-boundary claims, deontic or commitment claims, and effect or evidence claims.
5. @fact:CC-EF-7 **CC-EF-7 — No second face family.** @status:spec/done
   A publication-side reviewer can tell why the case remains explanation-facing rather than becoming a second semantic rule track.

### E.17.EFP:7.2 - EFP-Conditional checks {#efp-conditional-checks}

1. @fact:CC-EF-4 **CC-EF-4 — Interpretant-side block is explicit when reader-fit does real work.** @status:spec/done
   Only the reader-fit distinctions that change the current class, bounded use, blocked use, or reopen condition are stated. The five optional prompts are not a required block.
2. @fact:CC-EF-2 **CC-EF-2 — Face and `publication-face kind` boundary is explicit when present.** @status:spec/done
   State face, pinning, provenance, or reliability details only when the present form choice, dispute, derivative, or receiving use makes that boundary material and it is not already recoverable by source reference.
3. @fact:CC-EF-6 **CC-EF-6 — Boundary to interpretation, retargeting, coarsening, and world or gate use is explicit.** @status:spec/done
   The boundary is explicit, including `A.6.3.CSC Controlled Semantic Coarsening` when a narrower bounded claim or effect, blocked downstream claim or effect, or source-bearing reopen condition becomes primary.
4. @fact:CC-EF-8 **CC-EF-8 — Bundle-local class differences are explicit.** @status:spec/done
   When one publication bundle carries different explanation classes across faces, that difference is stated explicitly rather than hidden under one bundle-wide label.
5. @fact:CC-EF-9 **CC-EF-9 — Source-loss or changed-claim cases retain exact identity and use boundaries.** @status:spec/done
   A didactic target names its exact A.6.3 or other relation; a speculative form names its exact B.5.2 hypothesis episteme. Any material source loss or reliability downgrade states its bounded and forbidden uses without pretending that the EFP class supplies identity or relation evidence.
6. @fact:CC-EF-10 **CC-EF-10 — Reopen triggers match the class.** @status:spec/done
   The published review note makes class-relevant reopen triggers visible when source claim set, pins, provenance, or face-use assumptions change.
7. @fact:CC-EF-11 **CC-EF-11 — Every non-obvious source-linked connective has an actual basis.** @status:spec/done
   The exact source claims and effective scheme yield a stated derivation, or those source claims already report an exact relation occurrence whose obtaining is independently established. `addedLinkPolicy` points to that basis; without it, the added claim becomes an exact target episteme under its direct pattern or exits EFP.
8. @fact:CC-EF-12 **CC-EF-12 — Derivative renderings keep source links operative.** @status:spec/done
   A fork, adaptation, translation, generated explanation, tutorial, access-format conversion, or other derivative rendering that will guide work or reliance maps each operative claim to the exact source passage, carrier path, or project record that evidences it and names that record's FPF kind when material, or else downgrades to reader help or applies `A.6.3.CSC` as appropriate.
9. @fact:CC-EF-13 **CC-EF-13 — Generated explanation reliance boundary is explicit.** @status:spec/done
   A generated explanation used beyond ordinary reader help states its explanation class, source-finding state, operative claims, the FPF pattern used to test each relied-on claim, the exact project record that carries it, and blocked downstream use. The explanation itself is not evidence, assurance, approval, gate passage, release reliance, or work authority.

## E.17.EFP:9 - Consequences {#consequences}

- Explanation classes become explicit and reviewable.
- Existing MVPK face discipline stays intact.
- The ordinary result stays compact; exact pins, provenance, trace, reader-model, and evidence details appear only for the concrete use that consumes them.
- The boundary to interpretation, retargeting, and world or gate work becomes easier to review.

## E.17.EFP:12 - Relations {#relations}

- **Uses when current:** `C.2.8` for the extractable structural amount consumed by a bounded explanation use; its comparison retains the identified episteme, expressing form and qualified observer, while EFP retains explanation-use classification.
- **Builds on:** `E.17.0`, `E.17`, `A.7`, `E.10.D2`, `A.6.B`, `F.9`, `F.18`
- **Coordinates with:** `ConservativeRetextualization`, `RepresentationSchemeTransition`, `A.6.3.CSC Controlled Semantic Coarsening`, `E.17.ID.CR ComparativeReviewUnit`, `A.6.4`, `A.15`, `A.15.4`, `B.3`, `A.20`, `A.21`
- **Profile basis and main neighboring-pattern boundaries:** E.17 supplies face discipline; E.17.0 supplies viewpoint/view conformance only when `U.View` membership is material. A shift toward new semantics, a coarsened narrower-use target, or a gate-bearing claim or effect leaves the profile.
- **Boundary notes:** bounded comparison over a comparative review unit applies `E.17.ID.CR ComparativeReviewUnit`; explanation-like renderings with declared source-loss mode whose narrower bounded claim or effect, blocked downstream claim or effect, and source-bearing reopen are primary apply `A.6.3.CSC Controlled Semantic Coarsening`; retargeting applies `A.6.4`; work and reliance consequences apply their direct patterns, including `A.15` for alignment, `A.15.1` for dated Work, and `A.15.4` only while an appearance hides the needed prerequisite; assurance and engineering-justification consequences apply `B.3`; gate-bearing consequences apply `A.21` under the named gate’s applicable profile; use `A.20` only for a named internal-constraint check under that pattern's subject and applicability conditions.


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/E-17-0#root, spec://ai.lev/fpf-spec/contract/E-17#root, spec://ai.lev/fpf-spec/contract/A-7#root, spec://ai.lev/fpf-spec/contract/E-10-D2#root, spec://ai.lev/fpf-spec/contract/A-6-B#root, spec://ai.lev/fpf-spec/contract/F-9#root, spec://ai.lev/fpf-spec/contract/F-18#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/A-6-3-CR#root, spec://ai.lev/fpf-spec/contract/A-6-3-RT#root, spec://ai.lev/fpf-spec/contract/A-6-3-CSC#root, spec://ai.lev/fpf-spec/contract/E-17-ID-CR#root, spec://ai.lev/fpf-spec/contract/A-6-4#root, spec://ai.lev/fpf-spec/contract/A-10#root, spec://ai.lev/fpf-spec/contract/A-15#root, spec://ai.lev/fpf-spec/contract/A-15-4#root, spec://ai.lev/fpf-spec/contract/B-3#root, spec://ai.lev/fpf-spec/contract/A-20#root, spec://ai.lev/fpf-spec/contract/A-21#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-15-4#root, spec://ai.lev/fpf-spec/contract/A-6-3-CR#root, spec://ai.lev/fpf-spec/contract/A-6-3-CSC#root, spec://ai.lev/fpf-spec/contract/A-6-3-NAR#root, spec://ai.lev/fpf-spec/contract/A-6-3-RT#root, spec://ai.lev/fpf-spec/contract/C-2-8#root, spec://ai.lev/fpf-spec/contract/C-2-P#root, spec://ai.lev/fpf-spec/contract/C-29#root, spec://ai.lev/fpf-spec/contract/E-17#root, spec://ai.lev/fpf-spec/contract/E-17-AUD#root, spec://ai.lev/fpf-spec/contract/E-17-AUD-LHR#root, spec://ai.lev/fpf-spec/contract/E-17-AUD-OOTD#root, spec://ai.lev/fpf-spec/contract/E-17-ID-CR#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/E-17-EFP
