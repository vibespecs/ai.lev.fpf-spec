# A.6.RCD - Needed Relation Claim Derivation and Relation-Kind Admission {#root}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Kernel relation-foundation pattern
> **Status:** Stable
> **Normativity:** Normative unless explicitly marked informative

**Plain name.** Derive the needed relation claim before admitting a relation kind.

## A.6.RCD:0 - Use This When {#use-this-when}

Use this pattern when an engineer can name the exact participant referents and the claim, check, decision, or continuation that is blocked, but no current direct relation states the needed relation-bearing claim.

Typical first-minute situations are:

- several exact base-relation facts seem to imply the needed claim, but `related to` or a convenient verb hides how;
- a formula, query path, graph edge, or rule appears to define the answer, and the team is about to treat it as a relation kind;
- the same compound claim recurs and the team needs to decide whether to keep deriving it locally, publish reusable predicate semantics, or admit a relation kind;
- a proposed primitive relation appears to be only a composition, projection, closure, aggregation, or cross-algebra juxtaposition of existing claims.

**Primary EntityOfConcern.** One exact needed relation-bearing claim for one named receiving use. The application also settles whether that claim remains local, receives a reusable predicate-definition episteme, or justifies a derived or primitive relation kind. This wording does not mint a `NeededRelationClaim` kind or an application-record kind.

**First useful move.** Write the blocked receiving use and the participant meanings in ordinary domain language. Then use `A.6.P` to recover the pattern containing the current subject predicate and ask whether that predicate can already state the needed affirmative, negative, or exact rule-qualified modal claim for those participants. If it can, apply its test and use the exact blocker boundary below when the result cannot yet be stated. Derive a compound predicate only when no current direct predicate can express the needed claim.

**What goes wrong if missed.** A team either leaves the claim as vague connective prose or promotes a formula, query, graph path, definition, or convenient name into ontology. The first loses replayable meaning. The second invents relation kinds without an obtaining law or occurrence identity.

**What this buys.** The engineer gets the lightest sufficient result: an existing direct relation, a local compound claim, reusable predicate-definition content with an optional separately admitted derived relation kind, or a genuinely irreducible primitive relation kind. The ontology grows only when the receiving use needs occurrence semantics that claim content alone cannot supply.

**Ordinary non-use boundary.** Do not use this pattern when a current direct predicate can already state the needed affirmative, negative, or exact rule-qualified modal claim; write that claim using the predicate's pattern and stop. A negative, hypothetical, forecast, or rule-qualified modal claim needs no obtaining relation occurrence. If the predicate and its applicability rule exist but the attempted positive result cannot be stated, use the three-way boundary below: `factually unsupported` only when the available case basis is sufficient to apply the positive test and that test fails; `missing-information` when a fact needed to decide that test is unavailable. Do not use A.6.RCD for wording-only cleanup, mathematical-lens adequacy, naming, evidence, assurance, or publication questions. `E.10`, `C.29`, `F.18`, `A.10`, `B.3`, and `E.17` supply the relevant definitions or tests.

**Cheap stop.** If a readable current direct relation closes the receiving use, stop before constructing a compound claim. If a local compound claim closes it, stop before publishing a reusable definition. If a reusable definition closes it, stop before admitting a relation kind.

### A.6.RCD:0.1 - Name the exact blocker {#name-the-exact-blocker}

Use three ordinary blocker phrases without turning them into a common result kind:

- `missing-governor` means that, for the stated participants and use, no current predicate definition, applicability condition, occurrence rule, or other governing rule can state or test the attempted relation claim. It says nothing about whether case facts exist.
- `factually unsupported` means that the required governor and positive test exist, the available case basis is sufficient to apply that test, and the test fails. It stops the attempted affirmative; it does not establish the negative.
- `missing-information` means that at least one fact needed to decide the current test is unavailable, so the test cannot yet return its positive, negative, or inapplicable result.

If an applicability rule exists and the available case basis establishes that the case is outside it, return that rule's inapplicable result. State a negative claim only when an applicable non-obtaining criterion or complete closure basis exists and the available facts satisfy it; failure of the positive test alone is not that basis. If the governing rule itself is absent, use `missing-governor`; if a fact needed to decide its test is unavailable, use `missing-information`. `missing-substrate` remains the narrower section 4.2 stop for unavailable constructor semantics. These phrases are readable outcomes, not new U-kinds, result records, or an omnibus blocker ontology.

## A.6.RCD:1 - Problem Frame {#problem-frame}

FPF permits rich claims over already identified entities and admitted relations without requiring one primitive relation kind for every useful sentence. The difficult case begins after relational precision restoration: the participants are recoverable, the receiving use is real, and simpler direct relations exist, but no one current direct relation carries the needed claim.

The ordinary result of this pattern is claim content in a `C.2.1` episteme. Deriving that content is not the constitution of an actual relation occurrence. Repeated use can justify reusable predicate-definition content. Only a further occurrence-semantics need can justify a derived relation kind, and only irreducible action-facing semantics can justify a primitive relation kind.

## A.6.RCD:2 - Problem {#problem}

Two errors compete.

1. **Under-definition.** `Related to`, `fulfils`, `enacts`, `reachable`, `supports`, or another convenient phrase hides the base facts, participant meanings, polarity, intermediate participants, applicability, or rule by which the claim follows.
2. **Premature admission.** A repeated expression, formula, query, graph path, table row, definition, or name is treated as a relation kind or relation occurrence although no direct subject settlement states obtaining and occurrence identity.

Authors MUST preserve expressive claims while preventing representation-created ontology and primitive-kind inflation.

## A.6.RCD:3 - Forces {#forces}

| Force | Tension to resolve |
| --- | --- |
| Exact semantics vs readable use | Authors MUST make each conforming derivation replayable without making every practitioner read formal notation. |
| Local affordability vs repeated reuse | One local claim should stay cheap; repeated semantics should not be copied inconsistently. |
| Expressive claims vs small ontology | FPF should permit compound truths without minting one kind per compound predicate. |
| Reuse vs hidden dependencies | Reusable definitions need visible base-relation and substrate editions. |
| Truth conditions vs occurrence semantics | A predicate can be satisfied without supplying a way to reidentify relation occurrences. |
| Formal power vs substrate authority | Constructor names are available only where the selected substrate gives them semantics. |
| Mathematical representation vs ontology | A formula, path, graph, or query can represent a rule without making that rule obtain in the world. |

## A.6.RCD:4 - Solution {#solution}

Name the blocked receiving claim and participants. Reuse a current direct predicate when it can state that claim. Derive only what the selected substrate warrants. Publish reusable predicate semantics only for repeated use. Admit a relation kind only with its direct obtaining and occurrence-identity laws. Stop when the receiving use works.

### A.6.RCD:4.1 - Execute the demand-first method {#execute-the-demand-first-method}

1. **Name the blocked use.** State the exact claim, check, decision, or continuation that cannot proceed, and what answer would close it.
2. **Recover participants and direct relations.** Use `A.6.P` to name the actual participant referents under their relation-participant meanings and retrieve the smallest plausible base from the exact pattern content or declaration that defines each base predicate and its obtaining law. Similar tokens, shared field names, or adjacent graph edges are not a base.
3. **Choose the least constructor admitted by the current substrate.** State the constructor semantics and the base claim content it consumes. Do not infer an operator from punctuation or notation.
4. **Replay three things.** Test one positive case, one discriminating failure case, and the named receiving use. Keep hidden intermediates, polarity, scope, time, and base-definition editions visible when they change the result.
5. **Select the lightest disposition.** Choose exactly one of the four dispositions in section 4.3 and stop at its stopping rule.
6. **Open reusable semantics only when repeated use needs the same rule.** First decide whether every reuse concerns one exact subject or the parameterized rule is reused across several subject instances. For one subject, identify a subject-bounded compound-law episteme whose exact `EntityOfConcern` is that subject and state the reuse limit. For a rule reused across subject instances, identify the exact reusable predicate definition as `EntityOfConcern`; that episteme may satisfy A.6.0 `U.Signature` membership before any relation kind is admitted, but it is not a `RelationSignature`.
7. **Open kind admission only when occurrence semantics are consumed.** A derived kind needs a direct subject settlement with obtaining, applicability, base dependencies, and a non-optional occurrence-identity rule. A primitive candidate additionally carries the failed derivation, the exact action-facing distinction lost, its own obtaining and recurrence laws, independent receiving uses, and a standalone subject-pattern obligation.

Use this compact working note only while the decision is live:

```text
A.6.RCD working note:
  blockedReceivingUse:
  participantMeanings:
  candidateBaseRelationClaims:
  selectedSubstrateAndEdition:
  constructorSemantics:
  positiveCase:
  discriminatingFailureCase:
  receivingUseReplay:
  disposition:
  predicateDefinitionModeIfCurrent: subjectBounded | reusableAcrossSubjects
  predicateDefinitionEntityOfConcernIfCurrent:
  subjectBoundReuseBoundaryIfCurrent:
  directSubjectSettlementIfKindCurrent:
  stopOrReturn:
```

The note is a pattern-local prompt. A filled, claim-bearing use is an episteme under `C.2.1`; the printed shape is not a new record kind, `RelationSignature`, relation kind, or relation occurrence.

### A.6.RCD:4.2 - Respect substrate authority {#respect-substrate-authority}

A constructor probe is usable only when the selected substrate defines its inputs, output claim, applicability, and relevant laws. The following table is a non-exhaustive set of recurring single-substrate semantic probes. It is neither a universal operator registry nor a claim that any substrate supports the whole list.

| Recurring single-substrate semantic probe | Minimum semantics to recover | Boundary |
| --- | --- | --- |
| typed restriction | the base predicate, restricted participant kind or condition, and scope | a narrower claim is not automatically a new relation kind |
| participant permutation or converse | participant correspondence, polarity, and whether the direct subject ontology treats the inverse reading as the same occurrence | syntax does not decide occurrence identity |
| composition | the two or more base predicates, exact shared participant, order or direction, and intermediate witness policy | a hidden intermediate does not disappear from semantics because a query projects it away |
| projection | the source claim, retained participants, hidden participants, and existential or other projection law | projection can yield claim content without yielding an occurrence-identity rule |
| conjunction | all conjuncts, their common applicability, and one truth condition for the compound claim | co-truth does not create a cross-subject relation kind |
| negation or complement | the substrate's closed-world, open-world, constructive, probabilistic, or other negation law | absence of a base assertion is not automatically a negative relation fact |
| transitive or path closure | admitted edge relation, direction, path rule, zero-length policy, cycle policy, and subject structure | a graph path is a representation or witness; it is not the obtaining relation occurrence |
| aggregation | the population or collection, grouping rule, aggregated value, aggregation operator, empty or duplicate treatment, scope, and applicability | an aggregate or scalar summary does not silently become a relation predicate or occurrence |
| probabilistic operator | the event or sample space, random variables or events, probability operator or model, conditioning, threshold or decision rule, applicability, and uncertainty boundary | a probability, likelihood, or posterior does not silently become a relation predicate, and shared event labels do not bridge algebras |

**Cross-algebra claim-use boundary.** Ask how the named decision or work occurrence actually uses each result. For every consumed result, state its own obtaining premise-use, reference-use, decision-use, or other direct use relation under the pattern for that question. If the decision is one actual application of a declared operation, an exact A.6.1 argument binding may state that use instead. If no current predicate definition, applicability condition, or occurrence rule can state the required result-use relation for those participants, return `missing-governor`; if the governor exists and the available case basis is sufficient to apply its positive test but that test fails, return `factually unsupported`; if a fact needed to decide the test is unavailable, return `missing-information`. Co-publication, a shared topic, or one decision record supplies no use relation.

Stop there when those independent uses close the named decision or work question. Open a separate joint predicate only when the decision genuinely depends on a joint condition that the independent use relations cannot express; then name that condition and use A.6.RCD to derive exactly it. Do not add a generic joint-use relation or record merely because one decision cites results from two algebras.

When a consumed result relies on an obtaining F.9 Bridge between two exact F.17 `SchemeSenseCell` values, cite that Bridge and the separate bounded-use claim; add `CL` or a loss note only when the receiving use needs it. When the result instead crosses exact ReferencePlanes, cite the applicable plane relation and policy. If both facts are current, state both under their own predicates. A cell or plane difference alone creates neither relation, and one branch never fabricates the other. A Bridge-related penalty is current only when an actual named B.3 assurance claim uses an applicable declared domain model, calibrated mappings where needed, stated dependencies and assumptions, and current case facts whose rule yields that penalty. It affects only the calculated assurance result for that named use; it supplies no default fold and changes no independently stated characteristic.

A local compound claim needs recoverable constructor semantics, but it does not need a separately materialized substrate document. Authors MUST name and pin the substrate when the derivation is nontrivial, intended for interoperability, used as proof, or becomes a reusable predicate definition. If no current substrate supplies the proposed operator, return a missing-substrate blocker rather than improvising a universal constructor algebra.

### A.6.RCD:4.3 - Select one of four dispositions {#select-one-of-four-dispositions}

| Disposition | Test | Result | Stop |
| --- | --- | --- | --- |
| **1. Existing exact predicate** | One current exact ClaimGraph already supplies the participant meanings, obtaining predicate, applicability, and claim family needed by the use. | State the readable affirmative, negative, or exact modal claim in a claim-bearing episteme under that predicate, retaining the source pattern only as a locator. Current case facts or constituting history supply its factual basis. If no needed predicate, applicability condition, or occurrence rule exists, return `missing-governor`; if the governor exists and the available case basis is sufficient to apply its positive test but that test fails, return `factually unsupported`; if a fact needed to decide the test is unavailable, return `missing-information`. State a negative only under an applicable non-obtaining criterion or complete closure basis whose facts are satisfied. | Stop. Do not derive a synonym predicate or duplicate relation kind. Only when an adequately grounded affirmative case satisfies the predicate is there an obtaining occurrence; use A.6.REL only when a named use consumes that occurrence's identity. |
| **2. Local compound relation-bearing claim** | A substrate-admitted composition of current base predicates closes this one receiving use, and no repeated definition or occurrence semantics is needed. | Put positive or negative compound claim content in one identified `C.2.1` episteme. An information-sufficiency or reliance assessment stays with the evaluation or evidence pattern and uses the blocker boundary in section 0.1; it is not a third predicate value. | Stop. Introduce no relation kind, `RelationSignature`, or `U.Relation` occurrence. |
| **3. Reusable predicate semantics, with derived-kind continuation only when needed** | Several uses need the same parameterized rule. If they all concern one exact subject, the rule is subject-bounded; if the rule is reused across subject instances, it is a genuinely reusable predicate definition. | Publish one C.2.1 episteme with the truthful branch-specific `EntityOfConcern`: the exact subject for a subject-bounded compound law, or the exact reusable predicate definition for cross-subject reuse. The latter may independently satisfy A.6.0 `U.Signature` membership. If a receiving use also needs stable relation-occurrence semantics, return a derived-kind candidate plus its proposed direct subject settlement and handle that candidate under `E.24` and `E.24.UK`, and to `A.11` when parsimony is current. | Stop at the selected definition unless occurrence semantics are named and the proposed settlement is supplied. A definition is not a kind. A.6.0 membership does not make it a `RelationSignature`; only an admitted relation kind opens that specialization. |
| **4. Primitive relation kind** | Every accepted derivation loses one exact action-facing distinction, and the candidate has independent receiving uses plus its own obtaining, recurrence, applicability, and occurrence-identity laws. | Carry the candidate to `A.11`, `E.24`, and `E.24.UK`, and author a standalone direct subject pattern. | Stop or block if the failed derivation, lost distinction, independent use, direct pattern, or identity law is absent. A convenient name never passes this test. |

These are economy dispositions, not maturity stages. Later need can reopen a local claim or definition. The four dispositions do not impose a required maturity ladder on any application.

### A.6.RCD:4.4 - Keep kinds, predicates, claims, and occurrences distinct {#keep-kinds-predicates-claims-and-occurrences-distinct}

Keep the order visible: the admitted relation kind classifies; its direct predicate defines the test; current case facts or constituting history determine whether that test is satisfied, failed, or still open; a claim-bearing episteme states an affirmative, negative, or exact rule-qualified modal claim; and an obtaining world-side occurrence exists only in a satisfied affirmative case. Apply section 0.1 when the test or its factual basis cannot yet produce a result. Use A.6.REL for explicit occurrence individuation only when a named use consumes identity.

| Object | What it is | What it is not |
| --- | --- | --- |
| admitted direct relation kind | the admitted classificatory distinction over its possible obtaining occurrences | not the direct predicate, one case result, an assertion, or an occurrence |
| direct obtaining predicate | the declared test for named participant meanings under its applicability conditions | not proof that the test is satisfied in this case and not an occurrence |
| direct relation-bearing assertion | one `C.2.1` episteme whose exact claim family states affirmative, negative, or exact rule-qualified modal content about the predicate for named participants | not the world-side obtaining result and not an information-sufficiency or reliance disposition |
| obtaining direct relation occurrence | one world-side relation occurrence for which current case facts or constituting history satisfy the direct predicate; its direct identity rule exists even when no named use needs an explicit designator | not created by the assertion, evidence, a representation, or an identifier |
| local compound relation-bearing claim | claim content in one `C.2.1` episteme, asserting or denying satisfaction of a substrate-admitted compound predicate | not a relation kind and not a relation occurrence |
| subject-bounded compound-law episteme | one `C.2.1` episteme whose exact `EntityOfConcern` is the promise-content edition, subject structure, decision occurrence, or other exact subject to which the rule is explicitly limited | not a predicate definition reusable across subject instances, not a `RelationSignature`, and not a classifier of relation occurrences |
| reusable predicate-definition episteme | one `C.2.1` episteme whose exact `EntityOfConcern` is the reusable predicate definition itself and whose claims define its parameterized semantics across subject instances | may satisfy A.6.0 `U.Signature` membership, but is not a `RelationSignature` before relation-kind admission and does not classify relation occurrences |
| admitted derived relation kind | a classificatory distinction over relation occurrences, with obtaining defined through admitted base relations | not the definition episteme; it needs its own direct subject settlement and identity rule |
| admitted primitive relation kind | a classificatory distinction whose needed action-facing semantics cannot be preserved by accepted derivation | not a reward for a familiar word or notation |
| claim or derivation representation | formula tokens, formula trees, query paths, graph elements, tables, diagrams, or other `C.29` representation elements | not satisfaction, obtaining, admission, or occurrence identity |
| designator or typed reference | a name or reference associated with an already settled definition episteme, relation kind, or individuated occurrence | not one token that silently creates or identifies all three |

### A.6.RCD:4.5 - Settle a reusable predicate definition truthfully {#settle-a-reusable-predicate-definition-truthfully}

When the same rule is used more than once, first ask where the reuse actually travels.

- **One exact subject.** If every use asks about the same promise-content edition, subject structure, decision occurrence, or other exact subject, identify a subject-bounded compound-law episteme whose `EntityOfConcern` is that subject. State plainly that the rule may be reused only for claims about that subject; a familiar formula does not make it portable to another subject.
- **Across subject instances.** If the same parameterized rule is applied to several independently identified subjects, identify one reusable predicate-definition episteme whose `EntityOfConcern` is the exact predicate definition itself. If its claim graph supplies the subject and value range, Vocabulary, Laws, and Applicability required by A.6.0, the already identified episteme may satisfy `U.Signature` membership without relation-kind admission. It remains a predicate-definition declaration, not a `RelationSignature` or a classifier of occurrences.

In either branch, the definition content states:

- parameter and participant meanings;
- the exact base-relation claims and the pattern content or declarations that define their predicates and obtaining laws;
- the derivation rule under the selected substrate;
- polarity, scope, time, and applicability;
- base-definition and substrate dependencies plus their editions when current;
- positive and discriminating cases;
- the admissible claim use and the non-admissible occurrence or ontology overread.

If neither the exact subject nor the exact reusable predicate definition is the truthful `EntityOfConcern`, keep the needed results as local compound claims. Do not manufacture a union concern or alternate opportunistically between the rule and a nearby domain subject.

### A.6.RCD:4.5a - Reusable rule-content predicates stop before relation-kind admission {#reusable-rule-content-predicates-stop-before-relation-kind}

`RuleContentBasisFindingDefinition@R7` is the disposition-3 declaration for two repeated cross-subject predicate semantics: `derivedUsingRuleContent(dependentContent, baseContent)` and `evaluatedAgainstRuleContent(dependentContent, baseContent)`. Its exact EntityOfConcern is that reusable predicate definition. Its `SubjectKind` and `RangedValueKind` are both `U.ClaimGraph`; predicate obtaining is asserted through C.2.1, so no separate result kind is introduced. The declaration may satisfy ordinary A.6.0 `U.Signature` membership. It is not a `RelationSignature`, relation kind, relation occurrence, registry, or claim that every definition or constraint was actually used.

Use the first predicate only when an identified derivation claim names the exact nonempty base subgraph as a formal premise under a declared inference rule or application producing the exact dependent content. Use the second only when an identified criterion-selection claim selects that base for an exact bounded evaluation claim concerning the dependent content. The dependent and base values are predicate parameters, not A.6.5 SlotSpecs. Actual-use assertions remain ordinary C.2.1 epistemes; consultation, influence, provenance, evidence, evaluation Work, and later sufficiency remain separate.

This reusable declaration does not replace the cheaper branches. A subject-local assertion that names its defining or constraining ClaimGraph and closes the receiving use stops at disposition 1 or 2. Open the R7 definition only where repeated cross-subject semantics are actually reused; open a basis analysis only for a named comparison, replay, conflict, or reliance use. No accepted use currently needs an obtaining relation occurrence between rule content and dependent content as a participant or comparison object, so the relation-kind continuation remains closed.

### A.6.RCD:4.6 - Prepare derived or primitive relation-kind admission only with occurrence semantics {#prepare-derived-or-primitive-relation-kind-admission-only-with}

When a named use consumes occurrence semantics, A.6.RCD yields a relation-kind candidate and the settlement material needed for admission: a derived-kind candidate plus its proposed direct subject settlement, or a primitive-kind candidate plus its candidate standalone subject pattern. Apply the admission predicates defined in `E.24` and `E.24.UK`, and the parsimony predicate in `A.11` when that question is current. Neither a proposed settlement nor a candidate pattern locator admits the kind. For a candidate that is admitted, the resulting direct subject settlement states:

1. the classified relation occurrences and exact participant meanings;
2. the obtaining predicate and applicability;
3. for a derived kind, the exact derivation law and base-definition dependencies;
4. a direct occurrence-identity rule that distinguishes repetition;
5. recurrence, cessation, and continuation conditions when those distinctions matter;
6. at least one named receiving use that consumes occurrence semantics;
7. the standalone subject pattern.

An admitted relation kind never has `identity intentionally absent`. Ordinary use can omit explicit individuation, occurrence records, and designators because no named use consumes them; the direct identity rule still exists.

A pure converse preserves one base occurrence only when the direct subject ontology explicitly says that inverse wording concerns the same occurrence. Restriction, projection, composition, closure, aggregation, and hidden intermediates require an explicit identity decision. Their syntax does not decide whether the derived occurrence inherits one base identity, is constituted as a composite occurrence, or has a new direct identity rule. If no truthful rule is available, remain at local-claim or predicate-definition level.

Before relation-kind admission, authors MAY ask A.6.0 whether a genuinely reusable predicate-definition episteme satisfies ordinary `U.Signature` membership. That declaration's `EntityOfConcern` is the exact predicate definition, not a candidate relation kind, and the result neither classifies occurrences nor admits a kind.

Authors MAY publish under A.6.0 a `RelationSignature` whose `EntityOfConcern` is an exact relation kind only after that kind is admitted. The `RelationSignature` declares reusable SlotSpecs and restates the direct laws; it does not admit the kind or make an occurrence obtain.

### A.6.RCD:4.7 - Separate recognition from assurance {#separate-recognition-from-assurance}

**Recognition branch for ordinary receiving use.** Ask only:

1. What receiving claim or action is blocked?
2. Who or what are the exact participants, and under which meanings?
3. Does one current direct predicate already state the needed affirmative, negative, or exact rule-qualified modal claim?
4. If not, what smallest substrate-admitted compound claim answers it?
5. Which of the four dispositions lets the receiving use proceed now?

The ordinary branch can stop at a readable direct claim or one readable compound claim. It does not require a named substrate document, predicate-definition publication, new relation kind, signature, explicit occurrence, or designator when the receiving use consumes none of them.

**Negative direct-claim case.** A staffing check asks whether `Robot_7` holds `CellInspectorAssignment`, a declared direct species of `U.SystemRoleAssignment` for `InspectorSystemRole`, in `Cell_3` during `Interval_T`. The current A.2.1 participant meanings and the direct species predicate state the positive test over the actual holder system, cell, and interval; a taxonomy or scheme is not an assignment participant. If an applicable non-assignment criterion or complete assignment closure basis exists and the available facts satisfy it, one claim-bearing episteme states the negative result and disposition 1 closes the check; there is no obtaining assignment occurrence to individuate. If no current direct-species predicate, applicability condition, or needed occurrence rule exists, return `missing-governor`. If the governor exists and the available case basis is sufficient to apply the positive test but it fails, return `factually unsupported`; if a fact needed to decide the test is unavailable, return `missing-information`. Neither a failed positive test nor either blocker is a third assignment polarity.

**Assurance branch for DPF and FPF authors.** DPF and FPF authors use this branch whenever they author a compound claim, reusable predicate definition, or relation-kind admission candidate, including a durable local compound claim that stops at disposition 2. In addition, verify:

- exact base patterns, definitions, editions, and applicability;
- selected substrate and constructor semantics;
- positive case, discriminating failure case, and receiving-use replay;
- one truthful definition `EntityOfConcern` when reusable semantics are published;
- dependency and currentness conditions;
- direct occurrence-identity and recurrence rules for every admitted relation kind;
- representation correspondence without representation-to-world collapse;
- naming only after the exact definition episteme, kind, or occurrence is settled;
- evidence relations under A.10, assurance results under B.3, gate results under A.21, and decision results under C.11 or the pattern whose Solution answers the exact decision claim.

Passing the assurance branch does not make evidence constitutive of relation obtaining. It makes the derivation and admission decision replayable for the declared use.

### A.6.RCD:4.8 - Stop and return deliberately {#stop-and-return-deliberately}

Stop at the first disposition that closes the named receiving use. Use this pattern when:

- a relied-on base relation or predicate definition changes;
- the selected substrate edition or constructor semantics changes;
- applicability, polarity, participant meaning, scope, time, or hidden-intermediate policy changes;
- the derivation becomes unreadable, computationally unsuitable, or unable to interoperate for the declared use;
- repeated consumers begin to need one reusable definition or stable occurrence identity;
- a purported primitive gains an accepted lossless derivation, or a derived kind loses a truthful identity rule.

`G.11` supplies currentness, dependency closure, and scoped refresh when a relied-on base definition, substrate edition, or applicability settlement changes. Re-evaluate only affected claims and dependent kinds; do not rebuild a global relation registry.

## A.6.RCD:7 - Conformance Checklist {#conformance-checklist}

1. **Blocked use.** The exact claim, check, decision, or continuation under repair is named.
2. **Participants first.** Actual referents and relation-participant meanings are recovered before constructor or notation choice.
3. **Direct-predicate stop.** `A.6.P` recovers the current subject predicate before compound derivation begins. If that predicate can state the needed affirmative, negative, or exact rule-qualified modal claim, use it and stop. If no needed predicate, applicability condition, or occurrence rule exists, return `missing-governor`; if the governor exists and the available case basis is sufficient to apply its positive test but that test fails, return `factually unsupported`; if a fact needed to decide the test is unavailable, return `missing-information`. A negative additionally needs an applicable non-obtaining criterion or complete closure basis and facts that satisfy it.
4. **Exact base.** Every base predicate names the exact pattern content or declaration that defines it and its obtaining law. The current case separately supplies the relevant facts or constituting history; an assertion or representation does not turn that rule into an obtaining occurrence.
5. **Substrate authority.** Every used constructor has semantics in the selected substrate; nontrivial, interoperable, proof-bearing, or reusable derivation pins the substrate and edition.
6. **Replay.** One positive case, one discriminating failure case, and the receiving-use replay agree.
7. **Lightest disposition.** Exactly one of the four dispositions closes the current use; later branches are not opened by habit.
8. **Claim polarity and occurrence boundary.** Direct and compound assertions may be affirmative, negative, or rule-qualified modal claims. The subject predicate defines the test, current case facts or constituting history determine its satisfaction, and the assertion states the result without creating an occurrence. The three blocker phrases in section 0.1 remain distinct and are not predicate values. Use A.6.REL only when a satisfied affirmative case has an occurrence whose identity a named use consumes.
9. **Definition identity and reuse boundary.** A subject-bounded compound-law episteme names the exact subject as its `EntityOfConcern` and states that reuse does not travel to another subject. A genuinely reusable predicate-definition episteme names the exact reusable predicate definition as its `EntityOfConcern`. Both state exact applicability and visible base dependencies.
10. **Definition/signature boundary.** A genuinely reusable predicate-definition episteme may satisfy ordinary A.6.0 `U.Signature` membership before relation-kind admission. It is not a `RelationSignature`, does not classify relation occurrences, and does not make one obtain.
11. **Derived-kind candidate and admission.** When a named use needs stable occurrence semantics, the A.6.RCD application records a derived-kind candidate plus a proposed direct subject settlement covering derivation and dependencies, obtaining, applicability, recurrence where current, and a direct occurrence-identity rule. Apply the admission predicates defined in `E.24` and `E.24.UK`, and the parsimony predicate in `A.11` when current. Neither the proposal nor a `SubjectPatternLocator` admits the kind. Only an admitted relation kind proceeds to an A.6.0 `RelationSignature`; ordinary `U.Signature` membership of a predicate-definition episteme is independent of that branch.
12. **Primitive-kind settlement.** A primitive candidate records the failed derivation, exact action-facing loss, independent uses, own obtaining and identity laws, and standalone direct pattern before A.11/E.24/E.24.UK admission can pass.
13. **Identity never absent.** Explicit individuation can be omitted from ordinary use; an admitted relation kind's identity rule cannot.
14. **Representation boundary.** Formula, query, graph, tree, path, diagram, row, and name remain representations or designators connected to independently recovered content.
15. **Neighboring claims.** Apply A.10 for evidence, B.3 for assurance, A.21 for gates, A.15 for work, C.11 or the exact decision pattern for decisions, E.17 for publication, F.18 for naming, and G.11 for currentness.
16. **Stop or return.** The result states the current stop and the exact dependency or use change that would reopen it.

## A.6.RCD:9 - Consequences {#consequences}

**Benefits.** FPF can state many exact compound claims without multiplying primitive relation kinds. Repeated subject semantics become reusable without confusing a definition with ontology. When occurrence semantics really matter, derived and primitive relation kinds enter with direct obtaining and identity laws rather than with syntax or names.

**Costs.** Authors MUST expose base dependencies and substrate semantics for nontrivial reuse. Authors of a direct subject pattern MUST supply the additional settlement content required by section 4.6 before a relation kind is admitted. Some familiar relation words remain local claims or exact blockers.

**Boundary.** This pattern reduces public primitive kinds and duplicate declarations; it does not reduce the number of true compound claims or obtaining base-relation facts.

## A.6.RCD:13 - Relations {#relations}

- **Entered from:** `A.6.P` only after exact participants are recovered and no current direct relation closes the named receiving claim.
- **Builds on:** `A.6.REL` for relation obtaining and occurrence identity; `A.6.5` for participant declaration discipline; `C.2.1` for local claims and predicate-definition epistemes; and the direct subject patterns supplying base relations.
- **Coordinates with:** `A.11`, `E.24`, and `E.24.UK` for parsimony, ontic settlement, and durable admission; `A.6.0` for possible ordinary `U.Signature` membership of a genuinely reusable predicate-definition episteme before relation-kind admission, and for `RelationSignature` only after the exact relation kind is admitted; `C.29` for derivation representations; `F.9` only when a consumed result relies on an obtaining Bridge between two exact F.17 cells and its separate bounded-use claim; the applicable plane relation and policy only when an exact ReferencePlane crossing is current; `B.3` only when an actual named assurance claim uses an applicable declared domain calculation for a Bridge-related penalty, with any resulting penalty confined to the calculated assurance result for that named use; `F.18` for names and designators after settlement; and `G.11` for dependency currentness and scoped refresh. Bridge and plane branches may coexist, but neither supplies or requires the other.
- **Does not replace:** direct subject relation patterns, `A.6.P`, `E.24.UK`, `C.29`, `F.18`, evidence or assurance patterns, or work and decision patterns.


## Dependencies {#dependencies}

- @fact:ENTERED-FROM Entered from: spec://ai.lev/fpf-spec/contract/A-6-P#root after direct-relation recovery. @status:spec/done
- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/A-6-REL#root, spec://ai.lev/fpf-spec/contract/A-6-5#root, spec://ai.lev/fpf-spec/contract/C-2-1#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/A-6-0#root, spec://ai.lev/fpf-spec/contract/A-11#root, spec://ai.lev/fpf-spec/contract/E-24#root, spec://ai.lev/fpf-spec/contract/E-24-UK#root, spec://ai.lev/fpf-spec/contract/C-29#root, spec://ai.lev/fpf-spec/contract/F-18#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-1-CSD#root, spec://ai.lev/fpf-spec/contract/A-1-SCR#root, spec://ai.lev/fpf-spec/contract/A-11#root, spec://ai.lev/fpf-spec/contract/A-12#root, spec://ai.lev/fpf-spec/contract/A-15-2#root, spec://ai.lev/fpf-spec/contract/A-15-3#root, spec://ai.lev/fpf-spec/contract/A-15-6#root, spec://ai.lev/fpf-spec/contract/A-15-8#root, spec://ai.lev/fpf-spec/contract/A-15-PROD#root, spec://ai.lev/fpf-spec/contract/A-2-8#root, spec://ai.lev/fpf-spec/contract/A-3-1#root, spec://ai.lev/fpf-spec/contract/A-3-4#root, spec://ai.lev/fpf-spec/contract/A-6-P#root, spec://ai.lev/fpf-spec/contract/A-6-P-WMR#root, spec://ai.lev/fpf-spec/contract/B-1-5#root, spec://ai.lev/fpf-spec/contract/C-29#root, spec://ai.lev/fpf-spec/contract/E-10#root, spec://ai.lev/fpf-spec/contract/E-10-ARCH#root, spec://ai.lev/fpf-spec/contract/E-18#root, spec://ai.lev/fpf-spec/contract/E-18-NET#root, spec://ai.lev/fpf-spec/contract/E-24-CD#root, spec://ai.lev/fpf-spec/contract/F-12#root, spec://ai.lev/fpf-spec/contract/F-18#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/A-6-RCD
