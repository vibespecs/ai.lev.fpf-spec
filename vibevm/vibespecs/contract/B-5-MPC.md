# B.5.MPC - Connect Physical, Mathematical and Computational Reasoning {#root}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method pattern
> **Status:** Draft
> **Normativity:** Normative unless marked informative

## B.5.MPC:1 - Problem frame {#problem-frame}

**Use this when** a physical question needs contributions from mathematics and computation, and their results do not yet form an interpretable answer together. You may be choosing a robot command, determining whether a gear arrangement can turn, or organizing entry to a room with a finite stock of cards. The difficulty is to connect what the physical arrangement does, what the mathematical result establishes, and what the procedure and its execution actually produce.

Begin with the difference the answer should help you understand or make possible. Take one available contribution and explain what it would have to mean, and what else would have to hold, for that contribution to answer the question. Work the first missing connection far enough to obtain a consequence or locate the next missing contribution. For a motion command, this might already reveal that the supplied count concerns motor revolutions while the distance model concerns wheel revolutions.

The result is a connected solution, a useful conditional consequence or bound, or a particular missing connection that directs the next inquiry. This pattern specializes B.5's choice and connection of inquiry contributions for this joint physical, mathematical and computational difficulty. It governs the reasoning that connects those contributions. Physical laws, mathematical constructions, algorithm design and the engineering of an executing arrangement supply their respective subject content.

This is an epistemological and methodological synthesis. The epistemological question is what the connected contributions allow us to know: what follows from the constructions and premises, and how those consequences bear on the physical situation. The methodological question is how agents obtain and apply that knowledge, divide the work and change their methods. A result can support a physical change, expose a limitation or make a further question worth pursuing.

A practitioner needs enough preparation to recover the question, follow the meanings of the important quantities and operations, and recognize where specialist help is needed. The worked cases explain their elementary algebra, graph and counting constructions. A more demanding application can require additional physical theory, mathematics, computation or measurement expertise; obtain that contribution with its explanation when it is missing.

Use an already adequate calculation, implementation or operating procedure directly when its connection to the intended physical use is settled. A proof or bound can answer a physical design question before implementation is worthwhile. For an actual performance claim, add the observations, measurement relation and evidence needed for that claim; a conditional construction alone answers only what follows under its assumptions.

## B.5.MPC:2 - Problem {#problem}

Individually correct contributions can fail to support a joint result. A physical model may concern accumulated wheel rotation, a mathematical variable may represent orientation modulo one turn, and a program may accept an absolute target. Each account can be consistent while their composition loses the displacement that the user requested.

The same difficulty occurs without numerical approximation. A graph can correctly encode a chosen contact list, and a program can correctly colour that graph, while the contact list omits an actual mesh. A count invariant can be proved while the proposed admission procedure creates two independent stocks of cards. Improving the proof or the program leaves the missing physical correspondence untouched.

A simple division into “physics first, mathematics second, implementation last” also fails when a later contribution exposes an earlier omission. The interface may require initial state that the first model discarded. A measurement may distinguish fewer cases than the calculation assumes. A mathematical obstruction may make further computation unnecessary. The practitioner needs a way to construct the dependencies, use an available contribution at its point of need, and return a failure to the contribution that can change it.

## B.5.MPC:3 - Forces {#forces}

| Force | Working tension |
| --- | --- |
| Shared answer and distinct expertise | Specialists can work independently on contributions, while their results must concern compatible participants, assumptions and operations. |
| Useful simplification and physical interpretation | Omitting detail can make a problem tractable; an omitted distinction can determine the requested action. |
| Constructive freedom and justified consequence | New models, expressions and procedures can open a useful route; their decisive properties require the relevant physical or mathematical grounds. |
| Abstract result and executing means | A computation can be correct for its stated inputs while the proposed apparatus cannot prepare, represent or execute those inputs. |
| Reuse and change | Existing results save work, but their use depends on the premises and interpretations that the new question consumes. |
| Explanation and available effort | A person or team needs enough understanding to use and question contributions without reconstructing every discipline before an ordinary decision. |

## B.5.MPC:4 - Solution {#solution}

Construct the answer by connecting the contributions it actually needs. For each connection, identify the supplied result, the receiving operation and the condition that makes the result usable there. Follow those meanings through a small instance. If the connection is missing, construct it, obtain it from a suitable contributor, or return the particular missing result that prevents the next move.

The long mantra keeps the whole question available while attention moves between contributions:

**Orient by the physical question → propose the relevant physical account → construct a mathematical question and its interpretation → obtain a result and, where needed, a computation → connect its execution and observations to the intended quantities → return the consequence to the physical question → choose the useful action or the next missing contribution.**

The arrows recall result dependencies. They do not prescribe the order in which people must discover, receive or develop every contribution. A ready theorem, algorithm, measurement or physical mechanism can be the first available input.

### B.5.MPC:4.1 - Recover the physical difference the answer should resolve {#recover-the-physical-difference-the-answer-should-resolve}

Identify the thing or situation being understood or changed. Say which difference would make an answer useful: a displacement within a stated tolerance, the possibility of coupled rotation, a capacity bound during entry, or another consequence the work needs. Include the relevant boundary and operating conditions when changing them could change the answer.

Then recover what is already available. An engineer may have a trusted motion model but an unfamiliar command interface. A mathematician may have an odd-cycle theorem and ask which physical arrangements its obstruction describes. A room attendant may have a reliable card procedure and want to extend it to a second entrance. Enter through that available contribution and recover only the other results needed to answer the question.

Use B.5:4.1 when the question itself needs formation or revision. B.5.4 helps recognize the participants and relations of an explained concept in a concrete situation. If the receiving use is still unclear, work one small consequence of the available result and ask what it would let someone decide or do. Retain a theoretical question when its answer could enable a worthwhile construction, explanation or later inquiry.

### B.5.MPC:4.2 - Propose the physical account and the observations it needs {#propose-the-physical-account-and-the-observations-it-needs}

Identify the participants, interactions and configurations that could determine the requested difference. Give separately used quantities their participants and reference conditions: the robot's distance to a wall before motion, its distance afterwards and its displacement are three quantities, even though each is called a distance. Start from the arrangement and relevant subject knowledge. For a rolling robot, distinguish wheel, motor, transmission and ground contact. For gears, distinguish an actual contact from proximity in a drawing. For admission cards, distinguish a material card, its holder, the room boundary and the permitted transfers.

State the applicable physical or operating rules. Explain why a rule supplies the needed relation and where it is an assumption. Wheel rotation yields a distance relation only under the chosen rolling and geometry conditions. Exclusive possession of a card supports an admission limit only when the entrance procedure connects possession to entry and return. A.3.3 helps construct configurations, retained state and allowed continuations; the subject practice supplies the laws and mechanisms those continuations use.

Choose a sufficient account for the present question. A direction or impossibility result may need less physical detail than a trajectory, speed or load calculation. Make an omitted interaction explicit when it could defeat the inference: slip changes wheel travel, a moving gear carrier changes relative rotation, and uncontrolled entry breaks the visitor-to-card association.

When observations supply an input or test a consequence, construct the relation between the sought quantity and the indication. Use C.16:5.3 and C.16:5.4 for the measurement method and model. Motor counts can indicate motor rotation under an encoder account; using them to establish travel additionally consumes the transmission and ground-contact account. If the available indication cannot distinguish the cases needed by the question, obtain a different observation, use an adequate bound, or change the question.

Return a proposed physical account and its consequences under stated conditions. An unknown interaction or calibration is a useful missing contribution when it determines which mathematical question can be constructed.

### B.5.MPC:4.3 - Construct an interpretable mathematical question and expression {#construct-an-interpretable-mathematical-question-and-expression}

Choose mathematical objects and operations that retain the distinctions needed by the physical question. State what their important elements mean. For instance, let a vertex denote one particular gear, an edge denote a specified mesh, and a colour denote the sign of rotation when viewed from one common side. A colour number has meaning through that interpretation.

Construct the relation that connects the physical rules to the mathematical constraints. Derive a distance per motor increment from wheel circumference and transmission ratio; derive an opposite-colour constraint from the external-contact rule; derive a count invariant from a fixed stock and its permitted transfers. C.29:4.1 supplies the general correspondence-and-return method. When an operation or a compressed representation must preserve a result, use C.29.1 to compare performing the source operation and then transferring its result with transferring the inputs and then performing the receiving operation.

Work the distinction that could defeat the representation. A wheel orientation repeats after one turn; accumulated travel can continue to increase. A graph of opposite-direction contacts answers a different question from a graph in which an edge merely means “these parts are connected.” If two physical cases receive one mathematical representation but require different answers, retain their distinguishing information, restrict the cases or seek a weaker consequence.

Keep the relation available when the question changes. Identify which quantities are now given and which must be obtained, then derive the computational direction that serves that question. Under a model `d = v*T` and `v = k*u`, where u is a motor command setting, positive k, u and T permit `T = d/(k*u)` for a duration question or `u = d/(k*T)` for a command question. Obtain k and the range in which the speed model applies from the physical account. The device's word “power” needs its interface meaning; u is not assumed to be physical power in watts. A resulting command outside the supported range returns a realizability question.

For a conditional example, let u be dimensionless and let `k = 0.2 m/s`. A distance `d = 1 m` at `u = 0.5` takes `T = 10 s`. Changing the requested duration to `T = 5 s` requires `u = 1`. If the available range is `0 < u <= 0.8`, the shortest duration under this model is `1 / (0.2 * 0.8) = 6.25 s`. Returning that bound lets the requester change the deadline or seek a different realization.

An equality constrains the quantities in this model. A program assignment changes a stored value according to its execution rules. Construct the needed assignments or solver from the relation after selecting the givens and unknowns; C.29.2 supplies that formulation Method.

Make an expression that supports the next operation. Use A.6.3.RT:4.1 to express the givens and constraints under an available scheme and compare the result with its source. Put units and participant names where their absence permits the wrong operation. Keep a shared quantity recognizable across expressions, such as the same wheel revolution in the transmission ratio and circumference relation.

Notation can contribute to obtaining the result. A table can expose mutually exclusive card states; a graph can make a closed contact path traceable; a labelled equation can reveal the missing subtraction of an initial position. The subject Method supplies the construction or inference performed with those expressions. If the available scheme cannot express the needed distinction, change the scheme or obtain notation-design work before treating its expressions as adequate.

### B.5.MPC:4.4 - Obtain a sufficient consequence or construct its computation {#obtain-a-sufficient-consequence-or-construct-its-computation}

Choose the result the use needs: a value, distribution, statistic, bound or property of ongoing behavior. A witness can establish one feasible arrangement; a counterexample can refute a general claim; a proof can establish an obstruction; a bound can settle a threshold decision. Compute an exact numerical answer only when that answer contributes to the use.

When a procedure is needed, construct its inputs, retained state, elementary operations and output interpretation. Explain how it obtains the mathematical result and why it terminates, or which property it preserves during continued interaction. C.29.2 supplies this formulation work; the relevant algorithmic or mathematical Method supplies the actual construction and its argument. B.5:4.2 and B.5:4.3 help recover a construction or a decisive proof step that the available explanation leaves inaccessible.

Trace one instance with its meanings intact. In a two-colouring procedure, a waiting list records vertices still to be processed, while parent links can reconstruct a failed closed path. In a motion calculation, the integer is a count of a particular kind of increment. In an admission procedure, taking a free card changes a finite state and determines whether an entry may proceed.

For a numerical approximation, carry the error that can affect the physical use. Separate rounding of a computed command from uncertainty in radius, calibration or physical response. For a resource claim, include the cost of obtaining the input, representing it and interpreting the output when those costs matter. Counting one graph-edge inspection as one operation is useful under an adjacency-list cost model; it does not estimate the effort of discovering the actual contacts.

Use a supplied proof or computation when its premises, meaning and relevant resource conditions fit. If a necessary construction remains unknown, state the missing operation and what it must connect. C.39 supplies the search for or development of a missing way. A conditional answer or a less demanding bound can finish the current question while that larger construction remains open.

### B.5.MPC:4.5 - Connect the computation to preparation, execution and observation {#connect-the-computation-to-preparation-execution-and-observation}

Begin with the abstract input and explain how the proposed arrangement represents it. Then identify the system actions that perform the operations and the observation or final state from which the result is read. Use C.29.3 for this realization comparison.

Compare two routes for the same input:

~~~text
abstract input → stated computation → abstract result
abstract input → prepared system → system operation → interpreted result
~~~

The comparison asks whether the second route returns the equality, bound, statistical agreement or behavioral property that the receiving use needs. Input preparation and output interpretation can use different relations. Preparing a motor command and reading robot displacement are different operations; counting free cards and authorizing one transfer use different aspects of the same arrangement.

Recover range, units, initial state, ordering and completion conditions at the point where they affect that comparison. A signed command field cannot carry every positive integer. A command meaning “add this displacement” differs from one meaning “reach this position.” A material card available for transfer cannot simultaneously be assigned to another visitor.

Include the timing and retained physical state that the comparison consumes. When a controller is paused for debugging, determine which physical processes continue and which command remains active. Observe or replay the operation with the timing it needs, or interpret the changed run under its changed conditions. Establish the event that completes the requested physical action; program termination, a command acknowledgement and motor stopping can occur at different times. For an observation, include a settling interval or other preparation when the measurement relation requires it.

For a design question, use the stated model of the executing arrangement and return a conditional realization. For a claim about what happened, obtain the corresponding observations and their interpretation. A command receipt can establish that a command was accepted while leaving its successful physical completion open.

Use an existing adequate implementation directly when this comparison is already settled for the receiving use. A manual procedure, analog apparatus or controlled material transfer can supply an execution. Its adequacy follows from its permitted operations and interpretation, not from whether it contains digital software.

### B.5.MPC:4.6 - Keep joint requirements and alternative routes distinguishable {#keep-joint-requirements-and-alternative-routes-distinguishable}

Recover dependencies by asking, for each needed result, “What results and conditions make this operation possible, and what other operation could supply the same receiving need?” Keep the answer with the actual derivation, diagram or working explanation. A short case may need only a sentence; a shared design may need an explicit dependency diagram.

An **AND dependency** means that contributions are needed together for the stated inference. The robot's distance per motor increment uses the effective wheel radius, transmission ratio and increments per motor revolution together. Replacing any one can change the command.

An **OR alternative** is a different sufficient way to obtain the result needed by the receiving use. A proved upper bound and an exact computation can be alternatives for deciding whether a limit can be exceeded. Each route retains its own assumptions. Two different approximations do not become sufficient alternatives merely because both return a number.

For a conditional physical consequence, one useful small rendering is:

~~~text
applicable physical account
AND mathematical interpretation
AND (sufficient direct consequence OR sufficient interpreted computation)
→ consequence for the physical question
~~~

The computational branch additionally depends on a procedure and an adequate realization for any claimed execution. A claim about observed physical behavior adds the observations and measurement relation it consumes. These are different claims and can end the work at different places.

Keep a shared premise attached to every contribution that consumes it. Both an analytical calculation and a numerical simulation can depend on the same no-slip assumption. Switching between them does not remove that dependency. Conversely, when an upper bound already answers the decision, the exact optimizer need not be obtained.

Enter a ready result at the place where it is used. Recover its inputs and conditions backward, then continue forward with its consequence. When a missing input blocks one route, compare another sufficient route using the available inputs. Do not combine an output from one route with the assumptions of another without establishing their compatibility.

A failed connection can send the inquiry back to its physical account, mathematical construction, notation, procedure, realization or question. Use B.5.MPC.R to locate the incompatibility, construct a sufficient repair and carry it through the affected contributions. If several causes remain compatible with the observations, obtain a discriminating contribution or use a sufficient conditional result. B.5.RA supplies argument recovery and B.5.RR supplies general reasoning revision; C.29.1, C.29.2 and C.29.3 supply the transfer, formulation and realization methods respectively. Retain unaffected contributions whose conditions and meanings still hold.

### B.5.MPC:4.7 - Return the consequence and choose what to do with it {#return-the-consequence-and-choose-what-to-do-with-it}

Explain the result in the original physical terms. A count becomes a modeled displacement; an odd cycle becomes a set of contacts that prevents the stipulated nonzero rotation; a card invariant becomes a bound on occupancy under the entry rules. State what the result enables and the condition that changes that use.

When the consequence is insufficient, make the next contribution specific. “Determine whether these two wheels slip differently under this load” can direct physical work. “Find a representation that retains accumulated turns” can direct mathematical formulation. “Establish whether this interface interprets the number as an increment or an absolute target” can direct realization work. The uncertainty itself can be the result if locating it prevents further work on the wrong question.

Distinguish the consequence of an obstruction. A mathematical contradiction blocks a construction under its stated premises. A physical restriction blocks an intervention under the applicable laws. An expensive computation can remain mathematically possible while unavailable within the resources of this use. Their repairs can require different questions, arrangements or Methods.

Stop when the supported result answers the intended use. When development is the purpose, work one consequential variation far enough to reveal a new construction, obstruction or missing operation. Explain which additional action or longer inquiry it could enable. B.5:4.4, C.39 and C.40 supply the corresponding question and repertoire development; continued work is justified by that use.

### B.5.MPC:4.8 - Divide human and AI contributions by the result they must supply {#divide-human-and-ai-contributions-by-the-result-they-must-supply}

Allocate work around the dependencies above. A contributor can supply a physical account, a mathematical construction, a proof, a computation, a proposed realization or an explanation of the connection. State the working question, available inputs, missing result and intended use when obtaining help through A.15.9. Ask for the formulation itself when the equation has not yet been constructed.

Retain enough understanding at each receiving point to use and question its input. The receiver of a motion count should be able to identify its unit, the rotation it counts, its sign and its dependence on the motion model. The receiver of a two-colouring result should be able to connect the returned labels or odd-cycle witness to the actual contact list. The receiver of an occupancy bound should be able to identify the material and procedural conditions that preserve the stock.

That understanding can be held by one person or distributed across people and AI with an effective way to obtain a missing explanation. Arrange a capable contribution for each consequential connection. A completed report alone does not establish that this capability is available when a premise changes.

Choose depth from the later work. Using a stable formula may require interpretation and checks at the connection. Changing the formula requires understanding its derivation. Designing a new algorithm or physical theory requires the additional specialist capability. When assessing a person's preparation, examine their contribution on representative work with the assistance that will actually be available. Include a change of the requested result or a relevant premise when later work requires that adaptation. Ask the practitioner to recover the retained relation, the new unknown and the dependent physical operation.

## B.5.MPC:7 - Conformance Checklist {#conformance-checklist}

Use these checks on the claimed joint result and its explanation. They establish conformance to this Method's stated use; physical validity and any stronger assurance claim require their applicable subject evidence.

| Check | Content to inspect |
| --- | --- |
| CC-MPC.1 — Receiving question | @fact:CC-MPC-1 The explanation identifies the physical difference to be resolved and what the supported answer enables. @status:spec/work |
| CC-MPC.2 — Physical premises | @fact:CC-MPC-2 Participants, interactions and operating conditions are sufficient to recover the mathematical question; consequential assumptions remain distinguishable from observations. @status:spec/work |
| CC-MPC.3 — Interpretable construction | @fact:CC-MPC-3 Important quantities, structures and operations have meanings that survive the construction, and a lost distinction either leaves the use intact or changes the returned result. @status:spec/work |
| CC-MPC.4 — Obtained consequence | @fact:CC-MPC-4 The proof, construction, bound or computation is actually supplied for the stated case, with the decisive argument and its conditions. A missing operation is named as missing. @status:spec/work |
| CC-MPC.5 — Executing arrangement | @fact:CC-MPC-5 Any realization claim connects preparation, system operations and result reading. Range, units, initial state and ordering are recovered wherever they change the inference. @status:spec/work |
| CC-MPC.6 — Joint and alternative dependencies | @fact:CC-MPC-6 Jointly needed contributions remain together; alternative routes each satisfy the receiving need under their own conditions. A shared premise remains shared across alternatives. @status:spec/work |
| CC-MPC.7 — Notation in use | @fact:CC-MPC-7 The expression supports the needed operation under explained or familiar rules; new subject conclusions are justified by that operation rather than presented as mere re-expression of givens. @status:spec/work |
| CC-MPC.8 — Supported return | @fact:CC-MPC-8 The consequence is interpreted in the physical question with the bounds and uncertainties its use consumes. Conditional design and observed performance remain distinguishable. @status:spec/work |
| CC-MPC.9 — Useful continuation | @fact:CC-MPC-9 The explanation ends with an adequate use, a specific missing contribution or a justified next question. A change returns to its affected contribution and dependents. @status:spec/work |

A short sufficient calculation can satisfy these questions without separate records for each row. A shared or consequential result retains enough of the derivation, interpretation and evidence for its receiver to inspect the connections.

## B.5.MPC:9 - Consequences {#consequences}

The practitioner can assemble a useful answer from contributions obtained at different times and from different people, AI systems or established sources. The resulting explanation identifies how the answer concerns the physical situation and which premise or operation would change it. That makes a partial result useful: a bound can settle a decision, an odd cycle can locate a design obstruction, and an unresolved command meaning can direct one precise request.

The method also changes what work is commissioned. Instead of asking for another undifferentiated simulation or report, a team can ask for the missing physical relation, retained state, constructive algorithm, measurement or realization. An already adequate contribution remains available when an unrelated part changes.

This connection work has a cost. Recovering an unfamiliar source, learning notation or obtaining a physical premise can take more effort than calculating the displayed answer. Spend that effort where it changes the receiving use. The method provides no automatic completeness claim for physics, mathematics or computing; it makes the needed subject contribution and its remaining boundary visible.

## B.5.MPC:12 - Relations {#relations}

| Relation | Concrete contribution |
| --- | --- |
| **Specializes B.5 — Canonical Reasoning Cycle** | Retains question formation, selection of a missing contribution, result understanding and sufficient-result closure; adds the joint physical, mathematical and computational connections and their dependencies. |
| **Uses B.5.4 — Recognize a Reusable Concept in a Concrete Situation** | Supplies recognition of an explained concept's participants and relations when the physical situation has not yet been interpreted through it. |
| **Uses C.29 — Mathematical Lens Use** | Constructs the mathematical account and returns its consequence to the working question. |
| **Uses C.29.1 — Mathematical Result Transfer** | Constructs the correspondence and tests the operations and distinctions needed to carry a result between mathematical accounts. |
| **Uses C.29.2 — Computational Formulation** | Constructs the computational state, operations and obtaining procedure, with the result argument and resource account that its use needs. |
| **Uses C.29.3 — Computational Realization** | Compares input preparation, system operation and readout with the required result, and returns a failed connection to its repair. |
| **Uses A.3.3 — U.Dynamics** | Supports the construction of configurations, retained state and allowed continuations when the receiving prediction or operation requires them. It uses the supplied subject laws and interaction rules. |
| **Uses C.16 — Measurement and Metrics Characterization** | Constructs and interprets the measurement relation connecting the sought quantity, apparatus influences and indication. This contribution is needed when the joint consequence consumes an observation. |
| **Uses A.6.3.RT — Representation-Scheme Transition** | Constructs an operative expression under an available scheme and compares its content and use with the source. The applicable subject Method supplies any new conclusion obtained with that expression. |
| **Uses A.6.1 for realization semantics** | Keeps a declared operation, its realization relation and the performance of a Method distinguishable when those claims matter to the executing arrangement. |
| **Uses A.15.9 for a needed contribution from another practice** | Helps obtain the specific result, explanation or formulation that the next operation needs, with its receiving use made explicit. |
| **Coordinates with C.39 and C.40** | Searches for a missing way and develops the problem or Method repertoire when the existing connections expose a worthwhile construction question. |
| **Uses C.11.DUA for a decision about further effort** | Compares whether additional calculation, observation, explanation or checking can change the receiving action enough to justify its cost. |
| **Uses B.3 and B.3.3 for stronger assurance questions** | Qualifies evidence and assurance for the particular claim and use when a conditional consequence or ordinary construction no longer suffices. |


## Dependencies {#dependencies}

- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/B-5#root, spec://ai.lev/fpf-spec/contract/A-3-3#root, spec://ai.lev/fpf-spec/contract/C-16#root, spec://ai.lev/fpf-spec/contract/A-6-3-RT#root, spec://ai.lev/fpf-spec/contract/C-29#root, spec://ai.lev/fpf-spec/contract/C-29-1#root, spec://ai.lev/fpf-spec/contract/C-29-2#root, spec://ai.lev/fpf-spec/contract/C-29-3#root, spec://ai.lev/fpf-spec/contract/C-39#root and spec://ai.lev/fpf-spec/contract/C-40#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/A-3-3-CC#root, spec://ai.lev/fpf-spec/contract/A-3-3-TR#root, spec://ai.lev/fpf-spec/contract/B-5-MPC-R#root, spec://ai.lev/fpf-spec/contract/B-5-QD#root, spec://ai.lev/fpf-spec/contract/B-5-RA#root, spec://ai.lev/fpf-spec/contract/C-28-MR#root, spec://ai.lev/fpf-spec/contract/C-29#root, spec://ai.lev/fpf-spec/contract/C-29-3#root, spec://ai.lev/fpf-spec/contract/C-36-RP#root, spec://ai.lev/fpf-spec/contract/C-40-CD#root, spec://ai.lev/fpf-think-not/contract/NOT-8#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/B-5-MPC
