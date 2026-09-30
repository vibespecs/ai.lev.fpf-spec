# A.6.RSIG - Recognition Signatures: Find the Defining Episteme for a Description {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Architectural pattern
> **Status:** Stable
> **Normativity:** Normative unless marked informative

## A.6.RSIG:1 - Problem frame {#problem-frame}

A reader often meets one description before they know whether it is the right
description to inspect. The reader may see a boundary clause, method note,
interface excerpt, pattern opening, or public projection. The reader first needs
to recognize the description before reconstructing its full semantics:
what description is seen, where it is encountered, what it applies to, what
excludes it, and which `definitionEpistemeRef` identifies its defining `U.Episteme`.
Reject a nearby reading or wrong defining `U.Episteme` only when the grounded-guard
condition in §4.1 holds.

**Plain recognition line.** Find the defining `U.Episteme` for the encountered description.

Use this pattern while the reader needs to decide whether one encountered
description is the right description to inspect, before broader comparison,
publication-face selection, boundary-claim routing, or pattern-language entry
comparison begins.

What goes wrong if this pattern is missed:

- one summary, excerpt, boundary phrase, or local top is mistaken for the
  defining `U.Episteme` of the description;
- one access/request description is over-read as a promise about downstream
  effect;
- one boundary-presented description is over-read as L/A/D/E-classified claim structure or
  as the full semantic claim set;
- one method note is treated as applicable before its actual method family and
  exclusions are recoverable;
- one pattern-local opening is forced to carry cross-pattern comparison that
  belongs to `E.11`.

What this pattern buys:

- the reader can tell what the encountered description is for before deeper
  semantics are reconstructed;
- carrier, projection, description, and defining `U.Episteme` stay distinct;
- false neighboring descriptions and wrong defining `U.Episteme` references become
  rejectable in one first pass;
- later boundary, publication, lexical, or pattern-language repairs start
  from first-contact identification instead of from guesswork.

Ordinary not-this-pattern boundary:

- not when the reader's question already concerns full routed-claim structure, published
  view law, lexical repair, or cross-pattern entry orientation;
- not when the real question is the whole semantics of the method, boundary
  claim, interface promise, or pattern;
- not when a search/query phrase needs naming repair rather than
  first-contact recognition of a particular encountered description.

## A.6.RSIG:2 - Problem {#problem}

When first-contact recognition is under-governed, several defects recur:

1. One reader finds a boundary, method, interface, or pattern-local opening but
   cannot tell whether it is the right description to inspect.
2. An encountered carrier or public projection is misread as the defining `U.Episteme`.
3. Recognition cues drift into description semantics, workflow hints, graph
   metaphors, or lexical aliases that belong elsewhere.
4. Pattern-entry navigation is asked to identify the encountered description
   before the reader can begin pattern-language comparison.

## A.6.RSIG:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| First-contact precision vs reader economy | The cue needs enough discriminating detail without turning every opening into a mini essay. |
| Neutral substrate vs local specialization | This pattern governs description-recognition signatures in general without absorbing pattern-entry discoverability, publication-face law, or boundary-claim routing. |
| Recognition vs semantics | The cue helps the reader recover the right description and defining `U.Episteme`, not silently redefine the description's full semantics. |
| Carrier/projection vs authority | An encountered carrier can help recognition without becoming the defining episteme. |
| Local wording vs controlled lexemes | Real reader language remains usable without minting uncontrolled aliases or shadow names. |
| Readability vs auditability | The signature stays usable by readers while remaining crisp enough for later review and boundary checking. |

## A.6.RSIG:4 - Solution {#solution}

### A.6.RSIG:4.1 - Recognition-cue discipline and non-goals {#recognition-cue-discipline-and-non-goals}

`A.6.RSIG` governs description-recognition signatures in general: the
first-contact cue structure by which one reader can recover what encountered
description is live, what carrier or projection exposed it, what it applies to,
what excludes it, and which `definitionEpistemeRef` identifies its defining `U.Episteme`.
Reject a nearby reading or wrong defining `U.Episteme` only when it passes F.19's
grounded-guard test: the rejected reading has an independent local ground, is
plausible for the intended reader, and changes truth, understanding, selection,
safety, stop, reliance, or action. Use the
smallest clear correction; do not invent an alternative to fill the cue shape.

Here "description-recognition signature" is a lower-case authoring and reading
discipline, not by itself a typed `U.Signature` or a new formal kind. A typed
declaration requires the applicable neighboring pattern's explicit conditions.

The encountered carrier or projection may help recognition; it does not become
authoritative merely by being encountered.

Use `definitionEpistemeRef` for the defining `U.Episteme`. If the definition is available only through one publication, cite separately the exact E.24.PUB publication occurrence that makes it available; the publication, projection, or carrier does not become the defining episteme merely because it exposed the definition to the reader.

`A.6.RSIG` does not govern:

- general information architecture or search UX;
- documentation layout or publication-face selection;
- pattern-entry discoverability across a pattern language;
- the full semantics of the description itself;
- lexical repair, alias acceptance, or naming governance as such;
- graph ontology, workflow sequencing, or runtime route semantics.

### A.6.RSIG:4.2 - Two-level description-recognition shape {#two-level-description-recognition-shape}

**Reader-visible minimum.** For ordinary reader-facing use, the minimum is not a card. One or two
sentences may be enough if they make recoverable:

1. what this description is for;
2. when it applies;
3. when it does not apply;
4. which definitionEpistemeRef applies;
5. what nearby false reading or wrong defining `U.Episteme` to reject, when
   the grounded-guard condition in §4.1 holds.

**Review-expanded shape, only when needed.** When a recognition cue affects a
decision or is being reviewed, use the expanded recoverability shape:

```text
description_seen
encountered_carrier_or_projection
reader_viewpoint
case_signal_or_access_condition
applies_to
excludes
expected_first_recognition_gain
first_admissible_entry_stop_or_reroute
definitionEpistemeRef
projection_role_if_any
nearby_false_description_or_wrong_definition_episteme
```

The `nearby_false_description_or_wrong_definition_episteme` field is optional:
use it only when the grounded-guard condition in §4.1 holds.

This shape is a review aid, not a mandatory form for every encountered
description. It exists to keep description, carrier, projection, and definitionEpistemeRef from
collapsing into one overloaded publication label or projection label.

### A.6.RSIG:4.2.1 - Minimal local repair and review sequence {#minimal-local-repair-and-review-sequence}

Use this sequence when authoring or reviewing one recognition-signature repair:

1. Name the `description_seen` and the reader viewpoint in one concrete first
   sentence.
2. Name the encountered carrier or projection if confusing it with authority is
   a live risk.
3. State what the description applies to and what excludes it.
4. Name the defining `U.Episteme` to inspect first.
5. When the grounded-guard condition in §4.1 holds, name the nearby false
   description or wrong defining `U.Episteme` to reject.
6. State the first admissible entry stop or neighboring-pattern application.
7. If that stop cannot be stated without A.6.B claim routing, publication-face law,
   lexical repair, or cross-pattern comparison, apply the appropriate neighboring pattern instead of
   stretching `A.6.RSIG`.

Minimal admissible output:

- one first-contact recognition statement the reader can use immediately;
- one explicit defining `U.Episteme`;
- an explicit false-neighbor rejection when the grounded-guard condition in §4.1 holds;
- one admissible entry stop or reroute.

### A.6.RSIG:4.3 - Parent cases {#parent-cases}

`A.6.RSIG` keeps the main parent cases explicit:

- **boundary-description recognition**: can one reader recover what one
  boundary-presented description is for before the reader needs to classify its
  claims as L/A/D/E;
- **method-description applicability recognition**: can one reader recover
  whether one method description is the right description to inspect, reject, or
  compare for the reader's question;
- **interface/access-description recognition**: can one reader recover the
  right access or interface description without confusing it with promise,
  execution, or downstream effect semantics;
- **pattern-local recognition-signature case**: can one reader recover one
  pattern opening as the right first description to inspect before broader
  pattern-language comparison begins.

### A.6.RSIG:4.4 - Neighbor boundaries {#neighbor-boundaries}

Neighbor boundaries remain explicit:

- use `A.6.B` when the reader needs to classify the boundary claims as `L/A/D/E`;
- `E.17.0` tests viewpoint/view membership; `E.17` publishes reader-facing forms of an already accepted engineering account;
  use `E.24.PUB` when publication occurrence, form, or carrier identity affects the recognition use;
- `E.10.D2` recovers description-episteme and specification-use distinctions;
  use `E.10` cues within `F.19` for wording, `A.6.P` for under-specified direct relations, and `F.18` for durable naming and its collision checks;
- `C.16.Q` repairs overloaded recognition or discoverability quality wording;
  `C.25` applies when the quality-family claim depends on several differently typed contributors; a single-Characteristic claim stays with its direct Characteristic pattern;
- the relevant authoritative pattern body governs pattern semantics when the
  encountered description is one pattern-local opening.

The four-part split for pattern-local recognition is:

| Recognition concern | Governing FPF pattern or source | What it governs |
| --- | --- | --- |
| Generic first-contact description recognition | `A.6.RSIG` | The neutral cue shape: description, carrier or projection, definitionEpistemeRef, exclusions, and a false neighbor when §4.1's grounded-guard condition holds. |
| Local placement and form | `E.8` | How the pattern's `Problem frame` carries the first-reading role. |
| Actual local semantics | The pattern itself | The pattern's governed object, solution, consequences, and conformance law. |
| Cross-pattern comparison | `E.11` and `I.2` | Candidate patterns, tempting wrong patterns, reclassification of the reader's question, and expanded entry-disambiguation cases. |

### A.6.RSIG:4.5 - When a neighboring pattern is needed {#when-a-neighboring-pattern-is-needed}

If the task requires a quality claim, typed signature declaration, reusable
description, or publication-face rule, use the neighboring pattern that governs
that object or claim, including its evidence requirements. The recognition cue
alone does not establish that result.

## A.6.RSIG:7 - Conformance checklist {#conformance-checklist}

- @fact:CC-RSIG-1 **CC-RSIG-1 First-contact only.** The pattern governs recognition of the @status:spec/done
  right description, not the full semantics of that description.
- @fact:CC-RSIG-2 **CC-RSIG-2 Carrier/definition-episteme split.** A conforming description-recognition signature @status:spec/done
  distinguishes `description_seen`, encountered carrier or projection,
  defining `U.Episteme`, and projection role when those distinctions are
  load-bearing. The encountered carrier or projection may help recognition,
  but it does not become authoritative merely by being encountered.
- @fact:CC-RSIG-3 **CC-RSIG-3 Neighbor boundaries explicit.** The text states the conditions @status:spec/done
  under which the recognition question calls for each relevant neighboring
  pattern in §4.4; use only the patterns that govern the current questions.
- @fact:CC-RSIG-4 **CC-RSIG-4 No kind inflation.** An ordinary recognition cue is not by itself a @status:spec/done
  typed `U.Signature`; a task requiring a typed declaration uses the applicable
  neighboring pattern under §4.5.
- @fact:CC-RSIG-5 **CC-RSIG-5 Recoverable cue shape.** For load-bearing cases, description, @status:spec/done
  viewpoint, cue, applicability, exclusion, defining `U.Episteme`, and admissible
  entry stop remain recoverable. A false neighbor is required only when the
  grounded-guard condition in §4.1 holds.
- @fact:CC-RSIG-6 **CC-RSIG-6 No alias minting.** Query cues and ordinary phrasing do not by @status:spec/done
  themselves establish a naming settlement or Bridge. Use `F.18` for naming
  settlement and `F.9` for a Bridge, each under its own conditions.

## A.6.RSIG:9 - Consequences {#consequences}

This pattern gives one neutral governing discipline for first-contact
description recognition without turning discoverability into one universal
governing pattern. It sharpens the boundary between cue recognition, semantic
authority, lexical repair, publication-face projection, and pattern-language
entry.

The cost is one extra explicit split when a cue is confusing: description,
encountered carrier or projection, and defining `U.Episteme` must not be
collapsed; include the false neighbor when §4.1's grounded-guard condition holds. The cost stays bounded because the expanded shape is review-only
or risk-triggered, not a required card for ordinary prose.

## A.6.RSIG:12 - Relations {#relations}

- **Builds on:** `A.6`, `A.6.P`, `F.18`, `E.10`
- **Does not specialise:** `A.6.0` / `U.Signature`; it uses "signature" only in the lower-case cue-pattern sense unless an explicit neighbouring pattern promotes the structure into a typed declaration.
- **Neighbors:** `A.6.B`, `A.6.C`, `E.17.0`, `E.17`, `E.10.D2`, `C.25`, `C.16.Q`
- **Supports:** `E.11` as the pattern-language application above this neutral substrate


## Dependencies {#dependencies}

- @fact:DEPENDS-ON Dependencies (as published): `spec://ai.lev/fpf-spec/contract/A-6#root`, `spec://ai.lev/fpf-spec/contract/A-6-P#root`, `spec://ai.lev/fpf-spec/contract/F-18#root`, `spec://ai.lev/fpf-spec/contract/E-10#root` @status:spec/done

#source spec://ai.lev/fpf-spec/source/A-6-RSIG
