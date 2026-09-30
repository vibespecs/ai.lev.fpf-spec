# E.17.AUD - PublicationUnit Stability Discipline - keep one publication unit stable enough to read honestly: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## E.17.AUD:5 - Worked slices {#worked-slices}

### E.17.AUD:5.1 - Local-head case {#local-head-case}

A semio note keeps saying `this review` and `this interpretation`, but nobody can tell which FPF kind or locally declared head those lexical heads name here. The rest of the publication unit under review is still locally stable once the local lexical head is repaired. The honest move is not broad publication-unit stabilization. It is `Local Head Restoration`.

### E.17.AUD:5.2 - Whole-unit interpretation-shift case {#whole-unit-interpretation-shift-case}

A memo starts about one bounded architecture question over an inherited lineage or move, then shifts into wider rollout or approval language without declaring the transition. Repairing one sentence does not stabilize the publication unit under review because its concern and carried publication move have widened; that does not by itself establish a changed EntityOfConcern. The honest move is `PublicationUnit Primary-Subject Discipline`.

### E.17.AUD:5.3 - Stable-unit comparison case {#stable-unit-comparison-case}

A comparison sheet already keeps one stable primary subject and one clear outside boundary to work, work planning, decision, gate, or reliance claim, but the team is using publication-unit instability language because the comparison is contentious. The honest move is not more publication-unit stabilization. It is `E.17.ID.CR ComparativeReviewUnit`.

### E.17.AUD:5.4 - Explanation-laundering case {#explanation-laundering-case}

An onboarding explainer starts from one stable source-pinned note, but then the simplified prose begins to sound like canonical assurance or policy. The publication unit may still be readable, yet the main problem situation is no longer publication-unit stability. Leave publication-unit stability and use `E.17.EFP`'s simpler source-linked boundary sentence first; instantiate `ExplanationFaithfulnessProfile` only when explanation-class ambiguity still changes the next action.

### E.17.AUD:5.5 - Downstream decision and reliance case {#downstream-decision-and-reliance-case}

A status card starts as one bounded summary of progress, then quietly becomes the place where people infer approval, assignment, or go or no-go claim or effect. The problem is no longer only publication-unit stability. The honest move is to stop treating the card as if it were still only one neutral note and use the downstream decision, gate, work, or reliance publication.

### E.17.AUD:5.6 - Quick contrasting cases {#quick-contrasting-cases}

Use this quick contrast set when the first interpretation is still foggy:

| Near-miss case | What to look for | Honest next pattern or project reference |
| --- | --- | --- |
| `LHR-only` | one overloaded local lexical head is doing most of the semantic work while the publication unit under review otherwise stays stable | apply `Local Head Restoration` |
| `whole-unit interpretation shift` | the publication unit under review quietly changes primary subject or carried publication move | apply `PublicationUnit Primary-Subject Discipline` |
| `stable comparison -> CR` | the unit is already stable and the live problem situation is bounded comparison over pinned source publications | apply `E.17.ID.CR ComparativeReviewUnit` |
| `downstream claim or effect overread` | readers are inferring approval, assignment, or go or no-go claim or effect from the publication unit | leave the publication-unit stability family for the more honest downstream decision, gate, work, or reliance publication |
| `modeling-lens hidden` | the unit only makes sense because of one unpublished model, formal substrate, or rationale | publish that substrate or rationale briefly or use a heavier publication form or neighboring pattern |

## E.17.AUD:6 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Why it fails | How to avoid it |
| --- | --- | --- |
| Fixing one sentence while the whole unit already carries a quiet interpretation shift | local repair is asked to carry whole-unit stabilization | check primary subject, carried publication move, and outside boundary to work, work planning, decision, gate, or reliance claim before repairing the sentence |
| Treating form labels as if they changed the publication unit under review | `table`, `sheet`, or `screen` is used as if it already named a different ontology or downstream claim or effect | treat those as presentation forms first; only leave this pattern when the problem situation itself changes |
| Laundering comparison through stability language | teams keep saying the unit is unstable when the active problem situation is already bounded comparison | apply `E.17.ID.CR ComparativeReviewUnit` and name the exact source publications |
| Laundering downstream decision or reliance through clearer prose | a better-written note is over-read as if it had become an approval, gate, work, or reliance text | keep the outside boundary to work, work planning, decision, gate, or reliance claim explicit and leave this pattern when downstream claim or effect appears |
| Letting three repair choices act at once | lexical-head repair, whole-unit stabilization, and a neighboring-pattern application are patched in parallel with no shared primary-subject interpretation | use the working card first and name one current repair choice before patching the unit |

## E.17.AUD:8 - Rationale {#rationale}

`PublicationUnit Stability Discipline` is worth stating explicitly because local lexical-head repair and whole-unit primary-subject stabilization are both already real problem situations, but authors and reviewers still need one stabilization check that says when the case is local, when it is whole-unit, when it is already bounded comparison, and when it has left the publication-unit stability family entirely.

The pattern stays intentionally narrow. It does not turn every publication-unit problem into publication design or downstream decision, gate, work, or reliance work. Its job is to keep one publication unit honest enough that readers can still tell what it is mainly about, which carried publication move it makes, and which downstream `U.Work`, work planning, decision, gate, or reliance claim remains outside.

## E.17.AUD:9 - SoTA-Echoing {#sota-echoing}

**Claim 1.** FPF's current EntityOfConcern and description apparatus keeps the entity of concern distinct from the claim-bearing episteme or publication that describes it. This supplies the exact-entity case of the publication-unit subject distinction.

**Practice, source, alignment, and adoption.** `C.2.1`, `A.7`, `E.17`, and the description patterns keep an EntityOfConcern, a description episteme, its publication occurrence, form, and carrier distinct. ISO/IEC/IEEE 42010:2022 is standards lineage for the narrower architecture/architecture-description distinction, not the source of this general publication-unit ontology. `PublicationUnit Stability Discipline` adapts the current FPF distinction to one readable unit and requires a primary-subject shift to be explicit; an EntityOfConcern change requires the exact C.2.1 case. For a reviewer or architect, this is the practical guard behind worked slices 5.2 and 5.3.

**Claim 2.** Best-known current information-for-use practice treats user-facing units as purpose-bound, structured information rather than as loose bundles that can mix explanation, instruction, warning, and decision or reliance effect by convenience.

**Practice, source, alignment, and adoption.** Joint IEC and IEEE 82079-1:2019 requires information for use to be purpose-directed, structured, and evaluated for usability. `PublicationUnit Stability Discipline` adopts purpose-bound publication units and explicit outside boundaries to work, work planning, decision, gate, or reliance claim, adapts that discipline from information-for-use to notes, memos, sheets, tables, and screens, and rejects the shortcut where a clearer or official-looking unit is treated as if it had already become approval, policy, gate, work, or reliance text. For a manager or operator, this is the practical guard behind worked slices 5.4 and 5.5: better explanatory form does not itself mint downstream claim or effect.

**Claim 3.** Best-known current pattern-writing and pattern-validation practice keeps patterns tied to recognisable situations, explicit problem, solution, and consequence structure, and reviewable rationale rather than elegant internal naming alone.

**Practice, source, alignment, and adoption.** Iba (2021), [How to Write Patterns](https://hillside.net/plop/2021/plopourri/PLoP21_PLOPOURRI_Iba_Methodology4.pdf), and Riehle, Harutyunyan, and Barcomb (2025), [Pattern Discovery and Validation Using Scientific Research Methods](https://doi.org/10.1007/978-3-662-70810-1_6), with the [authors' 2021 preprint](https://arxiv.org/abs/2107.06065), treat pattern writing and validation as requiring recognisable situations, explicit structure, and reviewable reasoning rather than only elegant naming. `PublicationUnit Stability Discipline` adopts worked slices, recognisable entry cues, and an explicit next-pattern and project-reference boundary, adapts those expectations to publication-unit stability work, and rejects a pattern text that is cleanly labeled but domain-thin or reader-thin. For the current working reader, this is the practical guard behind the Problem frame and slices 5.1 through 5.5: the pattern should be usable before one has to reconstruct the surrounding rationale from scratch.

**Local stance.** The current SoTA claim is narrow. This pattern is not claiming one universal theory of documents. It claims a smaller and more practical point: one publication unit stays trustworthy only when its primary subject, carried publication move, and outside boundary to work, work planning, decision, gate, or reliance claim remain explicit enough for cold readers to recover, and when practitioners apply the specific neighboring pattern needed by a different problem.


## E.17.AUD:End {#end}
