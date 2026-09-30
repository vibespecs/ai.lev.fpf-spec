# C.2.P - Clarify Episteme, Publication, and Source Wording (Epistemic Precision Restoration): depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## C.2.P:5 - Archetypal Grounding {#archetypal-grounding}

### C.2.P:5.0.1 - Cheap case: ordinary reader help {#cheap-case-ordinary-reader-help}

**Starting sentence:** “The note supports the reader.”

**Questions:** What does the note let the reader do? Does the sentence claim evidence, authority, gate passage, work permission, or assurance?

**Result:** It only helps navigation. Rewrite: “The note helps the reader find section 4.2.” The recovered function is ordinary reader help. No FPF kind, relation, compact row, or full check is needed. Stop after the sentence.

### C.2.P:5.0.2 - Mixed case: display and decision {#mixed-case-display-and-decision}

**Starting sentence:** “The dashboard approves launch.”

**Questions:** Is the dashboard the decision, or does it display one? Which exact project object carries the approval claim?

**Result when a decision exists:** “The dashboard shows `GateDecision GD-17` for release candidate R; the decision, not the display, records that the gate passed.” E.24.PUB separates publication form, carrier, and occurrence; use E.17 when publishing a reader-facing account of the accepted decision. A.21 supplies the gate-decision meaning. The reader may find and cite GD-17, but must use the direct release or permission rule for launch. Stop.

**Result when no decision resolves:** “The dashboard is only a cue; launch approval is unresolved.” Block approval-bearing use until the exact decision exists.

### C.2.P:5.1 - Boundary and Anti-Cases {#boundary-and-anti-cases}
| Boundary case | C.2.P result | Why this protects use |
| --- | --- | --- |
| Ordinary reader help | The sentence says a note helps a reader find another section, with no evidence, authority, use-boundary, work, gate, decision, or project reliance claim. Leave ordinary wording ordinary or make one local wording repair. | Keeps ordinary prose affordable; `support` as ordinary help is not forced into a record. |
| Relation-only support wording | The sentence says one claim, source description, grounding relation, evidence record, `B.3` `AssuranceResult`, engineering-justification result, causal-use relation, mathematical-lens relation, characteristic relation, declared-use boundary, work relation, or publication-companion use bears on another claim, and source-relation use or publication construction is already clear. Apply `A.6.P`; no C.2.P recovery is needed. | Prevents this pattern from absorbing relation precision restoration. |
| Known FPF kind named by value | The sentence already names the project-side FPF kind and reference, such as an evidence path, gate decision, decision record, Work occurrence, `B.3` `AssuranceResult`, or architecture pattern application. Apply the named pattern without an intermediate C.2.P step. | Avoids a needless logical hop and keeps the relevant neighboring-pattern application intact. |
| Source phrase without recovered FPF-governed use | Source wording is interesting but its FPF kind, relation, or use disposition cannot be recovered. Keep it as reduced-use cue or block its FPF use. | Preserves source meaning without guessing FPF meaning. |
| Replacement head is another umbrella | A proposed repair changes `support` to `basis`, `display` to `face`, or `route` to `path` while the kind and relation are still hidden. Mark repair incomplete. | Blocks lexical churn and forces the kind named by value, relation, and declared use boundary to be recovered. |
| Apparatus too heavy | A one-sentence local repair is replaced by a full record, checklist, and source note with no additional declared use boundary. Use the local sentence or compact row instead. | Keeps first-use cost and maintenance cost inside the quality claim. |

### C.2.P:5.2 - Transfer Coverage {#transfer-coverage}

`C.2.P` is intentionally narrow but must transfer across three recurrent publication situations:

- FPF-side drafting: pattern text, DRR text, source-relation notes, review-use notes, and pattern draft prose;
- project-side publication: dashboards, explanations, cards, documents, front-ends, rendered files, and generated summaries used around evidence, work, gates, decisions, assurance, or methods;
- external source-expression clarification: seminar fragments, papers, reviews, standards, and tool outputs being clarified before possible FPF use.

In all three situations the same invariant holds: before accepting the wording as current FPF text, recover the distinction between source wording and current FPF wording, claim-bearing episteme, publication construction, carrier-relation construction, relation-like slice, the applicable neighboring pattern for any non-C.2.P field, and remaining reader use.

## C.2.P:6 - Bias-Annotation {#bias-annotation}

| Lens | Risk | Mitigation |
| --- | --- | --- |
| Ontology | Precise-looking words become a new parallel ontology. | Require recovery to current FPF kinds and relations before reuse. |
| Usability | The rule becomes too heavy for ordinary edits. | Use the smallest sufficient rewrite mode. Reserve the full check for several interacting unresolved fields, contested source-to-FPF use, or a reusable ontological or naming decision. |
| Preservation | Source-relation or source-ref target text is mistaken for direct pattern authority. | Keep source-related statements separate from the ordinary pattern guidance. |
| Checklist ritual | The rule becomes a form to satisfy rather than a wording action to perform. | Put the action in `Solution`; use row evidence only when wording has FPF-governed use. |

## C.2.P:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Failure | Avoidance |
| --- | --- | --- |
| Token swap | Replace `display` with `face` or `host` with `file` without recovering kind and sentence function. | Apply head-kind and relation recovery before rewriting. |
| Group-kind list | Leave a list such as `pattern, record, relation, or action` as if the list names one kind. | Decide whether the sentence needs one kind, a relation record, a tuple-like record, alternative cases, or a blocked ontology. |
| Type-correct but inert rewrite | All overread is removed, all heads are typed, and no practical guidance remains: the reader can see that local checks passed but cannot tell why the distinction matters, what to do, or which FPF pattern application or project-side FPF kind carries the claim being made. | Recover the didactic or recognition function in wording whose claim being made is recovered through the named FPF pattern, keep any Plain line mapped to the recovered Tech interpretation when both registers are current, state the remaining reader use, or demote the phrase to reduced-use cue, blocked use, or rewrite incomplete instead of treating the repair as complete. |
| Expressive overread rebound | A repair restores practical guidance with a memorable Plain or didactic line, but that line carries a claim not recoverable from the Tech fields, named FPF kind, recovered relation, project-side reference, disposition, or pattern application. | Map the line to the recovered Tech interpretation under `E.10:6.2`; use the FPF pattern that defines, constrains, or tests the claim; or demote the phrase to reduced-use cue, blocked use, or rewrite incomplete. |
| Pillar-blind precision pass | A broad cleanup proves trigger removal and kind recovery, but never checks whether `E.2` `P-2`, `E.6`, `E.8`, or `E.12` still let the intended reader see the working situation, why it matters, and what first useful move remains. | For FPF-governed Problem frames, Problem sections, recognition texts, examples, and worked slices, state the remaining reader use or FPF pattern application. Preserve intentional didactic metaphors when they are ordinary recognition aids or when their claim being made maps back to Tech. If the didactic function was harmed, repair the Plain wording so it maps back to the recovered Tech interpretation, or mark the rewrite incomplete instead of accepting type-correct but inert wording. |
| Source-companion header leakage | Carry a source-companion header into a pattern and let `Authority: none` or `Current use` define the new pattern. | State the pattern-use claim and authority claim in the pattern header and relations. |
| Pattern as procedure | Say the pattern is called, routed, invoked, or chained as if it were executable code. | Say that a practitioner uses or applies the pattern in a problem situation. If actual project activity is claimed, name the relevant work occurrence, method, decision, or action invitation; add actor or `U.MethodDescription` identity only when it changes the claim or its later use. |
| Strength metaphor | Say a claim is strong or weak without a recoverable comparison basis, such as a characteristic, threshold, evidence class, scope, gate condition, or use-boundary relation. | Name that basis, or replace the metaphor with the recovered use-boundary claim when that is what the sentence means. |

## C.2.P:10 - Rationale {#rationale}
FPF already contains the relevant ontology. The recurring defect was not lack of concepts but ad hoc wording that bypassed them: `source`, `target`, `display`, `object`, `host`, `route`, `supported use`, and similar trigger terms packed several FPF kinds and relations into one convenient phrase; they are examples of wording to unpack, not current replacement vocabulary.

For FPF-governed wording, use `F.19` with the `E.10` cues, then use only the pattern whose field remains unresolved: `F.18` for a reusable name, `A.6.P` for relation precision, and `A.7`, `C.2.1`, `E.17.0`, `E.17`, MVPK, or `E.24.PUB` for the relevant EntityOfConcern, episteme, view, publication, or carrier distinction. C.2.P stops as soon as the direct pattern and field are known.

Because every normative FPF pattern must satisfy `E.2`, epistemic precision is not a value apart from `P-2 Didactic Primacy`. A stricter repair is incomplete if it turns reader-facing problem text into a kind inventory with no working situation or first useful move. The remedy is recognition wording whose claim remains recoverable through the Tech interpretation or a named FPF pattern application, with a declared-use boundary when that boundary matters.



## C.2.P:11 - SoTA-Echoing {#sota-echoing}

When rewriting episteme-publication-heavy conformant text, the practitioner must recover accepted FPF kinds and relations, so that episteme, publication, view, carrier, naming, relation, and project-side records are not replaced by ad hoc words.

A full external SoTA comparison is not needed for this bounded architectural precision-restoration pattern. A reduced external practice set is still required to check terminology drift and epistemic precision restoration. It sharpens only the recovery discipline, creates no new ontology, and does not outrank the FPF patterns named below.

In this section, `SoTA-Echoing` means compatibility with current FPF ontology and selected external practice anchors, not that those anchors are sufficient SoTA for every field. ISO terminology entries are standards anchors for designation practice; SHACL-style validation is only a fail-closed constraint analogy; word-sense and ambiguity-resolution practice is used only for context-sensitive sense recovery. If one of those domains becomes the object of a future claim, use its current SoTA pattern or source review.


| Reduced source idea | Adapted FPF invariant | Rejected shortcut | Recovery section |
| --- | --- | --- | --- |
| ISO 704:2022 and ISO 1087:2019 terminology work distinguishes the entity under discussion, the concept used in a terminology system, the definition, the designation, and term-formation practice. | Recover the FPF kind, relation, and sentence function before accepting a rewritten phrase. Use external terminology work only as external corroboration for careful designation and definition practice. | Do not replace FPF episteme and publication ontology with an ISO concept system, a dictionary substitution, or a global class row. | `C.2.P:4.1`, `C.2.P:4.4`, and `C.2.P:10` |
| SHACL-style constraint validation makes local constraints explicit and fail-closed when a data shape does not satisfy them. | Use only the fail-closed analogy: when the FPF kind, relation, or declared use boundary cannot be recovered, return a non-use result instead of accepting the wording. | Do not import SHACL ontology, machine-validation authority, or shape vocabulary as FPF pattern ontology. | `C.2.P:4.0a`, `C.2.P:4.2`, and `C.2.P:8` |
| Word-sense disambiguation and ambiguity-resolution practice treats sense recovery as context-sensitive rather than solved by the most common word sense. | When one local head or qualifier carries several plausible senses, recover the local FPF context and the applicable named FPF pattern before choosing wording. | Do not import machine-learning benchmarks or treat common usage as proof that the local FPF sense is recovered. | C.2.P:4.4, C.2.P:4.1.2, E.17.AUD.LHR, and F.18 |

**External-practice boundary.** External traditions enter only through the local FPF invariant named by value they sharpen. Object-oriented modeling and OWL-style ontology modeling do not become the default repair for vague FPF wording. Architecture-description standards help keep views, viewpoints, concerns, and descriptions explicit. Explainability and NLP faithfulness work helps prevent explanation laundering. RAG evaluation helps separate retrieval evidence, source availability, and answer trust. Quality-diversity and multi-objective search help avoid premature scalarization in candidate selection. None of these traditions becomes FPF ontology, FPF authority, or a universal pattern-quality benchmark.

### C.2.P:11.1 - Relevant FPF Patterns {#relevant-fpf-patterns}

The current FPF corpus already has patterns that contribute to this discipline:

- `E.10` supplies word/head, morphology, register, and naming cues and routes within the connected `F.19` reading.
- `E.10.D2` gives the "thing vs words vs rules" discipline and the carrier humility rule.
- `F.18` gives the local-first naming protocol: governed value and kind; the pattern and contribution that define or constrain them; by-value scheme; local-sense claim; intended use; candidate comparison; and any separately obtaining relation.
- `A.6.P` gives the relation-precision restoration method: restore generic head kind, build candidate sets for endpoint kinds and relation kinds, select kind-explicit slots and qualifiers, then allow guardrailed wording.
- `C.2.1` gives episteme identity through exact claim content, EntityOfConcern, and effective ReferenceScheme and keeps empirical grounding and edition continuity as distinct direct relations.
- `A.7` keeps EntityOfConcern, Description episteme, and publication carrier distinct.
- `E.17.0` tests view conformance to a viewpoint; `E.17` governs reader-facing publication forms for an accepted account; `E.24.PUB` distinguishes publication occurrence, form, and carrier.
- `A.15.4` shows how to keep an encountered publication, display, or low-articulation cue distinct from the project-side FPF kind and reference used for work or reliance.
- `A.16` coordinates language-state moves; `A.16.0` supplies an optional trajectory account when their history matters; `A.19` defines the CharacteristicSpace and its reusable predicates; `B.2.5` governs supervisor-subholon feedback; `C.27` distinguishes state or rate readings from intervention-sensitive temporal claims; `A.3.3` defines the reusable state-space and transition-law episteme.
- `E.19` already treats terminology and sentence-level precision restoration as required review checks, not editorial polish.
- `A.6.A` carries action-invitation discipline when a publication, representation, or cue invites an action without itself becoming authority, evidence, gate passage, or work completion.
- `C.11` carries decision-making and decision-record discipline when the question under repair is a decision rather than generic action.
- `A.15` and `A.15.4` split system-role kind and assignment, Method, WorkPlan, and actual-Work alignment from appearance-based reliance repair; do not use `A.15` as a universal repair for episteme-publication wording.
- `E.9` is the campaign `DRR` pattern for campaign-level content decisions; `E.11` is only for entry-discoverability situations and must not organize an episteme and publication repair by default.

These internal FPF patterns remain primary:

| Claim need | Relevant FPF pattern(s) | Alignment with C.2.P | Adoption result |
| --- | --- | --- | --- |
| Head-kind discipline | `E.10` | Use head-kind recovery before accepting a phrase. | Adopt. |
| Stable naming | `F.18` | Run a name card when a reusable head is being minted. | Adopt. |
| Relation precision | `A.6.P` | Recover relation kind, endpoints, slots, qualifiers, and scope when a relation or use-boundary claim is current. | Adopt. |
| Carrier and EntityOfConcern-description humility | `A.7` | Keep EntityOfConcern, Description episteme, and carrier apart before treating a publication as evidence, work, gate, or authority. | Adopt. |
| Episteme and publication ontology | `C.2.1`, `E.17.0`, `E.17`, MVPK, `E.24.PUB` | Separate episteme, publication, view, generic publication face, MVPK face under E.17 constraints, publication unit, carrier, and rendering. | Adopt. |
| Project-side downstream use | `A.6.A`, `A.10`, `A.15`, `A.15.4`, `B.3`, `A.20`, `A.21`, `C.11` | When a publication, display, cue, or explanation is treated as evidence, gate, decision, work permission, method, assurance, or engineering justification, name the applicable FPF pattern and the project-side FPF kind and reference. | Adopt. |

This reduced external-practice set changes the Solution in one practical way: epistemic precision restoration cannot close merely because the replacement sounds cleaner. The FPF kind, relation, declared use boundary, and any needed pattern application must be recoverable by value; otherwise the wording is blocked or becomes a candidate for a separate FPF-kind decision.

### C.2.P:11.2 - E.19 Review Profile Carry-Through {#e-19-review-profile-carry-through}

Run `PCP-TERM` when the repair changes episteme-publication-heavy naming, umbrella words, slash compounds, trigger-word replacements, or relation wording.

Run `PCP-BRIDGE` when the repair imports terms, claims, norms, or authority expectations between named sources, practices, disciplines, reference schemes, publication forms, or project record kinds.

Run `PCP-ENTRY` only when the repair changes which FPF pattern a working reader should apply in a problem situation. Do not use `PCP-ENTRY` as a substitute for the epistemic precision restoration itself.

Run `PCP-PRAG` when the repair changes reader action, practical payoff, or what the working reader can safely do next. A type-correct but inert repair fails this line even when every recovered kind is technically right.

When the repair changes evidence, proof, witness, grounding, explanation, gate, release, or engineering-justification claims, apply the relevant FPF pattern (`A.10`, `E.17.EFP`, `A.20`, `A.21`, `B.3`, or another applicable pattern) and select the current `E.19` profile by the changed claim. Do not mint a local evidence-review profile inside `C.2.P`.


## C.2.P:End {#end}
