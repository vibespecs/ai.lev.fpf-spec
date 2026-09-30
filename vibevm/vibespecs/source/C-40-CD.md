# C.40.CD - Develop Problems and Ways of Solving Them Together: depth {#depth}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Depth sections of the pattern; the working sections are in the contract document of the same id. See LICENSE.md for the list of changes.

## C.40.CD:5 - Archetypal Grounding {#archetypal-grounding}

The following constructed cases supply their task conditions and ordinary subject operations. They demonstrate the reasoning and its limits.

### C.40.CD:5.1 - A mixed transfer leaves a narrower comparison available {#a-mixed-transfer-leaves-a-narrower-comparison-available}

An investigation requires each error/non-error comparison to share both setup and temperature regime. An existing grouping operation uses setup alone. The permitted target records are:

| Record | Outcome | Setup | Temperature |
| --- | --- | --- | --- |
| T1 | Error | S1 | Warm |
| T2 | Acceptable | S1 | Cool |
| T3 | Error | S2 | Warm |
| T4 | Acceptable | S2 | Warm |

The source operation returns T1–T2 and T3–T4. Comparing those outputs with the target rule exposes the first pair's temperature mismatch.

The changed local problem is to return eligible pairs and expose where no comparison is supported. An available filtering operation adds temperature to the grouping key. It returns T3–T4 and no eligible S1 pair. This operation constructs the target comparison; repeating the old setup-only grouping would preserve the mismatch.

The result permits the S2/warm comparison if it serves the investigation. The S1 question remains open. A next inquiry can seek a comparable S1 record when obtaining it could change the needed explanation; alternatively, receiving work can use the narrower result or stop. The original source operation retains its uses where setup alone was the applicable rule.

The grouping has established eligibility for comparison. A causal explanation would need the separate reasoning and observations for that claim.

### C.40.CD:5.2 - An obstruction changes the mathematical question {#an-obstruction-changes-the-mathematical-question}

A scheduling model represents pairwise conflicts by the finite undirected path A-B-C-D. There are no capacity or precedence conditions in this model. Assigning A and C to session 1, B and D to session 2 satisfies its conflicts.

A new conflict A-C creates the triangle A-B-C. Applying two-coloring now exposes an odd cycle. Two sessions are impossible under the retained pairwise-conflict model.

That result supports the next mathematical question: what is the least number of sessions? The triangle requires at least three. The assignment A=1, B=2, C=3, D=1 satisfies every edge, so three suffice and are minimal. The obstruction and construction together answer the new question.

If the receiving project actually has only two sessions, the new mathematical answer identifies a resource mismatch. Receiving work must change a real conflict condition, obtain another session or accept that the stated assignment cannot be supplied. Merely asking the easier resource question has not removed that requirement.

The successful three-session construction opens a further question when more conflicts are expected: which additions remain compatible with three sessions? Adding A-D invalidates the old assignment because A and D both use session 1. Retain A=1, B=2 and C=3, and move D to session 2. This changed construction satisfies all five conflicts.

If B-D is then added as well, every pair among the four vertices conflicts. Four sessions are now necessary, and assigning one vertex to each session attains that bound. The successful construction has led to a new question, a local repair and then a limit on that repair. These results distinguish which anticipated conflicts can be accommodated with three sessions and which require changing the allocation conditions.

### C.40.CD:5.3 - A physical invariant replaces a timed operation {#a-physical-invariant-replaces-a-timed-operation}

A device should dispense 40 cm³ from a reservoir. An earlier constant-flow model used `V = q t`; with `q = 20 cm³/s`, it prescribed two seconds. The receiving situation has unknown time-varying outflow, so that duration no longer determines the volume.

The reservoir has constant cross-sectional area `A = 10 cm²`, starts at height `h₀ = 15 cm` and has no inflow or leakage. The supplied model treats the level reading and shutoff as ideal. Conservation and geometry give the dispensed volume:

`V = A(h₀ − h)`.

The changed construction asks which level corresponds to the required volume. It gives `h = 15 − 40/10 = 11 cm`. The new operating rule is to stop outflow when that level is reached. At that event the model gives 40 cm³, independently of the outflow's variation before it. If outflow stops earlier, the desired level is never reached; the volume relation alone supplies no completion guarantee.

This result connects physical conservation, a mathematical invariant and an event-based operating rule. Realizing it requires usable level observation and shutoff through C.16 and C.29.3. This supplies a design result under the model's premises.

Suppose receiving work also requires completion within eight seconds. The level rule has left that condition open. A supplied bound `q(t) ≥ 5 cm³/s` until the target level makes the accumulated outflow at least `5t`, so 40 cm³ is reached within eight seconds under the same ideal model. If no such flow support is available, keep the deadline unresolved or change the physical arrangement.

## C.40.CD:6 - Bias-Annotation {#bias-annotation}

An attractive new question can make a partial result look like completion of the receiving need. Keep the old condition at the point where the new result is used. Conversely, fixation on the original formulation can hide a useful invariant, obstruction or intermediate operation. Examine what that result permits before discarding it.

## C.40.CD:8 - Common Anti-Patterns and How to Avoid Them {#common-anti-patterns-and-how-to-avoid-them}

| Misuse | Repair |
| --- | --- |
| Repeating a source operation after a target condition has changed. | Locate the affected contribution and examine a retained or changed operation on the target. |
| Calling the easier question solved a completion of the original need. | Show which requirement the new result answers and which remains open. |
| Generating challenges whose meanings or success conditions cannot be applied. | Repair the formulation; distinguish meaningful unknown feasibility from an invalid challenge. |
| Retaining a description of an attractive result without the construction needed to continue. | Preserve the usable material and explanation for the proposed next operation. |
| Trying every problem–way combination. | Select a transfer for the contribution its attainable result could make at the available cost. |
| Treating a passed artifact as an acquired skill. | Recover the receiving operation, tool and preparation needed for use or adaptation. |

## C.40.CD:10 - Architectural Rationale {#architectural-rationale}

Problem and operation development constrain one another. A changed condition can invalidate a constituent of the way; a new intermediate result can make a different question answerable. Keeping both directions explicit permits local repair while preserving the receiving need.

B.5.QD constructs the question and C.39.RO constructs an operation for changed or combined use. This Method coordinates their results through target application and the next decision. Ordinary C.40 variation can finish under one fixed question. The coupled Method is useful when the question itself develops or a subsidiary problem must be constructed to progress.

The mathematical obstruction, restricted record comparison and physical invariant have different grounds. Their common contribution is the connection between a changed question, the operation that addresses it and the use its result enables. Subject Methods establish the respective proof, comparison eligibility and physical conditions.

An automated problem generator supplies one implementation of problem construction. Its representation, policy encoding and evaluation thresholds determine which transfers it can try. For people and teams, availability and acquisition of the needed operations enter the same coordination through different means and costs.

## C.40.CD:11 - SoTA-Echoing {#sota-echoing}

The selected line combines constructive problem development, operation reuse and target examination. Compare it with keeping the target fixed and improving a sufficient existing way: that cheaper alternative is preferred when it supplies the wanted result without developing a new question.

[POET v3](https://arxiv.org/html/1901.01753v3), §3, supplies a concrete paired environment/agent construction with environment generation, optimization and cross-environment transfer. Adapt those connections in :4.2–4.5. Its fixed thresholds and copying of policy parameters belong to that computational implementation.

[Enhanced POET](https://arxiv.org/html/2003.08536v1), §3 and appendices A.1/A.4, distinguishes environment encoding from behavioral characterization and changes when costly transfer adaptation is attempted. Adapt characterization for the actual transfer choice and attention to adaptation cost in :4.6. A policy that skips adaptation after poor direct transfer is a bounded economy; an intelligible target-specific adaptation can warrant a different choice.

[LLM-POET](https://arxiv.org/html/2406.04663v1), §§2–4, changes the environment generator while retaining the need to make its generated representation usable in the environment. Adapt that validity condition in :4.2. Its reported performance comparison has substantial uncertainty and concerns the tested generators and environments.

[Environment Evolution for Terminal Agents](https://arxiv.org/html/2609.04128v1), §§3–4, develops tasks through changed situations, operations and sequence length. It realizes those edits as environments and checks solvability and rejection of an empty solution separately. Adapt the constructive connection between a proposed task and its usable examination. The preprint's difficulty account depends on a reference distribution and modeling assumptions; it supplies no observer-independent scale for all problems.

The worked comparisons show why the coupled result can be worth the extra operation. Setup-only reuse produces an invalid pair; adding temperature supplies one usable comparison and identifies the remaining need. Repeating two-coloring cannot supply an impossible assignment; its obstruction supports a minimal-resource question. Reusing a duration loses the volume condition under variable flow; a level construction recovers it while exposing the separate completion-time question.

Reopen the Method's use when the proposed problem cannot be interpreted or examined, an available operation already supplies the whole wanted result more affordably, or target use reveals a consequential condition that the construction omitted.


## C.40.CD:End {#end}
