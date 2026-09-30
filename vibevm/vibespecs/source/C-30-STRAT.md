# C.30.STRAT - Clarify Stratification and Architecture Source Labels: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## C.30.STRAT:5 - Archetypal Grounding {#archetypal-grounding}

| Template element | `U.System` illustration | `U.Episteme` illustration |
| --- | --- | --- |
| Source-label cue | A neural-network source says an `expert block` sits above a `router layer`. | A publication note says a `cache layer` keeps a diagram or view current. |
| Recovery result | The words stay source labels until module, function, path-selection, flow, or selected-structure facts become clear. | The words stay source labels until publication, view, state, currentness, temporal, or ordinary non-use facts become clear. |
| Next move | Use `A.6.M`, `A.6.F`, E.18, C.30.TFS-REL, G.5, or C.11 only for the recovered claim. | Use the episteme/publication route in C.30.STRAT:4.2, or A.19.SPR, A.3.3, C.27.TA, or C.27 only for the recovered claim. |

## C.30.STRAT:6 - Bias-Annotation {#bias-annotation}

Lenses: **Arch**, **Onto and Epist**, **Prag**, **Did**, and **Gov**. The pattern deliberately resists word-shape inference. Its counter-bias is equally important: ordinary prose stays ordinary, a known meaning uses its pattern directly, and the author-facing routing coordinates never become a project form.

## C.30.STRAT:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Symptom | Repair |
| --- | --- | --- |
| Source label as ontology | `layer`, `block`, `expert`, `cache`, or `gate` is treated as a kind by name. | Recover the actual object or relation, or keep ordinary source wording. |
| C.30 takeover | Every structure-like word is treated as an architecture claim. | Choose from the recovered meaning; use the rule for the actual control, module, flow, scale, publication, state, evidence, work, or decision claim. |
| Standard-label overreach | A standard or popular model uses `layer` or `level`, so its local convention is treated as a universal subject structure. | Preserve the convention inside its declared source use; state and test any wider object, relation, mapping, or architecture claim separately. |
| Controlled-language purge | A preferred-word rule deletes a clear domain term or replaces it with formal apparatus although no reader action was at risk. | Keep the term; repair only the ambiguity that changes use, using the shortest direct sentence. |
| Level by layout | A list, vertical diagram, first-then flow, carrier section, curriculum, scale label, stage sequence, or coarse-grained description is treated as a subject stratification. | Keep the wording local, or name the subject, say what is being ordered, compared, grouped, or mapped and how, state when the claim applies, and mark it as asserted, proposed, assumed, or illustrative; then use the pattern that defines or tests that claim. |
| Local trigger fanout | C.30.LCA, A.6.M, C.31, or another pattern copies this label catalogue. | Keep one thin pointer here and the other pattern's own invariant there. |
| Expert-as-role false positive | `expert` in mixture-of-experts prose becomes a system-role kind, assignment, performer, Work, responsibility, or authority by word alone. | First test submodel, transformation, path selection, candidate selection, or ordinary non-use. If a claim-bearing use of *role* remains, use E.10.ROLE; identify each claimed system-role kind, classification judgment, assignment occurrence, performer System, or Work occurrence under its direct pattern; assert a responsibility, authority, or other relation only when its defining predicate independently obtains. |
| Gate-as-decision false positive | A gating function, UI label, or source word becomes gate passage. | Use A.20 or A.21 only for actual constraint-validity or gate-decision claims; otherwise use the applicable function, flow, publication, or ordinary-label result. |

## C.30.STRAT:10 - Rationale {#rationale}

Stratification words compress local practice. That compression is useful for recognition and unsafe as a substitute for an object, relation, or claim. C.30.STRAT therefore keeps the source word, recovers what it means in the current sentence, and returns the reader to the applicable technical rule.

## C.30.STRAT:11 - SoTA-Echoing {#sota-echoing}

Standard status, publication date, and wide use do not by themselves show that an approach moves the relevant Pareto front. The comparison below adopts only contributions that recover a technical claim more reliably without making ordinary project language harder to use. The compact combination in this pattern—cheap exit, source-local meaning, recovered claim, next useful rule, stop or return condition, and any justified blocked overread—is FPF synthesis.

| Current source or practice | By-value decision | Contribution carried into this pattern | Limit and receiving loci |
| --- | --- | --- | --- |
| [ISO 704:2022, *Terminology work — Principles and methods*](https://www.iso.org/standard/79077.html) | Current published terminology-work standard checked 2026-08-22. **Adapt:** distinguish objects, concepts, definitions, and designations before standardizing a term; do not require a terminological entry for every ordinary sentence. | Treat `layer`, `level`, `gate`, and their neighbours first as designations in a bounded source use. Recover the object, relation, or claim before choosing a technical pattern. | A designation is not the thing or claim it helps name. Applied in recovery steps 2-4, the cue table, CC-C30STRAT-1/10, and the standard-label anti-pattern. |
| [ISO/IEC/IEEE 42010:2022, *Architecture description*](https://www.iso.org/standard/74393.html) | Current published architecture-description standard checked 2026-08-22. **Adopt narrowly:** distinguish an entity's architecture from an architecture description and recover the viewpoint or model-kind convention used by the description. **Reject:** using this standard as a system ontology, architecting Method, or proof that a described layer exists in the world. | When a label occurs in an architecture description, recover first what the description element means in its declared model or viewpoint; state separately any world-side structure or relation the sentence claims. | Architecture-description conformance is not architecture truth. Applied in recovery steps 3-5, the architecture-description worked case, the level-claim boundary, and CC-C30STRAT-11. |
| [ASD-STE100 Issue 9 (2025), *Simplified Technical English*](https://www.asd-ste100.org/) and its [scope explanation](https://www.asd-ste100.org/about_STE.html) | Current maintained controlled natural language checked 2026-08-22. **Adapt:** use short direct sentences and disambiguate a word when misunderstanding changes action; preserve subject-specific nouns and verbs. **Reject:** applying its controlled dictionary as a universal FPF vocabulary or deleting clear domain terms by lexical rule. | Keep the cheap exit and shortest direct repair; split compressed claims; preserve an already clear source-local technical term. | Controlled-language conformance cannot choose ontology and is not needed for every prose use. Applied in recovery steps 2 and 6, CC-C30STRAT-8/12, and the controlled-language-purge anti-pattern. |
| Current FPF `E.10`, `E.10.ARCH`, `F.18`, `F.19`, and the direct subject patterns | Current local architecture. **Adopt:** F.19 ordinary rewrite, E.10 cues, ontology-first recovery, direct source-local naming, and return to the pattern that defines or tests the recovered claim. | One short repair states recovered meaning, allowed use, next action, stop or return condition, and any blocked overread justified through F.19; author-facing routing stays out of ordinary project work. | This composition is the novel FPF synthesis. It must be reopened when a selected external source or a direct subject pattern supplies a better low-burden repair. Applied throughout Solution, Grounding, checklist, and Relations. |

Reopen only the affected cue, worked case, check, or pointer when a source changes. Reopen the wider pattern when a current approach demonstrates a meaning-recovery method that is more reliable at comparable reader effort, or when repeated use shows that the present cue table either misses consequential readings or sends clear ordinary language through unnecessary formal repair.


## C.30.STRAT:End {#end}
