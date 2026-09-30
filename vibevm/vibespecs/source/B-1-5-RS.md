# B.1.5.RS - Evaluate a Constituent Method Replacement in Its Encompassing Uses: depth {#depth}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## B.1.5.RS:5 - Archetypal Grounding {#archetypal-grounding}

### B.1.5.RS:5.1 - Faster ordering in two encompassing uses {#faster-ordering-in-two-encompassing-uses}

A team proposes replacing a stable sorting Method with a faster one that need not preserve the input order of equal keys.

One whole prepares a table showing how many records occur at each key. Internal order among equal keys does not affect those counts. Subject to the remaining input and performance conditions, the candidate can supply that contribution.

Another whole schedules requests by priority while retaining arrival order among requests of equal priority. Its method first orders records by arrival and then stably orders them by priority. Replacing the second sort with the candidate can reverse equal-priority requests. The earlier arrival ordering no longer survives the composition.

An allowed reversal of two equal-priority records with different arrival times exposes the incompatibility with the required guarantee. This is a counterexample to unrestricted replacement, not a prediction that this implementation reverses every such pair; repeated random benchmarks cannot restore the missing guarantee. Options include retaining the stable Method or sorting by an explicit compound key of priority and arrival. The compound-key candidate has changed the operation; compare its behavior and cost before using it. The same “sorted by priority” description concealed different requirements of the two wholes.

### B.1.5.RS:5.2 - A bounded estimate and a threshold decision {#a-bounded-estimate-and-a-threshold-decision}

A constituent estimates a quantity with absolute error at most 2. A receiving whole only needs to distinguish alternatives separated by more than 4; the bound can support their ordering when both estimates satisfy it.

Another whole must decide whether the quantity exceeds 100. An estimate of 99 is insufficient: the admitted interval is 97 to 101 and crosses the threshold. A more accurate estimate or another decision rule is needed for that case. At an estimate of 95, the same error bound puts the whole interval below 100 and can settle that particular decision.

The change from “estimate the quantity” to “support this decision” makes the scope of replacement explicit. The threshold is stipulated in this constructed example; the pattern does not supply a rule for choosing it.

### B.1.5.RS:5.3 - A quicker observation during coordinated work {#a-quicker-observation-during-coordinated-work}

A group performs a movement sequence in response to a leader. A proposed observation Method uses occasional snapshots rather than continuous observation. It can suffice for an exercise in holding a static pose, but miss the cue that starts a coordinated transition.

Recover the timing actually needed by the encompassing sequence. If the snapshot interval exceeds the available response window, better interpretation of each snapshot cannot restore the missed cue. Keep more frequent observation, redesign the cue so it remains available, or change the coordinated sequence. Each proposal has a different burden and requires its own bounded comparison.

## B.1.5.RS:6 - Bias-Annotation {#bias-annotation}

The participant proposing a replacement often sees its local saving more clearly than the costs borne by other users. Recover the receiving requirements before choosing. A demand to preserve everything can conceal the opposite bias: treating familiar implementation detail as necessary even when no receiving use depends on it.

## B.1.5.RS:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Failure | Repair |
| --- | --- |
| One matching output stands in for preserved behavior. | Recover the timing, interaction or property actually used by the whole and test that contribution. |
| Compatibility in one whole is exported to every user. | Separate receiving uses and restrict the conclusion accordingly. |
| Every implementation detail must remain unchanged. | Preserve what the declared use relies on; permit changes outside that dependence. |
| An adapter is omitted from the candidate's cost or failure analysis. | Include the adapter in the candidate arrangement and follow the combined behavior. |
| A successful trial becomes an unconditional guarantee. | State its supported scope and establish stronger claims only when required. |

## B.1.5.RS:10 - Architectural Rationale {#architectural-rationale}

Substitution is a relation to a receiving use. A constituent's attractive property does not establish that relation. Recovering the whole's dependence avoids both unrestricted replacement and unnecessary preservation of detail.

When the receiving uses are already understood, the practitioner can begin with their requirements and compare the replacement directly. The result is a directed substitution decision across one or several uses, including a candidate that changes the whole to accommodate the new constituent.

## B.1.5.RS:11 - SoTA-Echoing {#sota-echoing}

[Mazo, Compton, Cohen and Ames](https://arxiv.org/html/2409.14902v1) formulate compositional contracts for layered control systems. Their contribution supports checking what adjacent functions assume and supply, including their different signal and timing models. This pattern uses that conditional-composition idea beyond the paper's system class; its formal guarantees are not generalized.

The stable-sort case illustrates contextual preservation by an elementary algorithmic counterexample. The bounded-estimate case applies ordinary interval reasoning. These are constructed cases of the common Method, not evidence that every constituent requires a formal contract or a numerical error bound.

For the practical question of substituting a constituent, a local performance benchmark is a serious alternative: it can reveal speed, cost and errors on its tested inputs. It does not establish that a replacement preserving totals also preserves arrival order, or that its error bound supports the required threshold decision. Sections 4.2–4.4 therefore select receiving-use conditions first, then derive or test only the preservation those uses need. The worked counterexample or an available bound can settle the stated question at less effort than an additional benchmark; an unresolved performance question can still justify a targeted trial.

Formal compositional contracts offer a stronger alternative where the constituent, interfaces and encompassing system fit their mathematical assumptions. The cited control theory makes those assumptions and guarantees explicit. This Method adapts that conditional comparison into ordinary statements of inputs, interactions, results and permitted losses; it keeps the formal proof when its additional assurance is useful and attainable. It does not treat every professional practice as a control-system instance. Reopen the selected comparison when an unmodeled interaction, shared realization, changed receiver or unsupported adaptation defeats the preservation claim. If one constituent cannot satisfy the relevant uses together, retain different variants or change the encompassing arrangement instead of declaring one universally better Method.


## B.1.5.RS:End {#end}
