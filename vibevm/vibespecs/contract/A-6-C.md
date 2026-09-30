# A.6.C — Contract Unpacking for Boundaries {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Architectural (A)
> **Status:** Stable
> **Normativity:** Normative (unless explicitly marked informative)
> **Placement:** Part A → **A.6 Signature Stack & Boundary Discipline**
> **Builds on:** A.6 (stack + classification intent), **A.6.B** (L/A/D/E), **A.6.P:4.11a** (service/access subject-pattern recovery), **A.7** (EntityOfConcern, Description episteme, and carrier separation), **A.2.3** (`U.PromiseContent`), **A.2.8** (`U.Commitment`), **A.2.8.PER** (strong/weak permission, exercise, and conflict), **A.2.9** (`U.SpeechAct`), **A.15.1** (`U.Work`), **A.10** and **B.3** (evidence and assurance use), E.10 (`L-SERV` and `LEX-BUNDLE`), E.17 (MVPK “no new semantics” faces), F.12 (service acceptance and evidence discipline)
> **Naming boundary:** **F.18** may provide durable names for recovered terms when naming is current; it does not define or constrain the promise-content, speech-act, commitment, permission, work, evidence, or boundary ontology.
> **Vocabulary boundary:** Reuses “contract”, “SLA”, and “guarantee” only as Plain-level source cues. The four questions below are a boundary-language unpacking lens, not a `Contract`, bundle, register-part kind, or rival claim set. The existing A.6.B Claim Register may add `bundleId`, optional `questionRef`, `directObjectDesignation`, `directObjectPatternLocator`, and `faceRefs`; it remains the one atomic-claim record.
> **Purpose (one line):** Resolve consequential ambiguity in boundary contract language through the applicable four questions and atomic claims; use the A.6.B Claim Register only when the receiving use needs a record under §4.5.

**Use this when.** Use `A.6.C` when words such as *contract*, *promise*, *guarantee*, *SLA*, or *interface agreement* leave a consequential ambiguity about what was promised, instituted, governed, performed, produced, delivered, accepted, or evidenced.

**First useful move.** Rewrite the live passage so each asserted object has its actual subject, predicate, operands, and direct governor; apply only the questions that the passage makes live.

**What changes in practice.** Familiar contract language can remain in Plain prose while technical and normative claims become classifiable under `A.6.B` and adjudicable through their direct sources.

**Ordinary non-use boundary.** Clear local contract wording with no consequential ambiguity needs no unpacking record. A one-off repair may end in the repaired atomic prose; create or extend the Claim Register only when stable reuse, decision, audit, dispute, or cross-face projection needs it.

## A.6.C:1 — Problem frame {#problem-frame}

Boundary descriptions frequently use “contract” as shorthand for “the thing that governs the interaction”. That shorthand collapses four practical questions and the separately governed objects needed to answer them:

* **What was promised?** — the exact promise content, if any,
* **What was said, published, or instituted?** — the speech-act Work, descriptions, publication occurrences/forms/carriers, and any separately governed institutional effect,
* **What governance or permission-looking claim exists?** — the one atomic norm, grant, gate, exercise, evaluation, conflict, or source claim selected by its job,
* **What happened, what followed, and what supports reliance?** — dated Work, each separate result or delivery claim, and each evidence claim.

When these questions are answered with one undifferentiated object or row, authors can conflate a semantic guarantee with an undertaking, attribute a dated act to its description instead of its performer, encode runtime gates as if they were internal laws, or treat observability as a property of text rather than of carriers and work. A.6 and A.6.B already provide an L/A/D/E claim-classification discipline for boundary claims, but “contract” language remains a recurring entry point for category mistakes.

**Service-cluster note (modularity + lexicon).** When contract talk co-moves with *service*, *service provider*, *server*, *SLA*, *SLO*, or *service-level* and a relied-on boundary use still hides a concrete subject or relation, recover that hidden choice through **A.6.P:4.11a** while asking the four questions below. Mere co-occurrence does not trigger recovery, and clear, quoted, historical, illustrative, or harmless ordinary wording remains usable. `U.PromiseContent` is written as **promise content**, never as bare “service”.

A.6.C makes contract-language usable inside the A.6 stack by providing a canonical unpacking that can be applied to APIs, hardware interfaces, protocols, and socio-technical boundaries.

**Non‑goals (to preserve modularity).** A.6.C does **not**:
* define “legal contract” doctrine (offer, acceptance, consideration, jurisdictional enforceability, etc.);
* resolve conflicts across scales or contexts: keep the current grant or prohibition as its own D claim, classify the conflict finding as E through A.6 `A6-AW-CONFLICT`, and use the exact mediation predicate and assertion only when mediation is current;
* redefine the core meanings of `U.PromiseContent`, `U.Work`, `U.SpeechAct`, `U.Commitment`, or the exact `A.2.8.PER` results—it only makes “contract talk” classifiable into those objects or claims.
* redefine quadrant semantics (`L/A/D/E`) or cross‑quadrant reference rules; those are defined normatively in A.6.B.

## A.6.C:2 — Problem {#problem}

How can an author write (or repair) contract-language so that:

1. **Act and commitment claims name compatible participants**, without mistaking an interface description for the actual interface or its bearer,
2. **Governance claims** are distinguishable from permission-looking gate, exercise, evaluation, conflict, and source claims by the job of each atomic statement rather than by A.2.8.PER membership,
3. **Operational “guarantees”** become adjudicable by naming the exact Work, evaluation, or observation and its result, with an A.10 evidence path and exact carrier when a receiving decision relies on that support,
4. **Multi-view publication** (MVPK faces) does not create a parallel contract object or rival canonical claim set by paraphrase drift?

## A.6.C:3 — Forces {#forces}

| Force                      | Tension                                                                                                                                           |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| Conversational convenience | People will keep saying “contract”; banning the term is unrealistic.                                                                              |
| Ontological correctness | Familiar contract wording can hide whether a guarantee is semantic, a prescription, an undertaking, or an observed result. |
| Boundary diversity         | Software APIs, hardware connectors, protocols, and SLAs share the “contract” word but differ in what is adjudicated and how.                      |
| Multi-view publication | Faces support audience fit when projection is needed; rephrasing can change the claim. |
| Adjudicability | When “guarantee” or authority wording leaves a consequential ambiguity, recover the semantic truth, exact generic prescription, individual commitment or current grant, entry predicate, or observed/evaluated claim needed by the receiving use. |
| Minimality                 | The unpacking should be lightweight enough to apply during routine authoring and review.                                                          |

## A.6.C:4 — Solution {#solution}

A.6.C introduces a four-question boundary-language lens. It interprets and rewrites contract-like source wording under A.6.B without admitting a `Contract` object or another ontology branch.

### A.6.C:4.1 — Four questions for contract-like boundary wording {#four-questions-for-contract-like-boundary-wording}

When “contract”, “guarantee”, “promise”, “SLA”, or “interface agreement” leaves a consequential ambiguity, ask only the live questions below. A question may yield zero, one, or several atomic claims. Add corresponding rows only when stable reuse, decision, audit, dispute, or cross-face projection needs the Claim Register; the question itself is not a bundle part or direct-object kind.

1. **What was promised?**

   * The promised value or effect (the promise *content*) in the intended scope.
   * In FPF terms (A.2.3), **`U.PromiseContent` is promise content**—a **promise content**, not an execution event (`U.Work`) and not, by itself, an obtaining individual deontic relation (`U.Commitment`).
   * **Prose head rule (normative).** When referring to `U.PromiseContent` in normative prose, authors SHALL use the head phrase **promise content** (or **service offering clause** or **service promise clause**) and SHALL NOT rely on the bare head noun *service*. If the surrounding text also talks about endpoints, systems, and operations, apply **A.6.P:4.11a** only when the current relied-on use still hides which concrete subject or relation is meant; examples include a service access point, service delivery system, or service-delivery Work occurrence. Mere proximity to those words creates no additional claim or recovery duty.
   * **Recommendation:** when commitments, gates, evidence, or MVPK faces need stable citation of the promise content, give it a stable local ID (e.g., `SVC-*`) to prevent paraphrase drift.
   * **Claim-classification discipline:** keep meanings and definitions of the promised behavior in **L**. A generic prescription about that behavior is a separate **D** claim about its exact normative source and applicable rule content. If an actual System or separately governed party has that duty, state a separate **D** claim about the exact `U.Commitment`, plus any `A-*` and `E-*` references needed by that claim.

2. **What was said, published, or instituted?**

   * **Speech-act Work:** if the boundary decision depends on who stated, published, or approved something, identify that exact A.2.9 `U.SpeechAct <: U.Work` occurrence.
   * **Description/publication:** identify the versioned utterance epistemes separately from their publication occurrences, forms, renderings, and carriers. None is the speech act.
   * A speech act **may** institute or update a commitment or strong grant only when the exact context policy recognizes that act type and the subject pattern's obtaining conditions are met.
   * The published utterance descriptions (signature or mechanism descriptions plus MVPK faces) carry L/A/D/E-classified claims. The act is not “the contract”; it is the Work occurrence that created or updated those descriptions and may have a separately governed institutional effect.
   * **World-side obtaining rule (normative).** The predicates defined in A.2.8 and the cited context policy decide whether a commitment obtains; the predicate defined in A.2.8.PER together with that policy decides whether a strong grant obtains. For a commitment, use the actual instituting basis required by its constitutive rule: the current A.2.9 path uses an actual `U.SpeechAct`; another basis requires a subject pattern that admits it and gives its occurrence rule. A strong grant requires the actual instituting speech act under A.2.8.PER. Preserve the participants, scope/window, current policy, and any revocation or supersession conditions. A Claim Register row, utterance description, publication, carrier, or identifier creates or proves neither relation by itself. For a commitment, a cited fact is constitutive only when the identified rule makes that fact current and the pattern for that subject supplies its test. Publication or approval may establish a publication/status relation only through that relation's exact predicate and obtaining facts.
   * **Representation and reliance rule (normative).** The model **MAY assert or rely on** a commitment or grant only through a separate atomic claim that identifies the exact `U.Commitment` or `GrantedPermissionRelation@Context` occurrence and cites its exact predicate, `SubjectPatternLocator`, participants, scope/window, and the currentness or evidence required by that use. For a commitment, cite the rule-required actual instituting basis and policy; for a strong grant, cite the actual instituting speech act and policy. Never infer the relation from `Publish`/`Approve` wording, a document, carrier, or completed-looking record alone.

3. **What governance or permission-looking claim exists?**

   * A generic prescription states what one exact policy or other normative episteme requires; it does not create an individual duty bearer or commitment occurrence. A claim that one actual System or separately governed party has that duty instead cites one separately obtaining A.2.8 `U.Commitment`. Here the normative episteme may be a contract, SLA, protocol, or policy, and the generic claim also states where its rule applies.
   * When the model asserts or relies on an individual obligation, recommendation-as-duty, or prohibition, write a separate atomic D claim whose direct object is that exact separately obtaining `U.Commitment`.
   * For permission-looking wording, select one A.6 `A6-AW-*` row. Only `A6-AW-NORM-GRANT` enters D. Within `A6-AW-GATE`, a mechanism entry predicate enters A and an actual A.21 `GateDecisionResult` enters E; split them into separate atomic claims when both are present. Exercise, weak evaluation, conflict, and observed-source claims enter E when their closing facts are present. Classification under A.2.8.PER alone selects no quadrant.
   * **Individual-commitment checklist (use only for the individual branch):**
     * identify one exact `U.Commitment` occurrence and the separate D-claim or `CommitmentAssertion` about it;
     * select exactly one actual bearer branch: an admitted `U.System` or separately governed party;
     * name non-empty exact duty referents, any actual counterparties, normalized modality, scope, and validity window;
     * cite the exact current constitutive policy, its individualizing rule, and the actual instituting basis required by that rule;
     * cite a system-role assignment only when that rule uses the assignment as an applicability ground—the assignment is neither bearer nor duty; and
     * add evidence-claim or carrier references only when the receiving reliance or adjudication needs them.
   * **Permission-branch pointer:** cite the selected `A6-AW-*` row, its exact A.2.8.PER object when applicable, and that atomic claim's quadrant. Preserve the object's own schema, participants, and references; do not reuse the commitment checklist.
   * A commitment is not “the spec text”: an utterance description carries the statement, while `U.Commitment` is the separately obtaining relation described by that statement (A.7 and A.2.8).
4. **What happened, what followed, and what supports reliance?**

   * **Work:** For one exact dated `W : U.Work`, recover each exact actual performer through A.13 and let A.15.1 independently admit the occurrence from that performer, enacted Method, extent, and containing System. Add an exact A.2.1 assignment reference and F.6 only when this account or a receiving use expressly consumes precise assignment-bound attribution through the same obtaining A.13 assignment; F.6 identifies neither the assignment nor the performer, and missing or failed F.6 leaves the Work intact.
   * **Result or consequence:** only when the sentence asks for one, select the matching `A.15.1:4.6` row—an A.6.1 application/result binding or independently obtaining `WorkResultRelation`, A.15.PROD production branch, A.3.4 change, evaluation result, subject-specific delivery/transfer relation, or acceptance relation. An absent row stays absent.
   * **Evidence:** only when a receiving use relies on Work or one of those consequences, state an A.10 claim-bound evidence path and carrier.

### A.6.C:4.2 — Classification recipe into A.6.B (L/A/D/E) {#classification-recipe-into-a-6-b-l-a-d-e}

After unpacking, classify each **atomic** statement using the Boundary Norm Square as defined normatively in **A.6.B** (quadrant semantics + form constraints + cross‑quadrant reference discipline). A.6.C does not redefine `L/A/D/E`; it applies them to contract-language as follows:

* **Promise content → L/A (promise semantics + eligibility).**
  * Put meanings, invariants, and metric definitions for what is promised in **L** (`L-*` in signature laws and definitions).
  * Put “eligible, covered, or valid iff …” predicates as **A** (`A-*` admissibility or gate predicates), not as deontic obligations.
* **Governance and permission-looking claims → claim-specific quadrant.**
  * Put a generic contract, SLA, protocol, or policy prescription in **D** as a claim about its exact normative source and applicable rule content. Put an individual-duty claim in **D** only when it cites an exact separately obtaining `U.Commitment` under A.2.8; do not use a completed record as the relation.
  * For authority-looking wording, select one A.6 `A6-AW-*` row: norm/grant → **D**, mechanism entry predicate → **A**, and an actual A.21 `GateDecisionResult`, exercise, evaluated finding/conflict, or source observation → **E**. Split a predicate and an actual gate result into separate atomic claims. Cite the exact A.2.8.PER object only where that row requires it; the selected subject pattern or kind of direct object does not choose the sentence's quadrant.
  * If a generic prescription or individual duty requires satisfying or enforcing a gate, its `D-*` claim **MUST** reference the relevant `A-*` ID(s) (D→A).
  * If reliance on either D branch needs evidence, cite the relevant `E-*` claim or evidence-use relation (D→E); for the individual branch, a `CommitmentAssertion` may carry that reference.
* **Performed Work → E (did it happen?).**
  * Name the exact A.15.1 Work occurrence and its performer, Method, extent, and containing System. Add an assignment reference and F.6 only when the claim or a receiving use consumes precise assignment-bound attribution; do not add an output or delivery field.
* **Result or consequence → E when current (what else happened?).**
  * Use the one applicable `A.15.1:4.6` predicate and exact subject assertion for the returned value, production, change, evaluation result, delivery/transfer, or acceptance claim; retain its pattern only as a locator.
* **Evidence → E when relied on (how can the claim be used?).**
  * Name the exact A.10 path, observation conditions, and carrier for the Work or consequence claim being supported.
**Keyword placement rule (canonical claim set).**
Within the canonical L-, A-, D-, or E-classified claim set, BCP-14 keywords are statement operators, not ontology or quadrant selectors. `MUST`, `MUST NOT`, `SHOULD`, and `SHOULD NOT` enter D for a generic prescription or, when separately instituted for an actual bearer, an individual duty, recommendation-as-duty, or prohibition. `MAY`, `OPTIONAL`, and authority-looking synonyms trigger the A.6 `A6-AW-*` branch: a current norm or grant enters D, a mechanism entry predicate enters A, and an actual A.21 `GateDecisionResult`, exercise, or evaluated finding enters E. If the wording does not expose the branch and direct object, rewrite it or mark it informative.

A helpful rewrite rule:

> First recover what “allowed” asserts by selecting one A.6 `A6-AW-*` row. Put only the current norm/grant in D, the entry predicate in A, and an actual A.21 `GateDecisionResult`, exercise, or evaluated finding in E; cite each direct object and source. The word and A.2.8.PER membership select neither quadrant nor obtaining.

### A.6.C:4.3 — “Guarantee” disambiguation {#guarantee-disambiguation}

When “guarantee” leaves a consequential ambiguity, use the applicable distinction below:

* **Semantic guarantee** → **L** (“by definition or invariant”).
* **Runtime-entry guarantee** → **A** (“the mechanism admits this application iff …”).
* **Governance guarantee** → **D** (“provider commits or implementer must”).
* **Operational result** → **E** (the exact Work, evaluation, or observation and its measured or evaluated result; add an A.10 evidence path and exact carrier when the receiving decision relies on that support).

If none of these fits, the statement is likely rhetorical and should be rewritten or explicitly marked as aspirational or informative.

### A.6.C:4.4 — MVPK faces are not second contracts {#mvpk-faces-are-not-second-contracts}

The atomic claims grouped for one boundary use live in one canonical A.6.B Claim Register set; the four-question lens creates no parallel claim set. Publication faces present that set for a bounded reader/use under E.17:

* Faces may **select, summarize, and render** claims for audiences. A selected episteme's `U.View` membership separately requires E.17.0 conformance to an exact viewpoint.
* Faces must not add a new boundary claim; they project the existing classified claims.
* Any face-level decision-relevant or normative-looking statement **SHOULD** cite the underlying claim ID(s) or canonical location(s). A new boundary claim **MUST** be added to its canonical source before publication on a face. Informative commentary may explain source claims without adding boundary semantics.

**Keyword rule (faces).**
If a face contains a BCP-14 keyword, each sentence MUST cite its existing classified claim ID or canonical location and direct object. Duty/recommendation/prohibition and current-grant projections cite their D claim; a gate projection cites its A claim; exercise or evaluated-finding projections cite their E claim. Use the selected A.6 `A6-AW-*` row for permission-looking wording. A face-level keyword manufactures no object or quadrant. If the boundary claim is not traceable, put it in its canonical source before publishing it on the face; informative commentary is limited to explanation that adds no boundary semantics.
To avoid keyword-evasion, equivalent deontic phrasings (e.g., “is required to…”, “is prohibited from…”) SHOULD follow the same claim-reference discipline even when no BCP-14 keyword is present.

Projection may be paraphrased for audience fit, but it **MUST NOT** change the deontic or semantic claim; if exactness is critical or disputed, use verbatim.

This prevents faces from becoming “second contracts” by paraphrase drift.

### A.6.C:4.5 — A.6.B Claim Register additions (recommended) {#a-6-b-claim-register-additions-recommended}

When stable reuse, decision, audit, dispute, or cross-face projection needs a record, use the **A.6.B Claim Register** (IDs, statements, quadrant, and canonical location). A one-off local repair ends with the repaired atomic prose. When the register is needed, add only the current A.6.C fields below without minting another record or ontology kind:

* `bundleId` (optional local ID grouping atomic claims discussed together)
* `questionRef` (optional pointer `Q1`, `Q2`, `Q3`, or `Q4` to the four questions above; it selects no kind, subject predicate, or quadrant)
* `directObjectDesignation` (use `U.RelationRef` constrained to the exact relation family for a relation occurrence, the applicable `U.EpistemeRef` for a whole episteme, or the admitted reference kind for another independently identified entity. When one claim inside an episteme is the direct object, use `C.2.1 ClaimAddress`: exact episteme-edition reference plus intrinsic claim identity declared by that edition's ClaimGraph. The entity-reference branches designate independently identified objects; the claim branch designates content inside the named edition. Neither carries the designated content.)
* `directObjectPatternLocator` (the exact pattern-description locator for the ClaimGraph that defines or constrains that direct object; it asserts no ownership relation)
* `faceRefs` (optional mapping from `PlainView`, `TechCard`, `InteropCard`, or `AssuranceLane` to where this same claim is rendered)

Each row still uses the A.6.B fields for one exact statement, claim ID, quadrant, and canonical location. Do not create a second boundary-language record or a `Permission`, `Utterance`, `WorkEvidence`, or result-or-evidence umbrella kind.

## A.6.C:7 — Conformance Checklist {#conformance-checklist}

A boundary description conforms to A.6.C iff it satisfies all items below:

1. **CC‑A.6.C‑1 (Four questions, atomic answers).**
   When contract-like wording leaves a consequential ambiguity, the text **SHALL** answer only the applicable four-question branches with atomic claims. Speech act, description/publication, generic prescription, individual commitment, selected permission-side claim, dated Work, each consequence, and each evidence claim **SHALL** retain its own direct object, exact subject assertion, non-semantic pattern locator, and quadrant.

2. **CC‑A.6.C‑2 (No agency to epistemes).**
   When a dated act or individual commitment is claimed, the text **MUST** identify its capable actual participant and **MUST NOT** substitute an API/interface label, description, publication carrier, kind, or assignment for that participant's basis. Ordinary metonymy may remain when its participant and relation are locally recoverable. A generic prescription **SHALL** name its exact normative source and applicable content without inventing an individual bearer. An individual duty or commitment **SHALL** name its actual bearer and exact separately obtaining `U.Commitment`; an assignment may appear only as an instituting rule's applicability ground.

3. **CC‑A.6.C‑3 (Classify contract-language statements via A.6.B).**
   When contract-language leaves a consequential ambiguity, its unpacked statements **SHALL** be atomic L/A/D/E claims. In that unpacking, permission-looking wording **SHALL** select one A.6 `A6-AW-*` row; A.2.8.PER membership alone **MUST NOT** set the quadrant.

4. **CC‑A.6.C‑4 (Promise content ≠ Work discipline).**
   A performed-work statement **SHALL** name the exact A.15.1 dated Work occurrence. A result, production, change, delivery/transfer, evidence, or acceptance statement **SHALL** use its own direct object and shall not be inferred from Work. Promise-content language remains about `U.PromiseContent`, not execution or consequence.
   When *service* or access-like wording occurs in a relied-on boundary claim, recommendation, decision, gate, assurance, publication, or reuse and hides the concrete subject, participant, predicate, kind, permission, Work occurrence, or next subject question, the text **SHALL** recover that hidden choice through E.10 **L-SERV** and **A.6.P:4.11a**, then state the exact assertion under the recovered predicate with its pattern locator. Quoted, historical, illustrative, and harmless ordinary wording remains outside this recovery rule; an actual `U.PromiseContent` referent still uses the head phrase **promise content**, not bare *service*.

5. **CC‑A.6.C‑5 (Evidence hook for operational guarantees).**
   If a “guarantee” is operational (requires reality to decide), the text **SHALL** include an **E** claim naming the exact Work, evaluation, or observation, predicate and object, scope or window, and measured or evaluated result. When a receiving decision relies on evidence, the claim **SHALL** cite the A.10 evidence path and exact carrier used for that reliance.

6. **CC‑A.6.C‑6 (No second contracts via faces).**
   MVPK faces **MUST NOT** add new boundary claims; they publish only the existing canonical L/A/D/E claims under E.17. Informative commentary may explain those claims without adding boundary semantics. An asserted `U.View` separately requires E.17.0 conformance.

7. **CC‑A.6.C‑7 (RFC‑keyword discipline inside faces).**
   If an MVPK face contains a BCP-14 keyword, each sentence **MUST** cite its classified claim ID or canonical location, direct object, and selected `A6-AW-*` row when permission-looking. Only norm/grant claims cite D; gate claims cite A; exercise and evaluated findings cite E.

8. **CC‑A.6.C‑8 (Obtaining is not representation).**
   A `Publish` or `Approve` utterance, a document, carrier, or record does not by itself institute or prove a `U.Commitment` or `GrantedPermissionRelation@Context`. The exact obtaining predicate and cited context policy decide whether the relation obtains. A Claim Register row may assert or support reliance on it only when the row names the exact occurrence, predicate, `SubjectPatternLocator`, participants, scope/window, and current evidence required by that use. For a commitment, the row cites its rule-required actual instituting basis and policy; for a strong grant, it cites the actual instituting speech act and policy. The row alone does not create the relation. When the grant occurrence is the row's direct object, `directObjectDesignation` **SHALL** be a `U.RelationRef` constrained to `GrantedPermissionRelation@Context`; an entity reference, `ClaimAddress`, display label, or arbitrary identifier cannot fill that branch.

## A.6.C:9 — Consequences {#consequences}

**Benefits**

* Category mistakes (“contract soup”) become systematically repairable.
* Generic prescriptions remain usable without invented occurrences, while individual commitments remain distinguishable and adjudicable through their actual bearer, rule, instituting basis, scope, validity, and any evidence needed for reliance.
* Boundaries remain evolvable: laws, gates, governance, and evidence can evolve with controlled coupling.

**Trade-offs and mitigations**

* Additional authoring effort; mitigated by applying the unpacking only when contract-like wording leaves a consequential ambiguity, and by persisting a Claim Register entry only when stable reuse, decision, audit, dispute, or cross-face projection needs it.
* Some stakeholders prefer “one sentence contract”; mitigated by MVPK faces that present curated projections while keeping the underlying claim set coherent.

## A.6.C:12 — Relations {#relations}

* **Uses and is used by**

  * Uses **A.6.B** for L/A/D/E claim classification, atomicity, and cross-quadrant reference discipline.
  * Used by **A.6** cluster conformance (“contract unpacking”) as the detailed, reusable form of that discipline.
  * Complements **A.6.S** (signature engineering): contract unpacking is a common constructor step when turning prose boundaries into publishable signatures.
  * Coordinates with **A.6.P** families: when “contract or guarantee” wording in a boundary use still leaves a consequential ambiguity after RPR, apply A.6.C to that ambiguity. (A.6.C is **not** a specialization of A.6.P; A.6.P is relation‑precision, A.6.C is boundary‑contract disambiguation.)

* **Coordinates with**

  * **A.7** (EntityOfConcern, Description episteme, and carrier) for correct placement of evidence claims.
  * **A.15.1** for the exact dated Work occurrence and its §4.6 dispatch to application/result, production, change, evaluation, evidence, delivery/transfer, and acceptance patterns.
  * **F.12** (service acceptance) for structuring how promise-level commitments connect to evidence and acceptance windows.
  * **E.17** MVPK “no new semantics” rule to prevent publication faces from becoming new contracts.
  * **A.2.8.PER** for the exact permission-side direct objects; A.6 `A6-AW-*` and A.6.B classify each atomic claim without treating pattern selection as its quadrant.


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/A-6#root, spec://ai.lev/fpf-spec/contract/A-6-B#root, spec://ai.lev/fpf-spec/contract/A-6-P#root, spec://ai.lev/fpf-spec/contract/A-7#root, spec://ai.lev/fpf-spec/contract/A-2-3#root, spec://ai.lev/fpf-spec/contract/A-2-8#root, spec://ai.lev/fpf-spec/contract/A-2-8-PER#root, spec://ai.lev/fpf-spec/contract/A-2-9#root, spec://ai.lev/fpf-spec/contract/A-15-1#root, spec://ai.lev/fpf-spec/contract/A-10#root, spec://ai.lev/fpf-spec/contract/E-17#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/F-12#root, spec://ai.lev/fpf-spec/contract/F-18#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-2-3#root, spec://ai.lev/fpf-spec/contract/A-2-8#root, spec://ai.lev/fpf-spec/contract/A-2-8-PER#root, spec://ai.lev/fpf-spec/contract/A-2-9#root, spec://ai.lev/fpf-spec/contract/A-6#root, spec://ai.lev/fpf-spec/contract/A-6-B#root, spec://ai.lev/fpf-spec/contract/A-6-F#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/A-6-C
