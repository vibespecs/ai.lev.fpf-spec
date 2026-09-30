# C.29.BB - Construct a Balance across a Boundary {#root}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method
> **Status:** Draft
> **Normativity:** Normative

## C.29.BB:1 - Problem frame {#problem-frame}

Use this pattern when a total changes and you need to construct the relation between that change, transfers across a chosen boundary, and creation or removal within it. The difficulty may be choosing what belongs inside, combining accounts for parts, or understanding why a balance changes after the boundary is redrawn.

Two tanks can gain less liquid than their external inflow minus outflow suggests because some liquid remains in their connecting line. A job moving between two stages changes their separate counts while leaving the total unfinished count unchanged. A computation can introduce a discrepancy if two cells use different amounts for their shared transfer.

The Method constructs a balance for a chosen additive quantity over a specified interval and collection of parts. Its first result can be a predicted total, a bound, a missing-transfer question, or a computational update that preserves the supplied balance. The construction may describe a physical region, a defined population or a mathematical partition; identify which one answers the working question.

The reader needs the quantity's meaning and enough arithmetic to combine amounts with signs. A physical application also needs the relevant storage and transfer laws. A rate or field calculation needs the calculus used by that model.

If a complete, applicable balance already answers the question, use it. This pattern is useful when the balance itself must be built or revised. Detailed transport laws, reaction models and numerical solvers remain contributions of their respective subject Methods.

## C.29.BB:2 - Problem {#problem}

A plausible equation such as “change equals input minus output” can leave its subject undecided. The chosen parts may overlap, an intermediate store may be omitted, or two records may count the same transfer at different times. A selected quantity may also be created or removed within the boundary: the number of unfinished jobs changes when a job is completed, while the amount of a conserved material follows a different law.

Adding local equations works only after their quantities, intervals and shared transfers have been made compatible. Otherwise cancellation can hide a missing store or combine values that cannot be added.

## C.29.BB:3 - Forces {#forces}

| Force | Tension |
| --- | --- |
| Useful total | A coarse amount can answer a capacity question while hiding the local peak needed by another decision. |
| Boundary choice | A smaller region is easier to observe; a larger one can turn uncertain exchanges into internal transfers. |
| Additivity | Summing parts is simple when the quantity has an additive meaning; overlapping populations or intensive variables require another construction. |
| Incomplete information | A bound may settle the decision even when individual transfers remain unknown. |
| Computational preservation | A model can obey a balance while its implementation uses incompatible transfer amounts. |

## C.29.BB:4 - Solution {#solution}

Choose the quantity and boundary, account for changes in each included part, and combine only matching transfers. Use the resulting balance to answer the question at the needed resolution.

### C.29.BB:4.1 - Choose an additive quantity and a common interval {#choose-an-additive-quantity-and-a-common-interval}

Name the quantity Q, its unit or counting rule, the included parts S, and the start and end conditions. Define who or what belongs to each part. Use disjoint parts, or otherwise account for their overlap before summing.

For disjoint parts with amounts q_i, additivity means that Q(S) = sum q_i. The rule needs a basis in the selected model or counting definition. For a population, assigning each included job to one stage can provide it. For physical storage, use the appropriate physical quantity and law.

An average temperature is not an additive heat store. If the question concerns stored thermal energy, construct that quantity from the material and state relations; if it concerns the maximum temperature, preserve the local temperatures needed to obtain the maximum. Choosing a convenient sum changes the question unless the required result can be recovered from it.

Keep all amounts on the same interval. A transfer that leaves one store before the endpoint but reaches another afterward requires an in-transit store or separate boundary crossings. For snapshots at different times, first recover their relation to the requested interval.

### C.29.BB:4.2 - Identify transfers and internal production or removal {#identify-transfers-and-internal-production-or-removal}

For each included part, distinguish the amount crossing into it, the amount crossing out, and the change created or removed within it under the chosen quantity definition.

Orient each transfer once. When a transfer from part i to part j removes amount f from i and adds the same amount to j over the common interval, use -f and +f in their accounts. If a connector stores some of the quantity, its incoming and outgoing amounts can differ; represent that store or retain both crossings.

Production and removal depend on the quantity. A reaction can change the amount of one chemical species within a vessel. Completing a job removes it from the population of unfinished jobs. Determine those terms from the relevant physical or counting rule. Assign each contribution once: classify completion as a crossing out of the population or as removal under its counting rule, and use that convention throughout.

Do not set an unobserved term to zero merely because the first diagram omitted it. Use a supplied law, a justified approximation, a bound, or an unresolved term according to what the answer needs.

### C.29.BB:4.3 - Combine the local balances {#combine-the-local-balances}

Write each included part's change using the selected terms. Sum those equations. Matching internal transfers cancel, leaving

    Q(S, t1) - Q(S, t0)
        = total inward transfer - total outward transfer
          + internal production - internal removal.

The transfer terms are amounts over the interval. A rate must be integrated over that interval, or multiplied by its duration when the rate is constant. The signs follow the chosen boundary.

For a differentiable rate model, the corresponding instantaneous relation is

    dQ(S,t)/dt = inward rate - outward rate + production rate - removal rate.

Use the finite-interval form for discrete events or when a rate description adds no help. If the selected boundary moves, count crossings relative to that moving boundary using the appropriate transport relation.

A closed boundary eliminates crossing terms only when the model excludes those exchanges. Constancy of Q additionally requires net internal production and removal to cancel. Preserve that premise in any conservation conclusion.

### C.29.BB:4.4 - Redraw the boundary by reclassifying the same exchanges {#redraw-the-boundary-by-reclassifying-the-same-exchanges}

When enlarging S, include the added stores and their changes. Transfers between the old and added parts become internal only if both sides now refer to the same amount over the interval. The new exterior crossings remain.

When shrinking S, formerly internal transfers can become inputs or outputs. Recompute the requested total from the retained stores. A balance for a larger region supplies its total; obtaining a smaller region's value still needs the removed region's amount or a sufficient bound.

Check the two descriptions against each other: the larger total equals the sum of its disjoint parts, and their changes agree after shared transfers cancel. This comparison can expose an omitted connecting store without resolving every internal rate.

Changing the parts over time can also change membership. Include that effect through boundary crossings or a suitable population rule; keep it visible when comparing successive totals.

### C.29.BB:4.5 - Use uncertainty or discrepancy to choose the next move {#use-uncertainty-or-discrepancy-to-choose-the-next-move}

Substitute the available amounts and compute the requested consequence. If some terms are bounded, propagate the bounds through the signed sum. Preserve dependencies when independently combining endpoints would admit impossible combinations.

For observed values, define the discrepancy as observed change minus the change predicted by the included terms. A nonzero discrepancy establishes disagreement between those accounts. Its cause can lie in an omitted store or transfer, incompatible timing or units, a faulty observation, or an inadequate law. Use the working situation to choose a discriminating next observation or model change.

Resolve a remaining term only when it can change the answer enough to justify the work. A supported bound that settles the current decision is already a usable result. An unresolved cause can remain open when the decision tolerates the resulting uncertainty.

### C.29.BB:4.6 - Preserve the balance in a computation and return its result {#preserve-the-balance-in-a-computation-and-return-its-result}

When implementing a partitioned calculation, represent a shared transfer consistently on both sides. Use the same orientation, interval and quantity conversion. Recover total amounts with the appropriate cell volumes or population weights before comparing them.

Derive the aggregate change from the proposed updates. If a numerical approximation changes the balance, determine whether the discrepancy fits the receiving use or repair the update. Balance preservation addresses one property of the computation; accuracy of the local solution requires its own approximation argument.

Return the total, bound or identified missing contribution with the quantity, boundary and assumptions needed to use it. A subsequent question about a local maximum, delay or possible action may require the retained component account. Keep that account available rather than treating the total as a substitute for every question.

## C.29.BB:7 - Conformance Checklist {#conformance-checklist}

- [ ] The quantity, units or counting rule, included parts and common interval are sufficient to identify the requested total.
- [ ] Additivity is justified for those parts, with overlap or in-transit storage accounted for where present.
- [ ] Each crossing and internal production or removal term has its meaning and sign; only matching internal transfers cancel.
- [ ] A changed boundary includes the added or removed stores and reclassifies the affected exchanges.
- [ ] The returned value or bound supports the stated question. Any unresolved discrepancy retains its uncertainty instead of being assigned an unsupported cause.
- [ ] When a computation is used, its aggregate update has been derived with the correct weights and shared transfers.

## C.29.BB:9 - Consequences {#consequences}

A well-constructed boundary can remove the need to know complicated internal exchanges. A second boundary can locate where missing storage or transfer information matters. The same construction supports physical balances, defined counts and numerical preservation tests.

The total compresses information. Local capacity, spatial extremes, causal response and completion time can remain unresolved even when the aggregate balance is sufficient for its own question. Retaining the component account makes those further inquiries possible.

## C.29.BB:12 - Relations {#relations}

- **C.29 - Mathematical Lens Use:** identifies the subject correspondence and the consequences that may be carried back from the mathematical balance.
- **A.3.3.TR - Construct a Rule for State Change:** supplies the broader construction of state evolution; this pattern develops an additive change account.
- **C.29.1 - Mathematical Result Transfer:** preserves operations and requested results when changing mathematical accounts, including an aggregation that loses local values.
- **C.29.2 - Computational Formulation:** constructs the computation and its approximation conditions; the balance test here checks its aggregate update.
- **B.5.MPC.R:** coordinates a changed question across physical, mathematical and computational accounts when revising the balance requires more than an arithmetic update.
- **E.18.2 - Transformation Flow Mathematical Description:** applies when the balance mathematically describes a selected transformation-flow structure or network.
- **C.11.DUA:** helps decide whether resolving a remaining discrepancy or term can improve the available action enough to justify the effort.


## Dependencies {#dependencies}

- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/A-3-3-TR#root for state change, spec://ai.lev/fpf-spec/contract/C-29-1#root for aggregation, spec://ai.lev/fpf-spec/contract/C-29-2#root for computational preservation, spec://ai.lev/fpf-spec/contract/E-18-2#root for flow descriptions, and spec://ai.lev/fpf-spec/contract/C-11-DUA#root for further inquiry. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/C-29#root, spec://ai.lev/fpf-think-phy/contract/PHY-3#root, spec://ai.lev/fpf-think-phy/contract/PHY-6#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/C-29-BB
