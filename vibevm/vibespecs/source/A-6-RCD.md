# A.6.RCD - Needed Relation Claim Derivation and Relation-Kind Admission: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## A.6.RCD:5 - Archetypal Grounding — Worked Cases {#archetypal-grounding-worked-cases}

### A.6.RCD:5.1 - Promise-content fulfilment: use the existing direct A.2.3 predicate {#promise-content-fulfilment-use-the-existing-direct-a-2-3}

**Situation.** `PromiseContent_Housing42_v3` says that exact housing `Housing_42` must be delivered to `AssemblyCell_B` during `Interval_42`, satisfy `OutcomeSpec_Housing42_v3`, and satisfy the acceptance predicate in `AcceptanceSpec_Housing42_v3`. The actual delivery work is the independently identified `U.Work` occurrence `Work_DeliverHousing42`; it is not the delivered entity, the post-delivery state, the evaluation, or the acceptance result.

**A.2.3 predicate and required subset.** A.2.3 already supplies the direct predicate `fulfilsPromiseContent(W, SC)`, so disposition 1 is available. For this exact promise-content edition, the necessary and sufficient world-side subset is:

1. `PromiseContentUse(Work_DeliverHousing42, PromiseContent_Housing42_v3, Interval_42)` obtains;
2. `PromisedOutcomeDeliveryRelation(Work_DeliverHousing42, OutcomeSpec_Housing42_v3)` obtains because the selected work facts, exact delivered entity `Housing_42`, and its post-delivery state satisfy that OutcomeSpec; and
3. the acceptance predicate in `AcceptanceSpec_Housing42_v3` is satisfied for those exact facts and states.

No production or entity-inception claim is current because `Housing_42` already existed before this delivery work. This edition requires no additional generic transfer or institutional-acceptance relation beyond the two A.2.3 relations and its acceptance predicate. If another edition requires one, it must name that exact direct relation and its participants rather than adding a `delivery work` bundle.

**Evaluation, result, and evidence.** Separate evaluation work `Work_InspectHousing42` applies the declared acceptance method. Its exact operation-result binding carries the verdict value; optional episteme `InspectionVerdict_Housing42` states that evaluation result. An A.10 evidence-use relation may support reliance on the affirmative fulfilment assertion. The evaluation work, result binding, verdict episteme, and evidence-use relation neither become parts of `Work_DeliverHousing42` nor make `PromiseContentFulfilmentRelation` obtain. The three world-side conditions above make the direct relation obtain; evaluation and evidence only support an assertion about it.

**Positive case.** All three required conditions above are satisfied, so the direct predicate is satisfied and a claim-bearing episteme may state `fulfilsPromiseContent(Work_DeliverHousing42, PromiseContent_Housing42_v3)` without creating the occurrence.

**Discriminating failures.** `Work_DeliverHousing42` can occur and `Housing_42` can be in the target post-state while `PromiseContentUse` is absent or concerns another promise edition; then `PromisedOutcomeDeliveryRelation` for this promised outcome does not obtain and the promise is not fulfilled. Or the delivery relation can obtain while one acceptance condition is false; an `accepted` label or report cannot repair that failure. Missing evidence leaves reliance on the assertion unresolved; it creates neither fulfilment nor non-fulfilment.

**Disposition and stop.** Stop at disposition 1 under A.2.3. No new compound-law episteme, predicate definition, relation kind, or `RelationSignature` is needed. Use A.6.REL only if a later use must distinguish this fulfilment occurrence from another occurrence of the same admitted relation.

### A.6.RCD:5.2 - System-role assignment and performed Work: recover A.13 and A.15.1 first, then use F.6 directly when attribution is current {#system-role-assignment-and-performed-work-recover-a-13-and-a-15}

**Situation.** A work record needs the readable claim that one actual system performed one exact Work occurrence under one exact assignment to a system role.

**Base and direct result.** Recover `S : U.System` as the exact actual performer through A.13 and let A.15.1 independently admit exact `W : U.Work`. When the work record expressly needs the under-assignment claim, reuse the same obtaining A.13 assignment `RA`, apply F.6 to the direct predicate `performedUnderAssignment(W, RA)`, and compare `RA.HolderSystemSlot` with the already recovered `S`. F.6 identifies neither assignment nor performer. A C.2.1 episteme may assert that result for the receiving use. The system performs the Work; the assignment supplies its holder and assigned-kind projection but neither acts nor creates another participation relation. If F.6 is missing or fails, retain the Work and remove only the under-assignment claim.

**Positive case.** A.13 has already recovered `S` through the same obtaining `RA`, A.15.1 has independently admitted `W`, `RA` covers `W`, `RA.HolderSystemSlot = S`, and F.6's direct Work-attribution predicate holds for the exact pair. The readable result is “S performed W under RA.” No generic enactment object is needed.

**Discriminating failure.** The assignment obtains, but another system performs the Work, or `S` performs Work outside the assignment's extent. Assignment plus nearby Work is insufficient; capability, responsibility, authority, and a result also remain separate claims.

**Disposition and stop.** Stop at disposition 1 under A.2.1 and F.6. Admit no `RoleEnactment` kind, compound relation, occurrence, or `RelationSignature`. If a later use needs another participation or functioning relation in addition to Work attribution, name its direct predicate or return that exact missing governor instead of generalizing from *enacted*.

### A.6.RCD:5.3 - Supply-chain reachability: subject-bounded query or reusable predicate definition {#supply-chain-reachability-subject-bounded-query-or-reusable}

**Situation.** One planner asks whether `Supplier_A` can reach `Plant_B` inside `SupplyNetwork_North_2026`. Other planners want the same directed-reachability rule for independently identified supply-network structures.

**Base and derivation.** Name the direct edge-relation kinds, direction, structure parameter, source and target parameters, path or closure rule, zero-length and cycle policies, applicability, and edge-definition editions. A one-off answer is a local compound claim. Repeated queries only about `SupplyNetwork_North_2026` may use a subject-bounded compound-law episteme whose `EntityOfConcern` is that exact structure and whose reuse boundary excludes other structures. When the same parameterized rule is reused across independently identified structures, publish `DirectedReachabilityPredicate_v1` as a predicate-definition episteme whose `EntityOfConcern` is that exact reusable definition. If its claim graph supplies A.6.0's subject and value range, Vocabulary, Laws, and Applicability, it may independently satisfy ordinary `U.Signature` membership without becoming a `RelationSignature`.

**Positive case.** A path exists whose every edge is an obtaining occurrence of the admitted base relation under the selected structure and closure rule.

**Discriminating failure.** A graph representation contains a visual or stored path, but one edge points in the wrong direction, denotes a different base relation, or belongs to a superseded structure edition. Representation connectivity therefore does not satisfy the reachability predicate.

**Disposition and stop.** The one-off query stops at disposition 2. Repeated use confined to one exact structure stops at disposition 3's subject-bounded branch. Cross-structure reuse stops at disposition 3's reusable predicate-definition branch and may add ordinary A.6.0 `U.Signature` membership. If a subject practice later needs reachability occurrences with action-facing identity, recurrence, continuation, or participation in another relation, the A.6.RCD application records a derived reachability-kind candidate plus a proposed direct subject settlement; apply the E.24 and E.24.UK admission tests and the A.11 parsimony test when current. Create a `RelationSignature` only for an admitted relation kind. Path identity, query-result-row identity, predicate-definition identity, subject-structure identity, and relation-occurrence identity are not interchangeable.

### A.6.RCD:5.4 - Formal and probabilistic result use: preserve separate algebras {#formal-and-probabilistic-result-use-preserve-separate-algebras}

**Situation.** One engineering decision-work occurrence consumes one formal result episteme and one probabilistic result episteme.

**Base and derivation.** Keep the formal result in its formal substrate and the probabilistic result in its probability substrate. State the two result-use assertions under their exact predicates in one `C.2.1` episteme whose exact `EntityOfConcern` is the engineering decision-work occurrence. The formal and probabilistic result epistemes remain distinct used results; neither their pair nor a union of nearby objects replaces that concern.

No F.9 Bridge is needed for this case as stated: the two result epistemes enter the decision through separate direct use relations, and no obtaining relation between two exact F.17 cells is claimed. No ReferencePlane crossing is claimed either, so no plane relation or policy is added. Either fact could later become current without creating the other.

**Positive case.** Both direct use relations obtain for the decision-work occurrence under their own applicability, so the decision rationale can cite each result for its admitted use.

**Discriminating failure.** The two results are co-published or mention the same subject, but the decision work has no current direct use relation to one of them. Shared carrier, topic, or notation does not establish decision use.

**Disposition and stop.** The apparent combined need decomposes into two independently stated receiving claims. Each closes under disposition 1 with its exact direct decision-use relation. Do not publish a cross-algebra conjunction predicate merely to join the sentences, and do not infer one composite relation occurrence from a decision record.

### A.6.RCD:5.5 - Primitive-candidate stop test {#primitive-candidate-stop-test}

A subject practice proposes a primitive relation because all accepted bases preserve co-occurrence and shared participants but lose one independently used subject distinction. The candidate advances only when the subject can name that lost distinction, show a positive and discriminating case, state its own obtaining and recurrence laws, distinguish repeated occurrences, and identify independent receiving uses. If any item is missing, the honest result is a local claim, reusable predicate definition, or exact blocker. This is disposition 4's positive test, not a license to mint a placeholder relation.

## A.6.RCD:6 - Bias-Annotation {#bias-annotation}
Lenses tested: **Gov**, **Arch**, **Onto/Epist**, **Prag**, **Did**. Scope: **Universal** for applications of this pattern across FPF subject practices.

This pattern corrects primitive-kind bias: a useful repeated phrase or representation can look ontologically important before its exact claim and occurrence semantics are recovered. It also corrects false-parsimony bias: if every accepted derivation loses a distinction that changes real work and the subject supplies its own obtaining and identity laws, refusing the primitive would hide needed ontology.

The formal examples can bias authors toward syntax-first reasoning. The method therefore begins from the blocked receiving use, direct participants, and direct relations. The ordinary branch stays readable; formal apparatus appears only when it changes replay, reuse, proof, interoperability, or admission.

## A.6.RCD:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Anti-pattern | Failure | Repair |
| --- | --- | --- |
| `RelatedTo` as a universal fallback | Vague wording substitutes for participants and predicate. | Name the blocked use and derive the smallest exact claim. |
| Formula-as-fact | A formula tree or theorem token is treated as predicate satisfaction. | Recover the claim and its applicability; keep the formula under `C.29`. |
| Query-path ontology | A path match is treated as an obtaining relation occurrence. | Separate base-edge obtaining, closure semantics, query result, and any later occurrence identity. |
| Definition-as-kind | A reusable episteme is treated as a classifier of occurrences. | Keep its one `EntityOfConcern` and claim content; run separate derived-kind admission only for an occurrence-semantics need. |
| Kind-by-name | A good relation name is treated as admission evidence. | Use `F.18` only after the exact definition episteme, kind, or occurrence is settled. |
| Identity intentionally absent | An admitted kind has truth conditions but no occurrence identity because current prose does not expose occurrences. | Supply the direct identity rule or remain at claim or definition level. |
| Universal constructor algebra | Restriction, negation, closure, probability, and cross-algebra conjunction are assumed to mean the same thing everywhere. | Use only operators supplied by the selected substrate; return a blocker otherwise. |
| Hidden intermediate erased | Projection removes an intermediate from notation and therefore from semantics. | State the shared participant and witness policy even when the receiving claim projects it away. |
| Cross-algebra conjunction | Formal and probabilistic results are merged because one decision uses both. | Keep each algebra and direct decision-use relation separate. |
| Primitive by exhaustion | Failure to find a derivation is treated as proof of irreducibility. | Record the searched admitted base, exact lost distinction, positive and failure cases, and direct identity law; otherwise keep an exact blocker. |

## A.6.RCD:10 - Rationale {#rationale}

Claim composition and relation-kind admission answer different engineering questions. A claim asks whether an exact predicate, possibly built from admitted base predicates, is satisfied for named referents. A relation kind classifies obtaining occurrences and therefore needs a rule for reidentifying those occurrences. Repetition of the first question can justify publication of the predicate rule; it does not answer the second.

The demand-first order is deliberately asymmetric. Existing direct relations are cheapest because their admitted definitions already state obtaining and identity. Local compound claims preserve expressive reach without public ontology cost. Predicate-definition epistemes prevent repeated derivations from drifting. Derived relation kinds add occurrence semantics only where named uses consume them. Primitive relation kinds remain available for irreducible distinctions rather than being prohibited by abstract minimalism.

## A.6.RCD:11 - SoTA-Echoing {#sota-echoing}

| Practice or source line | What this pattern uses | What it rejects or bounds |
| --- | --- | --- |
| W3C [OWL 2 Structural Specification](https://www.w3.org/TR/owl2-syntax/) inverse object properties and property-chain axioms | Typed inverse and composition examples constrain the substrate-authority test in 4.2 and the supply-chain reachability case in 5.3: direction, shared participants, and the selected chain law remain explicit. | An OWL axiom neither establishes FPF equivalence nor supplies world-side obtaining or occurrence identity; case 5.3 still stops at a local claim or predicate definition unless the subject practice separately supplies occurrence semantics. |
| [Alloy language reference](https://alloytools.org/spec.html) relational restriction, transpose, join, product, union, difference, and closure | This mature explicit-operator substrate constrains 4.2 and the supply-chain reachability replay in 5.3, including direction, closure, zero-length, and cycle policy. | Alloy syntax is not a universal FPF constructor algebra and does not admit relation kinds; case 5.3's kind branch remains stopped until a direct subject practice supplies action-facing occurrence semantics and identity. |
| W3C [SPARQL 1.1 Property Paths](https://www.w3.org/TR/sparql11-property-paths/) | Query-local path and closure semantics for the reachability worked case. | A successful path query is not an obtaining relation occurrence and its result-row identity is not occurrence identity. |
| Florio and Linnebo, [Introduction to Constructional Ontology](https://www.utwente.nl/en/eemcs/fois2024/resources/papers/florio-linnebo-introduction-to-constructional-ontology.pdf), 2024, and Borgo and Righetti, [Towards Applied Constructional Ontology](https://doi.org/10.3233/FAIA250480), 2025 | Their constructor, input, process, and output-identity distinctions are adapted as a discriminating probe for the occurrence-semantics gate in 4.6 and the primitive-candidate stop in 5.5: authors MUST state in the candidate's direct subject rule which construction is identity-bearing. | A construction description or inherited source category neither constitutes FPF work or a relation occurrence nor admits a relation kind; 5.5 remains stopped until the direct subject practice supplies its own obtaining and identity law. |
| Chris Partridge, [BORO Ontology](https://borosolutions.net/boro-ontology), C-FORS 2025 presentation; current bounded extensional comparator | Its temporal-extent, recurrence, and ontology-evolution pressure is adapted for the occurrence-identity requirements in 4.6 and the primitive-candidate stop in 5.5: a temporal gap distinguishes repeated occurrences only when the direct subject rule adopts that discriminator. | FPF rejects universal 4D identity, unrestricted composition, and BORO category architecture. Reopen this bounded comparison if a later BORO edition or a direct FPF identity rule changes whether temporal extent is action-relevant for the 4.6/5.5 stop. |
| Almeida, Guizzardi, Sales, and Fonseca, [gUFO](https://arxiv.org/abs/2603.20948), 2026 preprint relation-reification comparison | Its differentiated relational-aspect and reification patterns stress the object boundary in 4.4 and the occurrence-identity and primitive-candidate stops in 4.6 and 5.5. | FPF adapts those distinctions as a current comparison but rejects an OWL class, property, reifier, or imported category hierarchy as proof of obtaining or occurrence identity; the candidate remains stopped until its direct subject rule supplies both. |

Reopen these source-use decisions when a selected substrate changes its operator semantics, a newer practice invalidates one of the representation boundaries, or a direct FPF relation pattern supplies a more action-capable derivation or identity rule without worse ontology truth, reader use, or modeling cost.

## A.6.RCD:12 - Reopen Conditions {#reopen-conditions}

Reopen the exact affected disposition, not the whole relation foundation, when:

- a base relation definition, participant meaning, obtaining law, or applicability changes;
- a substrate edition changes a constructor used by the claim;
- a local claim recurs enough to need one stable definition;
- a reusable definition gains or loses a truthful single `EntityOfConcern`;
- a named use begins or ceases to need stable occurrence identity;
- an admitted derived kind loses a base dependency or identity rule;
- an admitted primitive gains a lossless derivation or loses its independent action-facing use;
- repeated reader error shows that the definition, kind, occurrence, representation, or designator is being confused.


## A.6.RCD:End {#end}
