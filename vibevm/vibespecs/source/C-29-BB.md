# C.29.BB - Construct a Balance across a Boundary: depth {#depth}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## C.29.BB:5 - Archetypal Grounding {#archetypal-grounding}

### C.29.BB:5.1 - A transfer line changes which balance answers the tank question {#a-transfer-line-changes-which-balance-answers-the-tank-question}

Use a constant-density liquid, measured by volume in litres. At the start, tank A holds 30 L and tank B holds 10 L. Over the chosen interval, an external supply adds 12 L to A, and an external outlet removes 7 L from B.

First suppose the line transfers 15 L from A to B with no change in its liquid content. Then

    A: 30 + 12 - 15 = 27 L
    B: 10 + 15 - 7 = 18 L
    A+B: 40 + 12 - 7 = 45 L.

The internal 15 L cancels. The larger balance gives the combined amount without needing that internal transfer, while the separate balances give each tank's amount.

Now change the condition: the line begins empty, receives 15 L from A, delivers 13 L to B, and retains 2 L. The results become

    A: 27 L
    B: 10 + 13 - 7 = 16 L
    line: 0 + 15 - 13 = 2 L.

The two tanks contain 43 L. Their boundary excludes the line, so 15 L leaves that boundary and 13 L re-enters. The combined tank change is 12 - 7 - 15 + 13 = 3 L. Including the line gives 45 L and recovers the five-litre increase from the external exchanges alone.

If the line's increase is known only to lie between 0 and 2 L, the final tank total lies between 43 and 45 L. This bound settles a request for at least 42 L in the tanks. A request for at least 44 L needs a tighter bound or the line's actual content. No additional observation is required for the first request.

### C.29.BB:5.2 - Moving and reworking a job preserve one count but change its distribution {#moving-and-reworking-a-job-preserve-one-count-but-change-its}

Count accepted jobs that have not yet been completed. Each job occupies one of two stages, including any processing position in that stage. Initially A contains 6 jobs and B contains 4.

During an interval, 12 new jobs arrive at A, 9 move from A to B, and 7 are completed at B. With no other arrivals, completions or membership changes,

    A at end = 6 + 12 - 9 = 9
    B at end = 4 + 9 - 7 = 6
    unfinished total at end = 10 + 12 - 7 = 15.

A limit of 12 unfinished jobs is therefore exceeded at the endpoint. Determining whether the limit was exceeded earlier requires the event history or a bound on its prefixes.

If 2 of B's remaining jobs return to A for rework before the endpoint, the stage totals become 11 and 4; the unfinished total remains 15. The extra work is consequential, but moving the same jobs changes their distribution rather than their count.

If the question instead counts separately created work orders, specify that new population and its creation rule. A parent job and two newly opened orders cannot be mixed into the earlier job count without changing its meaning. The next operations-management question may need workload or completion-time modeling in addition to this balance.

### C.29.BB:5.3 - One shared transfer preserves the computational total {#one-shared-transfer-preserves-the-computational-total}

Two computational cells store amounts 10 and 20. One step adds 5 from outside to cell A, removes 2 from cell B, and transfers 3 from A to B. Using one transfer amount gives

    A' = 10 + 5 - 3 = 12
    B' = 20 + 3 - 2 = 21
    A' + B' = 33 = 30 + 5 - 2.

Suppose A subtracts 3 but B adds 2.9. The resulting total is 32.9; the inconsistent interface updates lose 0.1 in that step. Repairing the shared amount restores the aggregate balance. Whether the transfer approximates the intended transport well remains a separate question.

Now let both sides use 2.9. The result is A'=12.1, B'=20.9 and total 33. The aggregate balance holds, but the supplied transfer of 3 requires the local values 12 and 21. Agreement between the two interface amounts preserves the total; their accuracy must still be established for the requested local result.

If the cells store average densities, first multiply by their volumes to obtain the amounts. Summing unequal-volume cells' densities would test another quantity.

## C.29.BB:6 - Bias-Annotation {#bias-annotation}

The storage examples make additivity easy to see. Apply it elsewhere only with a corresponding quantity definition. For a count of file copies inside the chosen boundary, making one additional copy adds one through internal production.

The job example is a pathwise counting account. It introduces no arrival distribution, steady-state condition or claim that all jobs require equal effort. Those assumptions become relevant only for further questions that use them.

## C.29.BB:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Failure | Repair |
| --- | --- |
| **The connector disappears.** The tanks are combined while the line's changing content is omitted. | Include the line or retain its two crossings and storage difference. |
| **Similar numbers are added.** Temperatures or overlapping job populations are summed as a stored amount. | Construct an additive quantity or retain the local values required by the question. |
| **A discrepancy is named a leak.** Incompatible endpoints or transfer observations are never examined. | Compare the accounts and choose a discriminating check when its result matters. |
| **Local updates disagree.** The two sides of a computational interface use different transferred amounts. | Share the amount or provide a compatible conversion, then derive the aggregate update again. |

## C.29.BB:10 - Architectural Rationale {#architectural-rationale}

The independent difficulty is constructing what is added and what cancels. Once compatible local equations are supplied, summing them is elementary; selecting parts, quantities and shared exchanges is the substantive work that makes the sum useful.

A.3.3.TR constructs state-change rules and already demonstrates cancellation of internal forces. This pattern develops the choice and revision of a balance boundary across different quantities and descriptions. C.29.1 handles result transfer between mathematical accounts; the present construction explains why one particular aggregation preserves a total and what must be restored for a smaller-boundary question.

The finite-interval relation is the first construction because it works for discrete events as well as physical storage. Differential and field forms require the subject's regularity and transport assumptions. This separation keeps an elementary count accessible while leaving richer physical and numerical constructions available.

## C.29.BB:11 - SoTA-Echoing {#sota-echoing}

[OpenStax, University Physics Volume 1, §14.5](https://openstax.org/books/university-physics-volume-1/pages/14-5-fluid-dynamics) derives fluid continuity from mass flow and uses constant density to pass to volume flow. Adopt the need for a physical quantity basis; adapt the simple equal-flow case by retaining changing storage in the selected region.

[Sonin, On Choosing and Using Control Volumes (2001), Methods 1–6](https://ocw.mit.edu/courses/2-25-advanced-fluid-mechanics-fall-2013/1657c64b3737c8d35e5905ea21702c6b_MIT2_25F13_On_Choo_and_Usi.pdf) compares fixed and moving boundaries for the same piston-driven flow. The constructions obtain the same exit speed while changing accumulation and crossing terms; a boundary through the piston makes one formulation require a density-discontinuity treatment. Use this established control-volume Method when its continuum quantities and mathematical preparation fit the question. The finite construction in :4 also serves event counts and partitioned computational updates.

[Ketcheson, LeVeque and del Razo, Riemann Problems and Jupyter Solutions, “Finite volume methods”](https://www.clawpack.org/riemann_book/html/Approximate_solvers.html#Finite-volume-methods) obtains aggregate conservation by weighting cell averages and canceling neighboring fluxes. Adopt compatible interface transfer in a numerical update. The book's approximate-solver construction supplies additional transport and approximation methods beyond this balance test.

For the changed tank question, compare two adequate accounts with the same supplied interval amounts and elementary arithmetic. Direct accounting at the tank boundary uses the line's 15 L departure and 13 L arrival to obtain 43 L. Accounting over tanks plus line gives 45 L; recovering the tank amount then needs the line's final 2 L store. Choose the account whose needed quantities are available. Applying only the outside exchange to A+B gives the wrong 45 L answer because it omits the line's increase. If an applicable balance already answers the question, another account adds no benefit.

The boundary-revision procedure and the tank and job continuations are a conceptual synthesis of additive accounting, physical storage and computational conservation. Detailed continuum transport, chemical reaction accounting and stochastic queue models need their own subject Methods.

Reconsider the quantity, boundary or balance form when membership changes, needed storage information is unavailable, boundary motion changes the crossing law, or a cheaper adequate construction becomes available.


## C.29.BB:End {#end}
