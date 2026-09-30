# A.6.3.NAR - Structure-to-Narrative Rendering: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## A.6.3.NAR:5 - Archetypal Grounding {#archetypal-grounding}

Tell: NAR turns selected source structure into a reader-useful sequence while keeping ordering, loss, unsupported strengthening, and source return visible. It is not a general story-writing pattern.

### A.6.3.NAR:5.1 - Scientific mechanism narrative {#scientific-mechanism-narrative}

A chemistry paper has calculations, candidate mechanisms, failed synthesis attempts, and an unresolved tension between theory and experiment. For an internal explanation, the first useful result is a discovery-ordered account: failed attempts, structural clue, revised mechanism, new experiment, remaining uncertainty. Its compact note says that candidate relations and failed attempts are preserved, full calculations are deferred, connective claims are not proof, and mechanism-proof use returns to the calculations and experiment record.

If a published account must travel independently, be cited or disputed as a stable account, or support consequential reliance, open the exact branch. Mere publication of a source-linked low-reliance explanation does not require it. Source episteme `ChemistryMechanism-X` states the relevant claims about the reaction case; receiving episteme `ChemistryDiscovery-Y` concerns the same case. `DiscoveryNarrativization : X -> Y` records the exact selection, scheme relation, discovery order, preserved and lost claims, prohibited proof overread, and return. Calculation files are not `X`; the paper form and carrier are not `Y`.

### A.6.3.NAR:5.2 - Architecture trade-off narrative {#architecture-trade-off-narrative}

An architecture team needs to explain why one candidate structure was selected. It first writes a tension-ordered account: current pain, candidate split, data-custody and placement constraints, characteristic trade-off, rejected alternatives, selected structure, and remaining residual. For team orientation, the note identifies the architecture description or decision material, what alternatives are omitted, and that implementation authority remains outside the narrative.

If this account will guide a design decision or travel as architecture rationale, exact source episteme `ArchitectureTradeoff-X` and exact receiving narrative episteme `ArchitectureRationale-Y` concern the same project system. `ArchitectureRationaleNarrativization : X -> Y` records the exact construction and source return. Candidate structures remain independently identified A.22 objects designated by source claims, not source endpoints. The posture is prospective during choice and retrospective during reconstruction; publication, decision, synthesis, and performed Work remain separate.

### A.6.3.NAR:5.2.1 - Architecture narrative repair after source change {#architecture-narrative-repair-after-source-change}

Later, a rejected candidate gains a new measurement basis and a placement constraint changes. The old story remains coherent but no longer preserves the live candidate set. Lower it to historical orientation, update the selected structures and ordering, state the changed loss and residual, and restore return to the current architecture description or decision material. In an exact case, reidentify only source epistemes whose C.2.1 identity changed, and restate the affected construction `n` under A.6.3.

C.33 carries captured and lost architecture-relevant structures: preserve the old rejected-candidate relation as history, capture the new candidate-set relation, and mark the obsolete measurement basis lost for current decision use. C.34 carries only a correspondence that actually remains. Implementation or decision use stays non-admissible until the exact architecture claim, decision result, or synthesis result and any required use relation are current.

### A.6.3.NAR:5.2.2 - Live unfolding event narrative {#live-unfolding-event-narrative}

A commentator narrates a football match while it unfolds. The ordinary narrative selects score state, possession changes, tactical shape, player roles and positions, momentum, and uncertainty, then uses event and tension order for live orientation. Here *player roles* is ordinary football language for tactical contribution and behaviour—such as pressing, covering, marking, playmaking, or providing width—not an asserted FPF system-role kind or assignment. The narrative does not turn provisional interpretation into settled event evidence.

Later analysis, statistics, rule disputes, injuries, or official-result use returns to the event record and official sources. If the commentary itself must be replayed, cited, or disputed, an exact case identifies the live event-record episteme `MatchState-X`, commentary episteme `LiveNarrative-Y`, and `LiveNarrativization : MatchState-X -> LiveNarrative-Y`; the match and event stream are not `X`, and audio is a form or carrier rather than `Y`.

### A.6.3.NAR:5.3 - FPF seminar-route boundary {#fpf-seminar-route-boundary}

A team orders selected FPF claims for learners: EntityOfConcern discipline, problem frames, pattern use, relation records, source return, framework authoring, and improvement loops. The first result is a teachable route whose note records prerequisite order, deferred detail, reconstruction tasks, and return to exact FPF passages.

Teaching these claims does not establish that FPF is correct. A separate E.24.PUB occurrence may make a selected narrative episteme available through a teaching form and carrier; publication neither constitutes the narrative episteme nor establishes the NAR construction.

### A.6.3.NAR:5.4 - Franchise-continuation storycraft boundary {#franchise-continuation-storycraft-boundary}

A storycraft team selects continuity constraints, premise, theme, character-agency treatment, causal plot structure, viewpoint, stakes, and return points from an admitted canon or local source pack, then orders them into a proposed continuation. NAR records selection, order, foregrounding, loss, and source return; it does not turn storycraft vocabulary into FPF Core.

If an exact continuity claim must travel, `CanonSelection-X` and `ContinuationNarrative-Y` are independently identified and `ContinuationNarrativization : CanonSelection-X -> ContinuationNarrative-Y` states the exact construction. Canon classification, generation method, rights, publication, and full narrative-quality evaluation stay outside NAR. Use G.2 for SoTA source-pack synthesis, C.35 for generated results intended to inform architecturing, and the relevant agency, responsibility, evidence, and publication tests for those separate claims.

### A.6.3.NAR:5.5 - Homotopy-theory explanation boundary {#homotopy-theory-explanation-boundary}

A teacher turns graph-heavy mathematical material into a didactic sequence of definitions, dependencies, examples, counterexamples, theorem prerequisites, and proof-status boundaries. The ordinary note records which structures a learner can reconstruct, which proof details or generalizations are deferred, and when to return to formal statements. Recalling an analogy alone does not establish a proof or recovery of the mathematical structure being taught.

If the explanation is cited as a stable mathematical account, exact source episteme `HomotopySource-X` and receiving episteme `HomotopyNarrative-Y` concern the same mathematical EntityOfConcern; the construction records ordering and visible loss. For mathematical-lens, proof, source-use, evidence, publication, and teaching-evaluation claims, use the patterns that define or test those exact claims.

### A.6.3.NAR:5.6 - Automated event-graph narrative {#automated-event-graph-narrative}

An LLM or NLG system uses source claims designating an event graph, agent goals, constraints, and a domain schema, then performs generation Work and proposes the resulting story-scene carrier. The first inspection compares the proposed sequence with the selected event relations, marks preserved constraints, omissions, and hallucinated connective claims, and limits use to candidate review.

Generated prose is not an admitted narrative episteme merely because it is fluent. Use C.35 when the generated result is intended to inform architecturing; it tests that exact result's next architecture use. If reliance-facing use later opens exact NAR, independently identify `EventPlan-X` and `StoryScene-Y`, then state `EventNarrativization : EventPlan-X -> StoryScene-Y`, the additional source chain, loss, prohibited strengthening, and return. The graph and schema are not `X`; the system's generation Work, evidence, assurance, and publication remain separate.

## A.6.3.NAR:6 - Bias-Annotation {#bias-annotation}

| Bias | How NAR counters it |
| --- | --- |
| Story-substitution bias | Requires selected source structure, visible loss, bounded use, and source return before the narrative is relied on. |
| Formality-first bias | Produces a useful narrative and source comparison without opening an exact identity record that the receiving use does not need. |
| Engagement-authority bias | Treats engagement as a bounded use claim; evidence, assurance, ethics, and policy force remain with the patterns that define those claims. |
| Sequence-naturalization bias | Makes the ordering and connective account explicit instead of letting a fluent order look inevitable or source-given. |
| Carrier-serialization bias | Keeps file export, stream order, OCR, and layout changes outside NAR unless selected source structure is actually ordered into a narrative path. |
| Generated-fluency bias | Keeps generated output as candidate material until source comparison and any independently required admission pass. |
| Narratology-import bias | Keeps narratology and storycraft detail in domain practice instead of creating automatic FPF Core kinds. |

## A.6.3.NAR:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | What fails | Repair move |
| --- | --- | --- |
| Identity dossier before narrative | Ordinary teaching or orientation stalls before anyone receives a useful account. | Draft the smallest reader-useful sequence and source comparison first; open exact identity only when a named receiving use triggers it. |
| Good story as source replacement | The narrative is memorable, but later users cannot recover the selected source structure. | Add the compact note or exact case appropriate to the use: selected structures, preservation/loss, bounded use, and source return. |
| Tacit selection as narrative success | The author or model picked structures, but no one can explain why they serve this reader. | Reconstruct the selection rationale and reader-use hypothesis; keep the output orientation-only until they are clear. |
| Sequence by habit | Chronology, textbook order, or dramatic order is used without saying why it helps or what it hides. | State the ordering/connective account and compare it with the source. |
| Engagement as evidence | Attention, transportation, or emotional uptake is treated as stronger truth or permission. | Keep engagement as a bounded use effect; use A.10, B.3, or D.1–D.5 only for the specific evidence, assurance, or ethics claim. |
| Narratology word import | Plot, focalization, voice, protagonist, suspense, or narrator are treated as automatic Core kinds. | Keep domain vocabulary in narrative practice unless a separate Core decision admits a reusable distinction. |
| Generated narrative by fluency | LLM output is accepted because it reads coherently. | Compare it with admitted source claims, use C.35 when the generated result is intended to inform architecturing, and open exact NAR only if the receiving use requires it. |


## A.6.3.NAR:10 - Rationale {#rationale}

Narrative makes non-linear structure usable by giving readers a path through events, mechanisms, evidence, options, architecture decisions, or prerequisites. That strength is also the risk: a well-formed story can make a source look simpler, more certain, more complete, or more permissible than it is.

The narrow reusable move is therefore reader-first and progressive. Choose structure for a use, order it, connect it, draft the account, and expose loss and return. Exact `n : X -> Y` is the stronger description of that move when a receiving use needs claim-level identity; it is not the entrance fee for every explanation.

## A.6.3.NAR:11 - SoTA-Echoing {#sota-echoing}

| Exact source or practice anchor | Adopt, adapt, or reject | Contribution to NAR use | Boundary and currentness |
| --- | --- | --- | --- |
| Roald Hoffmann, “The Tensions of Scientific Storytelling” (American Scientist, 2014) | Adopt as practice grounding: scientific narratives order calculations, failed attempts, mechanisms, unresolved tensions, and discoveries rather than merely decorating results. | Grounds the discovery-order worked case and the need to retain unresolved tension and source return. | Historical practice anchor, not current cognitive SoTA or authority over FPF ethics. |
| Wolf Schmid, `Narratology: An Introduction` (2010), and Matei Chihaia, `Introductions to Narratology: Theory, Practice and the Afterlife of Structuralism` (2012) | Adapt source material, selection, composition, order, viewpoint, and presentation as domain distinctions. | Grounds the ordering/connective account and viewpoint-sensitive loss. | Historical domain anchors; fiction-specific vocabulary does not become FPF Core ontology. |
| Tan T. Nguyen, “A Review of Mechanistic Models of Event Comprehension” (2024); Lijuan Chen and Xiaodong Xu, “Neural and Behavioral Evidence for Differential Processing of Narrative Perspective in Novel Reading” (2026); Christoph Mengelkamp, Stefanie Golke, and Markus Appel, “Effects of Reading Goal Instructions on the Comprehension and Metacomprehension of Informative Narratives” (2025); Antonios Georgiou, Tankut Can, Mikhail Katkov, and Misha Tsodyks, “Large-scale study of human memory for meaningful narratives” (2025) | Adopt as current cognitive pressure for event models, prediction and update, reading-goal effects, reconstruction, memory loss, metacomprehension error, and viewpoint-sensitive recovery. | Supports triggered event-model/viewpoint fields, reader-use entry, source comparison, and return. | These studies inform narrative use; they do not supply evidence, assurance, ethics, or policy authority for a particular narrative. |
| Albert Gatt and Emiel Krahmer, “Survey of the State of the Art in Natural Language Generation” (2018); Amal Alabdulkarim, Siyan Li, and Xiangyu Peng, “Automatic Story Generation: Challenges and Attempts” (2021); Rogelio E. Cardona-Rivera, Arnav Jhala, Julie Porteous, and R. Michael Young, “The Story So Far on Narrative Planning” (2024); Vikram Kumaran, Jonathan Rowe, Bradford Mott, and James Lester, “SceneCraft: Automating Interactive Narrative Scene Generation in Digital Games with Large Language Models” (2023), DOI `10.1609/aiide.v19i1.27504`; Yuan Ma, Richard Susilo, Patrik Haslum, and Hanna Suominen, “Text-to-Text Automatic Story Generation: A Survey” (2026); Aynigar Rahman, Aihe Yu, and Kyungeun Cho, “Game Knowledge Management System: Schema-Governed LLM Pipeline for Executable Narrative Generation in RPGs” (2026) | Adopt content and narrative planning, grounding, controllability, schema constraints, repair, and evaluation limits for automated cases. | Grounds the generated event-graph case, generated-fluency boundary, source comparison, and conditional C.35 architecture-use exit. | The 2018/2021 surveys are historical anchors; the 2024/2026 planning, survey, and schema-governed work represents the current line used here. |
| Melanie C. Green and Timothy C. Brock, “The Role of Transportation in the Persuasiveness of Public Narratives” (2000); Michael F. Dahlstrom and Shirley S. Ho, “Ethical Considerations of Using Narrative to Communicate Science” (2012); Hanna Meretoja, “Narrative and Human Existence: Ontology, Epistemology, and Ethics” (2014, background only); FPF `D.1` through `D.5` | Adapt engagement as a real effect with a bounded-use and ethical boundary. | Grounds the engagement check and the anti-pattern against treating engagement as evidence or permission. | Historical/background anchors. Current evidence, assurance, ethics, and policy claims still require their own exact sources and FPF patterns. |


## A.6.3.NAR:End {#end}
