# B.5.TC - Compare Theoretical Accounts for a Working Question: depth {#depth}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## B.5.TC:5 - Archetypal Grounding {#archetypal-grounding}

### B.5.TC:5.1 - Routes, reachability and minimum cost {#routes-reachability-and-minimum-cost}

A mathematical account keeps routes as distinct objects. Routes p and q go from X to Y and cost 1 and 4. A route r goes from Y to Z and costs 2. Routes with matching endpoints can be concatenated; the cost of a concatenation is the sum of its costs. The two routes from X through Y to Z therefore cost 3 and 6.

A second account keeps only whether travel between endpoints is possible. Both X-to-Y routes become the answer “yes”. Joining that answer to Y-to-Z reachability gives “yes” for X-to-Z. This account answers whether travel is possible. It cannot give the cost of the route actually taken: p followed by r and q followed by r have the same reachability summary and different costs.

A third account keeps minimum costs. For finite nonempty sets of allowed first and second segments, assume every first segment can be followed by every second segment and costs add. Then the least combined cost is the sum of the two least costs. Every combined cost is at least that sum, and combining the two minimizing segments attains it. Here the answer is 1 + 2 = 3. The calculation can therefore answer the minimum-cost question without retaining every route. Choosing an actual route also requires the minimizing segments to be recoverable.

Now change the allowed combinations. Let the second segments be r with cost 2 and s with cost 10. Only p followed by s, and q followed by r, are allowed. The true minimum is min(1 + 10, 4 + 2) = 6. Independently minimizing the two stages gives 3, which no allowed route attains. The failure is the omitted compatibility relation. Retain the incoming-route distinction or calculate over the allowed pairs.

The comparison yields three useful accounts with different retained information. Its changed case also identifies a condition for the minimum-cost composition rule. No physical interpretation is needed for this mathematical result. Using cost as travel time or expenditure adds the corresponding interpretation and additivity conditions.

### B.5.TC:5.2 - The same oscillator, different formulation and computation {#the-same-oscillator-different-formulation-and-computation}

Consider an ideal one-dimensional mass on a linear spring, with mass m > 0, spring constant k > 0, displacement q and velocity v. Friction and external forcing are absent. The question is its motion from q(0) = a and v(0) = 0.

The force account gives m q'' = -k q. The variational account uses L(q,v) = m v²/2 - k q²/2. Its Euler-Lagrange equation is d/dt(∂L/∂v) - ∂L/∂q = 0; substitution gives m q'' + k q = 0. Both therefore give q(t) = a cos(√(k/m) t) under these premises. For this motion question, the two constructions agree. The variational formulation can become preferable when another coordinate choice simplifies constraints; the force formulation may be the quicker account for this simple case.

Suppose a computation appears to disagree. Take m = k = a = 1 and use the forward Euler updates q_next = q + h v and v_next = v - h q. From q = 1, v = 0 and h = 0.1, it returns q_next = 1, v_next = -0.1. The energy (q² + v²)/2 rises from 0.5 to 0.505. In fact these updates multiply energy by 1 + h² at each step, whereas the differential equation conserves it.

The discrepancy is produced by the approximation used in the computation. Compare an adequate step size or another numerical method under C.29.2 for the requested horizon and error. If the real oscillator loses energy, examine friction and other physical interactions; that changes the model question. The equality of the two ideal derivations remains available within its premises.

### B.5.TC:5.3 - Agreement in observation, disagreement under intervention {#agreement-in-observation-disagreement-under-intervention}

An indicator X and an output Y always follow a binary controller command U. Two causal hypotheses explain the observed pairs: A uses X := U and Y := X; B uses X := U and Y := U. In A, the indicator drives the output. In B, the controller drives both directly. Both yield X = Y = U in ordinary operation.

The question is now what happens when X is forced to 1 while U remains 0. Represent this intervention by replacing the assignment to X. A gives Y = 1; B gives Y = 0. The same observed pairs leave that difference unresolved.

The next contribution could be the circuit description, an already available intervention result or a worthwhile discriminating test. If the work only predicts the observed indicator from U in unchanged operation, this causal difference need not be settled for that use. If it proposes controlling Y through X, retain the unresolved consequence until the needed causal premise is supplied. C.28 governs that intervention claim.

## B.5.TC:6 - Bias-Annotation {#bias-annotation}

A shared question can favor the account that originally framed it. Retain a rival's newly expressible question when it opens useful inquiry; compare that contribution on its own terms. Conversely, unfamiliar notation can make an ordinary operation appear novel. Recover the operation before crediting or rejecting the account.

The cases use small formal constructions so their decisive steps can be inspected. They demonstrate the comparison method, with domain premises stated in each case. A difficult real application can need specialist knowledge, uncertain premises and more than one iteration. Human, AI and collective contributions can participate in the comparison; claims about their learning or reliability require their own basis.

## B.5.TC:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Failure | Repair |
|---|---|
| Comparing unlike outputs as rivals: reachability and minimum cost are both called a route answer. | State the question each answers, then construct the common question or their complementary use. |
| Identifying theoretical accounts because a fitted case gives the same number. | Compare the meanings and decisive operations; derive the range of agreement when a broader claim is needed. |
| Treating a numerical discrepancy as a physical-theory disagreement. | Recover the formulation and approximation, as in the oscillator case, before changing the physical account. |
| Selecting a more elaborate account for capabilities the present question does not use. | Compare the adequate answers and their burdens; retain the further capability for the question that needs it. |
| Seeking more observations to resolve a difference that ordinary observations cannot distinguish. | Derive the discriminating consequence and use the relevant causal or other domain method; retain an unresolved difference when further inquiry is unavailable or unwarranted. |

## B.5.TC:10 - Architectural Rationale {#architectural-rationale}

The unit of comparison is an application because a theory's objects alone leave its useful inference undetermined. Reconstructing that inference makes differences in representation, premises and operations comparable without first imposing a common ontology on every source concept.

Working a shared case provides a place to connect the accounts. Following the dependency that causes a difference then supports a broader argument or a discriminating example. These operations complement one another: a derivation establishes scope, while an example can reveal that the chosen scope misses the work's question.

Separating agreement, complementary use and unresolved difference keeps the result productive. An account may remain preferable for a cheap prediction and insufficient for an intervention. Another may be harder to use now yet expose a construction worth developing. This preserves the connection between obtaining knowledge, applying it and improving the available ways of inquiry.

## B.5.TC:11 - SoTA-Echoing {#sota-echoing}

For comparing what different mathematical accounts let a practitioner compute, **adopt** the operation-based comparison illustrated by Fong and Spivak's *Seven Sketches in Compositionality* (2019), §2.5.2–§2.5.3. Reachability and cost use different operations for combining steps and choosing among alternatives. Against comparison by shared route terminology, this makes the lost answer and composition condition visible in :4.3 and :5.1. The finite compatibility example is a construction here. Reopen its application when the quantity or allowed composition changes. [Author manuscript](https://arxiv.org/pdf/1803.05316).

For physical formulations that may agree, **adopt** the constructive comparison in Sussman and Wisdom's *Structure and Interpretation of Classical Mechanics*, second edition (2015), §1.6: derive the equations under the stated force and potential assumptions. This answers more than a numerical fit and often costs less than a new simulation. Against selecting a formulation solely by familiarity, preserve the advantage of coordinates adapted to constraints. Sections :4.3–:4.4 and :5.2 separate that choice from numerical approximation. Reopen when interactions, constraints or the requested result change. [Publisher's text](https://mitp-content-server.mit.edu/books/content/sectbyfn/books_pres_0/9579/sicm_edition_2.zip/chapter001.html).

For comparing causal uses, **adopt** intervention construction from Pearl's *Causal inference in statistics: An overview* (2009), §3.2.1, and **adapt** it here to expose the particular consequence on which two accounts disagree. Agreement in the observed distribution, a serious comparator for prediction, can leave that intervention consequence undecided. This changes :4.4 and :5.3. C.28 supplies the broader causal method. Reopen when the causal premises or intended intervention change. [Author's paper](https://ftp.cs.ucla.edu/pub/stat_ser/r350.pdf).

For prediction, a serious alternative to choosing a single account is combining predictive distributions. Yao, Vehtari, Simpson and Gelman's stacking method (2018) chooses weights through predictive performance when the candidate set need not contain the data-generating model. **Adapt** that question-relative choice into :4.5's permission to retain combinations. **Reject** using such predictive weights as a verdict about causal mechanism or mathematical equivalence; those are different comparison questions. The statistical method remains with its domain, including its scoring and validation conditions. Reopen when prediction under another distribution or a different use is required. [Authors' paper](https://sites.stat.columbia.edu/gelman/research/published/stacking.pdf).

This pattern combines these constructive contributions into a common comparison method. Its first result is the comparison obtained under the stated conditions.


## B.5.TC:End {#end}
