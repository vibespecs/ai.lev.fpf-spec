# E.10.ROLE - Recovering What “Role” Means in the Current Claim: depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## E.10.ROLE:5 - Archetypal Grounding — Worked Slices {#archetypal-grounding-worked-slices}

### E.10.ROLE:5.1 - Alice Is Reviewer {#alice-is-reviewer}

“Alice is reviewer” may stay as readable recognition prose when no technical classification claim is consumed. If only the local kind matters, identify `ReviewerSystemRole` through C.3 and A.2. If a technical classification judgment matters, use A.2 and C.3.2 and keep Alice, `ReviewerSystemRole`, the current `KindSignature` edition, the context slice, and the `true | false | unknown` result recoverable. If assignment identity matters, first name the declared assignment species `JournalReviewAssignmentRelation` and establish that its direct predicate obtains for the actual participants, including Alice as holder, under the stated applicability. Only then identify `ReviewAssignment-82` as the occurrence and state its extent. A roster, appointment label, description, or evidence item may support the assignment claim but does not make the assignment obtain. If performed Work matters, first recover Alice's A.13 core for this action and independently admit `ReviewWork-82` under A.15.1. Because this branch also says that Alice performed the Work under `ReviewAssignment-82`, F.6 afterward relates the already admitted Work to that same assignment. Classification, assignment, Work, and attribution remain separate. None follows merely from the ordinary sentence. A short projection may omit an assignment identifier unused by its receiving claim only when every relation the claim consumes remains recoverable.

### E.10.ROLE:5.2 - A Report Plays a Role in Approval {#a-report-plays-a-role-in-approval}

The report is an episteme. For the evidence-use reading established by the source, write “reviewers used Report-R as evidence for ApprovalClaim-C”, then use A.10 for the evidence-provenance account and B.3 only when an actual named assurance claim is current, including when an applicable material-reliance threshold requires that claim.

### E.10.ROLE:5.3 - API Provider Role {#api-provider-role}

“The API role is provider” does not yet reveal which claim is meant. It may hide several claims, but the wording alone does not establish that; recover the intended claim before selecting and applying a rule. First ask whether a provider System is current and whether its classification under a local provider system-role kind matters. If the assignment itself matters, name its declared assignment species and the obtaining occurrence separately; do not infer either from root-family typing or the word *role*. Provision, service, declaration, interface, schema position, publication, promise, and access claims each use their own pattern. Only when provider Work is current, recover every precise performer's A.13 core and independently admit the dated Work under A.15.1. Add F.6 afterward only if this provider account also needs precise assignment-bound attribution through the same obtaining assignment.

### E.10.ROLE:5.4 - Passive Test Article {#passive-test-article}

A passive test article may independently pass A.1 and be classified under `TestArticleSystemRole`. If an assignment claim matters, name its declared assignment species before identifying an occurrence. Neither classification nor assignment makes the article an agent or performer. The role-bearing source claim to recover is: `TestArticle-7 participates passively in TestWork-9 during TestInterval-9`; its intended participant order is article, Work, then applicability interval. No current pattern supplies a direct passive-participation predicate with those participants, applicability, and occurrence identity, so the current result is the A.6.RCD `missing-governor` for that exact attempted claim. Any tester or test-rig Work first reuses every precise performer's A.13 core and is independently admitted under A.15.1; add F.6 only when the tester account also needs precise assignment-bound attribution. A short projection may omit an unused assignment identifier, but it keeps the article, Work, interval, and missing relation recoverable.

## E.10.ROLE:6 - Bias-Annotation {#bias-annotation}

Lenses: **Gov**, **Arch**, **Onto/Epist**, **Prag**, **Did**. Scope: **Universal** for claim-bearing uses of *role* that enter this pattern; ordinary and quoted non-uses remain outside it. The pattern deliberately favors Onto/Epist precision, which can tempt an author to expand every sentence into technical apparatus. Writing the ordinary sentence first, adding only distinctions used by the receiving claim, and stopping when the applicable direct rule is clear preserve Prag and Did usefulness, while the separate branches preserve Gov and Arch boundaries.

## E.10.ROLE:8 - Common Anti-Patterns and How to Avoid Them — Role-Word Repairs {#common-anti-patterns-and-how-to-avoid-them-role-word-repairs}

| Anti-pattern | Repair |
|---|---|
| Replace every *role* with `SystemRole` | Recover the current claim first; use `SystemRole` morphology only for an exact local system-role kind. |
| Replace every *role* with *position* | Distinguish system classification, assignment, relation participation, declaration place, representation position, and ordinary wording. |
| Send every case through A.6.RSIR | Use RSIR only for direct-relation, declaration, interface, operation, or representation recovery. |
| Treat an episteme's use as a work assignment | Recover its evidence-use, source-use, publication-use, reliance, status-use, or other direct relation. |
| Expand a short sentence into a full ontology bundle | Add only the distinction consumed by the receiving claim, then stop. |
| Create a durable list of all possible senses | Keep the branch table as recovery examples; admit objects and relations only through their direct patterns. |

## E.10.ROLE:10 - Rationale {#rationale}

The recurring problem is word-sense recovery, not a missing universal role category. FPF therefore makes an internal architectural choice: recover the claim expressed in this use, then use the direct pattern for the recovered kind, assignment, participant, declaration place, representation position, or relation. The trigger word neither supplies that ontology nor makes the recovered claim obtain.

The pattern therefore stays thin. It supplies an entry and a stop rule, while C.3, A.2, A.2.1, A.6.RSIR, A.6.5, C.29, A.10, A.15, and other direct patterns retain their own predicates and identity laws.

## E.10.ROLE:11 - SoTA-Echoing {#sota-echoing}

No external source governs this design, and FPF imports neither an external upper ontology nor its terminology. Two current lines provide the main SoTA comparison. The [gUFO account](https://arxiv.org/abs/2603.20948) and [OntoUML role documentation](https://ontouml.readthedocs.io/en/latest/classes/sortals/role/index.html) and [specification](https://ontology.com.br/ontouml/spec/) test anti-rigidity, external dependence, and the connection to a base kind. [Engineering-function work](https://doi.org/10.3233/SW-223188) tests the separation among function, behavior, and capability. FPF uses both lines as bounded comparators and adapts their tests to keep holder identity, changing classification, assignment, capability, functioning, and Work distinct.

Other comparisons have narrower uses. FPF adapts [Toyoshima's role facets](https://doi.org/10.3233/AO-210244) as diagnostic questions about position, specification, and potential. It uses [DOLCE](https://doi.org/10.3233/AO-210259), [BFO](https://www.iso.org/standard/74572.html), and [CCO](https://arxiv.org/abs/2404.17758) as bounded comparators for dependence and the distinctions among persistent entities, processes, roles, dispositions, capabilities, and functions. It keeps [DnS](https://doi.org/10.1007/978-3-540-39964-3_44) as lineage for separating descriptions from entities participating in described settings. These comparisons supply distinctions and counterexamples, not FPF kinds or assignment identity.

Within FPF, E.10 and E.10.ARCH define trigger recognition and recovery distribution. A.2, C.3, and C.3.2 define system-role kinds and classification judgments; A.2.1 defines assignment occurrences; A.6.RSIR defines direct-relation, declaration, interface, and representation recovery; and F.19 constrains the final plain wording. Together they define the ordinary-sentence-first, thin entry, but cannot supply a missing direct relation or establish that the recovered claim is true. Reopen this choice if one of those patterns changes that boundary, or if a stronger current comparison exposes a case in which the thin entry cannot preserve both plain language and whether the recovered relation obtains.


## E.10.ROLE:End {#end}
