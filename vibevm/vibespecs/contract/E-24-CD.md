# E.24.CD - Ontic Candidate Detection and First-Use Disposition {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Part E FPF authoring discipline pattern
> **Status:** Stable
> **Normativity:** Normative unless a section is explicitly informative

## E.24.CD:0 - Use This When {#use-this-when}

Use this pattern when a recurring word, card, table, schema, diagram, record, draft pattern row, or field bundle looks like a new FPF subject and the author must decide what to do next.

Typical moments:

- one word such as "process", "source", "quality", "architecture", "problem", "view", the unqualified word "role", "function", "mechanism", or "method" points to several FPF objects or claims at once;
- several patterns repeat a similar declaration, participant list, or relation rule;
- a project data structure looks concept-shaped, although it may be only a claim-bearing episteme, publication form, representation, or local record;
- a draft ToC row names a family that no current pattern yet governs;
- a proposed `U.*` kind feels useful, but it may duplicate a current kind or direct relation.

**Primary EntityOfConcern.** When the author records this choice in a C.2.1 episteme, its EntityOfConcern is the subject already identified under a direct pattern. If that subject cannot yet be identified, use the source episteme or expression entity whose inquiry remains open. The visible form and the note recording the disposition are not substitutes.

**First useful move.** Write one plain sentence: “For this work or decision, we need to know or do `<action>` about `<subject>`.” Then ignore the wrapper long enough to recover the subject, the needed claim, and the current pattern that defines or constrains it. Apply the first truthful disposition in section 4.

**What goes wrong if missed.** FPF grows shadow ontology. A table becomes a kind; a field label is mistaken for a relation-participant meaning; a filled field is treated as an actual relation participant merely because it occupies a column; a card becomes the subject; or a convenient word creates a second ontology over values and relations that already have subject patterns.

**What this buys.** The author identifies one usable subject pattern without filling a candidate record or maintaining a registry. A genuine durable ontic must still pass E.24's full identity and relation test; simpler cases stop with their subject pattern, local classification, description or publication handling, wording repair, or a precise unresolved question.

**Not this pattern when.**

- If one existing subject pattern already states the needed claim, use it directly.
- If a local kind, criterion, candidate judgment, or extension is already the question, use `C.3`, `C.3.1`, and `C.3.2`.
- If the current question is a description episteme, use `C.2.1` for its identity and the subject-specific description pattern when one applies. For view membership, publication form or occurrence, representation, or carrier, use `E.17.0`, `E.24.PUB`, or `C.29`.
- If the subject and governing claim are clear and only the wording hides them, use `F.19` for wording repair and `E.10` for any unresolved meaning.
- If a durable ontic has already been selected, use `E.24`; if a durable public `U.*` kind is separately at issue, use `E.24.UK`.
- If the work is comparing architecture alternatives, construct the evaluation through `A.19.ECS`.

## E.24.CD:1 - Problem Frame {#problem-frame}

An apparent ontology candidate usually arrives inside something visible: a label, form, record, diagram, source passage, or repeated field list. That visible thing may point to a real durable subject, but it may instead carry claims about several already governed objects, publish or represent them, classify them for one context, or merely use an imprecise word.

E.24.CD governs this first-use choice before E.24 opens. It neither admits a durable ontic nor creates a candidate object of its own.

## E.24.CD:2 - Problem {#problem}

Without an explicit first-use disposition:

1. **Publication forms become false subjects.** A card, table, or schema receives ontology authority because it is visible.
2. **Local classification hardens into public ontology.** A criterion useful in one context is treated as a durable FPF kind.
3. **Subject patterns are bypassed.** Existing methods, work, relations, epistemes, structures, sources, and results are duplicated under a new head.
4. **Wording repair becomes ontology creation.** A broad word is replaced with a new broad word while the actual subject and predicate remain hidden.
5. **Candidate work becomes a registry ritual.** Authors fill fields or scores for possible ontics instead of deciding the current case.

## E.24.CD:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Early recognition vs premature ontology | A recurring concern should be noticed, but recurrence alone must not mint a durable subject or `U.*` kind. |
| Visible form vs governed subject | A form can reveal the problem while remaining an episteme, publication form, representation, carrier, or local record. |
| Direct reuse vs shared coordination | Existing patterns should carry their own claims; E.24 opens only when dependent patterns need one stable subject identity and minimal relation set. |
| First-use affordability vs adequate discrimination | The author needs a quick choice, but the choice must still separate direct use, local classification, publication, wording, and durable admission. |
| Traceability vs registry growth | A disputed choice may need one explanatory sentence; it does not need a standing candidate catalogue. |

## E.24.CD:4 - Solution {#solution}

Start from the work that is blocked, not from the shape of the source material.

Ask these four questions in order:

1. **What must the next person do or decide?** Name the comparison, classification, publication, repair, decision, or other practical use.
2. **What is that use about?** Name the subject, claim, or source expression without treating its card, row, filename, diagram, or field bundle as the answer.
3. **Which current pattern already governs the needed claim?** Name the predicate or judgment that would let the work proceed.
4. **If that pattern does not close the case, what is actually missing?** State one applicable pattern or one precise unresolved stop below.

### E.24.CD:4.1 - Apply the first truthful disposition {#apply-the-first-truthful-disposition}

Plain `situation`, `incident`, `current configuration`, `operating <system>`, and `emergency` are recognition cues, not kind names. Recover only the subjects, claims, and relations that the receiving work actually needs.

| Current need | Next use | Stop that follows |
| --- | --- | --- |
| One current subject pattern already states the needed claim or action. | Apply that subject pattern. If the missing piece is a relation-bearing claim that no current direct predicate closes, apply `A.6.RCD` before proposing a relation kind. | Do not create an ontic, kind, candidate note, or disposition record. A local compound claim or predicate-definition episteme is neither a relation kind nor an occurrence; only a separately justified kind candidate proceeds through `E.24` and `E.24.UK`. |
| One exact ClaimGraph forms one claim-bearing whole about one truthful exact EntityOfConcern under one effective ReferenceScheme. | Use `C.2.1` to identify that episteme. Other independently governed objects may be designated inside its claims without becoming extra EntityOfConcern fields or ontic slots. | If one truthful EntityOfConcern or one identity-bearing ClaimGraph cannot be recovered, keep the epistemes separate. State a collection, publication, representation, or other use relation only when its own predicate obtains; common use or co-publication does not identify one episteme. |
| Wording such as `situation`, `incident`, `current configuration`, `operating <system>`, or `emergency` groups several cues. | Recover the exact systems or holons, characteristic or state claims, actual part relations, and only the temporal or causal relations needed by the current use. Add actual `U.Transformation` or `U.Work` only when independently grounded under `A.3.4` or `A.15.1`. Use a possible-state episteme when possibility is the subject, and a separate C.2.1 description episteme only when claim-bearing orientation is current. | Their conjunction is neither `U.Situation` nor `U.IncidentSituation`. An episteme's EntityOfConcern and any grounding holon in a separately current `EpistemeEmpiricalGroundingRelation` neither identify the world-side subject nor become mandatory fields. Stop decomposition once the action-facing distinction needed by the receiving use is recovered. |
| A proposed subject exists only as an arbitrary fusion, co-presence, connected set, or chosen boundary. | Reject the bundle without forcing it through a construction record. If a constructed object survives as the current subject, apply `B.1`, `A.14`, and `C.13`, and apply `B.2` only when whole reidentification is current; recover its exact construction inputs, whole-forming relations, and identity rule. | Fusion, co-presence, connectedness, and a selected boundary alone form no durable whole. The no-mint result does not block a genuinely irreducible subject later shown to have its own identity and obtaining laws. |
| Repeated typed reasoning needs a local criterion, candidate judgment, or true-candidate set for one context slice. | Use `C.3`, `C.3.1`, and `C.3.2`. | The local kind, `KindSignature`, judgment, and optional extension stay distinct; neither a public `U.*` kind nor a classification-relation occurrence follows. |
| A card, record, table, diagram, file, or schema carries claims, is used as a description, conforms to a viewpoint, expresses an edition, represents something, or bears a form. | Use `C.2.1` to identify an episteme only when its constitution test passes. If it describes a method, structure, relation occurrence, or another subject, apply that subject's description pattern. Use `E.17.0` for actual view membership, `E.24.PUB` for publication, and `C.29` for representation and correspondence. Several patterns can apply because they govern different objects or relations. | Visible shape does not identify the described subject or make any neighboring relation obtain. |
| A path, table, dashboard, schema, or other declarative form seems to authorize, dispatch, prove, prescribe, or perform something by its shape. | Use `C.2.P.DR` to name the visible expression, recover the direct object or relation, state its representation or correspondence use—or `none`—and block the unsupported action claim. | A declarative form does not itself authorize or dispatch work, perform an action, or grant authority. |
| Words such as `relation`, `slot`, `field`, `interface`, bare *role*, `function`, or `endpoint` still leave the object or claim unclear. | Use E.10.ROLE first for bare *role*; continue to A.6.RSIR when it denotes relation participation, a declaration place, an interface place, or a representation position. Use A.6.F for function wording and A.6.P or the pattern for the recovered relation. Then stop at that pattern. | An engineering word creates no subject kind, relation kind, participant, declaration, system-role kind, or assignment. |
| The subject and governing claim are already clear, but a word or phrase compresses them. | Repair the bounded wording through `F.19`; use `E.10` for any unresolved meaning. | A clearer name does not create a new subject, relation, or kind. |
| An already governed value needs a stable reusable name rather than a repaired sentence. | Use `F.18` after recovering the value, its kind and subject pattern, its effective reference scheme, and the local sense to be named. For relation-facing wording, settle any missing direct relation through `A.6.RCD` first. | A label or `NameCard` neither admits the value or a public kind nor makes a relation obtain. |
| One blocked use concerns an independently recoverable candidate, proposal, or source construct; named consumers show concrete cross-pattern duplication or disagreement pressure; and one obvious direct route does not close it. | Open `E.24` and transfer only those detection facts. Let E.24 test identity, the minimal relation set, dependent reliance, non-duplication, declared use, and applicability limits. | E.24.CD neither requires those settlement results nor admits or rejects the ontic. A still-missing identity or relation rule can reach E.24's unresolved branch. |
| The subject, needed claim, or subject pattern cannot yet be recovered. | Keep the inquiry attached to the source expression or blocked work and name what is missing. | Do not hide non-settlement inside a candidate record, score, provisional `U.*` name, or “future ontology” list. |

When a durable public `U.*` kind is also proposed, `E.24.UK` returns its separate admission result. If the ontic and kind are both new, use the atomic co-decision already defined by E.24 and E.24.UK; neither result proves the other.

### E.24.CD:4.2 - Recover objects hidden by a visible form {#recover-objects-hidden-by-a-visible-form}

For a project card, row, schema, or diagram, inspect only what the current work consumes:

1. Which filled statements are claims, and what is each claim about?
2. Which entities or non-entity values are independently identified under their direct patterns?
3. Which direct predicates are asserted, what are their actual participants, and which independently established facts satisfy their obtaining conditions?
4. Is the visible arrangement a publication form, a C.29 representation, a carrier, or merely a local layout?
5. Does the work need local classification of a candidate, or only a claim about an already governed feature?
6. For a suspected overread of the visible form, use `F.19`'s grounded-contribution test and state the correction that changes the needed claim or next action.

A field label is not a `SlotSpec`. `A.6.5` governs the declaration: a reusable `SlotSpec` appears only inside a `RelationSignature` for an already recovered direct relation and only when a named later use needs that declaration. A row value is not an actual relation participant merely because it occupies a column.

### E.24.CD:4.3 - Open E.24 when cross-pattern pressure is concrete {#open-e-24-when-cross-pattern-pressure-is-concrete}

Open E.24 when these detection facts are recoverable:

- one blocked use or decision;
- one independently recoverable candidate entity, proposal episteme, or source-construct entity that carries the inquiry without presupposing a durable ontic;
- concrete duplication or disagreement pressure in more than one current pattern description;
- the named consumers that make shared coordination plausible; and
- why one obvious direct-pattern route does not already close the blocked use.

Transfer those facts to E.24. E.24—not E.24.CD—tests the complete identity or constitution rule, minimal direct-relation set, dependent reliance, non-duplication, practical gain, declared use, and its applicability limits. If a required entry fact or settlement condition cannot be established, E.24 may return its unresolved result. Detection therefore does not require the author to settle the candidate before opening the settlement pattern.

A plainly direct case still stops at its subject pattern. Repeated words, several source forms, copied fields, or a useful schema can prompt inspection, but without a blocked use, an independently recoverable inquiry subject, concrete cross-pattern pressure, named consumers, and failure of an obvious direct route, they do not open E.24.

### E.24.CD:4.4 - State one result and stop {#state-one-result-and-stop}

Most cases need only one sentence:

> For `<work or decision>`, apply `<subject pattern>` to `<exact subject or claim>` because `<decisive fact>`; next, `<action or stop>`.

When no pattern can yet apply truthfully, say:

> For `<work or decision>`, leave `<exact subject or claim question>` unresolved because `<missing subject, predicate, or subject pattern>`; return when `<missing fact becomes recoverable>`.

Any denied reading must pass `F.19`'s grounded-contribution test. Use a longer explanation only when another author must understand a disputed disposition. Do not create an `OnticCandidateCluster`, candidate registry, scorecard, or mandatory disposition form. Continue at the applicable pattern or unresolved return; reopen E.24.CD only if the recovered subject or practical use changes.

## E.24.CD:7 - Conformance Checklist {#conformance-checklist}

| Check | Requirement |
| --- | --- |
| `CC-E24CD-1` | @fact:CC-E24CD-1 The first-use disposition starts with a recognizable work or decision and the subject or claim that blocks it. @status:spec/done |
| `CC-E24CD-2` | @fact:CC-E24CD-2 A visible card, row, schema, diagram, filename, or field bundle is not treated as the subject merely by form. @status:spec/done |
| `CC-E24CD-3` | @fact:CC-E24CD-3 Independently governed objects and direct predicates are recovered before a new ontic or kind is proposed. @status:spec/done |
| `CC-E24CD-4` | @fact:CC-E24CD-4 A current subject pattern is applied when it already closes the needed claim. A relation-bearing claim that no current predicate closes goes through A.6.RCD; a local compound claim or predicate-definition episteme is not thereby a relation kind or occurrence. @status:spec/done |
| `CC-E24CD-5` | @fact:CC-E24CD-5 One C.2.1 episteme requires one exact ClaimGraph, one truthful exact EntityOfConcern, and one effective ReferenceScheme. Otherwise epistemes remain separate, and co-use or co-publication supplies no shared identity. @status:spec/done |
| `CC-E24CD-6` | @fact:CC-E24CD-6 Local classification uses C.3.2's kind, signature, judgment, and optional extension distinction and does not imply a public `U.*` kind or direct classification relation. @status:spec/done |
| `CC-E24CD-7` | @fact:CC-E24CD-7 Episteme, view membership, publication form, representation, carrier, and publication occurrence remain separate and use their subject patterns only when current. @status:spec/done |
| `CC-E24CD-8` | @fact:CC-E24CD-8 E.24 opens from a blocked use, an independently recoverable candidate, proposal, or source construct, concrete duplication or disagreement pressure across named patterns, named plausible consumers, and failure of one obvious direct route. E.24.CD supplies those entry facts; E.24 owns the identity rule, minimal relation set, dependent-use judgement, non-duplication result, practical gain, declared use, and applicability limits, and may return unresolved. @status:spec/done |
| `CC-E24CD-9` | @fact:CC-E24CD-9 Any public U-kind question is handled by E.24.UK as a separate admission result; E.24.CD admits neither ontic nor kind. @status:spec/done |
| `CC-E24CD-10` | @fact:CC-E24CD-10 No candidate cluster, registry, scorecard, or mandatory disposition form is created. @status:spec/done |
| `CC-E24CD-11` | @fact:CC-E24CD-11 The result names the exact pattern applied to the exact subject or claim, or a precise unresolved stop, and gives the next action or return condition. Any denied reading passes `F.19`'s grounded-contribution test. @status:spec/done |
| `CC-E24CD-12` | @fact:CC-E24CD-12 A record-shaped false candidate keeps holder, status bearer and value, method, mechanism, plan, work, evidence item and use, result and relation, target and subject relation, and source and source-use relation distinct; absent fields and row shape establish none of them. @status:spec/done |
| `CC-E24CD-13` | @fact:CC-E24CD-13 Bare *role* uses E.10.ROLE and then the recovered branch; ambiguous relation, slot, interface, function, and endpoint wording uses its matching precision-restoration pattern. None becomes ontology by wording alone. @status:spec/done |
| `CC-E24CD-14` | @fact:CC-E24CD-14 Declarative-form agency is blocked through C.2.P.DR, and reusable naming starts in F.18 only after the governed value and any needed relation settlement are available. @status:spec/done |
| `CC-E24CD-15` | @fact:CC-E24CD-15 Wording such as `situation`, `incident`, `current configuration`, `operating <system>`, or `emergency` recovers only the Systems, claims, Work, change, and temporal or causal relations needed by the current use; their conjunction creates neither `U.Situation` nor `U.IncidentSituation`. Every asserted actual Work first recovers each precise performer's A.13 core and is independently admitted under A.15.1 from its performance history, Method, time, and containing System. F.6 is added only when precise assignment-bound attribution is also current; local system-role-kind classification remains separate. Intended action stays plan or other modal content until its predicates obtain. @status:spec/done |
| `CC-E24CD-16` | @fact:CC-E24CD-16 Arbitrary fusion, co-presence, connectedness, or a chosen boundary creates no whole. Only a surviving constructed-object candidate is tested for exact inputs, whole-forming relations, and identity under B.1, A.14, C.13, and B.2 when reidentification is current. @status:spec/done |
| `CC-E24CD-17` | @fact:CC-E24CD-17 Mathematical inconsistency names exact claims or epistemes, the declared formal substrate, and the direct inconsistency or consequence relation; it establishes no world event, causation, Work, Transformation, Problem, or situation. @status:spec/done |
| `CC-E24CD-18` | @fact:CC-E24CD-18 A ProblemCard, signal, forecast, scenario, formulation, actual Problem, and later problematization or work remain under C.22.2, C.22.PFR, and their exact continuation governors rather than one card-derived ontic. @status:spec/done |

## E.24.CD:9 - Consequences {#consequences}

Positive consequences:

- authors reach a subject pattern from a recognizable work situation;
- durable ontics are proposed from an identity and reuse gap rather than from form or vocabulary;
- local classification, claim coordination, publication, representation, and wording remain cheaper dispositions;
- cards, records, tables, and schemas remain useful source material and detection cues without becoming ontology by appearance;
- no candidate registry or score ritual is added to routine authoring.

Costs:

- the author must recover the subject and needed claim before choosing a subject pattern or unresolved stop;
- some attractive names are lowered to local kinds, source wording, epistemes, publication forms, or representations;
- a genuine durable candidate still requires the full E.24 decision and, when current, a separate E.24.UK admission result.

## E.24.CD:12 - Relations {#relations}

- **Builds on:** `E.24` for durable ontic settlement; `E.24.UK` for separate public U-kind admission; `C.2.1` for exact episteme constitution; `C.3`, `C.3.1`, and `C.3.2` for local typed projection; `E.24.PUB` for publication; `C.29` and `C.2.P.DR` for representation and declarative-form overread; `A.6.5` for `SlotSpec` declaration and participant-designation discipline; `A.6.RSIR`, `A.6.F`, `A.6.P`, `E.10`, and `E.10.ARCH` for bounded ambiguity repair; and `F.18` for naming after the governed value is settled.
- **Coordinates with:** `A.6.RCD` when the missing piece is a relation-bearing claim that no current direct predicate closes. A local compound claim or predicate-definition episteme is neither a relation kind nor an occurrence; only a separately justified kind candidate proceeds through `E.24` and `E.24.UK`. It also coordinates with `E.17.0` for actual view membership; `A.1`, `B.1`, `B.2`, `A.14`, and `C.13` for a surviving constructed-whole question; `A.3.4`, `A.15.1`, the temporal patterns, and `C.28` for actual change, work, temporal, and causal claims; `A.6.0` and `C.29` for formal-substrate and mathematical-lens use; `C.22.PFR`, `C.22.2`, `E.18.1`, and `E.23` for actual Problem, problem-side formulation, and later problematization; `A.19` for `U.CharacteristicSpace`; and `A.19.ECS` for evaluation-characteristic construction.
- **Used by:** DRRs and authoring work that must decide whether a recurring construct uses an existing subject pattern, remains one or several bounded epistemes, becomes a local typed projection, applies description or publication handling, receives wording repair, opens E.24, or remains unresolved.


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/E-24#root, spec://ai.lev/fpf-spec/contract/E-24-UK#root, spec://ai.lev/fpf-spec/contract/C-2-1#root, spec://ai.lev/fpf-spec/contract/C-3#root, spec://ai.lev/fpf-spec/contract/C-3-1#root, spec://ai.lev/fpf-spec/contract/C-3-2#root, spec://ai.lev/fpf-spec/contract/E-24-PUB#root, spec://ai.lev/fpf-spec/contract/C-29#root, spec://ai.lev/fpf-spec/contract/C-2-P-DR#root, spec://ai.lev/fpf-spec/contract/A-6-5#root, spec://ai.lev/fpf-spec/contract/A-6-RSIR#root, spec://ai.lev/fpf-spec/contract/A-6-F#root, spec://ai.lev/fpf-spec/contract/A-6-P#root, spec://ai.lev/fpf-spec/contract/E-10#root, spec://ai.lev/fpf-spec/contract/E-10-ARCH#root, spec://ai.lev/fpf-spec/contract/E-10-ROLE#root, spec://ai.lev/fpf-spec/contract/F-18#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/A-6-RCD#root, spec://ai.lev/fpf-spec/contract/E-17-0#root, spec://ai.lev/fpf-spec/contract/A-1#root, spec://ai.lev/fpf-spec/contract/B-1#root, spec://ai.lev/fpf-spec/contract/B-2#root, spec://ai.lev/fpf-spec/contract/A-14#root, spec://ai.lev/fpf-spec/contract/C-13#root, spec://ai.lev/fpf-spec/contract/A-3-4#root, spec://ai.lev/fpf-spec/contract/A-15-1#root, spec://ai.lev/fpf-spec/contract/C-28#root, spec://ai.lev/fpf-spec/contract/A-6-0#root, spec://ai.lev/fpf-spec/contract/C-22-PFR#root, spec://ai.lev/fpf-spec/contract/C-22-2#root, spec://ai.lev/fpf-spec/contract/E-18-1#root, spec://ai.lev/fpf-spec/contract/E-23#root, spec://ai.lev/fpf-spec/contract/A-19#root, spec://ai.lev/fpf-spec/contract/A-19-ECS#root, spec://ai.lev/fpf-spec/contract/F-19#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/E-10#root, spec://ai.lev/fpf-spec/contract/E-10-ARCH#root, spec://ai.lev/fpf-spec/contract/E-24#root, spec://ai.lev/fpf-spec/contract/E-24-PUB#root, spec://ai.lev/fpf-spec/contract/E-24-UK#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/E-24-CD
