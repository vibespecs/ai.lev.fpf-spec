# A.3.1.MR - Candidate-Method Recovery from Work Evidence {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Architectural (A)
> **Status:** Stable
> **Normativity:** Normative unless marked informative

**Plain name.** Recover source-traceable candidate accounts of a reusable way from several performances or other direct evidence.

**Primary reader.** A practitioner, researcher, analyst, or method engineer who has observations or records from several performances and needs a reusable explanation before Method identification or specialist reconstruction.

## A.3.1.MR:1 - Problem frame {#problem-frame}

**Use this when.** Use this pattern when you have observations or records from several performances and want to understand what reusable way they may show, but no Method has yet been established.

**First useful result.** Return a traceable provisional explanation of the reusable way the material may show, its real rivals, important gaps and limits—or state that the material shows only what happened. A distinguishing question is included when it changes the intended recovery or downstream use; neither an answerable future test nor an investigation plan is required merely to finish the account.

**Three recognition cases.**

- Several maintenance visits have videos, logs, notes, and known performers. Most show one inspection order, while one changes order after a vibration cue. The question is whether the evidence supports a fixed-order way, a cue-responsive way, or only a local sequence.
- Event data has been prepared and a discovery tool has produced a behavioural model. The question is what the selected data and modeling choices actually support, including what embodied, discretionary, or unrecorded contributions may be missing.
- Several practitioners describe “the same practice,” but their accounts still differ in applicability, participant meanings, intended result, or stop. The question is whether one candidate reusable way, several candidates, or no reusable account can yet be distinguished.

**What goes wrong if missed.** One vivid occurrence is generalized into a Method. Repeated event order is treated as reusable applicability. Several rival candidate subjects are combined into one false EntityOfConcern. A mined model, executable diagram, or coherent account is called a MethodDescription before a Method has been admitted. Missing tacit or discretionary contributions disappear behind the record format.

**What this buys.** A project can use imperfect evidence without overclaiming. Each positive candidate has a truthful subject, source-to-claim trace and important limits, with real rivals or unresolved ambiguity preserved. A useful distinguishing question remains separate from a commitment to investigate it. Weak evidence can return a useful record-only result; specialist `ME.18` follows only when its larger contribution is needed.

**Not this pattern when.** Use the closest applicable pattern instead:

- If the evidence no longer leaves rival candidate ways and the remaining question is whether the proposed way qualifies as the `U.Method` being identified—or which identity claim needs repair—use `A.3.1`.
- If the Method is already identified and the question is whether an episteme is its MethodDescription, use `A.3.2`.
- If wording still hides the object or relation being asserted, use `F.19`; follow an `E.10` route only for a remaining FPF word, kind, or relation question.
- If the question concerns one dated Work occurrence only, use `A.15.1`.
- If the project needs prospective practice-architecture synthesis, use `C.32.MWA`.
- If the domain needs a complete reconstruction programme, use specialist `ME.18`.

**When a DPF reuses this pattern.** A DPF uses it only when several occurrences or sources create a candidate-recovery question that passes this entry. The DPF still supplies any domain-specific problem, evidence limits, vocabulary, result, and return that change practitioner action or judgment. If no such use-changing contribution remains, cite this pattern rather than copying it.

For example, an engineering study across several test runs may pass this entry, while a live maintenance incident may need only `A.15.7` and a stable administrative checklist may need neither pattern. A music or dance DPF uses this recovery Method only for an actual several-performance question and keeps its own evidence, terminology, result, and return.


## A.3.1.MR:2 - Problem {#problem}

Evidence about Work is not the reusable way itself. Videos, logs, interviews, artifacts, and process models are selected and interpreted under Methods. They may omit perception, conversation, manual adjustment, authority, intent, failure, or local workarounds. Several observations may support more than one reusable explanation, and a coherent explanation can still be wrong.

The practical gap lies between two existing results. `A.15.1` can identify what Work occurred and which Method it enacted when that claim is independently grounded. `A.3.1` can identify a reusable `U.Method` once its meaning, scope, and limits are supportable. Neither supplies the several-occurrence recovery Method needed before Method admission. Without that intermediate result, projects either jump from record to Method or import a full specialist reconstruction programme into every case.

## A.3.1.MR:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Reuse versus historical truth | The project seeks a reusable way, while every source first says something about particular Work or evidence construction. |
| Coherence versus underdetermination | One neat account is useful, but several accounts may fit the same observations. |
| Traceability versus tacit contribution | Sources must support each claim, yet important perceptual, embodied, conversational, or discretionary contributions may not be recorded. |
| Useful grain versus false detail | The receiving use may need one broad reusable way or a safety-critical branch; the evidence should not force the wrong grain. |
| Discovery power versus modeling choice | Process-mining tools can reveal patterns, but event extraction, naming, correlation, abstraction, and windows shape the result. |
| Provisional identity versus Method admission | A candidate reusable way needs enough identity to be discussed, without being admitted prematurely as `U.Method`. |
| Common minimum versus specialist burden | Every domain needs source-to-claim recovery and lowering; complete sampling, elicitation, integration, and trials belong in specialist Method Engineering. |

## A.3.1.MR:4 - Solution {#solution}

For every materially different reusable way that still fits the evidence, write a separate candidate account. Treat each account as one `U.Episteme`, keep it provisional until `A.3.1` admits the candidate as a Method, and keep MethodDescription membership separate until the account concerns that admitted Method and passes `A.3.2`.

### A.3.1.MR:4.1 - Identify each candidate account truthfully {#identify-each-candidate-account-truthfully}

Each positive candidate account is one `U.Episteme`. Before Method admission, distinguish the possible reusable way as one provisionally identified candidate entity: give it a working designation and enough source-supported participant meanings, applicability hypothesis, intended result or preserved condition, variation, and limits to tell it from rivals. That candidate entity is the account's `EntityOfConcern`.

The account's effective `U.ReferenceScheme` states only the designation and interpretation rules needed to read source terms such as performer, activity, cue, event, result, and stop. Add measurement or comparison rules only when the account uses them. This provisional entity identification admits neither a `U.Method` nor a `U.MethodDescription`.

When two or more candidate reusable ways still fit the evidence, return one account episteme per candidate. Each account may mention the rivals while retaining its own `EntityOfConcern`. If a later use needs a comparison that can be retained or reused, use `A.22` to select the candidate subjects and the comparison relations that already hold and together define one comparison structure, then return a separate episteme about that structure. Otherwise compare them in ordinary working prose. Several candidates do not by themselves form one subject for a combined account.

If no candidate entity or truthful effective scheme can be recovered, lower the result rather than fabricating an account.

### A.3.1.MR:4.2 - Run the nine-step recovery Method {#run-the-nine-step-recovery-method}

1. **State the receiving use and useful grain.** Say why a reusable Method is being sought and which later action or decision would change. Do not reconstruct a fine sequence when the use needs one broad way, or a broad routine when a safety-critical branch must remain explicit.
2. **Name several grounded occurrences or other direct evidence.** For every claimed Work occurrence, recover each precise performer's A.13 core and independently admit the Work under A.15.1. Add F.6 only when the candidate account also needs precise assignment-bound attribution. Keep sources such as videos, logs, notebooks, interviews, artifacts, measurements, and assertions as separate entities or epistemes with their actual evidence relations. One occurrence may open a hypothesis; it does not establish reusable applicability.
3. **Write what each source supports.** Keep a readable source-to-claim account of performer Systems, relevant facts, enacted-Method claims when independently grounded, actions, cues, variations, results, and stops.
4. **Expose how evidence was constructed and what it misses.** State which performers, objects, successful, failed, or atypical occurrences were observable and which contributions—such as embodied perception, conversation, manual adjustment, discretion, or tacit know-how—may be absent. For event data, name the preparation Method, relied-on description or configuration, source data, dated preparation Work, resulting event-log episteme, the identified event-data collection or structure that the log describes, and the interpretation scheme. If a relied-on Method, configuration, source, correlation key, event-state encoding, or observation window is unavailable, return that limit before mining.
5. **Distinguish each candidate subject.** For every materially different possible reusable way, state the provisional identity and scheme from §4.1. If two candidates cannot be told apart without unsupported claims, retain the ambiguity or lower the result.
6. **Write one account per candidate.** Ask the `A.3.1` questions without granting Method membership: applicability, participant meanings, preconditions, intended result or preserved condition, reusable actions, supported parts or interfaces, allowed variation, and stops. Mark every unsupported position unknown rather than filling a familiar template.
7. **Compare stability, variation, and alternatives.** Ask what recurs across independently grounded occurrences, what changes with the situation, what may be a performer-specific habit or local workaround, and whether another account explains the same evidence. Frequency alone establishes neither a Method part nor its value.
8. **State a distinguishing question when it changes use.** If separating, repairing or lowering the candidates matters to the receiving use, identify the meaningful difference and the representative occurrence, trial, comparison or additional source that could expose it. A held-out question preserves its independence from account construction. The question need not be answerable now and is not a study commitment. A source-traceable provisional account can finish without designing unavailable or irrelevant follow-up. Separately select investigation only when its attainable contribution warrants its whole design, acquisition, interpretation and displaced-Work burden.
9. **Return the strongest evidence-supported result.** Return one or more candidate accounts ready for `A.3.1` identification or specialist work, with a separate comparison only when needed; or lower to a Work-related record, local regularity, performer-specific habit, observed sequence, or unresolved cue. Prepare MethodDescription-authoring input separately. The same account can qualify as `U.MethodDescription` only after its `EntityOfConcern` is admitted as one `U.Method` and its claims pass `A.3.2`.

### A.3.1.MR:4.3 - Select the result branch {#select-the-result-branch}

| Evidence state | Result |
| --- | --- |
| Several occurrences support one reusable account at the required grain, with visible source limits | One source-traceable candidate-account episteme about one independently distinguished possible reusable way. No answerable held-out question is required unless that answer is needed by the receiving claim. |
| Several accounts still explain the observations | One account episteme per candidate with source support, gaps and real ambiguity; add a distinguishing question only when it changes recovery or downstream use, and a separate comparison episteme only for a named retained use. |
| The material shows only what happened or one local regularity | A Work-related record, local regularity, observed sequence, or habit claim; no Method or MethodDescription. |
| Candidate identity, scheme, Work occurrence, source support, or evidence construction cannot be grounded | The missing information, relation, Method, configuration, source, or interpretation rule and the blocked receiving use. |

### A.3.1.MR:4.4 - Keep process-mining contributions separate {#keep-process-mining-contributions-separate}

Treat evidence preparation, process discovery, and candidate-Method recovery as three contributions.

1. Named data-preparation Method or Methods select source events, name activities, correlate records and objects, choose event-state or start/complete encodings, and apply abstraction. Dated preparation Work uses named source data and produces an event-log episteme about the identified event-data collection or structure described by the log.
2. A named discovery Method may return a behavioural-model episteme. Conformance checking may compare a log with a separate descriptive or normative model. Enhancement may add timing, organizational, performance, or prediction claims. Object-centric mining may preserve several typed objects and qualified relations.
3. This recovery Method uses those well-scoped results with other evidence to return candidate reusable-way accounts, unrecorded contributions, lowering and a distinguishing question only when it changes the intended use.

None of the earlier contributions automatically recovers a Method. A discovered process model remains a `U.Episteme` about selected evidence unless another rule establishes a different kind or use. A conformance result relates a log and model; it does not prove that the model describes the obtaining Method or that every deviation is defective. Executability and visual process form do not satisfy `A.3.2`.

Treat *process*, *actual process*, *case*, *activity*, *event*, *variant*, *deviation*, and *process model* as cues to recover the direct subject, not as types supplied by the words. Use `E.10` and `A.15.6` when the source remains ambiguous.

### A.3.1.MR:4.5 - Stop or continue to specialist Method Engineering {#stop-or-continue-to-specialist-method-engineering}

Stop here when the receiving use needs only a source-traceable candidate account, a comparison, or a record-only result. Continue to specialist `ME.18` when the domain and consequence require a reconstruction programme—for example, sampling across performers and settings, interviews, cognitive task analysis, ethnography, protocol analysis, process-mining design, artifact analysis, tacit-contribution recovery, fragment composition, domain trial design, or stronger assurance.

`ME.18` may strengthen the candidate accounts and prepare separate inputs for MethodDescription authoring. Use `A.3.1` for Method identification and `A.3.2` for MethodDescription membership.

## A.3.1.MR:7 - Conformance Checklist {#conformance-checklist}

- @fact:CC-A3-1-MR-1 **CC-A3.1.MR-1 — Receiving use and grain.** Is the later use clear enough to choose the useful reconstruction grain? @status:spec/done
- @fact:CC-A3-1-MR-2 **CC-A3.1.MR-2 — Grounded evidence.** Are claimed Work occurrences and other sources identified under their own patterns and relations? @status:spec/done
- @fact:CC-A3-1-MR-3 **CC-A3.1.MR-3 — Source-to-claim trace.** Can the reader see which source supports each account claim? @status:spec/done
- @fact:CC-A3-1-MR-4 **CC-A3.1.MR-4 — Evidence construction.** Are selection, naming, correlation, abstraction, configuration, window, and likely missing contributions explicit when they matter? @status:spec/done
- @fact:CC-A3-1-MR-5 **CC-A3.1.MR-5 — One candidate per account.** Does every candidate-account episteme have one candidate reusable-way EntityOfConcern and effective scheme? @status:spec/done
- @fact:CC-A3-1-MR-6 **CC-A3.1.MR-6 — Rival retained.** Are real competing accounts or unresolved ambiguity visible without inventing a rival to complete the form? @status:spec/done
- @fact:CC-A3-1-MR-7 **CC-A3.1.MR-7 — Useful distinguishing question.** Where discrimination changes recovery or downstream use, is the question clear and, if held out, independent of account construction? Does the account remain usable when no answerable investigation is needed or available, with stronger dependent claims withheld? @status:spec/done
- @fact:CC-A3-1-MR-8 **CC-A3.1.MR-8 — Result branch.** Does the result stop at candidate account, separate comparison, record-only result, or named blocker without granting Method or MethodDescription membership? @status:spec/done
- @fact:CC-A3-1-MR-9 **CC-A3.1.MR-9 — Specialist exit.** Is `ME.18` used for complete reconstruction only when the receiving use needs its larger burden? @status:spec/done
- @fact:CC-A3-1-MR-10 **CC-A3.1.MR-10 — Plain use.** Can a cold practitioner explain the candidate, evidence, real rivals, gaps and supported current use without a mandatory next-test plan? @status:spec/done

## A.3.1.MR:9 - Consequences {#consequences}

| Benefit | Cost or caution |
| --- | --- |
| Several imperfect sources can support a useful provisional account. | Every account claim must remain traceable to its supporting sources. State the evidence-construction Method and choices when they affect reliance on those sources; retain the event-data requirements of §4.2. |
| Rival accounts remain visible instead of being averaged into one false subject. | A project may have to carry several candidates until discriminating evidence arrives. |
| Process mining becomes a well-scoped contribution rather than an ontological shortcut. | Preparation and discovery choices must be exposed when the account relies on them. |
| Record-only evidence still returns a useful result. | The user must resist promoting a coherent sequence to a Method by form or frequency. |
| Specialist Method Engineering receives source-traceable candidate accounts. | Complete reconstruction remains a separate, sometimes costly programme. |

## A.3.1.MR:12 - Relations {#relations}

- **Builds on:** `C.2.1` for each account episteme, its EntityOfConcern, and effective scheme; `A.3.1` for the questions that shape a candidate without granting Method membership; A.13 for each precise performer's local agency core; `A.15.1` for independent admission of grounded Work occurrences; F.6 only for a current precise assignment-bound attribution; and `A.10` for bounded source reliance.
- **Coordinates with:** `A.3.2` for later MethodDescription membership; `A.15.6` for ambiguous process or case wording; `A.22` for a separately selected comparison structure only when needed; `C.32.MWA` for prospective several-structure practice synthesis; and `C.11.DUA` when a questionable investigation demand needs appraisal of its attainable contribution and whole burden.
- **Receives bounded evidence from:** process-data preparation, discovery, conformance, enhancement, object-centric mining, interviews, observations, artifacts, and measurements under their own Methods and claims.
- **Hands off to:** `A.3.1` for Method identification or specialist `ME.18` for complete reconstruction; neither continuation is automatic.
- **Keeps separate:** source, record, event log, behavioural model, Work, candidate reusable way, candidate account, admitted Method, MethodDescription, and any comparison episteme.


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/C-2-1#root, spec://ai.lev/fpf-spec/contract/A-3-1#root, spec://ai.lev/fpf-spec/contract/A-15-1#root, spec://ai.lev/fpf-spec/contract/A-10#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/A-3-2#root, spec://ai.lev/fpf-spec/contract/A-15-6#root, spec://ai.lev/fpf-spec/contract/C-32-MWA#root, specialist spec://ai.lev/fpf-eng-me/contract/ME-18#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-eng-mdpe/contract/MDPE-18#root, spec://ai.lev/fpf-eng-me/contract/ME-18#root, spec://ai.lev/fpf-eng-ops/contract/OPS-16#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/A-3-1-MR
