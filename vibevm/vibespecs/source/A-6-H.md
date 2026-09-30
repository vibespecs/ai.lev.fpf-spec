# A.6.H - Wholeness Language Unpacking — RPR-WHOLE: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## A.6.H:5 - Archetypal Grounding {#archetypal-grounding}

### A.6.H:5.1 - Assembled pump {#assembled-pump}

Source sentence: “After seal replacement, the assembled pump remains an integral whole.”

1. The subject is `PumpUnit-37`, not the maintenance record, drawing, or seal-replacement Work.
2. The pump's direct identity rule decides whether the same individual continued.
3. The current use names the pump boundary, impeller, casing, replacement seal, and the exact assembly or parthood relations on which operation depends.
4. If the decision consumes one selected organization of those relations, A.22 governs that structure; if it consumes a construction account, C.13 reports already recovered facts.
5. A.1 recognizes the candidate whole; B.2 opens only if the replacement leaves a genuine whole-reidentification question.
6. For calibration, seal replacement, and inspection, identify any actual Work under A.15.1 and state any claimed change separately under the rule for the changed object.

### A.6.H:5.2 - Laboratory pipeline {#laboratory-pipeline}

Source sentence: “The whole chromatography pipeline is turnkey, and the chemist owns the whole thing.”

The repair separates the following claims and unresolved questions; `turnkey` and `owns` still need the receiving decision and discriminating facts:

- the reusable procedure is one exact Method or composite Method under A.3.1/B.1.5, with exact joins and exposed interactions;
- its procedure document is a separate `U.MethodDescription` episteme under C.2.1/A.3.2;
- “turnkey” becomes the exact specification, capability, Work, or evidence coverage claim needed by the receiving use;
- treat *owns* as a local wording cue. First state the decision that depends on it and the exact proposed sentence. Candidate readings include, for example, property or title, possession or custody, operational control, decision authority, stewardship or responsibility, assignment, commitment, and permission; they have different participants and predicates. Apply the direct rule when one exists, or return A.6.RCD `missing-governor[...]` naming the participants, proposed predicate, affected use, and absent definition; and
- an actual laboratory run is dated Work under A.15.1.

Thus “the laboratory owns the instrument,” “the chemist has custody during the run,” “the chemist may authorize disposal,” and “the chemist is responsible for calibration” are four different claims. None follows from belonging to the team, classification, assignment, commitment, or permission merely by form.

No one claim is a component relation merely because the source uses *pipeline* or *whole*.

### A.6.H:5.3 - Paper, proof, and revision {#paper-proof-and-revision}

Source sentence: “Section 3 is part of the proof, and v2 is part of v1.”

- Recover whether Section 3 is a constituent of the paper episteme, a publication-unit constituent, or a described proof step. Keep those subjects separate.
- Recover argument order under its subject pattern rather than as physical containment.
- Compare the exact C.2.1 triples for the two labelled epistemes. Changed claim content identifies two epistemes. Assert `EpistemeEditionRelation(E_v1,E_v2)` only when its historical-continuation predicate obtains.
- If one unchanged episteme is needed only during a proper interval, `PhaseOf(E@τ,E)` may state that restriction. It does not connect v1 to v2.
- Keep any drafting, review, or publication Work separate from publication occurrences and from the two epistemes that participate in `EpistemeEditionRelation`.

### A.6.H:5.4 - Integrity measurement and assurance {#integrity-measurement-and-assurance}

Source sentence: “The structural integrity score is 0.82, so the system is assured.”

First recover the bearer, integrity Characteristic, Scale, measurement method, result episteme, evidence, and time stance under C.16.P/C.16. For “the system is assured”, name the exact target claim and assurance use before applying B.3; then recover the evidence-use relation, scope, limitations, and relying context. The score alone does not establish that assurance result.

## A.6.H:6 - Recognition and assurance stay separate {#recognition-and-assurance-stay-separate}

**Recognition questions** decide which objects and direct relations are current:

- Is there one candidate whole under A.1?
- Which independently identified parts, constituents, members, portions, or temporal restrictions participate?
- Which direct relations obtain?
- Does a selected structure or construction account matter to this use?
- Does the same whole persist, or is reidentification current?

**Evidence-use questions** under A.10 decide what the evidence supports for the stated relying use:

- Which claim is being supported?
- Which evidence bears on it through which relation?
- What scope, limitation, time stance, and relying use apply?
- Does the evidence support recognition, relation truth, measurement, completion, or another claim?

Apply B.3 only when an actual named assurance claim and assurance use are current. Evidence can make an assertion inspectable without becoming constitutive of the whole or relation.

## A.6.H:6.1 - Bias-Annotation {#bias-annotation}

- **Governance bias.** The pattern favors reviewable direct claims over rhetorically satisfying wholeness language. Ordinary prose and explicit unresolved alternatives mitigate this when a decision is not yet due.
- **Architecture bias.** Use the applicable patterns and small typed vocabularies instead of one reusable wholeness schema. The minimum-current-object rule mitigates unnecessary apparatus.
- **Ontological/epistemic bias.** It insists on separating referent, episteme, publication, Method, plan, Work, and evidence. This cost is paid only when the distinction changes the receiving use.
- **Pragmatic bias.** It favors early disambiguation to avoid downstream refactoring. A local direct sentence is sufficient; reusable declarations or structures are added only for a named later use.
- **Didactic bias.** It uses recurring cue words and worked cases to teach the route; `F.19` governs the connected language-and-precision reading, with `E.10` cues and direct wording rules where needed.

## A.6.H:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Failure | Repair |
| --- | --- | --- |
| Holistic-as-evasion | “We took a holistic view” replaces the actual decision, subject, boundary, or relation. | Name the receiving use and exact claim, or remove the load-bearing assertion. |
| Universal part-of | Components, constituents, members, portions, phases, Method factors, and Work parts share one edge. | Recover each object and direct predicate under its subject pattern. |
| Record-as-whole | A `wholenessSituation`, bundle, BoM, graph, or trace is treated as the whole or relation. | Recover the candidate entity, independently grounded facts, exact assertion and predicate, and the subject pattern only as its ClaimGraph locator. |
| Structure-as-sequence | Method order or plan order becomes containment. | Recover exact Methods and order/join claims under B.1.5/B.1.4; keep Work separate. |
| Version-as-phase | Different epistemes are called phases of one document lineage. | Apply the C.2.1 identity triple, then test `EpistemeEditionRelation` independently. |
| Work-phase shortcut | Shift, monitoring window, episode, retry, or resumption uses generic `PhaseOf`. | Apply A.15.1's exact temporal-part, episode, operational-part, retry, resumption, or occurrence rule. |
| Integrity-as-wholeness | A measurement, security property, report, or assurance claim is forced through parts and boundary. | Use the four-way integrity classification in 4.3. |
| Completeness-by-rhetoric | “Turnkey” or “end-to-end” supplies no covered set, scope, criterion, or subject pattern. | State the exact specification, capability, Work, evidence, construction, or completion claim. |
| Description/referent drift | The same noun alternates among a system, model episteme, document, carrier, plan, and Work. | Name each current subject and its direct relation. |
| Generic change narration | A new change verb replaces the changed object and predicate. | State the exact boundary, relation, episteme, publication, Method, Work, or coverage change. |

## A.6.H:10 - Rationale {#rationale}

Wholeness language is useful because it compresses boundary, identity, relation, construction, coverage, and assurance into ordinary speech. The same compression becomes dangerous only when downstream work relies on one particular reading.

The minimal repair is an exact-object sequence that starts with the working decision, recovers only the objects that decision consumes, and applies another rule only for a still-current concrete question. This preserves conversational economy while preventing a representation, record, label, or adjective from replacing an in-world object or relation.

The sequence also preserves two positive uses. `PhaseOf` remains valid for a proper restriction of one unchanged enduring individual, including one unchanged episteme when its C.2.1 identity triple is fixed. And ordinary whole recognition remains useful when an exact candidate entity, boundary, parts, relations, and direct identity rule are genuinely current.

## A.6.H:11 - SoTA-Echoing {#sota-echoing}

| Source tradition | Current practice used here | Local adoption | Rejected shortcut |
| --- | --- | --- | --- |
| [ISO/IEC/IEEE 42010:2022](https://www.iso.org/standard/74393.html), architecture-description practice | Distinguish the entity of interest from its description and make concerns, viewpoints, environment, and boundary explicit. | Recover the candidate referent and boundary before treating a description or publication as evidence about it. | A view, diagram, or architecture document is the system whole or establishes its parts. |
| [ISO/IEC 21838-2:2021](https://www.iso.org/standard/74572.html), upper-ontology discipline | BFO distinguishes continuant parthood from occurrent parthood; its temporal parthood has occurrent domain and range. | FPF's A.14 makes a local choice: proper temporal restriction of one unchanged enduring individual, including an unchanged episteme, under its direct identity and relation tests. This differs from BFO temporal parthood and supplies no episteme-edition or Work shorthand. | One universal part edge or lifecycle object covers components, versions, and Work. |
| [ArchiMate 3.2](https://www.opengroup.org/sites/default/files/docs/downloads/n221p.pdf), enterprise-architecture relation practice | Different structural and behavioral relations answer different questions. | Use the source vocabulary as a comparison aid while retaining FPF subject patterns and occurrence rules. | A modelling-language edge label establishes the in-world FPF relation. |
| [Team Topologies](https://teamtopologies.com/), sociotechnical boundary practice | Team boundaries, interaction modes, and cognitive load affect organization and flow. | Treat team and ownership wording as cues. Recover the claim actually made using the distinctions in §5.2, and use A.6.RCD only when no current pattern defines the needed predicate. | A team boundary or a list of who belongs to the team establishes no ownership, responsibility, assignment, or Work by itself. |
| ISO/IEC/IEEE 29148:2018, requirements quality | Requirements should identify the item, condition, and verifiable claim without referent/document ambiguity. | Require exact subjects, scopes, predicates, and blocked overreads on load-bearing surfaces. | A specification sentence becomes true or complete because the document is complete-looking. |
| [NIST SP 800-53 Rev. 5](https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final), security and privacy controls | Integrity claims depend on exact information, constraints, threats, controls, assessment, and evidence. | Recover the data/security integrity characteristic, measurement, evaluation, or assurance question and apply its rule before any structural-whole reading. | Every occurrence of *integrity* means wholeness or mereological coherence. |

Whenever *fraction*, *percentage*, or *share* is used as a part claim, recover the extensive measure μ and additivity basis before `PortionOf`; otherwise keep the value with the pattern that defines its measurement, allocation, collection belonging, or other actual claim.


## A.6.H:End {#end}
