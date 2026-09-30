# A.3.1.MR - Candidate-Method Recovery from Work Evidence: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## A.3.1.MR:5 - Archetypal Grounding {#archetypal-grounding}

### A.3.1.MR:5.1 - Pump-inspection recovery {#pump-inspection-recovery}

Four independently grounded pump-inspection Work occurrences have video, sensor logs, technician notes, and known performer assignments. Three show the same inspection order. The fourth begins with a vibration cue and reverses two checks.

An analyst applying the recovery Method distinguishes two possible reusable ways under the plant's current inspection vocabulary: a fixed order with an undocumented exception, and a cue-responsive order. Each candidate gets its own account episteme, candidate subject, interpretation scheme, and source-to-claim support. The account notes that the video misses a tactile check named in interviews and that successful outcomes alone do not distinguish the candidates.

A fifth occurrence is held out. Whether the technician changes order when the vibration cue is present can separate the accounts. Until then, both remain candidates; neither trace nor account is a MethodDescription.

If that held-out occurrence and the remaining evidence support the cue-responsive account while the fixed-order rival no longer fits, recovery can return one candidate account ready for the `A.3.1` identity test.


### A.3.1.MR:5.2 - Process-mining replay {#process-mining-replay}

The same team names its event-data preparation Method: select inspection start and completion events from the source files, name activities under the plant vocabulary, correlate records by pump and maintenance visit, and collapse duplicate sensor bursts under a stated rule. It cites the selected configuration because that configuration affects the result. Dated preparation Work on the named files produces an event-log episteme about the selected event-data collection.

If the correlation key, configuration, or source window cannot be recovered, the result is that limitation—not a raw-fact log. A separately named discovery Method returns a behavioural-model episteme with observed variants. Candidate-Method recovery then adds the two candidate reusable-way accounts, the missing tactile contribution, the record-only branch, and the fifth-occurrence question.

### A.3.1.MR:5.3 - Record-only lowering {#record-only-lowering}

Three timestamped records show that one operator checked A before B on three shifts, but the performer assignments, applicability, source window, and purpose of the sequence cannot be grounded. The useful result is an observed sequence in those records and a list of missing facts. It is not a candidate Method account, Method, or MethodDescription.

### A.3.1.MR:5.4 - A current account without another investigation {#a-current-account-without-another-investigation}

In a constructed continuation of the pump-inspection case, the supervisor needs only to compare the two candidate explanations against the four existing records before deciding how to organize the instruction material. The fixed-order and cue-responsive accounts, their separate subjects, source support and missing tactile contribution are enough for that limited comparison. Both remain provisional. No new question, fifth visit or research plan is needed to complete the requested account.

If the receiving use changes to deciding whether to retain the fixed inspection order when a vibration cue is present, the cue response becomes a load-bearing distinction. State the question and preserve the unresolved boundary even when a fifth visit is unavailable. Select an actual investigation only if a suitable performer, source access, permission and window make useful discrimination worth its whole burden. Neither the useful question nor an available plan admits a Method or supplies an observed answer.

## A.3.1.MR:6 - Bias-Annotation {#bias-annotation}

- **Automation bias:** admitting a Method from a mined or executable model without testing the reusable way under A.3.1.
- **Frequency bias:** repeated order is evidence to examine, not a reusable Method part by count alone.
- **Success bias:** favorable outcomes without failed or atypical cases may hide the real limits of the reusable way.
- **Record bias:** unrecorded perceptual, embodied, conversational, and discretionary contributions remain possible gaps.
- **Single-tradition bias:** process mining, routine dynamics, interviews, and Method Engineering each expose different evidence limits; none alone is sufficient for complete reconstruction.
- **Template-completion bias:** unsupported account positions remain unknown rather than being completed from familiar practice.

## A.3.1.MR:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Repair |
| --- | --- |
| “The common sequence is the Method.” | Recover applicability, participant meanings, intended result, variation, limits, rivals, and missing contributions first. |
| “The mined model is the MethodDescription.” | Keep the model as a claim-bearing result about selected evidence until one Method is admitted and the episteme passes `A.3.2`. |
| “Several candidates form one concern.” | Return one account per candidate; create a separate comparison subject only for a named use. |
| “One expert performance proves the reusable way.” | Use it to open a hypothesis; seek several grounded occurrences or lower the result. |
| “The log is raw fact.” | Name preparation Method, configuration, source, dated Work, correlation, encoding, window, and resulting event-log episteme. |
| “Unknown means fill the standard field.” | Keep unsupported positions unknown and preserve their use limits. Add a distinguishing question only when it changes the receiving use; a missing field does not commission evidence collection. |
| “Every recovery needs a full study.” | Stop at the smallest source-traceable candidate or record-only result; enter `ME.18` only for specialist reconstruction. |

## A.3.1.MR:10 - Rationale {#rationale}

This pattern fills the smallest transdisciplinary gap between evidence about Work and identification of a reusable Method. A candidate account is an episteme about one provisionally distinguished possible reusable way. Method identity and MethodDescription membership remain later, separate judgments.

The one-account-per-candidate rule protects episteme subject truthfulness when evidence underdetermines the reusable way. The record-only branch protects utility when evidence is too weak. The specialist exit keeps ordinary recovery usable while preserving the larger evidence burden for domains that need it.

## A.3.1.MR:11 - SoTA-Echoing {#sota-echoing}

| Source line and status, qualified 2026-08-26 | Contribution | FPF adoption |
| --- | --- | --- |
| Feldman and Pentland, [*Routine dynamics: Toward a critical conversation*](https://journals.sagepub.com/doi/10.1177/14761270221130876) (2022) | Separates particular performances from enduring or emergent patterns and keeps variation visible. | **Adopt the performance/pattern distinction.** Repeated Work can support a candidate account without itself becoming the Method. |
| Stacey et al., [*Methods as a form of engineering knowledge*](https://www.cambridge.org/core/journals/design-science/article/methods-as-a-form-of-engineering-knowledge/D126E520FCE6935C3DCBA703F89C24E4) | Distinguishes descriptive reconstruction from prescriptive method content and shows why the distinction can be difficult to maintain. | **Adopt the candidate-account rule.** Coherent description does not establish Method admission or MethodDescription membership. |
| Mature process-mining reference: [*Process Mining Handbook*](https://doi.org/10.1007/978-3-031-08848-3) (2022); current exchange-format boundary: [OCEL 2.0 semantics and the 2.1 serialization revision](https://www.ocel-standard.org/specification/overview/) | Supplies preparation, discovery, conformance, enhancement, and multi-object event representation capabilities. | **Adopt as well-scoped evidence Methods.** Event extraction, naming, correlation, object identity, encoding, abstraction, windows, and serialization remain modeling choices; mining alone establishes no applicability, intention, authority, tacit contribution, causal value, or Method identity. |
| Current object-centric recovery alternatives: [Adams et al., *Defining Cases and Variants for Object-Centric Event Data*](https://arxiv.org/abs/2208.03235) and [Küsters and van der Aalst, *OCPQ*](https://arxiv.org/abs/2506.11541) | Real event data may relate one event to several objects; selecting one case key or flattening can discard information, while queries and constraints produce use-bounded results. | **Adopt the anti-flattening consequence.** Preserve the multi-object evidence and state the selected grouping, query, or constraint when it changes the candidate account. A graph-shaped execution, query result, or constraint result is still evidence or an episteme, not the reusable Method. |
| Current FPF `C.2.1`, `A.3.1`, `A.3.2`, and `A.15.1` | Separates episteme identity, Method identity, MethodDescription membership, and performed Work. | **Adopt directly.** Return one truthful candidate-account episteme per candidate and keep all later admissions separate. |



## A.3.1.MR:End {#end}
