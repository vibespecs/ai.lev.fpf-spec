# B.1.5.RS - Evaluate a Constituent Method Replacement in Its Encompassing Uses {#root}

<status stage="spec" state="work"/>

> Source: Anatoly Levenchuk, *First Principles Framework (FPF) - Core Conceptual Specification* (September 2026), `FPF-Spec.md` at https://github.com/ailev/FPF commit d131d30a44e7, licensed CC BY 4.0. Working sections of the pattern; its depth sections live in the source document named by the last line. See LICENSE.md for the list of changes.

> **Type:** Method pattern
> **Status:** Candidate

## B.1.5.RS:1 - Problem frame {#problem-frame}

Use this pattern when a constituent Method could be replaced, simplified or implemented differently and you need to know which encompassing uses remain possible. A faster check returns the same answer on familiar inputs but no longer exposes information another part needs. An approximation is adequate for ranking options but unsuitable for deciding whether a limit is exceeded.

Start with the direction of replacement and the practical gain sought. Ask: **“What do the receiving wholes rely on, and does this candidate still supply it under their conditions?”**

The first useful result is a bounded substitution decision: the uses preserved, uses needing adaptation or restriction, and uses for which the replacement is incompatible or unresolved. One decisive comparison may be enough. Do not perform a new trial when an available argument or known counterexample settles the decision.

Use B.1.5.EW first if the constituent and its encompassing uses are unclear. If only the wording or diagram changes and the performed Method remains unchanged, check that representation's correspondence instead. If the replacement supplies an entire standalone Method, use the relevant fit and choice Methods; this pattern contributes only the constituent-in-whole question.

## B.1.5.RS:2 - Problem {#problem}

Local adequacy does not establish substitutability. The whole can depend on output meaning, intermediate interactions, order, timing, recoverability or resource demand that a local comparison omitted. A shared constituent can satisfy one whole and fail another.

The opposite failure is to demand that every internal detail remain identical. This prevents useful replacement even when the receiving work does not depend on that detail. The preservation question must come from the actual use.

## B.1.5.RS:3 - Forces {#forces}

- A local gain can remove a contribution needed elsewhere.
- Several uses may require different guarantees from the same constituent.
- Simplification saves effort when its lost detail is irrelevant to the receiving action.
- Strong evidence can be expensive; a bounded argument or counterexample may already settle the next move.
- A common replacement reduces maintenance, while separate variants can preserve otherwise incompatible uses.
- Method identity, description correspondence and performance evidence answer different questions.

## B.1.5.RS:4 - Solution {#solution}

Compare the candidate against what the encompassing work needs, then carry the changed contribution through that work. State the direction and conditions of the result.

### B.1.5.RS:4.1 - Name the proposed change {#name-the-proposed-change}

Identify the current constituent, its candidate replacement and the gain: for example, reduced delay, effort or dependence on a scarce specialist. State what changes in the operation, its inputs, outputs, interactions or realization.

Keep a proposed replacement separate from one already performed. Use A.3.1 to settle any needed identity claim: exposing a hidden step, changing an implementation within an admitted variation and proposing another Method need not have the same answer.

### B.1.5.RS:4.2 - Recover the receiving wholes {#recover-the-receiving-wholes}

Identify the encompassing Methods or work arrangements whose use can change. Follow an indirect use through the intermediate whole while it affects the decision. Include a second receiving use when the constituent is shared; local success in the first use is not evidence for the second.

This is a search bounded by the intended replacement. If the actual users cannot be recovered, restrict adoption to the known uses or return the missing use information that prevents a broader decision. Do not require an inventory of all imaginable uses.

For each relevant whole, recover:

- what it supplies or assumes at the constituent's entry;
- what result or interaction it needs from the constituent;
- timing, ordering, coordination and resource conditions that affect this use;
- what variation or loss it can tolerate.

Plain statements are sufficient when they make the comparison executable. Use an existing interface or formal contract when it already states these conditions.

### B.1.5.RS:4.3 - Compare the contribution under those conditions {#compare-the-contribution-under-those-conditions}

Apply the proposed constituent to the receiving conditions. Follow what it supplies through the affected part of the whole, including an interaction before final output when the whole relies on it.

Choose an argument, available observations, calculation or trial that can discriminate the decision at proportionate cost. A known violation can reject a general replacement without testing every possible input. A successful example can reveal a usable construction but does not automatically support all inputs.

When an approximation is proposed, state the property preserved for the receiving use: a bound, ordering, feasible action, specified error or other needed consequence. Equal rounded answers on one example do not establish preservation of a different property.

If the same implementation must serve several wholes simultaneously, examine their joint demands. Separate success under incompatible settings is not one shared implementation. Compare retained variants or changed coordination where that is useful.

### B.1.5.RS:4.4 - Classify the replacement by use {#classify-the-replacement-by-use}

| Comparison result | What can follow |
| --- | --- |
| The needed contribution and conditions are preserved. | Adopt the replacement for that use at the supported scope. |
| Preservation holds only under a narrower condition. | Restrict use to that condition and retain a suitable alternative elsewhere. |
| An adapter or changed combination can restore the needed contribution. | Treat that adaptation as part of the candidate and check its full burden and behavior. |
| A required contribution is lost. | Reject the replacement for that whole, change the requirement through the relevant decision, or choose another candidate. |
| Information does not distinguish compatibility from failure. | Keep the uncertainty bounded and obtain more only if it can change a worthwhile next action. |

This is a directed conclusion. Replacing A by B in one use does not show that A can replace B, that they are the same Method, or that B is preferable in all uses.

### B.1.5.RS:4.5 - Adopt or retain alternatives {#adopt-or-retain-alternatives}

Choose at the supported scope, accounting for adaptation, learning, operation and maintenance costs. Retain separate variants when their different strengths justify the burden; a single universal replacement is not required.

For an ongoing operation, use its ordinary rules for introducing change and retaining continuity. State the condition that would require reconsideration: changed inputs, another receiving whole, a tighter timing limit, lost support or a newly relevant result property. No separate certificate or trial is required merely to record that an existing basis was sufficient.

Return the decision in the form its receiver needs. Where the conclusion is only recognition of a plausible substitute, say so. A claim of guaranteed preservation needs the argument or assurance appropriate to that claim under B.3; a local decision under uncertainty uses C.11 and C.11.DUA.

## B.1.5.RS:7 - Conformance Checklist {#conformance-checklist}

- Are the constituent, candidate, replacement direction and intended gain clear?
- Have the relevant receiving wholes and their relied-on contributions been recovered?
- Does the comparison carry the changed contribution through each affected use?
- Are joint requirements examined when one realization must satisfy several uses together?
- Does the conclusion preserve its conditions and evidence reach?
- Are adaptation costs and a useful reconsideration condition included where they change adoption?

## B.1.5.RS:9 - Consequences {#consequences}

Useful replacements can be adopted where they work without silently breaking other wholes. An incompatibility can also expose a better architecture: different variants, an explicit interface or a changed combination.

The method requires knowledge of receiving uses. Its cost grows with meaningful differences among them, not necessarily with the number of documents or callers. Reuse one comparison across uses only when their relevant conditions and relied-on contribution match.

## B.1.5.RS:12 - Relations {#relations}

- B.1.5 and A.3.1 define Method composition, identity and replacement-claim distinctions.
- B.1.5.EW recovers constituent and encompassing work when those connections are not yet understood.
- B.5.RA and B.5.RR reconstruct and revise the argument on which preservation depends.
- C.29 governs a mathematical correspondence used in the comparison.
- C.30.LCA supplies control-specific conditions; C.30.ILC addresses resulting cross-scope architecture conflicts.
- C.11 and C.11.DUA govern the local decision and whether further investigation is useful.


## Dependencies {#dependencies}

- @fact:BUILDS-ON Builds on: spec://ai.lev/fpf-spec/contract/A-3-1#root, spec://ai.lev/fpf-spec/contract/B-1-5#root. @status:spec/done
- @fact:COORDINATES-WITH Coordinates with: spec://ai.lev/fpf-spec/contract/B-1-5-EW#root, spec://ai.lev/fpf-spec/contract/C-11-DUA#root, spec://ai.lev/fpf-spec/contract/C-29#root. @status:spec/done
- @fact:REFERENCED-BY Referenced by (computed from the Tables of Contents): spec://ai.lev/fpf-spec/contract/B-1-5-EW#root, spec://ai.lev/fpf-spec/contract/E-4-CM#root @status:spec/done

#source spec://ai.lev/fpf-spec/source/B-1-5-RS
