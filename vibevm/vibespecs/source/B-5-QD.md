# B.5.QD - Develop a New Question from a Result or Construction: depth {#depth}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## B.5.QD:5 - Archetypal Grounding {#archetypal-grounding}

### B.5.QD:5.1 - From a false graph claim to a construction or obstruction {#from-a-false-graph-claim-to-a-construction-or-obstruction}

An engineer represents pairwise incompatibilities by a finite simple undirected graph. The proposed claim is that connectedness suffices to divide the vertices into two groups so every edge crosses between groups.

A triangle refutes the claim. Assign A to the first group and its neighbour B to the second. The third vertex C is adjacent to both, so neither group is available. The failure concerns the universal claim, not the ability to divide any graph: a four-vertex cycle A-B-C-D-A admits groups {A,C} and {B,D}.

Follow the failed operation. Along a path, successive vertices can alternate between the two groups. Returning around an odd cycle forces its final edge to join vertices assigned to the same group. That identifies an obstruction worth seeking.

The next question is: **For a given finite simple undirected graph, can we construct the division or return an odd cycle that explains why it is impossible?** The answer form now serves both allocation and diagnosis.

B.5:5.1 supplies the broader construction. Traverse each component by breadth-first search and assign groups by even or odd depth. If every edge joins opposite parities, the assignment works. An edge joining equal parities combines with the two parent paths up to their last shared vertex to give a simple odd cycle. The construction therefore answers the new question for the stated graph class.

The earlier connectedness requirement can be dropped: work through each component, including isolated vertices. For a real allocation, establish that the graph represents the relevant pairwise incompatibilities. Three-way constraints would change that application question.

### B.5.QD:5.2 - From a position to a sufficient state or useful bound {#from-a-position-to-a-sufficient-state-or-useful-bound}

A model describes a point moving along one line in an inertial frame. During the next two seconds there is no net force; use the classical relation q(t) = q(0) + v(0)t. The supplied position is q(0) = 0. Someone asks where the point will be two seconds later.

Construct two cases allowed by this description. With v(0) = +1 metre per second, q(2) = +2 metres. With v(0) = -1 metre per second, q(2) = -2 metres. Position alone leaves the requested answer undetermined.

One next question is **what information completes the state for this prediction?** Under this model, initial velocity together with position suffices. Obtaining velocity could use an already available displacement over a known interval of constant velocity. A.3.3 and C.16 develop state and measurement when those contributions are needed.

Another question is cheaper if the current decision only asks whether the point stays within three metres of its starting position for the next two seconds. Suppose the available information bounds the initial velocity between -1 and +1 metre per second. Then the displacement magnitude is at most (1 metre per second)t throughout that interval, so the point stays within two metres. The bound answers the decision without acquiring a more specific velocity.

The two questions support different uses. If an actuator must meet the point at a specified position, the bound can be insufficient and the state question becomes useful. If the net force becomes nonzero during the interval, revise the model and its prediction. The construction of the question has located the relevant missing contribution in each case.

### B.5.QD:5.3 - A successful cumulative computation opens an interval question {#a-successful-cumulative-computation-opens-an-interval-question}

A program can construct cumulative totals for an integer array a. It starts with S[0] = 0 and sets S[i+1] = S[i] + a[i]. For a = [2,-1,3,4], the result is S = [0,2,1,4,8].

The original task needed the total 8. Recovering the operation reveals that each S[i] already gives the sum before position i. This opens the question: **Can we answer many interval-sum queries from the same cumulative totals?**

Specify an interval by indices l and r, with 0 ≤ l ≤ r ≤ n; it includes l and ends just before r. Splitting the first r elements at l gives S[r] = S[l] + sum(a[l],...,a[r-1]). Hence the interval sum is S[r] - S[l]. For the last two elements, l = 2 and r = 4, so the answer is 8 - 1 = 7. For l = r the answer is 0.

This is a general derivation under integer arithmetic with enough capacity to avoid overflow. Each query uses two stored totals and one subtraction after the array has been prepared. Whether preparation is worthwhile depends on how many queries and changes the application requires.

If a[i] changes by d, every S[j] with j > i changes by d. Frequent changes therefore open a further question: which data organization supports the required mixture of updates and interval queries? That question can be developed when the workload makes it relevant. The successful cumulative operation already answers the unchanged-array question.

## B.5.QD:6 - Bias-Annotation {#bias-annotation}

The original formulation can anchor subsequent questions. Recovering its failed condition or unused operation helps reveal alternatives, but the new question should still explain what it contributes. A more familiar or easier formulation can silently abandon the unresolved use.

Mathematical search often favors statements that can be proved. Question development also benefits from locating a false conjecture, an underdetermined description or a construction that cannot meet its conditions. Their usefulness comes from the inquiry they enable.


## B.5.QD:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Failure | Repair |
|---|---|
| Appending exceptions until a refuted claim survives, while losing the original use. | Follow the counterexample's failed relation; formulate the condition or obstruction that helps answer the working question. |
| Treating a failed lemma as a refutation of the main conjecture. | Recover which argument used the lemma and what remains undecided; investigate an alternative step where useful. |
| Generating many syntactic variants and counting them as progress. | Work a variation that changes an available construction, an answer or a useful distinction. |
| Asking for a unique prediction from information shared by physically different continuations. | Exhibit the differing cases; obtain sufficient state information or return a useful bound. |
| Discarding a successful operation after it gives the requested number. | Recover its relation to inputs and outputs when another use could benefit, as with cumulative totals. |
| Making proof of eventual usefulness a prerequisite for exploration. | Identify the nearer inquiry or construction the question can enable and compare that contribution with its present cost. |

## B.5.QD:10 - Architectural Rationale {#architectural-rationale}

A new question needs an operation of construction. The instruction to find an interesting question becomes usable when it points to a dependency that failed or an operation that became available. This also connects developing a theory with applying it: an application can expose a new question, and a theoretical construction can create an application that could not previously be attempted.

The answer form matters because it determines what work counts as progress. A witness of impossibility can be as useful as a successful construction for deciding an allocation. A bound can answer an operational question while a unique prediction remains unavailable. These alternatives are obtained by examining the earlier result and its use.

The small case and the broader question develop together. Working the case tests whether the question identifies a real difference; stating the broader question prevents the case from becoming the only thing learned. Retaining unaffected results makes this development cumulative.

Practical interest includes opening future inquiry. The method asks for the next intelligible contribution while leaving later uses open.

## B.5.QD:11 - SoTA-Echoing {#sota-echoing}

For developing a question after a failed proof or conjecture, **adapt** Lakatos's proof-analysis method in *Proofs and Refutations (I)* (1963), §3 and the beginning of §4. Distinguishing a counterexample to a lemma from one to the main conjecture preserves recoverable reasoning; asking for the missing construction improves on protecting the claim by convenient restrictions alone. Sections :4.1–:4.3 and :5.1 use that contribution. The historical dialogue supplies a method of criticism and question change; the resulting mathematical claims still need their own arguments. Reopen the choice when a different failure prevents recovery of the consequential dependency. [Original article](https://pi.math.cornell.edu/~mann/classes/chicago/Lakatos.pdf).

For obtaining questions from either an unfinished proof or available constructions, **adapt** the distinction between goal-directed lemma discovery and bottom-up theory exploration in Zhang and Tan's *Automated Conjecturing and Theorem Finding: A Survey* (2026), §§3 and 5. The two approaches support different entries in :4.2. The surveyed filters for false, redundant or uninteresting conjectures help theorem search; using those filters as a general question filter would discard a useful counterexample. Section :4.3 instead evaluates the question's contribution separately from a proposed answer's truth. Syntactic complexity and proof-related scores remain local heuristics. Reopen when a stronger generation method offers more useful questions at comparable effort for the receiving practice. [Survey](https://jcst.ict.ac.cn/cn/article/pdf/preview/10.1007/s11390-026-6040-0.pdf).

For finding further uses of a successful operation, **adopt** Blelloch's constructive treatment of all-prefix-sums in *Prefix Sums and Their Applications* (1993), §1.1. It exposes an operation and its application conditions, improving on retaining only a program's final answer. Section :5.3 uses cumulative addition to develop an interval question; its range-sum derivation is worked here. Prefix operations over other associative operators can serve other questions, but subtraction requires the additional algebraic structure used in this example. The source's parallel implementations are separate Methods. Reopen when the operations, numeric semantics or workload change. [Author's chapter](https://www.cs.cmu.edu/afs/cs/academic/class/15750-s11/www/handouts/PrefixSumBlelloch.pdf).

For questions beyond a fixed objective, **adapt** Wang et al.'s *Enhanced POET* (2020), §§2–3, through C.40's coupled development of problems and ways. Relative difficulty and transfer can make a question worth retaining even when it is poorly served by the present best method. Against requiring an already known route to a final objective, :4.5 keeps a useful nearer contribution and examines its cost. The reported computational environments demonstrate that search approach under their conditions; they do not establish a universal measure of interest or development. E.10.INT supplies the broader distinction. Reopen when retained questions cease to enable useful transfer or the contributors' capabilities change. [Paper](https://proceedings.mlr.press/v119/wang20l/wang20l.pdf).


## B.5.QD:End {#end}
