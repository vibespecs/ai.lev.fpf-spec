# C.2.P.DR - Repair Claims Based on Declarative Form Alone (Declarative Representation Precision Restoration): depth {#depth}

<status stage="spec" state="done"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## C.2.P.DR:5 - Worked slices {#worked-slices}

### C.2.P.DR:5.1 - Graph path in a transformation-flow structure {#graph-path-in-a-transformation-flow-structure}

Wording: "The P2W path routes the team from principle to work."

Repair:

```text
DeclarativeRepresentationRepair:
  VisibleExpressionOrArtifact: P2W graph expression with a highlighted path or path slice
  CurrentDirectObjectOrRelation: exact E.18 `PathSlice` and E.18.1 carry-through relation among the named records when those objects are current
  RepresentationOrCorrespondenceUse: proposed correspondence from this P2W graph expression to the exact E.18 `PathSlice`; C.29 lens-use account not yet supplied
  SourceOrPublicationRelation: none
  TemptingStrongerActionClaim: ordered work route for the team
  RecoveredGoverningPattern: E.18.1, with A.15.2 or A.15.1 only if planned or dated work is current
  RetainedUse: selected graph path and carry-through relation for inspection
  BlockedStrongerActionClaim: no work route or prescribed workflow by path shape alone
  StopOrReopenCondition: recover or cite a C.29 lens-use account that states the preserved and lost structure and bounds the intended use; until then this representation branch is an incomplete rewrite, and claim-bearing use of the proposed correspondence is blocked; reopen when path, source currentness, graph edition, or intended work relation changes
```

A graph publication or pattern publication remains a separately governed publication object. If one is current, state its exact source or publication relation and participants in the neighbouring claim; neither publication object belongs in `SourceOrPublicationRelation` by mention alone.

### C.2.P.DR:5.2 - Evidence path near release {#evidence-path-near-release}

Wording: "The evidence path authorizes release."

Repair: name the claim or bounded use and recover the descriptive evidence-provenance path through `A.10`, with each cited direct relation established under its own subject pattern. Release, permission, or gate passage requires the authority, gate, or release pattern that defines or constrains that claim. This pattern is used only if `path` wording itself is causing the representation to be overread as a permission route.

### C.2.P.DR:5.3 - Query plan and access path {#query-plan-and-access-path}

Wording: "The query plan calls the production work sequence."

Repair: recover whether the query plan represents optimizer choices, expresses claims about an exact method, presents a formal substrate, supplies a source cue or evidence relation, states a work plan, or records an actual query run. If it only represents query-evaluation choices, stop at the representation. Use A.3.1 for a reusable semantic way-of-doing claim. Use A.3.2 only when the claim-bearing episteme passes the MethodDescription membership guard in 4.4. Use A.15.1 for a performed query run, together with the exact evidence or source-use relation when that later claim is current.

### C.2.P.DR:5.4 - Dashboard predicate {#dashboard-predicate}

Wording: "The dashboard green path lets the release move."

Repair: recover dashboard face, source relation, status or state bearer, value frame, source currentness, and gate or release claim. The dashboard may be a publication face and source cue. Recover release permission through the applicable gate decision (`A.21`) or authority relation, including any source contribution required by its governing rule.

### C.2.P.DR:5.5 - Pattern relation {#pattern-relation}

Wording: "This pattern exits to A.10."

Repair: if the current relation is "use `A.10` when an evidence relation or provenance relation is current", write that declarative boundary. Keep ordinary ownership or navigation wording when its relation and participants are clear. Use exit, receiver, route, owner, home, dispatch, or call language to assert action or control only when the pattern is actually about an action occurrence, work plan, control mechanism, or communication relation that has those semantics.

### C.2.P.DR:5.6 - Solver algorithm {#solver-algorithm}

Wording: "The solver algorithm is the mechanism."

Repair: first identify the direct object or relation, any representation use, and which claim is current. A solver configuration may represent claims carried by an episteme that qualifies as `U.MethodDescription` only after the 4.4 membership guard; the configuration is not that episteme by file form or executability. The reusable semantic way of solving may be `U.Method`; the MILP formulation may expose a formal substrate and mathematical-lens use; a reusable operation algebra with laws and admissibility predicates may be `U.Mechanism`; a solver run may be `U.Work`; and a run result may support another claim through its direct evidence relation. Select A.6.1 and E.20 only when their mechanism fields are present in the current claim.

### C.2.P.DR:5.7 - Reactor-cooling flow graph {#reactor-cooling-flow-graph}

Wording: "The preserved heat-flow path authorizes the valve change."

Repair:

```text
DeclarativeRepresentationRepair:
  VisibleExpressionOrArtifact: reactor-cooling heat-flow graph with one highlighted preserved path
  CurrentDirectObjectOrRelation: exact E.18 heat-flow path or `PathSlice`; keep boundary conditions and any flow valuation under their subject patterns
  RepresentationOrCorrespondenceUse: proposed correspondence from this reactor-cooling graph rendering to the exact selected E.18 heat-flow `PathSlice`; C.29 lens-use account not yet supplied
  SourceOrPublicationRelation: none
  TemptingStrongerActionClaim: graph path authorizes physical valve-change work
  RecoveredGoverningPattern: E.18 and C.29 for graph and lens use; A.21, A.10, A.15.2, and A.15.1 only if gate, evidence, work plan, or dated work is current
  RetainedUse: graph structure for comparison, model review, and source-finding
  BlockedStrongerActionClaim: no release, gate passage, physical intervention, or work occurrence by highlighted path alone
  StopOrReopenCondition: recover or cite a C.29 lens-use account that states the preserved and lost structure and bounds the intended use; until then this representation branch is an incomplete rewrite, and claim-bearing use of the proposed correspondence is blocked; reopen when gate decision, source currentness, measurement boundary, or work plan becomes current
```

An engineering-review publication and a gate record remain separate objects. State any exact source or publication relation with its participants, and keep any gate relation under its subject pattern; neither object belongs in `SourceOrPublicationRelation`.

### C.2.P.DR:5.8 - CRISPR guide-selection table {#crispr-guide-selection-table}

Wording: "The guide-selection table approves the edit."

Repair:

```text
DeclarativeRepresentationRepair:
  VisibleExpressionOrArtifact: CRISPR guide-selection table with off-target scores and candidate ranking
  CurrentDirectObjectOrRelation: candidate-guide comparison and exact characteristic values under C.16 or A.19; use A.10 to recover any independently established direct support relation needed for reliance
  RepresentationOrCorrespondenceUse: proposed correspondence from this table's candidate and off-target-score representation elements to the exact candidate-guide comparison and exact characteristic values named above; C.29 lens-use account not yet supplied
  SourceOrPublicationRelation: none
  TemptingStrongerActionClaim: ranked row approves biological intervention
  RecoveredGoverningPattern: C.16 or A.19 for characteristics when current; A.10 for evidence; A.15.2 for experimental work plan; A.21 or authority pattern only if approval or gate claim is current
  RetainedUse: source-finding, candidate comparison, and constraint review
  BlockedStrongerActionClaim: no edit approval, work occurrence, safety claim, or gate passage from table rank alone
  StopOrReopenCondition: recover or cite a C.29 lens-use account that states the preserved and lost structure and bounds the intended use; until then this representation branch is an incomplete rewrite, and claim-bearing use of the proposed correspondence is blocked; reopen when protocol, gate decision, evidence path, lab classification or assignment, exact GrantedPermissionRelation@Context or direct authority result, or dated lab Work becomes current; unresolved “role authorization” goes to E.10.ROLE, and an unsupported stronger permission or authority claim returns missing-governor
```

A lab notebook, protocol publication, source episteme, and review record remain separate objects. State an exact source or publication relation and its participants only when it obtains; none of these objects belongs in `SourceOrPublicationRelation` by mention alone.

## C.2.P.DR:7 - Common anti-patterns {#common-anti-patterns}

| Anti-pattern | Symptom | Repair |
| --- | --- | --- |
| Path word deletion | Every `path` is replaced or avoided. | Preserve legitimate `A.10`, `E.18`, carrier, mathematical, URL, and quoted-source path uses; repair only hidden stronger claims. |
| Imperative metaphor as ontology | Representations "route", "call", "dispatch", "receive", "invoke", or "flow" by prose habit. | Separate the visible expression, direct object or relation, exact representation use or `none`, and blocked stronger action claim; then write the direct relation declaratively. |
| Algorithm as method or description by form | Code, solver model, proof script, workflow, SOP, recipe, protocol, or diagram form is treated as proof of `U.Method` or `U.MethodDescription`. | Use A.3.1 only for the recovered reusable way of doing. Use A.3.2 only for an already identified claim-bearing episteme with one admitted `U.Method` as exact `EntityOfConcern` and a substantive way-of-doing claim; otherwise keep the representation or other claim with its subject pattern. |
| Mechanism by prestige | `mechanism` is used because the word sounds more rigorous than method or algorithm. | Require operation algebra, laws, admissibility predicates, transport, audit, realization, or governing-definition assignment. |
| Dashboard as gate | Green status, dashboard tile, score, or status label becomes permission or release. | Recover source relation or publication relation, state-family value, evidence relation, and gate or release pattern when current. |
| Pattern dispatcher | Pattern relations are given action or control effects through route, exit, receiver, call, owner, or home wording. | Write declarative neighboring-pattern boundary or application relation; use `E.8` and `F.19` together when both publication-form and phrase-apparatus claims are live, or use the one subject pattern when only one claim is live. |
| Generic representation theory | The repair tries to classify every representation in FPF or becomes an API pattern, schema pattern, legal framework, workflow framework, or generic admissibility pattern. | Stop at the representation-use field set and use the subject pattern for the current claim. |

## C.2.P.DR:10 - SoTA-Echoing {#sota-echoing}

This pattern uses external sources only for the representation-overread repair question. They do not replace FPF ontology, and older famous sources are lineage or contrast unless a current source below supplies the contemporary payload.

| Exact source or practice anchor | Source-use function or relation | What it changes here |
| --- | --- | --- |
| `E.10`, `E.10.ARCH`, and `C.2.P` | Current FPF precision-restoration architecture. | This pattern is a bounded child realization under `C.2.P`, not a new umbrella pattern. |
| `A.10` and `E.18` | Local FPF subject patterns for evidence paths, provenance paths, transformation-flow graph paths, and path slices. | Path wording is legitimate when the exact evidence or provenance relation, graph path, or `PathSlice` is current; the defect is stronger overread. |
| `A.3.1`, `A.3.2`, `A.6.0`, `C.29`, `A.6.1`, `E.20`, `A.15.2`, and `A.15.1` | Local FPF method-like and algorithm-like wording discipline. | The repair identifies the direct object or relation, current claim, and any representation use before choosing method, qualifying method-description episteme, formal substrate, mechanism, work plan, or work occurrence; representation form alone chooses none of them. |
| Stefano Gogioso, Vincent Wang-Mascianica, Muhammad Hamza Waseem, Carlo Maria Scandolo, and Bob Coecke, "Constructor Theory as Process Theory", arXiv:2401.05364, EPTCS 397, 2023; David Deutsch and Chiara Marletto, "Constructor theory of time", arXiv:2505.08692v3, revised 2026-06-05. | Current SoTA decision payload for transformation-theory and process-theory repair of computation, method, and dynamics wording. | Computation, information, dynamics, and procedure wording is interpreted through possible or impossible transformation and compositional-process claims when that claim is current, not through software notation or ordered instruction prose first. |
| Roger Bosman, Birthe van den Berg, Wenhao Tang, and Tom Schrijvers, "A Calculus for Scoped Effects & Handlers", Logical Methods in Computer Science 20(4), 2024, arXiv:2304.09697; Cristina Matache, Sam Lindley, Sean Moss, Sam Staton, Nicolas Wu, and Zhixuan Yang, "Scoped Effects as Parameterized Algebraic Theories", ESOP 2024 extended version, arXiv:2402.03103. | Current SoTA decision payload for effectful computation and programming-model wording. | Operation syntax, semantic handling, scope, resources, equations, and effect information remain separable; pure-function slogans and imperative-declarative slogans are not enough. |
| Francesco Chiariello, Valeria Fionda, Antonio Ielo, and Francesco Ricca, "Direct Encoding of Declare Constraints in ASP", Theory and Practice of Logic Programming 25, 2025, arXiv:2412.10152; Alessandro Berti et al., "OCEL (Object-Centric Event Log) 2.0 Specification", arXiv:2403.01975; Lien Bosmans et al., "Dynamic and Scalable Data Preparation for Object-Centric Process Mining", arXiv:2410.00596. | Current SoTA decision payload for process-model, trace, workflow, and event-record wording. | Constraint, event, object, relation, data model, ingestion, transformation, storage, and analysis claims are recovered separately before a method, work plan, work occurrence, evidence, or gate claim is accepted. |
| Aleksei Tiurin, Chris Barrett, Dan R. Ghica, and Nick Hu, "Equivalence Hypergraphs: DPO Rewriting for Monoidal E-Graphs", arXiv:2406.15882, v2 revised 2025-05-20. | Current SoTA decision payload for graph, equivalence, and compositional-representation wording. | Graph, equality, equivalence, and rewrite objects keep their direct kinds; any representation relation to them remains separate from instruction order, method, work, or action claims. |
| Robert Kowalski 1979; E. F. Codd 1970; Selinger et al. 1979; van der Aalst, Pesic, and Schonenberg 2009; Van Roy and Haridi 2004; Deutsch 2013; Deutsch and Marletto 2015. | Historical lineage or contrast only. | These sources explain why the overread is recognizable; they do not carry current SoTA weight for this pattern by age, fame, or popularity. |


## C.2.P.DR:End {#end}
